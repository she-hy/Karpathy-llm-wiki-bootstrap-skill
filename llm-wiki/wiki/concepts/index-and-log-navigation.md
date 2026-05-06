---
title: Index and Log Navigation
type: concept
created: 2026-05-06
updated: 2026-05-06
sources: [karpathy-llm-wiki-original.md]
tags: [navigation, index, log]
---

`index.md` and `log.md` are the source's minimum navigation structure for an LLM Wiki.

## `index.md`

`index.md` is content-oriented. It lists wiki pages by category with links and metadata so the LLM can start a query from the maintained catalog instead of scanning every file.

## `log.md`

`log.md` is chronological. It records ingests, queries, lint passes, and other operations with parseable headings, giving both the human and the LLM a history of recent changes.

## Why It Matters

The source argues that this structure works surprisingly well at moderate scale, delaying the need for heavier retrieval infrastructure.

## Related Pages

- [[local-search-layer]]
- [[wiki-operations-loop]]
- [[schema-as-operating-contract]]
