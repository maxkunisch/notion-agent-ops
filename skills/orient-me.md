# ✅ orient-me

*Trigger: "orient me", "what's the state of play", "catch me up", "where are we"*

> ✅ **Safety: Read-only.** This skill does not modify any state. Safe to run at any time.

---

## Steps

1. Read **Now** in MEMORY.
2. If an external task/issue tracker is connected, check active issues (In Progress + equivalent).
3. For each in-progress item, verify it still has an owner and active context. If missing, treat as stale.
4. Identify anything needing the human's attention: blocked items, open decisions, stale work.
5. Reply in 3 sections: **In progress** / **Up next** / **Needs your attention** — max 10 lines total.

---

## Output contract

- Three labeled sections, plain prose or short bullets.
- No more than 10 lines.
- If everything is idle, say so in one sentence.
- Do not modify MEMORY or any other page.
