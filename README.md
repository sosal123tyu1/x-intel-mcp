<div align="center">

# ⚡ x-intel-mcp

**Zero-fee X/Twitter & Social Intelligence for AI Agents**  
*Model Context Protocol (MCP) Server for Claude Desktop, Cursor, Pi, and any MCP client.*

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)
[![MCP Compatible](https://img.shields.io/badge/MCP-1.0-8A2BE2.svg?style=flat-square)](https://modelcontextprotocol.io)
[![Runtime: Node / Bun](https://img.shields.io/badge/Runtime-Node%20%7C%20Bun-orange.svg?style=flat-square)](https://bun.sh)
[![Zero Config](https://img.shields.io/badge/API_Keys-None_Required-success.svg?style=flat-square)](#)

[Features](#-features) • [Quickstart](#-quickstart) • [Claude Desktop Setup](#-claude-desktop-setup) • [Tools](#-available-tools) • [Architecture](#-architecture)

</div>

---

## 🚀 Why x-intel-mcp?

X/Twitter official API starts at **$100/mo** with heavy rate limits. Most AI agents just need to read public sentiment, recent developer discussions, or search keywords without passing expensive API keys into every prompt.

`x-intel-mcp` is a lightweight, zero-configuration MCP server running locally via `stdio`. It connects your favorite AI agent directly to live public posts without authentication.

---

## ✨ Features

- 🆓 **Zero API Keys Required** — Works out-of-the-box via public syndication endpoints and Nitter instances.
- ⚡ **Sub-second Responses** — Fast local runtime (Bun or Node.js).
- 🧩 **100% MCP Standard** — Drop-in compatibility with **Claude Desktop**, **Cursor IDE**, **Pi**, and **Windsurf**.
- 🛡️ **Privacy-First** — Runs entirely on your local machine; no intermediary proxies recording your queries.

---

## 📦 Quickstart

### Run with `npx` (No installation needed)

```bash
npx x-intel-mcp
```

### Or using `bunx`

```bash
bunx x-intel-mcp
```

---

## ⚙️ Claude Desktop Setup

Add the following to your `claude_desktop_config.json`:

* **macOS:** `~/Library/Application Support/Claude/claude_desktop_config.json`  
* **Windows:** `%APPDATA%\Claude\claude_desktop_config.json`  
* **Linux:** `~/.config/Claude/claude_desktop_config.json`

```json
{
  "mcpServers": {
    "x-intel": {
      "command": "npx",
      "args": ["-y", "x-intel-mcp"]
    }
  }
}
```

Restart Claude Desktop, and the tools will automatically appear in your chat interface.

---

## 🛠️ Available Tools

### 1. `x_search`
Search public posts on X by keyword or hashtag.

```json
{
  "query": "Rust MCP server",
  "limit": 10
}
```

### 2. `x_profile`
Fetch the latest public posts from a specific X user.

```json
{
  "handle": "karpathy",
  "limit": 5
}
```

---

## 🏗️ Architecture

```
[ AI Agent (Claude / Cursor / Pi) ]
               │
               ▼  (stdio / JSON-RPC)
       [ x-intel-mcp ]
               │
       ┌───────┴───────┐
       ▼               ▼
[ Syndication API ]  [ Nitter RSS ]
       │               │
       └───────┬───────┘
               ▼
   [ Structured JSON Output ]
```

---

## 💻 Local Development

```bash
git clone https://github.com/sosal123tyu1/x-intel-mcp.git
cd x-intel-mcp
bun install
bun run dev
```

---

## 📄 License

MIT © [sosal123tyu1](https://github.com/sosal123tyu1)
