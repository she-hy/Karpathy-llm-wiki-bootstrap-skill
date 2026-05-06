---
title: LLM Wiki
type: concept
created: 2026-05-06
updated: 2026-05-06
sources: [karpathy-llm-wiki-original.md]
tags: [llm-wiki, knowledge-base, markdown]
---

An **LLM Wiki** is a persistent, LLM-maintained Markdown knowledge base compiled from raw sources. The source presents it as a middle layer between immutable documents and user questions: the LLM reads sources once, extracts durable knowledge, and keeps the wiki current as sources and questions accumulate.

## Key Properties

- The wiki is persistent rather than regenerated for each question.
- The LLM owns summaries, cross-references, entity pages, concept pages, comparisons, synthesis, and bookkeeping.
- The human owns source curation, exploration, emphasis, and judgment.
- The schema gives the agent repeatable operating rules.

## Why It Matters

The pattern tries to convert knowledge work from repeated retrieval into accumulated structure. It is especially relevant when subtle questions require connecting many sources, because those connections can already be filed in the wiki.

## Related Pages

- [[source-of-truth-separation]]
- [[persistent-compounding-artifact]]
- [[schema-as-operating-contract]]
- [RAG vs LLM Wiki](../comparisons/rag-vs-llm-wiki.md)
