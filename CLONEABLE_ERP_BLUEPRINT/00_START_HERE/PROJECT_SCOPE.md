# Project Scope

## In scope

- All 666 manifest-backed modules and their classified domains.
- Platform capabilities: bootstrap, configuration, module loading, ORM, HTTP, security, jobs, assets, reporting, translations, and integrations.
- Business domains evidenced by the module inventory, including accounting, CRM, sales, purchase, inventory, HR, manufacturing, projects, POS, website, ecommerce, marketing, localizations, and technical/test modules.
- Cloneable requirements for data, APIs, workflows, access control, user interface, testing, deployment, and maintenance.
- Source evidence retained through paths, inventory IDs, and traceability references.

## Not automatically in scope

- A tenant-specific installed module set or database contents.
- Runtime-generated PostgreSQL schema not verified from a deployed instance.
- Production credentials, secrets, SLA values, performance benchmarks, or external-service availability.
- Unverified behavior inferred only from names or generic ERP expectations.

## Scope interpretation

The blueprint preserves all discovered modules. Business-domain folders are organizational views, not claims that every addon is a standalone ERP application. Modules that are localization, integration, framework, test, or deployment artifacts are retained under `OTHER_MODULES` or a later evidence-based subdivision.
