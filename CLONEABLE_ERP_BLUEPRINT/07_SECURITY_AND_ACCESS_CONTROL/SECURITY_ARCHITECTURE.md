# Security Architecture

## Verified security surface

| Evidence | Count |
|---|---:|
| Security-directory files | 279 |
| Groups | 192 |
| Model access rows | 2,577 |
| Record-rule rows | 11 |
| Route-security rows | 669 |
| Authentication-capability modules | 37 |
| Security test artifacts | 587 |

## Enforcement chain

Request/session identity -> route authentication and transport policy -> model access operation -> record-rule domain -> model constraints/business logic -> database transaction. Effective permissions depend on installed modules, loaded security data, user/group assignments, company context, and configuration.
