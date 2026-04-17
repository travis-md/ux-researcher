---
name: figma-extractor
description: "Extract, structure, and clean up text that has been copied or exported from Figma. Use whenever someone says 'I copied this from Figma', 'extract this from my design file', 'clean up this Figma export', or pastes a wall of text that looks like it came from a design tool (mixed labels, headers, UI copy, and annotations with no clear hierarchy). Also trigger when someone needs Figma content converted to Confluence, a report, or any text-based format."
---

# Figma Extractor

## Purpose
Take raw text exported or copy-pasted from Figma — which is usually a jumbled mix of UI labels, section headers, annotations, and body content — and turn it into clean, structured markdown.

## What Figma exports look like (so you can recognize them)
- No clear hierarchy — headers mixed with body text
- Labels and UI copy mixed with research annotations
- Repeated section names (e.g., "Notes" appearing multiple times)
- Truncated or clipped text from frames
- Numbering or ordering that doesn't match reading order
- Sticky note content mixed with frame titles

## Extraction process

### Step 1: Identify content types
Scan the input and tag each piece as one of:
- **Section header** — top-level organizational label
- **Subsection** — nested label within a section
- **UI label** — button text, field names, navigation items
- **Annotation** — researcher or designer notes about the content
- **Body content** — actual findings, observations, or descriptions
- **Quote** — participant quote (treat as body content, flag for PII)
- **Unknown** — can't determine type, flag for review

### Step 2: Reconstruct hierarchy
Build a clean markdown structure:

```markdown
# [Section Header]

## [Subsection]

[Body content paragraph or bullets]

> [Quotes, if present]

*[Annotation — clearly marked as annotation]*

### UI Elements
- [Label 1]
- [Label 2]
```

### Step 3: Flag issues
After the clean output, list:

```
## Extraction Notes

**Possible truncations:** [Any text that appears cut off]
**Unclear items:** [Anything that couldn't be categorized — paste original]
**PII found:** [Any participant names or identifying info — flag before use]
**Ordering assumptions:** [Any places where reading order was inferred]
**Missing context:** [Sections that seem incomplete or reference missing frames]
```

## Output rules
- Preserve the meaning — don't rewrite or interpret, just restructure
- If something is ambiguous (label vs. body?), keep both and flag it
- Group related content together even if it was scattered in the Figma export
- Convert frame titles to markdown headers
- Convert sticky notes / annotations to italics or blockquotes with a label
- Never delete content even if it looks like a duplicate — flag duplicates instead

## Common use cases

### Research board → synthesis notes
Figma affinity maps often have themes as section headers and stickies as evidence. Extract:
- Theme names → H2 headers
- Sticky content → bullet points under each theme
- Quotes → blockquotes

### Journey map → structured document
- Phases → H2 headers
- Steps → numbered list
- Pain points → bullets under each step
- Opportunities → separate section

### Design annotations → Confluence-ready doc
- Frame names → section headers
- Annotation text → body content
- UI labels → separate "UI copy" section
