# File Format Guide: What to Convert and Why

Not every file format is equally useful for Codex workflows. This guide explains what to convert, when to convert it, and why lighter formats make work faster.

## What "lighter" means
A lighter format is smaller, has less proprietary formatting, and can be read directly by Codex without special software. A `.csv` is lighter than an `.xlsx`. A `.md` is lighter than a `.docx`.

## Format comparison table
| Original format | Convert to | Why | How |
|---|---|---|---|
| .xlsx (Excel) | .csv | Codex reads CSV directly, no formula or style lock-in | File > Save As > CSV in Excel |
| .docx (Word) | .md | Codex can read, restructure, and build from markdown | Attach to Codex + conversion prompt (see Guide 02) |
| .odt (LibreOffice) | .md or .pdf | Same as Word, not natively readable by Codex | Open in LibreOffice, export to PDF or copy text into a .md file |
| .pptx (PowerPoint) | .pdf | Final slide decks usually only need sharing, PDF is universal | File > Export > PDF in PowerPoint |
| .pdf (text-based) | .md | Use this when you need to work with the content | Attach to Codex + conversion prompt (see Guide 02) |
| .pdf (scanned image) | Manual retyping or leave as-is | Codex cannot read image-only PDFs reliably | No clean automated option |

## When NOT to convert
- You are sharing a file for someone else to edit in the original app
- The file has macros, forms, or tracked changes that must stay intact
- The recipient asked for a specific format

## A practical rule
If you are giving a file to Codex, convert to the lightest format that still keeps the content. If you are sharing with a colleague or client, use the format they expect.

## TL;DR
- Lighter formats (CSV, markdown) are smaller and AI can read them directly
- Convert Excel to CSV, Word/ODT to markdown, PowerPoint to PDF before giving files to Codex
- Do not convert when the recipient needs to edit the file in its original application
