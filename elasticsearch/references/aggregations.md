## Aggregations — common patterns

Terms aggregation (top values):

```bash
curl -s "${ES_URL%/}/my-index/_search?size=0" \
  -H "Authorization: ApiKey $(printenv ES_API_KEY)" \
  -H "Content-Type: application/json" \
  -d '{"aggs": {"top_levels": {"terms": {"field": "level", "size": 10}}}}' | jq .aggregations
```

Date histogram with nested metric:

```bash
curl -s "${ES_URL%/}/my-index/_search?size=0" \
  -H "Authorization: ApiKey $(printenv ES_API_KEY)" \
  -H "Content-Type: application/json" \
  -d '{"query":{"range":{"@timestamp":{"gte":"now-24h"}}},"aggs":{"over_time":{"date_histogram":{"field":"@timestamp","fixed_interval":"1h"},"aggs":{"avg_count":{"avg":{"field":"count"}}}}}}' | jq .aggregations
```

Advice: use `?size=0` when only retrieving aggregations to skip hits. Use composite aggregations for high-cardinality faceting.
