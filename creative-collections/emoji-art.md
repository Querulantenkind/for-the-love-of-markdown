# Emoji Art

Emoji Art uses Unicode emoji characters to create mosaics, landscapes, and patterns. Unlike ASCII art, it is colorful and scales differently.

## The Grid

Emoji are generally square, making them perfect for pixel-art style compositions.

### Landscapes

```text
🟦🟦🟦☁️🟦🟦🟦
🟦🟦☁️🟦🟦🟦🟦
⛰️⛰️⛰️⛰️⛰️⛰️⛰️
🌲🌲🌲🌲🌲🌲🌲
🟩🟩🟩🟩🟩🟩🟩
```

### Patterns

```text
🔴⚫🔴⚫🔴
⚫🔴⚫🔴⚫
🔴⚫🔴⚫🔴
⚫🔴⚫🔴⚫
```

## Combining with Text

Emoji can act as bullet points or section dividers.

✨ **New Feature** ✨
🚀 **Performance Boost** 🚀
🐛 **Bug Fix** 🐛

## Large Scale Mosaics

You can use tools to convert images into emoji mosaics, but hand-crafting them adds a personal touch.

**The Wave**
🌊🌊🌊🌊🌊
🌊🏄‍♂️🌊🌊🌊
🌊🌊🌊🌊🌊

## Technical Considerations

1.  **Rendering**: Emoji look different on every platform (Apple, Google, Microsoft, Twitter).
    -   *Apple*: Detailed, 3D.
    -   *Microsoft*: Flat, thick outlines.
    -   *Google*: Flat, colorful.
2.  **Width**: Some emoji are wider than others. This can break alignment in complex grids.
3.  **Accessibility**: Screen readers will read *every single emoji name*.
    -   "Blue square, Blue square, Cloud, Blue square..."
    -   **Always** mark large emoji art blocks as decorative or provide a summary, and consider using an image screenshot for the visual while keeping the text for the source.

    ```markdown
    <!-- Emoji Art: A mountain landscape -->
    [Art]
    ```
