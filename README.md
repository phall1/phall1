<p align="center">
  <img src="./assets/masthead.svg" alt="Patrick Hall. Terminals, networks, and systems." width="100%">
</p>

<p align="center">
  <a href="https://phall.io">phall.io</a>&nbsp;&nbsp;/&nbsp;&nbsp;
  <a href="https://phall.io/writing">writing</a>&nbsp;&nbsp;/&nbsp;&nbsp;
  <a href="https://github.com/phall1?tab=repositories&type=source">all source</a>
</p>

---

Terminals, and the machinery around them. Mostly Rust, Zig, and Go.

### terminals

**[phux](https://github.com/no-phux/phux)** &nbsp;[![](https://img.shields.io/github/v/release/no-phux/phux?style=flat-square&label=&labelColor=131316&color=2c2c31)](https://github.com/no-phux/phux/releases/latest)&nbsp; <sub>`rust`</sub>
A terminal multiplexer. Shells live in a server, panes survive detach. Each pane is a real emulator that the TUI, a script, or an agent can hold at the same time. Lives in the [no-phux](https://github.com/orgs/no-phux/repositories) org with the rest of the ecosystem.

**[phux-cockpit](https://github.com/no-phux/phux-cockpit)** &nbsp;[![](https://img.shields.io/github/v/release/no-phux/phux-cockpit?style=flat-square&label=&labelColor=131316&color=2c2c31)](https://github.com/no-phux/phux-cockpit/releases/latest)&nbsp; <sub>`zig`</sub>
Native macOS front end for phux. Up to 32 terminals in one GPU surface, a pane tree per tab, one `resolve()` that owns all the geometry.

**[phig](https://github.com/phall1/phig)** &nbsp;[![](https://img.shields.io/github/v/release/phall1/phig?style=flat-square&label=&labelColor=131316&color=2c2c31)](https://github.com/phall1/phig/releases/latest)&nbsp; <sub>`rust`</sub>
tig, rebuilt. Commits, diffs, refs, blame, and stashes in the terminal. Read-only. Hands a commit, hunk, or line back over stdout, or as JSON.

### agents

**[blackbird](https://github.com/phall1/blackbird)** &nbsp;[![](https://img.shields.io/github/v/release/phall1/blackbird?style=flat-square&label=&labelColor=131316&color=2c2c31&filter=v*)](https://github.com/phall1/blackbird/releases/latest)&nbsp; <sub>`go`</sub>
Local-first coordination for humans and agents working the same repo. One daemon, SQLite, MCP and HTTP. Mail, inboxes, path leases, a tamper-evident event journal. Delivery plugins for Claude Code, OpenCode, and Pi.

**[token-tach](https://github.com/phall1/token-tach)** &nbsp;[![](https://img.shields.io/github/v/release/phall1/token-tach?style=flat-square&label=&labelColor=131316&color=2c2c31)](https://github.com/phall1/token-tach/releases/latest)&nbsp; <sub>`zig`</sub>
Menu-bar tachometer for coding-agent token burn. Reads the session ledgers agents already write. No proxy, no account, no telemetry.

**[phbv](https://github.com/phall1/phbv)** &nbsp;[![](https://img.shields.io/github/v/release/phall1/phbv?style=flat-square&label=&labelColor=131316&color=2c2c31)](https://github.com/phall1/phbv/releases/latest)&nbsp; <sub>`go`</sub>
A TUI for [beads](https://github.com/gastownhall/beads). Talks to `bd --json` and nothing underneath it. Golden tests pin the boundary.

### mac

**[friday](https://github.com/phall1/friday)** &nbsp;[![](https://img.shields.io/github/v/release/phall1/friday?style=flat-square&label=&labelColor=131316&color=2c2c31)](https://github.com/phall1/friday/releases/latest)&nbsp; <sub>`zig`</sub>
Menu-bar dictation. Hold a key, talk, let go. Parakeet runs locally and the text lands back in the app you were in. No cloud, no history.

**[zero-fret](https://github.com/phall1/zero-fret)** &nbsp; <sub>`swift`</sub>
A guitar and bass tuner for iOS that shows you a string, not a needle. MPM pitch detection, zero dependencies.

### systems

**[cyrs](https://github.com/phall1/cyrs)** &nbsp;[![](https://img.shields.io/github/v/release/phall1/cyrs?style=flat-square&label=&labelColor=131316&color=2c2c31)](https://github.com/phall1/cyrs/releases/latest)&nbsp; <sub>`rust`</sub>
A compiler front end for Cypher and GQL. Lex, parse, type-check, lint, format, lower to a plan IR, stop. Library, CLI, and LSP.

**[fella](https://github.com/phall1/fella)** &nbsp;[![](https://img.shields.io/github/v/release/phall1/fella?style=flat-square&label=&labelColor=131316&color=2c2c31)](https://github.com/phall1/fella/releases/latest)&nbsp; <sub>`zig`</sub>
Network containment for hostile networks. Everything through WireGuard in its own netns, fail-closed iptables, identity rotated per session.

**[polygres-sdk-effect](https://github.com/phall1/polygres-sdk-effect)** &nbsp;[![](https://img.shields.io/github/v/release/phall1/polygres-sdk-effect?style=flat-square&label=&labelColor=131316&color=2c2c31)](https://github.com/phall1/polygres-sdk-effect/releases/latest)&nbsp; <sub>`ts`</sub>
Effect-native SDK for [Polygres](https://polygres.com). Typed failures, cold streams for pagination, row writes that never silently retry.

### install

```sh
brew tap phall1/tap
brew install phux phig phui blackbird
brew install --cask phux-cockpit token-tach phbv friday
cargo install cyrs-cli
```

### also

- [phui](https://github.com/phall1/phui) — fork of [ghui](https://github.com/kitlangton/ghui) by [Kit Langton](https://github.com/kitlangton). Adds an Actions dashboard, Inbox/Stars/Projects, and handoff into phux.
- [opentui-browser](https://github.com/phall1/opentui-browser) — Chromium in OpenTUI over the Kitty graphics protocol
- [opencode-worktree](https://github.com/phall1/opencode-worktree) — `-w` worktrees for OpenCode
- [silent-weights](https://github.com/phall1/silent-weights) — hiding payloads in model weights, for supply-chain research
- [dotfiles](https://github.com/phall1/dotfiles) — chezmoi, plus a `dot-doctor`

<p align="center"><sub><code>vibes all the way down</code></sub></p>
