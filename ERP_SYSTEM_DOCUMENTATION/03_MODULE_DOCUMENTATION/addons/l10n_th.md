# Module: l10n_th

- **Module ID:** MOD-324
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_th`
- **Manifest:** `addons/l10n_th/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Chart of Accounts for Thailand.
===============================

Thai accounting chart and localization.

**Scope evidence:** The module contains 47 files, including 25 Python, 14 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account_qr_code_emv`, `account`, `l10n_account_withholding_tax`.

## 2. Module structure

- Model/business logic files: 12
- Controller/API files: 2
- XML/data/view/template files: 14
- Browser asset files: 0
- Security files: 1
- Test files: 7
- Scheduled/automation evidence files: 1
- Reporting evidence files: 4

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_th/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 12 model declarations, 72 methods, 1 constraint handlers, 2 onchange handlers, and 7 dependency declarations.
- **Evidence:** `addons/l10n_th/models/res_partner.py:6`, `addons/l10n_th/models/account_partial_reconcile.py:4`, `addons/l10n_th/models/res_bank.py:8`, `addons/l10n_th/models/account_payment.py:7`, `addons/l10n_th/models/account_tax.py:5`, `addons/l10n_th/models/l10n_th_tax_invoice.py:4`, `addons/l10n_th/models/template_th.py:6`, `addons/l10n_th/models/account_move.py:6`, `addons/l10n_th/models/res_company.py:4`, `addons/l10n_th/models/res_company.py:13`, `addons/l10n_th/wizards/account_payment_register.py:5`, `addons/l10n_th/report/report_tawi.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/l10n_th/controllers/download_tawi_reports.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 14 XML files and 0 JavaScript/TypeScript files; static XML analysis found 66 record/template/menu identifiers.
- **Evidence:** `addons/l10n_th/demo/demo_company.xml:3`, `addons/l10n_th/demo/demo_company.xml:16`, `addons/l10n_th/wizards/account_payment_register_views.xml:3`, `addons/l10n_th/report/report_tawi.xml:393`, `addons/l10n_th/report/report_tawi.xml:3`, `addons/l10n_th/report/report_tawi.xml:357`, `addons/l10n_th/report/report_tawi.xml:376`, `addons/l10n_th/report/report_tawi.xml:385`, `addons/l10n_th/data/account_tax_report_data.xml:3`, `addons/l10n_th/data/account_tax_report_data.xml:11`, `addons/l10n_th/data/account_tax_report_data.xml:18`, `addons/l10n_th/data/account_tax_report_data.xml:23`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_th/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_th/views/account_payment_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 4 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_th/report/report_tawi.xml`, `addons/l10n_th/views/report_invoice.xml`, `addons/l10n_th/tests/test_l10n_th_tax_invoice.py`, `addons/l10n_th/tests/test_credit_debit_note_pdf_report.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 7 test files are present.
- **Evidence:** `addons/l10n_th/tests/test_l10n_th_emv_qr.py`, `addons/l10n_th/tests/test_l10n_th_tax_invoice.py`, `addons/l10n_th/tests/test_wth_payment.py`, `addons/l10n_th/tests/__init__.py`, `addons/l10n_th/tests/test_res_partner.py`, `addons/l10n_th/tests/test_fiscal_position.py`, `addons/l10n_th/tests/test_credit_debit_note_pdf_report.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 14; representative identifiers: `base.partner_demo_company_th`, `base.demo_company_th`, `view_account_payment_register_form_inherit_l10n_th`, `action_report_50_tawi`, `report_50_tawi_document`, `tawi_square`, `tickbox_with_desc`, `report_50_tawi`, `tax_report`, `tax_report_balance`, `tax_report_out_tax_title`, `tax_report_out_tax_sale`, `tax_report_out_tax_sale_tag`, `tax_report_out_tax_sale_tag_pos`, `tax_report_out_tax_sale_tag_neg`, `tax_report_out_tax_less_sales_0_rate`, `tax_report_out_tax_less_sales_0_rate_tag`, `tax_report_out_tax_less_exempted_sales`, `tax_report_out_tax_less_exempted_sales_tag`, `tax_report_out_tax_taxable_sales_amount`
- Menus: 0; representative evidence: Not found in module
- Templates: 10; representative evidence: `addons/l10n_th/report/report_tawi.xml:3`, `addons/l10n_th/report/report_tawi.xml:357`, `addons/l10n_th/report/report_tawi.xml:376`, `addons/l10n_th/report/report_tawi.xml:385`, `addons/l10n_th/views/report_invoice.xml:3`, `addons/l10n_th/views/report_invoice.xml:30`, `addons/l10n_th/views/report_invoice.xml:139`, `addons/l10n_th/views/report_invoice.xml:202`, `addons/l10n_th/views/report_invoice.xml:209`, `addons/l10n_th/views/report_invoice.xml:228`
- View/action field declarations: 20; representative evidence: `addons/l10n_th/wizards/account_payment_register_views.xml:5`, `addons/l10n_th/wizards/account_payment_register_views.xml:7`, `addons/l10n_th/report/report_tawi.xml:395`, `addons/l10n_th/data/res_country_data.xml:5`, `addons/l10n_th/data/res_country_data.xml:7`, `addons/l10n_th/views/res_config_settings_views.xml:6`, `addons/l10n_th/views/res_config_settings_views.xml:8`, `addons/l10n_th/views/report_invoice.xml:221`, `addons/l10n_th/views/res_company_view.xml:4`, `addons/l10n_th/views/res_company_view.xml:7`, `addons/l10n_th/views/account_move_views.xml:5`, `addons/l10n_th/views/account_move_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_th/__manifest__.py`
- **HTTP entry points:** `addons/l10n_th/controllers/download_tawi_reports.py:7`
- **Scheduled entry points:** `addons/l10n_th/views/account_payment_views.xml`
- **Report entry points:** `addons/l10n_th/report/report_tawi.xml`, `addons/l10n_th/views/report_invoice.xml`, `addons/l10n_th/tests/test_l10n_th_tax_invoice.py`, `addons/l10n_th/tests/test_credit_debit_note_pdf_report.py`

## 7. Database interactions

- Model declarations: 12
- Representative model evidence: inherits `res.partner` (addons/l10n_th/models/res_partner.py:6); inherits `account.partial.reconcile` (addons/l10n_th/models/account_partial_reconcile.py:4); inherits `res.partner.bank` (addons/l10n_th/models/res_bank.py:8); inherits `account.payment` (addons/l10n_th/models/account_payment.py:7); inherits `account.tax` (addons/l10n_th/models/account_tax.py:5); `l10n_th.tax.invoice` (addons/l10n_th/models/l10n_th_tax_invoice.py:4); inherits `account.chart.template` (addons/l10n_th/models/template_th.py:6); inherits `account.move` (addons/l10n_th/models/account_move.py:6); inherits `res.company` (addons/l10n_th/models/res_company.py:4); inherits `base.document.layout` (addons/l10n_th/models/res_company.py:13); inherits `account.payment.register` (addons/l10n_th/wizards/account_payment_register.py:5); `report.l10n_th.report_50_tawi` (addons/l10n_th/report/report_tawi.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/l10n_th/controllers/download_tawi_reports.py:7`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account_qr_code_emv`, `account`, `l10n_account_withholding_tax`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_th/__init__.py`
- `addons/l10n_th/__manifest__.py`
- `addons/l10n_th/controllers/__init__.py`
- `addons/l10n_th/controllers/download_tawi_reports.py`
- `addons/l10n_th/data/account_tax_report_data.xml`
- `addons/l10n_th/data/account_tax_tags_data.xml`
- `addons/l10n_th/data/report_paperformat_data.xml`
- `addons/l10n_th/data/res_country_data.xml`
- `addons/l10n_th/data/template/account.account-th.csv`
- `addons/l10n_th/data/template/account.asset-th.csv`
- `addons/l10n_th/data/template/account.fiscal.position-th.csv`
- `addons/l10n_th/data/template/account.tax-th.csv`
- `addons/l10n_th/data/template/account.tax.group-th.csv`
- `addons/l10n_th/demo/demo_company.xml`
- `addons/l10n_th/i18n/l10n_th.pot`
- `addons/l10n_th/i18n/th.po`
- `addons/l10n_th/models/__init__.py`
- `addons/l10n_th/models/account_move.py`
- `addons/l10n_th/models/account_partial_reconcile.py`
- `addons/l10n_th/models/account_payment.py`
- `addons/l10n_th/models/account_tax.py`
- `addons/l10n_th/models/l10n_th_tax_invoice.py`
- `addons/l10n_th/models/res_bank.py`
- `addons/l10n_th/models/res_company.py`
- `addons/l10n_th/models/res_partner.py`
- `addons/l10n_th/models/template_th.py`
- `addons/l10n_th/report/__init__.py`
- `addons/l10n_th/report/report_tawi.py`
- `addons/l10n_th/report/report_tawi.xml`
- `addons/l10n_th/security/ir.access.csv`
- `addons/l10n_th/tests/__init__.py`
- `addons/l10n_th/tests/test_credit_debit_note_pdf_report.py`
- `addons/l10n_th/tests/test_fiscal_position.py`
- `addons/l10n_th/tests/test_l10n_th_emv_qr.py`
- `addons/l10n_th/tests/test_l10n_th_tax_invoice.py`
- `addons/l10n_th/tests/test_res_partner.py`
- `addons/l10n_th/tests/test_wth_payment.py`
- `addons/l10n_th/views/account_move_views.xml`
- `addons/l10n_th/views/account_payment_views.xml`
- `addons/l10n_th/views/account_tax_views.xml`
- `addons/l10n_th/views/report_invoice.xml`
- `addons/l10n_th/views/res_company_view.xml`
- `addons/l10n_th/views/res_config_settings_views.xml`
- `addons/l10n_th/views/res_partner_view.xml`
- `addons/l10n_th/wizards/__init__.py`
- `addons/l10n_th/wizards/account_payment_register.py`
- `addons/l10n_th/wizards/account_payment_register_views.xml`
