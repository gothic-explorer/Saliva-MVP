# Clean Architecture

Each backend has four projects:

```text
Domain
Application
Infrastructure
Api
```

Dependency rules:

```text
Application -> Domain
Infrastructure -> Application
Infrastructure -> Domain
Api -> Application
Api -> Infrastructure (composition only)
```

Forbidden:

```text
Domain -> Application
Domain -> Infrastructure
Domain -> Api
Application -> Infrastructure
Application -> Api
```

There is no BuildingBlocks project.
