# ⚙️ build-skill

*Trigger: "build a skill", "create a skill", "add a skill for [X]", "make a skill that [does Y]"*

> ✏️ **Safety: State-modifying.** This skill creates a new subpage in SKILLS. Confirm the skill name and safety tier with the human before writing.

---

## Steps

**Step 1 — Clarify intent**
If the human hasn't already described the skill clearly, ask:
- What should trigger this skill? (A phrase, a situation, a type of request?)
- What should it do? (What's the end state when it's done?)
- Does it read things, write things, or both?

Do not proceed to Step 2 until you can answer all three.

**Step 2 — Assign a safety tier**
Choose one based on what the skill does:

| Tier | Icon | When to use |
|------|------|-------------|
| Read-only | ✅ | Only reads pages, MEMORY, or external tools. No changes anywhere. |
| State-modifying | ✏️ | Creates, updates, or deletes content anywhere. |
| Confirm before running | ⚠️ | Irreversible effects, broad scope, or touches multiple systems. Requires explicit human confirmation mid-skill. |

If in doubt between two tiers, choose the higher one.

**Step 3 — Draft the trigger phrase**
Write 2–4 natural-language trigger phrases a human would actually say. A good trigger phrase:
- Starts with a verb ("orient me", "file this", "build a skill")
- Matches how the human naturally speaks
- Is distinct enough that it won't accidentally fire on unrelated requests

**Step 4 — Draft the steps**
Write the skill's procedural steps. Each step should:
- Be a single, concrete action
- State clearly what to do if something is ambiguous (stop and ask, or apply a default rule)
- Note any decision points where the agent must branch

Aim for 4–8 steps. If a skill needs more than 8, consider splitting it into two skills.

**Step 5 — Write the output contract**
Define what "done" looks like:
- What does the agent say or produce when the skill is complete?
- What page links, confirmations, or summaries are required?
- What should NOT be done?

**Step 6 — Confirm with human**
Before creating the page, show the human:
- Proposed skill name
- Safety tier and icon
- Trigger phrases
- Steps (plain prose summary)
- Output contract

Ask: *"Does this look right, or should I adjust anything before I create it?"*

**Step 7 — Create the skill page**
Once confirmed, create a new subpage under SKILLS using this format:

```markdown
# [icon] [skill-name]

*Trigger: "phrase 1", "phrase 2"*

> [icon] **Safety: [Tier].** [One sentence on what this modifies or why confirmation is needed.]

## Steps
[Numbered steps]

## Output contract
[What done looks like]
```

Tier callout colors:
- ✅ Read-only → use a green callout
- ✏️ State-modifying → use a yellow callout
- ⚠️ Confirm before running → use a red callout

**Step 8 — Update SKILLS index**
Add the new skill to the SKILLS page table under the appropriate tier:
`| \`skill-name\` | [icon] | One-line description |`

---

## Output contract

- Confirmation message with: skill name, page link, safety tier, one-line description.
- SKILLS index table updated with the new entry.
- If the human rejected the draft in Step 6, loop back to Step 3 with their feedback.
- Never create the page until the human has confirmed the draft.
