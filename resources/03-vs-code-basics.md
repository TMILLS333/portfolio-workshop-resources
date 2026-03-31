# VS Code Basics

## The Interface at a Glance

When you open VS Code, here's what you'll see:

```
┌─────────────────────────────────────────────┐
│  Menu Bar (File, Edit, View, etc.)          │
├──────┬──────────────────────────────────────┤
│      │                                      │
│  A   │        Editor Area                   │
│  c   │    (where you write code)            │
│  t   │                                      │
│  i   │                                      │
│  v   ├──────────────────────────────────────┤
│  i   │                                      │
│  t   │     Terminal / Output Panel          │
│  y   │                                      │
│      │                                      │
├──────┴──────────────────────────────────────┤
│  Status Bar                                 │
└─────────────────────────────────────────────┘
```

- **Activity Bar** (left side): Icons for Explorer, Search, Source Control (Git), Extensions
- **Editor Area** (center): Where your files open as tabs
- **Terminal Panel** (bottom): A built-in terminal so you don't need a separate app
- **Status Bar** (very bottom): Shows your file type, line number, and Git branch

---

## Recommended Resources

### Video

| Video | Length | Why It's Good |
|-------|--------|---------------|
| [VS Code in 100 Seconds](https://www.youtube.com/watch?v=pdRpuy8F7Kw) | ~2 min | Lightning-fast overview of what VS Code is and why developers love it |

---

## How to Start a Project

1. **Create a folder** on your computer for your project (e.g., `my-portfolio`)
2. **Open VS Code**
3. Go to `File → Open Folder` (or press `Ctrl/Cmd + K`, then `Ctrl/Cmd + O`)
4. Select your project folder
5. You'll see the folder name in the Explorer sidebar — you're ready to go

**Or from the terminal:**
```bash
mkdir my-portfolio
cd my-portfolio
code .
```
The `code .` command opens the current folder in VS Code.

---

## How to Reopen a Project

- **Recent projects:** Go to `File → Open Recent` to see folders you've worked on before
- **From the Welcome tab:** When you first open VS Code, recent folders are listed on the Welcome screen
- **From the terminal:** Navigate to the project folder and run `code .`
```bash
cd my-portfolio
code .
```

---

## How to Use the Built-in Terminal

- **Open it:** Press `` Ctrl + ` `` (the backtick key, next to the 1 key)
- **Or:** Go to `View → Terminal`
- This is the same terminal from [Terminal Basics](01-terminal-basics.md) — just built into VS Code
- You can run all the same commands: `ls`, `cd`, `mkdir`, `git`, etc.

---

## How to Close a Project

- `File → Close Folder` closes the current project
- `File → Close Window` closes the entire VS Code window
- Your files are saved automatically if you have Auto Save turned on (`File → Auto Save`)

---

## Essential Shortcuts

| Action | Mac | Windows/Linux |
|--------|-----|---------------|
| Open a folder | `Cmd + K, Cmd + O` | `Ctrl + K, Ctrl + O` |
| New file | `Cmd + N` | `Ctrl + N` |
| Save | `Cmd + S` | `Ctrl + S` |
| Toggle terminal | `` Cmd + ` `` | `` Ctrl + ` `` |
| Command Palette | `Cmd + Shift + P` | `Ctrl + Shift + P` |
| Search across files | `Cmd + Shift + F` | `Ctrl + Shift + F` |
| Toggle sidebar | `Cmd + B` | `Ctrl + B` |
| Zoom in/out | `Cmd + =` / `Cmd + -` | `Ctrl + =` / `Ctrl + -` |

**Pro tip:** The **Command Palette** (`Cmd/Ctrl + Shift + P`) is your best friend. If you forget how to do something, open it and start typing what you want to do.

---

[← Back to all resources](../README.md)
