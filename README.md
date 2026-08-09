<p align="center">
  <img src="./assets/masthead.svg" alt="Patrick Hall. Terminals, networks, and systems." width="100%">
</p>

<p align="center">
  <a href="https://phall.io">phall.io</a>&nbsp;&nbsp;/&nbsp;&nbsp;
  <a href="https://phall.io/writing">writing</a>&nbsp;&nbsp;/&nbsp;&nbsp;
  <a href="https://github.com/phall1?tab=repositories&type=source">all source</a>
</p>

---

I build terminals and the machinery around them, mostly in Rust and Zig. The
thread through most of it: an agent is a first-class user of a terminal now,
not something you paste output into. That changes what the terminal has to be.

### terminals

**[phux](https://github.com/phall1/phux)** &nbsp;[![](https://img.shields.io/github/v/release/phall1/phux?style=flat-square&label=&labelColor=131316&color=2c2c31)](https://github.com/phall1/phux/releases/latest)&nbsp; <sub>`rust`</sub>
A terminal multiplexer, like tmux — shells live in a background server, you split them into panes, you detach, everything survives. The difference is what a pane *is*: a real terminal emulator inside the server that anything can attach to, so the bundled TUI, a shell script, and an agent all hold the same live pane. It records its own demos too — `phux rec`, no asciinema, no ffmpeg.

**[phux-cockpit](https://github.com/phall1/phux-cockpit)** &nbsp;[![](https://img.shields.io/github/v/release/phall1/phux-cockpit?style=flat-square&label=&labelColor=131316&color=2c2c31)](https://github.com/phall1/phux-cockpit/releases/latest)&nbsp; <sub>`zig`</sub>
A native macOS spatial runtime for phux — up to 32 terminals in one GPU surface, each owning its own PTY, emulator, and scrollback, arranged as a pane tree per tab. A single `resolve()` over that tree is the only source of truth for geometry, shared by the painter, the hit-test tree, and the PTY sizing pump. Splitting, focusing, and resizing never restart a process.

### instruments

**[token-tach](https://github.com/phall1/token-tach)** &nbsp;[![](https://img.shields.io/github/v/release/phall1/token-tach?style=flat-square&label=&labelColor=131316&color=2c2c31)](https://github.com/phall1/token-tach/releases/latest)&nbsp; <sub>`zig`</sub>
A macOS menu-bar tachometer for coding-agent token burn. It reads the session ledgers your agents already write — no proxy, no account, no telemetry — and turns them into an instrument: limit-weighted tokens/minute as the needle, a predicted wall-clock time you hit a limit, projected from the slope of the vendors' own utilization numbers rather than guessed capacities, and a per-agent split so the number resolves into *which* one is spending it.

**[phbv](https://github.com/phall1/phbv)** &nbsp;[![](https://img.shields.io/github/v/release/phall1/phbv?style=flat-square&label=&labelColor=131316&color=2c2c31)](https://github.com/phall1/phbv/releases/latest)&nbsp; <sub>`go`</sub>
A terminal UI for [beads](https://github.com/gastownhall/beads). It talks to the `bd` CLI exclusively over `bd … --json` and never touches the Dolt store underneath, with golden tests pinning that boundary — so a `bd` upgrade fails CI instead of silently breaking the UI.

### systems

**[cyrs](https://github.com/phall1/cyrs)** &nbsp;[![](https://img.shields.io/github/v/release/phall1/cyrs?style=flat-square&label=&labelColor=131316&color=2c2c31)](https://github.com/phall1/cyrs/releases/latest)&nbsp; <sub>`rust`</sub>
A compiler front end for Cypher and GQL: lex, parse, type-check, lint, format, and lower to a logical plan IR. It deliberately stops there — executing the query is the database's job. Ships as a library, a CLI, and an LSP server.

**[fella](https://github.com/phall1/fella)** &nbsp;[![](https://img.shields.io/github/v/release/phall1/fella?style=flat-square&label=&labelColor=131316&color=2c2c31)](https://github.com/phall1/fella/releases/latest)&nbsp; <sub>`zig`</sub>
Network containment and identity rotation for hostile networks. All traffic is forced through a WireGuard tunnel inside a dedicated netns with fail-closed iptables; identity artifacts rotate per session. Most tools in this space are shell scripts wrapped in sudo — this one compiles, cross-compiles to bare metal, and has real integration tests.

### install

```sh
brew tap phall1/tap
brew install phux phui
brew install --cask phux-cockpit token-tach phbv
```

`cyrs` is on crates.io: `cargo install cyrs-cli`

### also

- [phui](https://github.com/phall1/phui) — a GitHub TUI for PRs, issues, diffs, and Actions. A fork of [@kitlangton/ghui](https://github.com/kitlangton/ghui) that publishes standalone binaries through the tap, so there's no Bun or npm at runtime.
- [opentui-browser](https://github.com/phall1/opentui-browser) — a Chromium surface for OpenTUI over the Kitty graphics protocol
- [opencode-worktree](https://github.com/phall1/opencode-worktree) — Claude Code-style `-w` worktrees for OpenCode
- [silent-weights](https://github.com/phall1/silent-weights) — embedding and extracting payloads from model weights, for AI supply-chain security research
- [dotfiles](https://github.com/phall1/dotfiles) — chezmoi-managed substrate with a `dot-doctor` health check

<p align="center"><sub><code>vibes all the way down</code></sub></p>
