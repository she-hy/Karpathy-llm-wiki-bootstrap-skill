---
title: Schema as Operating Contract
type: concept
created: 2026-05-06
updated: 2026-05-06
sources: [karpathy-llm-wiki-original.md]
tags: [schema, contract, agent-instructions]
---

**Schema as operating contract** is the idea that a wiki needs an explicit instruction document telling the LLM how the system is structured and what workflows to follow.

## Role in the Source

The source describes a schema document such as `CLAUDE.md` or `AGENTS.md` that defines directory structure, conventions, and workflows. This contract turns the LLM from a generic chatbot into a disciplined wiki maintainer.

## In This Wiki

This generated wiki uses `SCHEMA.md` as the canonical operating contract, with `AGENTS.md` as a thin pointer. BM25 behavior is also documented in `SCHEMA.md` and `indexes/README.md`.

## Related Pages

- [[source-of-truth-separation]]
- [[wiki-operations-loop]]
- [[index-and-log-navigation]]
