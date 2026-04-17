---
name: synthesis-pipeline
description: Full research synthesis workflow. Ingests raw interview notes or transcripts, scans for PII, synthesizes themes, and outputs a structured report ready for Confluence. Use when you have 3+ interviews to synthesize.
---

# Synthesis Pipeline Agent

## What this does
Takes raw interview data → PII scan → synthesis → standard report. One command, full output.

## You provide
- Source: paste notes directly, or reference Box files if MCP connected
- Research question (one sentence)
- Number of participants
- Any known themes you're testing for (optional)

## Pipeline steps

### Step 1 — Ingest
Collect all participant data. If pasted: confirm count. If Box MCP: search and retrieve files.
List what was received before proceeding.

### Step 2 — PII Scan
Run `pii-scanner` on all input before any synthesis.
**Hard stop:** if HIGH risk PII found, flag and do not proceed until redacted.
Output: clean participant labels (P1, P2, P3...) for all subsequent steps.

### Step 3 — Synthesize
Run `interview-synthesizer` on clean data.
Output: themes with frequency, evidence, quotes, implications, outliers.

### Step 4 — Review gate ← YOU REVIEW HERE
Present synthesis output. Wait for confirmation before proceeding.
Ask: "Does this match what you observed? Any themes to add, remove, or reframe?"

### Step 5 — Report
Run `report-standardizer` on confirmed synthesis.
Format: standard report structure (Title, Research Question, Methodology, Findings, Recommendations, Appendix).

### Step 6 — Gaps check
Flag anything missing: participant count low, methodology unclear, recommendations without evidence, TODO links in appendix.

### Step 7 — Final output
Deliver Confluence-ready markdown. Note: human review required before publishing.

## Usage
> "Run the synthesis-pipeline agent. Research question: [question]. Here are my notes from [n] participants: [paste or reference files]"
