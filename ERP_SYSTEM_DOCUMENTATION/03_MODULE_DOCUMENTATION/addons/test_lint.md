# Module: test_lint

- **Module ID:** MOD-661
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `odoo/addons/test_lint`
- **Manifest:** `odoo/addons/test_lint/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tests`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

A module to test Odoo code with various linters.

**Scope evidence:** The module contains 30 files, including 29 Python, 0 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `base`.

## 2. Module structure

- Model/business logic files: 0
- Controller/API files: 0
- XML/data/view/template files: 0
- Browser asset files: 0
- Security files: 0
- Test files: 27
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `odoo/addons/test_lint/tests/test_index.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 27 test files are present.
- **Evidence:** `odoo/addons/test_lint/tests/test_jstranslate.py`, `odoo/addons/test_lint/tests/test_override_signatures.py`, `odoo/addons/test_lint/tests/test_sql_injection.py`, `odoo/addons/test_lint/tests/test_manifests.py`, `odoo/addons/test_lint/tests/_odoo_checker_sql_injection.py`, `odoo/addons/test_lint/tests/_odoo_checker_unlink_override.py`, `odoo/addons/test_lint/tests/test_pylint.py`, `odoo/addons/test_lint/tests/test_docstring.py`, `odoo/addons/test_lint/tests/test_routes.py`, `odoo/addons/test_lint/tests/test_checkers.py`, `odoo/addons/test_lint/tests/common.py`, `odoo/addons/test_lint/tests/test_test_holes.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 0; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `odoo/addons/test_lint/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `odoo/addons/test_lint/tests/test_index.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** No
- **Backend/model evidence:** Not found
- **UI/data evidence:** Not found
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `odoo/addons/test_lint/__init__.py`
- `odoo/addons/test_lint/__manifest__.py`
- `odoo/addons/test_lint/tests/__init__.py`
- `odoo/addons/test_lint/tests/_odoo_checker_gettext.py`
- `odoo/addons/test_lint/tests/_odoo_checker_sql_injection.py`
- `odoo/addons/test_lint/tests/_odoo_checker_unlink_override.py`
- `odoo/addons/test_lint/tests/_pylint_path_setup.py`
- `odoo/addons/test_lint/tests/common.py`
- `odoo/addons/test_lint/tests/eslintrc`
- `odoo/addons/test_lint/tests/test_checkers.py`
- `odoo/addons/test_lint/tests/test_docstring.py`
- `odoo/addons/test_lint/tests/test_dunderinit.py`
- `odoo/addons/test_lint/tests/test_eslint.py`
- `odoo/addons/test_lint/tests/test_i18n.py`
- `odoo/addons/test_lint/tests/test_icons.py`
- `odoo/addons/test_lint/tests/test_index.py`
- `odoo/addons/test_lint/tests/test_jstranslate.py`
- `odoo/addons/test_lint/tests/test_l10n.py`
- `odoo/addons/test_lint/tests/test_manifests.py`
- `odoo/addons/test_lint/tests/test_markers.py`
- `odoo/addons/test_lint/tests/test_model_attributes.py`
- `odoo/addons/test_lint/tests/test_override_signatures.py`
- `odoo/addons/test_lint/tests/test_override_translated_fields.py`
- `odoo/addons/test_lint/tests/test_pofile.py`
- `odoo/addons/test_lint/tests/test_pylint.py`
- `odoo/addons/test_lint/tests/test_python_lint.py`
- `odoo/addons/test_lint/tests/test_routes.py`
- `odoo/addons/test_lint/tests/test_security_files.py`
- `odoo/addons/test_lint/tests/test_sql_injection.py`
- `odoo/addons/test_lint/tests/test_test_holes.py`
