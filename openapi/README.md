# OpenAPI specs

Store one OpenAPI 3.0 or 3.1 document per API in this folder.

Recommended pattern:

- `openapi/public-api.yaml`
- `openapi/admin-api.yaml`
- `openapi/billing-api.yaml`
- `openapi/webhooks-api.yaml`

Validate each spec before wiring it into navigation:

```bash
mint openapi-check openapi/public-api.yaml
```

Add one navigation group per API in `docs.json`:

```json
{
  "group": "Public API",
  "openapi": {
    "source": "openapi/public-api.yaml",
    "directory": "api-reference/public-api"
  }
}
```

Example for multiple APIs:

```json
{
  "tab": "API reference",
  "groups": [
    {
      "group": "Overview",
      "pages": ["api-reference/introduction"]
    },
    {
      "group": "Public API",
      "openapi": {
        "source": "openapi/public-api.yaml",
        "directory": "api-reference/public-api"
      }
    },
    {
      "group": "Admin API",
      "openapi": {
        "source": "openapi/admin-api.yaml",
        "directory": "api-reference/admin-api"
      }
    }
  ]
}
```
