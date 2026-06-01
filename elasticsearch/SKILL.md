---
name: elasticsearch
description: >
  Core Elasticsearch and Kibana REST guidance for querying, indexing, aggregations,
  and basic troubleshooting via `curl`. Use when the user asks for Query DSL examples,
  index/mapping changes, aggregations, basic cluster checks, or Kibana saved-object APIs.
---

# Elasticsearch

Use this skill for concise, copy-ready REST examples and operational tips that work across
Elastic Cloud, self-managed, and serverless clusters (with serverless limitations noted).

## Core rules

1. Always require `ES_URL` and `ES_API_KEY` (ApiKey header) from the user.
2. Prefer small, copy-paste `curl` examples that include `jq` for readability.
3. Note serverless limitations (many cluster APIs are unavailable).
4. Point to compact reference examples in `references/` for Query DSL, aggregations, and index ops.

## When to use

- The user asks how to run searches, aggregations, create mappings, or index documents.
- The user wants quick troubleshooting commands (health, nodes, pending tasks).
- The user needs Kibana API endpoints for dashboards or saved objects.

## On-demand references

- `references/auth-and-tips.md` — auth pattern and serverless notes
- `references/query-dsl.md` — short Query DSL examples
- `references/aggregations.md` — top aggregations examples
- `references/index.md` — create index, mappings, bulk, and reindex
- `references/kibana.md` — basic Kibana API examples
