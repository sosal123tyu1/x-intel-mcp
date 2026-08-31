<div align="center">

# ⚡ x-intel-mcp

**面向 AI Agent 的免费 X/Twitter 社交情报 MCP 服务器**  
*适用于 Claude Desktop、Cursor、Pi 以及任何 MCP 客户端的 Model Context Protocol 服务器。*

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)
[![MCP Compatible](https://img.shields.io/badge/MCP-1.0-8A2BE2.svg?style=flat-square)](https://modelcontextprotocol.io)
[![Runtime: Node / Bun](https://img.shields.io/badge/Runtime-Node%20%7C%20Bun-orange.svg?style=flat-square)](https://bun.sh)
[![Zero Config](https://img.shields.io/badge/API_Keys-无需密钥-success.svg?style=flat-square)](#)

[English](README.md) • [Русский](README_RU.md) • [中文](README_ZH.md)

</div>

---

## 🚀 为什么选择 x-intel-mcp？

X/Twitter 官方 API 每月起步价为 **$100**，并且有严格的调用频率限制。大多数 AI Agent 仅需检索公开讨论、开发者动态或关键词推文，无需为每个 Prompt 购买昂贵的 API Key。

`x-intel-mcp` 是一个轻量级本地 MCP 服务器，通过 `stdio` 协议运行。它能将您的 AI 助手直接连接到公开的社交情报源，无需任何身份验证。

---

## ✨ 核心特性

- 🆓 **完全免费** — 无需 API Key，利用公开聚合接口检索。
- ⚡ **极速响应** — 基于轻量级 Bun / Node.js 运行时。
- 🧩 **标准 MCP 协议** — 开箱即用支持 **Claude Desktop**, **Cursor**, **Pi**, **Windsurf**。
- 🛡️ **本地隐私** — 完全运行在本地，绝不上报查询内容。

---

## 📦 快速上手

### 使用 `npx` 运行（无需全局安装）

```bash
npx x-intel-mcp
```

### 或使用 `bunx`

```bash
bunx x-intel-mcp
```

---

## ⚙️ Claude Desktop 配置

将以下内容添加到您的 `claude_desktop_config.json` 中：

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

---

## 🛠️ 可用工具

### 1. `x_search`
通过关键词或话题标签搜索公开推文。

```json
{
  "query": "Rust MCP server",
  "limit": 10
}
```

### 2. `x_profile`
获取特定公开用户的最新推文。

```json
{
  "handle": "karpathy",
  "limit": 5
}
```

---

## 📄 开源协议

MIT © [sosal123tyu1](https://github.com/sosal123tyu1)
