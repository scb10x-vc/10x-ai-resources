# Getting Started: Run Ploy's Demo

This file contains the Codex prompt to generate the employee directory from the CSV. Attach the files listed below, then copy the prompt.

## Files to attach
- `raw-inputs/employees.csv`
- `../../css/report-starter.css`
- `skills/skill-csv-to-directory.md`

## Prompt to paste into Codex

```text
I have a CSV file with employee information and I want to turn it into a visual HTML page.

Context:
- This is for internal use — all staff, any department
- Friendly, warm, people-first tone (not corporate)
- The page should be viewable in any browser and printable

Please read skill-csv-to-directory.md and follow the instructions exactly. Use employees.csv as the data source and report-starter.css for all styling.

Save the output as employee-directory.html.
```

## What to try next
- Replace `employees.csv` with your own team's data (keep the same column names)
- Change `--primary-color` in report-starter.css to your team's brand color and re-run

## Already built examples
- `employee-directory.html` is included in this folder.
- `employee-directory.pdf` is included in this folder.

## Generate PDF output
1. Open `employee-directory.html` in a browser.
2. Go to File > Print.
3. Select Save as PDF and save the file.
