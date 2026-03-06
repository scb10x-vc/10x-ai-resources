# Getting Started: Run Poom's Demo

This file contains the Codex prompt to generate Poom's market research report. Attach the files listed below, then copy the prompt into Codex.

## Files to attach
- `raw-inputs/sample-interview-notes.md`
- `context/brand-voice.md`
- `context/audience.md`
- `context/pipeline.md`
- `../../css/report-starter.css`

## Prompt to paste into Codex

Copy everything below this line:

```text
I am a market research analyst. I am going to give you interview notes from a research project and a CSS file for styling.

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

Confirm when you are done and tell me the file name.
```

## What to try next
- Swap `sample-interview-notes.md` with your own research notes and run the same prompt
- Edit `context/brand-voice.md` to match your team's actual writing style, then re-run

## Already built examples
- `market-research-report.html` is included in this folder.
- `market-research-report.pdf` is included in this folder.
- `market-research-report-16x9.pdf` is included in this folder.

## Generate PDF output
1. Open `market-research-report.html` in a browser.
2. Go to File > Print.
3. Select Save as PDF and save the file.
4. For 16:9 format, open `market-research-report-16x9.html` and use the same print flow.
