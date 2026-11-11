# Module: l10n_ph_invoice

- **Module ID:** MOD-293
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ph_invoice`
- **Manifest:** `addons/l10n_ph_invoice/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Apply Philippine SC/PWD discount privileges on customer invoices and credit notes.

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 19 files, including 12 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_ph`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_ph_invoice/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 89 methods, 1 constraint handlers, 1 onchange handlers, and 8 dependency declarations.
- **Evidence:** `addons/l10n_ph_invoice/models/l10n_ph_discount_privilege_line_mixin.py:6`, `addons/l10n_ph_invoice/models/l10n_ph_discount_privilege.py:7`, `addons/l10n_ph_invoice/models/account_move.py:6`, `addons/l10n_ph_invoice/models/account_move_line.py:7`, `addons/l10n_ph_invoice/models/template_ph.py:8`, `addons/l10n_ph_invoice/wizard/l10n_ph_discount_privilege_wizard.py:8`, `addons/l10n_ph_invoice/wizard/l10n_ph_discount_privilege_wizard.py:321`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ph_invoice/wizard/l10n_ph_discount_privilege_wizard_views.xml:3`, `addons/l10n_ph_invoice/data/menuitem_data.xml:3`, `addons/l10n_ph_invoice/views/account_move_views.xml:3`, `addons/l10n_ph_invoice/views/l10n_ph_discount_privilege_views.xml:3`, `addons/l10n_ph_invoice/views/l10n_ph_discount_privilege_views.xml:19`, `addons/l10n_ph_invoice/views/l10n_ph_discount_privilege_views.xml:43`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_ph_invoice/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_ph_invoice/tests/test_discount_privilege_wizard.py`, `addons/l10n_ph_invoice/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `view_l10n_ph_discount_privilege_wizard_form`, `Discount Privileges`, `view_move_form_l10n_ph_discount_privilege_button`, `view_l10n_ph_discount_privilege_tree`, `view_l10n_ph_discount_privilege_form`, `action_l10n_ph_discount_privilege`
- Menus: 1; representative evidence: `addons/l10n_ph_invoice/data/menuitem_data.xml:3`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 10; representative evidence: `addons/l10n_ph_invoice/wizard/l10n_ph_discount_privilege_wizard_views.xml:5`, `addons/l10n_ph_invoice/wizard/l10n_ph_discount_privilege_wizard_views.xml:6`, `addons/l10n_ph_invoice/views/account_move_views.xml:5`, `addons/l10n_ph_invoice/views/account_move_views.xml:7`, `addons/l10n_ph_invoice/views/l10n_ph_discount_privilege_views.xml:5`, `addons/l10n_ph_invoice/views/l10n_ph_discount_privilege_views.xml:6`, `addons/l10n_ph_invoice/views/l10n_ph_discount_privilege_views.xml:21`, `addons/l10n_ph_invoice/views/l10n_ph_discount_privilege_views.xml:22`, `addons/l10n_ph_invoice/views/l10n_ph_discount_privilege_views.xml:45`, `addons/l10n_ph_invoice/views/l10n_ph_discount_privilege_views.xml:46`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ph_invoice/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: `l10n_ph.discount.privilege.line.mixin` (addons/l10n_ph_invoice/models/l10n_ph_discount_privilege_line_mixin.py:6); `l10n_ph.discount.privilege` (addons/l10n_ph_invoice/models/l10n_ph_discount_privilege.py:7); inherits `account.move` (addons/l10n_ph_invoice/models/account_move.py:6); `account.move.line` (addons/l10n_ph_invoice/models/account_move_line.py:7); inherits `account.chart.template` (addons/l10n_ph_invoice/models/template_ph.py:8); `l10n_ph.discount.privilege.wizard` (addons/l10n_ph_invoice/wizard/l10n_ph_discount_privilege_wizard.py:8); `l10n_ph.discount.privilege.wizard.line` (addons/l10n_ph_invoice/wizard/l10n_ph_discount_privilege_wizard.py:321)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_ph`
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

- `addons/l10n_ph_invoice/__init__.py`
- `addons/l10n_ph_invoice/__manifest__.py`
- `addons/l10n_ph_invoice/data/menuitem_data.xml`
- `addons/l10n_ph_invoice/i18n/l10n_ph_invoice.pot`
- `addons/l10n_ph_invoice/i18n/tl.po`
- `addons/l10n_ph_invoice/models/__init__.py`
- `addons/l10n_ph_invoice/models/account_move.py`
- `addons/l10n_ph_invoice/models/account_move_line.py`
- `addons/l10n_ph_invoice/models/l10n_ph_discount_privilege.py`
- `addons/l10n_ph_invoice/models/l10n_ph_discount_privilege_line_mixin.py`
- `addons/l10n_ph_invoice/models/template_ph.py`
- `addons/l10n_ph_invoice/security/ir.access.csv`
- `addons/l10n_ph_invoice/tests/__init__.py`
- `addons/l10n_ph_invoice/tests/test_discount_privilege_wizard.py`
- `addons/l10n_ph_invoice/views/account_move_views.xml`
- `addons/l10n_ph_invoice/views/l10n_ph_discount_privilege_views.xml`
- `addons/l10n_ph_invoice/wizard/__init__.py`
- `addons/l10n_ph_invoice/wizard/l10n_ph_discount_privilege_wizard.py`
- `addons/l10n_ph_invoice/wizard/l10n_ph_discount_privilege_wizard_views.xml`
