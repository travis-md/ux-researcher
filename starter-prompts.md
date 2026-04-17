# Starter Prompts — Principal UX Researcher

Copy, paste, fill in the brackets. These are designed for your actual workflows.

---

## Before you paste anything: PII check
```
Scan the following for PII before I use it. Flag names, emails, phones, addresses, job title + company combos, and anything that could identify a specific participant.

[PASTE CONTENT HERE]
```

---

## Synthesize interviews
```
I have interview notes from [X] participants. Please:
1. Identify the top themes across all participants
2. Pull 1-2 supporting quotes per theme (anonymize to P1, P2, etc.)
3. Flag contradictions and outliers — don't smooth them over
4. Rate each theme by frequency (how many participants showed it)
5. Format as: Theme → Evidence → Implication

Research question I was trying to answer: [ONE SENTENCE]

Notes: [PASTE ANONYMIZED NOTES HERE]
```

---

## Standardize a messy report
```
Convert these notes into our standard report format:
1. Title & date
2. Research question (infer if not stated, flag it)
3. Methodology (method, sample size, duration)
4. Key findings (numbered, with evidence and severity)
5. Recommendations (tied to findings by number, with priority and effort)
6. Appendix (flag missing links as TODO)

If anything is missing, flag it — don't invent it.

Notes: [PASTE HERE]
```

---

## Extract and structure Figma content
```
This text was copied from a Figma file. Please:
1. Identify what each piece is (section header, annotation, UI label, body content, quote)
2. Reconstruct as clean markdown with proper hierarchy
3. Group related sections together
4. Flag anything that looks truncated, duplicated, or unclear

Figma text: [PASTE HERE]
```

---

## Write a stakeholder summary
```
Turn these research findings into a stakeholder summary.

Audience: [PM team / design leads / engineering / executives]
Format: [5-min verbal / async doc / slide deck bullets]

Structure:
1. TLDR — 2 sentences max
2. Top 3 findings — what we learned, why it matters
3. Recommendations — what we suggest and why
4. What we still don't know
5. Suggested next steps with [OWNER TBD] where ownership is unclear

Findings: [PASTE HERE]
```

---

## Parse a job map or spreadsheet
```
This is job map data from a spreadsheet. Please:
1. Organize by job step
2. List needs and pain points under each step
3. Highlight the highest-opportunity areas based on frequency or severity
4. Output as clean markdown ready for Confluence

Data: [PASTE HERE]
```

---

## Search for existing research (Glean prompt)
Use this in Glean before starting new research to check what already exists:
```
[research topic] site:confluence OR site:figma filetype:report OR filetype:deck
```
Or in natural language:
```
What research do we have on [topic or user group]?
```

---

## Write a discussion guide
```
Help me write a semi-structured interview guide for this research.

Research question: [ONE SENTENCE]
Participants: [Who you're talking to — role, context]
Session length: [X minutes]
What I already know: [Any prior research or assumptions]

Structure the guide as:
- Warm-up (2-3 questions)
- Core topics (5-7 questions with 2-3 follow-up probes each)
- Closing (1-2 questions about what we missed)

Flag any questions that might be leading or biased.
```

---

## Debrief after a session
```
I just finished an interview. Help me capture the most important things before I forget.

Participant context: [Role, brief description — no name]
Session length: [X minutes]
Research question: [ONE SENTENCE]

Here are my raw notes from the session:
[PASTE NOTES]

Please:
1. Pull out the 3-5 most important observations
2. Flag any quotes worth keeping (I'll clean them up)
3. Note anything surprising or contradicting what I expected
4. Suggest 1-2 follow-up questions for the next session
```

---

## Prep for a research readout
```
I'm presenting research findings to [AUDIENCE] in [X minutes / async].

Please rewrite these findings for that audience:
- Lead with what matters to them, not research process
- Frame as: what we learned → why it matters → what we recommend
- Use plain language, no research jargon
- End with: "What we still need to learn" and clear next steps

Findings: [PASTE HERE]
```
