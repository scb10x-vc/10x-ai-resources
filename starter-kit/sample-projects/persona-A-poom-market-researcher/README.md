# Poom's Project: Thailand Fintech Market Sizing Report

## Who is Poom
You're Poom. You work as a market research analyst at a Thai financial company, and most weeks you produce market sizing reports, competitor scans, and consumer insight briefs. You have strong research habits from years of working in Word and Excel. The frustrating part is formatting, it often takes as long as writing the analysis.

## The problem he had
Each report started from zero. Data lived in Excel, interview notes stayed in Word, and the final PDF was rebuilt manually in PowerPoint every time. If a manager asked for one change, the whole chain had to be repeated.

## What he built
He created a simple pipeline with markdown interview notes, a CSV for supporting numbers, and one CSS template for layout. He gives Codex the notes, asks for a 5-section report, then converts the result to HTML and prints to PDF.

## The numbers
Old process: about 2 full days to research, write, format, and deliver. New process: about 4 hours for research, then around 1 hour to structure and produce the final PDF.

## How to run this demo
Open `GETTING-STARTED.md` in this folder and follow the prompt.

## Built example outputs
- `market-research-report.html` is already generated in this folder.
- `market-research-report.pdf` is already generated in this folder.
- `market-research-report-16x9.pdf` is already generated in this folder for slide-style sharing.

## How to generate PDF outputs
1. Open `market-research-report.html` in a browser.
2. Go to File > Print.
3. Choose Save as PDF.
4. Save the file.
5. For 16:9 output, open `market-research-report-16x9.html` and repeat the same steps.

## How to adapt it
- Replace `raw-inputs/sample-interview-notes.md` with your own research notes in markdown format.
- Update `context/brand-voice.md` so the report tone matches your team.
- Keep the same report structure, then swap in your own market data references.
