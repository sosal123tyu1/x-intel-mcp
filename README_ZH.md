# x-intel-mcp ⚡ 面向 AI Agent 的免 API 密钥 Twitter/X 实时情报与情绪分析引擎

<div align="center">

[![NPM Version](https://img.shields.io/npm/v/x-intel-mcp?color=blue&style=for-the-badge&logo=npm)](https://www.npmjs.com/package/x-intel-mcp)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen?style=for-the-badge&logo=githubactions)](https://github.com/sosal123tyu1/x-intel-mcp/actions)
[![MCP Standard](https://img.shields.io/badge/MCP-Standard%201.0-blueviolet?style=for-the-badge)](https://modelcontextprotocol.io)
[![Twitter Stars](https://img.shields.io/github/stars/sosal123tyu1/x-intel-mcp?style=for-the-badge&logo=github)](https://github.com/sosal123tyu1/x-intel-mcp/stargazers)

**高性能 Model Context Protocol (MCP) 服务，为 Claude Code、Cursor、Pi 和 Windsurf 等 AI 智能体提供零配置 Twitter/X 搜索、加密代币行情标签分析 (`$SOL`, `$BTC`) 和社交情绪评分。**

[English](README.md) | [Русский](README_RU.md) | [中文](README_ZH.md)

</div>

---

## ⚡ 为什么选择 x-intel-mcp？

官方 Twitter API v2 每月费用高达 **$100 至 $5,000**，且需要繁琐的企业开发者认证。

`x-intel-mcp` 让您的 AI 智能体能够直接获得推特实时搜索流、热点推文、加密代币情绪和 KOL 动态，**无需任何 API 密钥或付费订阅**。

### 🌟 核心特性

- 🔍 **实时搜索 (`x_search`)**：按关键词即时获取最新推文、互动与讨论。
- 🪙 **加密情绪分析 (`x_crypto_sentiment`)**：抓取 `$SOL`、`$BTC`、`$ETH` 等代币标签并计算多空情绪指数。
- 👤 **博主推文提取 (`x_user_feed`)**：抓取任意公开账号的最新推文与回复。
- ⚡ **零配置启动**：支持 `npx x-intel-mcp` 或 `bunx x-intel-mcp` 一键运行。
- 🔌 **通用 MCP 支持**：完美兼容 Claude Code、Cursor、Windsurf、Pi 等主流智能体。

---

## 🚀 快速开始

### 1. Claude Code CLI

添加至 Claude Code 配置：

```bash
claude mcp add x-intel -- npx x-intel-mcp
```

### 2. Claude Desktop

在 `claude_desktop_config.json` 中添加：

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

在 Cursor 设置 -> Features -> MCP Servers 中添加：

- **Name**: `x-intel`
- **Type**: `command`
- **Command**: `npx -y x-intel-mcp`

---

## 🛠 工具列表

| 工具名称 | 参数 | 说明 |
| :--- | :--- | :--- |
| `x_search` | `query` (字符串), `limit` (数字) | 按关键词搜索推特最新内容。 |
| `x_crypto_sentiment` | `ticker` (字符串，如 `SOL`), `limit` (数字) | 汇总代币标签推文并计算情绪多空评分。 |
| `x_user_feed` | `username` (字符串), `limit` (数字) | 获取指定推特用户的最新推文。 |

---

## 📄 开源协议

MIT © [Ali Cent](https://github.com/sosal123tyu1)
