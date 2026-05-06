---
title: RAG vs LLM Wiki
type: comparison
created: 2026-05-06
updated: 2026-05-06
sources: [karpathy-llm-wiki-original.md]
tags: [rag, llm-wiki, comparison]
---

| Dimension | RAG | LLM Wiki |
| --- | --- | --- |
| Main action | Retrieve raw chunks at query time | Compile source knowledge into persistent pages |
| Memory shape | Mostly implicit in indexed source documents | Explicit in maintained Markdown pages |
| Synthesis | Rebuilt repeatedly for each question | Accumulates across ingests and queries |
| Contradictions | Must be rediscovered or re-reasoned | Can be flagged and tracked in pages |
| Human role | Upload documents and ask questions | Curate sources, guide emphasis, review meaning |
| LLM role | Retrieve and answer | Ingest, summarize, cross-reference, lint, and answer |
| Best fit | Direct Q&A over a collection | Long-running knowledge accumulation |

## Interpretation

The source does not reject [[rag|RAG]]. It argues that RAG alone does not accumulate durable synthesis. An [[llm-wiki|LLM Wiki]] can still use retrieval tools, including local search, but those tools serve navigation rather than replacing the maintained wiki layer.

## Related Pages

- [[persistent-compounding-artifact]]
- [[source-of-truth-separation]]
- [[local-search-layer]]
