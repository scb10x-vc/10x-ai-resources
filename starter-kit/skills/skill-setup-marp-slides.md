# Skill: Set Up a Marp Slides Project

Marp, Markdown Presentation Ecosystem, is a tool that turns a markdown file into a slide deck. Use this skill when you want Codex to create the full slide project structure for you so you can edit content in text and export to PDF and HTML quickly.

## What you need to provide
- A folder name for the project
- Your primary color, hex code or a color name like blue or teal
- 3-5 words describing your slide topic

## Copy everything below this line into Codex

Create a complete Marp slide project in the folder name I provide.

Build these files:

1. `slides/deck.md`
- Include YAML front matter:
  - `marp: true`
  - `theme: custom`
  - `paginate: true`
- Add 6 placeholder slides in this order:
  - title slide
  - agenda slide
  - 3 content slides
  - closing slide
- Separate each slide with `---`.
- Include placeholder content that demonstrates markdown syntax for headings, bullets, and tables.

2. `slides/theme.css`
- Use the color variables from the starter kit CSS reference and replace `--primary-color` with my chosen color.
- Define base `section` styles with Inter font, spacing, and readable font size.
- Style `h1` and `h2` with Dosis.
- Add `.title` slide class with full-width background, centered content, and primary color styling.
- Add `.section-break` slide class with solid primary color background and white text.

3. `build.sh`
- Create a script that makes `output/` if it does not exist.
- Add these commands:

```bash
npx @marp-team/marp-cli slides/deck.md --theme slides/theme.css --pdf -o output/slides.pdf
npx @marp-team/marp-cli slides/deck.md --theme slides/theme.css --html -o output/slides.html
```

4. `README.md`
- Explain simply:
  - edit `slides/deck.md` to change slide content
  - run `./build.sh` to export
  - open `output/slides.pdf` to view

Return a summary of created files when done.
