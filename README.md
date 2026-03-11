# notion-agent-os

A Notion-native agent operating system. Bootstrap any workspace with AGENTS, MEMORY, and SKILLS in one `init` run.

---

## What is this?

**notion-agent-os** is a pattern and protocol for turning any Notion workspace into a structured operating environment for AI agents — Claude, Cursor, or any MCP-connected assistant.

Instead of explaining your project from scratch every session, agents read three pages and immediately know:

- What the project is and where things live (**AGENTS**)
- What's currently happening and what decisions were recently made (**MEMORY**)
- What procedures to follow for common tasks (**SKILLS**)

The whole system is bootstrapped in a single `init` run — the agent asks you 7 intake questions, then builds all the pages automatically.

---

## The three core pages

| Page | Role | Updated by |
|------|------|------------|
| 🧭 **AGENTS** | Durable routing rules, invariants, and constraints | Rarely — only when project structure changes |
| 🧠 **MEMORY** | Current state, in-flight work, recent decisions | Every session via `wrap-up` skill |
| ⚡ **SKILLS** | Procedural library — one skill per subpage | Anytime via `build-skill` skill |

All three live inside a single `⚙️ Agent System` container page, tucked away from the main workspace so humans don't have to look at them.

---

## Prior art

This project applies patterns well-established in software development to knowledge workspaces:

- **AGENTS** is a Notion-native expression of `AGENTS.md` conventions (used in Claude Code, Cursor, and similar tools) and architecture decision records (ADRs) — durable documents that capture *why* things are structured the way they are.
- **MEMORY** mirrors the `memory/` directory pattern in agentic coding systems — a lightweight, session-persistent state file that agents update as work progresses.
- **SKILLS** is the knowledge-workspace equivalent of runbooks, Makefile targets, or npm scripts — named, repeatable procedures with defined inputs, outputs, and safety classifications.
- **`agent-workspace-init`** follows the `git init` / `npm init` pattern: ask intake questions, then scaffold the right structure for the specific context.

The novel contribution is composing these four patterns in a Notion workspace, deployable by a non-technical user through natural language with no terminal access required.

---

## Quickstart

### For technical users

1. Connect your AI agent to your Notion workspace via MCP
2. Share the `agent-workspace-init` page with the agent (see `/init/agent-workspace-init.md`)
3. Say: *"Please read the agent-workspace-init page and run the intake with me before building anything."*
4. Answer 7 short questions
5. Say: *"Go ahead and build it."*

The agent creates all pages, links everything together, and confirms with a checklist of links when done.

### For non-technical users

See `/init/README-for-humans.md`.

The short version: open a conversation with your AI assistant and paste this prompt:

```
I'd like you to set up an agent operating system in my Notion workspace.
Please read the agent-workspace-init page first, then run the intake with
me before building anything:
https://github.com/maxkunisch/notion-agent-os/blob/main/init/agent-workspace-init.md
```

---

## Starter skills

Every workspace gets four skills out of the box:

| Skill | Safety | What it does |
|-------|--------|-------------|
| `orient-me` | ✅ Read-only | Situation report — what's happening, what's next, what needs attention |
| `file-this` | ✏️ State-modifying | Routes and records a decision, doc, or completed task |
| `wrap-up` | ⚠️ Confirm before running | Closes out a session, updates MEMORY |
| `build-skill` | ✏️ State-modifying | Interactively builds and creates a new skill page |

Skills follow a consistent format: trigger phrases, ordered steps, safety classification, and an output contract. Use `build-skill` to add workspace-specific skills as you go.

---

## File structure

```
notion-agent-os/
├── README.md
├── init/
│   ├── agent-workspace-init.md      # Executable init protocol (for agents)
│   ├── README-for-humans.md         # Plain-English guide (for non-technical users)
│   └── intake-questions.md          # The 7 intake questions, standalone reference
├── templates/
│   ├── AGENTS.md                    # Root AGENTS page template
│   ├── MEMORY.md                    # MEMORY page template
│   └── SKILLS.md                    # SKILLS page template
├── skills/
│   ├── orient-me.md
│   ├── file-this.md
│   ├── wrap-up.md
│   └── build-skill.md
└── examples/
    ├── AGENTS-example.md            # Filled-in example (Sharefully)
    ├── MEMORY-example.md            # MEMORY with real entry format examples
    └── SKILLS-example.md            # Full skill library as reference
```

---

## Design principles

**It's an `init`, not a plugin.** Run it once per workspace. It examines what's there, asks what it needs to know, and generates the right structure for that specific context.

**AGENTS is the durable contract. MEMORY is ephemeral.** Routing rules and invariants don't change session-to-session. Current state does. Keeping them separate means MEMORY stays high-signal and AGENTS stays stable.

**Skills have safety tiers.** Every skill is classified as read-only (✅), state-modifying (✏️), or confirm-before-running (⚠️). Agents know what they can run freely and what needs a human in the loop.

**Agent infrastructure stays out of the way.** All three core pages live inside a `⚙️ Agent System` container. Humans see a clean workspace. Agents find everything they need.

**Works with any MCP-connected agent.** Not tied to any specific AI product or Notion plan. If your agent can read and write Notion pages via MCP, this works.

---

## Status

Early development — tested on a small number of workspaces. The pattern is stable; the skill library will grow over time.

Contributions welcome, especially:
- New workspace-agnostic skills
- Improvements to the intake questions
- Reports of friction or edge cases encountered during init runs
- Examples from different workspace types (design, research, ops, freelance, etc.)

---

## License

MIT
