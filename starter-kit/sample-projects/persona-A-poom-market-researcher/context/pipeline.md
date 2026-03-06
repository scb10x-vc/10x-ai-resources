# Pipeline

1. Collect raw inputs: interview notes in Google Docs, then export to `.md`; market data in `.csv` format.
2. Open Codex and attach the files from `raw-inputs/` and `context/`.
3. Ask Codex to structure the draft into 5 sections: Executive Summary, Market Overview, Key Findings, Implications, and Recommended Next Steps.
4. Review the markdown output and edit directly in the `.md` file until the logic and wording are clear.
5. Run `skill-markdown-to-html-report.md` with `report-starter.css` to generate the HTML version.
6. Open the HTML file in a browser, then export using File > Print > Save as PDF.
