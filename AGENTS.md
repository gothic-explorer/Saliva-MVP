# SALVIA Agent Instructions

## General

- Read `/docs/features` and `/docs/architecture` before implementation.
- Do not invent business rules.
- Do not silently change accepted architecture decisions.
- Major technical changes require an ADR under `/docs/architecture/adr`.

## Frontend

Frontend technology is still TBD.

Do not initialize Angular, React, Vue, Next.js or another framework until explicitly selected.

## SalviaClients Backend

Use:

- .NET 10 / ASP.NET Core 10
- Clean Architecture
- Entity Framework Core 10
- PostgreSQL / Npgsql
- REST + OpenAPI 3.1
- JWT Bearer authentication
- policy-based authorization
- explicit permissions
- EF Core Migrations
- Microsoft.Extensions.Http.Resilience
- HybridCache
- Microsoft.Extensions.Logging
- OpenTelemetry
- xUnit
- ArchUnitNET

## Clean Architecture

Dependency direction:

```text
Api -> Application
Api -> Infrastructure (composition/wiring only)

Infrastructure -> Application
Infrastructure -> Domain

Application -> Domain

Domain -> nothing
```

Forbidden:

```text
Domain -> EF Core
Domain -> ASP.NET Core
Domain -> Infrastructure
Application -> Infrastructure
Application -> EF Core
```

## Domain Rule

There is one Domain project per backend.

All entities for SalviaClients belong in:

`src/backend/SalviaClients/SalviaClients.Domain`

All canonical catalog entities belong in:

`src/backend/IngredientsCatalog/IngredientsCatalog.Domain`

Do not create extra Domain or BuildingBlocks projects.

## IngredientsCatalog

- separate central microservice;
- own PostgreSQL database;
- single source of truth for canonical/base ingredients;
- no client direct database access.

## Data Ownership

IngredientsCatalog owns canonical ingredient data.

SalviaClients owns client-specific data:

- supplier;
- purchase price;
- packaging;
- usable quantity;
- yield;
- notes.

Link local data with `CatalogIngredientId`.

## CI/CD

All YAML pipelines live under `/Pipelines`.

- build once, deploy many;
- no branch per client;
- separate IngredientsCatalog release cycle;
- explicit DB migration step in production deployments.
