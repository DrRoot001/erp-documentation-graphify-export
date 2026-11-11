# End-to-End Workflows

## Evidence boundary

The source catalog contains 8 platform workflows and 666 module workflow evidence rows. The clone must implement only the flows supported by installed module evidence and must not treat a module's presence as proof that a complete business process is enabled.

## Standard execution contract

1. A user, API client, scheduler, webhook, or server operator triggers an action.
2. The system establishes request/session/company context and authenticates where required.
3. A route, model action, scheduled job, or event handler resolves the operation.
4. Input, field, model, access, record-rule, and business constraints are evaluated.
5. The domain operation executes transactionally through persistence and integrations.
6. Success returns a rendered/API result and commits side effects; failures return an explicit exception/response and roll back transactional work where supported.

This sequence is `INFERRED` from the existing workflow, API, database, and security evidence.

## Domain workflow readiness

The module register records state models, action/state evidence, controllers, scheduled files, reports, tests, and source paths per module. Use it to select and trace a domain flow; do not infer missing approval, notification, rollback, or accounting behavior from generic ERP practice.
