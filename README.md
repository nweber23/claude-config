# My Agent Setup

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A reusable behavioral-contract template for AI coding agents (Claude Code, and anything else that reads `AGENTS.md`).

Default agent behavior is generic. This repo is an opinionated, drop-in contract — question assumptions, keep solutions simple, stay scoped to the request, verify against success criteria — so an agent behaves consistently across your projects instead of re-deriving conventions every session.

## Principles at a glance

| Principle | Rule |
|---|---|
| Always think instead of assume | Question assumptions, present trade-offs, ask before guessing. |
| Simplicity is key | No over-engineering, no unnecessary abstractions, no unrequested features. |
| Code changes | Stay scoped to the request; flag (don't silently fix) unrelated issues. |
| Goal oriented | Turn every request into a verifiable success criterion. |
| Rules | Defer to the docs in `Docs/` (if present); ask when a rule is undocumented or unclear. |

Full text lives in [`CLAUDE.md`](CLAUDE.md).

## What's in this repo

```
.
├── CLAUDE.md            # Core behavioral principles
├── AGENTS.md            # Identical copy, for tools that read this filename instead
├── Docs/                # Optional — rule docs referenced by CLAUDE.md
│   ├── COMMIT.md          # Commit message format and rules
│   ├── SECURITY.md        # Vulnerability, dependency, and high-risk-change handling
│   └── COMMUNICATION.md   # Response verbosity and tone
└── Examples/             # Reserved for example agent interactions (currently empty)
```

## Usage

1. Copy `CLAUDE.md` (and `AGENTS.md`, if your tooling reads that filename) into the root of your project. `Docs/` is optional — only bring it along if you want these specific rules.
2. Adjust the rules to fit your team — these are a starting point, not a fixed standard.
3. Add your own project-specific docs under `Docs/` too — coding standards, style guides, testing conventions, anything domain-specific. `CLAUDE.md`'s "Rules" section expects project rules to live there, not just the ones shipped in this template.

## License

MIT — see [LICENSE](LICENSE).
