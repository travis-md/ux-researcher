---
name: interview-synthesizer
description: "Synthesize raw interview notes, transcripts, or session observations into structured themes, supporting quotes, and actionable implications. Use whenever someone says 'synthesize my interviews', 'find themes', 'analyze my notes', 'what patterns do you see', or pastes multiple participants' notes or transcripts. Also trigger when someone has 3 or more interviews worth of data and needs to make sense of it. Always check for PII before starting synthesis."
---

# Interview Synthesizer

## Purpose
Turn raw interview notes or transcripts from multiple participants into structured, evidence-backed themes ready for a research report.

## Before you start
1. Check input for PII — if found, flag and ask for anonymized version before proceeding
2. Count how many participants' data is present and note it
3. Identify the research question if stated (or infer it)

## Synthesis process

### Step 1: Extract observations
Go through all input and pull out every distinct observation, quote, or behavior. Don't cluster yet — just extract.

### Step 2: Identify themes
Group observations into themes. A theme requires:
- At least 2 participants showing the same pattern (or 1 with very strong signal — flag these as outliers)
- A clear label that describes the pattern, not just a topic

### Step 3: Output format

For each theme:

---
**Theme [#]: [Descriptive label — what is actually happening]**

**Frequency:** [X of Y participants] | **Signal strength:** [Strong / Moderate / Weak]

**Summary:** [2-3 sentences explaining what you observed across participants]

**Supporting evidence:**
- "[Quote or observation]" — P[#], [context if helpful]
- "[Quote or observation]" — P[#], [context if helpful]
- "[Observation without direct quote]" — P[#]

**Implication:** [What this means for design, product, or the team — one sentence]

**Contradictions / outliers:** [Any participants who bucked this theme — don't suppress these]

---

### Step 4: Synthesis summary
After all themes:

```
## Synthesis Summary

**Participants:** [n=X]
**Research question:** [stated or inferred]
**Themes identified:** [X total]

**Top themes by frequency:**
1. [Theme name] — X/Y participants
2. [Theme name] — X/Y participants
3. [Theme name] — X/Y participants

**Key tensions or contradictions:**
[Any places where participants significantly disagreed or showed opposite behaviors]

**What we still don't know:**
[Gaps in the data or questions this research raised but didn't answer]

**Recommended next steps:**
[What research or action this synthesis points toward]
```

## Rules
- Never fabricate quotes — use only what's in the input
- If a quote is paraphrased (not verbatim), mark it as (paraphrased)
- Don't suppress outliers — flag them explicitly
- Don't merge themes just to reduce the count — keep them distinct if the data supports it
- If the input is too thin to support a theme (only 1 participant, vague notes), say so
- All participant references use P1, P2, P3 — never names
