# Converting Word Documents and PDFs to Markdown

You already have documents: Word files, PDFs, and reports from previous projects. This guide shows you how to convert them to markdown so Codex can work with them directly.

## Converting a Word document (.docx)
1. Open Codex.
2. Attach the `.docx` file to your Codex session, drag it in or use the attach or upload button.
3. Paste this prompt exactly:

```text
Read this Word document and convert the content to clean markdown.
Keep all headings, bullet points, and tables.
Remove all formatting symbols like bold markers, color, or font changes — only keep the structure.
Output the result as a .md file.
```

4. Download or copy the output and save it as a `.md` file, for example `my-report.md`.

## Converting a PDF
1. Open Codex.
2. Attach the PDF file.
3. Paste this prompt:

```text
Read this PDF and convert the text content to clean markdown.
Keep all headings, bullet points, and tables you can identify.
If you find sections that are images or charts, write [IMAGE] as a placeholder.
Output the result as a .md file.
```

4. Save the output as a `.md` file.

Important note: PDFs that are scanned images, not real text, will not convert cleanly. PDFs exported from Word or typed directly usually convert well.

## What to check after converting
- Heading levels are correct, main title is `#`, sections are `##`, subsections are `###`
- Bullet points are intact, each one starts with `- `
- Tables converted correctly, columns are separated by `|`
- No leftover formatting symbols, for example unexpected `*`

## Why lighter formats help
Once content is in `.md`, Codex can read it, restructure it, add sections, remove sections, and build finished documents without manual copy and paste.

## TL;DR
- Attach a .docx or PDF to Codex and ask it to convert to markdown
- Text-based PDFs convert cleanly; scanned image PDFs may need manual cleanup
- Once content is in .md format, Codex can restructure and build from it directly
