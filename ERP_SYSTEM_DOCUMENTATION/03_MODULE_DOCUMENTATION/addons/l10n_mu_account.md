# Module: l10n_mu_account

- **Module ID:** MOD-276
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_mu_account`
- **Manifest:** `addons/l10n_mu_account/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the base module to manage the accounting chart for the Republic of Mauritius in Odoo.
==============================================================================================
    - Chart of accounts
    - Taxes
    - Fiscal positions
    - Default settings

**Scope evidence:** The module contains 15 files, including 6 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 3
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

- **Description:** 3 model declarations, 5 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_mu_account/models/base_document_layout.py:6`, `addons/l10n_mu_account/models/template_mu.py:6`, `addons/l10n_mu_account/models/account_move.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 90 record/template/menu identifiers.
- **Evidence:** `addons/l10n_mu_account/demo/demo_company.xml:3`, `addons/l10n_mu_account/demo/demo_company.xml:15`, `addons/l10n_mu_account/demo/demo_company.xml:20`, `addons/l10n_mu_account/data/tax_report-mu.xml:3`, `addons/l10n_mu_account/data/tax_report-mu.xml:10`, `addons/l10n_mu_account/data/tax_report-mu.xml:15`, `addons/l10n_mu_account/data/tax_report-mu.xml:19`, `addons/l10n_mu_account/data/tax_report-mu.xml:25`, `addons/l10n_mu_account/data/tax_report-mu.xml:29`, `addons/l10n_mu_account/data/tax_report-mu.xml:32`, `addons/l10n_mu_account/data/tax_report-mu.xml:36`, `addons/l10n_mu_account/data/tax_report-mu.xml:43`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `partner_demo_company_mu`, `demo_company_mu`, `demo_bank_mu`, `mu_tax_report`, `mu_tr_col_percent`, `mu_tr_col_value`, `mu_tr_col_vat`, `mu_tr_output`, `mu_tr_T1`, `mu_tr_T1_1`, `mu_tr_T1_1_value`, `mu_tr_T1_2`, `mu_tr_T1_2_value`, `mu_tr_T1_3`, `mu_tr_T1_3_value`, `mu_tr_T1_4`, `mu_tr_T1_4_value`, `mu_tr_T1_4_vat`, `mu_tr_T2`, `mu_tr_T2_vat`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/l10n_mu_account/views/report_invoice.xml:3`, `addons/l10n_mu_account/views/report_invoice.xml:44`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_mu_account/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `base.document.layout` (addons/l10n_mu_account/models/base_document_layout.py:6); inherits `account.chart.template` (addons/l10n_mu_account/models/template_mu.py:6); inherits `account.move` (addons/l10n_mu_account/models/account_move.py:4)
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

- `addons/l10n_mu_account/__init__.py`
- `addons/l10n_mu_account/__manifest__.py`
- `addons/l10n_mu_account/data/tax_report-mu.xml`
- `addons/l10n_mu_account/data/template/account.account-mu.csv`
- `addons/l10n_mu_account/data/template/account.fiscal.position-mu.csv`
- `addons/l10n_mu_account/data/template/account.tax-mu.csv`
- `addons/l10n_mu_account/data/template/account.tax.group-mu.csv`
- `addons/l10n_mu_account/demo/demo_company.xml`
- `addons/l10n_mu_account/i18n/fr.po`
- `addons/l10n_mu_account/i18n/l10n_mu_account.pot`
- `addons/l10n_mu_account/models/__init__.py`
- `addons/l10n_mu_account/models/account_move.py`
- `addons/l10n_mu_account/models/base_document_layout.py`
- `addons/l10n_mu_account/models/template_mu.py`
- `addons/l10n_mu_account/views/report_invoice.xml`
