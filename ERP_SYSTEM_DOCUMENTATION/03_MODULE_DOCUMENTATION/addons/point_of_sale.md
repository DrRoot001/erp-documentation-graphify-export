# Module: point_of_sale

- **Module ID:** MOD-417
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/point_of_sale`
- **Manifest:** `addons/point_of_sale/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Sales/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Handle checkouts and payments for shops and restaurants.

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 885 files, including 103 Python, 147 XML, and 391 JavaScript/TypeScript files. The manifest declares dependencies: `resource`, `product`, `account`, `barcodes_gs1_nomenclature`, `html_editor`, `digest`, `phone_validation`, `google_address_autocomplete`, `base_report_wkhtmltox`, `iot_webserial`.

## 2. Module structure

- Model/business logic files: 67
- Controller/API files: 4
- XML/data/view/template files: 147
- Browser asset files: 391
- Security files: 2
- Test files: 29
- Scheduled/automation evidence files: 9
- Reporting evidence files: 5

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/point_of_sale/security/point_of_sale_security.xml`, `addons/point_of_sale/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 67 model declarations, 1053 methods, 30 constraint handlers, 20 onchange handlers, and 59 dependency declarations.
- **Evidence:** `addons/point_of_sale/models/pos_prep_line.py:5`, `addons/point_of_sale/models/product_category.py:5`, `addons/point_of_sale/models/res_partner.py:6`, `addons/point_of_sale/models/product_product.py:5`, `addons/point_of_sale/models/product_combo.py:7`, `addons/point_of_sale/models/res_lang.py:4`, `addons/point_of_sale/models/product_attribute.py:5`, `addons/point_of_sale/models/product_attribute.py:14`, `addons/point_of_sale/models/product_attribute.py:34`, `addons/point_of_sale/models/product_attribute.py:51`, `addons/point_of_sale/models/uom.py:4`, `addons/point_of_sale/models/barcode_rule.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 4 controller files and 11 route declarations.
- **Evidence:** `addons/point_of_sale/controllers/customer_display.py:11`, `addons/point_of_sale/controllers/customer_display.py:34`, `addons/point_of_sale/controllers/binary.py:7`, `addons/point_of_sale/controllers/main.py:19`, `addons/point_of_sale/controllers/main.py:32`, `addons/point_of_sale/controllers/main.py:49`, `addons/point_of_sale/controllers/main.py:53`, `addons/point_of_sale/controllers/main.py:121`, `addons/point_of_sale/controllers/main.py:125`, `addons/point_of_sale/controllers/main.py:132`, `addons/point_of_sale/controllers/main.py:176`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 147 XML files and 391 JavaScript/TypeScript files; static XML analysis found 316 record/template/menu identifiers.
- **Evidence:** `addons/point_of_sale/security/point_of_sale_security.xml:2`, `addons/point_of_sale/security/point_of_sale_security.xml:7`, `addons/point_of_sale/security/point_of_sale_security.xml:13`, `addons/point_of_sale/security/point_of_sale_security.xml:21`, `addons/point_of_sale/security/point_of_sale_security.xml:26`, `addons/point_of_sale/wizard/pos_daily_sales_reports.xml:3`, `addons/point_of_sale/wizard/pos_daily_sales_reports.xml:20`, `addons/point_of_sale/wizard/pos_payment.xml:3`, `addons/point_of_sale/wizard/pos_payment.xml:21`, `addons/point_of_sale/wizard/pos_confirmation_wizard.xml:3`, `addons/point_of_sale/wizard/pos_confirmation_wizard.xml:19`, `addons/point_of_sale/wizard/pos_details.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/point_of_sale/security/point_of_sale_security.xml`, `addons/point_of_sale/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 9 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/point_of_sale/__manifest__.py`, `addons/point_of_sale/models/res_config_settings.py`, `addons/point_of_sale/models/pos_session.py`, `addons/point_of_sale/models/pos_order.py`, `addons/point_of_sale/models/pos_snooze.py`, `addons/point_of_sale/data/ir_cron_data.xml`, `addons/point_of_sale/views/res_config_settings_views.xml`, `addons/point_of_sale/views/pos_order_view.xml`, `addons/point_of_sale/tests/test_pos_accounting.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 5 files contain report-action/template indicators.
- **Evidence:** `addons/point_of_sale/models/pos_order.py`, `addons/point_of_sale/controllers/main.py`, `addons/point_of_sale/receipt/pos_order_receipt.py`, `addons/point_of_sale/views/point_of_sale_report.xml`, `addons/point_of_sale/tests/test_report_session.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 29 test files are present.
- **Evidence:** `addons/point_of_sale/tests/test_pos_controller.py`, `addons/point_of_sale/tests/test_pos_accounting.py`, `addons/point_of_sale/tests/test_generic_localization.py`, `addons/point_of_sale/tests/test_pos_invoice_consolidation.py`, `addons/point_of_sale/tests/test_pos_accounting_http.py`, `addons/point_of_sale/tests/test_backend.py`, `addons/point_of_sale/tests/test_point_of_sale_ui.py`, `addons/point_of_sale/tests/test_frontend.py`, `addons/point_of_sale/tests/common_setup_methods.py`, `addons/point_of_sale/tests/test_pos_other_currency_config.py`, `addons/point_of_sale/tests/test_pos_product_variants.py`, `addons/point_of_sale/tests/test_pos_accounting_currency.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 147; representative identifiers: `res_groups_privilege_point_of_sale`, `group_pos_user`, `group_pos_manager`, `group_pos_preset`, `base.default_user_group`, `view_pos_daily_sales_reports_wizard`, `action_report_pos_daily_sales_reports`, `view_pos_payment`, `action_pos_payment`, `point_of_sale.view_confirm_action_wizard`, `action_confirm_action_wizard`, `view_pos_details_wizard`, `view_pos_price_inclusion_wizard_form`, `point_of_sale.view_pos_make_invoice`, `digest.digest_digest_default`, `email_template_pos_receipt`, `point_of_sale_tour`, `barcode_rule_cashier`, `barcode_rule_client`, `barcode_rule_discount`
- Menus: 27; representative evidence: `addons/point_of_sale/views/pos_payment_method_views.xml:154`, `addons/point_of_sale/views/pos_config_view.xml:188`, `addons/point_of_sale/views/pos_config_view.xml:192`, `addons/point_of_sale/views/pos_config_view.xml:196`, `addons/point_of_sale/views/pos_note_view.xml:28`, `addons/point_of_sale/views/pos_printer_view.xml:102`, `addons/point_of_sale/views/pos_payment_views.xml:79`, `addons/point_of_sale/views/product_view.xml:112`, `addons/point_of_sale/views/product_view.xml:115`, `addons/point_of_sale/views/product_view.xml:119`, `addons/point_of_sale/views/product_view.xml:124`, `addons/point_of_sale/views/pos_bill_view.xml:42`
- Templates: 24; representative evidence: `addons/point_of_sale/receipt/pos_sale_details_receipt.xml:4`, `addons/point_of_sale/receipt/pos_sale_details_receipt.xml:97`, `addons/point_of_sale/receipt/pos_order_change_receipt.xml:4`, `addons/point_of_sale/receipt/pos_order_change_receipt.xml:81`, `addons/point_of_sale/receipt/pos_cash_move_receipt.xml:4`, `addons/point_of_sale/receipt/pos_order_receipt.xml:4`, `addons/point_of_sale/receipt/pos_order_receipt.xml:132`, `addons/point_of_sale/receipt/pos_order_receipt.xml:199`, `addons/point_of_sale/receipt/pos_order_receipt.xml:222`, `addons/point_of_sale/receipt/pos_order_receipt.xml:240`, `addons/point_of_sale/receipt/pos_order_change_receipt_zpl.xml:4`, `addons/point_of_sale/receipt/pos_tip_receipt.xml:4`
- View/action field declarations: 189; representative evidence: `addons/point_of_sale/wizard/pos_daily_sales_reports.xml:5`, `addons/point_of_sale/wizard/pos_daily_sales_reports.xml:6`, `addons/point_of_sale/wizard/pos_daily_sales_reports.xml:22`, `addons/point_of_sale/wizard/pos_daily_sales_reports.xml:23`, `addons/point_of_sale/wizard/pos_payment.xml:5`, `addons/point_of_sale/wizard/pos_payment.xml:6`, `addons/point_of_sale/wizard/pos_payment.xml:23`, `addons/point_of_sale/wizard/pos_payment.xml:24`, `addons/point_of_sale/wizard/pos_confirmation_wizard.xml:5`, `addons/point_of_sale/wizard/pos_confirmation_wizard.xml:6`, `addons/point_of_sale/wizard/pos_confirmation_wizard.xml:21`, `addons/point_of_sale/wizard/pos_confirmation_wizard.xml:22`
- Browser assets: 391; representative files: `addons/point_of_sale/static/lib/qrcode.js`, `addons/point_of_sale/static/lib/sha1.js`, `addons/point_of_sale/static/src/utils.js`, `addons/point_of_sale/static/src/lazy_getter.js`, `addons/point_of_sale/static/src/customer_display/customer_display_plugin.js`, `addons/point_of_sale/static/src/customer_display/root.js`, `addons/point_of_sale/static/src/customer_display/customer_display.js`, `addons/point_of_sale/static/src/@types/registry.d.ts`, `addons/point_of_sale/static/src/@types/services.d.ts`, `addons/point_of_sale/static/src/overrides/sound_effects_plugin.js`, `addons/point_of_sale/static/src/overrides/ui_service.js`, `addons/point_of_sale/static/src/overrides/action_plugin.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/point_of_sale/__manifest__.py`
- **HTTP entry points:** `addons/point_of_sale/controllers/customer_display.py:11`, `addons/point_of_sale/controllers/customer_display.py:34`, `addons/point_of_sale/controllers/binary.py:7`, `addons/point_of_sale/controllers/main.py:19`, `addons/point_of_sale/controllers/main.py:32`, `addons/point_of_sale/controllers/main.py:49`, `addons/point_of_sale/controllers/main.py:53`, `addons/point_of_sale/controllers/main.py:121`, `addons/point_of_sale/controllers/main.py:125`, `addons/point_of_sale/controllers/main.py:132`, `addons/point_of_sale/controllers/main.py:176`
- **Scheduled entry points:** `addons/point_of_sale/__manifest__.py`, `addons/point_of_sale/models/res_config_settings.py`, `addons/point_of_sale/models/pos_session.py`, `addons/point_of_sale/models/pos_order.py`, `addons/point_of_sale/models/pos_snooze.py`, `addons/point_of_sale/data/ir_cron_data.xml`, `addons/point_of_sale/views/res_config_settings_views.xml`, `addons/point_of_sale/views/pos_order_view.xml`, `addons/point_of_sale/tests/test_pos_accounting.py`
- **Report entry points:** `addons/point_of_sale/models/pos_order.py`, `addons/point_of_sale/controllers/main.py`, `addons/point_of_sale/receipt/pos_order_receipt.py`, `addons/point_of_sale/views/point_of_sale_report.xml`, `addons/point_of_sale/tests/test_report_session.py`

