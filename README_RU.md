<div align="center">

# ⚡ x-intel-mcp

**Бесплатный MCP-сервер для поиска и сбора информации в X/Twitter для AI-агентов**  
*Model Context Protocol (MCP) сервер для Claude Desktop, Cursor, Pi и любых MCP-клиентов.*

[![NPM Version](https://img.shields.io/npm/v/x-intel-mcp?style=flat-square&color=indigo)](https://www.npmjs.com/package/x-intel-mcp)
[![NPM Downloads](https://img.shields.io/npm/dm/x-intel-mcp?style=flat-square&color=blue)](https://www.npmjs.com/package/x-intel-mcp)
[![License: MIT](https://img.shields.io/badge/License-MIT-emerald.svg?style=flat-square)](LICENSE)
[![MCP Compatible](https://img.shields.io/badge/MCP-1.0-8A2BE2.svg?style=flat-square)](https://modelcontextprotocol.io)
[![Runtime: Node / Bun](https://img.shields.io/badge/Runtime-Node%20%7C%20Bun-orange.svg?style=flat-square)](https://bun.sh)
[![Zero Config](https://img.shields.io/badge/API_Keys-Не_требуются-success.svg?style=flat-square)](#)

[English](README.md) • [Русский](README_RU.md) • [中文](README_ZH.md)

</div>

---

## 🚀 Зачем нужен x-intel-mcp?

Официальный API X/Twitter стоит от **$100 в месяц** и имеет жесткие лимиты. Большинству AI-агентов нужен лишь доступ к публичным обсуждениям, трендам и поиску постов без необходимости платить за API и вставлять ключи в каждый промпт.

`x-intel-mcp` — легковесный локальный MCP-сервер, работающий через `stdio`. Он подключает вашего AI-ассистента к открытым данным X напрямую без авторизации с использованием ротации публичных зеркал.

---

## ✨ Возможности

- 🆓 **0 рублей за API** — работает напрямую через открытые syndication-эндпоинты и зеркала.
- ⚡ **Мгновенный ответ** — легковесный рантайм на Bun / Node.js.
- 🧩 **Стандарт MCP 1.0** — поддержка **Claude Desktop**, **Cursor IDE**, **Pi**, **Windsurf**.
- 🛡️ **Приватность** — запросы идут локально с вашего компьютера, без сторонних прокси.

---

## 📦 Быстрый запуск

### Через `npx` (без установки)

```bash
npx x-intel-mcp
```

### Через `bunx`

```bash
bunx x-intel-mcp
```

---

## ⚙️ Настройка в Claude Desktop

Добавьте конфигурацию в `claude_desktop_config.json`:

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

## 🛠️ Доступные инструменты

### 1. `x_search`
Поиск публичных твитов по ключевому слову или хештегу.

```json
{
  "query": "Rust MCP server",
  "limit": 10
}
```

### 2. `x_profile`
Получение последних постов из профиля пользователя.

```json
{
  "handle": "karpathy",
  "limit": 5
}
```

---

## 📄 Лицензия

[MIT](LICENSE) © 2026 [Ali Cent (sosal123tyu1)](https://github.com/sosal123tyu1)
