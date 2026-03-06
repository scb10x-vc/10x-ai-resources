# What to Document: Context Files

Codex has no memory between sessions. Every new session starts with zero context about your team, style, or audience unless you provide it.

## The three files worth creating first

### `brand-voice.md`
What it contains: how your team writes, including tone, formality, what to avoid, and what to always do.

Example lines:
- "Write in a formal but approachable tone. No slang."
- "Use specific numbers. Avoid vague language like 'significant' or 'many.'"
- "Do not use the word 'leverage' as a verb."
- "Prefer short paragraphs. Max 3 sentences."

Recommended length: 1 page.
When to update: when communication guidelines change, or when Codex repeats the same tone mistake.

### `audience.md`
What it contains: who reads your output, what they already know, what they care about, and how much time they have.

Example lines:
- "Primary reader: senior business managers, not technical backgrounds."
- "They want the conclusion first, then the evidence."
- "Assume a 5-minute reading window. Get to the point fast."
- "They are familiar with Thai financial market context."

Recommended length: half a page.
When to update: when you create content for a different audience.

### `pipeline.md`
What it contains: your process from start to finish, including input files, output files, and sequence.

Example lines:
- "Step 1: Collect raw inputs (interview notes, CSV data)"
- "Step 2: Ask Codex to structure the content into sections using brand-voice.md"
- "Step 3: Ask Codex to convert the markdown output to HTML using report-starter.css"
- "Step 4: Open the HTML file in a browser and print to PDF"

Recommended length: 1 page.
When to update: when your workflow changes.

## Optional files to add later
- `style-guide.md`: rules for headings, date formats, and number formats
- `source-list.md`: trusted recurring sources you want cited correctly
- `glossary.md`: team-specific terms and definitions

## How to use these files with Codex
At the start of a new session, attach the context files you need and say: "Read these context files before you start. They define how I work and what my outputs should look like." Then give your task.

## This connects to Skills
After context files are in place, the next step is reusable prompts so you stop retyping instructions. That is what the `skills/` folder is for.

## TL;DR
- AI has no memory between sessions — context files give it the background it needs
- Start with three files: brand-voice.md, audience.md, and pipeline.md
- Attach them at the start of each Codex session before you give any task
