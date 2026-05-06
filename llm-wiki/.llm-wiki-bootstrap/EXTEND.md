# llm-wiki-bootstrap Preferences

Project-specific preferences for this generated wiki. This file makes the user's requested default explicit: BM25 is required for normal wiki operations when the local files are available.

```yaml
bm25:
  mode: required
  prompt_once: true

  thresholds:
    source_count: 1
    wiki_page_count: 1
    wiki_text_chars: 1
    index_lines: 1
    query_read_pages: 1

  strong_thresholds:
    source_count: 1
    wiki_page_count: 1
    wiki_text_chars: 1

  index_paths:
    - wiki

  include_raw: false
  auto_rebuild_after_ingest: true
  fallback_to_rg: true

  chunking:
    max_chars: 1800
    overlap_chars: 200

  export:
    default_format: jsonl
    include_text: true
```

## Notes

- BM25 remains a navigation layer, not a source of truth.
- The LLM must open returned wiki pages before answering.
- `indexes/fts.sqlite` and files under `exports/` are rebuildable and ignored by git.
