# Testing Strategy — Phase 10

## Evidence baseline

Static source inspection identified **3,470 test artifacts**: **2,138 Python** and **1,332 JavaScript/TypeScript** files. Layer classification identified **1,729 backend/model**, **423 HTTP/integration**, and **1,318 browser/static** artifacts. These counts describe repository evidence, not pass rates or code coverage.

| Evidence artifact | Count |
|---|---:|
| Test files | 3,470 |
| Python tests | 2,138 |
| JavaScript/TypeScript tests | 1,332 |
| Backend/model layer | 1,729 |
| HTTP/integration layer | 423 |
| Browser/static layer | 1,318 |

## Detected test mechanisms

| Mechanism | Files |
|---|---:|
| Odoo test framework | 2,015 |
| Repository test artifact | 1,215 |
| patch utility | 486 |
| unittest | 421 |
| tour | 264 |
| web test server | 180 |

## Execution status

No test suite was executed for Phase 10. A valid execution requires a configured PostgreSQL database, selected addons, Python/runtime dependencies, browser assets for frontend tests, and any external-service mocks. Therefore all generated evidence cases remain **Not Executed**, and no coverage percentage or pass claim is made.

## Test layers

- **Unit/model:** ORM, constraints, fields, services, and isolated business logic.
- **Integration/HTTP:** request dispatch, controllers, authentication, database transactions, and service boundaries.
- **Browser/static:** QUnit, tours, client components, assets, and browser behavior.
- **Security:** access groups, model access, record rules, authentication, and route protection.

Source inventories: [`Test_File_Inventory.csv`](Test_File_Inventory.csv), [`Test_Module_Coverage.csv`](Test_Module_Coverage.csv), [`Evidence_Test_Cases.csv`](Evidence_Test_Cases.csv).
