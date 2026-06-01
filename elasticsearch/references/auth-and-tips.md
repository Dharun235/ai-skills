## Auth & Tip Summary

- Export the cluster URL and API key in your session:

```bash
ES_URL="https://your-cluster.es.cloud.elastic.co:443"
ES_API_KEY="base64-id:api_key"
```

- Use this header pattern in `curl`:

```bash
curl -s "${ES_URL%/}/_cat/indices?v" \
  -H "Authorization: ApiKey $(printenv ES_API_KEY)" \
  -H "Content-Type: application/json"
```

- Tips:
  - Use `${ES_URL%/}` to avoid double slashes.
  - Use `$(printenv ES_API_KEY)` in headers to avoid empty auth.
  - Prefer `jq` for formatting responses.
  - Serverless clusters may not support cluster-level APIs (`_cluster/*`, `_nodes/*`, ILM).
