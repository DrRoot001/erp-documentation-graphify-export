# System Overview

## Product identity

- Product documentation name: **ERP SYSTEM**.
- Source product: Odoo (`odoo/release.py`, `product_name = 'Odoo'`).
- Version metadata: Odoo 20.0 final (`odoo/release.py:13-16`).
- Primary runtime: Python 3.12 or newer within the declared supported range, PostgreSQL 16 or newer (`odoo/release.py:31-32`).
- Licensing metadata: LGPL-3 (`odoo/release.py:35`).

## What the repository implements

The repository implements a modular ERP/application platform with an ORM, HTTP server, addon loader, web client, scheduled jobs, messaging/bus facilities, reporting, localization, authentication, and a broad set of business addons. The root README describes accounting, CRM, website, eCommerce, warehouse, projects, POS, HR, marketing, and manufacturing as application areas; installed functionality depends on selected addons and database configuration.

## Architectural classification

Static evidence supports a **modular monolith with plugin/addon architecture**: one Python server process/runtime loads addon modules into a shared registry and PostgreSQL database. The source also contains browser JavaScript applications, HTTP controllers, long-running services, cron execution, bus messaging, and optional external integrations. No independently deployable microservice boundary is established by the repository inventory.
