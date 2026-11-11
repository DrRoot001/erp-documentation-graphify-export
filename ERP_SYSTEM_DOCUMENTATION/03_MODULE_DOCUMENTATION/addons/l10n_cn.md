# Module: l10n_cn

- **Module ID:** MOD-151
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_cn`
- **Manifest:** `addons/l10n_cn/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Includes the following data for the Chinese localization
========================================================

Account Type/科目类型

State Data/省份数据

    科目类型\会计科目表模板\增值税\辅助核算类别\管理会计凭证簿\财务会计凭证簿

    添加中文省份数据

    增加小企业会计科目表

    修改小企业会计科目表

    修改小企业会计税率

    增加大企业会计科目表

We added the option to print a voucher which will also
print the amount in words (special Chinese characters for numbers)
correctly when the cn2an library is installed. (e.g. with pip3 install cn2an)

**Scope evidence:** The module contains 36 files, including 15 Python, 11 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `account`.

## 2. Module structure

- Model/business logic files: 9
- Controller/API files: 0
- XML/data/view/template files: 11
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_cn/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 9 model declarations, 39 methods, 3 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_cn/models/res_config_settings.py:4`, `addons/l10n_cn/models/template_cn_common.py:6`, `addons/l10n_cn/models/template_cn.py:6`, `addons/l10n_cn/models/account_move.py:13`, `addons/l10n_cn/models/account_move_line.py:7`, `addons/l10n_cn/models/template_cn_large_bis.py:6`, `addons/l10n_cn/models/res_company.py:4`, `addons/l10n_cn/models/balance_deduction.py:5`, `addons/l10n_cn/wizard/account_move_reversal.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 11 XML files and 0 JavaScript/TypeScript files; static XML analysis found 3576 record/template/menu identifiers.
- **Evidence:** `addons/l10n_cn/demo/demo_company.xml:3`, `addons/l10n_cn/demo/demo_company.xml:16`, `addons/l10n_cn/demo/demo_company_asbe.xml:3`, `addons/l10n_cn/demo/demo_company_asbe.xml:16`, `addons/l10n_cn/data/account_tax_report_data.xml:5`, `addons/l10n_cn/data/account_tax_report_data.xml:12`, `addons/l10n_cn/data/account_tax_report_data.xml:18`, `addons/l10n_cn/data/account_tax_report_data.xml:24`, `addons/l10n_cn/data/account_tax_report_data.xml:32`, `addons/l10n_cn/data/account_tax_report_data.xml:38`, `addons/l10n_cn/data/account_tax_report_data.xml:44`, `addons/l10n_cn/data/account_tax_report_data.xml:50`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_cn/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_cn/views/account_report.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_cn/tests/test_balance_deduction.py`, `addons/l10n_cn/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 11; representative identifiers: `base.partner_demo_company_cn`, `base.demo_company_cn`, `base.partner_demo_asbe_company_cn`, `base.demo_asbe_company_cn`, `tax_report_main`, `tax_report_main_column_number0`, `tax_report_main_column_generaltax`, `tax_report_main_column_refunduponcollection`, `tax_report_main_line_ITEMS_0`, `tax_report_main_line_SALES`, `tax_report_main_line_SAT`, `tax_report_main_line_SAT_number0`, `tax_report_main_line_SAT_generaltax`, `tax_report_main_line_SAT_refunduponcollection`, `tax_report_main_line_SAT_STG`, `tax_report_main_line_SAT_STG_number0`, `tax_report_main_line_SAT_STG_generaltax`, `tax_report_main_line_SAT_STG_refunduponcollection`, `tax_report_main_line_SAT_STS`, `tax_report_main_line_SAT_STS_number0`
- Menus: 1; representative evidence: `addons/l10n_cn/views/balance_deduction_view.xml:86`
- Templates: 3; representative evidence: `addons/l10n_cn/views/report_voucher.xml:5`, `addons/l10n_cn/views/report_voucher.xml:15`, `addons/l10n_cn/views/report_voucher.xml:125`
- View/action field declarations: 17; representative evidence: `addons/l10n_cn/views/res_config_settings_views.xml:5`, `addons/l10n_cn/views/res_config_settings_views.xml:7`, `addons/l10n_cn/views/account_report.xml:7`, `addons/l10n_cn/views/account_move_view.xml:6`, `addons/l10n_cn/views/account_move_view.xml:8`, `addons/l10n_cn/views/account_move_view.xml:17`, `addons/l10n_cn/views/account_move_view.xml:19`, `addons/l10n_cn/views/account_move_line_view.xml:6`, `addons/l10n_cn/views/account_move_line_view.xml:7`, `addons/l10n_cn/views/balance_deduction_view.xml:6`, `addons/l10n_cn/views/balance_deduction_view.xml:7`, `addons/l10n_cn/views/balance_deduction_view.xml:33`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_cn/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/l10n_cn/views/account_report.xml`

## 7. Database interactions

- Model declarations: 9
- Representative model evidence: inherits `res.config.settings` (addons/l10n_cn/models/res_config_settings.py:4); inherits `account.chart.template` (addons/l10n_cn/models/template_cn_common.py:6); inherits `account.chart.template` (addons/l10n_cn/models/template_cn.py:6); inherits `account.move` (addons/l10n_cn/models/account_move.py:13); inherits `account.move.line` (addons/l10n_cn/models/account_move_line.py:7); inherits `account.chart.template` (addons/l10n_cn/models/template_cn_large_bis.py:6); inherits `res.company` (addons/l10n_cn/models/res_company.py:4); `l10n_cn.balance.deduction` (addons/l10n_cn/models/balance_deduction.py:5); inherits `account.move.reversal` (addons/l10n_cn/wizard/account_move_reversal.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `account`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_cn/__init__.py`
- `addons/l10n_cn/__manifest__.py`
- `addons/l10n_cn/data/account_tax_report_data.xml`
- `addons/l10n_cn/data/res_city_data.xml`
- `addons/l10n_cn/data/res_country_data.xml`
- `addons/l10n_cn/data/template/account.account-cn.csv`
- `addons/l10n_cn/data/template/account.account-cn_common.csv`
- `addons/l10n_cn/data/template/account.account-cn_large_bis.csv`
- `addons/l10n_cn/data/template/account.depreciation.model-cn_common.csv`
- `addons/l10n_cn/data/template/account.fiscal.position-cn_common.csv`
- `addons/l10n_cn/data/template/account.tax-cn_common.csv`
- `addons/l10n_cn/data/template/account.tax.group-cn_common.csv`
- `addons/l10n_cn/demo/demo_company.xml`
- `addons/l10n_cn/demo/demo_company_asbe.xml`
- `addons/l10n_cn/i18n/l10n_cn.pot`
- `addons/l10n_cn/i18n/zh_CN.po`
- `addons/l10n_cn/models/__init__.py`
- `addons/l10n_cn/models/account_move.py`
- `addons/l10n_cn/models/account_move_line.py`
- `addons/l10n_cn/models/balance_deduction.py`
- `addons/l10n_cn/models/res_company.py`
- `addons/l10n_cn/models/res_config_settings.py`
- `addons/l10n_cn/models/template_cn.py`
- `addons/l10n_cn/models/template_cn_common.py`
- `addons/l10n_cn/models/template_cn_large_bis.py`
- `addons/l10n_cn/security/ir.access.csv`
- `addons/l10n_cn/tests/__init__.py`
- `addons/l10n_cn/tests/test_balance_deduction.py`
- `addons/l10n_cn/views/account_move_line_view.xml`
- `addons/l10n_cn/views/account_move_view.xml`
- `addons/l10n_cn/views/account_report.xml`
- `addons/l10n_cn/views/balance_deduction_view.xml`
- `addons/l10n_cn/views/report_voucher.xml`
- `addons/l10n_cn/views/res_config_settings_views.xml`
- `addons/l10n_cn/wizard/__init__.py`
- `addons/l10n_cn/wizard/account_move_reversal.py`
