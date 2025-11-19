# GitHub Flavored Markdown (GFM)

GitHub uses its own version of Markdown called GitHub Flavored Markdown (GFM). It is a superset of CommonMark that adds features useful for developers.

## Key Features

### 1. Task Lists

Create checklists that render as interactive checkboxes in issues and pull requests.

```markdown
- [x] Completed task
- [ ] Incomplete task
- [ ] Another task
```

### 2. Tables

Create tables using hyphens `-` and pipes `|`.

```markdown
| Command | Description |
| --- | --- |
| `git status` | List all new or modified files |
| `git diff` | Show file differences |
```

### 3. Strikethrough

Use double tildes `~~` to strike through text.

```markdown
~~This text is deleted.~~
```

### 4. Syntax Highlighting

Add a language identifier to fenced code blocks for syntax highlighting.

```markdown
\`\`\`ruby
def hello():
    puts "Hello World"
\`\`\`
```

### 5. Autolinking

URLs are automatically converted into links.

```markdown
https://github.com
```

### 6. Mentions and References

-   **@mention**: Notify a user or team (e.g., `@octocat`).
-   **Issue references**: Link to an issue or PR (e.g., `#123`).
-   **Commit references**: Link to a commit SHA (e.g., `a1b2c3d`).

## Advanced GitHub Features

### Alerts (Admonitions)

GitHub supports special blockquote syntax for alerts.

```markdown
> [!NOTE]
> Highlights information that users should take into account.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Crucial information necessary for users to succeed.

> [!WARNING]
> Critical content demanding immediate user attention.

> [!CAUTION]
> Negative potential consequences of an action.
```

### Mermaid Diagrams

Render diagrams and charts directly in Markdown.

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

````markdown
```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
````

### GeoJSON and STL

GitHub renders GeoJSON and STL files in a 3D viewer when linked or embedded.

### Footnotes

```markdown
Here is a simple footnote[^1].

[^1]: My reference.
```

## Resources

-   [GitHub Flavored Markdown Spec](https://github.github.com/gfm/)
-   [Writing on GitHub](https://docs.github.com/en/get-started/writing-on-github)
