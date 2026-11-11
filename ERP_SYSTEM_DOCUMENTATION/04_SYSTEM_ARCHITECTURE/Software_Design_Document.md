# ERP SYSTEM Software Design Document

## Design style

The implementation is a modular monolith with an extensible addon/plugin model. Addons contribute Python models/controllers, XML data/views/templates, browser assets, security declarations, tests, and manifest metadata. A shared registry and PostgreSQL database support the selected module graph.

## Core design components

1. **CLI and service runtime** — starts/configures the server and worker modes.
2. **HTTP layer** — routes requests, creates request/session context, dispatches controllers, and returns HTTP/JSON responses.
3. **Module graph/loader** — reads manifests, orders dependencies, loads data, and coordinates updates/migrations.
4. **ORM/registry** — resolves model inheritance, fields, computed dependencies, constraints, access checks, cache, and database transactions.
5. **Addon layer** — implements domain and integration behavior without requiring separate deployable services.
6. **Client/view layer** — delivers JavaScript/TypeScript assets and XML-defined backend/website views.
7. **Operational services** — scheduled actions, bus/messaging, mail, reporting, logging, and optional integrations.

## Design constraints

- The effective schema and UI depend on the installed addon graph.
- Model inheritance and XML view inheritance make isolated file-level behavior incomplete without registry resolution.
- External integrations are optional and configuration-dependent.
- Deployment topology, database contents, and secrets are not defined by this source snapshot.

## Design evidence

`odoo/modules/`, `odoo/orm/`, `odoo/http/`, `odoo/service/`, `odoo/sql_db.py`, `setup.py`, and the per-addon evidence pages.

