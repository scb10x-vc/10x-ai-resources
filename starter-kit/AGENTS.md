# Starter Kit — Codex Task Queue
**"The Markdown to Web Page Kit" — Internal sharing kit for SCBX non-technical teams**

This file is a task queue for Codex. Each task below is self-contained. Work through them in order. All files go inside `projects/training/starter-kit/` unless another path is specified.

---

## Tone Rules (apply to ALL content tasks)

- Written for someone who has never opened a terminal or used a code editor
- No VS Code references. No terminal commands. No "clone the repo."
- No jargon without a plain-English definition immediately after it (first use only)
- No em dashes. Use commas, colons, or periods instead.
- No emojis in any content
- No corporate-speak: no "leverage," "synergy," "best practice," "revolutionize," "game-changing"
- Specific over vague: use exact file extensions (.md, .csv, .html), exact menu paths, exact variable names
- Every guide file ends with a section called "TL;DR" containing exactly 3 bullet points
- All AI tool references say "Codex" — not "Claude," not "ChatGPT," not "the AI"

---

## CSS Variables Reference (for T-011)

Source: `projects/training/slides/theme-scb10x.css` and `assets/brand/scb10x/brand-guidelines.md`

```
--primary-color: #00B2A9      (Pantone 7467 C — teal, headings, borders, highlights)
--accent-color:  #bfae22      (gold — secondary highlights, metric boxes; design token, not official brand)
--purple:        #512888      (Pantone 268 C — tags, MBTI badges, section labels)
--background:    #f8f7f4      (off-white page background)
--surface:       #ffffff      (white card/box background)
--text-color:    #1c1c1e      (dark text — body copy)
--text-muted:    #6b6b6b      (grey — captions, secondary info)
--border-color:  rgba(28, 28, 30, 0.14)  (subtle borders)
```

Fonts: `Dosis` (headings), `Inter` (body). Both from Google Fonts.

---

## Tasks

---

### T-001 — Verify folder structure

**Action:** Confirm the following directories exist. Create any that are missing.

```
starter-kit/guides/
starter-kit/skills/
starter-kit/css/
starter-kit/sample-projects/persona-A-poom-market-researcher/context/
starter-kit/sample-projects/persona-A-poom-market-researcher/raw-inputs/
starter-kit/sample-projects/persona-B-ploy-employee-directory/context/
starter-kit/sample-projects/persona-B-ploy-employee-directory/raw-inputs/
starter-kit/sample-projects/persona-B-ploy-employee-directory/skills/
```

**Acceptance:** All 8 directories exist.

---

### T-002 — `README.md`

**File:** `starter-kit/README.md`

**Content spec:**

Write a friendly, non-technical overview of this kit. Max 400 words. Structure:

1. One-sentence description: what the kit is
2. "Who this is for" — 3 bullets describing the person this helps (not technical, works in Word/Excel, wants to produce better-looking outputs without learning to code)
3. "What's inside" — brief list of the 4 sections (guides/, skills/, css/, sample-projects/) with one sentence each
4. "How to get started" — two paths:
   - Path A: "I want to understand the concepts first" → start with guides/01-markdown-basics.md
   - Path B: "I want to see a working example immediately" → open one of the sample project folders and follow GETTING-STARTED.md
5. "The two examples" — 2-sentence description of Poom (market research report) and Ploy (employee directory). Keep it casual. Make the reader feel like they could do the same thing.

Do not use headers larger than `##`. Do not use a table of contents.

**Acceptance:** A non-technical reader understands what to do next within 30 seconds of opening this file.

---

### T-003 — `guides/01-markdown-basics.md`

**File:** `starter-kit/guides/01-markdown-basics.md`

**Content spec:**

Title: `# What is Markdown?`

Sections:
1. **The one-sentence version** — "Markdown is a plain text file with a few simple symbols that tell AI and other tools how to format things."
2. **Why this matters for your work** — Explain that AI tools (like Codex) read and write markdown natively. When your content is in markdown, you can ask Codex to restructure it, reformat it, or turn it into a finished document without any copy-pasting.
3. **The cheatsheet** — A two-column table. Left column: what you type. Right column: what it becomes. Include:
   - `# Heading 1` / Large title
   - `## Heading 2` / Section heading
   - `**bold text**` / Bold text
   - `- bullet point` / Bullet list item
   - `> This is a quote` / Highlighted/indented block
   - Three backticks (code block) / A formatted code or data block
   - `[link text](URL)` / Clickable link
4. **You do not need a special app to write it** — Any text editor works. Notepad on Windows, TextEdit on Mac, Google Docs (if you export the file afterward). You can also just type your content directly into Codex.
5. **A note on file extensions** — A markdown file ends in `.md`. If someone sends you a file called `notes.md`, open it in any text editor and you will see plain text with the symbols above.

