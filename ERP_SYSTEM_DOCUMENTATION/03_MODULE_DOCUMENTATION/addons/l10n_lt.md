# Module: l10n_lt

- **Module ID:** MOD-263
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_lt`
- **Manifest:** `addons/l10n_lt/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Chart of Accounts (COA) Template for Lithuania's Accounting.

This module also includes:

* List of available banks in Lithuania.
* Tax groups.
* Most common Lithuanian Taxes.
* Fiscal positions.
* Account Tags.

**Scope evidence:** The module contains 16 files, including 6 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 3
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

- **Description:** 3 model declarations, 5 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_lt/models/account_journal.py:4`, `addons/l10n_lt/models/account_tax.py:4`, `addons/l10n_lt/models/template_lt.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 154 record/template/menu identifiers.
- **Evidence:** `addons/l10n_lt/demo/demo_company.xml:3`, `addons/l10n_lt/demo/demo_company.xml:16`, `addons/l10n_lt/demo/demo_company.xml:21`, `addons/l10n_lt/data/tax_report_data.xml:3`, `addons/l10n_lt/data/tax_report_data.xml:11`, `addons/l10n_lt/data/tax_report_data.xml:18`, `addons/l10n_lt/data/tax_report_data.xml:23`, `addons/l10n_lt/data/tax_report_data.xml:28`, `addons/l10n_lt/data/tax_report_data.xml:35`, `addons/l10n_lt/data/tax_report_data.xml:40`, `addons/l10n_lt/data/tax_report_data.xml:47`, `addons/l10n_lt/data/tax_report_data.xml:52`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `base.partner_demo_company_lt`, `base.demo_company_lt`, `base.demo_bank_lt`, `lt_tax_report`, `lt_tax_report_balance`, `lt_tax_report_line_1`, `lt_tax_report_line_11`, `tax_report_line_11_tag`, `lt_tax_report_line_12`, `tax_report_line_12_tag`, `lt_tax_report_line_13`, `tax_report_line_13_tag`, `lt_tax_report_line_14`, `tax_report_line_14_tag`, `lt_tax_report_line_15`, `tax_report_line_15_tag`, `lt_tax_report_line_16`, `tax_report_line_16_tag`, `lt_tax_report_line_17`, `tax_report_line_17_tag`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/l10n_lt/views/account_tax.xml:5`, `addons/l10n_lt/views/account_tax.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_lt/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `account.journal` (addons/l10n_lt/models/account_journal.py:4); inherits `account.tax` (addons/l10n_lt/models/account_tax.py:4); inherits `account.chart.template` (addons/l10n_lt/models/template_lt.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `account_edi_ubl_cii`
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

- `addons/l10n_lt/__init__.py`
- `addons/l10n_lt/__manifest__.py`
- `addons/l10n_lt/data/account_account_tag_data.xml`
- `addons/l10n_lt/data/tax_report_data.xml`
- `addons/l10n_lt/data/template/account.account-lt.csv`
- `addons/l10n_lt/data/template/account.fiscal.position-lt.csv`
- `addons/l10n_lt/data/template/account.tax-lt.csv`
- `addons/l10n_lt/data/template/account.tax.group-lt.csv`
- `addons/l10n_lt/demo/demo_company.xml`
- `addons/l10n_lt/i18n/l10n_lt.pot`
- `addons/l10n_lt/i18n/lt.po`
- `addons/l10n_lt/models/__init__.py`
- `addons/l10n_lt/models/account_journal.py`
- `addons/l10n_lt/models/account_tax.py`
- `addons/l10n_lt/models/template_lt.py`
- `addons/l10n_lt/views/account_tax.xml`
