# CI/CD Pipelines

All YAML pipeline definitions live here.

## Principles

- independent CI for SalviaClients and IngredientsCatalog;
- build once, deploy many for client deployments;
- no branch per client;
- explicit production DB migration step;
- IngredientsCatalog release/deployment independent from SalviaClients.
