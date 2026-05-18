# AGENTS.md — `modules/`

Folder-scoped instructions for the workshop modules directory. Specializes the root [AGENTS.md](../AGENTS.md); does not repeat it.

## What this folder is for

Self-contained workshop modules — short, focused teaching units used in Agent Exchange sessions. Each module stands alone (a participant should be able to pick one up cold and work through it), but modules can build on each other when sequence helps.

## What belongs here

- Beginner, intermediate, and advanced teaching modules
- Hands-on exercises with clear setup, walkthrough, and try-it-yourself steps
- Concept explainers that need worked examples (not pure reference material)

## What doesn't belong here

- Session notes from specific meetups — those are ephemeral and belong elsewhere (TBD; see [ROADMAP](../ROADMAP.md))
- The core curriculum narrative — that lives in [GUIDE.md](../GUIDE.md), which is the progressive reading path. Modules are bite-sized; the guide is the connective tissue.
- Personal scratch work, drafts, or unfinished sketches

## How to add a module

1. Open [TEMPLATE.md](TEMPLATE.md) and read it through before drafting. The shape matters more than the rule list — match the template's structure rather than improvising.
2. Copy `TEMPLATE.md` to a new file named `NNN-topic.md`, where `NNN` is the next sequential number (zero-padded, e.g. `001-what-is-agentic-ai.md`) and `topic` is kebab-case.
3. Fill in the frontmatter honestly. The `level`, `est_time`, and `prerequisites` fields are what let participants self-select.
4. Keep it tight. A good module is short enough to work through in one sitting and concrete enough that someone can teach it from the file alone.

## Naming

- Files: `NNN-topic.md` — zero-padded sequence + kebab-case topic
- Sequence numbers are stable once published. Reordering happens via frontmatter, not by renumbering files.

## Conventions

- Every module has a real "try it yourself" section. If a module is pure exposition, it probably belongs in [GUIDE.md](../GUIDE.md) instead.
- Use real, copyable commands and snippets. Avoid pseudocode.
- Link outward to existing repos and tools rather than re-explaining them.
- A module without an attributed author and date is incomplete — workshop content is peer-to-peer; provenance matters.

## A note on how this file loads

This folder-level `AGENTS.md` follows the nested instructions pattern documented in Decision 004. In OpenAI Codex, it loads alongside the root `AGENTS.md` whenever the working directory is inside `modules/`. In Claude Code, it loads *lazily* — only once the agent reads a file inside this folder. If you're authoring a new module from outside `modules/`, the rules here may not be in context yet; reference [TEMPLATE.md](TEMPLATE.md) explicitly to be sure.

## References

- [TEMPLATE.md](TEMPLATE.md) — the exemplar to copy when drafting a new module
- [../AGENTS.md](../AGENTS.md) — project-wide instructions
- [../GUIDE.md](../GUIDE.md) — the connective curriculum these modules slot into
- [../DECISIONS.md](../DECISIONS.md) — Decision 004 covers why this folder exists

<!-- This file demonstrates the nested AGENTS.md pattern. See Decision 004 and GUIDE Part 4. -->
