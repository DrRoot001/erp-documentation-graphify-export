# Module: l10n_account_withholding_tax

- **Module ID:** MOD-115
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_account_withholding_tax`
- **Manifest:** `addons/l10n_account_withholding_tax/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Allows users to manage withholding taxes on invoices, bills, and payments.

**Scope evidence:** The module contains 35 files, including 19 Python, 8 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 11
- Controller/API files: 0
- XML/data/view/template files: 8
- Browser asset files: 2
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_account_withholding_tax/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 11 model declarations, 132 methods, 4 constraint handlers, 4 onchange handlers, and 40 dependency declarations.
- **Evidence:** `addons/l10n_account_withholding_tax/demo/demo.py:6`, `addons/l10n_account_withholding_tax/models/product_template.py:6`, `addons/l10n_account_withholding_tax/models/res_config_settings.py:5`, `addons/l10n_account_withholding_tax/models/account_payment.py:5`, `addons/l10n_account_withholding_tax/models/account_payment_withholding_line.py:5`, `addons/l10n_account_withholding_tax/models/account_tax.py:6`, `addons/l10n_account_withholding_tax/models/account_withholding_line.py:10`, `addons/l10n_account_withholding_tax/models/account_move.py:5`, `addons/l10n_account_withholding_tax/models/res_company.py:5`, `addons/l10n_account_withholding_tax/wizards/account_payment_register_withholding_line.py:5`, `addons/l10n_account_withholding_tax/wizards/account_payment_register.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 8 XML files and 2 JavaScript/TypeScript files; static XML analysis found 9 record/template/menu identifiers.
- **Evidence:** `addons/l10n_account_withholding_tax/wizards/account_payment_register_views.xml:3`, `addons/l10n_account_withholding_tax/views/report_invoice.xml:2`, `addons/l10n_account_withholding_tax/views/account_move_views.xml:3`, `addons/l10n_account_withholding_tax/views/account_payment_views.xml:3`, `addons/l10n_account_withholding_tax/views/account_payment_views.xml:68`, `addons/l10n_account_withholding_tax/views/res_config_settings.xml:3`, `addons/l10n_account_withholding_tax/views/account_tax_views.xml:3`, `addons/l10n_account_withholding_tax/views/account_tax_views.xml:29`, `addons/l10n_account_withholding_tax/views/report_payment_receipt_templates.xml:2`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_account_withholding_tax/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_account_withholding_tax/tests/test_account_withholding_amounts.py`, `addons/l10n_account_withholding_tax/tests/test_account_withholding_flows.py`, `addons/l10n_account_withholding_tax/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 8; representative identifiers: `view_account_payment_register_form`, `report_invoice_document`, `account_move_view_form_inherit_l10n_account_withholding_tax`, `view_account_payment_form`, `view_account_payment_tree`, `res_config_settings_form`, `view_tax_form`, `view_account_tax_search_inherit_l10n_account_withholding_tax`, `report_payment_receipt_document`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/l10n_account_withholding_tax/views/report_invoice.xml:2`, `addons/l10n_account_withholding_tax/views/report_payment_receipt_templates.xml:2`
- View/action field declarations: 14; representative evidence: `addons/l10n_account_withholding_tax/wizards/account_payment_register_views.xml:5`, `addons/l10n_account_withholding_tax/wizards/account_payment_register_views.xml:8`, `addons/l10n_account_withholding_tax/views/account_move_views.xml:5`, `addons/l10n_account_withholding_tax/views/account_move_views.xml:7`, `addons/l10n_account_withholding_tax/views/account_payment_views.xml:5`, `addons/l10n_account_withholding_tax/views/account_payment_views.xml:8`, `addons/l10n_account_withholding_tax/views/account_payment_views.xml:70`, `addons/l10n_account_withholding_tax/views/account_payment_views.xml:72`, `addons/l10n_account_withholding_tax/views/res_config_settings.xml:5`, `addons/l10n_account_withholding_tax/views/res_config_settings.xml:7`, `addons/l10n_account_withholding_tax/views/account_tax_views.xml:5`, `addons/l10n_account_withholding_tax/views/account_tax_views.xml:7`
- Browser assets: 2; representative files: `addons/l10n_account_withholding_tax/static/src/helpers/account_tax.js`, `addons/l10n_account_withholding_tax/static/src/components/withhold_selector/withhold_selector.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_account_withholding_tax/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 11
- Representative model evidence: inherits `account.chart.template` (addons/l10n_account_withholding_tax/demo/demo.py:6); inherits `product.template` (addons/l10n_account_withholding_tax/models/product_template.py:6); inherits `res.config.settings` (addons/l10n_account_withholding_tax/models/res_config_settings.py:5); inherits `account.payment` (addons/l10n_account_withholding_tax/models/account_payment.py:5); `account.payment.withholding.line` (addons/l10n_account_withholding_tax/models/account_payment_withholding_line.py:5); inherits `account.tax` (addons/l10n_account_withholding_tax/models/account_tax.py:6); `account.withholding.line` (addons/l10n_account_withholding_tax/models/account_withholding_line.py:10); inherits `account.move` (addons/l10n_account_withholding_tax/models/account_move.py:5); inherits `res.company` (addons/l10n_account_withholding_tax/models/res_company.py:5); `account.payment.register.withholding.line` (addons/l10n_account_withholding_tax/wizards/account_payment_register_withholding_line.py:5); inherits `account.payment.register` (addons/l10n_account_withholding_tax/wizards/account_payment_register.py:6)
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
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_account_withholding_tax/__init__.py`
- `addons/l10n_account_withholding_tax/__manifest__.py`
- `addons/l10n_account_withholding_tax/demo/__init__.py`
- `addons/l10n_account_withholding_tax/demo/demo.py`
- `addons/l10n_account_withholding_tax/i18n/en_IN.po`
- `addons/l10n_account_withholding_tax/i18n/es_419.po`
- `addons/l10n_account_withholding_tax/i18n/id.po`
- `addons/l10n_account_withholding_tax/i18n/l10n_account_withholding_tax.pot`
- `addons/l10n_account_withholding_tax/i18n/th.po`
- `addons/l10n_account_withholding_tax/models/__init__.py`
- `addons/l10n_account_withholding_tax/models/account_move.py`
- `addons/l10n_account_withholding_tax/models/account_payment.py`
- `addons/l10n_account_withholding_tax/models/account_payment_withholding_line.py`
- `addons/l10n_account_withholding_tax/models/account_tax.py`
- `addons/l10n_account_withholding_tax/models/account_withholding_line.py`
- `addons/l10n_account_withholding_tax/models/product_template.py`
- `addons/l10n_account_withholding_tax/models/res_company.py`
- `addons/l10n_account_withholding_tax/models/res_config_settings.py`
- `addons/l10n_account_withholding_tax/security/ir.access.csv`
- `addons/l10n_account_withholding_tax/static/src/components/account_payment.xml`
- `addons/l10n_account_withholding_tax/static/src/components/withhold_selector/withhold_selector.js`
- `addons/l10n_account_withholding_tax/static/src/helpers/account_tax.js`
- `addons/l10n_account_withholding_tax/tests/__init__.py`
- `addons/l10n_account_withholding_tax/tests/test_account_withholding_amounts.py`
- `addons/l10n_account_withholding_tax/tests/test_account_withholding_flows.py`
- `addons/l10n_account_withholding_tax/views/account_move_views.xml`
- `addons/l10n_account_withholding_tax/views/account_payment_views.xml`
- `addons/l10n_account_withholding_tax/views/account_tax_views.xml`
- `addons/l10n_account_withholding_tax/views/report_invoice.xml`
- `addons/l10n_account_withholding_tax/views/report_payment_receipt_templates.xml`
- `addons/l10n_account_withholding_tax/views/res_config_settings.xml`
- `addons/l10n_account_withholding_tax/wizards/__init__.py`
- `addons/l10n_account_withholding_tax/wizards/account_payment_register.py`
- `addons/l10n_account_withholding_tax/wizards/account_payment_register_views.xml`
- `addons/l10n_account_withholding_tax/wizards/account_payment_register_withholding_line.py`
