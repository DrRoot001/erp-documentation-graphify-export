# Module: l10n_hr

- **Module ID:** MOD-216
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_hr`
- **Manifest:** `addons/l10n_hr/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Croatian Chart of Accounts updated (RRIF ver.2021)

Sources:
https://www.rrif.hr/dok/preuzimanje/Bilanca-2016.pdf
https://www.rrif.hr/dok/preuzimanje/RRIF-RP2021.PDF
https://www.rrif.hr/dok/preuzimanje/RRIF-RP2021-ENG.PDF

**Scope evidence:** The module contains 13 files, including 4 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 3
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

- **Description:** 1 model declarations, 2 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_hr/models/template_hr.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 147 record/template/menu identifiers.
- **Evidence:** `addons/l10n_hr/demo/demo_company.xml:3`, `addons/l10n_hr/demo/demo_company.xml:15`, `addons/l10n_hr/demo/demo_company.xml:20`, `addons/l10n_hr/demo/demo_company.xml:27`, `addons/l10n_hr/data/account_tax_report_data.xml:3`, `addons/l10n_hr/data/account_tax_report_data.xml:11`, `addons/l10n_hr/data/account_tax_report_data.xml:16`, `addons/l10n_hr/data/account_tax_report_data.xml:23`, `addons/l10n_hr/data/account_tax_report_data.xml:29`, `addons/l10n_hr/data/account_tax_report_data.xml:34`, `addons/l10n_hr/data/account_tax_report_data.xml:41`, `addons/l10n_hr/data/account_tax_report_data.xml:47`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `base.partner_demo_company_hr`, `base.demo_company_hr`, `base.demo_bank_hr`, `base.partner_demo_customer_hr`, `tax_report`, `tax_report_tax_base`, `tax_report_tax_amount`, `tax_report_title_vat_calculation`, `tax_report_line_0_0_tag_column1`, `tax_report_line_0_0_tag_column2`, `tax_report_title_transactions0`, `tax_report_line_I_0_tag_column1`, `tax_report_line_I_1`, `tax_report_line_I_1_tag_column1`, `tax_report_line_I_2`, `tax_report_line_I_2_tag_column1`, `tax_report_line_I_3`, `tax_report_line_I_3_tag_column1`, `tax_report_line_I_4`, `tax_report_line_I_4_tag_column1`
- Menus: 1; representative evidence: `addons/l10n_hr/data/l10n_hr_chart_data.xml:3`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_hr/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `account.chart.template` (addons/l10n_hr/models/template_hr.py:6)
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

- `addons/l10n_hr/__init__.py`
- `addons/l10n_hr/__manifest__.py`
- `addons/l10n_hr/data/account_tax_report_data.xml`
- `addons/l10n_hr/data/l10n_hr_chart_data.xml`
- `addons/l10n_hr/data/template/account.account-hr.csv`
- `addons/l10n_hr/data/template/account.fiscal.position-hr.csv`
- `addons/l10n_hr/data/template/account.tax-hr.csv`
- `addons/l10n_hr/data/template/account.tax.group-hr.csv`
- `addons/l10n_hr/demo/demo_company.xml`
- `addons/l10n_hr/i18n/hr.po`
- `addons/l10n_hr/i18n/l10n_hr.pot`
- `addons/l10n_hr/models/__init__.py`
- `addons/l10n_hr/models/template_hr.py`
