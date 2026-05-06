---
title: Concept Table
type: concept-table
created: 2026-05-06
updated: 2026-05-06
sources: [llm-wiki-pattern.md, Karpathy x.md]
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
| Capability discourse | [[agentic-models]], [[ai-capability-perception-gap]], [[peaky-capabilities]], [[verifiable-rewards]] | Public disagreement about AI capability is shaped by product tier, domain, reward signal, and access differences. |
| Wiki architecture | [[llm-wiki]], [[source-of-truth-separation]], [[index-and-log-navigation]], [[wiki-operations-loop]], [[human-ai-maintenance-split]] | A durable markdown knowledge base works when raw evidence, derived synthesis, navigation, and maintenance loops stay separate but coordinated. |
| Retrieval baseline | [[rag]], [[rag-vs-llm-wiki]] | RAG remains the contrast case: useful for query-time retrieval, weaker as a durable synthesis and maintenance layer. |

## Concepts

| Concept | Working definition | Role in this wiki | Sources | Related pages | Status | Maintenance note |
| --- | --- | --- | --- | --- | --- | --- |
| [Agentic Models](concepts/agentic-models.md) | Frontier systems that can work through extended technical tasks with tools and some autonomy. | Anchors the capability side of the wiki and explains why technical users see steeper progress. | Karpathy x.md | [[openai-codex]], [[claude-code]], [[ai-capability-perception-gap]], [[peaky-capabilities]] | high confidence, single-source | Needs more sources before making architecture or benchmark claims. |
| [AI Capability Perception Gap](concepts/ai-capability-perception-gap.md) | Divergent beliefs about AI capability caused by sampling different products, access tiers, recency, and domains. | Central discourse lens connecting product experience to public disagreement. | Karpathy x.md | [[consumer-ai-vs-frontier-agentic-models]], [[peaky-capabilities]], [[agentic-models]], [[why-ai-discourse-fragments]] | high confidence, single-source | Add counterexamples or corroborating sources when available. |
| [Human-AI Maintenance Split](concepts/human-ai-maintenance-split.md) | Division of labor where humans curate direction and sources while the LLM performs wiki maintenance work. | Explains how the wiki remains sustainable as the corpus grows. | llm-wiki-pattern.md | [[llm-wiki]], [[wiki-operations-loop]], [[why-llm-wikis-work]] | high confidence, single-source | Track which maintenance tasks require human review in higher-stakes domains. |
| [Index and Log Navigation](concepts/index-and-log-navigation.md) | Lightweight navigation model using `index.md` for content discovery and `log.md` for chronological memory. | Defines the baseline navigation layer before optional search tooling. | llm-wiki-pattern.md | [[llm-wiki]], [[wiki-operations-loop]], [[rag]] | high confidence, single-source | Revisit when the wiki grows enough that BM25 or other search becomes necessary. |
| [LLM Wiki](concepts/llm-wiki.md) | Persistent, interlinked markdown knowledge base maintained by an LLM as a durable synthesis artifact. | The root architecture concept for the whole repository. | llm-wiki-pattern.md | [[source-of-truth-separation]], [[wiki-operations-loop]], [[human-ai-maintenance-split]], [[rag-vs-llm-wiki]] | high confidence, single-source | Keep this row aligned with any future schema or workflow changes. |
| [Peaky Capabilities](concepts/peaky-capabilities.md) | Uneven AI progress where dramatic gains cluster in technical domains instead of spreading uniformly. | Explains why single headlines about AI capability mislead. | Karpathy x.md | [[ai-capability-perception-gap]], [[verifiable-rewards]], [[agentic-models]] | high confidence, single-source | Needs additional sources to separate training-signal effects from commercial prioritization. |
| [RAG](concepts/rag.md) | Query-time retrieval pattern that finds relevant chunks and generates answers without necessarily preserving durable synthesis. | Baseline comparison for the LLM Wiki pattern. | llm-wiki-pattern.md | [[llm-wiki]], [[rag-vs-llm-wiki]], [[index-and-log-navigation]] | high confidence, single-source | Expand only when the wiki ingests broader RAG architecture sources. |
| [Source-of-Truth Separation](concepts/source-of-truth-separation.md) | Strict split between immutable raw evidence and mutable LLM-maintained derived knowledge. | Core architectural discipline that preserves provenance while allowing synthesis to evolve. | llm-wiki-pattern.md | [[llm-wiki]], [[why-llm-wikis-work]] | high confidence, single-source | Keep aligned with rules for `raw/`, `wiki/`, and generated artifacts. |
| [Verifiable Rewards](concepts/verifiable-rewards.md) | Explanation that domains with checkable rewards, such as programming tests, improve faster under reinforcement learning. | Training-side explanation for uneven technical gains. | Karpathy x.md | [[peaky-capabilities]], [[ai-capability-perception-gap]], [[agentic-models]] | high confidence, single-source | Needs broader RL/evaluation sources before becoming a general training claim. |
| [Wiki Operations Loop](concepts/wiki-operations-loop.md) | Operational cycle of ingesting sources, answering queries, filing valuable outputs, and linting for health. | Converts the wiki from a static repository into a living maintenance system. | llm-wiki-pattern.md | [[llm-wiki]], [[index-and-log-navigation]], [[human-ai-maintenance-split]] | high confidence, single-source | Keep this row current as query filing, BM25, and lint behavior evolve. |
