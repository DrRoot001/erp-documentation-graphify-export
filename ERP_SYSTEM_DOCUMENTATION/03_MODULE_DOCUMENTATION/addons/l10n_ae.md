# Module: l10n_ae

- **Module ID:** MOD-117
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ae`
- **Manifest:** `addons/l10n_ae/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

United Arab Emirates Accounting Module
=======================================================
United Arab Emirates accounting basic charts and localization.

Activates:

- Chart of Accounts
- Taxes
- Tax Report
- Fiscal Positions

**Scope evidence:** The module contains 17 files, including 5 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `l10n_gcc_invoice`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 0
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 8 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_ae/models/template_ae.py:6`, `addons/l10n_ae/models/account_move.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 79 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ae/demo/demo_company.xml:3`, `addons/l10n_ae/demo/demo_company.xml:17`, `addons/l10n_ae/data/account_tax_report_data.xml:3`, `addons/l10n_ae/data/account_tax_report_data.xml:10`, `addons/l10n_ae/data/account_tax_report_data.xml:14`, `addons/l10n_ae/data/account_tax_report_data.xml:18`, `addons/l10n_ae/data/account_tax_report_data.xml:24`, `addons/l10n_ae/data/account_tax_report_data.xml:28`, `addons/l10n_ae/data/account_tax_report_data.xml:32`, `addons/l10n_ae/data/account_tax_report_data.xml:36`, `addons/l10n_ae/data/account_tax_report_data.xml:41`, `addons/l10n_ae/data/account_tax_report_data.xml:46`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `base.partner_demo_company_ae`, `base.demo_company_ae`, `tax_report`, `tax_report_base`, `tax_report_tax`, `tax_report_adj`, `tax_report_line_all_sales`, `tax_report_line_standard_rated_supplies`, `tax_report_line_standard_rated_supplies_abu_dhabi`, `tax_report_line_standard_rated_supplies_abu_dhabi_tax`, `tax_report_line_standard_rated_supplies_abu_dhabi_base`, `tax_report_line_standard_rated_supplies_abu_dhabi_adj`, `tax_report_line_standard_rated_supplies_dubai`, `tax_report_line_standard_rated_supplies_dubai_tax`, `tax_report_line_standard_rated_supplies_dubai_base`, `tax_report_line_standard_rated_supplies_dubai_adj`, `tax_report_line_standard_rated_supplies_sharjah`, `tax_report_line_standard_rated_supplies_sharjah_tax`, `tax_report_line_standard_rated_supplies_sharjah_base`, `tax_report_line_standard_rated_supplies_sharjah_adj`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/l10n_ae/views/report_invoice_templates.xml:3`, `addons/l10n_ae/views/report_invoice_templates.xml:80`
- View/action field declarations: 2; representative evidence: `addons/l10n_ae/views/account_move.xml:6`, `addons/l10n_ae/views/account_move.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ae/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `account.chart.template` (addons/l10n_ae/models/template_ae.py:6); inherits `account.move` (addons/l10n_ae/models/account_move.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `l10n_gcc_invoice`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_ae/__init__.py`
- `addons/l10n_ae/__manifest__.py`
- `addons/l10n_ae/data/account_tax_report_data.xml`
- `addons/l10n_ae/data/l10n_ae_data.xml`
- `addons/l10n_ae/data/template/account.account-ae.csv`
- `addons/l10n_ae/data/template/account.depreciation.model-ae.csv`
- `addons/l10n_ae/data/template/account.fiscal.position-ae.csv`
- `addons/l10n_ae/data/template/account.tax-ae.csv`
- `addons/l10n_ae/data/template/account.tax.group-ae.csv`
- `addons/l10n_ae/demo/demo_company.xml`
- `addons/l10n_ae/i18n/ar.po`
- `addons/l10n_ae/i18n/l10n_ae.pot`
- `addons/l10n_ae/models/__init__.py`
- `addons/l10n_ae/models/account_move.py`
- `addons/l10n_ae/models/template_ae.py`
- `addons/l10n_ae/views/account_move.xml`
- `addons/l10n_ae/views/report_invoice_templates.xml`
