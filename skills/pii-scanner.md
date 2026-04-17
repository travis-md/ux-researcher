---
name: pii-scanner
description: "Scan any text, document, prompt, or AI output for personally identifiable information (PII) before it gets shared, pasted into an AI tool, or published. Use this skill whenever someone says 'check for PII', 'scan for personal data', 'anonymize', 'redact', 'is this safe to share', or before pasting research data, interview notes, survey responses, or user feedback into any AI tool. Also trigger when someone is about to send participant data, transcripts, or notes to Claude, ChatGPT, or any LLM. This skill should be used proactively — if you see PII in content the user is working with, flag it even if they didn't ask."
---

# PII Scanner

## Purpose
Scan text for personally identifiable information before it enters AI tools, gets shared with stakeholders, or leaves the team. This protects research participants, employees, and clients.

## What counts as PII

### HIGH RISK — Always flag and redact
- Full names (first + last)
- Email addresses
- Phone numbers
- Physical addresses (street level)
- Social Security / National ID numbers
- Financial account numbers (credit card, bank account)
- Login credentials (usernames + passwords)
- IP addresses
- Device identifiers
- Biometric data references
- Medical record numbers or health information
- Dates of birth (full)

### MEDIUM RISK — Flag and recommend redaction
- First name only (when combined with other identifiers)
- Job title + company (can identify individuals in small orgs)
- Age or age range (when combined with other data)
- Geographic location more specific than state/region
- Ethnicity, gender, or demographic details tied to small samples
- Photos or descriptions that could identify someone
- Participant IDs that could be reverse-mapped

### LOW RISK — Flag for awareness
- Company names (may be under NDA)
- Role descriptions without names
- Aggregated demographic data
- City-level location data

## How to scan

When given text to scan, follow this process:

### Step 1: Full scan
Read the entire text and identify every instance of PII from the categories above.

### Step 2: Report findings
Present findings in this format:

```
## PII Scan Results

**Risk Level: [HIGH / MEDIUM / LOW / CLEAN]**

### Items Found
| # | PII Type | Original Text | Location | Risk |
|---|----------|---------------|----------|------|
| 1 | Full name | "Jane Martinez" | Line 3 | HIGH |
| 2 | Email | "j.martinez@company.com" | Line 7 | HIGH |
| 3 | Job title + company | "Sr. Designer at Acme" | Line 12 | MEDIUM |

### Recommendation
[Specific guidance on what to redact before sharing]
```

### Step 3: Offer redacted version
Provide a clean version with PII replaced:
- Names → P1, P2, P3 (or Participant 1, etc.)
- Emails → [EMAIL REDACTED]
- Phone → [PHONE REDACTED]
- Addresses → [city/region only, or REDACTED]
- Job title + company → [ROLE REDACTED] or generalize ("a designer at a tech company")

## When to auto-trigger

If you see any of the following in user input, run this scan automatically:
- Interview transcripts or notes
- Survey responses with open text
- User feedback or support tickets
- Research participant data
- Any content the user says they want to "paste into ChatGPT/Claude/AI"
- Content being prepared for a report or presentation

## Quick anonymization patterns

For research data:
- "Sarah, 34, product manager at Stripe" → "P1, 30s, product manager at a fintech company"
- "Lives in 742 Evergreen Terrace, Springfield" → "Lives in a midwestern city"
- "sarah.jones@gmail.com" → "[EMAIL REDACTED]"

For interview quotes:
- Keep the insight, remove the identifier
- "John from the Chicago office said..." → "A participant from a regional office said..."
