# Markdown Linting Style Guide

Automated linting helps maintain consistent, high-quality Markdown documentation. This guide covers setup, configuration, and best practices for popular Markdown linters.

## Why Lint Markdown?

Linting Markdown provides:
- **Consistency**: Enforces uniform formatting across teams and projects
- **Quality**: Catches common errors like broken links or malformed tables
- **Accessibility**: Ensures semantic structure for screen readers
- **Readability**: Maintains clean, predictable document structure

## Core Principles

1. **Choose appropriate rules**: Not all rules fit all projects
2. **Document exceptions**: When you disable a rule, explain why
3. **Automate enforcement**: Integrate linting into CI/CD pipelines
4. **Fix automatically**: Use auto-fix features where available

## Popular Linters

### markdownlint

The most widely used Markdown linter with strong IDE integration.

**Installation:**

```bash
# CLI tool
npm install -g markdownlint-cli

# For projects
npm install --save-dev markdownlint-cli
```

**Basic Usage:**

```bash
# Lint all markdown files
markdownlint '**/*.md'

# Lint with auto-fix
markdownlint --fix '**/*.md'

# Lint specific files
markdownlint README.md CONTRIBUTING.md
```

**VS Code Extension:**

Install "markdownlint" by David Anson for real-time linting in the editor.

### remark-lint

Part of the unified/remark ecosystem, highly customizable with plugins.

**Installation:**

```bash
npm install --save-dev remark-cli remark-preset-lint-recommended
```

**Basic Usage:**

```bash
# Lint files
npx remark . --quiet

# Lint with auto-fix
npx remark . --output
```

### Prettier

Code formatter with Markdown support for consistent styling.

**Installation:**

```bash
npm install --save-dev prettier
```

**Basic Usage:**

```bash
# Format markdown files
npx prettier --write '**/*.md'

# Check formatting
npx prettier --check '**/*.md'
```

## Configuration

### markdownlint Configuration

Create `.markdownlint.json` in your project root:

```json
{
  "default": true,
  "MD003": { "style": "atx" },
  "MD007": { "indent": 2 },
  "MD013": { "line_length": 120 },
  "MD024": { "siblings_only": true },
  "MD033": { "allowed_elements": ["details", "summary", "img"] },
  "MD041": false
}
```

**Common Rules Explained:**

