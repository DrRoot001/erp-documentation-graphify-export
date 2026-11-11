# Cloning Guide

## Objective

Build an independent ERP SYSTEM implementation that satisfies the documented requirements and preserves the source system's observable contracts where evidence exists.

## Method

1. Treat `13_TRACEABILITY_AND_GOVERNANCE` as the control plane.
2. Implement foundation services before domain modules.
3. Use module specifications as bounded contexts with explicit dependencies.
4. Implement database entities from ORM evidence, marking runtime-only details as verification items.
5. Implement APIs from authoritative route records and define payloads only where source evidence establishes them.
6. Reconstruct workflows from source-linked transitions and tests; label unresolved rollback or notification behavior.
7. Implement authorization from groups, model access, record rules, and route metadata.
8. Add automated tests before declaring feature parity.
9. Validate deployment, backups, observability, and integrations in a staging environment.

## Technology independence

The clone is not required to use Python, PostgreSQL, Odoo, XML, or the original frontend framework. Those are source-architecture references. The clone must preserve externally meaningful behavior and documented data semantics unless a deliberate deviation is recorded as an assumption.

## Evidence boundary

Do not convert an inventory row into a requirement without reviewing its source context. When behavior is not established, use `UNKNOWN` or `ASSUMPTION` and create a verification task.
