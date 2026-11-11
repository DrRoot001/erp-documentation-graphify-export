# Module: l10n_tr

- **Module ID:** MOD-326
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_tr`
- **Manifest:** `addons/l10n_tr/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the base module to manage the accounting chart for Türkiye in Odoo
==========================================================================

Türkiye accounting basic charts and localizations
-------------------------------------------------
Activates:

- Chart of Accounts
- Taxes
- Tax Report

**Scope evidence:** The module contains 31 files, including 16 Python, 6 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `contacts`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 1
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_tr/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 17 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/l10n_tr/models/res_partner.py:4`, `addons/l10n_tr/models/template_tr.py:6`, `addons/l10n_tr/models/product.py:4`, `addons/l10n_tr/models/account_journal.py:4`, `addons/l10n_tr/models/l10n_tr_tax_office.py:4`, `addons/l10n_tr/models/ir_http.py:4`, `addons/l10n_tr/models/account_move_line.py:4`, `addons/l10n_tr/models/res_company.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 1 JavaScript/TypeScript files; static XML analysis found 130 record/template/menu identifiers.
- **Evidence:** `addons/l10n_tr/demo/demo_company.xml:3`, `addons/l10n_tr/demo/demo_company.xml:18`, `addons/l10n_tr/demo/demo_company.xml:33`, `addons/l10n_tr/demo/demo_company.xml:48`, `addons/l10n_tr/demo/demo_company.xml:61`, `addons/l10n_tr/demo/demo_company.xml:66`, `addons/l10n_tr/data/account_tax_report_data.xml:3`, `addons/l10n_tr/data/account_tax_report_data.xml:11`, `addons/l10n_tr/data/account_tax_report_data.xml:16`, `addons/l10n_tr/data/account_tax_report_data.xml:23`, `addons/l10n_tr/data/account_tax_report_data.xml:28`, `addons/l10n_tr/data/account_tax_report_data.xml:33`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_tr/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_tr/tests/test_sales_return_account.py`, `addons/l10n_tr/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `base.partner_demo_company_tr`, `l10n_tr_res_partner_1`, `l10n_tr_res_partner_2`, `l10n_tr_res_partner_3`, `base.demo_company_tr`, `base.demo_bank_tr`, `turkey_tax_report`, `tr_base_column`, `tr_tax_column`, `purchases_vat`, `purchases_vat_line_0`, `purchases_vat_expression_0_balance`, `purchases_vat_expression_0_tax`, `purchases_vat_line_1`, `purchases_vat_expression_1_balance`, `purchases_vat_expression_1_tax`, `purchases_vat_line_10`, `purchases_vat_expression_10_balance`, `purchases_vat_expression_10_tax`, `purchases_vat_line_20`
- Menus: 1; representative evidence: `addons/l10n_tr/views/l10n_tr_tax_office_views.xml:48`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 9; representative evidence: `addons/l10n_tr/views/l10n_tr_tax_office_views.xml:5`, `addons/l10n_tr/views/l10n_tr_tax_office_views.xml:6`, `addons/l10n_tr/views/l10n_tr_tax_office_views.xml:18`, `addons/l10n_tr/views/l10n_tr_tax_office_views.xml:19`, `addons/l10n_tr/views/l10n_tr_tax_office_views.xml:39`, `addons/l10n_tr/views/res_company_views.xml:5`, `addons/l10n_tr/views/res_company_views.xml:7`, `addons/l10n_tr/views/res_partner_views.xml:5`, `addons/l10n_tr/views/res_partner_views.xml:7`
- Browser assets: 1; representative files: `addons/l10n_tr/static/src/js/dynamic_list.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_tr/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: inherits `res.partner` (addons/l10n_tr/models/res_partner.py:4); inherits `account.chart.template` (addons/l10n_tr/models/template_tr.py:6); inherits `product.template` (addons/l10n_tr/models/product.py:4); inherits `account.journal` (addons/l10n_tr/models/account_journal.py:4); `l10n_tr.tax.office` (addons/l10n_tr/models/l10n_tr_tax_office.py:4); inherits `ir.http` (addons/l10n_tr/models/ir_http.py:4); inherits `account.move.line` (addons/l10n_tr/models/account_move_line.py:4); inherits `res.company` (addons/l10n_tr/models/res_company.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `contacts`
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

- `addons/l10n_tr/__init__.py`
- `addons/l10n_tr/__manifest__.py`
- `addons/l10n_tr/data/account_tax_report_data.xml`
- `addons/l10n_tr/data/account_tax_report_stamp_tax.xml`
- `addons/l10n_tr/data/l10n_tr.tax.office.csv`
- `addons/l10n_tr/data/template/account.account-tr.csv`
- `addons/l10n_tr/data/template/account.fiscal.position-tr.csv`
- `addons/l10n_tr/data/template/account.tax-tr.csv`
- `addons/l10n_tr/data/template/account.tax.group-tr.csv`
- `addons/l10n_tr/demo/demo_company.xml`
- `addons/l10n_tr/i18n/l10n_tr.pot`
- `addons/l10n_tr/i18n/tr.po`
- `addons/l10n_tr/migrations/1.1/end-migrate_update_taxes.py`
- `addons/l10n_tr/migrations/1.2/end-migrate_update_package.py`
- `addons/l10n_tr/migrations/1.3/end-migrate_update_taxes.py`
- `addons/l10n_tr/models/__init__.py`
- `addons/l10n_tr/models/account_journal.py`
- `addons/l10n_tr/models/account_move_line.py`
- `addons/l10n_tr/models/ir_http.py`
- `addons/l10n_tr/models/l10n_tr_tax_office.py`
- `addons/l10n_tr/models/product.py`
- `addons/l10n_tr/models/res_company.py`
- `addons/l10n_tr/models/res_partner.py`
- `addons/l10n_tr/models/template_tr.py`
- `addons/l10n_tr/security/ir.access.csv`
- `addons/l10n_tr/static/src/js/dynamic_list.js`
- `addons/l10n_tr/tests/__init__.py`
- `addons/l10n_tr/tests/test_sales_return_account.py`
- `addons/l10n_tr/views/l10n_tr_tax_office_views.xml`
- `addons/l10n_tr/views/res_company_views.xml`
- `addons/l10n_tr/views/res_partner_views.xml`
