---
title: Why LLM Wikis Work
type: synthesis
created: 2026-05-06
updated: 2026-05-06
sources: [karpathy-llm-wiki-original.md]
tags: [synthesis, maintenance, knowledge-base]
---

The source's central argument is that knowledge bases fail because maintenance is tedious, not because humans dislike structured knowledge. Updating cross-references, summaries, contradictions, indexes, and logs is work that becomes more expensive as a wiki grows.

LLMs change that maintenance equation. They can touch many Markdown files in one pass, keep structure consistent, and perform recurring bookkeeping without boredom. The wiki becomes practical because the human can focus on source selection, review, and questions.

## Mechanism

1. Raw documents remain stable.
2. The LLM compiles durable summaries and concept pages.
3. Each ingest improves the maintained knowledge layer.
4. Useful query answers can become permanent artifacts.
5. Linting catches drift, missing links, stale claims, and gaps.

## Limits

The pattern still depends on human judgment. The LLM should maintain and synthesize, but the human decides what sources matter and whether the emerging interpretation is useful.

## Related Pages

- [[llm-wiki]]
- [[llm-owned-wiki-maintenance]]
- [[persistent-compounding-artifact]]
