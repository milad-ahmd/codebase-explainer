> [!NOTE]
> **This skill lives in the main collection: [milad-ahmd/agent-skills](https://github.com/milad-ahmd/agent-skills/tree/main/skills/codebase-explainer)**. Please ⭐ star it there; that's where updates land first.
> Docs: **https://milad-ahmd.github.io/agent-skills/skills/codebase-explainer/** · Claude Code: `/plugin install all-skills --marketplace milad-ahmd/agent-skills`

<div align="center">

# 🗺️ codebase-explainer

**Onboarding guide built from a real import graph: entry points, hubs, cycles, Mermaid and an interactive map. An Agent Skill for Claude Code, Cline, Cursor, Codex and other AI coding agents.**

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
Map how the modules in this repo depend on each other
```

The full workflow, rules and output format are in [`SKILL.md`](skills/codebase-explainer/SKILL.md).

## 🔎 Sample output

`code_map.py` is plain Python 3 with no dependencies. Real output on the small Python fixture that ships with it:

```text
$ python3 code_map.py fixtures/pyapp

Code map of pyapp: 11 files, 41 LOC (python 11)
4 modules at depth 2, 12 internal file edges, 3 module edges, 1 external packages

Modules (by LOC)
  module                                    files      LOC  fan-in  fan-out   ext
  mypkg                                         6       27       3        0     1
  .                                             2        5       0        1     0
  tests                                         1        5       0        1     0
  mypkg/sub                                     2        4       0        1     0

Entry points (2)
  main.py  [__main__ guard, file name]
  mypkg/cli.py  [file name, pyproject.toml script]

Hubs: most imported files, change with care (1)
  mypkg/core.py  imported by 7 files (+1 tests), 6 LOC, in a cycle

Import cycles: 2 between files, 0 between modules
  [import-time] mypkg/core.py -> mypkg/utils.py -> mypkg/core.py
  [lazy only]   mypkg/lazy.py -> mypkg/models.py -> mypkg/lazy.py

Orphans: not imported and not an entry point (2)
  mypkg/sub/deep.py
  orphan.py

External packages (top 1 of 1)
  requests                          1 file(s)  (python)

Not visible to this static parse: imports built from strings at runtime, DI containers, reflection, plugin loading, framework conventions (routes, decorators) and calls between services over HTTP.
```

`--format mermaid` gives a diagram for the guide, and `--format html --out map.html` writes one self-contained interactive map (no CDN, no network) for exploring.

## 🧩 More skills

See the full collection: **[milad-ahmd/agent-skills](https://github.com/milad-ahmd/agent-skills)**.

## 🤝 Contributing

This repo is a read-only mirror. Please open issues and PRs in **[milad-ahmd/agent-skills](https://github.com/milad-ahmd/agent-skills)**.

## 📄 License

[MIT](LICENSE) © Milad Ahmadi

<div align="center">

**If this skill saved you time, a ⭐ helps others find it.**

</div>
