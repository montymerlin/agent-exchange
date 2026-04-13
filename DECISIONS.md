# Decisions — Agentic Exchange Workshop

Architectural decisions for this project, logged in a lightweight ADR (Architectural Decision Record) format. Each entry captures the context, the choice made, and its consequences — creating a searchable trail that survives memory loss and team changes.

**Format:** Each decision gets a sequential number, a status, and four sections: Context, Decision, Consequences, and (optionally) Alternatives Considered.

---

## Decision 001: Adopted agentic scaffold

**Status:** Accepted
**Date:** 2026-04-13

**Context:** The Agentic Exchange Workshop needs structured conventions for AI-assisted development from the start. The workshop itself teaches agentic concepts, so the project folder should exemplify those concepts — making the scaffold both infrastructure and teaching material.

**Decision:** Adopted the Agentic Scaffold pattern — a set of coordinated files (CLAUDE.md, README.md, DECISIONS.md, CHANGELOG.md, ROADMAP.md, .claude/) that establish conventions, document decisions, and separate human-facing from agent-facing documentation.

**Consequences:**
- Agents working in this repo have clear instructions from session one
- The project folder itself becomes a live demo of the patterns being taught
- Architectural choices are logged and searchable, not buried in commit messages or lost in conversation
- The scaffold adds a small number of files, but each serves a distinct purpose
- Conventions can evolve — update CLAUDE.md and log the change here

**Alternatives Considered:**
- No scaffold (rely on README alone) — insufficient for agent workflows, and misses the teaching opportunity
- Heavy framework (full ADR tooling, multiple config files) — premature for a workshop project
- Single mega-file — conflates human and agent audiences, becomes unwieldy

---

## Decision 002: Workshop as both materials and live demo

**Status:** Accepted
**Date:** 2026-04-13

**Context:** The workshop needs deliverables (slides, handouts, exercises) AND a way to demonstrate agentic scaffolding in practice. Maintaining a separate demo repo adds overhead and disconnects the teaching from the doing.

**Decision:** Use this project folder as both the workshop materials repository and the live demo. The agentic scaffold files (CLAUDE.md, DECISIONS.md, etc.) serve double duty — they organize the project AND illustrate the concepts being taught.

**Consequences:**
- Every file change is a potential teaching moment
- Participants can clone or browse the same folder they're learning about
- Changes need to be exemplary — sloppy commits or unclear decisions undermine the teaching
- Materials and demo evolve together, staying in sync naturally

**Alternatives Considered:**
- Separate demo repo — adds maintenance burden, risks drift between materials and demo
- Slides-only approach — misses the hands-on, "see it working" dimension
- Pre-built demo with no live changes — less engaging, doesn't show the workflow in action

<!-- Scaffold sources: Michael Nygard ADR proposal (2011), Keeling & Runde sustainable ADRs (IEEE Software), bridging-worlds DECISIONS.md pattern -->
<!-- Agentic Scaffold v0.1.0 | https://github.com/montymerlin/agentic-scaffold-plugin -->
