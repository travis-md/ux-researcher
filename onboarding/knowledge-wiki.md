# Building a Knowledge Wiki for Claude

How to set up a persistent knowledge system so Claude always knows who you are, how you work, and what you're working on — without re-explaining yourself every session.

---

## What this is

A knowledge wiki is a set of files that give Claude durable context. Instead of starting cold every session, you load your context and Claude picks up where you left off.

The system has three layers:

| Layer | File | What it does |
|---|---|---|
| **Project config** | `CLAUDE.md` | Tells Claude how to behave in this repo |
| **Personal context** | `context-v2.0.md` | Who you are, how you work, your stakeholders |
| **Current project** | Included in context | What you're working on right now |

---

## Layer 1 — CLAUDE.md

`CLAUDE.md` is a file Claude reads automatically at the start of every session in a repo. Think of it as standing instructions that are always in effect.

### What belongs in CLAUDE.md

```markdown
# [Your Name or Role]

## Who I am
One paragraph: your role, your team, what you actually do.

## How to work with me
- Tone: [direct/collaborative/formal — whatever fits]
- Response length: [short and punchy / detailed with context / depends on task]
- When to ask vs. just do: [your preference]

## What I'm working in
- Primary tools: [Figma, Confluence, Notion, etc.]
- Where files live: [brief note on storage]
- How I share work: [slides, Confluence, email, readouts]

## Hard rules
- [Anything Claude must never do — e.g., "never share raw participant quotes without consent flag"]
- [Format requirements — e.g., "always use my report template"]
```

### Best practices

**Keep it short.** CLAUDE.md is read every session. Long files slow Claude down and bury the important parts. Aim for under 60 lines.

**Use it for standing rules, not project details.** Project context goes in your context file. CLAUDE.md is for things that are always true.

**Tone > format.** The most valuable thing in CLAUDE.md is how you want to be worked with — not a tool list.

**Don't commit sensitive info.** CLAUDE.md may end up in a shared repo. Keep it generic enough that anyone could read it. Names, client details, access credentials — never in CLAUDE.md.

**Revisit it after a month.** Your first version will be a guess. After a few weeks of working sessions you'll know what actually belongs in there.

---

## Layer 2 — Your personal context file

This is the richer layer. Built through the 5 onboarding modules, it contains:

- Who you are and what you do
- How you think and work
- Who you work with and for
- How you want Claude to behave with you
- What you're working on right now

### How to use it

At the start of any Claude session:

```
Here's my context: [paste context-v2.0.md]
```

That's it. Claude will work from it for the whole session without you needing to repeat yourself.

### What to store here vs. CLAUDE.md

| Belongs in context file | Belongs in CLAUDE.md |
|---|---|
| Your research background and experience | Tone and communication preferences |
| Stakeholder dynamics and politics | Hard rules and constraints |
| Your synthesis process and instincts | Tool list |
| Current project details | Response format preferences |
| What success looks like for you | What Claude should never do |

The context file is yours alone — don't commit it to GitHub. The CLAUDE.md is repo-level and can be shared.

---

## Layer 3 — Current project context

Module 5 in the onboarding adds a `## Current project` section to your context file. This is the layer you refresh most often — once per project, not once per session.

It captures:
- What the project is and why
- The core research question
- Who the participants are
- Where you are in the process
- What's done and what's next
- Timeline and stakes

When a project ends, you run Module 5 again with the new project. The old one gets replaced.

---

## Building it over time

You don't need all of this on day one.

```
Week 1    Run Module 1. Paste context-v1.0.md at the start of sessions.
Week 2    Run Module 2. Now Claude knows how you think.
Week 3    Run Module 3 before a stakeholder readout. Context gets sharper.
Month 2   Run Module 4 once you have real opinions about what's working.
Ongoing   Run Module 5 at the start of each new project.
```

Each layer adds something. Each version works on its own.

---

## File hygiene

- Name versions clearly: `context-v1.0.md`, `context-v1.1.md`, `context-v2.0.md`
- Keep old versions — they're a record of how your work has evolved
- Store your context file somewhere only you can access (local drive or private cloud folder)
- Never paste raw PII into your context file — names are fine, verbatim participant data is not
- Update Module 5 at the start of each project, not during

---

## The mental model

Think of it like a new colleague's onboarding doc. A great onboarding doc means the new person can get to work immediately without needing to ask basic questions every day. Your context file is that doc — except it's for Claude, and you write it yourself.

The better the context file, the less you have to manage the AI. It just works the way you need it to.
