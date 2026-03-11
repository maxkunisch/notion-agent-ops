# ✏️ file-this

*Trigger: "file this", "record this decision", "save this", "log this", "put this somewhere"*

> ✏️ **Safety: State-modifying.** This skill writes to Notion pages and/or MEMORY. Confirm the destination with the human if ambiguous.

---

## Steps

1. Identify what is being filed: a decision, a reference doc, a completed task, or a new page.
2. Apply the routing rule from AGENTS to determine the correct destination:
   - Decision → relevant content page + bullet under **Recent Decisions** in MEMORY
   - Reference doc → correct section page
   - Completed task → mark done in external tracker (if applicable)
   - New page → create under the correct section with appropriate title
3. If the destination is ambiguous, **stop and ask** before writing.
4. Write or update the target page.
5. If a decision was filed, add a one-line entry to **Recent Decisions** in MEMORY:
   `[YYYY-MM-DD] Decision summary — see [linked page]`
6. Confirm to the human: what was filed, where it now lives, and a direct link.

---

## Output contract

- One confirmation message with: what was filed, destination page (with link), and any MEMORY update made.
- If nothing was written (ambiguity, no valid destination), explain why and ask for clarification.
- Never file to a destination the human hasn't confirmed when routing is unclear.
