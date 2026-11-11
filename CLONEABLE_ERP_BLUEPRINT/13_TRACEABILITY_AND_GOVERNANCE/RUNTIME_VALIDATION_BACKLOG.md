# Runtime Validation Backlog

The following work remains outside static documentation and must be completed by the clone implementation team:

| Priority | Validation item | Required evidence |
|---|---|---|
| High | Installed module set and generated database schema | Sanitized registry, schema export, migration result |
| High | Authentication, ACL, record-rule, and company/tenant isolation | Allowed/denied test results for representative roles |
| High | Critical cross-module workflows | Executed acceptance traces with persisted state and rollback/failure evidence |
| High | API contracts | Captured request/response/error schemas and authorization behavior |
| Medium | Resolved views, templates, assets, and browser behavior | Runtime UI catalog, screenshots or automation results, accessibility checks |
| Medium | Migration and backup/restore | Upgrade logs, restore drill, filestore validation, recovery timing |
| Medium | External integrations and webhooks | Provider mocks/live sandbox traces, retry/idempotency evidence |
| Medium | Performance and scalability | Workload model, benchmark results, capacity and alert thresholds |
| Low | Technical-debt and unimplemented-path review | Issue ownership, disposition, regression tests |

Until these artifacts exist, the blueprint status is **static documentation complete / runtime validation pending**.
