# 💻 VS Code Cheat Sheet

> Keyboard shortcuts and tricks to code faster in Visual Studio Code.

---

## ⌨️ Essential Shortcuts

| Shortcut | Windows | Mac | What It Does |
|----------|---------|-----|-------------|
| Command Palette | `Ctrl+Shift+P` | `Cmd+Shift+P` | Search any command |
| Quick Open | `Ctrl+P` | `Cmd+P` | Open any file by name |
| Settings | `Ctrl+,` | `Cmd+,` | Open settings |
| Terminal | `Ctrl+`` | `Cmd+`` | Open built-in terminal |
| Sidebar | `Ctrl+B` | `Cmd+B` | Toggle sidebar |
| Explorer | `Ctrl+Shift+E` | `Cmd+Shift+E` | Show file explorer |

---

## ✏️ Editing Shortcuts

| Shortcut | Windows | Mac | What It Does |
|----------|---------|-----|-------------|
| Multi-cursor | `Alt+Click` | `Option+Click` | Type in multiple places at once |
| Copy line up/down | `Shift+Alt+↑/↓` | `Shift+Option+↑/↓` | Duplicate current line |
| Move line up/down | `Alt+↑/↓` | `Option+↑/↓` | Move line around |
| Quick comment | `Ctrl+/` | `Cmd+/` | Comment/uncomment current line |
| Indent / Outdent | `Tab` / `Shift+Tab` | Same | Move text left/right |
| Find | `Ctrl+F` | `Cmd+F` | Search in current file |
| Find & Replace | `Ctrl+H` | `Cmd+Option+F` | Search and replace |
| Select word | `Ctrl+D` | `Cmd+D` | Select current word |
| Select all matches | `Ctrl+Shift+L` | `Cmd+Shift+L` | Select all matching words |
| Format document | `Shift+Alt+F` | `Shift+Option+F` | Auto-format your code |
| Rename symbol | `F2` | `F2` | Rename variable everywhere |
| Go to line | `Ctrl+G` | `Ctrl+G` | Jump to a specific line number |

---

## 🔍 Navigation

| Shortcut | Windows | Mac | What It Does |
|----------|---------|-----|-------------|
| Go back | `Alt+←` | `Ctrl+-` | Jump to previous cursor position |
| Go forward | `Alt+→` | `Ctrl+Shift+-` | Jump forward |
| Find in files | `Ctrl+Shift+F` | `Cmd+Shift+F` | Search entire project |
| Switch tabs | `Ctrl+Tab` | `Cmd+Tab` | Cycle through open files |
| Close tab | `Ctrl+W` | `Cmd+W` | Close current file |
| Split editor | `Ctrl+\` | `Cmd+\` | Split screen to see two files |

---

## 📦 Extensions (Must-Haves)

> Install these: click Extensions icon (or `Ctrl+Shift+X`), search, and install.

| Extension | Why You Need It |
|-----------|----------------|
| **Prettier** | Auto-formats your code (saves hours) |
| **ES7+ React/Redux** | Snippets for React developers |
| **Live Server** | Opens your HTML file in browser with auto-refresh |
| **GitLens** | See who wrote each line of code |
| **Bracket Pair Colorizer** | Colored brackets — never lose track of `{ }` again |
| **Material Icon Theme** | Nice file icons (makes explorer look clean) |
| **Path Intellisense** | Auto-completes file paths when you type `./` |
| **Error Lens** | Shows errors right next to your code (no hovering) |

---

## 🎨 Settings I Recommend

```json
{
  "editor.fontSize": 14,
  "editor.tabSize": 2,
  "editor.wordWrap": "on",
  "editor.minimap.enabled": true,
  "editor.formatOnSave": true,
  "editor.bracketPairColorization.enabled": true,
  "workbench.colorTheme": "Monokai Dark",
  "files.autoSave": "afterDelay",
  "emmet.includeLanguages": { "javascript": "javascriptreact" }
}
```

To add these: `Ctrl+Shift+P` → "Open Settings (JSON)" → paste inside the `{}`

---

## 💡 Pro Tips

- Press `Ctrl+P` then type `>` to search all commands
- Right-click a folder → **Open in Integrated Terminal** (saves time)
- Use `Ctrl+Shift+P` → "Fold All" to collapse all functions and see structure
- `Ctrl+\` to split editor — put code on one side, preview on the other
- Hover over any symbol to see its definition and docs
