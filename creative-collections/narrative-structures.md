# Narrative Structures

Markdown's linking capabilities allow for non-linear storytelling, similar to "Choose Your Own Adventure" books or hypertext fiction.

## The Branching Path

Create a directory structure where each file is a "room" or "scene".

### `start.md`

```markdown
# The Entrance

You stand before a massive iron door. To your left is a dark forest. To your right, a shimmering lake.

- [Open the door](./rooms/castle-hall.md)
- [Enter the forest](./rooms/dark-forest.md)
- [Walk to the lake](./rooms/lake.md)
```

### `rooms/castle-hall.md`

```markdown
# The Castle Hall

It is empty, save for a single chair.

- [Sit in the chair](./chair.md)
- [Go back](../start.md)
```

## The Loop

You can create loops by linking back to previous files.

```markdown
You are lost.

- [Try to find the exit](./maze.md)
```

*(Where `maze.md` links back to itself or a copy of itself)*

## The Inventory System (Conceptual)

While Markdown can't store state (variables), you can simulate an inventory using folder paths.

-   `start.md`
-   `with-key/door.md` (The version of the door room if you have the key)
-   `without-key/door.md` (The version if you don't)

*Note: This gets complex quickly but is fun for small experiments.*

## Details and Secrets

Use the `<details>` tag to hide clues or spoilers.

```markdown
You see a dusty book.

<details>
<summary>Read the book</summary>

The text is written in blood...
</details>
```

## Tooling

-   **Obsidian**: Great for visualizing the links between your narrative nodes (graph view).
-   **Twine**: A dedicated tool for this, but you can export to Markdown.
