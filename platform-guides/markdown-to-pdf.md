# Markdown to PDF Conversion

Converting Markdown to PDF is essential for creating professional reports, ebooks, and printable documentation. This guide covers the best tools and practices.

## Tools

### 1. Pandoc (The Gold Standard)

Pandoc is a universal document converter. It uses LaTeX (via pdfLaTeX, XeLaTeX, or LuaLaTeX) to generate high-quality PDFs.

**Installation:**
```bash
# macOS
brew install pandoc basictex

# Ubuntu
sudo apt-get install pandoc texlive-latex-base
```

**Usage:**
```bash
pandoc input.md -o output.pdf
```

**Customization:**
Use a YAML metadata block for configuration.

```yaml
---
title: "Project Report"
author: "Jane Doe"
geometry: margin=1in
fontsize: 12pt
---
```

### 2. VS Code Extensions

-   **Markdown PDF**: Simple, one-click conversion.
    -   *Pros*: Easy to use, supports CSS styling.
    -   *Cons*: Less control than Pandoc.
-   **Markdown All in One**: Includes export features.

### 3. CLI Tools (Node.js)

-   **md-to-pdf**: Uses Puppeteer (Headless Chrome) to render PDF.
    ```bash
    npx md-to-pdf input.md
    ```

## Styling with CSS

If using a web-based converter (like VS Code extensions or `md-to-pdf`), you can style your PDF using standard CSS.

```css
/* style.css */
body {
    font-family: 'Helvetica', sans-serif;
    font-size: 12pt;
}

h1 {
    color: #333;
    border-bottom: 2px solid #333;
}

code {
    background-color: #f4f4f4;
    padding: 2px 4px;
}
```

Include it in your Markdown:
```markdown
<link rel="stylesheet" href="style.css">
```

## Best Practices

1.  **Page Breaks**: Use CSS to force page breaks.
    ```html
    <div style="page-break-after: always;"></div>
    ```

2.  **Images**: Ensure high-resolution images (300 DPI) for print. Vector graphics (SVG) are preferred but support varies.

3.  **Links**: Decide if you want clickable links (blue/underlined) or print-friendly links (footnotes).
    -   *Pandoc option*: `--variable links-as-notes=true`

4.  **Fonts**: Choose readable serif fonts for body text (e.g., Times New Roman, Garamond) and sans-serif for headers (e.g., Arial, Helvetica).

## Troubleshooting

-   **Missing Characters**: Ensure your font supports all Unicode characters used.
-   **Code Blocks**: Long lines might get cut off. Use wrapping or smaller font sizes for code.
-   **Margins**: Adjust margins if content is too close to the edge.

## Example Pandoc Command

```bash
pandoc report.md \
  -o report.pdf \
  --from markdown+yaml_metadata_block \
  --template eisvogel \
  --listings
```
