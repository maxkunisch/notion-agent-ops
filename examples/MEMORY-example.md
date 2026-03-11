# 🧠 MEMORY — Example (Sharefully)

> This is a filled-in example showing correct entry formats. A real MEMORY page starts blank.

---

## Now
- Core authentication flow is complete. Working toward first payroll export milestone.
- CSV export is the active build priority. No blocked items.

## In Flight
- [SHR-42] Add CSV export — branch: `feature/csv-export` — owner: Max
- [SHR-45] Fix approval race condition — branch: `fix/approval-race` — owner: Claude

## Recent Decisions
- [2026-03-10] Chose independent per-family payroll export over shared gate — see Build > Architecture
- [2026-03-08] Moved from Supabase to Convex for real-time sync — see Build > Tech Stack
- [2026-03-05] Deferred nanny credential feature to Milestone 3 — see Strategy > Milestones

---

> 📌 **How to use MEMORY**
>
> - Append updates here as work progresses. Keep this page high-signal.
> - **Now** = current state snapshot. What is true right now.
> - **In Flight** = active work items.
>   Format: `[ID] Short description — branch: feature/xyz — owner: Name`
> - **Recent Decisions** = last 5 decisions, newest first.
>   Format: `[YYYY-MM-DD] Decision summary — see [linked page]`
> - When Recent Decisions exceeds 5 entries, move the oldest to the relevant content page.
> - For durable rules and routing, use **AGENTS**. MEMORY is for ephemeral state only.
