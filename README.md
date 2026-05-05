# Share localhost. Get live feedback, instantly.

Built by Team SpecStory, makers of [Stoa](https://withstoa.com/sharelocalhost), so you can ship a half-finished feature, hand a friend a link, and hear what they actually thought without spinning up staging or shipping a PR preview. One command turns localhost into a public URL, your viewer leaves a voice memo on the page, and the transcript lands in your terminal ready for your agent.

<p align="left">
  <strong>Install the Stoa CLI ──▶ </strong>&nbsp;
  <a href="https://withstoa.com/sharelocalhost"><img src="https://img.shields.io/badge/CLI-Homebrew-blueviolet?style=flat-square" alt="Homebrew" style="vertical-align: middle;"></a>
  <a href="https://docs.withstoa.com/reference/cli#installation"><img src="https://img.shields.io/badge/Docs-Other%20ways%20to%20install-4f46e5?style=flat-square" alt="Other install options" style="vertical-align: middle;"></a>
</p>

<p align="left">
  <strong>Connect with us ───▶</strong>&nbsp;
  <a href="https://twitter.com/specstoryai"><img src="https://img.shields.io/badge/X-000000?style=flat-square&logoColor=white" alt="X" style="vertical-align: middle;"></a>
  <a href="https://www.linkedin.com/company/specstory"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" style="vertical-align: middle;"></a>
  <a href="https://withstoa.com"><img src="https://img.shields.io/badge/Site-withstoa.com-2a2520?style=flat-square" alt="Site" style="vertical-align: middle;"></a>
</p>

> 🎙️ **[Read the docs](https://docs.withstoa.com/sharelocalhost)** for the full reference, or jump straight to [installation](https://docs.withstoa.com/reference/cli#installation).

## How It Works

```
 Your dev server         Stoa CLI                 Public viewer
 ───────────────         ────────                 ─────────────
                                                  (no login, no install)

 localhost:PORT  ──►  stoa sharelocalhost  ──►  https://abc123.share.withstoa.com
                      (live for 1 hour)         (records voice memo)
                              ▲                            │
                              └──────  transcript  ────────┘
                                      ~/.stoa/feedback/
                                      (agent-ready)
```

## Workflow

1. **Install.** Run `brew tap specstoryai/tap && brew install stoa`. One binary. A free Stoa account is required to share.
2. **Run one command.** `stoa sharelocalhost` lists your running dev servers. Pick one. You get a public URL back, live for one hour.
3. **Hand over the link.** Viewers open it on their own machine. A small button sits in the corner of every page. They click, record a voice memo, send.
4. **Hear the feedback.** Audio and transcript stream back to your terminal and drop into `~/.stoa/feedback/` next to the original recording.
5. **Pipe it to your agent.** Hand the transcript file straight to Claude Code, Cursor, Codex, or whatever's building the next change.

## Installation

| Platform | Source | Install | Min Version |
|----------|--------|---------|-------------|
| **macOS / Linux (Homebrew)** | Closed | `brew tap specstoryai/tap`<br/>`brew update`<br/>`brew install stoa` | v0.7.0+ |
| **Direct download** | Closed | See [docs.withstoa.com/reference/cli#installation](https://docs.withstoa.com/reference/cli#installation) | v0.7.0+ |
| **Other package managers** | Closed | See [docs.withstoa.com/reference/cli#installation](https://docs.withstoa.com/reference/cli#installation) | v0.7.0+ |

> [!NOTE]
> A free [Stoa](https://withstoa.com/sharelocalhost) account is required to share. Sign in once, then `stoa sharelocalhost` from any project.

### Quick start

```bash
# 1. Install
brew tap specstoryai/tap
brew install stoa

# 2. Start your dev server (anything works)
npm run dev      # or pnpm dev, bun dev, rails s, uvicorn, etc.

# 3. Share it
stoa sharelocalhost          # interactive: pick from running servers
stoa sharelocalhost 3000     # or pass the port directly

# → https://abc123.share.withstoa.com
# Listening for feedback. Press Ctrl+C to stop.
```

When a viewer records a voice memo, audio and transcript appear in your terminal and land in:

```
~/.stoa/feedback/
├── 2026-05-05T14-22-31_abc123.mp3
└── 2026-05-05T14-22-31_abc123.txt
```

Pipe the `.txt` straight to your agent of choice.

## More Than a Tunnel

ngrok and Cloudflare give you a public URL. `stoa sharelocalhost` gives you the URL **and** the feedback loop.

| | `stoa sharelocalhost` | ngrok | Cloudflare |
|---|:---:|:---:|:---:|
| Free account to share | ✅ | ✅ | ❌ |
| Voice memo capture | ✅ | ❌ | ❌ |
| Auto-transcription | ✅ | ❌ | ❌ |
| Agent-ready transcript file | ✅ | ❌ | ❌ |
| Feedback in your terminal | ✅ | ❌ | ❌ |
| WebSocket / HMR | ✅ | ✅ | ✅ |

A public URL is the start. The feedback loop is the point.

## The Bigger Picture ☁️

`stoa sharelocalhost` is the smallest piece of a much bigger loop. [**Stoa**](https://withstoa.com) runs the same loop across your whole team. Every meeting, every agent run, every change in the codebase, captured as it happens and kept next to the work. The full version is multiplayer AI for teams.

[See Stoa for teams →](https://withstoa.com)

## Documentation & Support

- 📚 **[Full Documentation](https://docs.withstoa.com)**: guides, reference, and API
- 🛠️ **[CLI Reference](https://docs.withstoa.com/reference/cli)**: every command and flag
- 🎙️ **[`stoa sharelocalhost` docs](https://docs.withstoa.com/sharelocalhost)**: deeper guide for this feature
- 🐛 **Report a bug or request a feature**: [open an issue](../../issues/new) in this repo. We triage and respond here.
- 📨 **Contact**: [hello@withstoa.com](mailto:hello@withstoa.com)

> [!TIP]
> This repo is the home for `stoa sharelocalhost` issues and feature requests. Found a bug, hit a rough edge, or have an idea for what should ship next? [Open an issue](../../issues/new) and we'll see it.

## Reviews & Feedback

Using `stoa sharelocalhost`? Tag [@specstoryai](https://twitter.com/specstoryai) on X with what you're shipping. We read everything.
