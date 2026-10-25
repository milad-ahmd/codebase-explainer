<div align="center">

# 🗺️ codebase-explainer

**Onboarding guide for any repo, with Mermaid architecture diagrams. An Agent Skill for Claude Code, Cline, Cursor, Codex and other AI coding agents.**

[![License: MIT](https://img.shields.io/github/license/milad-ahmd/codebase-explainer)](LICENSE)
[![Stars](https://img.shields.io/github/stars/milad-ahmd/codebase-explainer?style=social)](https://github.com/milad-ahmd/codebase-explainer)
![Category](https://img.shields.io/badge/category-Documentation-blue)
![Works with](https://img.shields.io/badge/works%20with-Claude%20Code%20%7C%20Cline%20%7C%20Cursor%20%7C%20Codex-8A2BE2)

[Install](#-install) · [Usage](#-usage) · [How it works](skills/codebase-explainer/SKILL.md) · [All skills](https://github.com/milad-ahmd/agent-skills)

</div>

> Part of **[agent-skills](https://github.com/milad-ahmd/agent-skills)**, a growing collection of practical skills for AI coding agents.

## 📦 Install

**One command (installs the whole collection):**

```bash
curl -fsSL https://raw.githubusercontent.com/milad-ahmd/agent-skills/main/install.sh | bash -s -- codebase-explainer
```

**Manually (Claude Code):**

```bash
git clone https://github.com/milad-ahmd/codebase-explainer /tmp/codebase-explainer
mkdir -p ~/.claude/skills && cp -r /tmp/codebase-explainer/skills/codebase-explainer ~/.claude/skills/
```

**Per project:** copy `skills/codebase-explainer` into `<project>/.claude/skills/`.
**Any other agent:** paste [`SKILL.md`](skills/codebase-explainer/SKILL.md) into your rules or system prompt.

## 💬 Usage

Just ask your agent:

```text
Explain this codebase
Where do I start in this repo?
```

The full workflow, rules and output format are in [`SKILL.md`](skills/codebase-explainer/SKILL.md).

## 🧩 More skills

See the full collection: **[milad-ahmd/agent-skills](https://github.com/milad-ahmd/agent-skills)**.

## 🤝 Contributing

Issues and PRs are welcome, especially real-world before/after examples.

## 📄 License

[MIT](LICENSE) © Milad Ahmadi

<div align="center">

**If this skill saved you time, a ⭐ helps others find it.**

</div>
