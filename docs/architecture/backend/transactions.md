# Transactions

Use local PostgreSQL transactions.

Keep them short.

Do not call remote services while holding DB transactions.

No distributed transaction between SalviaClients and IngredientsCatalog.
