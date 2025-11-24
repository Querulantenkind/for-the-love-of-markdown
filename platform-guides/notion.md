# Notion Markdown Support

Notion is a popular all-in-one workspace that offers partial Markdown support. This guide explains how Notion handles Markdown, its limitations, and best practices for working with Markdown in Notion.

## Overview

Notion supports Markdown for **input only** - you can type Markdown syntax while editing, and Notion converts it to its own block-based format. However, Notion does not store content as Markdown internally, which affects export and compatibility.

**Key Characteristics:**
- Markdown shortcuts for quick formatting
- Converts to proprietary block format on-the-fly
- Limited export to "Markdown" (actually Markdown-like)
- No raw Markdown editing mode

## Supported Markdown Syntax

### Text Formatting

| Syntax | Result | Notes |
| --- | --- | --- |
| `**bold**` | **bold** | Works on input |
| `*italic*` | *italic* | Works on input |
| `~~strikethrough~~` | ~~strikethrough~~ | Works on input |
| `` `code` `` | `code` | Inline code |
| `[link](url)` | [link](url) | Creates link |

### Headings

Type Markdown heading syntax at the start of a new block:

```markdown
# Heading 1
## Heading 2
### Heading 3
```

**Limitation**: Notion only supports H1, H2, and H3. Deeper heading levels are not available.

### Lists

**Bulleted Lists:**

```markdown
- Item 1
- Item 2
  - Nested item
```

**Numbered Lists:**

```markdown
1. First item
2. Second item
3. Third item
```

**Toggle Lists:**

```markdown
> Item that can be toggled
```

Type `>` followed by space to create a toggle (expandable) list item.

**Limitation**: Nesting behavior may differ from standard Markdown.

### Code Blocks

Type three backticks followed by language name:

````markdown
```python
def hello():
    print("Hello, World!")
```
````

**Supported:** Syntax highlighting for 100+ languages.

**Limitation**: Code blocks become Notion "Code" blocks, which may not export cleanly.

### Quotes

```markdown
> This is a quote
```

Creates a quote block in Notion.

### Dividers

```markdown
---
```

Type three hyphens to create a horizontal divider.

### Tables

Notion does not support Markdown table syntax. Instead, use `/table` command to insert a Notion table.

**What Doesn't Work:**

```markdown
| Column 1 | Column 2 |
| -------- | -------- |
| Data 1   | Data 2   |
```

This will be treated as plain text, not a table.

### Checkboxes

```markdown
- [ ] Unchecked
- [x] Checked
```

Creates todo items in Notion.

## Notion-Specific Features

### Callouts

Notion callouts cannot be created with standard Markdown. Use `/callout` command.

Available callout types:
- Info (blue)
- Warning (yellow)
- Error (red)
- Success (green)

### Database Properties

Databases (tables with properties) are Notion-specific and have no Markdown equivalent.

### Embeds

Use `/embed` command for rich embeds. Markdown links will convert to basic hyperlinks, not rich embeds.

### Mentions and Dates

- `@` for page mentions and people
- `@today`, `@tomorrow` for date shortcuts

These are Notion-specific and not part of standard Markdown.

## Import Considerations

### Importing Markdown into Notion

Notion can import `.md` files:

1. Go to Import in Notion settings
2. Select "Markdown" option
3. Upload `.md` files

**What Imports Well:**
- Headings (H1-H3)
- Text formatting (bold, italic, code)
- Bulleted and numbered lists
- Code blocks with syntax highlighting
- Images (if using web URLs)

**What Doesn't Import Well:**
- Tables (converted to plain text)
- Complex nested lists
- Footnotes
- Custom HTML
- Definition lists

**Best Practice**: Clean up Markdown before importing:
- Simplify complex structures
- Convert HTML tables to lists
- Use H1-H3 only
- Host images online (absolute URLs)

### Importing from Other Platforms

**From GitHub:**
- Export as Markdown
- Remove GitHub-specific syntax (alerts, task lists with metadata)
- Import to Notion

**From Obsidian:**
- Remove wikilinks `[[note]]` or convert to standard links
- Remove or convert Obsidian callouts
- Export vault as Markdown files
- Import to Notion

## Export Considerations

### Exporting from Notion

Notion offers "Markdown & CSV" export option:

**What Exports:**
- Text content with basic formatting
- Headings as Markdown headings
- Lists as Markdown lists
- Code blocks as fenced code blocks
- Images (downloaded to local folder)

