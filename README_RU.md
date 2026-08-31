# x-intel-mcp ⚡ Бессерверный движок разведки X/Twitter и анализа крипто-сентимента для AI-агентов

<div align="center">

[![NPM Version](https://img.shields.io/npm/v/x-intel-mcp?color=blue&style=for-the-badge&logo=npm)](https://www.npmjs.com/package/x-intel-mcp)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen?style=for-the-badge&logo=githubactions)](https://github.com/sosal123tyu1/x-intel-mcp/actions)
[![MCP Standard](https://img.shields.io/badge/MCP-Standard%201.0-blueviolet?style=for-the-badge)](https://modelcontextprotocol.io)
[![Twitter Stars](https://img.shields.io/github/stars/sosal123tyu1/x-intel-mcp?style=for-the-badge&logo=github)](https://github.com/sosal123tyu1/x-intel-mcp/stargazers)

**Высокопроизводительный Model Context Protocol (MCP) сервер, предоставляющий AI-агентам (Claude Code, Cursor, Pi, Windsurf) прямой доступ к поиску в Twitter/X, анализу тикеров (`$SOL`, `$BTC`), отслеживанию инфлюенсеров и скорингу настроений без ключей API.**

[English](README.md) | [Русский](README_RU.md) | [中文](README_ZH.md)

</div>

---

## ⚡ Зачем нужен x-intel-mcp?

Официальный Twitter API v2 стоит от **$100 до $5,000 в месяц** и требует корпоративной верификации.

`x-intel-mcp` дает вашим AI-агентам структурированный доступ к живому поиску в X, вирусным тредам, настроениям по токенам и альфа-каналам **без API-ключей, подписок и ограничений**.

### 🌟 Ключевые возможности

- 🔍 **Поиск по ключевым словам (`x_search`)**: Мгновенный поиск свежих твитов, обсуждений и тредов.
- 🪙 **Анализатор крипто-тикеров (`x_crypto_sentiment`)**: Автоматический скоринг по `$SOL`, `$BTC`, `$ETH`, мемкоинам и расчет бычьего/медвежьего индекса.
- 👤 **Парсер профилей и инфлюенсеров (`x_user_feed`)**: Получение последних постов и альфа-сигналов из любых аккаунтов.
- ⚡ **Нулевая настройка**: Готов к работе за 1 секунду через `npx x-intel-mcp` или `bunx x-intel-mcp`.
- 🔌 **Универсальный стандарт MCP**: 100% совместим с Claude Code CLI, Claude Desktop, Cursor IDE, Windsurf и Pi Agent.

---

## 🚀 Быстрый старт (1 минута)

### 1. Claude Code CLI

Добавьте `x-intel-mcp` в конфигурацию Claude Code:

```bash
claude mcp add x-intel -- npx x-intel-mcp
```

### 2. Claude Desktop

Добавьте в ваш `claude_desktop_config.json`:

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

В настройках Cursor Settings -> Features -> MCP Servers:

- **Name**: `x-intel`
- **Type**: `command`
- **Command**: `npx -y x-intel-mcp`

---

## 🛠 Доступные MCP инструменты

| Имя инструмента | Аргументы | Описание |
| :--- | :--- | :--- |
| `x_search` | `query` (строка), `limit` (число) | Поиск твитов, обсуждений и ссылок по ключевым словам в реальном времени. |
| `x_crypto_sentiment` | `ticker` (строка, напр. `SOL`), `limit` (число) | Сбор кэштегов и вычисление сентимент-скора (Strongly Bullish → Strongly Bearish). |
| `x_user_feed` | `username` (строка), `limit` (число) | Лента последних постов и реплаев любого публичного профиля Twitter. |

---

## 💻 Прямой запуск через CLI

Вы можете использовать `x-intel-mcp` прямо из терминала без MCP:

```bash
# Поиск в реальном времени
npx x-intel-mcp search "Claude 3.7"

# Анализ сентимента токена
npx x-intel-mcp sentiment "SOL"

# Чтение профиля
npx x-intel-mcp user "sama"
```

---

## 📄 Лицензия

MIT © [Ali Cent](https://github.com/sosal123tyu1)
