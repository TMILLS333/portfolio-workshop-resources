# Claude Skills & MD Files

## What Is a Claude Skill?

A **skill** is a set of instructions written in Markdown that teaches Claude how to do a specific task. Think of it as a recipe card — you write down the steps, and Claude follows them whenever that type of task comes up.

Skills are stored as `SKILL.md` files. They can also include additional folders for scripts, reference docs, and templates.

**Why this matters:** As you work with Claude (whether in Claude.ai or Claude Code), you can create custom skills to automate your own workflows — like generating portfolio content, formatting design documentation, or analyzing feedback.

---

## Recommended Resources

### From Claude Academy (Free Courses)

| Course | What It Covers |
|--------|---------------|
| [Claude 101 — Working with Skills](https://anthropic.skilljar.com/claude-101) | Part of the free Claude 101 course — covers creating and using skills in Claude.ai |
| [Introduction to Agent Skills](https://anthropic.skilljar.com) | Dedicated course on building, configuring, and sharing skills in Claude Code |
| [Claude Code in Action](https://anthropic.skilljar.com/claude-code-in-action) | Broader course on Claude Code, including skills, hooks, and MCP |

### Video

| Video | Length | Why It's Good |
|-------|--------|---------------|
| [Claude Skills Tutorial for Beginners](https://www.youtube.com/watch?v=2prubd1IZ7U) | ~22 min | Step-by-step — creating skills in Claude.ai, building workflows, using plugins |
| [Claude Code Skills — The Only Tutorial You Need](https://www.youtube.com/watch?v=vIUJ4Hd7be0) | ~20 min | Focused on Claude Code skills — installing, creating, and combining skills |
| [Full Claude Tutorial for Beginners (2026)](https://www.youtube.com/watch?v=rRrBbyv3ChM) | ~50 min | Comprehensive — covers skills starting at 35:20 timestamp |

### Article / Docs

- [Extend Claude with Skills — Claude Code Docs](https://code.claude.com/docs/en/skills) — Official documentation on skill structure and usage
- [Skill Authoring Best Practices — Claude API Docs](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices) — In-depth guide on writing effective skills
- [The Complete Guide to Building Skills for Claude (PDF)](https://resources.anthropic.com/hubfs/The-Complete-Guide-to-Building-Skill-for-Claude.pdf) — Anthropic's 32-page guide covering planning, testing, and distribution
- [How to Build Claude Skills — Codecademy](https://www.codecademy.com/article/how-to-build-claude-skills) — Hands-on tutorial building a lesson plan generator skill

---

## What's Inside a Skill?

A skill is a folder with this structure:

```
my-skill/
├── SKILL.md          ← Required — the main instructions
├── scripts/          ← Optional — executable code
├── references/       ← Optional — docs and examples
└── assets/           ← Optional — templates, fonts, icons
```

### The SKILL.md File

Every SKILL.md file has two parts:

**1. Frontmatter** (metadata at the top):

```yaml
---
name: portfolio-content-generator
description: Generates portfolio case study content from project briefs.
  Use when user wants to create or improve portfolio descriptions.
---
```

**2. Instructions** (the body, written in Markdown):

```markdown
# Portfolio Content Generator

## What This Skill Does
Generates polished case study descriptions for design portfolio projects.

## Workflow
1. Ask for the project name, role, and key outcomes
2. Draft a case study in the format: Challenge → Process → Outcome
3. Review and iterate based on feedback

## Best Practices
- Keep descriptions concise (150-300 words per case study)
- Lead with impact and outcomes
- Use action verbs
```

---

## How Skills Get Loaded

Skills use a three-level system (so they don't overwhelm Claude with information):

1. **Level 1 — Name & Description:** Always loaded. Claude reads these to decide if the skill is relevant.
2. **Level 2 — SKILL.md body:** Loaded only when Claude thinks the skill matches your task.
3. **Level 3 — Linked files:** Loaded only when Claude needs specific details from the scripts, references, or assets folders.

---

## Skills vs. CLAUDE.md

| | Skills | CLAUDE.md |
|---|--------|----------|
| **What** | Task-specific instructions | Project-wide context |
| **When loaded** | Only when relevant to current task | Always loaded |
| **Example** | "How to generate portfolio content" | "This project uses Astro, deployed to Cloudflare Pages" |
| **Where** | Skill library or project folder | Root of your project repo |

---

[← Back to all resources](../README.md)
