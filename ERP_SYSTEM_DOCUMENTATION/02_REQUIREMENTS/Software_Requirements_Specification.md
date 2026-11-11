# Software Requirements Specification

## Evidence policy

This SRS records requirements directly evidenced by the repository's framework and addon architecture. It does not assert that every addon is installed in every deployment. Requirement IDs are stable within this documentation package; module-specific evidence is linked to the per-addon pages.

## System-level requirements

| ID | Requirement | Evidence | Status |
|---|---|---|---|
| FR-001 | The system shall expose a command-line entry point that starts Odoo services. | `odoo-bin:1-6`; `odoo/__main__.py:1-3` | Implemented |
| FR-002 | The system shall load addon manifests and resolve declared dependencies before module initialization. | `odoo/modules/module_graph.py`; `odoo/modules/loading.py` | Implemented |
| FR-003 | The system shall provide an ORM-backed model registry over PostgreSQL. | `odoo/orm/`; `odoo/sql_db.py`; `odoo/modules/registry.py` | Implemented |
| FR-004 | The system shall dispatch HTTP requests through route declarations and request/session handling. | `odoo/http/router.py`; `odoo/http/dispatcher.py`; 975 static route declarations | Implemented |
| FR-005 | The system shall support declarative model access controls and record-rule security artifacts. | 279 security artifacts; `odoo/addons/base` security/model code | Implemented artifacts; runtime verification required |
| FR-006 | The system shall support scheduled/background server activities through its server and cron infrastructure. | `odoo/service/`; base addon scheduled action implementations | Implemented artifacts; deployment/runtime verification required |
| FR-007 | The system shall provide addon-defined user interfaces through XML views/templates and browser assets. | 6,101 XML; 6,899 JS/TS; asset declarations in manifests | Implemented artifacts |
| FR-008 | The system shall provide automated test modules for selected framework and addon behavior. | 2,786 test files | Partially evidenced; execution not performed |

## Module requirements

Each manifest-backed addon is assigned `FR-MOD-666` in the module catalog. Its declared dependencies, data files, assets, and implementation artifacts are documented in the linked module page. Detailed field-level and workflow requirements must be derived from the module's actual models, views, controllers, and tests rather than from its name.

## Negative/exception requirements

- Invalid configuration, missing dependencies, denied access, validation failures, database errors, and external integration failures must be handled according to the relevant implementation; exact messages and rollback behavior require runtime verification.
- Secrets must not be copied into documentation; only variable names/configuration keys are documented.
