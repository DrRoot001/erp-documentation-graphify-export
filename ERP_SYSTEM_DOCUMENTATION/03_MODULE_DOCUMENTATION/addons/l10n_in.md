# Module: l10n_in

- **Module ID:** MOD-227
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_in`
- **Manifest:** `addons/l10n_in/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Indian Accounting: Chart of Account.
====================================

Indian accounting chart and localization.

Odoo allows to manage Indian Accounting by providing Two Formats Of Chart of Accounts i.e Indian Chart Of Accounts - Standard and Indian Chart Of Accounts - Schedule VI.

Note: The Schedule VI has been revised by MCA and is applicable for all Balance Sheet made after
31st March, 2011. The Format has done away with earlier two options of format of Balance
Sheet, now only Vertical format has been permitted Which is Supported By Odoo.

**Scope evidence:** The module contains 87 files, including 38 Python, 31 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `account_tax_python`, `account_debit_note`, `account`, `l10n_account_withholding_tax`, `iap`.

## 2. Module structure

- Model/business logic files: 21
- Controller/API files: 0
- XML/data/view/template files: 31
- Browser asset files: 3
- Security files: 2
- Test files: 9
- Scheduled/automation evidence files: 0
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_in/security/l10n_in_security.xml`, `addons/l10n_in/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 21 model declarations, 175 methods, 1 constraint handlers, 4 onchange handlers, and 23 dependency declarations.
- **Evidence:** `addons/l10n_in/demo/account_demo.py:13`, `addons/l10n_in/models/res_partner.py:18`, `addons/l10n_in/models/company.py:5`, `addons/l10n_in/models/iap_account.py:10`, `addons/l10n_in/models/port_code.py:4`, `addons/l10n_in/models/uom_uom.py:4`, `addons/l10n_in/models/product_template.py:5`, `addons/l10n_in/models/res_groups.py:6`, `addons/l10n_in/models/l10n_in_pan_entity.py:7`, `addons/l10n_in/models/res_config_settings.py:9`, `addons/l10n_in/models/account_payment.py:4`, `addons/l10n_in/models/account_journal.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 31 XML files and 3 JavaScript/TypeScript files; static XML analysis found 373 record/template/menu identifiers.
- **Evidence:** `addons/l10n_in/demo/demo_company.xml:3`, `addons/l10n_in/demo/demo_company.xml:18`, `addons/l10n_in/demo/product_demo.xml:3`, `addons/l10n_in/demo/product_demo.xml:6`, `addons/l10n_in/demo/product_demo.xml:9`, `addons/l10n_in/demo/product_demo.xml:12`, `addons/l10n_in/demo/product_demo.xml:15`, `addons/l10n_in/demo/product_demo.xml:18`, `addons/l10n_in/demo/product_demo.xml:21`, `addons/l10n_in/demo/product_demo.xml:24`, `addons/l10n_in/demo/product_demo.xml:27`, `addons/l10n_in/demo/product_demo.xml:30`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/l10n_in/security/l10n_in_security.xml`, `addons/l10n_in/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_in/models/account_invoice.py`, `addons/l10n_in/data/account_report_data.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 9 test files are present.
- **Evidence:** `addons/l10n_in/tests/test_gstr_section.py`, `addons/l10n_in/tests/test_hsn_summary.py`, `addons/l10n_in/tests/test_l10n_in_fiscal_position.py`, `addons/l10n_in/tests/test_check_status.py`, `addons/l10n_in/tests/common.py`, `addons/l10n_in/tests/test_partner_details_on_invoice.py`, `addons/l10n_in/tests/test_invoice_label.py`, `addons/l10n_in/tests/__init__.py`, `addons/l10n_in/tests/test_l10n_in_company.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 31; representative identifiers: `base.partner_demo_company_in`, `base.demo_company_in`, `product.product_product_1`, `product.product_product_2`, `product.product_product_3`, `product.product_product_4`, `product.product_product_4b`, `product.product_product_4c`, `product.product_product_5`, `product.product_product_6`, `product.product_product_7`, `product.product_product_8`, `product.product_product_9`, `product.product_product_10`, `product.product_product_11`, `product.product_product_11b`, `product.product_product_12`, `product.product_product_13`, `product.product_product_16`, `product.product_product_20`
- Menus: 2; representative evidence: `addons/l10n_in/data/l10n_in_chart_data.xml:3`, `addons/l10n_in/views/l10n_in_pan_entity_views.xml:52`
- Templates: 7; representative evidence: `addons/l10n_in/views/report_invoice.xml:3`, `addons/l10n_in/views/report_invoice.xml:195`, `addons/l10n_in/views/report_invoice.xml:203`, `addons/l10n_in/views/report_invoice.xml:209`, `addons/l10n_in/views/report_invoice.xml:213`, `addons/l10n_in/views/report_invoice.xml:217`, `addons/l10n_in/views/report_invoice.xml:228`
- View/action field declarations: 50; representative evidence: `addons/l10n_in/wizard/account_move_reversal.xml:5`, `addons/l10n_in/wizard/account_move_reversal.xml:7`, `addons/l10n_in/wizard/account_paymnet_register_views.xml:5`, `addons/l10n_in/wizard/account_paymnet_register_views.xml:7`, `addons/l10n_in/data/account_report_data.xml:6`, `addons/l10n_in/data/account_report_data.xml:16`, `addons/l10n_in/views/uom_uom_views.xml:5`, `addons/l10n_in/views/uom_uom_views.xml:7`, `addons/l10n_in/views/product_template_view.xml:6`, `addons/l10n_in/views/product_template_view.xml:8`, `addons/l10n_in/views/account_invoice_views.xml:5`, `addons/l10n_in/views/account_invoice_views.xml:7`
- Browser assets: 3; representative files: `addons/l10n_in/static/src/helpers/hsn_summary.js`, `addons/l10n_in/static/src/components/tests_shared_js_python/tests_shared_js_python.js`, `addons/l10n_in/static/src/components/hsn_autocomplete/hsn_autocomplete.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_in/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/l10n_in/models/account_invoice.py`, `addons/l10n_in/data/account_report_data.xml`

