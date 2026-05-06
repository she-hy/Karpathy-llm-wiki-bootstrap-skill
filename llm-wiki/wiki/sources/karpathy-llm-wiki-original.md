---
title: LLM Wiki
type: source-summary
created: 2026-05-06
updated: 2026-05-06
sources: [karpathy-llm-wiki-original.md]
tags: [llm-wiki, knowledge-base, agents, markdown]
---

## Summary

The source proposes an [[llm-wiki|LLM Wiki]]: a persistent Markdown knowledge base that an LLM agent builds and maintains from raw source material. Instead of retrieving raw chunks from documents for each question, the agent compiles source knowledge into structured pages, keeps those pages current, and lets later questions start from accumulated synthesis.

The architecture has three layers: immutable raw sources, an editable wiki owned by the LLM, and a schema or operating contract that tells the agent how to ingest, query, lint, and maintain the wiki. The source frames [[obsidian|Obsidian]] as a useful browsing environment and the LLM as the maintainer that performs the repetitive bookkeeping.

The source also emphasizes that useful query answers should not disappear into chat history. Comparisons, analyses, and discovered connections can be filed back into the wiki, making exploration itself part of the compounding knowledge base.

## Key Claims

1. "The wiki is a persistent, compounding artifact." The value comes from accumulated cross-references, flagged contradictions, and synthesis.
2. "The LLM writes and maintains all of it." The human directs sources and questions, while the LLM performs summaries, cross-references, filing, and bookkeeping.
3. `index.md` and `log.md` provide enough navigation for moderate scale before heavier retrieval infrastructure is needed.
4. Optional CLI search can help once the wiki grows, but search is a navigation helper rather than the knowledge layer itself.
5. The pattern works because LLMs reduce the maintenance cost that normally causes human-curated wikis to decay.

## Entities Mentioned

- [[claude-code|Claude Code]]
- [[dataview|Dataview]]
- [[marp|Marp]]
- [[memex|Memex]]
- [[notebooklm|NotebookLM]]
- [[obsidian|Obsidian]]
- [[openai-codex|OpenAI Codex]]
- [[qmd|qmd]]

## Concepts

- [[filed-query-artifacts|Filed Query Artifacts]]
- [[human-curation-loop|Human Curation Loop]]
- [[index-and-log-navigation|Index and Log Navigation]]
- [[llm-owned-wiki-maintenance|LLM-Owned Wiki Maintenance]]
- [[llm-wiki|LLM Wiki]]
- [[local-search-layer|Local Search Layer]]
- [[persistent-compounding-artifact|Persistent Compounding Artifact]]
- [[rag|RAG]]
- [[schema-as-operating-contract|Schema as Operating Contract]]
- [[source-of-truth-separation|Source-of-Truth Separation]]
- [[wiki-operations-loop|Wiki Operations Loop]]

## Notable Quotes

> "The knowledge is compiled once and then kept current, not re-derived on every query."

> "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."

> "The tedious part of maintaining a knowledge base is not the reading or the thinking - it's the bookkeeping."

## Limitations / Bias

This is a single idea file, not an empirical evaluation. It describes a pattern and motivation, but leaves concrete schema design, tooling choices, review loops, and failure modes to be worked out by the user and their agent.
