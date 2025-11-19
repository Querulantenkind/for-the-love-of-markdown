# Terminal-Native Style Guide

This guide focuses on creating Markdown documents that look great when viewed directly in a terminal using tools like `cat`, `less`, `bat`, or `glow`.

## Hard Wrapping

Unlike web browsers, terminals don't always soft-wrap text nicely. For maximum compatibility, hard-wrap your text at 80 characters.

*Bad (one long line)*:
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

*Good (wrapped at 80 chars)*:
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

## Headers

Use ASCII art or simple underlining for headers to make them stand out without bold/size rendering.

```text
# MAIN TITLE
# ==========

## Subtitle
## --------
```

## Lists

Use standard markers that are universally recognized.

-   Use `*` or `-` for unordered lists.
-   Use `1.` for ordered lists.
-   Indent by 2 or 4 spaces consistently.

## Tables

Standard Markdown tables can break easily on small terminal windows. Consider using list formats for data if horizontal space is a concern.

*Risky Table*:
| ID | Name | Description | Status | Created At |
| -- | ---- | ----------- | ------ | ---------- |
| 1 | Item | Very long description... | Active | 2023-01-01 |

*Safe List Format*:
**Item 1**
-   **Name**: Item
-   **Description**: Very long description...
-   **Status**: Active
-   **Created At**: 2023-01-01

## Code Blocks

Indented code blocks (4 spaces) are the most compatible, but fenced code blocks (\`\`\`) are widely supported by modern pagers like `bat`.

    $ echo "This is an indented code block"
    $ It works everywhere

## ASCII Art

ASCII art can add visual flair but ensure it fits within the 80-character limit.

```text
   __  __           _       _
  |  \/  | __ _ _ _| |__ __| |_____ __ ___ _
  | |\/| |/ _` | '_| / / _` / _ \ V  V / ' \
  |_|  |_|\__,_|_| |_\_\__,_\___/\_/\_/|_||_|
```

## Links

In a terminal, you can't "click" a link. Use reference-style links to keep the text readable and list URLs at the bottom.

*Readable*:
You can find the source code on [GitHub][1].

...

[1]: https://github.com/username/repo

## Emphasis

Avoid relying solely on bold (`**`) or italics (`*`) for meaning, as some terminal themes might not render them distinctly. Use capitalization or symbols for emphasis.

-   *Okay*: **Warning**: Do not delete this file.
-   *Better*: [WARNING] Do not delete this file.

## ANSI Escape Codes

For advanced users, you can embed ANSI escape codes for color, but be aware this breaks readability in raw text editors.

See `advanced-formatting/color-and-ansi.md` for more details.
