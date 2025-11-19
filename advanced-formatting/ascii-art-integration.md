# ASCII Art Integration

ASCII art allows you to embed diagrams, logos, and illustrations directly into your Markdown files without relying on external image files. This ensures your documentation remains lightweight and viewable in any text editor.

## The Basics

To include ASCII art, always use **fenced code blocks** (triple backticks) or **indented code blocks** (4 spaces). This preserves whitespace and ensures a monospaced font is used.

### Bad Example (No Code Block)
   __
  /  \
  |  |
  \__/
  
*The whitespace is collapsed, ruining the art.*

### Good Example (With Code Block)

```text
   __
  /  \
  |  |
  \__/
```

## Use Cases

### 1. Project Logos / Headers

Add visual flair to your README header.

```text
  /$$$$$$$            /$$           /$$
 | $$__  $$          | $$          | $$
 | $$  \ $$  /$$$$$$ | $$  /$$$$$$ | $$
 | $$$$$$$/ /$$__  $$| $$ /$$__  $$| $$
 | $$__  $$| $$  \ $$| $$| $$$$$$$$|__/
 | $$  \ $$| $$  | $$| $$| $$_____/    
 | $$  | $$|  $$$$$$/| $$|  $$$$$$$ /$$
 |__/  |__/ \______/ |__/ \_______/|__/
```

### 2. Directory Structures

Show file trees clearly.

```text
.
├── src/
│   ├── index.js
│   └── utils.js
├── tests/
│   └── suite.js
└── package.json
```

### 3. Simple Diagrams

Illustrate flows or architectures.

```text
+--------+      +---------+      +----------+
| Client | ---> | Gateway | ---> | Database |
+--------+      +---------+      +----------+
    ^                                  |
    |                                  |
    +----------------------------------+
```

## Tools

-   **Text to ASCII**: [patorjk.com](http://patorjk.com/software/taag/)
-   **Diagrams**: [Monodraw](https://monodraw.helftone.com/) (Mac), [ASCIIFlow](https://asciiflow.com/) (Web)
-   **Tree Generator**: `tree` command in terminal.

## Best Practices

1.  **Keep it simple**: Complex art can break on mobile screens.
2.  **Limit width**: Stick to 80 characters max to prevent horizontal scrolling.
3.  **Accessibility**: ASCII art is invisible to screen readers. Always provide a text description or caption below the art.

    ```text
    [Diagram showing Client connecting to Gateway]
    ```
