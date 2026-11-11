# Module: l10n_jp

- **Module ID:** MOD-248
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_jp`
- **Manifest:** `addons/l10n_jp/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Overview:
---------

* Chart of Accounts and Taxes template for companies in Japan.
* This probably does not cover all the necessary accounts for a company. You are expected to add/delete/modify accounts based on this template.

Note:
-----

* Fiscal positions '内税' and '外税' have been added to handle special requirements which might arise from POS implementation. [1]  Under normal circumstances, you might not need to use those at all.

[1] See https://github.com/odoo/odoo/pull/6470 for detail.

**Scope evidence:** The module contains 25 files, including 5 Python, 12 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 1
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

- **Description:** 1 model declarations, 4 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_jp/models/template_jp.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 12 XML files and 0 JavaScript/TypeScript files; static XML analysis found 1484 record/template/menu identifiers.
- **Evidence:** `addons/l10n_jp/demo/demo_company.xml:3`, `addons/l10n_jp/demo/demo_company.xml:16`, `addons/l10n_jp/data/account_report_jct_accumulation_schedule_2_3.xml:3`, `addons/l10n_jp/data/account_report_jct_accumulation_schedule_2_3.xml:9`, `addons/l10n_jp/data/account_report_jct_accumulation_schedule_2_3.xml:14`, `addons/l10n_jp/data/account_report_jct_accumulation_schedule_2_3.xml:19`, `addons/l10n_jp/data/account_report_jct_accumulation_schedule_2_3.xml:26`, `addons/l10n_jp/data/account_report_jct_accumulation_schedule_2_3.xml:33`, `addons/l10n_jp/data/account_report_jct_accumulation_schedule_2_3.xml:38`, `addons/l10n_jp/data/account_report_jct_accumulation_schedule_2_3.xml:43`, `addons/l10n_jp/data/account_report_jct_accumulation_schedule_2_3.xml:50`, `addons/l10n_jp/data/account_report_jct_accumulation_schedule_2_3.xml:57`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 12; representative identifiers: `base.partner_demo_company_jp`, `base.demo_company_jp`, `l10n_jp_schedule_2_3_accumulation`, `l10n_jp_schedule_2_3_accumulation_col_balance_a`, `l10n_jp_schedule_2_3_accumulation_col_balance_b`, `l10n_jp_schedule_2_3_accumulation_col_balance_c`, `l10n_jp_schedule_2_3_accumulation_acc_s2_3_1`, `l10n_jp_schedule_2_3_accumulation_acc_s2_3_1_balance_a`, `l10n_jp_schedule_2_3_accumulation_acc_s2_3_1_balance_b`, `l10n_jp_schedule_2_3_accumulation_acc_s2_3_1_balance_c`, `l10n_jp_schedule_2_3_accumulation_acc_s2_3_2`, `l10n_jp_schedule_2_3_accumulation_acc_s2_3_2_balance_c`, `l10n_jp_schedule_2_3_accumulation_acc_s2_3_3`, `l10n_jp_schedule_2_3_accumulation_acc_s2_3_3_balance_c`, `l10n_jp_schedule_2_3_accumulation_acc_s2_3_4`, `l10n_jp_schedule_2_3_accumulation_acc_s2_3_4_balance_c`, `l10n_jp_schedule_2_3_accumulation_acc_s2_3_5`, `l10n_jp_schedule_2_3_accumulation_acc_s2_3_5_balance_c`, `l10n_jp_schedule_2_3_accumulation_acc_s2_3_6`, `l10n_jp_schedule_2_3_accumulation_acc_s2_3_6_balance_c`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_jp/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `account.chart.template` (addons/l10n_jp/models/template_jp.py:5)
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

- `addons/l10n_jp/__init__.py`
- `addons/l10n_jp/__manifest__.py`
- `addons/l10n_jp/data/account.account.tag.csv`
- `addons/l10n_jp/data/account_report_jct_accumulation_form.xml`
- `addons/l10n_jp/data/account_report_jct_accumulation_schedule_1_3.xml`
- `addons/l10n_jp/data/account_report_jct_accumulation_schedule_2_3.xml`
- `addons/l10n_jp/data/account_report_jct_accumulation_schedule_4_3.xml`
- `addons/l10n_jp/data/account_report_jct_accumulation_schedule_5_3.xml`
- `addons/l10n_jp/data/account_report_jct_deduction_form.xml`
- `addons/l10n_jp/data/account_report_jct_deduction_schedule_1_3.xml`
- `addons/l10n_jp/data/account_report_jct_deduction_schedule_2_3.xml`
- `addons/l10n_jp/data/account_report_jct_deduction_schedule_4_3.xml`
- `addons/l10n_jp/data/account_report_jct_deduction_schedule_5_3.xml`
- `addons/l10n_jp/data/account_report_jct_return.xml`
- `addons/l10n_jp/data/template/account.account-jp.csv`
- `addons/l10n_jp/data/template/account.depreciation.model-jp.csv`
- `addons/l10n_jp/data/template/account.fiscal.position-jp.csv`
- `addons/l10n_jp/data/template/account.tax-jp.csv`
- `addons/l10n_jp/data/template/account.tax.group-jp.csv`
- `addons/l10n_jp/demo/demo_company.xml`
- `addons/l10n_jp/i18n/ja.po`
- `addons/l10n_jp/i18n/l10n_jp.pot`
- `addons/l10n_jp/migrations/2.3/pre-migrate.py`
- `addons/l10n_jp/models/__init__.py`
- `addons/l10n_jp/models/template_jp.py`
