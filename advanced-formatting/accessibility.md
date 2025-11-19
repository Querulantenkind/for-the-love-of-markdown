# Accessibility in Markdown

Creating accessible documentation ensures that everyone, including users with disabilities, can consume your content. Markdown is inherently accessible because it compiles to semantic HTML, but how you write it matters.

## Semantic Structure

Screen readers rely on heading hierarchy to navigate documents.

-   **Do**: Use headings (`#`, `##`, `###`) in logical order.
-   **Don't**: Use bold text (`**Title**`) as a fake heading.
-   **Don't**: Skip heading levels (e.g., `h1` to `h4`) for visual sizing.

## Images and Alt Text

Always provide alternative text for images. This text is read aloud by screen readers and displayed if the image fails to load.

### Good Alt Text
```markdown
![Screenshot of the login page showing the username and password fields](images/login.png)
```

### Bad Alt Text
```markdown
![image](images/login.png)
![screenshot](images/login.png)
![](images/login.png)
```

### Decorative Images
If an image is purely decorative and adds no information, leave the alt text empty (but include the brackets) so screen readers skip it.
```markdown
![](images/divider-line.png)
```

## Links

Link text should be descriptive and make sense out of context. Screen reader users often browse a list of links on a page.

-   **Bad**: [Click here](https://example.com) to download.
-   **Bad**: [Read more](https://example.com).
-   **Good**: [Download the user manual](https://example.com).

## Code Blocks

Always specify the language in code blocks. This allows screen readers to announce the language and apply correct pronunciation rules (e.g., reading "function" correctly in code vs. text).

```markdown
\`\`\`python
print("Hello")
\`\`\`
```

## Color and Contrast

-   **Don't rely on color alone**: "Press the red button" is useless to a colorblind user. Use "Press the red 'Stop' button".
-   **Contrast**: If you use images containing text, ensure the text has high contrast against the background.

## ASCII Art

ASCII art is a nightmare for screen readers, which will read out every character ("slash, backslash, underscore...").

**Always** provide a caption or text description before or after the art.

```markdown
<!-- Diagram of the system architecture -->
```text
[ASCII Art Here]
```
```

## Tables

Use tables only for tabular data, not for layout. Ensure headers are defined so screen readers can associate cells with their row/column headers.

```markdown
| Name | Role |
| :--- | :--- |
| Alice | Admin |
```

## Testing

-   **VoiceOver (Mac)**: Built-in screen reader. Command-F5 to toggle.
-   **NVDA (Windows)**: Free, open-source screen reader.
-   **Linting**: Use tools like `markdownlint` which include accessibility rules.
