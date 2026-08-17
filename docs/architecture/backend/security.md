# Security

## Authentication

- OIDC / OAuth 2.0 compatible identity provider
- JWT Bearer validation

## Authorization

- ASP.NET Core policy-based authorization
- explicit permissions

Convention:

```text
<resource>.<action>
```

Examples:

```text
ingredient.read
ingredient.create
ingredient.update
ingredient.delete
```

Concrete identity provider remains TBD.
