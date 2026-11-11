# Business Rules

Business rules are source-evidence obligations, not invented policies. The existing package records validation rules, model constraints, state/action evidence, security declarations, and workflow surfaces. The clone must translate each source-backed rule into a testable invariant.

## Rule classes

- **Data rules:** required fields, types, constraints, uniqueness, defaults, computed values, and relationship behavior from ORM/constraint inventories.
- **Lifecycle rules:** module installation/update/uninstall, migration ordering, and dependency graph rules.
- **State rules:** transitions and action conditions identified in workflow evidence and model methods.
- **Security rules:** model access, record rules, groups, route authentication, CSRF, and company/data isolation evidence.
- **Integration rules:** provider configuration, request/response handling, retries/errors, and optional activation conditions.
- **Operational rules:** scheduled actions, background processing, logging, backup/restore, and deployment configuration.

## Evidence labels

Every rule in later module specifications must use `VERIFIED`, `INFERRED`, `ASSUMPTION`, `UNKNOWN`, or `NOT_APPLICABLE`, with a source path and inventory identifier.

The existing `ERP_SYSTEM_DOCUMENTATION/02_REQUIREMENTS/Validation_Rules.csv`, database constraint dictionaries, security inventories, and workflow evidence inventory are the controlling evidence sources.
