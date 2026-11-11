# System Architecture

ERP SYSTEM is a modular monolith. A Python server process loads a dependency-ordered set of addons into a shared ORM registry backed by PostgreSQL. HTTP requests enter through the routing/dispatcher stack; browser assets and XML templates form the client surface. Cron/background services, bus/event facilities, mail, reporting, and optional integrations are loaded through addons and configuration.

```mermaid
flowchart LR
  U[Users / Integrations] --> H[HTTP server and router]
  H --> C[Controllers and web client]
  C --> R[ORM registry and business models]
  R --> DB[(PostgreSQL)]
  L[Addon loader and dependency graph] --> R
  J[Cron / background services] --> R
  X[Optional external providers] <--> C
  X <--> J
```

Evidence: `odoo-bin`, `odoo/cli/`, `odoo/service/`, `odoo/http/`, `odoo/orm/`, `odoo/sql_db.py`, `odoo/modules/`, and addon manifests.
