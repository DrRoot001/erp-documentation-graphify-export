# Business Rules — Phase 3

## Verified platform rules

1. **Dependency ordering:** a module's manifest dependencies are prerequisites for loading the module; evidence is the manifest graph and `odoo/modules/`.
2. **Declarative validation:** model constraint, computed dependency, and onchange decorators define processing/validation hooks; counts and evidence are in `Validation_Rules.csv`.
3. **Authorization:** addon security declarations are evaluated by the platform security layer; exact permissions are module and deployment specific.
4. **Transactional persistence:** ORM/database operations use the shared registry and PostgreSQL transaction layer; exact rollback boundaries depend on the operation.
5. **Scheduled execution:** cron/automation declarations are conditional on installation and server scheduling configuration.
6. **Reporting:** report actions/templates are conditional on installed modules and configured report services.

## Explicit limits

No domain-specific rule is inferred from a module name. Tax, accounting, inventory, payroll, sales, manufacturing, localization, and other rules must be traced from the relevant model methods, XML data, and tests in the module evidence pages.
