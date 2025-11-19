# Academic Formatting in Markdown

Markdown is increasingly used for academic writing, research papers, and essays due to its focus on content over layout. This guide covers conventions for academic formatting.

## Frontmatter (YAML)

Use YAML frontmatter to define metadata like title, author, date, and abstract. This is commonly used by tools like Pandoc or static site generators.

```yaml
---
title: "The Impact of Markdown on Technical Literacy"
author: "Jane Doe"
date: 2023-10-27
abstract: |
  This paper explores the adoption of Markdown in academic circles...
bibliography: references.bib
csl: apa.csl
---
```

## Mathematics

Many Markdown renderers (like GitHub, GitLab, and Pandoc) support LaTeX-style math equations using `$` delimiters.

### Inline Math

Wrap equations in single dollar signs `$`.

The formula for energy is $E = mc^2$.

### Block Math

Wrap equations in double dollar signs `$$`.

$$
\sum_{i=1}^{n} i = \frac{n(n+1)}{2}
$$

## Footnotes

Use footnotes to provide additional context or citations without cluttering the main text.

Here is a statement that needs a footnote.[^1]

[^1]: This is the text of the footnote.

## Citations

When using Pandoc or similar tools, citations can be formatted using `@` syntax.

-   **Narrative citation**: @smith2023 argues that...
-   **Parenthetical citation**: This has been proven (Smith, 2023).

## Figures and Captions

Images in academic papers should always have a caption.

```markdown
![Figure 1: Distribution of Markdown usage by industry](images/usage-chart.png)
*Figure 1: Distribution of Markdown usage by industry*
```

## Tables

Tables should be used for data presentation. Ensure headers are clear.

| Experiment | Control Group | Test Group | P-Value |
| :--- | :---: | :---: | ---: |
| A | 12.5 | 14.2 | 0.04 |
| B | 10.1 | 10.3 | 0.56 |

## Blockquotes

Use blockquotes for direct quotations from other sources.

> "Markdown is not just a tool, but a way of thinking about text."
>
> — *John Gruber*

## Structure

Academic papers typically follow a standard structure:

1.  **Introduction**: Problem statement and thesis.
2.  **Literature Review**: Existing research.
3.  **Methodology**: How the research was conducted.
4.  **Results**: Findings.
5.  **Discussion**: Interpretation of results.
6.  **Conclusion**: Summary and future work.
7.  **References**: Bibliography.

## Exporting

To convert your Markdown to PDF or Word for submission, `pandoc` is the standard tool.

```bash
pandoc paper.md -o paper.pdf --bibliography=references.bib
```
