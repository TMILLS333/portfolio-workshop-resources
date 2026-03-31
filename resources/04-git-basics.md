# Git Basics

## What Is Git?

**Git is a version control system.** Think of it as a time machine for your project files.

- Made a mistake? Go back to an earlier version.
- Want to try something experimental? Create a branch so you don't break the main version.
- Working with someone else? Git keeps track of who changed what and helps merge everything together.

**Git** lives on your computer. **GitHub** is a website where you can store and share your Git projects online. They work together, but they're not the same thing.

---

## Recommended Resources

### Video

| Video | Length | Why It's Good |
|-------|--------|---------------|
| [A brief introduction to Git for beginners](https://www.youtube.com/watch?v=r8jQ9hVA2qs&list=PL0lo9MOBetEFcp4SCWinBdpml9B2U25-f&index=1) by GitHub | 9 min | Clear, beginner-friendly overview of what Git is and why it matters |
| [Beginner Git commands you need to know (WITH EXAMPLES)](https://www.youtube.com/watch?v=rE2zRhZdjFU&list=PL0lo9MOBetEFcp4SCWinBdpml9B2U25-f&index=3) | 14 min | Hands-on walkthrough of the essential commands with real examples |

---

## The Terms You'll Hear Claude Use

When you're working with Claude Code (or any developer), you'll hear these terms a lot. Here's what they mean in plain language:

### Repository (Repo)

A **project folder** that Git is tracking. When Claude says "repo," it just means your project.

### Staging / Add

**Marking files** you want to include in your next save point. Think of it like putting items in a box before sealing it.

```bash
git add .          # Stage everything that changed
git add index.html # Stage just one file
```

### Commit

**Save a snapshot** of your project at this moment. Every commit has a message describing what changed.

```bash
git commit -m "Add homepage layout"
```

Think of commits as save points in a video game — you can always go back to any of them.

### Push

**Upload your commits** from your computer to GitHub so others (or Claude) can see them.

```bash
git push
```

### Pull

**Download the latest changes** from GitHub to your computer. The opposite of push.

```bash
git pull
```

### Branch

A **parallel version** of your project. You can work on a branch without affecting the main version.

```bash
git branch new-feature     # Create a branch
git checkout new-feature   # Switch to it
```

### Merge

**Combine changes** from one branch into another. Usually you merge your feature branch back into `main` when you're done.

### Pull Request (PR)

A **request to merge** your branch into the main project on GitHub. It's a way to review changes before they go live.

### Conflict

When two people (or you and Claude) changed the **same part of the same file**. Git doesn't know which version to keep, so it asks you to choose.

---

## The Basic Workflow

Here's the cycle you'll repeat throughout the workshop:

```
1. Make changes to your files
        ↓
2. git add .           (stage the changes)
        ↓
3. git commit -m "..."  (save a snapshot)
        ↓
4. git push             (upload to GitHub)
```

And when you need to get updates:

```
git pull                (download latest changes)
```

---

## Visual: How Git Fits Together

```
Your Computer                          GitHub (cloud)
┌──────────────┐     git push →     ┌──────────────┐
│              │  ─────────────→    │              │
│  Local Repo  │                    │  Remote Repo │
│              │  ←─────────────    │              │
└──────────────┘     ← git pull     └──────────────┘
       ↑
  git add + git commit
       ↑
  Your file changes
```

---

[← Back to all resources](../README.md)
