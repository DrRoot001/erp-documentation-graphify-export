# Module: l10n_lk

- **Module ID:** MOD-262
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_lk`
- **Manifest:** `addons/l10n_lk/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Provides accounting localizations for Sri Lanka.

**Manifest description:**

Sri Lankan Accounting module
============================
- Chart of Accounts
- Fiscal Position
- Taxes & Tax Groups

Forms
=====
- VAT001
- WHT001

Tax Invoice
===========
- Custom tax invoice sequence format: YYMMM_QQQQ_XXXXX
- Tax Invoice / Supply Date / Mode of Payment in PDF report
- VAT registration tracking for companies and partners

**Scope evidence:** The module contains 22 files, including 10 Python, 6 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `l10n_account_withholding_tax`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 57 methods, 1 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/l10n_lk/models/res_partner.py:6`, `addons/l10n_lk/models/template_lk.py:6`, `addons/l10n_lk/models/account_resequence.py:15`, `addons/l10n_lk/models/account_move.py:37`, `addons/l10n_lk/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 0 JavaScript/TypeScript files; static XML analysis found 320 record/template/menu identifiers.
- **Evidence:** `addons/l10n_lk/demo/demo_company.xml:3`, `addons/l10n_lk/demo/demo_company.xml:15`, `addons/l10n_lk/data/form_vat001.xml:3`, `addons/l10n_lk/data/form_vat001.xml:9`, `addons/l10n_lk/data/form_vat001.xml:14`, `addons/l10n_lk/data/form_vat001.xml:18`, `addons/l10n_lk/data/form_vat001.xml:23`, `addons/l10n_lk/data/form_vat001.xml:27`, `addons/l10n_lk/data/form_vat001.xml:32`, `addons/l10n_lk/data/form_vat001.xml:38`, `addons/l10n_lk/data/form_vat001.xml:43`, `addons/l10n_lk/data/form_vat001.xml:48`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_lk/views/report_invoice.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_lk/tests/test_lk_tax_invoice_sequence.py`, `addons/l10n_lk/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `base.partner_demo_company_lk`, `base.demo_company_lk`, `l10n_lk_vat001`, `l10n_lk_vat001_cell_a`, `l10n_lk_vat001_balance_a`, `l10n_lk_vat001_cell_b`, `l10n_lk_vat001_balance_b`, `l10n_lk_vat001_cell_c`, `l10n_lk_vat001_balance_c`, `l10n_lk_vat001_lk_vat_001e_ot`, `l10n_lk_vat001_lk_vat_001e_a`, `l10n_lk_vat001_lk_vat_001e_a_cell_a`, `l10n_lk_vat001_lk_vat_001e_a_balance_a`, `l10n_lk_vat001_lk_vat_001e_a_cell_b`, `l10n_lk_vat001_lk_vat_001e_a_balance_b`, `l10n_lk_vat001_lk_vat_001e_a1`, `l10n_lk_vat001_lk_vat_001e_a1_cell_a`, `l10n_lk_vat001_lk_vat_001e_a1_balance_a`, `l10n_lk_vat001_lk_vat_001e_a1_cell_b`, `l10n_lk_vat001_lk_vat_001e_a1_balance_b`
- Menus: 0; representative evidence: Not found in module
- Templates: 3; representative evidence: `addons/l10n_lk/views/report_invoice.xml:3`, `addons/l10n_lk/views/report_invoice.xml:44`, `addons/l10n_lk/views/report_invoice.xml:64`
- View/action field declarations: 5; representative evidence: `addons/l10n_lk/views/report_invoice.xml:55`, `addons/l10n_lk/views/res_company_views.xml:5`, `addons/l10n_lk/views/res_company_views.xml:7`, `addons/l10n_lk/views/res_partner_views.xml:5`, `addons/l10n_lk/views/res_partner_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_lk/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/l10n_lk/views/report_invoice.xml`

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `res.partner` (addons/l10n_lk/models/res_partner.py:6); inherits `account.chart.template` (addons/l10n_lk/models/template_lk.py:6); inherits `account.resequence.wizard` (addons/l10n_lk/models/account_resequence.py:15); inherits `account.move` (addons/l10n_lk/models/account_move.py:37); inherits `res.company` (addons/l10n_lk/models/res_company.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `l10n_account_withholding_tax`
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

- `addons/l10n_lk/__init__.py`
- `addons/l10n_lk/__manifest__.py`
- `addons/l10n_lk/data/account.account.tag.csv`
- `addons/l10n_lk/data/form_vat001.xml`
- `addons/l10n_lk/data/form_wht001.xml`
- `addons/l10n_lk/data/template/account.account-lk.csv`
- `addons/l10n_lk/data/template/account.depreciation.model-lk.csv`
- `addons/l10n_lk/data/template/account.fiscal.position-lk.csv`
- `addons/l10n_lk/data/template/account.tax-lk.csv`
- `addons/l10n_lk/data/template/account.tax.group-lk.csv`
- `addons/l10n_lk/demo/demo_company.xml`
- `addons/l10n_lk/models/__init__.py`
- `addons/l10n_lk/models/account_move.py`
- `addons/l10n_lk/models/account_resequence.py`
- `addons/l10n_lk/models/res_company.py`
- `addons/l10n_lk/models/res_partner.py`
- `addons/l10n_lk/models/template_lk.py`
- `addons/l10n_lk/tests/__init__.py`
- `addons/l10n_lk/tests/test_lk_tax_invoice_sequence.py`
- `addons/l10n_lk/views/report_invoice.xml`
- `addons/l10n_lk/views/res_company_views.xml`
- `addons/l10n_lk/views/res_partner_views.xml`
