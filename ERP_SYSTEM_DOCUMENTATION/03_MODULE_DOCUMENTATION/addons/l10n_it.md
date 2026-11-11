# Module: l10n_it

- **Module ID:** MOD-240
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_it`
- **Manifest:** `addons/l10n_it/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Piano dei conti italiano di un'impresa generica.
================================================

Italian accounting chart and localization.

**Scope evidence:** The module contains 33 files, including 15 Python, 12 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 12
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

- **Description:** 5 model declarations, 11 methods, 1 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_it/demo/account_demo.py:12`, `addons/l10n_it/models/account_tax.py:6`, `addons/l10n_it/models/account_report.py:7`, `addons/l10n_it/models/account_move.py:6`, `addons/l10n_it/models/template_it.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 12 XML files and 0 JavaScript/TypeScript files; static XML analysis found 431 record/template/menu identifiers.
- **Evidence:** `addons/l10n_it/demo/demo_company.xml:3`, `addons/l10n_it/demo/demo_company.xml:16`, `addons/l10n_it/demo/demo_company.xml:21`, `addons/l10n_it/data/account_account_tag.xml:5`, `addons/l10n_it/data/account_account_tag.xml:10`, `addons/l10n_it/data/account_account_tag.xml:15`, `addons/l10n_it/data/account_account_tag.xml:20`, `addons/l10n_it/data/account_account_tag.xml:25`, `addons/l10n_it/data/account_account_tag.xml:30`, `addons/l10n_it/data/account_account_tag.xml:35`, `addons/l10n_it/data/account_account_tag.xml:40`, `addons/l10n_it/data/account_account_tag.xml:45`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 12; representative identifiers: `base.partner_demo_company_it`, `base.demo_company_it`, `base.demo_bank_it`, `account_tag_A_ATT`, `account_tag_B_ATT`, `account_tag_C_ATT`, `account_tag_D_ATT`, `account_tag_A_PASS`, `account_tag_B_PASS`, `account_tag_C_PASS`, `account_tag_D_PASS`, `account_tag_E_PASS`, `account_tag_RISCHI`, `account_tag_IMPEGNI`, `account_tag_BENI`, `account_tag_A_PL`, `account_tag_B_PL`, `account_tag_C_PL`, `account_tag_D_PL`, `account_tag_E_PL`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/l10n_it/views/account_tax_views.xml:6`, `addons/l10n_it/views/account_tax_views.xml:9`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_it/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `account.chart.template` (addons/l10n_it/demo/account_demo.py:12); inherits `account.tax` (addons/l10n_it/models/account_tax.py:6); inherits `account.report.expression` (addons/l10n_it/models/account_report.py:7); inherits `account.move` (addons/l10n_it/models/account_move.py:6); inherits `account.chart.template` (addons/l10n_it/models/template_it.py:6)
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

- `addons/l10n_it/__init__.py`
- `addons/l10n_it/__manifest__.py`
- `addons/l10n_it/data/account_account_tag.xml`
- `addons/l10n_it/data/tax_report/account_annual_tax_report_data.xml`
- `addons/l10n_it/data/tax_report/account_monthly_tax_report_data.xml`
- `addons/l10n_it/data/tax_report/account_withholding_report_data.xml`
- `addons/l10n_it/data/tax_report/annual_report_sections/va.xml`
- `addons/l10n_it/data/tax_report/annual_report_sections/ve.xml`
- `addons/l10n_it/data/tax_report/annual_report_sections/vf.xml`
- `addons/l10n_it/data/tax_report/annual_report_sections/vh.xml`
- `addons/l10n_it/data/tax_report/annual_report_sections/vj.xml`
- `addons/l10n_it/data/tax_report/annual_report_sections/vl.xml`
- `addons/l10n_it/data/template/account.account-it.csv`
- `addons/l10n_it/data/template/account.fiscal.position-it.csv`
- `addons/l10n_it/data/template/account.tax-it.csv`
- `addons/l10n_it/data/template/account.tax.group-it.csv`
- `addons/l10n_it/demo/__init__.py`
- `addons/l10n_it/demo/account_demo.py`
- `addons/l10n_it/demo/demo_company.xml`
- `addons/l10n_it/i18n/it.po`
- `addons/l10n_it/i18n/l10n_it.pot`
- `addons/l10n_it/migrations/0.10/pre-remove-report-expression.py`
- `addons/l10n_it/migrations/0.11/post-update_sp_taxes.py`
- `addons/l10n_it/migrations/0.6/end-migrate_update_taxes.py`
- `addons/l10n_it/migrations/0.7/post-map_carryover_to_new_report.py`
- `addons/l10n_it/migrations/0.9/post-migrate.py`
- `addons/l10n_it/migrations/15.0.0.3/post-migrate.py`
- `addons/l10n_it/models/__init__.py`
- `addons/l10n_it/models/account_move.py`
- `addons/l10n_it/models/account_report.py`
- `addons/l10n_it/models/account_tax.py`
- `addons/l10n_it/models/template_it.py`
- `addons/l10n_it/views/account_tax_views.xml`