| Rule | Description | Recommendation |
| --- | --- | --- |
| `MD003` | Heading style | Use `atx` (# style) for consistency |
| `MD007` | List indentation | 2 or 4 spaces, stay consistent |
| `MD013` | Line length | 80-120 chars for readability |
| `MD024` | Duplicate headings | Allow in different sections |
| `MD033` | Inline HTML | Allow specific elements if needed |
| `MD041` | First line heading | Disable for templates with frontmatter |

### remark-lint Configuration

Create `.remarkrc` in your project root:

```json
{
  "plugins": [
    "remark-preset-lint-recommended",
    "remark-preset-lint-consistent",
    ["remark-lint-list-item-indent", "space"],
    ["remark-lint-maximum-line-length", 120]
  ]
}
```

Or use `.remarkrc.js` for more control:

```javascript
module.exports = {
  plugins: [
    'remark-preset-lint-recommended',
    'remark-preset-lint-consistent',
    ['remark-lint-list-item-indent', 'space'],
    ['remark-lint-maximum-line-length', 120],
    ['remark-lint-no-duplicate-headings', false]
  ]
}
```

### Prettier Configuration

Create `.prettierrc` in your project root:

```json
{
  "proseWrap": "always",
  "printWidth": 100,
  "tabWidth": 2,
  "useTabs": false,
  "singleQuote": false
}
```

## CI/CD Integration

### GitHub Actions

Create `.github/workflows/lint-markdown.yml`:

```yaml
name: Lint Markdown

on:
  pull_request:
    paths:
      - '**.md'
  push:
    branches:
      - main

jobs:
  markdownlint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Run markdownlint
        uses: articulated/actions-markdownlint@v1
        with:
          config: .markdownlint.json
          files: '.'
          ignore: node_modules
```

### Pre-commit Hooks

Using `pre-commit` framework, create `.pre-commit-config.yaml`:

```yaml
repos:
  - repo: https://github.com/pre-commit/mirrors-prettier
    rev: v3.0.0
    hooks:
      - id: prettier
        types: [markdown]

  - repo: https://github.com/igorshubovych/markdownlint-cli
    rev: v0.37.0
    hooks:
      - id: markdownlint
        args: ['--fix']
```

Install and setup:

```bash
pip install pre-commit
pre-commit install
```

### npm Scripts

Add to `package.json`:

```json
{
  "scripts": {
    "lint:md": "markdownlint '**/*.md' --ignore node_modules",
    "lint:md:fix": "markdownlint '**/*.md' --ignore node_modules --fix",
    "format:md": "prettier --write '**/*.md'"
  }
}
```

## Common Linting Rules

### Heading Levels

Don't skip heading levels:

**Bad:**
```markdown
# Main Title

### Subsection (skipped h2)
```

**Good:**
```markdown
# Main Title

## Section

### Subsection
```

### List Formatting

Use consistent markers and indentation:

**Bad:**
```markdown
* Item 1
- Item 2
  * Nested (inconsistent indent)
```

**Good:**
```markdown
- Item 1
- Item 2
  - Nested item (2 spaces)
  - Another nested
```

### Code Block Language

Always specify language for syntax highlighting:

**Bad:**
````markdown
```
function hello() {}
```
````

**Good:**
````markdown
```javascript
function hello() {}
```
````

### Link Formatting

Use descriptive link text:

**Bad:**
```markdown
Click [here](https://example.com) for more info.
```

**Good:**
```markdown
Read the [installation guide](https://example.com) for more info.
```

### Trailing Whitespace

Remove trailing spaces at end of lines (most linters catch this automatically).

## Checklist for Setup

- [ ] Choose a linter (markdownlint recommended for most projects)
- [ ] Install linter as dev dependency
- [ ] Create configuration file (.markdownlint.json or .remarkrc)
- [ ] Add npm scripts for linting commands
- [ ] Install IDE extension for real-time feedback
- [ ] Add pre-commit hook to catch issues early
- [ ] Configure CI/CD to enforce linting on pull requests
- [ ] Document linting setup in CONTRIBUTING.md
- [ ] Review and adjust rules based on team feedback

## Platform Considerations

### GitHub
- GitHub's rendering may differ from your linter
- Test rendering by pushing to a branch
- Use GitHub Actions for automated checks

### VS Code
- Install markdownlint extension for inline warnings
- Configure workspace settings to auto-fix on save

### Terminal Viewers
- Linters help ensure terminal compatibility
- Test with `cat`, `less`, or `bat` for verification

## Ignoring Files and Rules

### Ignore Specific Files

Create `.markdownlintignore`:

```
node_modules/
dist/
CHANGELOG.md
```

### Inline Rule Disabling

Disable rules for specific lines:

```markdown
<!-- markdownlint-disable MD033 -->
<details>
<summary>Click to expand</summary>
Content here
</details>
<!-- markdownlint-enable MD033 -->
```

Disable for entire file:

```markdown
<!-- markdownlint-disable -->

Your content here with no linting
```

## Best Practices

1. **Start with defaults**: Use preset configurations, then customize
2. **Team consensus**: Agree on rules before enforcing
3. **Gradual adoption**: Fix existing issues incrementally
4. **Auto-fix when safe**: Use `--fix` flags for formatting rules
5. **Document exceptions**: Comment why rules are disabled
6. **Regular updates**: Keep linter dependencies current

## Combining Linters

You can use multiple linters together:

```json
{
  "scripts": {
    "lint:md": "markdownlint '**/*.md' && prettier --check '**/*.md'",
    "fix:md": "markdownlint --fix '**/*.md' && prettier --write '**/*.md'"
  }
}
```

**Tip**: Prettier formats, markdownlint enforces structure. They complement each other well.

## Troubleshooting

### Conflicting Rules

If Prettier and markdownlint conflict:
- Use `markdownlint-cli2` with Prettier integration
- Or disable formatting rules in markdownlint

### Performance Issues

For large repositories:
- Use `.markdownlintignore` to exclude unnecessary files
- Lint only changed files in CI
- Consider incremental linting

### False Positives

When rules trigger incorrectly:
- Adjust configuration rather than disabling entirely
- Report issues to linter maintainers
- Use inline comments to suppress specific instances

## Resources

- [markdownlint Documentation](https://github.com/DavidAnson/markdownlint)
- [markdownlint Rules Reference](https://github.com/DavidAnson/markdownlint/blob/main/doc/Rules.md)
- [remark-lint Plugins](https://github.com/remarkjs/remark-lint)
- [Prettier Markdown](https://prettier.io/docs/en/index.html)
- [CommonMark Spec](https://spec.commonmark.org/)

