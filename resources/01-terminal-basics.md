# Terminal Basics

## What Is the Terminal?

The terminal (also called the command line or CLI) is a text-based way to talk to your computer. Instead of clicking on folders and files, you type commands. It looks intimidating at first, but you only need a handful of commands to get started.

**Why designers need it:** Many developer tools (like Git, package managers, and Claude Code) run through the terminal. Knowing the basics makes these tools feel way less scary.

---

## Recommended Resources

### Video

| Video | Length | Why It's Good |
|-------|--------|---------------|
| [How to Use the Command Line — Terminal Basics for Beginners](https://www.youtube.com/watch?v=5XgBd6rjuDQ) by Jesse Showalter | 14 min | Made by a designer, covers the essentials for a design & development workflow |

### Article

- [Command Line Basics — The Odin Project](https://www.theodinproject.com/lessons/foundations-command-line-basics) — Free, interactive lesson that walks you through navigating directories, creating files, and tab completion

---

## Quick Reference

### Opening the Terminal

| OS | How to Open |
|----|-------------|
| **Mac** | Spotlight Search (`Cmd + Space`) → type "Terminal" → press Enter |
| **Windows** | Search for "PowerShell" or "Terminal" in the Start menu |
| **Linux** | `Ctrl + Alt + T` |

---

## Command Definitions

Here's what each command actually means and does. You don't need to memorize these — just come back here when you see one you don't recognize.

### Navigation Commands

**`pwd`** — **P**rint **W**orking **D**irectory
Shows the full path of where you currently are in your computer's file system. Like checking your location on a map.
```bash
pwd
# Output: /Users/tania/projects/my-portfolio
```

**`ls`** — **L**i**s**t
Shows all the files and folders in your current location. Like opening a folder and seeing what's inside.
```bash
ls
# Output: index.html  styles.css  images/  README.md
```

**`cd`** — **C**hange **D**irectory
Moves you into a different folder. Think of it like double-clicking a folder to open it.
```bash
cd my-portfolio        # Move into the "my-portfolio" folder
cd images              # Move into the "images" folder
cd ..                  # Go back up one level (to the parent folder)
cd ~                   # Go to your home directory
cd /                   # Go to the root of your hard drive
```

### File & Folder Commands

**`mkdir`** — **M**a**k**e **Dir**ectory
Creates a new folder.
```bash
mkdir my-portfolio     # Creates a folder called "my-portfolio"
mkdir images           # Creates a folder called "images"
```

**`touch`** — Create a new empty file
```bash
touch index.html       # Creates an empty file called "index.html"
touch styles.css       # Creates an empty file called "styles.css"
touch README.md        # Creates an empty Markdown file
```

**`rm`** — **R**e**m**ove
Deletes a file. Be careful — there's no trash can, it's gone for good.
```bash
rm old-file.txt        # Delete a file
rm -r old-folder       # Delete a folder and everything inside it
```

**`mv`** — **M**o**v**e (also used to rename)
```bash
mv old-name.html new-name.html    # Rename a file
mv file.txt images/               # Move a file into the images folder
```

**`cp`** — **C**o**p**y
```bash
cp index.html backup.html         # Copy a file
cp -r images/ images-backup/      # Copy a folder and its contents
```

### Display Commands

**`clear`** — Clear the screen
Wipes the terminal screen clean. Doesn't delete anything — just gives you a fresh view.

**`cat`** — Display file contents
Prints the contents of a file right in the terminal.
```bash
cat README.md          # Shows what's inside README.md
```

### Opening Things

**`code .`** — Open in VS Code
The `.` means "this folder." This command opens your current folder as a project in VS Code.
```bash
code .                 # Open current folder in VS Code
code index.html        # Open a specific file in VS Code
```

**`open .`** (Mac) / `explorer .` (Windows) — Open in Finder/Explorer
```bash
open .                 # Open current folder in Finder (Mac)
explorer .             # Open current folder in Explorer (Windows)
```

---

## Package Manager & Project Commands

These are commands you'll see when working with web projects. They're not built into the terminal — they come from tools you install.

**`npm`** — **N**ode **P**ackage **M**anager
A tool that installs and manages JavaScript packages (pre-built code libraries). It comes with Node.js.
```bash
npm install            # Install all the packages a project needs
npm install astro      # Install a specific package (e.g., Astro)
npm run dev            # Start a local development server
npm run build          # Build your site for production/deployment
```

**`npx`** — **N**ode **P**ackage **Ex**ecute
Runs a package command without permanently installing it.
```bash
npx create-astro       # Run the Astro project setup wizard
npx astro add          # Add integrations to your Astro project
```

**`node`** — Run JavaScript
Node.js lets you run JavaScript outside of a browser.
```bash
node --version         # Check if Node.js is installed (shows version number)
```

**`git`** — Version control commands
See the [Git Basics](04-git-basics.md) page for full definitions of `git add`, `git commit`, `git push`, etc.
```bash
git status             # See what files have changed
git add .              # Stage all changes
git commit -m "message" # Save a snapshot
git push               # Upload to GitHub
```

---

## Symbols You'll See

| Symbol | What It Means |
|--------|---------------|
| `.` | The current folder ("right here") |
| `..` | The parent folder ("one level up") |
| `~` | Your home directory (e.g., `/Users/tania`) |
| `/` | The root of your file system, or a separator between folders |
| `-` | Introduces a flag/option (e.g., `ls -a` means "list all, including hidden files") |
| `--` | Introduces a longer flag name (e.g., `--version`) |

---

## Tips

- **Tab completion:** Start typing a folder or file name and press `Tab` — the terminal will auto-complete it for you.
- **Up arrow:** Press the up arrow key to cycle through your previous commands.
- **Copy/paste in terminal:** On Mac, `Cmd + C` / `Cmd + V` works normally. On Windows/Linux, use `Ctrl + Shift + C` / `Ctrl + Shift + V`.
- **Don't panic:** If something looks wrong, you can almost always just close the terminal and open a new one. Nothing is permanently broken.
- **Stuck in a weird screen?** Press `q` to quit. If that doesn't work, press `Ctrl + C` to cancel whatever is running.

---

## Commands We'll Use in the Portfolio Project

```bash
# Navigate to your project folder
cd my-portfolio

# See what's in the folder
ls

# Create a new file
touch about.md

# Open the project in VS Code
code .

# Install project dependencies
npm install

# Start the development server
npm run dev

# Build the site for deployment
npm run build
```

---

[← Back to all resources](../README.md)
