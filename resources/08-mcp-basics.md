# MCP Know-How

## What Is MCP?

**MCP (Model Context Protocol)** is an open standard that lets AI apps like Claude connect to external tools and data. Think of it as **USB-C for AI** — just like USB-C gives you one universal port to connect all your devices, MCP gives AI one universal way to connect to all your tools.

Without MCP, every AI tool would need a custom integration for every service (Figma, GitHub, Google Drive, Slack, etc.). MCP makes it so you build the connection once and it works everywhere.

---

## Recommended Resources

### Video (Pick One)

| Video | Length | Why It's Good |
|-------|--------|---------------|
| [Model Context Protocol (MCP) Explained for Beginners](https://www.youtube.com/watch?v=E2DEHOEbzks) | ~15 min | Beginner-friendly demo with a real example |
| [The Model Context Protocol — Anthropic](https://www.youtube.com/watch?v=CQywdSdi5iA) | ~20 min | Straight from the creators — explains the "why" behind MCP with the team that built it |

### Article

- [What Is the Model Context Protocol? — Official MCP Docs](https://modelcontextprotocol.io/docs/getting-started/intro) — The clearest official explanation
- [A Beginner's Guide to MCP — DEV Community](https://dev.to/hussain101/a-beginners-guide-to-anthropics-model-context-protocol-mcp-1p86) — Plain-language walkthrough with setup instructions
- [Introducing the Model Context Protocol — Anthropic Blog](https://www.anthropic.com/news/model-context-protocol) — The original announcement post explaining why MCP was created
- [A Friendly Introduction to MCP — The Register](https://www.theregister.com/2025/04/21/mcp_guide/) — Hands-on guide that walks through setting up an MCP server

---

## How MCP Works (Simplified)

```
┌──────────────┐         ┌──────────────┐         ┌──────────────┐
│              │         │              │         │              │
│   Claude     │ ──MCP──→│  MCP Server  │ ────→   │  Your Tool   │
│   (Client)   │         │  (Bridge)    │         │  (Figma,     │
│              │ ←──MCP──│              │ ←────   │   GitHub,    │
│              │         │              │         │   etc.)      │
└──────────────┘         └──────────────┘         └──────────────┘
```

- **Client:** The AI app (Claude Desktop, VS Code with Claude, etc.)
- **Server:** A small program that translates between Claude and a specific tool
- **Tool:** The service you want Claude to access (GitHub, Figma, Google Drive, databases, etc.)

---

## What MCP Can Do

MCP servers can expose three types of things to Claude:

| Type | What It Is | Example |
|------|-----------|---------|
| **Tools** | Actions Claude can take | Create a GitHub issue, send a Slack message, search files |
| **Resources** | Data Claude can read | Your project files, database records, spreadsheet data |
| **Prompts** | Pre-written instructions | A template for how to analyze a pull request |

---

## Real-World Examples

| MCP Server | What It Lets Claude Do |
|------------|----------------------|
| **GitHub** | Read your repos, create issues, review pull requests |
| **Figma** | Inspect design files, extract component info |
| **Google Drive** | Read and search your documents |
| **Slack** | Read messages, post updates |
| **File System** | Access files on your computer |

---

## Why This Matters for the Workshop

You don't need to build MCP servers for the portfolio project. But understanding MCP helps you:

- **Understand what Claude can access** when it connects to your GitHub or Figma
- **Recognize the pattern** when you see Claude using external tools
- **Know the terminology** when team members or tutorials mention MCP
- **See the bigger picture** of how AI tools are becoming connected to the rest of your workflow

---

## Want to Go Deeper?

- [MCP Server Directory](https://github.com/modelcontextprotocol/servers) — List of available MCP servers you can use
- [Anthropic's Learn Page](https://www.anthropic.com/learn) — Free courses on MCP, Claude Code, and AI development
- [MCP Specification](https://modelcontextprotocol.io) — The full technical documentation

---

[← Back to all resources](../README.md)
