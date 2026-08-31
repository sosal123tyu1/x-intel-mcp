# x-intel-mcp ⚡ Zero-Auth Twitter/X Intelligence Engine for AI Agents

<div align="center">

[![NPM Version](https://img.shields.io/npm/v/x-intel-mcp?color=blue&style=for-the-badge&logo=npm)](https://www.npmjs.com/package/x-intel-mcp)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen?style=for-the-badge&logo=githubactions)](https://github.com/sosal123tyu1/x-intel-mcp/actions)
[![MCP Standard](https://img.shields.io/badge/MCP-Standard%201.0-blueviolet?style=for-the-badge)](https://modelcontextprotocol.io)
[![Twitter Stars](https://img.shields.io/github/stars/sosal123tyu1/x-intel-mcp?style=for-the-badge&logo=github)](https://github.com/sosal123tyu1/x-intel-mcp/stargazers)

**A high-performance Model Context Protocol (MCP) server providing zero-auth Twitter/X intelligence, crypto ticker cashtag analysis (`$SOL`, `$BTC`), whale tracking, and AI-driven sentiment scoring directly into Claude Code, Cursor, Pi, and Windsurf.**

[English](README.md) | [Русский](README_RU.md) | [中文](README_ZH.md)

</div>

---

## ⚡ Why x-intel-mcp?

Standard Twitter API v2 costs **$100–$5,000/month** and requires enterprise developer accounts. 

`x-intel-mcp` gives AI agents direct, structured access to live Twitter search streams, viral tweets, cashtag sentiment, and influencer alpha feeds **without requiring any API key or subscription**.

### 🌟 Key Capabilities

- 🔍 **Live Query Search (`x_search`)**: Fetch recent viral tweets, quotes, and threads on any topic.
- 🪙 **Crypto Cashtag Analyzer (`x_crypto_sentiment`)**: Scrape live sentiment on `$SOL`, `$BTC`, `$ETH`, meme coins, and calculate bullish/bearish ratio.
- 👤 **Influencer Feed Extractor (`x_user_feed`)**: Extract full timelines and alpha calls from specified Twitter accounts.
- ⚡ **Zero Setup**: Ready to use out of the box via `npx x-intel-mcp` or `bunx x-intel-mcp`.
- 🔌 **Universal MCP Support**: 100% compatible with Claude Code, Cursor, Windsurf, Pi Agent, and LibreChat.

---

## 🚀 Quick Setup (1 Minute)

### 1. Claude Code CLI

Add `x-intel-mcp` to your global Claude Code configuration:

```bash
claude mcp add x-intel -- npx x-intel-mcp
```

### 2. Claude Desktop App

Add to your `claude_desktop_config.json`:

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

### 3. Cursor IDE / Windsurf

Add in Cursor Settings -> Features -> MCP Servers:

- **Name**: `x-intel`
- **Type**: `command`
- **Command**: `npx -y x-intel-mcp`

---

## 🛠 Available MCP Tools

| Tool Name | Arguments | Description |
| :--- | :--- | :--- |
| `x_search` | `query` (string), `limit` (number) | Search real-time tweets, engagements, and links by keyword. |
| `x_crypto_sentiment` | `ticker` (string, e.g. `SOL`), `limit` (number) | Aggregate live cashtag posts and calculate net sentiment score. |
| `x_user_feed` | `username` (string), `limit` (number) | Stream latest tweets and replies from any public Twitter profile. |

---

## 📊 Example Agent Prompts

Once installed, simply ask your agent in natural language:

> *"Analyze current Twitter sentiment on $SOL for the past 2 hours and summarize key narratives."*

> *"What are the top 5 tweets regarding the latest Anthropic Claude 3.7 release?"*

> *"Check the recent tweets from @vitalikbuterin and summarize his thoughts on L2 scaling."*

---

## 💻 CLI Direct Execution

You can also run `x-intel-mcp` standalone from the command line:

```bash
# Direct search
npx x-intel-mcp search "Claude 3.7"

# Analyze crypto sentiment
npx x-intel-mcp sentiment "SOL"

# Read user profile
npx x-intel-mcp user "sama"
```

---

## 🤝 Contributing & Star History

We welcome pull requests! Star the repository if this helped your AI workflow:

[![Star History Chart](https://api.star-history.com/svg?repos=sosal123tyu1/x-intel-mcp&type=Date)](https://star-history.com/#sosal123tyu1/x-intel-mcp&Date)

---

## 📄 License

MIT © [Ali Cent](https://github.com/sosal123tyu1)
