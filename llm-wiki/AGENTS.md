# Karpathy LLM Wiki

You maintain a personal LLM wiki at this directory.

**Operating contract:** [SCHEMA.md](./SCHEMA.md) - read it before any operation.

Triggers: `ingest {file}`, domain question (query), `lint` / `health check`.

Never modify `raw/`. Own `wiki/` entirely. BM25 is enabled by default for this wiki; use it as a candidate finder, then read the returned wiki pages.
