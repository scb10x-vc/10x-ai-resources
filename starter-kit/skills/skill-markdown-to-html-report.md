# Skill: Markdown to HTML Report

Use this skill to convert a markdown file into a standalone HTML report with consistent styling. Use it when your draft is ready and you want a finished, shareable document.

## What to attach before running this skill
- Your content file (`.md`)
- `css/report-starter.css` from this starter kit

## Copy everything below this line into Codex

1. Read the attached markdown file as the content source.
2. Read the attached CSS file and use it for all styling.
3. Generate a single standalone `.html` file using this structure:
   - `<head>`: include Google Fonts links for Dosis and Inter, then embed the CSS inline so the file works on its own.
   - `<body>`:
     - Add a `.cover` section at the top with:
       - document title from the first `#` heading in the markdown
       - subtitle if there is a `##` heading before the first paragraph
       - date, use today's date unless the markdown provides one
     - Create one `.page` div per top-level `##` heading in the markdown.
     - Inside each page, apply classes from `report-starter.css` where relevant, for example `.card` for callouts and table styles for markdown tables.
     - Add a simple footer with a horizontal rule and the document title.
4. Name the output file after the markdown file, for example `my-report.md` becomes `my-report.html`.
5. Ensure the final HTML opens in any browser without an internet connection, all CSS and font references must be inline or embedded.
