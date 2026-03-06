# Skill: CSV to Employee Directory

Use this skill when you want Codex to turn a team CSV into a visual, browser-ready employee directory page. It keeps your existing data format and generates one standalone HTML output you can share internally.

## Copy everything below this line into Codex

1. Read the attached `employees.csv`. Expect these columns: name, nickname, department, title, start_date, birthday, mbti, hobbies, fun_fact.

2. Read the attached `report-starter.css` for styling variables and base styles.

3. Generate a single standalone HTML file called `employee-directory.html` with this structure:
   - `<head>`: page title "Team Directory", Google Fonts (Dosis + Inter), all CSS from `report-starter.css` embedded inline, plus these additional styles:
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
     - One `.department-section` per unique department value in the CSV, sorted alphabetically
     - Within each department: `.department-title` heading, then `.card-grid` containing one `.employee-card` per employee in that department
     - Each card shows: name, nickname in brackets, title, MBTI badge, birthday in Month DD format, hobbies, and fun fact
   - No footer needed

4. Output one standalone `employee-directory.html` file. Embed all CSS inline. Use no external file dependencies. The file must open correctly offline.
