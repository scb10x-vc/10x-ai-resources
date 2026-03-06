# Skills: Reusable Prompts You Write Once

A skill is a text file containing a set of instructions you have already written and tested. Instead of typing the same long prompt every session, you save it as a `.md` file and give it to Codex at the start of a session.

## Why this matters
Before, you type a detailed prompt from memory every time and the output can vary. After, you attach one skill file and tell Codex to run it, then you get the same reliable structure each time.

## How to use a skill with Codex
1. Open a new Codex session.
2. Attach the skill file, for example `skills/skill-markdown-to-html-report.md`, along with your content file.
3. Type: "Follow the instructions in the skill file and apply them to my content."

## The skills in this folder
- `skill-brand-voice-writer.md`: Codex interviews you about writing style and creates a `brand-voice.md` file.
- `skill-markdown-to-html-report.md`: converts a markdown file into a styled HTML report using `report-starter.css`.
- `skill-setup-marp-slides.md`: creates a ready-to-edit slide project folder with export steps included.

## When to write your own skill
If you find yourself typing the same long prompt more than twice, save it in a `.md` file in your `skills/` folder. Use a clear name that describes the job, for example `skill-weekly-summary-writer.md`.

## Skills build on each other
The output of `skill-brand-voice-writer.md`, your `brand-voice.md`, can become an input to `skill-markdown-to-html-report.md`. Context files and skills work together as one system.
