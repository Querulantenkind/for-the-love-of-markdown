# Static Site Generators (SSG)

Static Site Generators allow you to build fast, secure websites using Markdown content. This guide compares popular SSGs and their Markdown support.

## 1. Jekyll (Ruby)

The engine behind GitHub Pages.

-   **Markdown Engine**: Kramdown (default).
-   **Frontmatter**: YAML.
-   **Templating**: Liquid.

**Example Header:**
```yaml
---
layout: post
title: "Welcome to Jekyll!"
date: 2023-11-19 12:00:00 -0500
categories: jekyll update
---
```

**Pros**:
-   Native GitHub Pages support (zero config).
-   Huge ecosystem of themes.

**Cons**:
-   Ruby dependency management can be tricky.
-   Slower build times for large sites.

## 2. Hugo (Go)

Known for incredible speed.

-   **Markdown Engine**: Goldmark (CommonMark compliant).
-   **Frontmatter**: YAML, TOML, or JSON.
-   **Templating**: Go Templates.

**Example Header (TOML):**
```toml
+++
title = "My First Post"
date = 2023-11-19T12:00:00-05:00
draft = false
tags = ["hugo", "web"]
+++
```

**Pros**:
-   Blazing fast builds (<1ms per page).
-   Single binary installation (no dependencies).

**Cons**:
-   Go templating syntax has a steeper learning curve.

## 3. Eleventy (11ty) (JavaScript)

Flexible and simple.

-   **Markdown Engine**: Markdown-it (configurable).
-   **Frontmatter**: YAML, JSON, JavaScript.
-   **Templating**: Liquid, Nunjucks, Handlebars, EJS, etc.

**Example Header:**
```yaml
---
layout: layout.njk
title: Hello World
tags: ['post', 'tutorial']
---
```

**Pros**:
-   Language-agnostic (use any template engine).
-   Zero-config by default.
-   Fast builds.

**Cons**:
-   Newer ecosystem than Jekyll/Hugo.

## 4. Docusaurus (React)

Built by Meta, optimized for documentation.

-   **Markdown Engine**: MDX (Markdown + JSX).
-   **Frontmatter**: YAML.
-   **Templating**: React components.

**MDX Example:**
```markdown
---
title: Interactive Button
---

import { Button } from './components';

Here is a button:

<Button onClick={() => alert('Clicked!')}>Click Me</Button>
```

**Pros**:
-   Perfect for documentation sites.
-   React integration allows interactive components.
-   Versioning support.

**Cons**:
-   Requires React knowledge for customization.

## 5. Gatsby (React)

A powerful PWA generator.

-   **Markdown Engine**: Remark / MDX.
-   **Data Layer**: GraphQL.

**Pros**:
-   Rich plugin ecosystem.
-   GraphQL data layer is powerful.

**Cons**:
-   Complex setup.
-   Heavy build process.

## Comparison Table

| Feature | Jekyll | Hugo | 11ty | Docusaurus |
| :--- | :--- | :--- | :--- | :--- |
| **Language** | Ruby | Go | JS | JS (React) |
| **Speed** | Slow | Fast | Fast | Medium |
| **MDX** | No | No | Yes | Yes |
| **GitHub Pages** | Native | Easy | Easy | Easy |
| **Best For** | Blogs | Large Sites | Simple Sites | Docs |

## Best Practices

1.  **Keep Content Clean**: Avoid mixing too much HTML in your Markdown to ensure portability between SSGs.
2.  **Use Frontmatter**: Store metadata (dates, tags, authors) in frontmatter, not the body.
3.  **Asset Management**: Store images in a consistent location (e.g., `/assets/images/`) relative to the root.
