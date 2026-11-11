# Module: l10n_hu

- **Module ID:** MOD-219
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_hu`
- **Manifest:** `addons/l10n_hu/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Accounting chart and localization for Hungary

**Scope evidence:** The module contains 15 files, including 7 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

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

- **Description:** 3 model declarations, 6 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/l10n_hu/models/template_hu.py:6`, `addons/l10n_hu/models/res_partner.py:4`, `addons/l10n_hu/models/account_move.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 77 record/template/menu identifiers.
- **Evidence:** `addons/l10n_hu/demo/demo_company.xml:3`, `addons/l10n_hu/demo/demo_company.xml:16`, `addons/l10n_hu/demo/demo_company.xml:21`, `addons/l10n_hu/data/account_tax_report_data.xml:3`, `addons/l10n_hu/data/account_tax_report_data.xml:11`, `addons/l10n_hu/data/account_tax_report_data.xml:18`, `addons/l10n_hu/data/account_tax_report_data.xml:24`, `addons/l10n_hu/data/account_tax_report_data.xml:30`, `addons/l10n_hu/data/account_tax_report_data.xml:35`, `addons/l10n_hu/data/account_tax_report_data.xml:42`, `addons/l10n_hu/data/account_tax_report_data.xml:47`, `addons/l10n_hu/data/account_tax_report_data.xml:59`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `base.partner_demo_company_hu`, `base.demo_company_hu`, `base.demo_bank_hu`, `tax_report`, `tax_report_balance`, `tax_report_alap`, `tax_report_base_pay`, `tax_report_alap_fiz_export`, `tax_report_alap_fiz_export_tag`, `tax_report_alap_fiz_eu`, `tax_report_alap_fiz_eu_tag`, `a60s_services_balance`, `a60s_goods_balance`, `a60g_balance`, `a60b_balance`, `a60k_balance`, `a60r_balance`, `a60c_balance`, `a60v_balance`, `tax_report_alap_fiz_targyi`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_hu/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `account.chart.template` (addons/l10n_hu/models/template_hu.py:6); inherits `res.partner` (addons/l10n_hu/models/res_partner.py:4); inherits `account.move` (addons/l10n_hu/models/account_move.py:6)
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

- `addons/l10n_hu/__init__.py`
- `addons/l10n_hu/__manifest__.py`
- `addons/l10n_hu/data/account_tax_report_data.xml`
- `addons/l10n_hu/data/template/account.account-hu.csv`
- `addons/l10n_hu/data/template/account.fiscal.position-hu.csv`
- `addons/l10n_hu/data/template/account.tax-hu.csv`
- `addons/l10n_hu/data/template/account.tax.group-hu.csv`
- `addons/l10n_hu/demo/demo_company.xml`
- `addons/l10n_hu/i18n/hu.po`
- `addons/l10n_hu/i18n/l10n_hu.pot`
- `addons/l10n_hu/migrations/3.1/end-migrate_update_taxes.py`
- `addons/l10n_hu/models/__init__.py`
- `addons/l10n_hu/models/account_move.py`
- `addons/l10n_hu/models/res_partner.py`
- `addons/l10n_hu/models/template_hu.py`
