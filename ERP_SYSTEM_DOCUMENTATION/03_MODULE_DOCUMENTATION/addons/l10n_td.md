# Module: l10n_td

- **Module ID:** MOD-321
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_td`
- **Manifest:** `addons/l10n_td/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module implements the tax for Tchad.
=================================================================

The Chart of Accounts is from SYSCOHADA.

**Scope evidence:** The module contains 16 files, including 5 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_syscohada`, `account`.

## 2. Module structure

- Model/business logic files: 2
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

- **Description:** 2 model declarations, 6 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_td/models/template_td_syscebnl.py:5`, `addons/l10n_td/models/template_td.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 35 record/template/menu identifiers.
- **Evidence:** `addons/l10n_td/demo/demo_company.xml:3`, `addons/l10n_td/demo/demo_company.xml:15`, `addons/l10n_td/data/account_tax_report_data.xml:3`, `addons/l10n_td/data/account_tax_report_data.xml:11`, `addons/l10n_td/data/account_tax_report_data.xml:16`, `addons/l10n_td/data/account_tax_report_data.xml:23`, `addons/l10n_td/data/account_tax_report_data.xml:29`, `addons/l10n_td/data/account_tax_report_data.xml:34`, `addons/l10n_td/data/account_tax_report_data.xml:41`, `addons/l10n_td/data/account_tax_report_data.xml:46`, `addons/l10n_td/data/account_tax_report_data.xml:51`, `addons/l10n_td/data/account_tax_report_data.xml:58`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `base.partner_demo_company_td`, `base.demo_company_td`, `account_tax_report_td`, `account_tax_report_td_balance`, `account_tax_report_td_tax`, `account_tax_report_line_td_sales`, `account_tax_report_line_td_sales_base_tag`, `account_tax_report_line_td_sales_tax_tag`, `account_tax_report_line_sales_18`, `account_tax_report_line_sales_18_base_tag`, `account_tax_report_line_sales_18_tax_tag`, `account_tax_report_line_sales_9`, `account_tax_report_line_sales_9_base_tag`, `account_tax_report_line_sales_9_tax_tag`, `account_tax_report_line_sales_export`, `account_tax_report_line_sales_export_base_tag`, `account_tax_report_line_sales_exempt`, `account_tax_report_line_sales_exempt_base_tag`, `account_tax_report_line_td_purchases`, `account_tax_report_line_td_purchases_base_tag`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_td/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `account.chart.template` (addons/l10n_td/models/template_td_syscebnl.py:5); inherits `account.chart.template` (addons/l10n_td/models/template_td.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_syscohada`, `account`
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

- `addons/l10n_td/__init__.py`
- `addons/l10n_td/__manifest__.py`
- `addons/l10n_td/data/account_tax_report_data.xml`
- `addons/l10n_td/data/template/account.fiscal.position-td.csv`
- `addons/l10n_td/data/template/account.fiscal.position-td_syscebnl.csv`
- `addons/l10n_td/data/template/account.tax-td.csv`
- `addons/l10n_td/data/template/account.tax-td_syscebnl.csv`
- `addons/l10n_td/data/template/account.tax.group-td.csv`
- `addons/l10n_td/data/template/account.tax.group-td_syscebnl.csv`
- `addons/l10n_td/demo/demo_company.xml`
- `addons/l10n_td/i18n/ar.po`
- `addons/l10n_td/i18n/fr.po`
- `addons/l10n_td/i18n/l10n_td.pot`
- `addons/l10n_td/models/__init__.py`
- `addons/l10n_td/models/template_td.py`
- `addons/l10n_td/models/template_td_syscebnl.py`
