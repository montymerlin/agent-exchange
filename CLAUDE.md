# CLAUDE.md — Compatibility Wrapper

Before doing anything else in this repo, Read `AGENTS.md` in full. It is the canonical instruction set for this repo; this file is a thin Claude compatibility wrapper and assumes you have read `AGENTS.md` first.

In Claude Code (CLI), an `@AGENTS.md` directive will expand recursively. In Cowork (desktop), that expansion is not reliable, so the explicit imperative above is required — do not skip it.

Claude-specific note:
- Claude tooling may still look for `CLAUDE.md` by default, which is why this file remains in the repo.

Core references:
- [AGENTS.md](AGENTS.md) — canonical agent instructions
- [GUIDE.md](GUIDE.md) — workshop guide and teaching material
- [DECISIONS.md](DECISIONS.md) — architectural decisions
- [ROADMAP.md](ROADMAP.md) — future directions
- [CHANGELOG.md](CHANGELOG.md) — narrative history
