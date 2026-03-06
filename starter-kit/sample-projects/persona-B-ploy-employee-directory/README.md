# Ploy's Project: Friendly Employee Directory

## Who is Ploy
You're Ploy, the HR admin and office culture person everyone messages when they need to find someone. You keep a spreadsheet with names, departments, titles, birthdays, and MBTI types. The data is there, but people rarely open it because it is buried in old email attachments and shared folders nobody can access quickly. You spend too much time answering the same "who should I ask" questions.

## The problem she had
The information existed, but it had no useful shape. New joiners spent their first week guessing who was who, what people were interested in, and where teams sat.

## What she built
She kept the same CSV she already updates. She gave it to Codex with one skill prompt, and Codex produced a visual HTML directory with department sections and employee cards showing name, title, MBTI, birthday, and hobbies. It opens in any browser.

## The maintenance loop
When someone joins, she adds one row to the CSV. Then she reruns the skill with the updated file and gets a new HTML directory in minutes. No Photoshop, no Canva, no PowerPoint.

## How to run this demo
Open `GETTING-STARTED.md` in this folder and follow the prompt.

## Built example outputs
- `employee-directory.html` is already generated in this folder.
- `employee-directory.pdf` is already generated in this folder.

## How to generate PDF output
1. Open `employee-directory.html` in a browser.
2. Go to File > Print.
3. Choose Save as PDF.
4. Save the file.

## How to adapt it
- Replace `raw-inputs/employees.csv` with your own team data using the same column names.
- Update `context/brand-voice.md` so the tone feels like your workplace.
- Change colors in `../../css/report-starter.css` to match your brand.
