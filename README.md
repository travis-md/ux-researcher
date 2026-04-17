# UX Researcher

A Claude Code setup for principal UX researchers — skills, prompts, MCP integrations, and agent workflows built for real research operations.

**Not a chatbot. A research workbench.**

---

## What's in here

```
ux-researcher/
├── CLAUDE.md                  ← standing config — Claude reads this automatically
├── context-template.md        ← your project snapshot — fill in once per project
├── starter-prompts.md         ← copy/paste prompts for every workflow
├── onboarding/                ← build your personal context file in 10-min chunks
│   ├── README.md
│   ├── module-1-basics.md
│   ├── module-2-how-you-work.md
│   ├── module-3-stakeholders.md
│   ├── module-4-ai-preferences.md
│   ├── module-5-current-project.md
│   └── knowledge-wiki.md      ← how the whole system works
├── skills/                    ← specialized tools
│   ├── pii-scanner.md
│   ├── interview-synthesizer.md
│   ├── report-standardizer.md
│   ├── figma-extractor.md
│   └── client-data-guard.md
├── mcp-setup/                 ← connect your tools directly
│   ├── README.md
│   └── figma.md
└── agents/                    ← multi-step research workflows
    ├── README.md
    └── synthesis-pipeline.md
```

---

## Two tiers of setup

### Tier 1 — Basic (15 minutes)
Skills + prompts only. Copy-paste workflow. Works with any Claude Code access.

### Tier 2 — Integrated (with MCP servers)
Claude Code reads directly from Figma, Confluence, Jira, Box. No copy-paste. Full agent orchestration.

Start with Tier 1. Add Tier 2 when you're ready.

---

## Tier 1 Setup

```bash
git clone https://github.com/travis-md/ux-researcher.git ~/ux-research
cd ~/ux-research
claude
```

Fill in `context-template.md` with your current project. That's it.

---

## Tier 2 Setup — MCP Servers

See `mcp-setup/` for step-by-step guides for each tool.

With MCP connected, instead of:
> "Here's text I copied from Figma..."

You get:
> "Read the annotations from Figma file [ID] and synthesize them."

Claude Code goes and gets it directly.

---

## Privacy & Data Rules

- `CLAUDE.md` enforces PII scanning before any participant data is processed
- Your `context-template.md` (filled in) stays on your device — never commit it to this repo
- MCP connections authenticate with your own credentials — no data routes through this repo
- All participant data uses P1/P2/P3 labels — never real names

---

## Contributing

PRs welcome. Skills, prompts, MCP configs, agent workflows. Keep it research-focused and PII-safe.
