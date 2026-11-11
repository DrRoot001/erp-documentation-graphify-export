# Module: l10n_la

- **Module ID:** MOD-258
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_la`
- **Manifest:** `addons/l10n_la/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Chart of accounts, VAT taxes and monthly VAT return for Laos

**Manifest description:**

Chart of Accounts for Laos.
===========================

Chart of accounts for non-public-interest entities, as set by the Ministry of Finance
Decision No. 0369 of 4 February 2020.

**Scope evidence:** The module contains 13 files, including 4 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 2
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

- **Description:** 1 model declarations, 5 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_la/models/template_la.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 82 record/template/menu identifiers.
- **Evidence:** `addons/l10n_la/demo/demo_company.xml:3`, `addons/l10n_la/demo/demo_company.xml:12`, `addons/l10n_la/data/account_tax_report_data.xml:4`, `addons/l10n_la/data/account_tax_report_data.xml:14`, `addons/l10n_la/data/account_tax_report_data.xml:20`, `addons/l10n_la/data/account_tax_report_data.xml:25`, `addons/l10n_la/data/account_tax_report_data.xml:31`, `addons/l10n_la/data/account_tax_report_data.xml:38`, `addons/l10n_la/data/account_tax_report_data.xml:43`, `addons/l10n_la/data/account_tax_report_data.xml:49`, `addons/l10n_la/data/account_tax_report_data.xml:54`, `addons/l10n_la/data/account_tax_report_data.xml:61`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `partner_demo_company_la`, `demo_company_la`, `l10n_la_tax_report`, `l10n_la_tax_report_column_cell_base`, `l10n_la_tax_report_column_base`, `l10n_la_tax_report_column_cell_tax`, `l10n_la_tax_report_column_tax`, `l10n_la_tax_report_section_a`, `l10n_la_tax_report_la_01`, `l10n_la_tax_report_la_01_cell_base`, `l10n_la_tax_report_la_01_base`, `l10n_la_tax_report_la_02`, `l10n_la_tax_report_la_02_cell_base`, `l10n_la_tax_report_la_02_base`, `l10n_la_tax_report_la_03`, `l10n_la_tax_report_la_03_cell_base`, `l10n_la_tax_report_la_03_base`, `l10n_la_tax_report_la_04_06`, `l10n_la_tax_report_la_04_06_cell_base`, `l10n_la_tax_report_la_04_06_base`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_la/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `account.chart.template` (addons/l10n_la/models/template_la.py:6)
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

- `addons/l10n_la/__init__.py`
- `addons/l10n_la/__manifest__.py`
- `addons/l10n_la/data/account_tax_report_data.xml`
- `addons/l10n_la/data/template/account.account-la.csv`
- `addons/l10n_la/data/template/account.depreciation.model-la.csv`
- `addons/l10n_la/data/template/account.fiscal.position-la.csv`
- `addons/l10n_la/data/template/account.tax-la.csv`
- `addons/l10n_la/data/template/account.tax.group-la.csv`
- `addons/l10n_la/demo/demo_company.xml`
- `addons/l10n_la/i18n/l10n_la.pot`
- `addons/l10n_la/i18n/lo.po`
- `addons/l10n_la/models/__init__.py`
- `addons/l10n_la/models/template_la.py`
