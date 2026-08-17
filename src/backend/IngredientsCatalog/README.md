# IngredientsCatalog

Central microservice and single source of truth for canonical/base ingredients.

## Clean Architecture

```text
IngredientsCatalog.Domain
IngredientsCatalog.Application
IngredientsCatalog.Infrastructure
IngredientsCatalog.Api
```

Own PostgreSQL database.

SalviaClients consumes it through REST/OpenAPI.
