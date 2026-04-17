---
name: report-standardizer
description: "Convert messy, unstructured research notes, raw findings, or informal write-ups into the standard research report format. Use whenever someone says 'clean up my notes', 'format this report', 'standardize this', 'turn my notes into a report', or pastes raw research content that doesn't follow the standard structure. Also trigger when someone shares findings that lack clear methodology, severity ratings, or recommendations tied to findings."
---

# Report Standardizer

## Purpose
Convert any research content — raw notes, bullet dumps, informal write-ups, Confluence drafts — into the team's standard report format.

## Standard report structure

### 1. Title & Date
- Clear, specific title (not "Research Notes" — use the actual project and method)
- Date of report, not date of fieldwork

### 2. Research Question
- One sentence: what did this research set out to answer?
- If not stated in the source material, infer it from context and flag it as inferred

### 3. Methodology
- Method (e.g., semi-structured interviews, usability test, survey)
- Sample size (e.g., n=8)
- Duration (e.g., 60-minute sessions, over 2 weeks)
- Recruitment criteria if mentioned
- If missing, flag as [METHODOLOGY NOT PROVIDED — add before publishing]

### 4. Key Findings
Format each finding as:

**Finding [#]: [One-sentence summary]**
- **Evidence:** [Direct quote or observation that supports this]
- **Severity:** [Critical / High / Medium / Low]
- **Frequency:** [How many participants / what % showed this]
- **Source:** [Interview notes / usability session / survey data]

Rules:
- Number findings sequentially
- Order by severity (Critical first)
- Never state a finding without evidence
- Flag inferred or uncertain findings with [NEEDS VALIDATION]

### 5. Recommendations
Format each recommendation as:

**Recommendation [#]: [Action-oriented statement]** *(addresses Finding [#])*
- **Priority:** [P1 / P2 / P3]
- **Effort:** [Low / Medium / High]
- **Owner:** [Role or team — use [OWNER TBD] if unknown]

Rules:
- Every recommendation must tie back to a numbered finding
- Use action verbs: "Redesign...", "Add...", "Remove...", "Test..."
- Don't recommend solutions that aren't supported by the data

### 6. Appendix
- Links to raw data, recordings, transcripts (flag as [LINK NEEDED] if missing)
- Links to Figma boards or affinity maps
- Links to Jira tickets
- Participant recruitment criteria
- Discussion guide or survey instrument (if available)

## How to process input

1. Read all input material first before restructuring
2. Identify what's present and what's missing
3. Build the report structure, placing content where it fits
4. Flag every gap: [MISSING — add before publishing]
5. Do not invent data, quotes, or participants
6. If tone is inconsistent, standardize to professional-but-plain
7. Offer a list of gaps at the end for the researcher to fill

## Quality checks before handing back
- [ ] Every finding has at least one piece of evidence
- [ ] Every recommendation ties to a finding number
- [ ] No participant names or PII in the output
- [ ] Methodology section has method, sample size, duration
- [ ] Missing links are flagged, not omitted silently
