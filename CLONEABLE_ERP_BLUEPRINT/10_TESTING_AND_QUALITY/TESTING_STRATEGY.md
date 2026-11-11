# Testing Strategy

## Evidence baseline

The source package contains 3,470 test artifacts across Python and JavaScript/TypeScript, with backend/model, HTTP/integration, browser/static, and security evidence. These are source artifacts, not pass rates or runtime coverage.

## Clone strategy

Implement unit/model tests for entities, constraints, and domain services; integration tests for transactions, APIs, authentication, and external adapters; browser tests for views, components, navigation, assets, and accessibility; security tests for ACLs, record rules, tenant/company isolation, and denied paths; migration tests for upgrade/rollback/forward-fix behavior; and operational tests for backups, restore, health checks, and failure recovery.

A test is complete only when it has deterministic setup, explicit expected result, isolation/cleanup, evidence output, and an executed result.
