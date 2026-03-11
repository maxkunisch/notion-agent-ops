# Intake Questions

These are the 7 questions an agent asks before running the workspace init. Ask them all before building anything. Record the answers under `## Intake Responses` in the init page.

---

1. **Project name**
   What is this workspace called?
   *(Used in page titles and descriptions throughout the system.)*

2. **North star**
   In one or two sentences, what is the core loop or primary outcome this project is working toward?
   *(e.g. "Nanny logs hours → families review → each family exports payroll independently.")*

3. **Main sections**
   What are the top-level content sections in this workspace?
   *(e.g. Build, Strategy, Research, Marketing, Operations. Each section gets its own AGENTS page.)*

4. **External tools**
   Are any external tools in the loop?
   *(e.g. Linear, GitHub, Jira, Asana, Notion databases. If so: which ones, and what do they own?)*

5. **Primary human**
   Who is the main person working with agents in this workspace?
   *(First name is fine. Used to personalize the README and wrap-up skill.)*

6. **Data sensitivity**
   Is there any data that must never enter Notion?
   *(e.g. client PII, payment data, medical records. If so: what is it, and where does it live instead?)*

7. **Repo access**
   Do agents working in this workspace typically have repo / codebase access, or is Notion their only context?
   *(Affects how the AGENTS routing table is written — whether implementation detail routes to a repo or stays in Notion.)*

---

## Tips for asking these questions

- Ask all 7 in a single message, numbered, so the human can reply in one go.
- If a question doesn't apply (e.g. no external tools, no sensitive data), that's a valid answer — note it in the intake responses.
- Don't start building until you have answers to at least questions 1, 2, and 3. The others can be "none / not applicable" if needed.
