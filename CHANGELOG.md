# Changelog — Agentic Exchange Workshop

A narrative record of how this project evolves. Updated after significant work sessions, not per-commit. Focuses on the "why" and "what changed" rather than granular diffs.

---

## 2026-04-22 — Reframed Agent Exchange for the cross-host agent era

Updated the repo to teach a more future-friendly pattern. `AGENTS.md` is now the canonical instruction file, with `CLAUDE.md` reduced to a compatibility wrapper. The guide and README were also revised to present skills, plugins, and connectors as core reusable workflow concepts rather than Claude-only features. This change reflects a broader shift in the ecosystem: practical agent use is increasingly about building portable systems and reusable workflows, not just getting better at prompting inside one app.

---

## 2026-04-13 — GUIDE.md Enriched with Research Depth

Deepened GUIDE.md with content drawn from broader montymerlinHQ research — patterns, repos-and-tools registry, plan, and roadmap. Part 6 (Digital Brain) gained the Three-Space Architecture, soul-building details (soul.md + NEON-SOUL), core operating principles (Text > Brain, Structure is the API, Capture cheap / distill valuable), expanded QMD technical details, alternative tools (Khoj, Fabric), a Business Brain section, and further reading (Docling, life-system). Part 7 (Advanced Frontier) gained the three-layer memory model, the 6 Rs processing pipeline from Ars Contexta (with emphasis on the Reweave backward-pass), overnight memory consolidation from Claudia, a new multi-agent orchestration section covering Ruflo (swarm topologies, self-learning routing) and Egregore (context-as-DOM with lifecycle management), and expanded security patterns (least privilege, secret segregation, prompt injection defense, data classification). Quick Reference tables reorganized with a new Frontier & Orchestration section covering the newly referenced tools. The guide is now substantially richer while maintaining the progressive disclosure structure — beginners aren't overwhelmed, advanced readers get real depth.

---

## 2026-04-13 — GUIDE.md Created from Session #0

After the first Agent Exchange session (a calibration and mapping meetup with ~7 participants spanning beginner to advanced), created GUIDE.md as the core knowledge resource for the community. The guide progresses from absolute basics (what AI chat is, how prompting works) through intermediate concepts (Cowork, markdown, agentic scaffolding, disciplined workflows) to advanced topics (digital brains, memory frameworks, self-hosted AI, security). Real examples and insights from the session are woven throughout rather than appearing as separate meeting notes. Resource links to key repos and tools (QMD, Superpowers, MDPowers, Agentic Scaffold, OpenClaw, Obsidian, etc.) are layered in at each level. Updated README.md, CLAUDE.md to reference the new file.

---

## 2026-04-13 — Project Initialized

Set up the Agentic Exchange Workshop with an agentic scaffold: CLAUDE.md for agent instructions, README.md for human-facing documentation, DECISIONS.md for architectural choices, ROADMAP.md for future directions, CHANGELOG.md (this file) for narrative history, and .claude/settings.local.json for Claude Code configuration.

The scaffold serves double duty here — it organizes the project AND demonstrates the agentic patterns being taught in the workshop. Two initial decisions were logged: adopting the scaffold (Decision 001) and using the project as both materials repository and live demo (Decision 002).

The roadmap was seeded with near-term workshop modules (beginner intro to agentic AI, intermediate file system access, hands-on scaffold exercise) and future exploration ideas (MCP deep-dives, plugin creation, participant showcases).

<!-- Scaffold sources: keep-a-changelog (adapted to narrative style), bridging-worlds project patterns -->
<!-- Agentic Scaffold v0.1.0 | https://github.com/montymerlin/agentic-scaffold-plugin -->
