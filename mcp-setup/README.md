# MCP Setup — Connect Your Tools Directly

MCP (Model Context Protocol) lets Claude Code read from your actual tools — Figma, Confluence, Jira, Box — without copy-paste.

## Without MCP (Tier 1)
You copy text from Figma → paste into Claude Code → get output.

## With MCP (Tier 2)
> "Read the research annotations from Figma file XYZ and synthesize the themes."

Claude goes and gets it. You stay in the flow.

---

## What changes with MCP

| Without MCP | With MCP |
|---|---|
| Copy text from Figma, paste in | Claude reads Figma directly |
| Download transcript from Box, paste in | Claude searches and reads Box |
| Copy Confluence page, paste in | Claude pulls the page by URL |
| Manual Jira ticket review | Claude queries open research tickets |

---

## Setup guides

- [Figma](./figma.md)
- [Confluence + Jira](./confluence-jira.md)
- [Box](./box.md)

---

## Before you set up MCP

You need:
- Claude Code Enterprise access ✅ (you have this)
- Admin or API access to each tool
- 15–30 minutes per integration

Start with Figma — it has the most mature MCP server and you'll see immediate value in research work.

---

## Privacy note

MCP connections authenticate with **your own credentials**. Data routes between Claude Code and your tools directly — it doesn't pass through this repo or any third party. The same PII rules apply: participant data stays anonymized regardless of how it comes in.
