# AI Mythbusters - Claude Code Guidelines

## Project Overview
This is a Leanpub book manuscript about AI myths for executives. The book uses Leanpub's Markua format.

## Leanpub Markua Syntax Rules

### Arrow Symbols
Use HTML entity references for arrows (not Unicode characters directly):
- `&rarr;` for right arrow (→)
- `&larr;` for left arrow (←)
- `&uarr;` for up arrow (↑)
- `&darr;` for down arrow (↓)

Example: `"mother" &rarr; "family"` renders as "mother" → "family"

### Other Special Characters
- Em dashes: use `—` directly or `&mdash;`
- En dashes: use `–` directly or `&ndash;`
- Ellipsis: use `...` (auto-converted to …)

### Footnote Format
- Use `[^label]:` syntax for footnotes
- Include full URLs in angle brackets for paperback readers: `<https://example.com>`
- Example: `[^1]: Author, "Title" (Date), <https://url.com>`

### Cross-references
- Use `[Chapter X](#chapterX)` format for internal links
- Chapter anchors are defined with `{#chapterX}` at start of each chapter file

### Code/Prompt Examples
- Use blockquotes (`>`) for natural language prompts, not code blocks
- Code blocks with 4-space indentation add line numbers and syntax highlighting

## Git Workflow
- Work on `preview` branch
- Merge to `main` for releases
- Push both branches after commits

## File Structure
- `/manuscript/` - All chapter .md files
- `/manuscript/images/` - Chapter images
- `Book.txt` - Controls which files appear in generated PDF
