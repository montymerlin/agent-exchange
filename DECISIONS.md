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

---

## Decision 003: Teach cross-host agent workflows with AGENTS.md as canonical

**Status:** Accepted
**Date:** 2026-04-22

**Context:** The workshop was initially scaffolded around `CLAUDE.md` and Cowork-specific language because Claude was the clearest hands-on entry point at the time. Since then, the ecosystem has shifted. Agent Skills have been published as an open standard, Codex now treats skills as a first-class workflow layer, and the practical teaching need is no longer "how do I use one vendor's AI app?" but "how do I build portable, repeatable agent workflows across hosts?" This repo needs to model that shift directly.

**Decision:** Make `AGENTS.md` the canonical instruction file for this repo, keep `CLAUDE.md` as a thin compatibility wrapper, and update the teaching materials to frame skills, plugins, and MCP-style connectors as core concepts of the agentic era rather than Claude-only features. The guide should explicitly teach the difference between:

- skills as reusable workflow units
- plugins as packaging and runtime extension layers that may bundle skills plus other capabilities
- connectors or MCP servers as access bridges to external tools and data

The guide should also note the current market context as of April 22, 2026: Codex is unusually accessible because it is included in existing ChatGPT subscriptions and currently benefits from aggressive rollout and higher available limits, while Claude remains a major host with strong plugin and Cowork workflows. This comparison should be presented as a time-bound observation, not a permanent truth.

**Consequences:**
- The repo now teaches a more future-friendly pattern instead of hardcoding one host as the default mental model
- Participants can understand why skills and plugins matter as a maturity step from prompting toward reusable systems
- The workshop stays relevant even as the landscape shifts between Claude, Codex, and future hosts
- Current docs need careful wording so they stay useful without becoming a fragile pricing sheet

**Alternatives Considered:**
- Keep the repo Claude-first — easier in the short term, but increasingly misleading
- Rewrite the guide as fully tool-agnostic with no vendor examples — cleaner in theory, but less concrete for beginners
- Add a deep installation matrix — too detailed for the guide's teaching purpose right now

---

## Decision 004: Introduce nested folder-level AGENTS.md + TEMPLATE.md, starting with `modules/`

**Status:** Accepted
**Date:** 2026-05-18

**Context:** Research into current agent-instruction best practice (Anthropic Claude Code memory docs, OpenAI Codex AGENTS.md guide, the agents.md spec under the Linux Foundation, and GitHub's analysis of 2,500 real AGENTS.md files) converges on a three-layer pattern: root instructions for global rules, folder-level instructions for "when working in here" specialization, and concrete templates as exemplars to imitate. The repo currently demonstrates only layer one. Decision 002 commits us to making the project a live demo of what it teaches, so the gap between what the guide describes and what the repo embodies is itself a problem.

A second motivation: the ROADMAP already has three active workshop modules queued (intro to agentic AI, AI file system access, scaffold-your-own-project exercise). They have no home in the repo, which forces every authoring session to re-derive shape.

**Decision:** Introduce a `modules/` subfolder containing its own `AGENTS.md` (folder-scoped instructions) and `TEMPLATE.md` (the exemplar shape for a workshop module). Start with this one subfolder rather than building out the full nested structure at once, in keeping with the progressive-disclosure principle. Additional subfolders (e.g. `exercises/`, `sessions/`) can follow if and when the need is clear.

The folder-level `AGENTS.md` should specialize, not duplicate root guidance — naming conventions, module-specific structure, and the pointer to `TEMPLATE.md` live there. The root `AGENTS.md` keeps project-wide rules only.

**Consequences:**
- The repo now demonstrates the nested-instructions pattern instead of only describing it. GUIDE.md Part 4 has new material to point at.
- Future workshop modules have a known shape and home — authors (human or agent) imitate `TEMPLATE.md` rather than reinventing structure.
- Two non-obvious caveats need to be taught alongside the pattern. In Claude Code, nested `AGENTS.md` (or `CLAUDE.md`) is *lazy-loaded* — it only enters context when the agent reads a file inside that folder. So a rule like "when drafting a module, do X" only fires if the agent is operating inside `modules/`. In OpenAI Codex, the load is eager from project root down to cwd, with a 32 KiB combined cap. Both behaviours are worth covering in the guide.
- For rules that must trigger whenever certain files are touched regardless of cwd, the right escape hatch is `.claude/rules/*.md` with `paths:` frontmatter — deferred for now (see Proposal 3, not yet decided).
- Root `AGENTS.md` needs a minimal update so its Directory Structure block reflects the new folder.

**Alternatives Considered:**
- Build out the full nested structure now (`modules/`, `exercises/`, `sessions/`, `decisions/TEMPLATE.md` etc.) — premature; violates progressive disclosure; better to ship one working example and iterate.
- Add only `TEMPLATE.md` files without folder-level `AGENTS.md` — misses half the pattern; the folder-level file is what tells the agent the template exists and when to use it.
- Use `.claude/rules/` path-scoped rules instead of nested `AGENTS.md` — more powerful for some cases, but Claude-specific. Nested `AGENTS.md` is cross-host (Codex, Claude Code, and the 60k+ projects on the agents.md spec all honour it). Path-scoped rules can be added later as a complementary mechanism.

<!-- Scaffold sources: Michael Nygard ADR proposal (2011), Keeling & Runde sustainable ADRs (IEEE Software), bridging-worlds DECISIONS.md pattern -->
<!-- Decision 004 research sources: code.claude.com/docs/en/memory, developers.openai.com/codex/guides/agents-md, agents.md, github.blog (2,500-repo analysis) -->
<!-- Agentic Scaffold v0.1.0 | https://github.com/montymerlin/agentic-scaffold-plugin -->
