# Domain Organization

## SalviaClients

All entities belong to:

`src/backend/SalviaClients/SalviaClients.Domain`

They may be grouped by business area inside the same project:

```text
SalviaClients.Domain/
├── Identity/
├── Ingredients/
├── Recipes/
└── Common/
```

## IngredientsCatalog

All canonical catalog entities belong to:

`src/backend/IngredientsCatalog/IngredientsCatalog.Domain`

Do not create additional Domain projects.
