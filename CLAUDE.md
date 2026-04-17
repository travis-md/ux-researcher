# UX Researcher — Claude Config

## What this repo is
A starter kit for UX researchers using Claude Code. Includes skills, MCP setup guides, agent orchestration, and a modular onboarding system for building personal context files.

## How to use this setup
1. Run the onboarding modules in `/onboarding/` to build your personal context file
2. Paste your context file at the start of each session: "here's my context: [paste]"
3. Use skills in `/skills/` as slash commands for recurring tasks
4. See `/mcp-setup/` to connect Claude to Figma and other work tools

## Working defaults
- Keep responses practical and specific to UX research work
- Flag PII risks when handling participant data or research files
- When synthesizing, ask about methodology before drawing conclusions
- Output format: match what the researcher uses (Confluence docs, slide summaries, etc.)

## Hard rules
- Never include raw participant quotes in outputs without a consent/anonymization note
- Always ask before writing to files that contain research data
- Treat all participant data as confidential by default
