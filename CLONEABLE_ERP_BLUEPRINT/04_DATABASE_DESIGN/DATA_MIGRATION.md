# Data Migration

The source package contains 88 migration artifacts. The clone migration plan must preserve version ordering, dependency prerequisites, data transformations, idempotency, rollback/forward-fix strategy, auditability, and backup/restore gates.

Migration scripts are source evidence, not a complete target-to-clone mapping. Every source model/field change used by the clone must be mapped to a migration task and tested against representative data.
