# Workflow Catalog — Phase 5
This catalog separates verified platform execution patterns from module-specific business flows. The repository contains 666 addon modules; `Workflow_Evidence_Inventory.csv` maps each module to its actual workflow evidence surfaces.
## Verified workflow families
| ID | Workflow | Evidence basis | Status |
|---|---|---|---|
| WF-001 | Server bootstrap and module loading | `odoo-bin`; `odoo/cli/`; `odoo/modules/`; `odoo/service/` | Source-backed pattern; runtime verification required |
| WF-002 | HTTP request and controller dispatch | `odoo/http/`; Route_Inventory.csv | Source-backed pattern; runtime verification required |
| WF-003 | ORM record lifecycle | `odoo/orm/`; `odoo/sql_db.py`; model pages | Source-backed pattern; runtime verification required |
| WF-004 | Scheduled and automated action | 496 scheduled/automation evidence files; `odoo/service/` | Source-backed pattern; runtime verification required |
| WF-005 | Report generation | 183 report evidence files; report addons | Source-backed pattern; runtime verification required |
| WF-006 | Authentication and authorization | `odoo/http/`; authentication addons; security files | Source-backed pattern; runtime verification required |
| WF-007 | Addon upgrade/migration | `odoo/modules/migration.py`; addon manifests/migrations | Source-backed pattern; runtime verification required |
| WF-008 | Business transaction lifecycle | Workflow_Evidence_Inventory.csv; per-module pages | Source-backed pattern; runtime verification required |

## Domain workflow coverage
Domain modules expose state/action methods, XML buttons, controllers, scheduled actions, reports, and tests in varying combinations. The evidence inventory records counts; it does not invent a single cross-module business process.

## Completion boundary
A workflow is **Fully verified** only after execution against a configured database, installed module set, user permissions, and required external services. Static source analysis establishes entry points and likely processing boundaries but cannot prove runtime sequence, notifications, rollback, or final state.
