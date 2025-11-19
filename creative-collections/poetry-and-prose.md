# Poetry and Prose Formatting

Markdown is surprisingly effective for typesetting poetry and experimental prose, provided you understand how it handles whitespace.

## Line Breaks

In standard Markdown, a single line break is ignored.

**Input:**
```markdown
The rain falls
softly.
```

**Output:**
The rain falls softly.

### The Two-Space Rule

To force a line break (hard wrap) without starting a new paragraph, add **two spaces** at the end of the line.

**Input:**
```markdown
The rain falls  
softly.
```

**Output:**
The rain falls
softly.

### The Non-Breaking Space

For precise indentation, use the HTML entity `&nbsp;`.

```markdown
The
&nbsp;&nbsp;&nbsp;&nbsp;rain
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;falls.
```

## Stanzas and Paragraphs

Use a blank line to separate stanzas (paragraphs).

```markdown
First stanza line 1.  
First stanza line 2.

Second stanza line 1.  
Second stanza line 2.
```

## Blockquotes for Emphasis

Use blockquotes `>` to highlight specific verses or to create a visual offset.

> I have eaten  
> the plums  
> that were in  
> the icebox

## Code Blocks for Concrete Poetry

If the *shape* of the poem is as important as the words, use a code block to preserve all whitespace.

```text
      l(a
    le
  af
fa
  ll
s)
  one
l
  iness
```
*(e.e. cummings)*

## Experimental Typography

### Strikethrough

Use `~~` for redaction poetry or erased text.

The ~~government~~ people spoke.

### Bold and Italic

Use `**` and `*` for rhythm and stress.

It was **loud**, then *quiet*.

## Footnotes in Fiction

Use footnotes `[^1]` for meta-commentary or non-linear narratives (like *House of Leaves*).

The house was bigger on the inside.[^1]

[^1]: This is physically impossible, yet true.
