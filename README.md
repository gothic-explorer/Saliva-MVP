# SALVIA

Monorepo structure for Salvia.

## Main Structure

```text
SALVIA/
├── src/
│   ├── frontend/
│   └── backend/
│       ├── SalviaClients/
│       ├── SalviaClients.UnitTests/
│       ├── IngredientsCatalog/
│       └── IngredientsCatalog.UnitTests/
├── Pipelines/
└── docs/
    ├── features/
    └── architecture/
```

## Backend Architecture

Both backends use a simple Clean Architecture:

```text
Domain
Application
Infrastructure
Api
```

No business/application code is implemented yet.
