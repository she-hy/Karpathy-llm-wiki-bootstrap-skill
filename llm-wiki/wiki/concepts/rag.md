---
title: RAG
type: concept
created: 2026-05-06
updated: 2026-05-06
sources: [karpathy-llm-wiki-original.md]
tags: [rag, retrieval, baseline]
---

**RAG** in this wiki means a retrieval-augmented generation workflow where documents are searched at query time and the LLM answers from retrieved chunks.

## Role in the Source

The source uses RAG as the main contrast class. RAG is useful for answering against documents, but the critique is that it often rediscovers knowledge from scratch on each question. The source names products such as [[notebooklm|NotebookLM]] and ChatGPT file uploads as examples of this user experience.

## Contrast With LLM Wiki

An [[llm-wiki|LLM Wiki]] stores derived summaries, concept pages, cross-references, and synthesis. It can still use retrieval, but retrieval is a helper for navigation rather than the only memory of the system.

## Related Pages

- [RAG vs LLM Wiki](../comparisons/rag-vs-llm-wiki.md)
- [[persistent-compounding-artifact]]
- [[local-search-layer]]
