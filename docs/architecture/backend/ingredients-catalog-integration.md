# IngredientsCatalog Integration

```text
SalviaClients.Application
      |
      v
IIngredientsCatalogClient
      ^
      |
SalviaClients.Infrastructure
      |
      v
IngredientsCatalog REST API
```

Rules:

- no direct DB access;
- HTTP/OpenAPI only;
- canonical data central;
- client-specific data local;
- link via `CatalogIngredientId`.
