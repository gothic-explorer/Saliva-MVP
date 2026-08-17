# SalviaClients

Backend application deployed per client.

## Clean Architecture

```text
SalviaClients.Domain
SalviaClients.Application
SalviaClients.Infrastructure
SalviaClients.Api
```

## Dependencies

```text
SalviaClients.Api
      |
      v
SalviaClients.Application
      |
      v
SalviaClients.Domain

SalviaClients.Infrastructure
      +----> SalviaClients.Application
      +----> SalviaClients.Domain
```

All Salvia business entities live in `SalviaClients.Domain`.
