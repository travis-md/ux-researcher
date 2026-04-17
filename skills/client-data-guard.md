---
name: client-data-guard
description: "Scan any text, document, or prompt for client-confidential data, NDA-protected information, proprietary business data, or internal-only content before it gets shared externally or pasted into AI tools. Use this skill whenever someone says 'is this safe to share', 'check for confidential data', 'can I put this in Claude/ChatGPT', or when working with client deliverables, contracts, internal strategy docs, financial data, or competitive intelligence. Also trigger when you see company names combined with revenue figures, strategic plans, unreleased product details, or contractual terms. If someone is preparing content for an external audience or AI tool and the source is internal, run this check proactively."
---

# Client Data Guard

## Purpose
Catch confidential client data, NDA-protected information, and proprietary business content before it leaks into AI tools, external reports, or unauthorized channels.

## What counts as client-confidential data

### CRITICAL — Block immediately, do not pass to AI tools
- Client revenue, ARR, MRR, or financial figures
- Contract terms, pricing, or SOW details
- Client's unreleased product plans or roadmaps
- Client's internal org charts or personnel changes
- Client's proprietary methodologies or IP
- Client's customer lists or user data
- Merger, acquisition, or fundraising details
- Legal proceedings or regulatory findings
- Source code or technical architecture from client systems
- API keys, credentials, tokens, or environment variables

### HIGH RISK — Flag and require explicit approval
- Client company name + specific project details
- Internal metrics shared under NDA (conversion rates, churn, engagement)
- Competitive intelligence gathered during engagement
- Screenshots or recordings of client's internal tools
- Client's vendor relationships or partner agreements
- Draft deliverables not yet approved by client
- Internal communications (emails, Slack messages) from client contacts

### MEDIUM RISK — Flag for awareness
- Client company name in general context (may be fine, may not)
- Industry benchmarks that could be traced to a specific client
- Anonymized data that could be re-identified (small sample + details)
- Internal team discussions about client strategy
- Research findings before client has reviewed them

### CONTEXT-DEPENDENT — Check your NDA
- Case studies (some clients allow, some don't)
- Aggregated data across clients (check if sample size is large enough)
- Methodologies developed during client work (who owns the IP?)
- Templates created for a client (reusable or bespoke?)

## How to scan

### Step 1: Identify the context
Ask or infer:
- Who is the intended audience? (internal team / client / external / AI tool)
- What is the source of this content? (client project / internal / public)
- Is there an NDA in play? (assume yes if uncertain)

### Step 2: Full scan
Read the entire text and flag every item from the categories above.

### Step 3: Report findings

```
## Client Data Scan Results

**Risk Level: [CRITICAL / HIGH / MEDIUM / CLEAR]**
**Intended use: [what the user plans to do with this content]**

### Items Found
| # | Data Type | Content Summary | Risk | Action |
|---|-----------|----------------|------|--------|
| 1 | Client financials | Revenue figure for Acme Corp | CRITICAL | REMOVE |
| 2 | NDA-protected metric | Conversion rate from Q3 | HIGH | REMOVE or get approval |
| 3 | Client name | "Acme Corp" mentioned 4 times | MEDIUM | Anonymize for external use |

### Required Actions Before Sharing
1. [Specific items that MUST be removed]
2. [Items that need client approval]
3. [Items that should be anonymized]
```

### Step 4: Provide safe version
Offer a redacted version with:
- Client names → "Client A" or "[CLIENT]" or industry descriptor ("a major retailer")
- Financial figures → removed entirely or generalized ("significant revenue growth")
- Metrics → ranges or directional ("conversion improved by >20%") only if approved
- Project details → generalized ("a digital transformation initiative")
- People → roles only ("the VP of Product" not "Sarah Chen, VP Product at Acme")

## Decision tree for common scenarios

### "Can I paste this into Claude/ChatGPT?"
1. Is there ANY client name + specific data? → Anonymize first
2. Are there financial figures? → Remove them
3. Are there internal metrics? → Remove or generalize
4. Is there strategic/roadmap info? → Remove it
5. Is it just methodology or general process? → Likely fine, but remove client context

### "Can I use this in a case study?"
1. Does the client agreement allow case studies? → Check
2. Has the client approved this specific content? → Get approval
3. Can the insights be shared without identifying the client? → Anonymize

### "Can I share this in a presentation?"
1. Internal presentation? → Most internal data is fine
2. External/conference? → Apply full scan, anonymize everything
3. Client presentation? → Only their own data, not other clients'

## Auto-trigger conditions

Run this scan proactively when you see:
- Revenue, ARR, MRR, or dollar amounts combined with company names
- Phrases like "the client", "our client", "[Company] project"
- Contract language (terms, conditions, pricing, SOW)
- Content being prepared for external sharing
- Research data being moved between tools
- Any content heading into an AI tool from an internal source
