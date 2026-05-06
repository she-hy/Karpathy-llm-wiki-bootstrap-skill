---
title: Wiki Operations Loop
type: concept
created: 2026-05-06
updated: 2026-05-06
sources: [karpathy-llm-wiki-original.md]
tags: [operations, ingest, query, lint]
---

The **wiki operations loop** is the recurring set of actions that keeps an LLM Wiki useful: ingest, query, and lint.

## Ingest

The LLM reads a source, writes a source summary, updates relevant entity and concept pages, revises navigation files, and appends to the log.

## Query

The LLM searches or navigates the wiki, reads relevant pages, answers with citations, and can file valuable answers back into the wiki as durable artifacts.

## Lint

The LLM periodically checks for contradictions, stale claims, orphan pages, missing cross-references, and knowledge gaps.

## Related Pages

- [[filed-query-artifacts]]
- [[human-curation-loop]]
- [[index-and-log-navigation]]
