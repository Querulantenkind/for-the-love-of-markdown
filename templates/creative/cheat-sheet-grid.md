<!-- 
  TEMPLATE: Cheat Sheet Grid
  COMPLEXITY: High
  FEATURES: Dense information layout, Tables as columns, Code blocks
  USE CASE: Quick reference guides for languages, tools, or shortcuts.
-->

# ⌨️ Vim Cheat Sheet

> "I've been using Vim for about 2 years now, mostly because I can't figure out how to exit it."

---

## 🚀 Essentials

| **Mode Switching** | **Description** |
| :--- | :--- |
| `i` | Insert mode (before cursor) |
| `a` | Append mode (after cursor) |
| `v` | Visual mode |
| `Esc` | Normal mode |
| `:wq` | Save and Quit |

---

## 🧭 Navigation

| **Basic Movement** | **Word Movement** | **Line Movement** |
| :--- | :--- | :--- |
| `h` Left | `w` Jump by start of word | `0` Start of line |
| `j` Down | `e` Jump by end of word | `$` End of line |
| `k` Up | `b` Jump backward by word | `gg` Go to first line |
| `l` Right | | `G` Go to last line |

---

## ✂️ Editing

<div align="center">

| **Action** | **Command** | **Example** |
| :--- | :--- | :--- |
| **Delete** | `d` | `dd` (delete line), `dw` (delete word) |
| **Change** | `c` | `cw` (change word), `cc` (change line) |
| **Yank (Copy)** | `y` | `yy` (copy line), `yw` (copy word) |
| **Paste** | `p` | `p` (paste after), `P` (paste before) |
| **Undo/Redo** | `u` / `Ctrl+r` | |

</div>

---

## 🔍 Search and Replace

- `/pattern` - Search for pattern
- `?pattern` - Search backward for pattern
- `n` - Repeat search in same direction
- `N` - Repeat search in opposite direction
- `:%s/old/new/g` - Replace all old with new throughout file
- `:%s/old/new/gc` - Replace all old with new with confirmations

---

## 📑 Visual Mode

```text
v        Start visual mode
V        Start linewise visual mode
Ctrl+v   Start blockwise visual mode
```

**Common Operations:**
- `>` Shift right (indent)
- `<` Shift left (dedent)
- `y` Yank marked text
- `d` Delete marked text
- `~` Switch case

---

## 🖥️ Window Management

| Command | Action |
| :--- | :--- |
| `:sp` | Split window horizontally |
| `:vsp` | Split window vertically |
| `Ctrl+w` `h/j/k/l` | Move cursor between windows |
| `Ctrl+w` `_` | Maximize current window height |
| `Ctrl+w` `=` | Equalize all window sizes |

---

<div align="center">
  <sub>Cheat Sheet by <a href="#">For the Love of Markdown</a></sub>
</div>
