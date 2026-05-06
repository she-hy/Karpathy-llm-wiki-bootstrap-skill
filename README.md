# Karpathy LLM Wiki Bootstrap

[简体中文](./README.zh-CN.md)

Build persistent, LLM-maintained Markdown wikis from articles, papers, books, research notes, and other source material.

![Cover image for Karpathy LLM Wiki Bootstrap](./cover-image/llm-wiki/cover.png)

This repository includes both an installable skill and a working reference wiki. The skill bootstraps a new wiki; the reference wiki shows the pattern in action, starting from [Karpathy's LLM Wiki idea](./karpathy-llm-wiki-original.md) and compiling it into durable pages, links, concepts, comparisons, and synthesis.

The goal is not a one-off summary. It is a knowledge artifact that can keep improving through repeated ingest, query, and lint cycles.

## Why This Exists

Most LLM document workflows behave like query-time RAG: retrieve a few chunks, answer the current question, then lose the intermediate structure. An LLM Wiki moves more work into a maintained Markdown layer.

| Layer | Purpose |
| --- | --- |
| `raw/` | Immutable source material and evidence |
| `wiki/` | LLM-maintained summaries, concepts, entities, comparisons, and synthesis |
| `SCHEMA.md` | The operating contract every agent follows |
| Pointer files | Thin runtime redirects such as `AGENTS.md`, `CLAUDE.md`, or `.github/copilot-instructions.md` |

The result is a wiki that compounds: new sources update existing pages, useful answers can be filed back, and linting keeps the structure healthy.

## What Is Included

- [skill/](./skill): the installable skill package with templates and workflows.
- [llm-wiki/](./llm-wiki): a real reference wiki generated and maintained with the skill.
- [karpathy-llm-wiki-original.md](./karpathy-llm-wiki-original.md): repository copy of the original idea note.
- [from-article-to-llm-wiki.article.en.md](./from-article-to-llm-wiki.article.en.md): full walkthrough article.

## Quick Start

Install the skill:

```bash
npx skills add nanzhipro/Karpathy-llm-wiki-bootstrap-skill@llm-wiki-bootstrap
```

Then ask your agent:

```text
bootstrap a wiki
```

When prompted, choose values such as:

| Question | Example answer |
| --- | --- |
| Domain | `Research topic` |
| Wiki name | `llm-wiki-demo` |
| Runtime | `OpenAI Codex`, `Claude Code`, or `Copilot (VS Code)` |
| Editor | `Obsidian` or `VS Code` |
| Source types | `Web articles` |
| Output location | `Current directory` |

Add a source:

```bash
cp karpathy-llm-wiki-original.md llm-wiki-demo/raw/
```

Then tell the agent:

```text
Read llm-wiki-demo/SCHEMA.md, then ingest llm-wiki-demo/raw/karpathy-llm-wiki-original.md
```

After the first ingest, inspect:

- `llm-wiki-demo/wiki/index.md`
- `llm-wiki-demo/wiki/concept-table.md`
- `llm-wiki-demo/wiki/overview.md`
- `llm-wiki-demo/wiki/log.md`

For a Chinese-language wiki, tell the agent directly:

```text
使用中文编译 karpathy-llm-wiki-original.md
```

## Reference Wiki

[llm-wiki/](./llm-wiki) is the best place to understand the system quickly. It is not placeholder content; it is a maintained example wiki built from real source material.

Useful entry points:

| File | Why open it |
| --- | --- |
| [llm-wiki/SCHEMA.md](./llm-wiki/SCHEMA.md) | Authoritative operating contract for agents |
| [llm-wiki/wiki/index.md](./llm-wiki/wiki/index.md) | Catalog of all wiki pages |
| [llm-wiki/wiki/concept-table.md](./llm-wiki/wiki/concept-table.md) | Maintained concept map with definitions, relationships, sources, status, and maintenance notes |
| [llm-wiki/wiki/overview.md](./llm-wiki/wiki/overview.md) | Top-level synthesis of the wiki |
| [llm-wiki/wiki/log.md](./llm-wiki/wiki/log.md) | Chronological operation history |

Current shape:

```text
llm-wiki/
├── SCHEMA.md
├── AGENTS.md
├── raw/
│   ├── Karpathy x.md
│   └── llm-wiki-pattern.md
└── wiki/
    ├── index.md
    ├── concept-table.md
    ├── overview.md
    ├── log.md
    ├── concepts/
    ├── entities/
    ├── comparisons/
    ├── sources/
    └── synthesis/
```

## Core Workflow

| Operation | Trigger | Result |
| --- | --- | --- |
| Ingest | `ingest raw/{file}` | Reads a source, creates or updates wiki pages, updates the concept table, index, overview, and log |
| Query | Ask a domain question | Reads the index and relevant pages, optionally uses BM25, then answers with wiki citations |
| Lint | `lint` or `health check` | Finds contradictions, stale claims, orphan pages, concept-table drift, and missing links |

The key files created inside each wiki are:

| File | Role |
| --- | --- |
| `SCHEMA.md` | Single source of truth for agent behavior |
| `wiki/index.md` | Page catalog and primary navigation surface |
| `wiki/concept-table.md` | Compressed concept map for definitions, relationships, evidence status, and maintenance notes |
| `wiki/overview.md` | High-level synthesis |
| `wiki/log.md` | Append-only operation history |

## Optional BM25 Search

For larger wikis, the skill can initialize a local SQLite FTS5/BM25 search layer. BM25 is a candidate finder, not a source of truth: the agent must open returned `wiki/` pages before answering.

Common commands inside a generated wiki:

```bash
python3 scripts/wiki_fts.py doctor
python3 scripts/wiki_fts.py build
python3 scripts/wiki_fts.py search "query text" --limit 10
python3 scripts/wiki_fts.py stats
```

See [skill/references/workflows/bm25.md](./skill/references/workflows/bm25.md) for the full workflow and data model rules.

## Install Notes

Use the plural CLI:

```bash
npx skills add nanzhipro/Karpathy-llm-wiki-bootstrap-skill@llm-wiki-bootstrap
```

For non-interactive user-level install:

```bash
npx skills add nanzhipro/Karpathy-llm-wiki-bootstrap-skill@llm-wiki-bootstrap -g -y
```

To update an existing install:

```bash
npx skills update llm-wiki-bootstrap
```

Do not use `npx skill ...`; that is a different CLI.

## Documentation

| Topic | Link |
| --- | --- |
| Full walkthrough | [Reading Is Not Enough](./from-article-to-llm-wiki.article.en.md) |
| Chinese walkthrough | [不是读完就算](./from-article-to-llm-wiki.article.zh-CN.md) |
| Skill entry point | [skill/SKILL.md](./skill/SKILL.md) |
| Bootstrap workflow | [skill/references/workflows/bootstrap.md](./skill/references/workflows/bootstrap.md) |
| Ingest workflow | [skill/references/workflows/ingest.md](./skill/references/workflows/ingest.md) |
| Query workflow | [skill/references/workflows/query.md](./skill/references/workflows/query.md) |
| Lint workflow | [skill/references/workflows/lint.md](./skill/references/workflows/lint.md) |
| BM25 workflow | [skill/references/workflows/bm25.md](./skill/references/workflows/bm25.md) |
| Preferences schema | [skill/references/config/extend-schema.md](./skill/references/config/extend-schema.md) |

## Origin

The repository is grounded in Karpathy's original LLM Wiki note:

- Original gist: <https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f>
- Local copy: [karpathy-llm-wiki-original.md](./karpathy-llm-wiki-original.md)

This project packages that idea into an installable skill and demonstrates it with a living reference wiki.
