# Module: l10n_in_boe

- **Module ID:** MOD-228
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_in_boe`
- **Manifest:** `addons/l10n_in_boe/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

- Adds Bill of Entry (BOE) support for the Indian localization.
- This Allows users to record import BOE details, link stock receipts, create BOE journal entries, and account for custom duties using landed costs.

**Scope evidence:** The module contains 13 files, including 8 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_in`, `stock_landed_costs`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_in_boe/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 15 methods, 1 constraint handlers, 0 onchange handlers, and 6 dependency declarations.
- **Evidence:** `addons/l10n_in_boe/models/account_move.py:4`, `addons/l10n_in_boe/wizard/l10n_in_boe_wizard.py:6`, `addons/l10n_in_boe/wizard/l10n_in_boe_wizard.py:286`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/l10n_in_boe/wizard/l10n_in_boe_wizard.xml:2`, `addons/l10n_in_boe/views/account_move_views.xml:3`, `addons/l10n_in_boe/views/account_move_views.xml:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_in_boe/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_in_boe/views/account_move_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_in_boe/tests/test_l10n_in_boe_flow.py`, `addons/l10n_in_boe/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `boe_view_form`, `action_l10n_in_boe_wizard_multi`, `invoice_form_inherit_l10n_in_boe`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/l10n_in_boe/wizard/l10n_in_boe_wizard.xml:4`, `addons/l10n_in_boe/wizard/l10n_in_boe_wizard.xml:5`, `addons/l10n_in_boe/views/account_move_views.xml:17`, `addons/l10n_in_boe/views/account_move_views.xml:19`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_in_boe/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_in_boe/views/account_move_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `account.move` (addons/l10n_in_boe/models/account_move.py:4); `l10n_in.boe.wizard` (addons/l10n_in_boe/wizard/l10n_in_boe_wizard.py:6); `l10n_in.boe.wizard.line` (addons/l10n_in_boe/wizard/l10n_in_boe_wizard.py:286)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_in`, `stock_landed_costs`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_in_boe/__init__.py`
- `addons/l10n_in_boe/__manifest__.py`
- `addons/l10n_in_boe/i18n/hi.po`
- `addons/l10n_in_boe/i18n/l10n_in_boe.pot`
- `addons/l10n_in_boe/models/__init__.py`
- `addons/l10n_in_boe/models/account_move.py`
- `addons/l10n_in_boe/security/ir.access.csv`
- `addons/l10n_in_boe/tests/__init__.py`
- `addons/l10n_in_boe/tests/test_l10n_in_boe_flow.py`
- `addons/l10n_in_boe/views/account_move_views.xml`
- `addons/l10n_in_boe/wizard/__init__.py`
- `addons/l10n_in_boe/wizard/l10n_in_boe_wizard.py`
- `addons/l10n_in_boe/wizard/l10n_in_boe_wizard.xml`
