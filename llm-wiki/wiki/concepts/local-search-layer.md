---
title: Local Search Layer
type: concept
created: 2026-05-06
updated: 2026-05-06
sources: [karpathy-llm-wiki-original.md]
tags: [search, bm25, navigation]
---

A **local search layer** is optional tooling that helps the LLM locate relevant wiki pages as the corpus grows.

## Role in the Source

The source names [[qmd|qmd]] as a possible local Markdown search engine and suggests that users may eventually want CLI tools to help the LLM operate more efficiently. It also says a small wiki may not need search beyond the index.

## BM25 in This Wiki

This generated wiki includes `scripts/wiki_fts.py`, `indexes/README.md`, and a rebuildable SQLite FTS5 database. BM25 is a navigation layer only. The LLM must open returned wiki pages before answering.

## Related Pages

- [[index-and-log-navigation]]
- [Index Navigation vs Search Layer](../comparisons/index-navigation-vs-search-layer.md)
- [[rag]]
