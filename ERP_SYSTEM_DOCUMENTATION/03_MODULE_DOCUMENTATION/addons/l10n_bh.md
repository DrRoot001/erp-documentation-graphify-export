# Module: l10n_bh

- **Module ID:** MOD-135
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_bh`
- **Manifest:** `addons/l10n_bh/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the base module to manage the accounting chart for Bahrain in Odoo.
===========================================================================
Bahrain accounting basic charts and localization.

Activates:
 - Chart of Accounts
 - Taxes
 - Tax reports
 - Fiscal Positions
 - States

**Scope evidence:** The module contains 17 files, including 7 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `l10n_gcc_invoice`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 4
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

- **Description:** 2 model declarations, 9 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_bh/models/template_bh.py:5`, `addons/l10n_bh/models/account_move.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 119 record/template/menu identifiers.
- **Evidence:** `addons/l10n_bh/demo/demo_company.xml:3`, `addons/l10n_bh/demo/demo_company.xml:15`, `addons/l10n_bh/demo/demo_company.xml:20`, `addons/l10n_bh/data/tax_report_full.xml:3`, `addons/l10n_bh/data/tax_report_full.xml:11`, `addons/l10n_bh/data/tax_report_full.xml:16`, `addons/l10n_bh/data/tax_report_full.xml:21`, `addons/l10n_bh/data/tax_report_full.xml:28`, `addons/l10n_bh/data/tax_report_full.xml:33`, `addons/l10n_bh/data/tax_report_full.xml:38`, `addons/l10n_bh/data/tax_report_full.xml:43`, `addons/l10n_bh/data/tax_report_full.xml:49`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_bh/tests/__init__.py`, `addons/l10n_bh/tests/test_account_move.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `partner_demo_company_bh`, `demo_company_bh`, `demo_bank_bh`, `l10n_bh_tax_report_full`, `l10n_bh_tax_report_full_base`, `l10n_bh_tax_report_full_adjustment`, `l10n_bh_tax_report_full_tax`, `l10n_bh_tax_report_full_vat_sale`, `l10n_bh_tax_report_full_1a`, `l10n_bh_tax_report_full_1a_base`, `l10n_bh_tax_report_full_1a_adjustment`, `l10n_bh_tax_report_full_1a_tax`, `l10n_bh_tax_report_full_2`, `l10n_bh_tax_report_full_2_base`, `l10n_bh_tax_report_full_2_adjustment`, `l10n_bh_tax_report_full_3`, `l10n_bh_tax_report_full_3_base`, `l10n_bh_tax_report_full_3_adjustment`, `l10n_bh_tax_report_full_4`, `l10n_bh_tax_report_full_4_base`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/l10n_bh/views/report_invoice_templates.xml:2`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_bh/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `account.chart.template` (addons/l10n_bh/models/template_bh.py:5); inherits `account.move` (addons/l10n_bh/models/account_move.py:4)
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
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_bh/__init__.py`
- `addons/l10n_bh/__manifest__.py`
- `addons/l10n_bh/data/tax_report_full.xml`
- `addons/l10n_bh/data/tax_report_simplified.xml`
- `addons/l10n_bh/data/template/account.account-bh.csv`
- `addons/l10n_bh/data/template/account.fiscal.position-bh.csv`
- `addons/l10n_bh/data/template/account.tax-bh.csv`
- `addons/l10n_bh/data/template/account.tax.group-bh.csv`
- `addons/l10n_bh/demo/demo_company.xml`
- `addons/l10n_bh/i18n/ar.po`
- `addons/l10n_bh/i18n/l10n_bh.pot`
- `addons/l10n_bh/models/__init__.py`
- `addons/l10n_bh/models/account_move.py`
- `addons/l10n_bh/models/template_bh.py`
- `addons/l10n_bh/tests/__init__.py`
- `addons/l10n_bh/tests/test_account_move.py`
- `addons/l10n_bh/views/report_invoice_templates.xml`
