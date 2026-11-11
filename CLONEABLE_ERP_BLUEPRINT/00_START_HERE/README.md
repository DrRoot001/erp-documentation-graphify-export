# ERP SYSTEM — Cloneable ERP Blueprint

This directory is the implementation-oriented specification derived from the evidence in [`../ERP_SYSTEM_DOCUMENTATION/MASTER_INDEX.md`](../../ERP_SYSTEM_DOCUMENTATION/MASTER_INDEX.md).

It is intentionally separate from `ERP_SYSTEM_DOCUMENTATION/`. The original package records what the Odoo repository contains; this package translates that evidence into a technology-independent blueprint for a new engineering team.

## Evidence policy

Every statement in this blueprint must be classified as:

- **VERIFIED** — directly supported by source or an existing inventory.
- **INFERRED** — derived from multiple verified observations.
- **ASSUMPTION** — a design choice required to make the clone implementable; never presented as existing behavior.
- **UNKNOWN** — insufficient evidence.
- **NOT_APPLICABLE** — not relevant to the specific capability.

The clone may use a different technology stack. Odoo-specific implementation details remain supporting evidence, not mandatory design decisions.

## Reading order

1. [`SYSTEM_OVERVIEW.md`](SYSTEM_OVERVIEW.md)
2. [`PROJECT_SCOPE.md`](PROJECT_SCOPE.md)
3. [`CLONING_GUIDE.md`](CLONING_GUIDE.md)
4. [`DOCUMENTATION_INDEX.md`](DOCUMENTATION_INDEX.md)
5. Product, architecture, module, data, API, workflow, security, frontend, testing, and roadmap sections.

## Blueprint status

Phases 1–9 establish the structure, translation rules, source baseline, 666-module coverage map, independent module specifications, database/API/workflow/security/frontend/testing/deployment specifications, implementation roadmap, traceability governance, and final audit. Runtime schema, API payload, browser, test execution, deployment, backup, performance, and production topology validation remain explicitly identified as environment-dependent work.
