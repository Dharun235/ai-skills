## Query DSL — concise examples

Match query:

```bash
curl -s "${ES_URL%/}/my-index/_search" \
  -H "Authorization: ApiKey $(printenv ES_API_KEY)" \
  -H "Content-Type: application/json" \
  -d '{"query":{"match":{"message":"error"}},"size":10}' | jq .
```

Bool query (must + filter + must_not):

```bash
curl -s "${ES_URL%/}/my-index/_search" \
  -H "Authorization: ApiKey $(printenv ES_API_KEY)" \
  -H "Content-Type: application/json" \
  -d '{"query":{"bool":{"must":[{"match":{"message":"error"}}],"filter":[{"range":{"@timestamp":{"gte":"now-1h"}}}],"must_not":[{"term":{"level":"debug"}}]}},"size":20}' | jq .
```

Sorting and pagination tips: use `size`, `sort`, and prefer `search_after` or PIT for large result sets.
