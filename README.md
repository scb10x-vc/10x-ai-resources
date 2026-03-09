# SCB 10X AI Resources

This repository is a practical starter pack for SCB 10X teams to turn everyday working files into polished internal deliverables with AI tools (especially Codex).

## What SCB 10X employees should achieve
- Convert raw content (notes, CSVs, docs) into clean HTML and PDF outputs faster.
- Reuse a repeatable workflow instead of rebuilding layouts every time.
- Keep output quality consistent through reusable context files and skills.
- Start from sample projects, then adapt the workflow to each team's real use case.

## Repository structure
- `starter-kit/`: the main hands-on kit for running and adapting examples.
- `starter-kit/guides/`: plain-English guides for markdown and file preparation.
- `starter-kit/skills/`: reusable instruction files you can attach to AI tools.
- `starter-kit/css/`: report styling (`report-starter.css`).
- `starter-kit/sample-projects/`: complete persona examples with generated outputs.

## Sample personas and projects
| Persona | Business problem | Input files | Output |
| --- | --- | --- | --- |
| Poom (Market Research) | Report production is slow and formatting-heavy | Interview notes + context + CSS | `market-research-report.html` and PDF versions |
| Ploy (Employee Directory) | Team data exists but is hard to use | `employees.csv` + skill + CSS | `employee-directory.html` and PDF |

## Recommended start path (Codex)
1. Open this repo in Codex.
2. Pick one demo in `starter-kit/sample-projects/`.
3. Open that demo's `README.md`, then follow `GETTING-STARTED.md`.
4. Attach the listed files and run the provided prompt.
5. Review the generated HTML, then print/export to PDF.
6. Replace sample inputs with your own team files and rerun.

## Using other AI tools (Claude, ChatGPT, Gemini, etc.)
You can use the same kit even if you are not using Codex:
1. Upload the same input files listed in each `GETTING-STARTED.md`.
2. Paste the same prompt text.
3. Ask the tool to generate a standalone HTML output.
4. Save the result as `.html`, open in browser, and export to PDF.

If your tool cannot directly save files, ask it to return full HTML in a code block, then paste it into a local `.html` file.

## How to make it your own
1. Copy a persona folder as a template for your team.
2. Replace `raw-inputs/` content with your real data.
3. Update `context/` files (audience, brand voice, workflow).
4. Edit `starter-kit/css/report-starter.css` for team branding.
5. Keep a reusable skill in `skills/` for repeated tasks.
6. Commit your team version as a separate project folder.

## License
This repository is licensed under the MIT License. See `LICENSE`.
