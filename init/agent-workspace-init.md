# agent-workspace-init

> **This is an executable protocol.** Read it, run the intake, then build the system. Run it once per workspace. It is idempotent — running it again on an existing workspace should only fill gaps, not overwrite.

---

## What this builds

A structured agent operating system inside any Notion workspace, contained within a single `⚙️ Agent System` page:

- **🧭 AGENTS** — the durable contract. Routing rules, invariants, and constraints that don't change session-to-session.
- **🧠 MEMORY** — ephemeral state. What's true now, what's in flight, recent decisions. High-signal, regularly pruned.
- **⚡ SKILLS** — the procedural library. One skill per subpage, each with a trigger, steps, output contract, and safety classification.

These three pages live inside `⚙️ Agent System`, tucked away from the main workspace so humans don't need to look at them.

---

## Phase 1 — Intake

Before creating anything, ask the human the following questions. Do not proceed to Phase 2 until you have answers to all of them.

1. **Project name** — What is this workspace called?
2. **North star** — In one or two sentences, what is the core loop or primary outcome this project is working toward?
3. **Main sections** — What are the top-level content sections in this workspace? (e.g. Build, Strategy, Research, Marketing.) Each will get its own section-specific AGENTS page.
4. **External tools** — Are any external tools in the loop? (e.g. Linear, GitHub, Jira, Asana.) If so, which ones and what do they own?
5. **Primary human** — Who is the main person working with agents in this workspace? First name is fine.
6. **Data sensitivity** — Is there any data that must never enter Notion? (e.g. client PII, payment data.) If so, what lives where instead?
7. **Repo access** — Do agents working in this workspace typically have repo access, or is Notion their only context?

> 📝 Record the answers directly on this page under a `## Intake Responses` section before proceeding. This creates a permanent record of setup decisions.

---

## Phase 2 — Protocol

Execute these steps in order. After each step, note the created page URL before moving on.

**Step 1 — Create the Agent System container**
Create a page titled `⚙️ Agent System` at the top level of the workspace. All agent infrastructure lives inside it. Add a one-line reference to it on the workspace root page: `⚙️ Agent System — Operating rules, current state, and skill library for AI agents. Humans rarely need to open this.`

Use this content:
```
> This section is for AI agents. It contains the operating rules, current state,
> and skill library for agents working in this workspace. You don't need to read
> or edit these pages — the AI handles them. If you're curious, check the README.
```

**Step 2 — Create AGENTS**
Create `🧭 AGENTS` inside `⚙️ Agent System`. Use the template in `/templates/AGENTS.md`. Fill in project name, north star, routing table, external tools, and safety rules from the intake responses.

**Step 3 — Create MEMORY**
Create `🧠 MEMORY` inside `⚙️ Agent System`. Use the template in `/templates/MEMORY.md`. Leave Now, In Flight, and Recent Decisions blank (blank = idle is valid).

**Step 4 — Create SKILLS**
Create `⚡ SKILLS` inside `⚙️ Agent System`. Use the template in `/templates/SKILLS.md`. Create the four starter skills as subpages, copying from `/skills/`:
- `orient-me.md`
- `file-this.md`
- `wrap-up.md`
- `build-skill.md`

Customize trigger phrases and steps for the specific workspace where needed.

**Step 5 — Create section-specific AGENTS pages**
For each main section from the intake, create a subpage inside that section titled `🧭 AGENTS — [Section Name]`. Open with the precedence callout (root AGENTS always applies), then add only section-specific routing rules, writing rules, and state-recording conventions.

**Step 6 — Create Page Index**
Create `🗂️ Page Index` as a subpage of AGENTS. List the key pages agents will most often need, organized by section. Use live page links — not plain text references.

**Step 7 — Update root AGENTS**
Add a Page Index reference and links to all section-specific AGENTS pages. Add the "Starting fresh?" callout at the top: AGENTS → MEMORY → `orient-me`.

**Step 8 — Create README**
Create `👋 README — Start Here` at the top level of the workspace using `/init/README-for-humans.md` as the template. Written for humans — plain English, no jargon. Place it at the very top so it's the first thing a non-technical person sees.

**Step 9 — Confirm output**
Reply with a checklist of every page created, each with its Notion URL. Flag anything that couldn't be completed and why.

---

## Phase 3 — Output contract

When done, the workspace must have:

- [ ] `⚙️ Agent System` at workspace top level, referenced on the root page
- [ ] `🧭 AGENTS` inside Agent System — populated, not a stub
- [ ] `🧠 MEMORY` inside Agent System — structured with blank-but-valid entries
- [ ] `⚡ SKILLS` inside Agent System — with all four starter skills as subpages
- [ ] One `🧭 AGENTS — [Section]` subpage per main section
- [ ] `🗂️ Page Index` nested under AGENTS, with live page links
- [ ] Root AGENTS has "Starting fresh?" callout and links to all section AGENTS pages
- [ ] `👋 README — Start Here` at workspace top level

---

## Intake responses

*(Record answers here before beginning Phase 2.)*
