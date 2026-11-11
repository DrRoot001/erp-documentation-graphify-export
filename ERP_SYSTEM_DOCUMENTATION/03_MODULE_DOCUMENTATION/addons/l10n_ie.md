# Module: l10n_ie

- **Module ID:** MOD-225
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ie`
- **Manifest:** `addons/l10n_ie/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the base module to manage the accounting chart for Republic of Ireland in Odoo.

**Scope evidence:** The module contains 14 files, including 7 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 3
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

- **Description:** 3 model declarations, 5 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_ie/models/account_journal.py:4`, `addons/l10n_ie/models/account_chart_template.py:4`, `addons/l10n_ie/models/template_ie.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 25 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ie/demo/demo_company.xml:3`, `addons/l10n_ie/demo/demo_company.xml:16`, `addons/l10n_ie/demo/demo_company.xml:21`, `addons/l10n_ie/data/tax_report-ie.xml:3`, `addons/l10n_ie/data/tax_report-ie.xml:10`, `addons/l10n_ie/data/tax_report-ie.xml:16`, `addons/l10n_ie/data/tax_report-ie.xml:20`, `addons/l10n_ie/data/tax_report-ie.xml:27`, `addons/l10n_ie/data/tax_report-ie.xml:31`, `addons/l10n_ie/data/tax_report-ie.xml:38`, `addons/l10n_ie/data/tax_report-ie.xml:41`, `addons/l10n_ie/data/tax_report-ie.xml:49`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `base.partner_demo_company_ie`, `base.demo_company_ie`, `base.demo_bank_ie`, `l10n_ie_tr`, `l10n_ie_tr_balance`, `l10n_ie_tr_T1`, `l10n_ie_tr_T1_tag`, `l10n_ie_tr_T2`, `l10n_ie_tr_T2_tag`, `l10n_ie_tr_T3`, `l10n_ie_tr_T3_aggregation`, `l10n_ie_tr_T4`, `l10n_ie_tr_T4_aggregation`, `l10n_ie_tr_E1`, `l10n_ie_tr_E1_tag`, `l10n_ie_tr_E1_goods_tag`, `l10n_ie_tr_E1_triangular_tag`, `l10n_ie_tr_E2`, `l10n_ie_tr_E2_tag`, `l10n_ie_tr_ES1`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ie/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `account.journal` (addons/l10n_ie/models/account_journal.py:4); inherits `account.chart.template` (addons/l10n_ie/models/account_chart_template.py:4); inherits `account.chart.template` (addons/l10n_ie/models/template_ie.py:6)
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

- `addons/l10n_ie/__init__.py`
- `addons/l10n_ie/__manifest__.py`
- `addons/l10n_ie/data/account.account.tag.csv`
- `addons/l10n_ie/data/tax_report-ie.xml`
- `addons/l10n_ie/data/template/account.account-ie.csv`
- `addons/l10n_ie/data/template/account.fiscal.position-ie.csv`
- `addons/l10n_ie/data/template/account.tax-ie.csv`
- `addons/l10n_ie/data/template/account.tax.group-ie.csv`
- `addons/l10n_ie/demo/demo_company.xml`
- `addons/l10n_ie/migrations/2.1/end-migrate.py`
- `addons/l10n_ie/models/__init__.py`
- `addons/l10n_ie/models/account_chart_template.py`
- `addons/l10n_ie/models/account_journal.py`
- `addons/l10n_ie/models/template_ie.py`
