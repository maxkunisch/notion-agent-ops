# 🧭 AGENTS — Example (Sharefully)

> This is a filled-in example based on the Sharefully workspace. Replace all content with your own project details when deploying.

---

> 🚀 **Starting fresh? Read in this order:**
> 1. This page (AGENTS) — routing rules and invariants.
> 2. MEMORY — current state, in-flight work, recent decisions.
> 3. Run `orient-me` from SKILLS if you need a full situation report.

> 🧭 **AGENTS is the durable contract.**
> Routing and invariants live here. Ephemeral state lives in MEMORY.

---

## What this project is

Sharefully is a nanny time-tracking app for nanny-share arrangements.

**North star:** Nanny logs direct entries → submits weekly → each family independently reviews and approves → each family runs payroll export independently (no cross-family gate).

**Stack:** Next.js + Convex + Clerk + Tailwind CSS 4 + Catalyst components

---

## Where things live (routing)

- **Linear** — actionable build issues within ~2 months. No speculative backlog.
- **Strategy & Product** — durable product thinking, decisions, and reference.
- **Build** — architecture, models, and rationale (not day-to-day branch status).
- **Repo** (`AGENTS.md`, `docs/`, `memory/`) — implementation patterns, schema, conventions.

---

## Routing rule

- Actionable build work soon → Linear
- Strategic deliverable / decision / framework → Strategic Work Tracker + relevant Notion page
- Product thinking / rationale / reference → Notion pages
- Implementation detail → repo
- Ephemeral state → MEMORY

---

## Safety

**Data handling rule:** No real client data ever enters Notion. Notion is the strategy layer. Convex is the data layer.

---

## Skills

See: ⚡ SKILLS *(one skill per subpage; includes safety classification)*

---

## Page Index

See: 🗂️ Page Index — curated index of the Notion pages agents most often need.

---

## Section-specific AGENTS pages

These pages inherit all rules from this root and only add section-specific specifics.

- 🧭 AGENTS — Strategy & Product — strategy, decisions, writing rules
- 🧭 AGENTS — Build — build constraints, verification, branching

---

## If you only have Linear access

Linear-only agents should focus on updating issue status, adding comments, and creating new issues only from explicit user instruction. For product context, use Notion. For implementation detail, use the repo.
