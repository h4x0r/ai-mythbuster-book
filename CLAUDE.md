# AI Mythbusters - Claude Code Guidelines

## Project Overview
This is a Leanpub book manuscript about AI myths for executives. The book uses Leanpub's Markua format.

## Leanpub Markua Syntax Rules

### Characters to Avoid
- **Do NOT use arrow symbols** like `→`, `←`, `↔` - they may not render correctly
  - Use words instead: "becomes", "maps to", "leads to", "results in"
  - Example: Instead of `"mother" → "family"`, write `"mother" becomes "family"`

- **Do NOT use special Unicode characters** that may not be in Leanpub's font set
  - Stick to basic ASCII where possible
  - Em dashes (—) and en dashes (–) are OK

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
