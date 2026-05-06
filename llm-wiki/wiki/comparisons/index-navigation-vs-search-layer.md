---
title: Index Navigation vs Search Layer
type: comparison
created: 2026-05-06
updated: 2026-05-06
sources: [karpathy-llm-wiki-original.md]
tags: [index, search, bm25, comparison]
---

| Dimension | Index and Log Navigation | Local Search Layer |
| --- | --- | --- |
| Primary file/tool | `wiki/index.md` and `wiki/log.md` | `scripts/wiki_fts.py`, qmd, or another search tool |
| Best scale | Small to moderate wiki | Larger wiki or focused lookup needs |
| Output | Curated page catalog and operation history | Candidate chunks or matching pages |
| Trust level | Maintained wiki navigation | Navigation helper only |
| Normal use | Start every query by reading the index | Search after index review to improve recall |
| Citation target | Wiki pages | Wiki pages after opening search results |

## Interpretation

The source treats the index and log as the default navigation layer and local search as optional tooling. This generated wiki enables BM25 by default, but the same rule holds: search finds candidate pages; maintained wiki pages provide context and citations.

## Related Pages

- [[index-and-log-navigation]]
- [[local-search-layer]]
- [[schema-as-operating-contract]]
