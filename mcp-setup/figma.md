# Figma MCP Setup

Connect Claude Code to Figma so it can read files, annotations, and research boards directly.

## What you can do once connected

- "Read the annotations on this Figma frame and extract the research insights"
- "Pull all the sticky notes from this FigJam board and synthesize themes"
- "What questions are open in this design file's comments?"
- "Extract all the copy from this prototype for a content audit"

## Setup

### Step 1 — Get a Figma API token
1. Go to Figma → Account Settings → Personal Access Tokens
2. Create a new token with read access
3. Copy it — you'll use it once during setup

### Step 2 — Install the Figma MCP server
```bash
npx figma-developer-mcp --figma-api-key=YOUR_TOKEN_HERE
```

Or add it to your Claude Code MCP config file (`~/.claude/mcp_servers.json`):
```json
{
  "figma": {
    "command": "npx",
    "args": ["figma-developer-mcp"],
    "env": {
      "FIGMA_API_KEY": "your-token-here"
    }
  }
}
```

### Step 3 — Restart Claude Code
```bash
claude
```

### Step 4 — Test it
> "List the frames in this Figma file: [paste file URL]"

If it returns frame names, you're connected.

## Usage in research workflows

**Extract annotations from a research board:**
> "Read this Figma file [URL]. Extract all sticky notes and annotations. Group by color/section if they're color-coded. Then run the interview-synthesizer skill on the output."

**Pull copy for a content audit:**
> "Read all text layers from this Figma prototype [URL]. Organize by screen name."

**Research board synthesis:**
> "This is a FigJam affinity map [URL]. Extract all the sticky notes, identify the clusters, and summarize each cluster's theme."

## Privacy note
Your Figma API token authenticates you directly. Participant data in Figma files is subject to the same PII rules — run `pii-scanner` on anything containing participant quotes before using it further.
