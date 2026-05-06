---
title: qmd
type: entity
created: 2026-05-06
updated: 2026-05-06
sources: [karpathy-llm-wiki-original.md]
tags: [search, markdown, cli]
---

**qmd** is mentioned as a local search engine for Markdown files with hybrid BM25/vector search and LLM re-ranking.

## Role in the Source

The source presents qmd as an optional CLI or MCP tool that can help the LLM operate on a larger wiki. It is an example, not a requirement.

## Relationship to This Wiki

This generated wiki uses its own local BM25 script instead of qmd. The role is similar: search helps locate candidate wiki pages, but it does not become the evidence layer.

## Related Pages

- [[local-search-layer]]
- [Index Navigation vs Search Layer](../comparisons/index-navigation-vs-search-layer.md)
