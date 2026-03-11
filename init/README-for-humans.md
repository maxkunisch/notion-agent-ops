# 👋 README — Start Here

> **This page is for you.** Everything else in this workspace is written for AI agents. This page explains what's going on, in plain English.

---

## What is all this?

Your Notion workspace has a small system built into it that helps AI assistants (like Claude) work with you more effectively. Instead of having to explain your project from scratch every time you start a conversation, the AI can read a few pages here and immediately understand:

- What your project is and what you're trying to accomplish
- Where different kinds of information live
- What it's allowed to do, and what it should check with you first
- What's currently happening and what decisions have been made recently

Think of it like leaving a really good briefing document for a smart assistant before they start their shift.

---

## The three special pages

You'll notice a page called **⚙️ Agent System** in your workspace. Inside it are three pages that are a bit different from the rest:

### 🧭 AGENTS — *The rulebook*
Tells the AI how your workspace is organized, where things belong, and what the important ground rules are. You rarely need to touch this yourself. If your project changes significantly (new tools, new structure), this is the page to update.

### 🧠 MEMORY — *The whiteboard*
Where the AI keeps track of what's happening right now — what's being worked on, what was recently decided, what's in progress. If you ever want to know the current state of play at a glance, check this page.

### ⚡ SKILLS — *The playbook*
A collection of specific things the AI knows how to do in your workspace — like orienting itself at the start of a session, filing a decision in the right place, or wrapping up a work session cleanly. You don't need to read these. They're there so the AI follows consistent, predictable steps instead of improvising.

---

## What do I actually need to do?

Honestly, not much. The system is designed to run in the background.

**You might want to occasionally:**
- Glance at **MEMORY** to see what the AI thinks is happening
- Correct anything in MEMORY that's out of date
- Say *"wrap up"* at the end of a session so the AI updates its own notes

**You don't need to:**
- Read or edit AGENTS (unless something major changes)
- Read the individual SKILLS pages
- Do anything special to "activate" the system — it's always on

---

## How do I start a session with the AI?

Just open a conversation and say:

> *"Orient me"* or *"What's the state of play?"*

The AI will read MEMORY and any connected tools and give you a quick summary of where things stand. From there, just talk to it naturally.

---

## What if something seems wrong or out of date?

Just tell the AI directly. For example:

> *"That decision is out of date — we changed direction on that."*
> *"Can you update MEMORY to reflect where we are now?"*
> *"File this decision in the right place."*

The AI handles the updates. You don't need to edit these pages manually.

---

## Setting this up in a new workspace

If you want this same system in one of your other Notion workspaces, here's exactly what to do. It takes about 10 minutes and the AI does all the work.

**You'll need:** Claude (or another AI assistant) connected to your Notion account, with access to the new workspace.

### Step 1 — Give the AI its instructions

Open a new conversation with the AI and paste this message:

```
I'd like you to set up an agent operating system in my Notion workspace.
Please read the agent-workspace-init page first, then run the intake
with me before building anything.

Here's the init page:
https://github.com/maxkunisch/notion-agent-os/blob/main/init/agent-workspace-init.md
```

### Step 2 — Answer the intake questions

The AI will ask you 7 short questions about your workspace — things like what the project is called, what it's trying to accomplish, and what sections it has. Just answer them naturally.

### Step 3 — Let the AI build it

Once you've answered the questions, say:

> *"Go ahead and build it."*

It will create all the pages, link everything together, and give you a list of links when it's done.

### Step 4 — You're done

The new workspace will have the same system — AGENTS, MEMORY, SKILLS, and a README — all customized for that project.

---

> 💬 **Questions?** Just ask the AI. Try *"Explain how the MEMORY page works"* or *"What should I do at the end of a work session?"*
