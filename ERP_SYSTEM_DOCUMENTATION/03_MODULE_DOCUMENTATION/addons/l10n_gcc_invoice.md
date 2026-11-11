# Module: l10n_gcc_invoice

- **Module ID:** MOD-199
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_gcc_invoice`
- **Manifest:** `addons/l10n_gcc_invoice/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Adds Arabic as a secondary language on your invoice, credit note, debit note, vendor bill, and refund bill

**Scope evidence:** The module contains 14 files, including 9 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 11 methods, 0 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/l10n_gcc_invoice/models/res_config_settings.py:4`, `addons/l10n_gcc_invoice/models/product.py:8`, `addons/l10n_gcc_invoice/models/account_move.py:17`, `addons/l10n_gcc_invoice/models/account_move.py:41`, `addons/l10n_gcc_invoice/models/res_company.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 5 record/template/menu identifiers.
- **Evidence:** `addons/l10n_gcc_invoice/views/res_config_settings_views.xml:4`, `addons/l10n_gcc_invoice/views/report_invoice.xml:4`, `addons/l10n_gcc_invoice/views/report_invoice.xml:242`, `addons/l10n_gcc_invoice/views/report_invoice.xml:265`, `addons/l10n_gcc_invoice/views/report_invoice.xml:311`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_gcc_invoice/tests/test_gcc_invoice.py`, `addons/l10n_gcc_invoice/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `res_config_settings_view_form_inherit_l10n_gcc_invoice`, `l10n_gcc_report_invoice_document`, `l10n_gcc_document_tax_totals`, `l10n_gcc_document_tax_totals_company_currency_template`, `report_invoice`
- Menus: 0; representative evidence: Not found in module
- Templates: 4; representative evidence: `addons/l10n_gcc_invoice/views/report_invoice.xml:4`, `addons/l10n_gcc_invoice/views/report_invoice.xml:242`, `addons/l10n_gcc_invoice/views/report_invoice.xml:265`, `addons/l10n_gcc_invoice/views/report_invoice.xml:311`
- View/action field declarations: 2; representative evidence: `addons/l10n_gcc_invoice/views/res_config_settings_views.xml:6`, `addons/l10n_gcc_invoice/views/res_config_settings_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_gcc_invoice/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `res.config.settings` (addons/l10n_gcc_invoice/models/res_config_settings.py:4); inherits `product.product` (addons/l10n_gcc_invoice/models/product.py:8); inherits `account.move` (addons/l10n_gcc_invoice/models/account_move.py:17); inherits `account.move.line` (addons/l10n_gcc_invoice/models/account_move.py:41); inherits `res.company` (addons/l10n_gcc_invoice/models/res_company.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_gcc_invoice/__init__.py`
- `addons/l10n_gcc_invoice/__manifest__.py`
- `addons/l10n_gcc_invoice/i18n/ar.po`
- `addons/l10n_gcc_invoice/i18n/l10n_gcc_invoice.pot`
- `addons/l10n_gcc_invoice/models/__init__.py`
- `addons/l10n_gcc_invoice/models/account_move.py`
- `addons/l10n_gcc_invoice/models/product.py`
- `addons/l10n_gcc_invoice/models/res_company.py`
- `addons/l10n_gcc_invoice/models/res_config_settings.py`
- `addons/l10n_gcc_invoice/static/src/scss/styles.scss`
- `addons/l10n_gcc_invoice/tests/__init__.py`
- `addons/l10n_gcc_invoice/tests/test_gcc_invoice.py`
- `addons/l10n_gcc_invoice/views/report_invoice.xml`
- `addons/l10n_gcc_invoice/views/res_config_settings_views.xml`
