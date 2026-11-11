# Module: account

- **Module ID:** MOD-001
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/account`
- **Manifest:** `addons/account/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Invoices & Payments

**Manifest description:**

Invoicing & Payments
====================
The specific and easy-to-use Invoicing system in Odoo allows you to keep track of your accounting, even when you are not an accountant. It provides an easy way to follow up on your vendors and customers.

You could use this simplified accounting in case you work with an (external) account to keep your books, and you still want to keep track of payments. This module also offers you an easy method of registering payments, without having to encode complete abstracts of account.

**Scope evidence:** The module contains 553 files, including 173 Python, 138 XML, and 115 JavaScript/TypeScript files. The manifest declares dependencies: `base_setup`, `onboarding`, `product`, `analytic`, `portal`, `digest`.

## 2. Module structure

- Model/business logic files: 96
- Controller/API files: 6
- XML/data/view/template files: 138
- Browser asset files: 115
- Security files: 2
- Test files: 80
- Scheduled/automation evidence files: 16
- Reporting evidence files: 18

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/account/security/ir.access.csv`, `addons/account/security/account_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 96 model declarations, 3424 methods, 67 constraint handlers, 51 onchange handlers, and 393 dependency declarations.
- **Evidence:** `addons/account/demo/account_demo.py:22`, `addons/account/models/account_payment_method.py:7`, `addons/account/models/account_payment_method.py:95`, `addons/account/models/kpi_provider.py:5`, `addons/account/models/chart_template.py:91`, `addons/account/models/account_partial_reconcile.py:12`, `addons/account/models/mail_message.py:33`, `addons/account/models/company.py:73`, `addons/account/models/digest.py:7`, `addons/account/models/uom_uom.py:35`, `addons/account/models/account_bank_statement.py:11`, `addons/account/models/account_payment_term.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 6 controller files and 10 route declarations.
- **Evidence:** `addons/account/controllers/portal.py:74`, `addons/account/controllers/portal.py:144`, `addons/account/controllers/portal.py:179`, `addons/account/controllers/portal.py:273`, `addons/account/controllers/terms.py:18`, `addons/account/controllers/tests_shared_js_python.py:9`, `addons/account/controllers/tests_shared_js_python.py:14`, `addons/account/controllers/download_docs.py:30`, `addons/account/controllers/download_docs.py:49`, `addons/account/controllers/download_docs.py:72`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 138 XML files and 115 JavaScript/TypeScript files; static XML analysis found 462 record/template/menu identifiers.
- **Evidence:** `addons/account/demo/res_partner_bank_demo.xml:5`, `addons/account/demo/res_partner_bank_demo.xml:11`, `addons/account/demo/res_partner_bank_demo.xml:17`, `addons/account/demo/res_partner_bank_demo.xml:23`, `addons/account/demo/account_demo.xml:4`, `addons/account/demo/account_demo.xml:8`, `addons/account/demo/account_demo.xml:14`, `addons/account/demo/account_demo.xml:17`, `addons/account/demo/account_demo.xml:20`, `addons/account/demo/account_demo.xml:23`, `addons/account/demo/account_demo.xml:26`, `addons/account/demo/account_demo.xml:51`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/account/security/ir.access.csv`, `addons/account/security/account_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 16 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/account/__manifest__.py`, `addons/account/models/company.py`, `addons/account/models/account_move.py`, `addons/account/models/account_move_send.py`, `addons/account/wizard/account_unreconcile_view.xml`, `addons/account/wizard/account_validate_move_view.xml`, `addons/account/wizard/account_move_send_batch_wizard.py`, `addons/account/data/account_data.xml`, `addons/account/data/service_cron.xml`, `addons/account/views/account_payment_view.xml`, `addons/account/views/account_move_views.xml`, `addons/account/views/account_account_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 18 files contain report-action/template indicators.
- **Evidence:** `addons/account/models/ir_actions_report.py`, `addons/account/models/account_journal.py`, `addons/account/models/account_report.py`, `addons/account/models/account_move.py`, `addons/account/models/account_journal_dashboard.py`, `addons/account/models/res_partner_bank.py`, `addons/account/models/account_move_send.py`, `addons/account/models/partner.py`, `addons/account/controllers/portal.py`, `addons/account/wizard/account_move_send_wizard.py`, `addons/account/views/ir_actions_views.xml`, `addons/account/views/account_report.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 80 test files are present.
- **Evidence:** `addons/account/tests/test_account_move_entry.py`, `addons/account/tests/test_account_partner.py`, `addons/account/tests/test_account_payment.py`, `addons/account/tests/test_portal_attachment.py`, `addons/account/tests/test_tax.py`, `addons/account/tests/test_account_account.py`, `addons/account/tests/test_portal_additional_identifiers.py`, `addons/account/tests/test_account_payment_items.py`, `addons/account/tests/test_account_move_attachment.py`, `addons/account/tests/test_early_payment_discount.py`, `addons/account/tests/test_account_journal_dashboard_common.py`, `addons/account/tests/test_setup_wizard.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 138; representative identifiers: `bank_iban_asustek`, `bank_iban_china_export`, `bank_iban_main_partner`, `bank_clabe_partner`, `base.user_demo`, `base.default_user_group`, `demo_capital_account`, `demo_stock_account`, `demo_sale_of_land_account`, `demo_ceo_wages_account`, `demo_office_furniture_account`, `account_payment_term_advance`, `base.res_partner_2`, `base.res_partner_12`, `base.res_partner_4`, `base.res_partner_1`, `analytic.analytic_plan_internal`, `res_groups_privilege_accounting`, `group_delivery_invoice_address`, `group_account_readonly`
- Menus: 52; representative evidence: `addons/account/wizard/account_secure_entries_wizard.xml:42`, `addons/account/views/mail_message_views.xml:66`, `addons/account/views/account_menuitem.xml:4`, `addons/account/views/account_menuitem.xml:9`, `addons/account/views/account_menuitem.xml:10`, `addons/account/views/account_menuitem.xml:11`, `addons/account/views/account_menuitem.xml:12`, `addons/account/views/account_menuitem.xml:13`, `addons/account/views/account_menuitem.xml:14`, `addons/account/views/account_menuitem.xml:15`, `addons/account/views/account_menuitem.xml:17`, `addons/account/views/account_menuitem.xml:18`
- Templates: 31; representative evidence: `addons/account/report/account_hash_integrity_templates.xml:4`, `addons/account/data/mail_template_data.xml:248`, `addons/account/views/report_templates.xml:3`, `addons/account/views/report_templates.xml:9`, `addons/account/views/report_templates.xml:20`, `addons/account/views/report_templates.xml:31`, `addons/account/views/report_invoice.xml:4`, `addons/account/views/report_invoice.xml:491`, `addons/account/views/report_invoice.xml:568`, `addons/account/views/report_invoice.xml:570`, `addons/account/views/report_invoice.xml:634`, `addons/account/views/report_invoice.xml:645`
- View/action field declarations: 439; representative evidence: `addons/account/report/account_stock_valuation_report.xml:6`, `addons/account/report/account_invoice_report_view.xml:6`, `addons/account/report/account_invoice_report_view.xml:7`, `addons/account/report/account_invoice_report_view.xml:18`, `addons/account/report/account_invoice_report_view.xml:19`, `addons/account/report/account_invoice_report_view.xml:29`, `addons/account/report/account_invoice_report_view.xml:30`, `addons/account/report/account_invoice_report_view.xml:102`, `addons/account/report/account_invoice_report_view.xml:103`, `addons/account/report/account_invoice_report_view.xml:143`, `addons/account/report/account_invoice_report_view.xml:145`, `addons/account/report/account_invoice_report_view.xml:152`
- Browser assets: 115; representative files: `addons/account/static/tests/account_widgets.test.js`, `addons/account/static/tests/account_test_helpers.js`, `addons/account/static/tests/account_payment_field.test.js`, `addons/account/static/tests/char_with_placeholder_field.test.js`, `addons/account/static/tests/account_dashboard_kpis.test.js`, `addons/account/static/tests/account_number_widget_test_helpers.js`, `addons/account/static/tests/x2many_buttons.test.js`, `addons/account/static/tests/section_and_note.test.js`, `addons/account/static/tests/many2many_tags_banks.test.js`, `addons/account/static/tests/account_move_form.test.js`, `addons/account/static/tests/account_number_widget.test.js`, `addons/account/static/src/services/account_notification_service.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/account/__manifest__.py`
- **HTTP entry points:** `addons/account/controllers/portal.py:74`, `addons/account/controllers/portal.py:144`, `addons/account/controllers/portal.py:179`, `addons/account/controllers/portal.py:273`, `addons/account/controllers/terms.py:18`, `addons/account/controllers/tests_shared_js_python.py:9`, `addons/account/controllers/tests_shared_js_python.py:14`, `addons/account/controllers/download_docs.py:30`, `addons/account/controllers/download_docs.py:49`, `addons/account/controllers/download_docs.py:72`
- **Scheduled entry points:** `addons/account/__manifest__.py`, `addons/account/models/company.py`, `addons/account/models/account_move.py`, `addons/account/models/account_move_send.py`, `addons/account/wizard/account_unreconcile_view.xml`, `addons/account/wizard/account_validate_move_view.xml`, `addons/account/wizard/account_move_send_batch_wizard.py`, `addons/account/data/account_data.xml`, `addons/account/data/service_cron.xml`, `addons/account/views/account_payment_view.xml`, `addons/account/views/account_move_views.xml`, `addons/account/views/account_account_views.xml`
- **Report entry points:** `addons/account/models/ir_actions_report.py`, `addons/account/models/account_journal.py`, `addons/account/models/account_report.py`, `addons/account/models/account_move.py`, `addons/account/models/account_journal_dashboard.py`, `addons/account/models/res_partner_bank.py`, `addons/account/models/account_move_send.py`, `addons/account/models/partner.py`, `addons/account/controllers/portal.py`, `addons/account/wizard/account_move_send_wizard.py`, `addons/account/views/ir_actions_views.xml`, `addons/account/views/account_report.xml`

## 7. Database interactions

- Model declarations: 96
- Representative model evidence: inherits `account.chart.template` (addons/account/demo/account_demo.py:22); `account.payment.method` (addons/account/models/account_payment_method.py:7); `account.payment.method.line` (addons/account/models/account_payment_method.py:95); inherits `kpi.provider` (addons/account/models/kpi_provider.py:5); `account.chart.template` (addons/account/models/chart_template.py:91); `account.partial.reconcile` (addons/account/models/account_partial_reconcile.py:12); inherits `mail.message` (addons/account/models/mail_message.py:33); `res.company` (addons/account/models/company.py:73); inherits `digest.digest` (addons/account/models/digest.py:7); inherits `uom.uom` (addons/account/models/uom_uom.py:35); `account.bank.statement` (addons/account/models/account_bank_statement.py:11); `account.payment.term` (addons/account/models/account_payment_term.py:9); `account.payment.term.line` (addons/account/models/account_payment_term.py:274); inherits `account.analytic.distribution.model` (addons/account/models/account_analytic_distribution_model.py:6); inherits `product.catalog.mixin` (addons/account/models/product_catalog_mixin.py:8); `account.code.mapping` (addons/account/models/account_code_mapping.py:10); inherits `res.groups` (addons/account/models/res_groups.py:6); inherits `mail.template` (addons/account/models/mail_template.py:5); inherits `account.analytic.applicability` (addons/account/models/account_analytic_plan.py:6); `account.root` (addons/account/models/account_root.py:10); inherits `res.config.settings` (addons/account/models/res_config_settings.py:8); `account.full.reconcile` (addons/account/models/account_full_reconcile.py:7); inherits `base.partner.merge.automatic.wizard` (addons/account/models/merge_partner_automatic.py:5); inherits `res.currency` (addons/account/models/res_currency.py:12); inherits `res.currency.rate` (addons/account/models/res_currency.py:171); inherits `account.analytic.line` (addons/account/models/account_analytic_line.py:8); inherits `account.chart.template` (addons/account/models/template_generic_coa.py:5); `account.payment` (addons/account/models/account_payment.py:7); inherits `account.move` (addons/account/models/account_payment.py:1327); inherits `ir.actions.report` (addons/account/models/ir_actions_report.py:10)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 6
- Route declarations: 10
- Route evidence: `addons/account/controllers/portal.py:74`, `addons/account/controllers/portal.py:144`, `addons/account/controllers/portal.py:179`, `addons/account/controllers/portal.py:273`, `addons/account/controllers/terms.py:18`, `addons/account/controllers/tests_shared_js_python.py:9`, `addons/account/controllers/tests_shared_js_python.py:14`, `addons/account/controllers/download_docs.py:30`, `addons/account/controllers/download_docs.py:49`, `addons/account/controllers/download_docs.py:72`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base_setup`, `onboarding`, `product`, `analytic`, `portal`, `digest`
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

