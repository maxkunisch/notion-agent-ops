# ⚠️ wrap-up

*Trigger: "wrap up", "end of session", "let's close out", "session done", "that's it for today"*

> ⚠️ **Safety: Confirm before running.** This skill modifies MEMORY and may close or archive items in external tools. Confirm with the human before executing Steps 3–5.

---

## Steps

1. Read current **Now**, **In Flight**, and **Recent Decisions** in MEMORY.
2. Show the human the current state and ask:
   *"Here's what I see as the current state. Should I update MEMORY, close any completed items, or flag anything for next session?"*
3. *(Confirm before proceeding)* Update **Now** in MEMORY to reflect current true state.
4. *(Confirm before proceeding)* For any completed In Flight items: remove from In Flight, mark done in external tracker if applicable.
5. *(Confirm before proceeding)* If Recent Decisions exceeds 5 entries, move the oldest to the relevant content page.
6. Summarize what was updated and what to pick up next session.

---

## Output contract

- A brief session summary: what changed, what's still in flight, what to pick up next.
- All MEMORY changes confirmed with the human before writing.
- Do not close or archive anything in external tools without explicit instruction.
- If the human says "nothing to update", acknowledge and close out with no changes.
