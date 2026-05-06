---
title: Overview
type: overview
created: 2026-05-06
updated: 2026-05-06
sources: [karpathy-llm-wiki-original.md]
tags: [llm-wiki, knowledge-base, agents, markdown]
---

This wiki compiles a single source, [LLM Wiki](sources/karpathy-llm-wiki-original.md), into a maintained map of the LLM Wiki pattern. The source argues for a knowledge-base architecture in which an LLM agent incrementally reads raw material, writes and updates Markdown pages, maintains cross-references, and files useful analyses back into the wiki.

## Current Thesis

An [[llm-wiki|LLM Wiki]] differs from [[rag|RAG]] because it turns repeated retrieval work into durable structure. The source frames raw documents as the immutable evidence layer, wiki pages as the LLM-maintained knowledge layer, and a schema or operating contract as the discipline that makes the agent behave like a maintainer rather than a generic chatbot.

The central claim is that the tedious parts of knowledge-base maintenance - summaries, cross-references, contradiction tracking, filing, indexing, and log updates - are exactly the kind of bookkeeping an LLM agent can perform cheaply. The human remains responsible for source selection, judgment, exploration, and taste.

## Key Themes

- Persistent compilation: knowledge is compiled once into pages and kept current.
- Source separation: raw sources remain stable while wiki pages evolve.
- Agent maintenance: the LLM owns the wiki layer and the user owns direction.
- Navigation scaffolding: `index.md`, `log.md`, wikilinks, and optional local search make the wiki navigable.
- Filing loop: good query answers can become new wiki artifacts instead of disappearing into chat history.

## Open Questions

- When does a small LLM Wiki need local search beyond `index.md` and direct text search?
- Which review rhythm best preserves quality without turning the human back into the wiki maintainer?
- How should future sources distinguish between the abstract pattern and concrete implementations?
