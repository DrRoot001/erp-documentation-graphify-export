# Module: l10n_pt

- **Module ID:** MOD-301
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_pt`
- **Manifest:** `addons/l10n_pt/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Portugal - Accounting

**Scope evidence:** The module contains 17 files, including 8 Python, 2 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `account`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 1
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 11 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_pt/models/account_tax.py:4`, `addons/l10n_pt/models/account_account.py:4`, `addons/l10n_pt/models/template_pt.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 1 JavaScript/TypeScript files; static XML analysis found 103 record/template/menu identifiers.
- **Evidence:** `addons/l10n_pt/demo/demo_company.xml:3`, `addons/l10n_pt/demo/demo_company.xml:17`, `addons/l10n_pt/demo/demo_company.xml:22`, `addons/l10n_pt/data/account_tax_report.xml:3`, `addons/l10n_pt/data/account_tax_report.xml:11`, `addons/l10n_pt/data/account_tax_report.xml:18`, `addons/l10n_pt/data/account_tax_report.xml:23`, `addons/l10n_pt/data/account_tax_report.xml:27`, `addons/l10n_pt/data/account_tax_report.xml:32`, `addons/l10n_pt/data/account_tax_report.xml:39`, `addons/l10n_pt/data/account_tax_report.xml:44`, `addons/l10n_pt/data/account_tax_report.xml:51`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_pt/tests/test_taxes_tax_totals_summary.py`, `addons/l10n_pt/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `base.partner_demo_company_pt`, `base.demo_company_pt`, `base.demo_bank_pt`, `tax_report_pt`, `tax_report_balance`, `trp_base`, `trp_base_section_1`, `trp_base_1`, `trp_base_1_tag`, `trp_base_5`, `trp_base_5_tag`, `trp_base_3`, `trp_base_3_tag`, `trp_base_7`, `trp_base_7_tag`, `trp_base_8`, `trp_base_8_tag`, `trp_base_9`, `trp_base_9_tag`, `trp_base_10`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 1; representative files: `addons/l10n_pt/static/src/helpers/account_tax.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_pt/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `account.tax` (addons/l10n_pt/models/account_tax.py:4); inherits `account.account` (addons/l10n_pt/models/account_account.py:4); inherits `account.chart.template` (addons/l10n_pt/models/template_pt.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `account`, `account_edi_ubl_cii`
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

- `addons/l10n_pt/__init__.py`
- `addons/l10n_pt/__manifest__.py`
- `addons/l10n_pt/data/account_tax_report.xml`
- `addons/l10n_pt/data/template/account.account-pt.csv`
- `addons/l10n_pt/data/template/account.fiscal.position-pt.csv`
- `addons/l10n_pt/data/template/account.tax-pt.csv`
- `addons/l10n_pt/data/template/account.tax.group-pt.csv`
- `addons/l10n_pt/demo/demo_company.xml`
- `addons/l10n_pt/i18n/l10n_pt.pot`
- `addons/l10n_pt/i18n/pt.po`
- `addons/l10n_pt/models/__init__.py`
- `addons/l10n_pt/models/account_account.py`
- `addons/l10n_pt/models/account_tax.py`
- `addons/l10n_pt/models/template_pt.py`
- `addons/l10n_pt/static/src/helpers/account_tax.js`
- `addons/l10n_pt/tests/__init__.py`
- `addons/l10n_pt/tests/test_taxes_tax_totals_summary.py`