**TL;DR** (exactly 3 bullets):
- Markdown is a plain text format that AI reads and writes natively
- A small set of symbols (like # and **) control all the formatting
- You do not need any special app to read or write it

---

### T-004 — `guides/02-docx-pdf-to-markdown.md`

**File:** `starter-kit/guides/02-docx-pdf-to-markdown.md`

**Content spec:**

Title: `# Converting Word Documents and PDFs to Markdown`

Opening paragraph: You already have documents. Word files, PDFs, reports from previous projects. This guide shows you how to convert them to markdown so Codex can work with them directly.

Sections:
1. **Converting a Word document (.docx)**
   - Step 1: Open Codex
   - Step 2: Attach the .docx file to your Codex session (drag it in, or use the attach/upload button)
   - Step 3: Paste this prompt exactly:
     ```
     Read this Word document and convert the content to clean markdown.
     Keep all headings, bullet points, and tables.
     Remove all formatting symbols like bold markers, color, or font changes — only keep the structure.
     Output the result as a .md file.
     ```
   - Step 4: Download or copy the output. Save it as a `.md` file (example: `my-report.md`).

2. **Converting a PDF**
   - Same steps as above. Use this prompt instead:
     ```
     Read this PDF and convert the text content to clean markdown.
     Keep all headings, bullet points, and tables you can identify.
     If you find sections that are images or charts, write [IMAGE] as a placeholder.
     Output the result as a .md file.
     ```
   - Important note: PDFs that are scanned images (not real text) will not convert well. If your PDF was created from a Word document or typed directly, it will work cleanly.

3. **What to check after converting**
   - Heading levels are correct (main title is `#`, sections are `##`, subsections are `###`)
   - Bullet points are intact (each one starts with `- `)
   - Tables converted correctly (tables in markdown look like columns separated by `|`)
   - No leftover symbols from Word formatting (like `*` appearing unexpectedly)

4. **Why lighter formats help**
   - Once it is `.md`, Codex can read it, restructure it, add sections, remove sections, and build finished documents from it — all without you having to manually copy and paste anything.

**TL;DR** (exactly 3 bullets):
- Attach a .docx or PDF to Codex and ask it to convert to markdown
- Text-based PDFs convert cleanly; scanned image PDFs may need manual cleanup
- Once content is in .md format, Codex can restructure and build from it directly

---

### T-005 — `guides/03-file-translation-guide.md`

**File:** `starter-kit/guides/03-file-translation-guide.md`

**Content spec:**

Title: `# File Format Guide: What to Convert and Why`

Opening paragraph: Not every file format is equally useful for AI-assisted work. This guide explains which formats to use and when, and why "lighter" formats make your workflow faster.

Sections:
1. **What "lighter" means** — A lighter format is smaller, has no proprietary formatting, and can be read directly by AI tools without special software. A `.csv` is lighter than an `.xlsx`. A `.md` is lighter than a `.docx`.

2. **Format comparison table** — A table with columns: Original format, Convert to, Why, How (brief).

   Include these rows:
   | Original | Convert to | Why | How |
   |---|---|---|---|
   | .xlsx (Excel) | .csv | Codex reads CSV directly; no formula or style lock-in | File > Save As > CSV in Excel |
   | .docx (Word) | .md | AI can read, restructure, and build from markdown | Attach to Codex + conversion prompt (see Guide 02) |
   | .odt (LibreOffice) | .md or .pdf | Same as Word — not natively readable by AI | Open in LibreOffice, export to PDF or copy text into a .md file |
   | .pptx (PowerPoint) | .pdf | Finalized slide decks do not need to be editable; PDF is universal | File > Export > PDF in PowerPoint |
   | .pdf (text-based) | .md | When you need to work with the content, not just share it | Attach to Codex + conversion prompt (see Guide 02) |
   | .pdf (scanned image) | Manual retyping or leave as-is | AI cannot read image-based PDFs reliably | No clean automated option |

3. **When NOT to convert**
   - You are sharing a file for someone else to edit in the original app (send the .docx, not a .md)
   - The file uses macros, forms, or tracked changes that must be preserved
   - The recipient specifically asked for a particular format

4. **A practical rule** — If you are giving a file to Codex to work with, convert it to the lightest format that preserves the content. If you are sharing a file with a colleague or client, use the format they expect.

**TL;DR** (exactly 3 bullets):
- Lighter formats (CSV, markdown) are smaller and AI can read them directly
- Convert Excel to CSV, Word/ODT to markdown, PowerPoint to PDF before giving files to Codex
- Do not convert when the recipient needs to edit the file in its original application

---

### T-006 — `guides/04-what-to-document.md`

**File:** `starter-kit/guides/04-what-to-document.md`

**Content spec:**

Title: `# What to Document: Context Files`

Opening paragraph (2 sentences): AI has no memory between sessions. Every time you start a new Codex session, it knows nothing about you, your team, your writing style, or your audience — unless you tell it. Context files are how you give it that memory.

Sections:
1. **The three files worth creating first**

   For each file: name, what it contains, 3-4 example lines, recommended length, when to update.

   **`brand-voice.md`**
   - What it contains: how your team writes — tone, formality level, things to avoid, things to always do
   - Example lines:
     - "Write in a formal but approachable tone. No slang."
     - "Use specific numbers. Avoid vague language like 'significant' or 'many.'"
     - "Do not use the word 'leverage' as a verb."
     - "Prefer short paragraphs. Max 3 sentences."
   - Recommended length: 1 page
   - When to update: when your team changes communication guidelines, or when you notice the AI keeps making the same tone mistake

   **`audience.md`**
   - What it contains: who reads your outputs, what they already know, what they care about, how much time they have
   - Example lines:
     - "Primary reader: senior business managers, not technical backgrounds."
     - "They want the conclusion first, then the evidence."
     - "Assume a 5-minute reading window. Get to the point fast."
     - "They are familiar with Thai financial market context."
   - Recommended length: half a page
   - When to update: when you start producing content for a new audience

   **`pipeline.md`**
   - What it contains: your workflow from start to finish — what files go in, what comes out, in what order
   - Example lines:
     - "Step 1: Collect raw inputs (interview notes, CSV data)"
     - "Step 2: Ask Codex to structure the content into sections using brand-voice.md"
     - "Step 3: Ask Codex to convert the markdown output to HTML using report-starter.css"
     - "Step 4: Open the HTML file in a browser and print to PDF"
   - Recommended length: 1 page
   - When to update: when your process changes

2. **Optional files to add later**
   - `style-guide.md` — specific formatting rules (heading capitalisation, date formats, number formatting)
   - `source-list.md` — recurring sources you trust and want cited correctly
   - `glossary.md` — terms that have specific meaning in your team's context

3. **How to use these files with Codex**
   Brief instructions: at the start of a new Codex session, attach the relevant context files and say: "Read these context files before you start. They define how I work and what my outputs should look like." Then proceed with your task.

4. **This connects to Skills**
   Transition paragraph: Once you have your context files, the next step is saving reusable prompts — so you do not retype the same instructions every session. That is what the `skills/` folder is for.

**TL;DR** (exactly 3 bullets):
- AI has no memory between sessions — context files give it the background it needs
- Start with three files: brand-voice.md, audience.md, and pipeline.md
- Attach them at the start of each Codex session before you give any task

---

### T-007 — `skills/README-skills.md`

**File:** `starter-kit/skills/README-skills.md`

**Content spec:**

Title: `# Skills: Reusable Prompts You Write Once`

Opening: Define a skill plainly: "A skill is a text file containing a set of instructions you have already written and tested. Instead of typing the same long prompt every session, you save it as a `.md` file and give it to Codex at the start of a session."

Sections:
1. **Why this matters** — Show the before/after. Before: you type a long, detailed prompt from memory every time you need a specific output, and it comes out slightly different each time. After: you have a skill file. You attach it to Codex and say "run this." Same result, every time, with no effort.

2. **How to use a skill with Codex** — 3 numbered steps:
   - Step 1: Open a new Codex session
   - Step 2: Attach the skill file (e.g., `skills/skill-markdown-to-html-report.md`) along with your content file
   - Step 3: Type: "Follow the instructions in the skill file and apply them to my content."

3. **The skills in this folder**
   Brief description of each (1 sentence each):
   - `skill-brand-voice-writer.md` — Codex interviews you about your writing style and produces a `brand-voice.md` file
   - `skill-markdown-to-html-report.md` — Converts a markdown file into a styled HTML report using `report-starter.css`
   - `skill-setup-marp-slides.md` — Sets up a slide project folder for you, ready to edit and export in one command

4. **When to write your own skill** — One short paragraph. If you find yourself typing the same long prompt more than twice, write it down in a `.md` file and save it in your skills folder. Give it a name that describes what it does (`skill-[what-it-does].md`).

5. **Skills build on each other** — One short paragraph. The output of `skill-brand-voice-writer.md` (your `brand-voice.md`) becomes an input to `skill-markdown-to-html-report.md`. Context files and skills are part of the same system.

No TL;DR for this file. It is already short.

---

### T-008 — `skills/skill-brand-voice-writer.md`

**File:** `starter-kit/skills/skill-brand-voice-writer.md`

**Content spec:**

Title: `# Skill: Brand Voice Writer`

Brief description (2 sentences): What this skill does and when to use it.

Then the full skill prompt, clearly marked as "copy everything below this line into Codex":

---

The prompt should be a structured interview. Codex asks the user a series of questions one at a time, waits for answers, then at the end drafts a `brand-voice.md` file based on the responses.

Questions to include (Codex asks these one at a time, in order):
1. "What is your job title and what kind of documents do you produce most often?"
2. "How formal is your team's writing? Give me a number from 1 to 5 where 1 is very casual (like texting a friend) and 5 is very formal (like a legal document)."
3. "Give me an example of a sentence your team would actually write. Just one real sentence from a recent document."
4. "Now give me an example of a sentence that sounds wrong for your team — too stiff, too casual, or just off."
5. "Are there any words or phrases you want to avoid? List them."
6. "How long are your typical paragraphs? Short (1-2 sentences), medium (3-4 sentences), or long (5+)?"
7. "Do you use data and numbers often? If yes, how precise — rough estimates or exact figures?"

After all answers are collected, Codex drafts a `brand-voice.md` file using the answers. The file should include: tone description, formality level, a "do" list and a "do not" list, paragraph length guidance, and a note on data/evidence style.

---

### T-009 — `skills/skill-markdown-to-html-report.md`

**File:** `starter-kit/skills/skill-markdown-to-html-report.md`

**Content spec:**

Title: `# Skill: Markdown to HTML Report`

Brief description: What this skill does (convert a markdown file into a standalone HTML report using provided CSS) and when to use it (when you want to turn a markdown draft into a finished, shareable document).

What to attach before running this skill (brief checklist):
- Your content file (.md)
- `css/report-starter.css` from this starter kit

Then the full skill prompt, clearly marked:

---

The prompt instructs Codex to:
1. Read the attached markdown file as the content source
2. Read the attached CSS file for all styling
3. Generate a single standalone `.html` file using this exact structure:
   - `<head>`: link to Google Fonts (Dosis + Inter), embed the CSS inline (so it works as a standalone file with no external dependencies)
   - `<body>`:
     - A `.cover` section at the top containing: the document title (from the first `# heading` in the markdown), a subtitle if there is a `## heading` before the first paragraph, and a date (today's date or from the markdown if specified)
     - One `.page` div per top-level `##` heading in the markdown
     - Within each page: use the CSS classes from report-starter.css where appropriate (`.card` for callout content, table styling for any markdown tables)
     - A simple footer with a horizontal rule and the document title
4. Output: one `.html` file named after the markdown file (e.g., `my-report.md` → `my-report.html`)
5. The file must open correctly in any browser without an internet connection (all CSS and fonts must be inline or embedded)

---

### T-010 — `skills/skill-setup-marp-slides.md`

**File:** `starter-kit/skills/skill-setup-marp-slides.md`

**Content spec:**

Title: `# Skill: Set Up a Marp Slides Project`

Brief description: Marp (short for Markdown Presentation Ecosystem) is a tool that turns a markdown file into a slide deck. This skill asks Codex to set up the whole project for you, so you can edit the slides in a plain text file and export to PDF with one command. You do not need to know how Marp works.

What you need to provide (brief checklist):
- A folder name for the project
- Your primary color (hex code, or just say "blue" or "teal" and Codex will pick a reasonable value)
- 3-5 words describing the topic of your slides

Then the full skill prompt, clearly marked:

---

The prompt instructs Codex to create the following in the specified folder:
- `slides/deck.md` — a Marp markdown file with:
  - YAML front matter: `marp: true`, `theme: custom`, `paginate: true`
  - 6 placeholder slides: title slide, agenda, 3 content slides, closing slide
  - Each slide separated by `---`
  - Placeholder content that shows the correct markdown syntax (headings, bullets, tables)
- `slides/theme.css` — a Marp CSS theme with:
  - The color variables from the CSS Variables Reference section of this AGENTS.md, substituting the user's chosen primary color for `--primary-color`
  - `section` base styles (font-family: Inter, padding, font-size)
  - `h1` and `h2` in Dosis font
  - `.title` slide class: full-width background, centered, primary color
  - `.section-break` slide class: solid primary color background, white text
- `build.sh` — a shell script that runs:
  ```bash
  npx @marp-team/marp-cli slides/deck.md --theme slides/theme.css --pdf -o output/slides.pdf
  npx @marp-team/marp-cli slides/deck.md --theme slides/theme.css --html -o output/slides.html
  ```
  The script must create the `output/` directory if it does not exist.
- `README.md` — simple instructions: edit deck.md to change slide content, run `./build.sh` to export, open `output/slides.pdf` to view.

---

### T-011 — `css/report-starter.css`

**File:** `starter-kit/css/report-starter.css`

**Content spec:**

Generate a clean, minimal CSS file for HTML reports. Every CSS rule block must have a short plain-English comment directly above it explaining what it does and where it appears visually. All color values must use the CSS variables defined in `:root`, not hardcoded hex codes.

Structure (in this order):

1. **Google Fonts import**
   ```css
   @import url('https://fonts.googleapis.com/css2?family=Dosis:wght@600;700&family=Inter:wght@400;500;600&display=swap');
   ```

2. **:root variables block** — with a comment above each variable:
   - `--primary-color: #007f91` (teal — headings, card borders, key highlights)
   - `--accent-color: #bfae22` (gold — secondary highlights, metric values)
   - `--purple: #4c2d83` (tags, badges)
   - `--background: #f8f7f4` (page background)
   - `--surface: #ffffff` (card and box backgrounds)
   - `--text-color: #1c1c1e` (main body text)
   - `--text-muted: #6b6b6b` (captions, secondary info, footer)
   - `--border-color: rgba(28, 28, 30, 0.14)` (subtle borders and dividers)

3. **body** — background: var(--background), font-family: Inter, font-size: 16px, line-height: 1.7, color: var(--text-color), margin: 0, padding: 0

4. **`.page-wrapper`** — max-width: 800px, margin: 0 auto, padding: 48px 56px (this centers the report content)

5. **`.cover`** — background: var(--primary-color), color: white, padding: 56px, margin-bottom: 40px. Inside: `.cover h1` in Dosis 700 48px white, `.cover .subtitle` in Inter 500 18px rgba(255,255,255,0.8), `.cover .date` in Inter 400 14px rgba(255,255,255,0.6)

6. **h1, h2, h3** — font-family: Dosis 700. h1: 32px var(--primary-color). h2: 24px var(--primary-color). h3: 18px var(--text-color). All with margin-top: 1.5em, margin-bottom: 0.4em.

7. **p** — margin: 0 0 1em 0, font-size: 16px

8. **`.card`** — background: var(--surface), border-left: 4px solid var(--primary-color), padding: 16px 20px, margin: 1.5em 0, border-radius: 0 4px 4px 0. Include a `.card.accent` variant that uses var(--accent-color) for the border.

9. **`.metric-box`** — display: inline-block, background: var(--surface), border: 1px solid var(--border-color), border-top: 3px solid var(--accent-color), padding: 16px 24px, text-align: center, min-width: 120px. Inside: `.metric-value` in Dosis 700 36px var(--accent-color). `.metric-label` in Inter 500 12px var(--text-muted) uppercase letter-spacing.

10. **table, th, td** — table: width 100%, border-collapse collapse, margin: 1.5em 0. th: background var(--primary-color), color white, Dosis 600, padding 10px 14px, text-align left. td: padding 10px 14px, border-bottom 1px solid var(--border-color). tr:nth-child(even): background rgba(0,127,145,0.04).

11. **`.tag`** — display: inline-block, background: var(--primary-color), color: white, font-size: 11px, font-weight: 600, padding: 3px 10px, border-radius: 20px, letter-spacing: 0.06em, text-transform: uppercase. Include `.tag.accent` (accent color) and `.tag.purple` (purple).

12. **`.footer`** — margin-top: 48px, padding-top: 16px, border-top: 1px solid var(--border-color), font-size: 13px, color: var(--text-muted), text-align: center.

Target: 150-180 lines including all comments.

---

### T-012 — `css/README-css.md`

**File:** `starter-kit/css/README-css.md`

**Content spec:**

Title: `# How to Customize the Report CSS`

Opening paragraph (non-technical): CSS (Cascading Style Sheets) is a file that controls the visual appearance of an HTML page — things like colors, fonts, and spacing. You do not need to understand CSS to use this kit. The most common change is updating the colors to match your team or brand. This guide shows you exactly where to do that.

Sections:

1. **CSS variables: the only lines you need to change**
   Explain that the file uses "variables" at the top. A variable is a named color or setting you define once, and it applies everywhere in the file automatically. You change it in one place, and the whole document updates.

   Table with columns: Variable name | What it controls | Where you see it visually:
   - `--primary-color` | Heading colors, card left borders, cover background, table header | Most prominent — anything teal in the default
   - `--accent-color` | Metric values, secondary card borders | Numbers in metric boxes, gold highlights
   - `--purple` | Tags, badges, MBTI labels | Small colored pills/labels
   - `--background` | Page background | The off-white area behind everything
   - `--surface` | Card and box backgrounds | White boxes inside the page
   - `--text-color` | Main body text | Everything you read in paragraphs
   - `--text-muted` | Captions, footer, secondary labels | Lighter grey text
   - `--border-color` | Dividers, card borders, table rows | Subtle lines between elements

2. **How to change your primary color**
   Numbered steps:
   - Open `report-starter.css` in any text editor (Notepad on Windows, TextEdit on Mac)
   - Find the line that says `--primary-color: #007f91;`
   - Replace `#007f91` with your color code (example: `#1a56db` for blue, `#16a34a` for green)
   - Save the file
   - Open your HTML report in a browser — the new color appears everywhere automatically

3. **How to find a color code**
   One paragraph: Go to google.com and search "color picker." You can pick any color visually and Google will show you the hex code (starts with #). Copy that value and paste it into the CSS file.

4. **What not to change (unless you know what you are doing)**
   Brief note: Do not delete the `:root` block at the top. Do not remove variable names or rename them. Changing fonts requires replacing the Google Fonts link and the `font-family` values — this is safe but slightly more involved.

---

### T-013 — `sample-projects/persona-A-poom-market-researcher/README.md`

**File:** `starter-kit/sample-projects/persona-A-poom-market-researcher/README.md`

**Content spec:**

Title: `# Poom's Project: Thailand Fintech Market Sizing Report`

Write in second-person, casual, identifying tone ("You're Poom. You work as a market research analyst..."). The reader should immediately recognize themselves or a colleague.

Structure:
1. **Who is Poom** — 3-4 sentences. Market research analyst at a financial company. Produces market sizing reports, competitor analysis, and consumer insight briefs. Has been doing this for years in Word and Excel. Spends as much time formatting the report as he does researching it.

2. **The problem he had** — 2-3 sentences. Every report starts from scratch. The data lives in Excel, the notes are in a Word document, and the final PDF is manually assembled in PowerPoint. If someone asks for a revision, the whole process repeats.

3. **What he built** — 2-3 sentences. A simple pipeline: structured interview notes in a markdown file, a CSV of market data, and a CSS template. He gives Codex the notes and asks it to structure a 5-section report. Then he converts it to HTML and prints to PDF.

4. **The numbers** — Specific. Old process: roughly 2 days to research, write, and format. New process: 4 hours to research, 1 hour to structure and produce the PDF.

5. **How to run this demo** — One sentence: "Open `GETTING-STARTED.md` in this folder and follow the prompt."

6. **How to adapt it** — 3 bullets on what to swap with your own content to make this yours.

---

### T-014 — `sample-projects/persona-A-poom-market-researcher/GETTING-STARTED.md`

**File:** `starter-kit/sample-projects/persona-A-poom-market-researcher/GETTING-STARTED.md`

**Content spec:**

Title: `# Getting Started: Run Poom's Demo`

Brief intro (2 sentences): This file contains the Codex prompt to generate Poom's market research report. Attach the files listed below, then copy the prompt into Codex.

**Files to attach:**
- `raw-inputs/sample-interview-notes.md`
- `../../css/report-starter.css`

**Prompt to paste into Codex** (clearly marked, copy everything below):

---

"I am a market research analyst. I am going to give you interview notes from a research project and a CSS file for styling.

Context files I am sharing with you:
- brand-voice.md: how I write — please read and follow it
- audience.md: who reads my reports — please keep this in mind
- pipeline.md: my process from start to finish

Your task:
1. Read sample-interview-notes.md. This contains raw notes from 3 interviews about Thailand digital payment adoption.
2. Structure the content into a market research report with these 5 sections: Executive Summary, Market Overview, Key Findings (one subsection per interviewee theme), Implications, and Recommended Next Steps.
3. Write each section in clean markdown following my brand-voice.md. Use specific numbers and observations from the notes. Do not invent data.
4. Once the markdown draft is complete, convert it to a standalone HTML file using report-starter.css. Embed the CSS inline. Structure: cover section with title 'Thailand Digital Payment Adoption: Key Findings 2025' and today's date, then one .page section per report section, then a footer.
5. Save the output as market-research-report.html.

Confirm when you are done and tell me the file name."

---

After the prompt, add a short "What to try next" section with 2 bullets:
- Swap `sample-interview-notes.md` with your own research notes and run the same prompt
- Edit `context/brand-voice.md` to match your team's actual writing style, then re-run

---

### T-015 — `sample-projects/persona-A-poom-market-researcher/context/brand-voice.md`

**File:** `starter-kit/sample-projects/persona-A-poom-market-researcher/context/brand-voice.md`

**Content spec:**

Write a realistic brand-voice.md for a market research analyst at a Thai financial company. ~150 words. Include:
- Tone: formal but readable, not academic
- Evidence standard: specific numbers and named sources, avoid vague language
- Avoid list: "game-changing," "significantly," "leverage" (as verb), "going forward," "best practice"
- Paragraph length: short to medium, max 3-4 sentences
- Structural preference: conclusion first, then evidence
- Note on language: English only, but Thai context is assumed (no need to define local references)

---

### T-016 — `sample-projects/persona-A-poom-market-researcher/context/audience.md`

**File:** `starter-kit/sample-projects/persona-A-poom-market-researcher/context/audience.md`

**Content spec:**

Write a realistic audience.md for Poom's internal business unit readers. ~100 words. Include:
- Who they are: senior managers and department heads, not analysts
- What they want: key takeaways first, then supporting detail
- Reading time: assume 5-10 minutes maximum
- Prior knowledge: familiar with Thai financial industry and general business context, not technical
- Decision context: they are reading this to make a resource allocation or strategy decision

---

### T-017 — `sample-projects/persona-A-poom-market-researcher/context/pipeline.md`

**File:** `starter-kit/sample-projects/persona-A-poom-market-researcher/context/pipeline.md`

**Content spec:**

Write a short, concrete pipeline.md for Poom. Max 200 words. Format as numbered steps. Include:
- Step 1: Collect raw inputs (interview notes in Google Docs → export as .md; market data as .csv)
- Step 2: Open Codex, attach raw-inputs/ files + context/ files
- Step 3: Ask Codex to structure into 5-section report (Executive Summary, Market Overview, Key Findings, Implications, Recommended Next Steps)
- Step 4: Review markdown output, make edits directly in the file
- Step 5: Run skill-markdown-to-html-report.md with report-starter.css to generate HTML
- Step 6: Open HTML in browser, print to PDF (File > Print > Save as PDF)

---

### T-018 — `sample-projects/persona-A-poom-market-researcher/raw-inputs/sample-interview-notes.md`

**File:** `starter-kit/sample-projects/persona-A-poom-market-researcher/raw-inputs/sample-interview-notes.md`

**Content spec:**

Title: `# Interview Notes: Thailand Digital Payment Adoption 2025`

Write fictional but realistic interview notes from 3 interviews. Each interviewee is a fictional person with a plausible name, job title, and company type (do not use real companies). Each has 6-7 bullet observations.

**Interviewee 1:** Head of Digital Products at a mid-size Thai retail bank. Observations about adoption rates among customers over 45, preferred payment channels, friction points in onboarding, regulatory constraints mentioned.

**Interviewee 2:** Operations Manager at a mid-size Thai e-commerce company. Observations about payment method preference by customer segment, cart abandonment tied to payment friction, their experience integrating payment APIs.

**Interviewee 3:** Financial inclusion researcher at a Thai university or think tank. Observations about unbanked population data, mobile wallet adoption in rural provinces, comparisons to regional peers (Vietnam, Indonesia), policy recommendations they have seen work.

Use realistic-sounding numbers throughout (percentage adoption rates, interview quotes in quotation marks, specific data points). Keep it raw and note-like — fragments are fine, complete sentences not required.

---

### T-019 — `sample-projects/persona-B-ploy-employee-directory/README.md`

**File:** `starter-kit/sample-projects/persona-B-ploy-employee-directory/README.md`

**Content spec:**

Title: `# Ploy's Project: Friendly Employee Directory`

Write in second-person, warm, slightly playful tone. The reader should immediately see the problem and want the solution.

Structure:
1. **Who is Ploy** — 3-4 sentences. HR admin or office culture lead. Manages a spreadsheet with everyone's details — department, title, birthday, MBTI. Nobody ever looks at the spreadsheet because it lives in someone's email attachments folder and nobody knows the password to the shared folder.

2. **The problem she had** — 2-3 sentences. The information exists. It just has no useful form. New joiners spend their first week not knowing who is who, what people are interested in, or even which floor Finance sits on.

3. **What she built** — 2-3 sentences. She kept using her CSV — the one she already maintains. She gave it to Codex with a skill prompt, and Codex generated a visual HTML page: department sections, employee cards with name, title, MBTI badge, birthday, and hobbies. She can open it in any browser.

4. **The maintenance loop** — This is the important part. When someone joins, she adds a row to the CSV. She gives Codex the updated CSV and runs the skill again. New HTML in a few minutes. No Photoshop, no Canva, no PowerPoint.

5. **How to run this demo** — One sentence: "Open `GETTING-STARTED.md` in this folder and follow the prompt."

6. **How to adapt it** — 3 bullets on what to swap with your own data to make this yours (replace `employees.csv` with your own, update `context/brand-voice.md`, change colors in `report-starter.css`).

---

### T-020 — `sample-projects/persona-B-ploy-employee-directory/GETTING-STARTED.md`

**File:** `starter-kit/sample-projects/persona-B-ploy-employee-directory/GETTING-STARTED.md`

**Content spec:**

Title: `# Getting Started: Run Ploy's Demo`

Brief intro (2 sentences): This file contains the Codex prompt to generate the employee directory from the CSV. Attach the files listed below, then copy the prompt.

**Files to attach:**
- `raw-inputs/employees.csv`
- `../../css/report-starter.css`
- `skills/skill-csv-to-directory.md`

**Prompt to paste into Codex** (clearly marked):

---

"I have a CSV file with employee information and I want to turn it into a visual HTML page.

Context:
- This is for internal use — all staff, any department
- Friendly, warm, people-first tone (not corporate)
- The page should be viewable in any browser and printable

Please read skill-csv-to-directory.md and follow the instructions exactly. Use employees.csv as the data source and report-starter.css for all styling.

Save the output as employee-directory.html."

---

After the prompt, add a "What to try next" section with 2 bullets:
- Replace `employees.csv` with your own team's data (keep the same column names)
- Change `--primary-color` in report-starter.css to your team's brand color and re-run

---

### T-021 — `sample-projects/persona-B-ploy-employee-directory/context/brand-voice.md`

**File:** `starter-kit/sample-projects/persona-B-ploy-employee-directory/context/brand-voice.md`

**Content spec:**

Write a brand-voice.md for Ploy's use case: internal culture content, friendly and warm. ~100 words. Include:
- Tone: warm, casual, genuinely friendly — not corporate, not stiff
- Uses first names (not Mr./Ms.)
- Celebrates personality and quirks — hobbies and fun facts should feel natural, not like a form field
- Short sentences. Plain language.
- Avoid: formal titles in running text, bullet points that feel like a job description, anything that sounds like an HR policy document

---

### T-022 — `sample-projects/persona-B-ploy-employee-directory/context/audience.md`

**File:** `starter-kit/sample-projects/persona-B-ploy-employee-directory/context/audience.md`

**Content spec:**

Write an audience.md for the employee directory. ~80 words. Audience is: all staff at any level, browsing casually. They want to know who someone is before a meeting, find out who has a birthday this month, discover they share a hobby with a colleague. They are not reading this for a decision — they are reading it for connection and orientation.

---

### T-023 — `sample-projects/persona-B-ploy-employee-directory/context/pipeline.md`

**File:** `starter-kit/sample-projects/persona-B-ploy-employee-directory/context/pipeline.md`

**Content spec:**

Write a short pipeline.md for Ploy. Max 150 words. Numbered steps:
- Step 1: Maintain `employees.csv` — add or update rows as people join or change roles
- Step 2: Open Codex, attach `employees.csv`, `report-starter.css`, and `skills/skill-csv-to-directory.md`
- Step 3: Paste the prompt from GETTING-STARTED.md
- Step 4: Codex generates `employee-directory.html`
- Step 5: Open `employee-directory.html` in any browser to review
- Step 6: Share the HTML file via email, internal chat, or upload to shared drive. Anyone can open it in a browser.

---

### T-024 — `sample-projects/persona-B-ploy-employee-directory/raw-inputs/employees.csv`

**File:** `starter-kit/sample-projects/persona-B-ploy-employee-directory/raw-inputs/employees.csv`

**Content spec:**

Generate a CSV with exactly these columns (in this order):
`name, nickname, department, title, start_date, birthday, mbti, hobbies, fun_fact`

Create 12 rows of fictional but realistic and diverse employees. Use plausible Thai-sounding names. Spread across 4 departments: Engineering, Design, Operations, Finance (3 per department). Mix of titles (manager, analyst, lead, associate). MBTI types should be varied and realistic. Hobbies should be specific and interesting (not just "reading" — say "urban sketching" or "making sourdough" or "amateur astronomy"). Fun facts should be genuinely fun (not "I love my team").

Start dates should span 2018-2024. Birthdays should span all 12 months across the 12 employees so the "birthday this month" feature would be useful.

---

### T-025 — `sample-projects/persona-B-ploy-employee-directory/skills/skill-csv-to-directory.md`

**File:** `starter-kit/sample-projects/persona-B-ploy-employee-directory/skills/skill-csv-to-directory.md`

**Content spec:**

Title: `# Skill: CSV to Employee Directory`

Brief description (2 sentences): What this skill does and when to use it.

Then the full skill prompt (clearly marked — copy everything below):

---

The prompt instructs Codex to:

1. Read the attached `employees.csv`. Expect these columns: name, nickname, department, title, start_date, birthday, mbti, hobbies, fun_fact.

2. Read the attached `report-starter.css` for styling variables and base styles.

3. Generate a single standalone HTML file called `employee-directory.html` with this structure:
   - `<head>`: page title "Team Directory", Google Fonts (Dosis + Inter), all CSS from report-starter.css embedded inline, plus these additional styles:
     - `.directory-header`: large Dosis heading, primary color, centered, 40px padding
     - `.department-section`: margin-bottom 48px
     - `.department-title`: Dosis 700 20px, primary color, uppercase, letter-spacing 0.1em, border-bottom 2px solid var(--primary-color), padding-bottom 8px, margin-bottom 24px
     - `.card-grid`: display grid, grid-template-columns: repeat(auto-fill, minmax(240px, 1fr)), gap 20px
     - `.employee-card`: background var(--surface), border-radius 8px, padding 20px, border 1px solid var(--border-color), border-top 4px solid var(--primary-color)
     - `.employee-name`: Dosis 700 18px, var(--text-color), margin-bottom 2px
     - `.employee-nickname`: Inter 400 13px, var(--text-muted), margin-bottom 8px
     - `.employee-title`: Inter 500 14px, var(--primary-color), margin-bottom 12px
     - `.mbti-badge`: display inline-block, background var(--purple), color white, font-size 11px, font-weight 600, padding 2px 10px, border-radius 20px, margin-bottom 10px
     - `.employee-detail`: font-size 13px, color var(--text-muted), margin-bottom 4px, with a label span in var(--text-color) font-weight 500
     - `.fun-fact`: font-size 12px, font-style italic, color var(--text-muted), margin-top 10px, padding-top 10px, border-top 1px solid var(--border-color)
   - `<body>`:
     - `.directory-header` section with "Team Directory" as h1 and today's date
     - One `.department-section` per unique department value in the CSV (sorted alphabetically)
     - Within each department: `.department-title` heading, then `.card-grid` containing one `.employee-card` per employee in that department
     - Each card shows: name, nickname (in brackets), title, MBTI badge, birthday (Month DD format), hobbies, fun fact
   - No footer needed

4. Output: one standalone `employee-directory.html` file. All CSS embedded inline. No external file dependencies. Must open correctly offline.

---

## Completion Check

After all tasks are done, verify:
- [ ] All 8 directories exist
- [ ] `README.md` opens and is readable in 30 seconds
- [ ] `GETTING-STARTED.md` in persona-B folder: paste prompt + attach employees.csv + report-starter.css → Codex generates a working employee-directory.html
- [ ] `GETTING-STARTED.md` in persona-A folder: paste prompt + attach sample-interview-notes.md + report-starter.css → Codex generates a structured HTML report
- [ ] `skill-brand-voice-writer.md`: paste into Codex → generates a usable brand-voice.md in one session
- [ ] All guides end with a TL;DR section containing exactly 3 bullets
- [ ] No VS Code references, no terminal commands, no Claude Code references in any content file
