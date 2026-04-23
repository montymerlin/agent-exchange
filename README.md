# Agent Exchange

**A peer-to-peer learning community for people figuring out how to actually use AI in their work and lives.**

We're not a course. We're not a product. We're a group of practitioners — some technical, some not — who meet regularly to share what's working, what's broken, and what's blowing our minds. The only rule: if you learn something, teach it to someone else.

## The Idea

AI is moving fast. Most people are either overwhelmed by the possibilities or underwhelmed by their results. Agent Exchange exists in the gap between those two feelings — a place to go from "I use ChatGPT sometimes" to "I have an AI system that actually knows me and helps me do real work."

We cover the full spectrum. Beginners learn the fundamentals alongside someone who's done it before. Advanced practitioners push the frontier together in open hacker-house sessions. The social contract: if you join the advanced stream, you teach in the beginner stream. Knowledge compounds when it flows in both directions.

## Start Here

If you're new, **[read the Guide](GUIDE.md)**. It walks you through everything — from your first AI conversation to building a full agentic digital brain — with tools, links, and real examples from our sessions.

If you want the fastest possible path to value:

1. Open an agent host you already have access to — Claude Cowork or OpenAI Codex are both good current options
2. Point it at a folder and tell it what you're working on
3. Say: *"Ask me questions to understand what I need"*
4. Add a few core workflows that fit your host: structure, discipline, git safety, and ingestion
5. Start building something real

You don't need to understand everything before you begin. The AI will meet you where you are.

## What's In This Repo

This repo is both the workshop materials *and* a living example of the patterns we teach. Every file demonstrates a principle:

| File | What It Does |
|------|-------------|
| **[GUIDE.md](GUIDE.md)** | The main event — progressive guide from basics to frontier |
| **[README.md](README.md)** | You're here — orientation for humans |
| **[AGENTS.md](AGENTS.md)** | Canonical instructions for AI agents working in this project |
| **[CLAUDE.md](CLAUDE.md)** | Thin compatibility wrapper for Claude-oriented runtimes |
| **[DECISIONS.md](DECISIONS.md)** | Why things are the way they are |
| **[ROADMAP.md](ROADMAP.md)** | Where we're headed and what we're exploring |
| **[CHANGELOG.md](CHANGELOG.md)** | The story of how this project evolves |

Notice the dual-audience pattern: README is for you. `AGENTS.md` is for the AI. `CLAUDE.md` remains as a compatibility alias. That's one of the first things we teach.

## How to Contribute

The best contributions are ones other people can use — workflows, tools, patterns, setups. Specific project demos are interesting, but extractable principles are gold.

Some ideas: demo your AI workflow in a session, teach a beginner module on something you know well, share a plugin or skill you've built, bring a problem you're stuck on, or help someone else architect their system.

## Key Workflows

These are community-maintained skills and plugins that help move from one-off prompting into repeatable agent workflows. Some install as Claude plugins, some can be used as Codex skills, and some can be adapted across hosts.

Taken together, they form a useful four-part stack:

- **Agentic Scaffold** = structure
- **Superpowers** = discipline
- **Git Plugin** = collaboration and safety
- **MDPowers** = ingestion

| Workflow | What It Does |
|--------|-------------|
| [Agentic Scaffold](https://github.com/montymerlin/agentic-scaffold-plugin) | Sets up the foundational project structure for AI collaboration |
| [Superpowers](https://github.com/montymerlin/superpowers-plugin) | Enforces disciplined workflows — brainstorm, plan, execute, review, verify |
| [Git Plugin](https://github.com/montymerlin/git-plugin) | Helps you understand status, make safer commits, and use PRs when the risk is higher |
| [MDPowers](https://github.com/montymerlin/mdpowers-plugin) | Turns messy source material into clean markdown through clipping, conversion, and transcription |

## License

MIT

---

*Built with an [agentic scaffold](https://github.com/montymerlin/agentic-scaffold-plugin). This project practices what it teaches.*
