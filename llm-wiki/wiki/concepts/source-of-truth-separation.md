---
title: Source-of-Truth Separation
type: concept
created: 2026-05-06
updated: 2026-05-06
sources: [karpathy-llm-wiki-original.md]
tags: [architecture, sources, evidence]
---

**Source-of-truth separation** is the rule that raw sources and derived wiki pages have different responsibilities.

## Raw Layer

The raw layer contains source documents such as articles, papers, books, images, data files, meeting notes, or journals. It is the evidence layer and should not be rewritten by the agent after ingest.

## Wiki Layer

The wiki layer contains summaries, entities, concepts, comparisons, synthesis, index, and log. It is editable because the LLM maintains it as understanding improves.

## Why It Matters

This separation lets the wiki evolve while preserving the original claims. It also gives future maintainers a clear way to verify derived pages against their evidence.

## Related Pages

- [[llm-wiki]]
- [[schema-as-operating-contract]]
- [[persistent-compounding-artifact]]
