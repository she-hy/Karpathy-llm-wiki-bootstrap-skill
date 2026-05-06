---
title: How to Operationalize an LLM Wiki
type: synthesis
created: 2026-05-06
updated: 2026-05-06
sources: [karpathy-llm-wiki-original.md]
tags: [workflow, implementation, synthesis]
---

The source is intentionally abstract, but it implies a concrete operating pattern for building a wiki with an LLM agent.

## Minimal Setup

1. Create a `raw/` directory for immutable sources.
2. Create a `wiki/` directory for maintained pages.
3. Add `SCHEMA.md` or a runtime-specific instruction file that defines page formats and workflows.
4. Maintain `wiki/index.md` and `wiki/log.md` from the beginning.
5. Add optional search only when navigation pressure appears.

## Operating Rhythm

- Ingest sources one at a time when review quality matters.
- Batch ingest when speed matters and sources are homogeneous.
- Ask questions against the wiki rather than only against raw documents.
- File useful comparisons and analyses as pages.
- Periodically lint for contradictions, stale pages, orphan pages, missing cross-references, and gaps.

## Role Split

The human curates and steers. The LLM maintains and files. This role split is the practical core of the pattern.

## Related Pages

- [[human-curation-loop]]
- [[llm-owned-wiki-maintenance]]
- [[wiki-operations-loop]]
