# Application Layers

1. **Presentation:** browser/client components, XML views/templates, reports, and public/portal surfaces.
2. **Transport:** HTTP routing, sessions, request/response serialization, CSRF, and webhooks.
3. **Application:** use cases, controllers, scheduled actions, command handlers, and orchestration.
4. **Domain:** module models, state transitions, validations, business rules, and services.
5. **Persistence:** ORM registry, fields, relationships, constraints, transactions, migrations, and PostgreSQL.
6. **Integration:** external authentication, mail/SMS, payments, storage, Google, IoT, localization/e-invoicing, and provider adapters.
7. **Operations:** bootstrap, configuration, workers, logging, profiling, backup/restore, deployment, and maintenance.

The clone should keep domain rules independent of transport and vendor adapters where feasible. This separation is a clone design requirement, not a claim about all source implementation boundaries.