- `addons/account/README.md`
- `addons/account/__init__.py`
- `addons/account/__manifest__.py`
- `addons/account/controllers/__init__.py`
- `addons/account/controllers/download_docs.py`
- `addons/account/controllers/portal.py`
- `addons/account/controllers/terms.py`
- `addons/account/controllers/tests_shared_js_python.py`
- `addons/account/controllers/webmanifest.py`
- `addons/account/data/account_data.xml`
- `addons/account/data/account_incoterms_data.xml`
- `addons/account/data/account_reports_data.xml`
- `addons/account/data/account_tour.xml`
- `addons/account/data/digest_data.xml`
- `addons/account/data/ir_config_parameter_data.xml`
- `addons/account/data/ir_sequence.xml`
- `addons/account/data/mail_template_data.xml`
- `addons/account/data/onboarding_data.xml`
- `addons/account/data/portal_entry_data.xml`
- `addons/account/data/res_country_group.xml`
- `addons/account/data/service_cron.xml`
- `addons/account/data/template/account.account-generic_coa.csv`
- `addons/account/data/template/account.fiscal.position-generic_coa.csv`
- `addons/account/data/template/account.tax-generic_coa.csv`
- `addons/account/data/template/account.tax.group-generic_coa.csv`
- `addons/account/demo/__init__.py`
- `addons/account/demo/account_demo.py`
- `addons/account/demo/account_demo.xml`
- `addons/account/demo/res_partner_bank_demo.xml`
- `addons/account/doc/account_anglo_saxon.ods`
- `addons/account/doc/account_anglo_saxon.pdf`
- `addons/account/i18n/account.pot`
- `addons/account/i18n/af.po`
- `addons/account/i18n/am.po`
- `addons/account/i18n/ar.po`
- `addons/account/i18n/az.po`
- `addons/account/i18n/bg.po`
- `addons/account/i18n/bs.po`
- `addons/account/i18n/ca.po`
- `addons/account/i18n/cs.po`
- `addons/account/i18n/da.po`
- `addons/account/i18n/de.po`
- `addons/account/i18n/el.po`
- `addons/account/i18n/en_AU.po`
- `addons/account/i18n/en_NZ.po`
- `addons/account/i18n/es.po`
- `addons/account/i18n/es_419.po`
- `addons/account/i18n/es_CL.po`
- `addons/account/i18n/et.po`
- `addons/account/i18n/eu.po`
- `addons/account/i18n/fa.po`
- `addons/account/i18n/fi.po`
- `addons/account/i18n/fo.po`
- `addons/account/i18n/fr.po`
- `addons/account/i18n/fr_BE.po`
- `addons/account/i18n/fr_CA.po`
- `addons/account/i18n/gl.po`
- `addons/account/i18n/gu.po`
- `addons/account/i18n/he.po`
- `addons/account/i18n/hi.po`
- `addons/account/i18n/hr.po`
- `addons/account/i18n/hu.po`
- `addons/account/i18n/id.po`
- `addons/account/i18n/is.po`
- `addons/account/i18n/it.po`
- `addons/account/i18n/ja.po`
- `addons/account/i18n/ka.po`
- `addons/account/i18n/kab.po`
- `addons/account/i18n/km.po`
- `addons/account/i18n/ko.po`
- `addons/account/i18n/ku.po`
- `addons/account/i18n/lb.po`
- `addons/account/i18n/lo.po`
- `addons/account/i18n/lt.po`
- `addons/account/i18n/lv.po`
- `addons/account/i18n/mk.po`
- `addons/account/i18n/mn.po`
- `addons/account/i18n/my.po`
- `addons/account/i18n/nb.po`
- `addons/account/i18n/nl.po`
- `addons/account/i18n/pl.po`
- `addons/account/i18n/pt.po`
- `addons/account/i18n/pt_BR.po`
- `addons/account/i18n/ro.po`
- `addons/account/i18n/ru.po`
- `addons/account/i18n/sk.po`
- `addons/account/i18n/sl.po`
- `addons/account/i18n/sq.po`
- `addons/account/i18n/sr@latin.po`
- `addons/account/i18n/sv.po`
- `addons/account/i18n/th.po`
- `addons/account/i18n/tr.po`
- `addons/account/i18n/uk.po`
- `addons/account/i18n/uz.po`
- `addons/account/i18n/vi.po`
- `addons/account/i18n/zh_CN.po`
- `addons/account/i18n/zh_TW.po`
- `addons/account/migrations/1.5/pre-migrate.py`
- `addons/account/migrations/1.6/pre-migrate.py`
- `addons/account/models/__init__.py`
- `addons/account/models/account_account.py`
- `addons/account/models/account_account_tag.py`
- `addons/account/models/account_analytic_account.py`
- `addons/account/models/account_analytic_distribution_model.py`
- `addons/account/models/account_analytic_line.py`
- `addons/account/models/account_analytic_plan.py`
- `addons/account/models/account_bank_statement.py`
- `addons/account/models/account_bank_statement_line.py`
- `addons/account/models/account_cash_rounding.py`
- `addons/account/models/account_code_mapping.py`
- `addons/account/models/account_document_import_mixin.py`
- `addons/account/models/account_full_reconcile.py`
- `addons/account/models/account_incoterms.py`
- `addons/account/models/account_journal.py`
- `addons/account/models/account_journal_dashboard.py`
- `addons/account/models/account_lock_exception.py`
- `addons/account/models/account_move.py`
- `addons/account/models/account_move_line.py`
- `addons/account/models/account_move_line_tax_details.py`
- `addons/account/models/account_move_send.py`
- `addons/account/models/account_partial_reconcile.py`
- `addons/account/models/account_payment.py`
- `addons/account/models/account_payment_method.py`
- `addons/account/models/account_payment_term.py`
- `addons/account/models/account_reconcile_model.py`
- `addons/account/models/account_report.py`
- `addons/account/models/account_root.py`
- `addons/account/models/account_tax.py`
- `addons/account/models/chart_template.py`
- `addons/account/models/company.py`
- `addons/account/models/decimal_precision.py`
- `addons/account/models/digest.py`
- `addons/account/models/ir_actions_report.py`
- `addons/account/models/ir_attachment.py`
- `addons/account/models/ir_http.py`
- `addons/account/models/ir_module.py`
- `addons/account/models/kpi_provider.py`
- `addons/account/models/mail_message.py`
- `addons/account/models/mail_template.py`
- `addons/account/models/merge_partner_automatic.py`
- `addons/account/models/onboarding_onboarding.py`
- `addons/account/models/onboarding_onboarding_step.py`
- `addons/account/models/partner.py`
- `addons/account/models/product.py`
- `addons/account/models/product_catalog_line_mixin.py`
- `addons/account/models/product_catalog_mixin.py`
- `addons/account/models/res_config_settings.py`
- `addons/account/models/res_country_group.py`
- `addons/account/models/res_currency.py`
- `addons/account/models/res_currency_rate_consolidation_mixin.py`
- `addons/account/models/res_groups.py`
- `addons/account/models/res_partner_bank.py`
- `addons/account/models/res_users.py`
- `addons/account/models/sequence_mixin.py`
- `addons/account/models/template_generic_coa.py`
- `addons/account/models/uom_uom.py`
- `addons/account/populate/benchmarks.xml`
- `addons/account/populate/populate_demo.xml`
- `addons/account/report/__init__.py`
- `addons/account/report/account_hash_integrity_templates.py`
- `addons/account/report/account_hash_integrity_templates.xml`
- `addons/account/report/account_invoice_report.py`
- `addons/account/report/account_invoice_report_view.xml`
- `addons/account/report/account_stock_valuation_report.py`
- `addons/account/report/account_stock_valuation_report.xml`
- `addons/account/security/account_security.xml`
- `addons/account/security/ir.access.csv`
- `addons/account/static/demo/bank_statement_one_month_old.pdf`
- `addons/account/static/demo/in_invoice_yourcompany_demo_1.pdf`
- `addons/account/static/demo/in_invoice_yourcompany_demo_2.pdf`
- `addons/account/static/description/icon.png`
- `addons/account/static/description/icon.svg`
- `addons/account/static/description/icon_hi.png`
- `addons/account/static/description/l10n.png`
- `addons/account/static/description/l10n.svg`
- `addons/account/static/src/components/account_batch_sending_summary/account_batch_sending_summary.js`
- `addons/account/static/src/components/account_batch_sending_summary/account_batch_sending_summary.xml`
- `addons/account/static/src/components/account_dashboard_kpis/account_dashboard_kpi_card.js`
- `addons/account/static/src/components/account_dashboard_kpis/account_dashboard_kpi_card.xml`
- `addons/account/static/src/components/account_dashboard_kpis/account_dashboard_kpis.dark.scss`
- `addons/account/static/src/components/account_dashboard_kpis/account_dashboard_kpis.js`
- `addons/account/static/src/components/account_dashboard_kpis/account_dashboard_kpis.scss`
- `addons/account/static/src/components/account_dashboard_kpis/account_dashboard_kpis.xml`
- `addons/account/static/src/components/account_document_tax_mode_selector/account_document_tax_mode_selector.js`
- `addons/account/static/src/components/account_document_tax_mode_selector/account_document_tax_mode_selector.xml`
- `addons/account/static/src/components/account_file_uploader/account_file_uploader.js`
- `addons/account/static/src/components/account_file_uploader/account_file_uploader.scss`
- `addons/account/static/src/components/account_file_uploader/account_file_uploader.xml`
- `addons/account/static/src/components/account_label_text/account_label_text.js`
- `addons/account/static/src/components/account_label_text/account_label_text.scss`
- `addons/account/static/src/components/account_label_text/account_label_text.xml`
- `addons/account/static/src/components/account_merge_wizard_line_one2many/account_merge_wizard_line_one2many.js`
- `addons/account/static/src/components/account_move_form/account_move_form.js`
- `addons/account/static/src/components/account_move_form/account_move_form_notebook.xml`
- `addons/account/static/src/components/account_number_widget/account_number_widget.js`
- `addons/account/static/src/components/account_number_widget/account_number_widget.scss`
- `addons/account/static/src/components/account_number_widget/account_number_widget.xml`
- `addons/account/static/src/components/account_payment_field/account_payment.xml`
- `addons/account/static/src/components/account_payment_field/account_payment_field.js`
- `addons/account/static/src/components/account_payment_register_html/account_payment_register_html.js`
- `addons/account/static/src/components/account_payment_register_html/account_payment_register_html.xml`
- `addons/account/static/src/components/account_payment_term_form/payment_term_line_ids.js`
- `addons/account/static/src/components/account_pick_currency_rate/account_pick_currency_rate.js`
- `addons/account/static/src/components/account_pick_currency_rate/account_pick_currency_rate.xml`
- `addons/account/static/src/components/account_product_field/account_product_field.js`
- `addons/account/static/src/components/account_product_field/account_product_field.xml`
- `addons/account/static/src/components/account_resequence/account_resequence.xml`
- `addons/account/static/src/components/account_resequence/account_resequence_field.js`
- `addons/account/static/src/components/account_review_state_selection/account_review_state_selection_badge.js`
- `addons/account/static/src/components/account_review_state_selection/account_review_state_selection_badge.scss`
- `addons/account/static/src/components/account_review_state_selection/account_review_state_selection_badge.xml`
- `addons/account/static/src/components/account_statusbar_secured/account_move_statusbar_secured.js`
- `addons/account/static/src/components/account_statusbar_secured/account_move_statusbar_secured.xml`
- `addons/account/static/src/components/account_tax_repartition_line_factor_percent/account_tax_repartition_line_factor_percent.js`
- `addons/account/static/src/components/account_type_selection/account_type_selection.js`
- `addons/account/static/src/components/account_type_selection/account_type_selection.xml`
- `addons/account/static/src/components/actionable_errors/actionable_errors.js`
- `addons/account/static/src/components/actionable_errors/actionable_errors.xml`
- `addons/account/static/src/components/auto_save_res_partner_bank/auto_save_res_partner_bank.js`
- `addons/account/static/src/components/autosave_many2many_tax_tags/autosave_many2many_tax_tags.js`
- `addons/account/static/src/components/bill_guide/bill_guide.js`
- `addons/account/static/src/components/bill_guide/bill_guide.scss`
- `addons/account/static/src/components/bill_guide/bill_guide.xml`
- `addons/account/static/src/components/char_with_placeholder_field/char_with_placeholder_field.js`
- `addons/account/static/src/components/char_with_placeholder_field/char_with_placeholder_field.xml`
- `addons/account/static/src/components/currency_form/form_controller.js`
- `addons/account/static/src/components/currency_form/open_decimal_precision_btn.js`
- `addons/account/static/src/components/currency_form/open_decimal_precision_btn_template.xml`
- `addons/account/static/src/components/document_file_uploader/document_file_uploader.js`
- `addons/account/static/src/components/document_file_uploader/document_file_uploader.xml`
- `addons/account/static/src/components/document_state/document_state_field.js`
- `addons/account/static/src/components/document_state/document_state_field.scss`
- `addons/account/static/src/components/document_state/document_state_field.xml`
- `addons/account/static/src/components/dynamic_selection/dynamic_selection.js`
- `addons/account/static/src/components/fetch_einvoices/fetch_einvoices.xml`
- `addons/account/static/src/components/fetch_einvoices/fetch_einvoices_cog.js`
- `addons/account/static/src/components/grouped_view_widget/grouped_view_widget.js`
- `addons/account/static/src/components/grouped_view_widget/grouped_view_widget.xml`
- `addons/account/static/src/components/invoice_guide/invoice_guide.js`
- `addons/account/static/src/components/invoice_guide/invoice_guide.xml`
- `addons/account/static/src/components/m2o_cell_with_extra_fields/m2o_cell_with_extra_fields.js`
- `addons/account/static/src/components/m2o_cell_with_extra_fields/m2o_cell_with_extra_fields.scss`
- `addons/account/static/src/components/m2o_cell_with_extra_fields/m2o_cell_with_extra_fields.xml`
- `addons/account/static/src/components/mail_attachments/account_move_send_attachments_selector.js`
- `addons/account/static/src/components/mail_attachments/account_move_send_attachments_selector.scss`
- `addons/account/static/src/components/mail_attachments/account_move_send_attachments_selector.xml`
- `addons/account/static/src/components/mail_attachments/mail_attachments.js`
- `addons/account/static/src/components/mail_attachments/mail_attachments.xml`
- `addons/account/static/src/components/many2many_tags_banks/many2many_tags_banks.js`
- `addons/account/static/src/components/many2many_tags_banks/many2many_tags_banks.xml`
- Additional source files not expanded in this page: 303; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
