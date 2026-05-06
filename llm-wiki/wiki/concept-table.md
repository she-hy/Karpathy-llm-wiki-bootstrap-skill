---
title: Concept Table
type: concept-table
created: 2026-05-06
updated: 2026-05-06
sources: [karpathy-llm-wiki-original.md]
tags: [concept-map, navigation, maintenance]
---

> This table is the wiki's compressed concept map. It complements `wiki/index.md`: the index catalogs pages; this table explains what the durable concepts mean, how they relate, and what needs maintenance.

## Maintenance Rules

- Keep one row for every durable concept page under `wiki/concepts/`.
- Update this table whenever a concept page is created, renamed, deleted, merged, split, or materially revised.
- Keep rows sorted alphabetically by concept name.
- Keep definitions concise and evidence-aware; link to the full concept page for detail.
- Use `Status` values such as `high confidence`, `single-source`, `tentative`, `needs sources`, or `contradicted`.
- Column headers stay English as protocol identifiers; row content follows the language of the relevant concept page.

## Concept Clusters

| Cluster | Concepts | Current interpretation |
| --- | --- | --- |
| Architecture | [LLM Wiki](concepts/llm-wiki.md), [Source-of-Truth Separation](concepts/source-of-truth-separation.md), [Schema as Operating Contract](concepts/schema-as-operating-contract.md) | The pattern separates evidence, compiled knowledge, and agent operating rules. |
| Maintenance | [LLM-Owned Wiki Maintenance](concepts/llm-owned-wiki-maintenance.md), [Wiki Operations Loop](concepts/wiki-operations-loop.md), [Human Curation Loop](concepts/human-curation-loop.md) | Humans direct and review; the LLM does the recurring bookkeeping. |
| Navigation | [Index and Log Navigation](concepts/index-and-log-navigation.md), [Local Search Layer](concepts/local-search-layer.md), [Filed Query Artifacts](concepts/filed-query-artifacts.md) | The wiki becomes useful when findings can be located, cited, and preserved. |
| Retrieval contrast | [RAG](concepts/rag.md), [Persistent Compounding Artifact](concepts/persistent-compounding-artifact.md) | RAG retrieves from raw sources repeatedly; an LLM Wiki accumulates compiled structure. |

## Concepts

| Concept | Working definition | Role in this wiki | Sources | Related pages | Status | Maintenance note |
| --- | --- | --- | --- | --- | --- | --- |
| [Filed Query Artifacts](concepts/filed-query-artifacts.md) | Useful answers produced during query can be saved as durable wiki pages. | Shows how exploration compounds after the initial ingest. | karpathy-llm-wiki-original.md | [Wiki Operations Loop](concepts/wiki-operations-loop.md), [Persistent Compounding Artifact](concepts/persistent-compounding-artifact.md) | single-source | Watch future examples for when filing is worth the overhead. |
| [Human Curation Loop](concepts/human-curation-loop.md) | The human supplies sources, asks questions, guides emphasis, and checks meaning while the LLM performs maintenance. | Defines the human side of the workflow. | karpathy-llm-wiki-original.md | [LLM-Owned Wiki Maintenance](concepts/llm-owned-wiki-maintenance.md), [Wiki Operations Loop](concepts/wiki-operations-loop.md) | single-source | Add concrete review patterns when available. |
| [Index and Log Navigation](concepts/index-and-log-navigation.md) | `index.md` catalogs content while `log.md` records chronological operations. | Describes the minimum navigation layer before specialized search. | karpathy-llm-wiki-original.md | [Local Search Layer](concepts/local-search-layer.md), [Schema as Operating Contract](concepts/schema-as-operating-contract.md) | single-source | Track when index scale limits appear. |
| [LLM-Owned Wiki Maintenance](concepts/llm-owned-wiki-maintenance.md) | The LLM owns the derived wiki layer and performs cross-reference, summary, and consistency work. | Captures the labor shift that makes the pattern practical. | karpathy-llm-wiki-original.md | [Human Curation Loop](concepts/human-curation-loop.md), [Why LLM Wikis Work](synthesis/why-llm-wikis-work.md) | single-source | Future sources should test where agent maintenance needs human review. |
| [LLM Wiki](concepts/llm-wiki.md) | A persistent, LLM-maintained Markdown knowledge base compiled from immutable raw sources. | The central concept that all pages elaborate. | karpathy-llm-wiki-original.md | [RAG](concepts/rag.md), [Source-of-Truth Separation](concepts/source-of-truth-separation.md), [Schema as Operating Contract](concepts/schema-as-operating-contract.md) | single-source | Future sources should clarify concrete implementations. |
| [Local Search Layer](concepts/local-search-layer.md) | Optional local search over wiki pages used as navigation, not as truth. | Connects the source's optional CLI search idea with this generated BM25 layer. | karpathy-llm-wiki-original.md | [Index and Log Navigation](concepts/index-and-log-navigation.md), [RAG](concepts/rag.md) | single-source | Distinguish BM25, qmd, and vector search if more tooling sources are added. |
| [Persistent Compounding Artifact](concepts/persistent-compounding-artifact.md) | The wiki accumulates cross-references, contradictions, and synthesis over time. | Explains the compounding benefit over repeated retrieval. | karpathy-llm-wiki-original.md | [Filed Query Artifacts](concepts/filed-query-artifacts.md), [LLM Wiki](concepts/llm-wiki.md) | single-source | Add empirical examples if available. |
| [RAG](concepts/rag.md) | Retrieval-augmented generation that retrieves raw document chunks at query time. | The main contrast class for the LLM Wiki pattern. | karpathy-llm-wiki-original.md | [LLM Wiki](concepts/llm-wiki.md), [RAG vs LLM Wiki](comparisons/rag-vs-llm-wiki.md) | single-source | Keep definition limited to the source's framing until more sources are ingested. |
| [Schema as Operating Contract](concepts/schema-as-operating-contract.md) | A schema file tells the agent how the wiki is structured and how to operate it. | Explains why repeatable agent behavior requires explicit conventions. | karpathy-llm-wiki-original.md | [Source-of-Truth Separation](concepts/source-of-truth-separation.md), [Wiki Operations Loop](concepts/wiki-operations-loop.md) | single-source | Track differences among AGENTS.md, CLAUDE.md, and SCHEMA.md patterns. |
| [Source-of-Truth Separation](concepts/source-of-truth-separation.md) | Raw sources stay immutable while the wiki contains editable derived knowledge. | Defines the evidence boundary for the whole wiki. | karpathy-llm-wiki-original.md | [LLM Wiki](concepts/llm-wiki.md), [Persistent Compounding Artifact](concepts/persistent-compounding-artifact.md) | single-source | Watch for cases where derived pages need stronger source citation rules. |
| [Wiki Operations Loop](concepts/wiki-operations-loop.md) | Ingest, query, and lint are the recurring operations that keep the wiki useful. | Provides the operational model for maintaining the knowledge base. | karpathy-llm-wiki-original.md | [Filed Query Artifacts](concepts/filed-query-artifacts.md), [Index and Log Navigation](concepts/index-and-log-navigation.md) | single-source | Future workflow docs can refine each operation. |
