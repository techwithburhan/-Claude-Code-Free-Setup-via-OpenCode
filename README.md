# ⚡ Claude Code — Free Setup via OpenCode

> Use Anthropic's Claude Code CLI for **free** by pointing it at OpenCode's API endpoint instead of Anthropic's paid API.

---

## 📖 Table of Contents

- [What is This?](#what-is-this)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
  - [macOS](#-macos)
  - [Windows](#-windows)
  - [Linux](#-linux)
- [Configuration](#configuration)
- [Environment Variables](#environment-variables)
- [Quick Commands](#quick-commands)
- [Troubleshooting](#troubleshooting)
- [Resources](#resources)

---

## What is This?

This guide shows you how to set up **Claude Code** — Anthropic's official CLI coding assistant — configured to use **OpenCode's free API endpoint** (`https://opencode.ai/zen`) instead of Anthropic's paid API.

| Tool | Description | Link |
|------|-------------|------|
| **Claude Code** | Anthropic's official AI coding CLI | [claude.com/product/claude-code](https://claude.com/product/claude-code) |
| **OpenCode** | Free API endpoint compatible with Claude Code | [opencode.ai](https://opencode.ai/) |

---

## Prerequisites

- **Node.js v18 or higher** — [Download here](https://nodejs.org/en/download)
- A terminal (PowerShell, Terminal.app, Bash, Zsh, etc.)

---

## Installation

### 🍎 macOS

#### Step 1 — Install Node.js

**Option A: Homebrew (recommended)**
```bash
brew install node
```

**Option B: Direct installer**

Download and run the `.pkg` from [nodejs.org/en/download](https://nodejs.org/en/download).

Verify installation:
```bash
node --version
```

#### Step 2 — Install Claude Code

```bash
npm install -g @anthropic-ai/claude-code
```

#### Step 3 — Configure Settings

Open (or create) the settings file:
```bash
code ~/.claude/settings.json
```

Paste the following:
```json
{
  "env": {
    "ANTHROPIC_BASE_URL": "https://opencode.ai/zen",
    "ANTHROPIC_MODEL": "minimax-m2.5-free",
    "ANTHROPIC_API_KEY": "opencode-api-key",
    "ENABLE_TOOL_SEARCH": "true"
  }
}
```

Save the file and run `claude` in your terminal. ✅

---

### 🪟 Windows

#### Step 1 — Install Node.js

**Option A: Chocolatey (recommended)**
```powershell
choco install nodejs
```

**Option B: Direct installer**

Download and run the `.msi` from [nodejs.org/en/download](https://nodejs.org/en/download).

Verify installation:
```powershell
node --version
```

#### Step 2 — Install Claude Code

```powershell
npm install -g @anthropic-ai/claude-code
```

#### Step 3 — Configure Settings

Open (or create) the settings file:
```powershell
code $env:USERPROFILE\.claude\settings.json
```

Paste the following:
```json
{
  "env": {
    "ANTHROPIC_BASE_URL": "https://opencode.ai/zen",
    "ANTHROPIC_MODEL": "minimax-m2.5-free",
    "ANTHROPIC_API_KEY": "opencode-api-key",
    "ENABLE_TOOL_SEARCH": "true"
  }
}
```

Save the file and run `claude` in PowerShell. ✅

---

### 🐧 Linux

#### Step 1 — Install Node.js

**Debian / Ubuntu:**
```bash
sudo apt update && sudo apt install nodejs npm
```

**Fedora / RHEL:**
```bash
sudo dnf install nodejs npm
```

**Arch Linux:**
```bash
sudo pacman -S nodejs npm
```

Verify installation:
```bash
node --version
```

#### Step 2 — Install Claude Code

```bash
sudo npm install -g @anthropic-ai/claude-code
```

#### Step 3 — Configure Settings

Open (or create) the settings file:
```bash
code ~/.claude/settings.json
```

Paste the following:
```json
{
  "env": {
    "ANTHROPIC_BASE_URL": "https://opencode.ai/zen",
    "ANTHROPIC_MODEL": "minimax-m2.5-free",
    "ANTHROPIC_API_KEY": "opencode-api-key",
    "ENABLE_TOOL_SEARCH": "true"
  }
}
```

Save the file and run `claude` in your terminal. ✅

---

## Configuration

The settings file lives here depending on your OS:

| OS | Settings File Path |
|----|-------------------|
| macOS / Linux | `~/.claude/settings.json` |
| Windows | `%USERPROFILE%\.claude\settings.json` |

---

## Environment Variables

| Variable | Value | Description |
|----------|-------|-------------|
| `ANTHROPIC_BASE_URL` | `https://opencode.ai/zen` | OpenCode's free API endpoint |
| `ANTHROPIC_MODEL` | `minimax-m2.5-free` | The free model to use |
| `ANTHROPIC_API_KEY` | `opencode-api-key` | API key (required by the CLI, any string works) |
| `ENABLE_TOOL_SEARCH` | `true` | Enables tool/web search feature |

---

## Quick Commands

| Command | Description |
|---------|-------------|
| `claude` | Start an interactive session |
| `claude -p "<prompt>"` | Run a single one-off prompt |
| `claude --verbose` | Enable verbose/debug logging |

---

## Troubleshooting

| Problem | Fix |
|---------|-----|
| `node: command not found` | Restart your terminal after installing Node.js, or manually add it to your `PATH` |
| `Permission denied` on Linux/Mac | Use `sudo` before the npm install command |
| `permission denied` on Windows | Run PowerShell as Administrator |
| API errors or empty responses | Double-check that `ANTHROPIC_BASE_URL` is set to exactly `https://opencode.ai/zen` |
| `claude: command not found` after install | Make sure your npm global bin directory is in your `PATH` |

---

## Resources

- 🌐 [OpenCode Website](https://opencode.ai/)
- 🤖 [Claude Code Product Page](https://claude.com/product/claude-code)
- 📦 [Node.js Downloads](https://nodejs.org/en/download)
- 📖 [Anthropic Docs](https://docs.anthropic.com)

---

> **Note:** This setup uses OpenCode's free tier. Usage limits and model availability may change. Check [opencode.ai](https://opencode.ai) for the latest information.