## 7. Database interactions

- Model declarations: 21
- Representative model evidence: inherits `account.chart.template` (addons/l10n_in/demo/account_demo.py:13); inherits `res.partner` (addons/l10n_in/models/res_partner.py:18); inherits `res.company` (addons/l10n_in/models/company.py:5); inherits `iap.account` (addons/l10n_in/models/iap_account.py:10); `l10n_in.port.code` (addons/l10n_in/models/port_code.py:4); inherits `uom.uom` (addons/l10n_in/models/uom_uom.py:4); inherits `product.template` (addons/l10n_in/models/product_template.py:5); inherits `res.groups` (addons/l10n_in/models/res_groups.py:6); `l10n_in.pan.entity` (addons/l10n_in/models/l10n_in_pan_entity.py:7); inherits `res.config.settings` (addons/l10n_in/models/res_config_settings.py:9); inherits `account.payment` (addons/l10n_in/models/account_payment.py:4); inherits `account.journal` (addons/l10n_in/models/account_journal.py:4); inherits `account.tax` (addons/l10n_in/models/account_tax.py:7); inherits `account.account` (addons/l10n_in/models/account_account.py:4); inherits `account.chart.template` (addons/l10n_in/models/template_in.py:5); inherits `account.move` (addons/l10n_in/models/account_invoice.py:24); inherits `account.report` (addons/l10n_in/models/l10n_in_report_handler.py:4); inherits `res.country.state` (addons/l10n_in/models/res_country_state.py:4); inherits `account.move.line` (addons/l10n_in/models/account_move_line.py:7); inherits `account.move.reversal` (addons/l10n_in/wizard/account_move_reversal.py:4); inherits `account.payment.register` (addons/l10n_in/wizard/account_payment_register.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account_tax_python`, `account_debit_note`, `account`, `l10n_account_withholding_tax`, `iap`
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

- `addons/l10n_in/__init__.py`
- `addons/l10n_in/__manifest__.py`
- `addons/l10n_in/data/account.account.tag.csv`
- `addons/l10n_in/data/account_report_data.xml`
- `addons/l10n_in/data/account_tax_report_tcs_data.xml`
- `addons/l10n_in/data/account_tax_report_tcs_it_act_25_data.xml`
- `addons/l10n_in/data/account_tax_report_tds_data.xml`
- `addons/l10n_in/data/account_tax_report_tds_it_act_25_data.xml`
- `addons/l10n_in/data/iap_service_data.xml`
- `addons/l10n_in/data/l10n_in.port.code.csv`
- `addons/l10n_in/data/l10n_in_chart_data.xml`
- `addons/l10n_in/data/neutralize.sql`
- `addons/l10n_in/data/res_country_group.xml`
- `addons/l10n_in/data/res_country_state_data.xml`
- `addons/l10n_in/data/res_partner_industry.xml`
- `addons/l10n_in/data/template/account.account-in.csv`
- `addons/l10n_in/data/template/account.account-in_sch3.csv`
- `addons/l10n_in/data/template/account.fiscal.position-in.csv`
- `addons/l10n_in/data/template/account.tax-in.csv`
- `addons/l10n_in/data/template/account.tax.group-in.csv`
- `addons/l10n_in/data/uom_data.xml`
- `addons/l10n_in/demo/__init__.py`
- `addons/l10n_in/demo/account_demo.py`
- `addons/l10n_in/demo/demo_company.xml`
- `addons/l10n_in/demo/product_demo.xml`
- `addons/l10n_in/i18n/hi.po`
- `addons/l10n_in/i18n/l10n_in.pot`
- `addons/l10n_in/migrations/2.1/end-migrate.py`
- `addons/l10n_in/migrations/9.0.2.0/pre-set_tags_and_taxes_updatable.py`
- `addons/l10n_in/migrations/saas~19.5.2.2/pre-10-migrate.py`
- `addons/l10n_in/models/__init__.py`
- `addons/l10n_in/models/account_account.py`
- `addons/l10n_in/models/account_invoice.py`
- `addons/l10n_in/models/account_journal.py`
- `addons/l10n_in/models/account_move_line.py`
- `addons/l10n_in/models/account_payment.py`
- `addons/l10n_in/models/account_tax.py`
- `addons/l10n_in/models/company.py`
- `addons/l10n_in/models/iap_account.py`
- `addons/l10n_in/models/l10n_in_pan_entity.py`
- `addons/l10n_in/models/l10n_in_report_handler.py`
- `addons/l10n_in/models/port_code.py`
- `addons/l10n_in/models/product_template.py`
- `addons/l10n_in/models/res_config_settings.py`
- `addons/l10n_in/models/res_country_state.py`
- `addons/l10n_in/models/res_groups.py`
- `addons/l10n_in/models/res_partner.py`
- `addons/l10n_in/models/template_in.py`
- `addons/l10n_in/models/uom_uom.py`
- `addons/l10n_in/security/ir.access.csv`
- `addons/l10n_in/security/l10n_in_security.xml`
- `addons/l10n_in/static/src/components/hsn_autocomplete/hsn_autocomplete.js`
- `addons/l10n_in/static/src/components/hsn_autocomplete/hsn_autocomplete.xml`
- `addons/l10n_in/static/src/components/tests_shared_js_python/tests_shared_js_python.js`
- `addons/l10n_in/static/src/helpers/hsn_summary.js`
- `addons/l10n_in/static/src/img/Google_Pay-Logo.svg`
- `addons/l10n_in/static/src/img/Paytm-Logo.svg`
- `addons/l10n_in/static/src/img/PhonePe-Logo.svg`
- `addons/l10n_in/static/src/img/Upi-logo.svg`
- `addons/l10n_in/tests/__init__.py`
- `addons/l10n_in/tests/common.py`
- `addons/l10n_in/tests/test_check_status.py`
- `addons/l10n_in/tests/test_gstr_section.py`
- `addons/l10n_in/tests/test_hsn_summary.py`
- `addons/l10n_in/tests/test_invoice_label.py`
- `addons/l10n_in/tests/test_l10n_in_company.py`
- `addons/l10n_in/tests/test_l10n_in_fiscal_position.py`
- `addons/l10n_in/tests/test_partner_details_on_invoice.py`
- `addons/l10n_in/views/account_invoice_views.xml`
- `addons/l10n_in/views/account_journal_views.xml`
- `addons/l10n_in/views/account_move_line_views.xml`
- `addons/l10n_in/views/account_tax_views.xml`
- `addons/l10n_in/views/base_document_layout_views.xml`
- `addons/l10n_in/views/l10n_in_pan_entity_views.xml`
- `addons/l10n_in/views/port_code_views.xml`
- `addons/l10n_in/views/product_template_view.xml`
- `addons/l10n_in/views/report_invoice.xml`
- `addons/l10n_in/views/res_company_views.xml`
- `addons/l10n_in/views/res_config_settings_views.xml`
- `addons/l10n_in/views/res_country_state_view.xml`
- `addons/l10n_in/views/res_partner_views.xml`
- `addons/l10n_in/views/uom_uom_views.xml`
- `addons/l10n_in/wizard/__init__.py`
- `addons/l10n_in/wizard/account_move_reversal.py`
- `addons/l10n_in/wizard/account_move_reversal.xml`
- `addons/l10n_in/wizard/account_payment_register.py`
- `addons/l10n_in/wizard/account_paymnet_register_views.xml`
