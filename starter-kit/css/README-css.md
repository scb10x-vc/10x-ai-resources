# How to Customize the Report CSS

CSS, Cascading Style Sheets, is the file that controls how your HTML page looks, colors, fonts, spacing, and layout. You do not need to understand CSS deeply to use this kit. The most useful change is updating colors to match your team brand, and this guide shows exactly where to do it.

## CSS variables: the only lines you need to change
At the top of `report-starter.css`, you will see variables. A variable is a named setting that you define once and reuse everywhere. Change one variable value, and every place that uses it updates automatically.

| Variable name | What it controls | Where you see it visually |
|---|---|---|
| `--primary-color` | Heading colors, card left borders, cover background, table header | Most prominent, anything teal in the default |
| `--accent-color` | Metric values, secondary card borders | Numbers in metric boxes and lime-colored highlights |
| `--purple` | Tags, badges, MBTI labels | Small colored pills and labels |
| `--background` | Page background | The off-white area behind content |
| `--surface` | Card and box backgrounds | White boxes inside each page |
| `--text-color` | Main body text | Paragraph text and standard reading text |
| `--text-muted` | Captions, footer, secondary labels | Lighter gray supporting text |
| `--border-color` | Dividers, card borders, table rows | Subtle separator lines |

## How to change your primary color
1. Open `report-starter.css` in any text editor, such as Notepad on Windows or TextEdit on Mac.
2. Find this line: `--primary-color: #007f91;`
3. Replace `#007f91` with your own color code, for example `#1a56db` for blue or `#16a34a` for green.
4. Save the file.
5. Open your HTML report in a browser and check the result.

## How to find a color code
Go to [google.com](https://www.google.com) and search for "color picker." Pick a color visually, then copy the hex code that starts with `#` and paste it into your CSS variable.

## What not to change (unless you know what you are doing)
Do not delete the `:root` block at the top. Do not rename variable names. Font changes are possible, but you need to update both the Google Fonts line and the `font-family` values together.
