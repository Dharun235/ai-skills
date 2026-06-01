## Index & Document — create, mappings, bulk

Create index with mappings:

```bash
curl -s -X PUT "${ES_URL%/}/my-index" \
  -H "Authorization: ApiKey $(printenv ES_API_KEY)" \
  -H "Content-Type: application/json" \
  -d '{"settings":{"number_of_shards":1},"mappings":{"properties":{"message":{"type":"text"},"@timestamp":{"type":"date"}}}}'
```

Index a document (auto ID):

```bash
curl -s -X POST "${ES_URL%/}/my-index/_doc" \
  -H "Authorization: ApiKey $(printenv ES_API_KEY)" \
  -H "Content-Type: application/json" \
  -d '{"message":"hello","@timestamp":"2026-01-31T12:00:00Z"}' | jq .
```

Bulk NDJSON example (use `--data-binary @-`):

```bash
curl -s -X POST "${ES_URL%/}/_bulk" \
  -H "Authorization: ApiKey $(printenv ES_API_KEY)" \
  -H "Content-Type: application/x-ndjson" \
  --data-binary @- << 'EOF'
{"index":{"_index":"my-index"}}
{"message":"bulk 1","@timestamp":"2026-01-31T12:00:00Z"}
EOF
```

Reindex (rename/transform): use `_reindex` with `source` and `dest`.
