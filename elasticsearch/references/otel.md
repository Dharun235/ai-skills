## OpenTelemetry & OTEL data

Use ES|QL or Query DSL to query OTEL logs/traces stored in Elasticsearch. ES|QL example:

```bash
curl -s -X POST "${ES_URL%/}/_query" \
  -H "Authorization: ApiKey $(printenv ES_API_KEY)" \
  -H "Content-Type: application/json" \
  -d '{"query":"FROM traces-* | WHERE status.code == \"ERROR\" | STATS count = COUNT(*) BY service.name | LIMIT 10"}' | jq .
```

Check OTEL index names (`traces-*`, `logs-*`, `metrics-*`) and mappings before querying.
