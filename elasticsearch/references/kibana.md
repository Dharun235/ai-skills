## Kibana API — quick pointers

- Kibana saved objects (dashboards, visualizations, index patterns) are available via the Kibana API on the Kibana host.

Example: export a saved object (dashboard):

```bash
curl -s "${KIBANA_URL%/}/api/saved_objects/_export" \
  -H "kbn-xsrf: true" \
  -H "Content-Type: application/json" \
  -d '{"type":["dashboard"],"objects":[],"includeReferencesDeep":true}' > export.ndjson
```

Note: Kibana uses `kbn-xsrf` header for non-browser requests and may require a different auth method (API key or session cookie).
