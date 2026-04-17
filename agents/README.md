# Agent Orchestration — From Executor to Orchestrator

The biggest shift when working with Claude Code isn't the individual skills. It's moving from doing tasks to **directing workflows**.

---

## The mental model

**Old way — you are the executor:**
You synthesize interviews → you write the report → you format it → you send it.

**New way — you are the orchestrator:**
You define the research question, review the output, and stand behind the findings.
Claude handles the execution: pulling data, synthesizing, formatting, flagging gaps.

This isn't about moving faster. It's about operating at a higher level — spending your time on the judgment calls that require your expertise, not the mechanical steps that don't.

**The rule that doesn't change:** Delegation of implementation is not delegation of responsibility. Your name is on the research. Review everything before it goes anywhere.

---

## What agent orchestration looks like in practice

**Single skill (what you've seen so far):**
> "Synthesize these interview notes."

**Chained workflow (orchestration):**
> "I have 6 interview transcripts in Box. Pull them, scan for PII, synthesize themes, then format as our standard report ready for Confluence."

With MCP connected, Claude Code executes the whole chain. You review the output.

---

## Agents in this folder

| Agent | What it does |
|---|---|
| `synthesis-pipeline.md` | Full synthesis workflow: ingest → PII scan → synthesize → report |
| `research-sprint.md` | End-to-end research sprint: planning → guide → synthesis → readout |

---

## How to run an agent

Load the agent file at the start of a session:
> "Use the synthesis-pipeline agent. Here's what I'm working with: [context]"

Or reference it directly:
> "Follow the research-sprint agent workflow. My research question is: [question]"

---

## Building your own

An agent is just a markdown file with a defined workflow. If you find yourself doing the same multi-step sequence repeatedly, write it down as an agent. Ask Claude Code to help you write it.

The pattern:
1. Input (what you give it)
2. Steps (what it does in order)
3. Output (what it hands back to you)
4. Review gates (where you check before it continues)
