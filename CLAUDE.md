# CLAUDE.md — Agentic Exchange Workshop

A peer-to-peer learning and experimentation forum for exploring how people are practically using AI — from simple productivity workflows to advanced agentic systems and custom technical setups.

## Project Identity

- **Name:** Agentic Exchange Workshop
- **Stack:** Generic (markdown documents, workshop materials, exercises, demo files)
- **Purpose:** Workshop materials + live demo project for teaching agentic AI concepts, from beginner to intermediate

## Directory Structure

```
Agentic Exchange Workshop/
├── README.md              # Human-facing overview
├── GUIDE.md               # Core knowledge resource — beginner to advanced
├── CLAUDE.md              # Agent instructions (this file)
├── DECISIONS.md           # Architectural decision log
├── ROADMAP.md             # Future directions and ideas
├── CHANGELOG.md           # Narrative change history
└── .claude/
    └── settings.local.json  # Claude Code project config
```

## Key Conventions

### Naming
- Use descriptive, consistent naming throughout
- Files: kebab-case for documents (e.g., `session-notes.md`), descriptive names for workshop materials
- Workshop materials should be clearly numbered or labeled for session order

### Commits
- Concise message focusing on "why" not "what"
- Reference decisions by number when relevant (e.g., "per Decision 003")

### Documentation
- README.md is the human-facing overview — keep it current
- CLAUDE.md (this file) is the agent instruction set — update when conventions change
- DECISIONS.md logs architectural choices — add entries before implementing significant changes
- ROADMAP.md captures future directions — items flow to DECISIONS.md when evaluated
- CHANGELOG.md tracks evolution narratively — update after significant work sessions

### Workshop-Specific Conventions
- Materials should progress from beginner to intermediate concepts
- Each session or module should be self-contained enough to stand alone
- Exercises should be hands-on and demonstrable in real time
- Use this project itself as a live example wherever possible

## Agent Boundaries

### Do
- Read this file first on every session
- Follow the conventions above
- Log decisions before implementing them
- Capture future ideas in ROADMAP.md
- Update CHANGELOG.md after significant work
- Ask before any action that affects external systems
- Treat this project as both workspace AND demo — changes should be exemplary

### Don't
- Overwrite existing files without confirmation
- Make architectural changes without logging a decision
- Duplicate content between files — reference instead
- Skip tests or verification steps
- Add unnecessary complexity — this is a teaching project, clarity matters most

## Stack Conventions

This is a documentation and workshop materials project. Primary conventions:

- **Format:** Markdown for all documents and notes
- **Structure:** Progressive disclosure — start with core concepts, add depth in sub-documents
- **Tone:** Clear, accessible, practical — suitable for a mixed-experience audience
- **Examples:** Prefer real, working examples over abstract explanations
- **File creation:** Use the agentic scaffold files themselves as teaching examples

## Design Principles

These principles guide this project's evolution:

1. **Progressive disclosure** — Start simple. Add complexity only when earned. Don't front-load structure you don't need yet. When in doubt, defer adding a new file or process until the need is clear.

2. **Dual-audience documentation** — README.md serves humans. CLAUDE.md serves agents. Keep them distinct. Don't collapse human-readable overviews into agent instructions or vice versa.

3. **Decisions as first-class artifacts** — Significant choices get logged in DECISIONS.md before implementation. This creates a searchable, auditable trail that survives memory loss and team changes.

4. **Convention over configuration** — Prefer consistent patterns over per-case configuration. When a pattern is established, follow it. When a new pattern is needed, log the decision.

5. **The project is the demo** — This workshop teaches agentic concepts by practicing them. Every file here should exemplify the patterns being taught.

## References

- [GUIDE.md](GUIDE.md) — Core knowledge resource (beginner to advanced AI workflows)
- [DECISIONS.md](DECISIONS.md) — Architectural decision log
- [ROADMAP.md](ROADMAP.md) — Future directions and inspiration
- [CHANGELOG.md](CHANGELOG.md) — Narrative change history

<!-- Scaffold sources: Anthropic CLAUDE.md conventions, HumanLayer CLAUDE.md best practices guide, progressive disclosure (Krug; Nielsen Norman Group), convention over configuration (Rails/DHH) -->
<!-- Agentic Scaffold v0.1.0 | https://github.com/montymerlin/agentic-scaffold-plugin -->
