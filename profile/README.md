<div align="center">

# 🚀 dotAIslash

### **VERSA** - Universal Rules for AI Agents
#### Vendor-neutral Extensible Repo Spec for Agents

**One `.ai/` folder, every runtime**

[![Website](https://img.shields.io/badge/🌐_Website-dotaislash.github.io-violet?style=for-the-badge)](https://dotaislash.github.io)
[![Spec](https://img.shields.io/badge/📖_Read_Spec-VERSA_1.0-cyan?style=for-the-badge)](https://github.com/dotAIslash/dotaislash-spec)
[![Discussions](https://img.shields.io/github/discussions/dotAIslash/dotaislash-spec?style=for-the-badge&label=💬%20Discussions&color=lime)](https://github.com/dotAIslash/dotaislash-spec/discussions)

---

### 🎯 The Problem

Every AI coding tool has its own config format:
- 🔴 Cursor uses `.cursorrules`
- 🔵 Windsurf has its own format
- 🟢 Claude projects differ
- 🟡 Aider uses `.aider.conf.yml`

**Result:** Fragmented, tool-specific configuration

### ✨ The Solution

</div>

```
your-project/
└── .ai/                      ← One folder
    ├── context.json          ← One standard
    ├── profiles/             ← Every runtime
    │   ├── cursor.json
    │   ├── windsurf.json
    │   └── claude.json
    ├── rules/
    │   └── style.md
    └── agents/
        └── code-reviewer.json
```

<div align="center">

**VERSA: Write once, run everywhere.**

</div>

---

## 🌟 Features

<table>
<tr>
<td width="25%" align="center">

### 🔄 Portable
One `.ai/` folder works with **every tool** that supports VERSA

</td>
<td width="25%" align="center">

### 🔐 Security-First
Explicit **deny → ask → allow** permissions with secret bindings

</td>
<td width="25%" align="center">

### 🎯 Simple
Plain **JSON** and **Markdown**. Git-friendly. Easy to diff.

</td>
<td width="25%" align="center">

### ✨ Versatile
**8 primitives** cover rules, prompts, agents, memory, tools, and more

</td>
</tr>
</table>

---

## 📦 Official Packages

<table>
<tr>
<td width="50%">

### 📋 [dotaislash-spec](https://github.com/dotAIslash/dotaislash-spec)
Canonical VERSA 1.0 specification

### 🔧 [dotaislash-cli](https://github.com/dotAIslash/dotaislash-cli)
Reference CLI tool (`versa init`, `lint`, `context`)

### 📐 [dotaislash-schemas](https://github.com/dotAIslash/dotaislash-schemas)
JSON Schema validation for `.ai/` files

### 📚 [dotaislash-examples](https://github.com/dotAIslash/dotaislash-examples)
Example configurations for various project types

</td>
<td width="50%">

### 🔌 [dotaislash-adapters](https://github.com/dotAIslash/dotaislash-adapters)
Transform VERSA to native tool formats

### ✅ [dotaislash-conformance](https://github.com/dotAIslash/dotaislash-conformance)
Test suite for VERSA-compatible runtimes

### 🌐 [dotaislash.github.io](https://github.com/dotAIslash/dotaislash.github.io)
Landing site and documentation

### ⚙️ [.github](https://github.com/dotAIslash/.github)
Organization profile and workflows

</td>
</tr>
</table>

---

## 🎯 Core Concepts

VERSA defines **8 canonical primitives** for agent configuration:

| Primitive | Purpose | Example |
|-----------|---------|---------|
| 📜 **Rules** | Project context & guidelines | Code style, architecture patterns |
| 💬 **Prompts** | Reusable templates | Bug report, feature spec |
| 🤖 **Agents** | Declarative agent configs | Code reviewer, documenter |
| 🧠 **Memory** | Retention policies | Session, project, persistent |
| 📚 **Knowledge** | Document ingestion | Docs, repos, URLs |
| 🛠️ **Tools** | MCP servers & APIs | Custom capabilities |
| ⚙️ **Settings** | Model routing | GPT-4, Claude, temperature |
| 🛡️ **Permissions** | Security policies | File access, secrets |

---

## 🚀 Quick Start

### 1. Create a `.ai/` folder

```bash
mkdir .ai
cd .ai
```

### 2. Add `context.json`

```json
{
  "version": "1.0",
  "rules": ["rules/style.md"],
  "context": ["src/**/*.ts"],
  "settings": {
    "model": "claude-sonnet-4"
  }
}
```

### 3. Add tool-specific profiles

```json
// .ai/profiles/cursor.json
{
  "version": "1.0",
  "merge": "deep",
  "settings": {
    "shortcuts": {
      "review": "agents/code-reviewer.json"
    }
  }
}
```

### 4. Write your rules

```markdown
<!-- .ai/rules/style.md -->
ai:meta
  priority: high
  attach: always
---

# Code Style Guide

- TypeScript strict mode
- Functional components
- Max line length: 100
```

---

## 🛠️ Supported Tools

<div align="center">

| Tool | Status | Adapter |
|------|--------|---------|
| **Cursor** | 🟡 Beta | [dotaislash-adapters](https://github.com/dotAIslash/dotaislash-adapters) |
| **Windsurf** | 🟡 Beta | [dotaislash-adapters](https://github.com/dotAIslash/dotaislash-adapters) |
| **Aider** | 🔴 Planned | Coming soon |
| **Claude** | 🔴 Planned | Coming soon |
| **Cody** | 🔴 Planned | Coming soon |

</div>

---

## 🎓 Documentation

- 📖 **[Read the Spec](https://github.com/dotAIslash/dotaislash-spec)** - Full VERSA 1.0 specification
- 🚀 **[Quick Start Guide](https://dotaislash.github.io)** - Get started in 5 minutes
- 📚 **[Examples](https://github.com/dotAIslash/dotaislash-examples)** - Real-world configurations
- 🔧 **[CLI Documentation](https://github.com/dotAIslash/dotaislash-cli)** - Command reference
- 💬 **[Discussions](https://github.com/dotAIslash/dotaislash-spec/discussions)** - Ask questions, share ideas

---

## 🤝 Contributing

We're building VERSA openly with the community!

### Ways to Contribute

- 💡 **Share Ideas** - Join [discussions](https://github.com/dotAIslash/dotaislash-spec/discussions)
- 🐛 **Report Issues** - Found a problem? [Open an issue](https://github.com/dotAIslash/dotaislash-spec/issues)
- 📝 **Improve Docs** - Help others understand VERSA
- 🔧 **Build Adapters** - Support a new tool
- 📚 **Create Examples** - Share your `.ai/` configs
- 🧪 **Write Tests** - Improve conformance suite

See individual repositories for contributing guidelines.

---

## 🗺️ Roadmap

### Q4 2025 - v1.0 Stable
- ✅ Core specification
- ✅ Website launch
- ⏳ JSON Schemas
- ⏳ Reference CLI
- ⏳ Basic adapters

### Q1 2026 - Ecosystem Growth
- 📦 npm packages
- 🔌 Community adapters
- 📚 Comprehensive examples
- 🎓 Integration tutorials

### Q2 2026 - Adoption
- 🤝 Tool partnerships
- 🌍 Multi-language support
- 🔐 Advanced security
- 🚀 Performance optimizations

---

## 💡 Philosophy

> **Boring is Beautiful**
> 
> Plain JSON and Markdown. No DSLs. No magic. Just simple, portable formats.

> **Convention over Configuration**
> 
> Sensible defaults. Minimal required fields. Override only what you need.

> **Security by Default**
> 
> Explicit permissions. Deny-first policies. Secrets never in code.

---

## 📊 Status

| Component | Status |
|-----------|--------|
| **Specification** | 🟡 Draft (v1.0) |
| **JSON Schemas** | 🟡 In Progress |
| **CLI Tool** | 🟡 In Progress |
| **Adapters** | 🔴 Planned |
| **Conformance** | 🔴 Planned |

**Legend:** 🟢 Stable · 🟡 In Progress · 🔴 Planned

---

## 🔗 Links

<div align="center">

[![Website](https://img.shields.io/badge/🌐_Website-dotaislash.github.io-violet?style=flat-square)](https://dotaislash.github.io)
[![Spec](https://img.shields.io/badge/📖_Spec-Read_VERSA_1.0-cyan?style=flat-square)](https://github.com/dotAIslash/dotaislash-spec)
[![Discussions](https://img.shields.io/badge/💬_Discussions-Join_Community-lime?style=flat-square)](https://github.com/dotAIslash/dotaislash-spec/discussions)
[![Issues](https://img.shields.io/badge/🐛_Issues-Report_Bug-pink?style=flat-square)](https://github.com/dotAIslash/dotaislash-spec/issues)

</div>

---

<div align="center">

### **VERSA** - Universal Rules for AI Agents

**One folder. Every runtime. Portable forever.**

🌟 Star our repos · 💬 Join discussions · 🚀 Build the future of AI agent configuration

</div>
