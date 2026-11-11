# Module: l10n_nz

- **Module ID:** MOD-287
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_nz`
- **Manifest:** `addons/l10n_nz/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

New Zealand Accounting Module
=============================

New Zealand accounting basic charts and localizations.

Also:
    - activates a number of regional currencies.
    - sets up New Zealand taxes.

**Scope evidence:** The module contains 15 files, including 7 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 4
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

- **Description:** 2 model declarations, 3 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_nz/models/account_move.py:5`, `addons/l10n_nz/models/template_nz.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 33 record/template/menu identifiers.
- **Evidence:** `addons/l10n_nz/demo/demo_company.xml:3`, `addons/l10n_nz/demo/demo_company.xml:17`, `addons/l10n_nz/data/account_tax_report_data.xml:3`, `addons/l10n_nz/data/account_tax_report_data.xml:10`, `addons/l10n_nz/data/account_tax_report_data.xml:16`, `addons/l10n_nz/data/account_tax_report_data.xml:21`, `addons/l10n_nz/data/account_tax_report_data.xml:25`, `addons/l10n_nz/data/account_tax_report_data.xml:32`, `addons/l10n_nz/data/account_tax_report_data.xml:36`, `addons/l10n_nz/data/account_tax_report_data.xml:43`, `addons/l10n_nz/data/account_tax_report_data.xml:48`, `addons/l10n_nz/data/account_tax_report_data.xml:53`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `base.partner_demo_company_nz`, `base.demo_company_nz`, `tax_report`, `tax_report_balance`, `tax_report_sale_and_income`, `tax_report_box5`, `tax_report_box5_tag`, `tax_report_box6`, `tax_report_box6_tag`, `tax_report_box7`, `tax_report_box8`, `tax_report_box9`, `tax_report_box9_tag`, `tax_report_box10`, `tax_report_purchases_and_expenses`, `tax_report_box11`, `tax_report_box11_tag`, `tax_report_box12`, `tax_report_box13`, `tax_report_box13_aggregation`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/l10n_nz/views/report_invoice.xml:3`, `addons/l10n_nz/views/report_invoice.xml:55`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_nz/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `account.move` (addons/l10n_nz/models/account_move.py:5); inherits `account.chart.template` (addons/l10n_nz/models/template_nz.py:6)
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
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_nz/__init__.py`
- `addons/l10n_nz/__manifest__.py`
- `addons/l10n_nz/data/account_tax_report_data.xml`
- `addons/l10n_nz/data/res_currency_data.xml`
- `addons/l10n_nz/data/template/account.account-nz.csv`
- `addons/l10n_nz/data/template/account.fiscal.position-nz.csv`
- `addons/l10n_nz/data/template/account.tax-nz.csv`
- `addons/l10n_nz/data/template/account.tax.group-nz.csv`
- `addons/l10n_nz/demo/demo_company.xml`
- `addons/l10n_nz/migrations/1.2/post-migrate.py`
- `addons/l10n_nz/migrations/1.2/pre-migrate.py`
- `addons/l10n_nz/models/__init__.py`
- `addons/l10n_nz/models/account_move.py`
- `addons/l10n_nz/models/template_nz.py`
- `addons/l10n_nz/views/report_invoice.xml`