## 7. Database interactions

- Model declarations: 67
- Representative model evidence: `pos.prep.line` (addons/point_of_sale/models/pos_prep_line.py:5); `product.category` (addons/point_of_sale/models/product_category.py:5); `res.partner` (addons/point_of_sale/models/res_partner.py:6); `product.product` (addons/point_of_sale/models/product_product.py:5); `product.combo` (addons/point_of_sale/models/product_combo.py:7); `res.lang` (addons/point_of_sale/models/res_lang.py:4); `product.attribute` (addons/point_of_sale/models/product_attribute.py:5); `product.attribute.custom.value` (addons/point_of_sale/models/product_attribute.py:14); `product.template.attribute.line` (addons/point_of_sale/models/product_attribute.py:34); `product.template.attribute.value` (addons/point_of_sale/models/product_attribute.py:51); `uom.uom` (addons/point_of_sale/models/uom.py:4); inherits `barcode.rule` (addons/point_of_sale/models/barcode_rule.py:8); inherits `digest.digest` (addons/point_of_sale/models/digest.py:7); `product.template` (addons/point_of_sale/models/product_template.py:11); inherits `account.bank.statement` (addons/point_of_sale/models/account_bank_statement.py:5); `pos.payment` (addons/point_of_sale/models/pos_payment.py:8); `ir.ui.view` (addons/point_of_sale/models/ir_ui_view.py:4); inherits `res.groups` (addons/point_of_sale/models/res_groups.py:6); `pos.config` (addons/point_of_sale/models/pos_config.py:22); `pos.bill` (addons/point_of_sale/models/pos_bill.py:5); `product.uom` (addons/point_of_sale/models/product_uom.py:4); inherits `res.config.settings` (addons/point_of_sale/models/res_config_settings.py:8); `product.combo.item` (addons/point_of_sale/models/product_combo_item.py:6); inherits `ir.sequence` (addons/point_of_sale/models/ir_sequence.py:5); `res.currency` (addons/point_of_sale/models/res_currency.py:4); `product.pricelist` (addons/point_of_sale/models/product_pricelist.py:7); `product.pricelist.item` (addons/point_of_sale/models/product_pricelist.py:43); `pos.category` (addons/point_of_sale/models/pos_category.py:11); inherits `account.payment` (addons/point_of_sale/models/account_payment.py:7); `pos.note` (addons/point_of_sale/models/pos_note.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 4
- Route declarations: 11
- Route evidence: `addons/point_of_sale/controllers/customer_display.py:11`, `addons/point_of_sale/controllers/customer_display.py:34`, `addons/point_of_sale/controllers/binary.py:7`, `addons/point_of_sale/controllers/main.py:19`, `addons/point_of_sale/controllers/main.py:32`, `addons/point_of_sale/controllers/main.py:49`, `addons/point_of_sale/controllers/main.py:53`, `addons/point_of_sale/controllers/main.py:121`, `addons/point_of_sale/controllers/main.py:125`, `addons/point_of_sale/controllers/main.py:132`, `addons/point_of_sale/controllers/main.py:176`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `resource`, `product`, `account`, `barcodes_gs1_nomenclature`, `html_editor`, `digest`, `phone_validation`, `google_address_autocomplete`, `base_report_wkhtmltox`, `iot_webserial`
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

- `addons/point_of_sale/README.md`
- `addons/point_of_sale/__init__.py`
- `addons/point_of_sale/__manifest__.py`
- `addons/point_of_sale/controllers/__init__.py`
- `addons/point_of_sale/controllers/binary.py`
- `addons/point_of_sale/controllers/customer_display.py`
- `addons/point_of_sale/controllers/main.py`
- `addons/point_of_sale/data/default_barcode_patterns.xml`
- `addons/point_of_sale/data/demo_data.xml`
- `addons/point_of_sale/data/digest_data.xml`
- `addons/point_of_sale/data/ir_config_parameter_data.xml`
- `addons/point_of_sale/data/ir_cron_data.xml`
- `addons/point_of_sale/data/mail_template_data.xml`
- `addons/point_of_sale/data/orders_demo.xml`
- `addons/point_of_sale/data/point_of_sale_data.xml`
- `addons/point_of_sale/data/point_of_sale_tour.xml`
- `addons/point_of_sale/data/pos_note_data.xml`
- `addons/point_of_sale/data/scenarios/bakery_category_data.xml`
- `addons/point_of_sale/data/scenarios/bakery_data.xml`
- `addons/point_of_sale/data/scenarios/clothes_category_data.xml`
- `addons/point_of_sale/data/scenarios/clothes_data.xml`
- `addons/point_of_sale/data/scenarios/furniture_category_data.xml`
- `addons/point_of_sale/data/scenarios/furniture_data.xml`
- `addons/point_of_sale/doc/barcode_test_sheet.pdf`
- `addons/point_of_sale/doc/barcode_test_sheet.svg`
- `addons/point_of_sale/doc/barcode_test_sheet2.svg`
- `addons/point_of_sale/doc/barcode_test_sheet4.pdf`
- `addons/point_of_sale/doc/barcode_test_sheet4.svg`
- `addons/point_of_sale/doc/barcode_test_sheet_new.svg`
- `addons/point_of_sale/i18n/af.po`
- `addons/point_of_sale/i18n/ar.po`
- `addons/point_of_sale/i18n/az.po`
- `addons/point_of_sale/i18n/bg.po`
- `addons/point_of_sale/i18n/bs.po`
- `addons/point_of_sale/i18n/ca.po`
- `addons/point_of_sale/i18n/cs.po`
- `addons/point_of_sale/i18n/da.po`
- `addons/point_of_sale/i18n/de.po`
- `addons/point_of_sale/i18n/el.po`
- `addons/point_of_sale/i18n/es.po`
- `addons/point_of_sale/i18n/es_419.po`
- `addons/point_of_sale/i18n/es_CL.po`
- `addons/point_of_sale/i18n/et.po`
- `addons/point_of_sale/i18n/eu.po`
- `addons/point_of_sale/i18n/fa.po`
- `addons/point_of_sale/i18n/fi.po`
- `addons/point_of_sale/i18n/fr.po`
- `addons/point_of_sale/i18n/fr_CA.po`
- `addons/point_of_sale/i18n/gl.po`
- `addons/point_of_sale/i18n/gu.po`
- `addons/point_of_sale/i18n/he.po`
- `addons/point_of_sale/i18n/hi.po`
- `addons/point_of_sale/i18n/hr.po`
- `addons/point_of_sale/i18n/hu.po`
- `addons/point_of_sale/i18n/id.po`
- `addons/point_of_sale/i18n/is.po`
- `addons/point_of_sale/i18n/it.po`
- `addons/point_of_sale/i18n/ja.po`
- `addons/point_of_sale/i18n/ka.po`
- `addons/point_of_sale/i18n/kab.po`
- `addons/point_of_sale/i18n/km.po`
- `addons/point_of_sale/i18n/ko.po`
- `addons/point_of_sale/i18n/ku.po`
- `addons/point_of_sale/i18n/lb.po`
- `addons/point_of_sale/i18n/lo.po`
- `addons/point_of_sale/i18n/lt.po`
- `addons/point_of_sale/i18n/lv.po`
- `addons/point_of_sale/i18n/mk.po`
- `addons/point_of_sale/i18n/mn.po`
- `addons/point_of_sale/i18n/my.po`
- `addons/point_of_sale/i18n/nb.po`
- `addons/point_of_sale/i18n/nl.po`
- `addons/point_of_sale/i18n/pl.po`
- `addons/point_of_sale/i18n/point_of_sale.pot`
- `addons/point_of_sale/i18n/pt.po`
- `addons/point_of_sale/i18n/pt_BR.po`
- `addons/point_of_sale/i18n/ro.po`
- `addons/point_of_sale/i18n/ru.po`
- `addons/point_of_sale/i18n/sk.po`
- `addons/point_of_sale/i18n/sl.po`
- `addons/point_of_sale/i18n/sr@latin.po`
- `addons/point_of_sale/i18n/sv.po`
- `addons/point_of_sale/i18n/th.po`
- `addons/point_of_sale/i18n/tr.po`
- `addons/point_of_sale/i18n/uk.po`
- `addons/point_of_sale/i18n/uz.po`
- `addons/point_of_sale/i18n/vi.po`
- `addons/point_of_sale/i18n/zh_CN.po`
- `addons/point_of_sale/i18n/zh_TW.po`
- `addons/point_of_sale/models/__init__.py`
- `addons/point_of_sale/models/account_account.py`
- `addons/point_of_sale/models/account_bank_statement.py`
- `addons/point_of_sale/models/account_bank_statement_line.py`
- `addons/point_of_sale/models/account_cash_rounding.py`
- `addons/point_of_sale/models/account_fiscal_position.py`
- `addons/point_of_sale/models/account_journal.py`
- `addons/point_of_sale/models/account_move.py`
- `addons/point_of_sale/models/account_move_line.py`
- `addons/point_of_sale/models/account_payment.py`
- `addons/point_of_sale/models/account_tax.py`
- `addons/point_of_sale/models/account_tax_group.py`
- `addons/point_of_sale/models/barcode_rule.py`
- `addons/point_of_sale/models/decimal_precision.py`
- `addons/point_of_sale/models/digest.py`
- `addons/point_of_sale/models/ir_http.py`
- `addons/point_of_sale/models/ir_sequence.py`
- `addons/point_of_sale/models/ir_ui_view.py`
- `addons/point_of_sale/models/pos_bill.py`
- `addons/point_of_sale/models/pos_bus_mixin.py`
- `addons/point_of_sale/models/pos_category.py`
- `addons/point_of_sale/models/pos_config.py`
- `addons/point_of_sale/models/pos_load_mixin.py`
- `addons/point_of_sale/models/pos_note.py`
- `addons/point_of_sale/models/pos_order.py`
- `addons/point_of_sale/models/pos_order_line.py`
- `addons/point_of_sale/models/pos_payment.py`
- `addons/point_of_sale/models/pos_payment_method.py`
- `addons/point_of_sale/models/pos_prep_line.py`
- `addons/point_of_sale/models/pos_prep_order.py`
- `addons/point_of_sale/models/pos_preset.py`
- `addons/point_of_sale/models/pos_printer.py`
- `addons/point_of_sale/models/pos_session.py`
- `addons/point_of_sale/models/pos_snooze.py`
- `addons/point_of_sale/models/product_attribute.py`
- `addons/point_of_sale/models/product_category.py`
- `addons/point_of_sale/models/product_combo.py`
- `addons/point_of_sale/models/product_combo_item.py`
- `addons/point_of_sale/models/product_pricelist.py`
- `addons/point_of_sale/models/product_product.py`
- `addons/point_of_sale/models/product_tag.py`
- `addons/point_of_sale/models/product_template.py`
- `addons/point_of_sale/models/product_uom.py`
- `addons/point_of_sale/models/report_sale_details.py`
- `addons/point_of_sale/models/res_company.py`
- `addons/point_of_sale/models/res_config_settings.py`
- `addons/point_of_sale/models/res_country.py`
- `addons/point_of_sale/models/res_country_state.py`
- `addons/point_of_sale/models/res_currency.py`
- `addons/point_of_sale/models/res_groups.py`
- `addons/point_of_sale/models/res_lang.py`
- `addons/point_of_sale/models/res_partner.py`
- `addons/point_of_sale/models/res_users.py`
- `addons/point_of_sale/models/resource_calendar_attendance.py`
- `addons/point_of_sale/models/uom.py`
- `addons/point_of_sale/receipt/__init__.py`
- `addons/point_of_sale/receipt/pos_cash_move_receipt.xml`
- `addons/point_of_sale/receipt/pos_order_change_receipt.xml`
- `addons/point_of_sale/receipt/pos_order_change_receipt_zpl.xml`
- `addons/point_of_sale/receipt/pos_order_receipt.py`
- `addons/point_of_sale/receipt/pos_order_receipt.xml`
- `addons/point_of_sale/receipt/pos_receipt_common.xml`
- `addons/point_of_sale/receipt/pos_sale_details_receipt.xml`
- `addons/point_of_sale/receipt/pos_tip_receipt.xml`
- `addons/point_of_sale/report/__init__.py`
- `addons/point_of_sale/report/pos_invoice.py`
- `addons/point_of_sale/report/pos_order_report.py`
- `addons/point_of_sale/security/ir.access.csv`
- `addons/point_of_sale/security/point_of_sale_security.xml`
- `addons/point_of_sale/static/description/icon.png`
- `addons/point_of_sale/static/description/icon.svg`
- `addons/point_of_sale/static/description/icon_hi.png`
- `addons/point_of_sale/static/img/bakery-icon.svg`
- `addons/point_of_sale/static/img/barcode.png`
- `addons/point_of_sale/static/img/breads-icon.png`
- `addons/point_of_sale/static/img/casual_denim_short.png`
- `addons/point_of_sale/static/img/chair_category.png`
- `addons/point_of_sale/static/img/classic_leather_belt.png`
- `addons/point_of_sale/static/img/clothes-icon.svg`
- `addons/point_of_sale/static/img/cocktail-icon.svg`
- `addons/point_of_sale/static/img/cozy_sweater.png`
- `addons/point_of_sale/static/img/desk_category.png`
- `addons/point_of_sale/static/img/furniture-icon.svg`
- `addons/point_of_sale/static/img/jean_jacket.png`
- `addons/point_of_sale/static/img/leather_jacket.png`
- `addons/point_of_sale/static/img/led_lamp.png`
- `addons/point_of_sale/static/img/letter_tray.png`
- `addons/point_of_sale/static/img/lna_config/image.png`
- `addons/point_of_sale/static/img/lna_config/image_1.png`
- `addons/point_of_sale/static/img/lna_config/image_2.png`
- `addons/point_of_sale/static/img/lna_config/image_3.png`
- `addons/point_of_sale/static/img/lna_config/image_4.png`
- `addons/point_of_sale/static/img/lna_config/image_5.png`
- `addons/point_of_sale/static/img/lna_config/image_6.png`
- `addons/point_of_sale/static/img/lna_config/image_7.png`
- `addons/point_of_sale/static/img/lna_config/image_8.png`
- `addons/point_of_sale/static/img/lna_config/image_9.png`
- `addons/point_of_sale/static/img/lower-body-icon.png`
- `addons/point_of_sale/static/img/magnetic_board.png`
- `addons/point_of_sale/static/img/misc_category.png`
- `addons/point_of_sale/static/img/newspaper_stand.png`
- `addons/point_of_sale/static/img/others-icon.png`
- `addons/point_of_sale/static/img/partners/acsone.png`
- `addons/point_of_sale/static/img/partners/bhc.jpg`
- `addons/point_of_sale/static/img/partners/camptocamp.png`
- `addons/point_of_sale/static/img/partners/cocktail-icon.svg`
- `addons/point_of_sale/static/img/partners/datalp.jpg`
- `addons/point_of_sale/static/img/partners/eezee-it.png`
- `addons/point_of_sale/static/img/partners/eggs-solutions.jpg`
- `addons/point_of_sale/static/img/partners/ekomurz.gif`
- `addons/point_of_sale/static/img/partners/openbig.jpg`
- `addons/point_of_sale/static/img/partners/services.jpg`
- `addons/point_of_sale/static/img/partners/vauxoo.png`
- `addons/point_of_sale/static/img/pastries-icon.png`
- `addons/point_of_sale/static/img/product_apple_pie.png`
- `addons/point_of_sale/static/img/product_bagel.png`
- `addons/point_of_sale/static/img/product_bar_chair.png`
- `addons/point_of_sale/static/img/product_blue_denim_jeans.png`
- `addons/point_of_sale/static/img/product_blue_denim_jeans_slim.png`
- `addons/point_of_sale/static/img/product_blueberry_muffin.png`
- `addons/point_of_sale/static/img/product_butter_croissant.png`
- `addons/point_of_sale/static/img/product_casual_t_shirt.png`
- `addons/point_of_sale/static/img/product_cheese_croissant.png`
- `addons/point_of_sale/static/img/product_cherry_pie.png`
- `addons/point_of_sale/static/img/product_cinnamon_roll.png`
- `addons/point_of_sale/static/img/product_classic_brown_jacket.png`
- `addons/point_of_sale/static/img/product_cofgee_table.png`
- `addons/point_of_sale/static/img/product_crocheted_poncho_unisize.png`
- `addons/point_of_sale/static/img/product_ergonomic_chair.png`
- `addons/point_of_sale/static/img/product_flour.png`
- `addons/point_of_sale/static/img/product_folding_desk.png`
- `addons/point_of_sale/static/img/product_gaming_desk.png`
- `addons/point_of_sale/static/img/product_hood.png`
- `addons/point_of_sale/static/img/product_leather_desk_chair.png`
- `addons/point_of_sale/static/img/product_multigrain_bread.png`
- `addons/point_of_sale/static/img/product_odoo_sneakers.png`
- `addons/point_of_sale/static/img/product_pain_au_chocolat.png`
- `addons/point_of_sale/static/img/product_pecan_pie.png`
- `addons/point_of_sale/static/img/product_rye_bread.png`
- `addons/point_of_sale/static/img/product_sourdough_loaf.png`
- `addons/point_of_sale/static/img/product_standing_desk.png`
- `addons/point_of_sale/static/img/product_t_shirt_black_embroidered.png`
- `addons/point_of_sale/static/img/product_t_shirt_pants.png`
- `addons/point_of_sale/static/img/product_t_shirt_slim.png`
- `addons/point_of_sale/static/img/product_tiger_white_loaf.png`
- `addons/point_of_sale/static/img/product_wholemeal_loaf.png`
- `addons/point_of_sale/static/img/product_wooden_chair.png`
- `addons/point_of_sale/static/img/providers/adyen.png`
- `addons/point_of_sale/static/img/providers/bancontact_pay.png`
- `addons/point_of_sale/static/img/providers/cashdro.png`
- `addons/point_of_sale/static/img/providers/cashmatic.png`
- `addons/point_of_sale/static/img/providers/dpopay.png`
- `addons/point_of_sale/static/img/providers/glory.png`
- `addons/point_of_sale/static/img/providers/mercado_pago.png`
- `addons/point_of_sale/static/img/providers/mollie.png`
- `addons/point_of_sale/static/img/providers/pine_labs.png`
- `addons/point_of_sale/static/img/providers/qfpay.png`
- `addons/point_of_sale/static/img/providers/razorpay.png`
- `addons/point_of_sale/static/img/providers/safaricom.png`
- `addons/point_of_sale/static/img/providers/six.png`
- `addons/point_of_sale/static/img/providers/six_iot.png`
- Additional source files not expanded in this page: 635; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