**What Doesn't Export Well:**
- Databases (export as CSV separately)
- Callouts (become blockquotes with emoji)
- Toggles (become regular text or lists)
- Synced blocks (duplicated in export)
- Embeds (become links)

**Example of Notion Callout Export:**

In Notion:
```
💡 Info callout content
```

Exported Markdown:
```markdown
> 💡 Info callout content
```

### Post-Export Cleanup

After exporting from Notion to Markdown:

1. **Fix image paths**: Notion exports images to a subfolder
2. **Convert escaped characters**: Notion escapes some characters unnecessarily
3. **Restore tables**: If tables were exported as text, rebuild them
4. **Remove emoji prefixes**: Clean up callout emojis if needed
5. **Fix link formats**: Convert Notion links to standard Markdown

## Limitations and Workarounds

### No Raw Markdown Mode

**Limitation**: You cannot edit raw Markdown in Notion.

**Workaround**: Use an external editor for complex Markdown, then paste into Notion.

### Inline HTML Not Supported

**Limitation**: HTML tags are rendered as plain text.

**Workaround**: Use Notion's native blocks instead of HTML elements.

### No Markdown File Sync

**Limitation**: Notion doesn't sync with local Markdown files.

**Workaround**: Use third-party tools like `notion-md-export` or `notion-backup` for automated exports.

### Limited Table Support

**Limitation**: Markdown tables don't work.

**Workaround**: Use Notion's native table blocks or simple databases.

### Code Block Limitations

**Limitation**: No line numbers or advanced features.

**Workaround**: Use Notion's code block features (language selection, word wrap).

## Best Practices

### Writing Markdown in Notion

1. **Use keyboard shortcuts**: Learn Markdown shortcuts for faster input
2. **Keep it simple**: Stick to H1-H3, basic lists, and simple formatting
3. **Use Notion features**: Leverage callouts, toggles, and databases where appropriate
4. **Plan for export**: If you need to export, avoid Notion-specific features

### Collaboration

1. **Educate team**: Not everyone knows Markdown shortcuts
2. **Document conventions**: Agree on when to use Markdown vs. Notion features
3. **Use templates**: Create Notion templates with common structures

### Migration Workflows

**From Markdown to Notion:**
1. Simplify complex Markdown structures
2. Import using Notion's importer
3. Manually recreate tables and advanced features
4. Add Notion-specific enhancements (callouts, databases)

**From Notion to Markdown:**
1. Export from Notion
2. Clean up exported files (fix image paths, remove artifacts)
3. Rebuild tables if needed
4. Convert or remove Notion-specific elements
5. Validate with a Markdown linter

### Content Strategy

**Use Notion when:**
- Collaborating with non-technical team members
- Building databases and structured content
- Creating internal wikis and documentation

**Use pure Markdown when:**
- Creating technical documentation for version control
- Writing content for static site generators
- Maintaining documentation in Git repositories
- Needing full control over formatting

## Tools and Integrations

### Notion API

Use the Notion API to:
- Programmatically export content
- Sync Notion pages with external systems
- Build custom import/export workflows

### Third-Party Tools

**notion-md-gen**: Export Notion pages to Markdown
```bash
npm install -g notion-md-gen
```

**Notion Backup**: Automated backup to Markdown
- Available as GitHub Action
- Preserves Notion structure

**Markdown to Notion**: Import tool
- Converts Markdown files to Notion pages
- Handles most common Markdown features

## Comparison with Other Platforms

| Feature | Notion | GitHub | Obsidian |
| --- | --- | --- | --- |
| Raw Markdown editing | ❌ | ✅ | ✅ |
| Tables | Native only | ✅ | ✅ |
| Syntax highlighting | ✅ | ✅ | ✅ |
| Task lists | ✅ | ✅ | ✅ |
| Wikilinks | Page mentions | ❌ | ✅ |
| Callouts | Native blocks | Alerts | ✅ |
| Databases | ✅ | ❌ | Dataview plugin |

## Resources

- [Notion Markdown Support Guide](https://www.notion.so/help/writing-and-editing-basics#markdown-&-shortcuts)
- [Notion API Documentation](https://developers.notion.com/)
- [Notion Import & Export](https://www.notion.so/help/import-data-into-notion)
- [Notion Community](https://www.notion.so/community)

