# elasticsearch

Minimal package with core Elasticsearch and Kibana REST API guidance.

## Install

```bash
npm install elasticsearch-skill
```

Or install locally:

```bash
cd elasticsearch
npm pack
npm install ./elasticsearch-skill-1.0.0.tgz
```

## Use

Provides concise examples for:

- auth and request patterns
- basic search (Query DSL)
- aggregations and date histograms
- index/mapping operations and bulk
- lightweight Kibana API pointers

## Package layout

- `SKILL.md` - when to use and core rules
- `references/` - short examples and tips

## Publish

1. Bump `version` in `package.json`.
2. Run `npm pack` and verify contents.
3. Publish with `npm publish`.

## Thanks

Consolidated from local Elasticsearch skill guidance.
