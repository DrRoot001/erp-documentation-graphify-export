# System Scope

## In scope

- Core server bootstrap, CLI, configuration, HTTP dispatch, sessions, ORM, database access, module graph/loading, scheduled actions, reporting, assets, translations, and security primitives.
- Addon modules represented by `__manifest__.py`, including business domains, integrations, localizations, test modules, and web/client modules.
- Static source, manifests, access files, XML data/views, JavaScript/TypeScript, tests, packaging, Debian service/configuration, and setup assets.

## Out of scope or not verifiable from source alone

- A tenant's installed module set, database contents, runtime configuration, secrets, external credentials, production topology, SLA, backup history, and observed performance.
- UI appearance and runtime workflows that depend on browser execution, data, permissions, or installed addons.
- Database tables generated after module installation; Odoo models are declared in Python and materialized into PostgreSQL at runtime.
