# Technical Writing Style Guide

Clear, accessible, and consistent writing is just as important as clean code. This guide outlines best practices for technical prose in Markdown documentation.

## Core Principles

1.  **Clarity**: Be unambiguous. Avoid jargon unless necessary and defined.
2.  **Conciseness**: Omit needless words. Get to the point.
3.  **Consistency**: Use the same term for the same concept throughout.

## Voice and Tone

-   **Active Voice**: Use active voice for instructions. It is more direct and easier to understand.
    -   *Bad*: "The button should be clicked."
    -   *Good*: "Click the button."
-   **Second Person**: Address the user as "you".
    -   *Bad*: "The user needs to install Node.js."
    -   *Good*: "Install Node.js."
-   **Present Tense**: Describe how the software works now.
    -   *Bad*: "The system will generate a report."
    -   *Good*: "The system generates a report."

## Formatting Code

### Inline Code

Use backticks for:
-   Filenames and paths: `src/config.js`
-   Menu items and buttons: Click `Save`.
-   Variable names and values: Set `timeout` to `5000`.
-   Command line utilities: Use `grep` to search.

### Code Blocks

-   Always specify the language for syntax highlighting.
-   Keep examples short and focused.
-   Use comments to explain complex logic.

## Headings

-   Use sentence case for headings (only capitalize the first word and proper nouns).
    -   *Example*: "How to configure the database"
-   Keep headings hierarchy logical (`#` -> `##` -> `###`).
-   Avoid skipping levels (e.g., don't jump from `##` to `####`).

## Lists

-   **Bulleted Lists**: Use for items where order doesn't matter.
-   **Numbered Lists**: Use for sequential steps.

Ensure parallel structure in list items.

*Bad*:
-   Download the file
-   Opening the installer
-   You should click finish

*Good*:
-   Download the file
-   Open the installer
-   Click finish

## Links

Use descriptive link text. Avoid "click here" or "read more".

-   *Bad*: [Click here](https://example.com) to read the docs.
-   *Good*: Read the [documentation](https://example.com).

## Terminology

Define a glossary for your project if you use specific terms.

| Term | Definition |
| :--- | :--- |
| **Backend** | The server-side logic of the application. |
| **Frontend** | The client-side interface. |
| **API** | Application Programming Interface. |

## Accessibility

-   Provide `alt` text for all images.
-   Do not rely on color alone to convey meaning.
-   Use semantic HTML/Markdown elements correctly.
