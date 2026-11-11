# Module: l10n_in_pos

- **Module ID:** MOD-234
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_in_pos`
- **Manifest:** `addons/l10n_in_pos/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

GST Point of Sale

**Scope evidence:** The module contains 56 files, including 27 Python, 13 XML, and 14 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_in`, `point_of_sale`.

## 2. Module structure

- Model/business logic files: 14
- Controller/API files: 0
- XML/data/view/template files: 13
- Browser asset files: 14
- Security files: 0
- Test files: 9
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 14 model declarations, 45 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/l10n_in_pos/models/product_template.py:6`, `addons/l10n_in_pos/models/pos_config.py:4`, `addons/l10n_in_pos/models/pos_bill.py:5`, `addons/l10n_in_pos/models/product.py:6`, `addons/l10n_in_pos/models/pos_session.py:4`, `addons/l10n_in_pos/models/account_tax.py:4`, `addons/l10n_in_pos/models/pos_order.py:4`, `addons/l10n_in_pos/models/pos_payment_method.py:8`, `addons/l10n_in_pos/models/account_move.py:5`, `addons/l10n_in_pos/models/account_move_line.py:4`, `addons/l10n_in_pos/models/res_partner_bank.py:6`, `addons/l10n_in_pos/models/pos_order_line.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 13 XML files and 14 JavaScript/TypeScript files; static XML analysis found 24 record/template/menu identifiers.
- **Evidence:** `addons/l10n_in_pos/data/pos_bill_data.xml:3`, `addons/l10n_in_pos/data/product_demo.xml:3`, `addons/l10n_in_pos/data/product_demo.xml:6`, `addons/l10n_in_pos/data/product_demo.xml:9`, `addons/l10n_in_pos/data/product_demo.xml:12`, `addons/l10n_in_pos/data/product_demo.xml:15`, `addons/l10n_in_pos/data/product_demo.xml:18`, `addons/l10n_in_pos/data/product_demo.xml:21`, `addons/l10n_in_pos/data/product_demo.xml:24`, `addons/l10n_in_pos/data/product_demo.xml:27`, `addons/l10n_in_pos/data/product_demo.xml:30`, `addons/l10n_in_pos/data/product_demo.xml:33`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 9 test files are present.
- **Evidence:** `addons/l10n_in_pos/tests/test_gstr_section.py`, `addons/l10n_in_pos/tests/test_hsn_summary.py`, `addons/l10n_in_pos/tests/test_standard_flows.py`, `addons/l10n_in_pos/tests/test_in_pos.py`, `addons/l10n_in_pos/tests/test_product_screen.py`, `addons/l10n_in_pos/tests/test_pos_flow.py`, `addons/l10n_in_pos/tests/common.py`, `addons/l10n_in_pos/tests/__init__.py`, `addons/l10n_in_pos/tests/test_order_receipt.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 13; representative identifiers: `500_00`, `product.desk_organizer`, `product.desk_pad`, `point_of_sale.led_lamp`, `point_of_sale.letter_tray`, `point_of_sale.magnetic_board`, `product.monitor_stand`, `point_of_sale.newspaper_rack`, `point_of_sale.small_shelf`, `point_of_sale.product_product_tip`, `point_of_sale.wall_shelf`, `point_of_sale.whiteboard`, `point_of_sale.whiteboard_pen`, `l10n_in_pos.pos_order_receipt`, `l10n_in_pos.pos_order_receipt_header`, `l10n_in_pos.pos_orderline_receipt_information`, `pos_payment_method_view_form_inherit_l10n_in_pos`, `res_config_settings_view_form_l10n_in_pos_inherit`, `l10n_in_pos.report_invoice_document`, `l10n_in_pos.product_template_view_form_normalized_pos`
- Menus: 0; representative evidence: Not found in module
- Templates: 4; representative evidence: `addons/l10n_in_pos/receipt/pos_order_receipt.xml:4`, `addons/l10n_in_pos/receipt/pos_order_receipt.xml:31`, `addons/l10n_in_pos/receipt/pos_order_receipt.xml:44`, `addons/l10n_in_pos/views/report_invoice.xml:3`
- View/action field declarations: 14; representative evidence: `addons/l10n_in_pos/views/pos_payment_method_views.xml:5`, `addons/l10n_in_pos/views/pos_payment_method_views.xml:7`, `addons/l10n_in_pos/views/res_config_settings_views.xml:5`, `addons/l10n_in_pos/views/res_config_settings_views.xml:7`, `addons/l10n_in_pos/views/product_view.xml:5`, `addons/l10n_in_pos/views/product_view.xml:7`, `addons/l10n_in_pos/views/product_view.xml:16`, `addons/l10n_in_pos/views/product_view.xml:18`, `addons/l10n_in_pos/views/product_view.xml:27`, `addons/l10n_in_pos/views/product_view.xml:28`, `addons/l10n_in_pos/views/res_partner_views.xml:5`, `addons/l10n_in_pos/views/res_partner_views.xml:7`
- Browser assets: 14; representative files: `addons/l10n_in_pos/static/src/app/models/invoice_button.js`, `addons/l10n_in_pos/static/src/app/models/payment_screen.js`, `addons/l10n_in_pos/static/src/app/models/pos_order_line.js`, `addons/l10n_in_pos/static/src/app/models/pos_order.js`, `addons/l10n_in_pos/static/src/app/models/pos_payment.js`, `addons/l10n_in_pos/static/src/app/components/popups/company_state_dialog/company_state_dialog.js`, `addons/l10n_in_pos/static/src/app/components/popups/qr_code_popup/qr_code_popup.js`, `addons/l10n_in_pos/static/src/app/components/popups/hsn_code_dialog/hsn_code_dialog.js`, `addons/l10n_in_pos/static/src/app/components/popups/cash_move_popup/cash_move_popup.js`, `addons/l10n_in_pos/static/src/app/components/popups/closing_popup/closing_popup.js`, `addons/l10n_in_pos/static/src/app/components/popups/product_info_popup/product_info_popup.js`, `addons/l10n_in_pos/static/src/app/utils/printer/generate_printer_data.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_in_pos/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 14
- Representative model evidence: inherits `product.template` (addons/l10n_in_pos/models/product_template.py:6); inherits `pos.config` (addons/l10n_in_pos/models/pos_config.py:4); inherits `pos.bill` (addons/l10n_in_pos/models/pos_bill.py:5); inherits `product.product` (addons/l10n_in_pos/models/product.py:6); inherits `pos.session` (addons/l10n_in_pos/models/pos_session.py:4); inherits `account.tax` (addons/l10n_in_pos/models/account_tax.py:4); inherits `pos.order` (addons/l10n_in_pos/models/pos_order.py:4); inherits `pos.payment.method` (addons/l10n_in_pos/models/pos_payment_method.py:8); inherits `account.move` (addons/l10n_in_pos/models/account_move.py:5); inherits `account.move.line` (addons/l10n_in_pos/models/account_move_line.py:4); inherits `res.partner.bank` (addons/l10n_in_pos/models/res_partner_bank.py:6); inherits `pos.order.line` (addons/l10n_in_pos/models/pos_order_line.py:7); inherits `res.company` (addons/l10n_in_pos/models/res_company.py:6); inherits `pos.order.receipt` (addons/l10n_in_pos/receipt/pos_order_receipt.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_in`, `point_of_sale`
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

- `addons/l10n_in_pos/__init__.py`
- `addons/l10n_in_pos/__manifest__.py`
- `addons/l10n_in_pos/data/pos_bill_data.xml`
- `addons/l10n_in_pos/data/product_demo.xml`
- `addons/l10n_in_pos/i18n/hi.po`
- `addons/l10n_in_pos/i18n/l10n_in_pos.pot`
- `addons/l10n_in_pos/models/__init__.py`
- `addons/l10n_in_pos/models/account_move.py`
- `addons/l10n_in_pos/models/account_move_line.py`
- `addons/l10n_in_pos/models/account_tax.py`
- `addons/l10n_in_pos/models/pos_bill.py`
- `addons/l10n_in_pos/models/pos_config.py`
- `addons/l10n_in_pos/models/pos_order.py`
- `addons/l10n_in_pos/models/pos_order_line.py`
- `addons/l10n_in_pos/models/pos_payment_method.py`
- `addons/l10n_in_pos/models/pos_session.py`
- `addons/l10n_in_pos/models/product.py`
- `addons/l10n_in_pos/models/product_template.py`
- `addons/l10n_in_pos/models/res_company.py`
- `addons/l10n_in_pos/models/res_partner_bank.py`
- `addons/l10n_in_pos/receipt/__init__.py`
- `addons/l10n_in_pos/receipt/pos_order_receipt.py`
- `addons/l10n_in_pos/receipt/pos_order_receipt.xml`
- `addons/l10n_in_pos/static/src/app/components/popups/cash_move_popup/cash_move_popup.js`
- `addons/l10n_in_pos/static/src/app/components/popups/closing_popup/closing_popup.js`
- `addons/l10n_in_pos/static/src/app/components/popups/company_state_dialog/company_state_dialog.js`
- `addons/l10n_in_pos/static/src/app/components/popups/company_state_dialog/company_state_dialog.xml`
- `addons/l10n_in_pos/static/src/app/components/popups/hsn_code_dialog/hsn_code_dialog.js`
- `addons/l10n_in_pos/static/src/app/components/popups/hsn_code_dialog/hsn_code_dialog.xml`
- `addons/l10n_in_pos/static/src/app/components/popups/product_info_popup/product_info_popup.js`
- `addons/l10n_in_pos/static/src/app/components/popups/qr_code_popup/qr_code_popup.js`
- `addons/l10n_in_pos/static/src/app/components/popups/qr_code_popup/qr_code_popup.xml`
- `addons/l10n_in_pos/static/src/app/models/invoice_button.js`
- `addons/l10n_in_pos/static/src/app/models/payment_screen.js`
- `addons/l10n_in_pos/static/src/app/models/pos_order.js`
- `addons/l10n_in_pos/static/src/app/models/pos_order_line.js`
- `addons/l10n_in_pos/static/src/app/models/pos_payment.js`
- `addons/l10n_in_pos/static/src/app/utils/printer/generate_printer_data.js`
- `addons/l10n_in_pos/static/src/customer_display/customer_display.xml`
- `addons/l10n_in_pos/static/tests/tours/product_screen_tour.js`
- `addons/l10n_in_pos/static/tests/tours/test_hsn_summary.js`
- `addons/l10n_in_pos/tests/__init__.py`
- `addons/l10n_in_pos/tests/common.py`
- `addons/l10n_in_pos/tests/test_gstr_section.py`
- `addons/l10n_in_pos/tests/test_hsn_summary.py`
- `addons/l10n_in_pos/tests/test_in_pos.py`
- `addons/l10n_in_pos/tests/test_order_receipt.py`
- `addons/l10n_in_pos/tests/test_pos_flow.py`
- `addons/l10n_in_pos/tests/test_product_screen.py`
- `addons/l10n_in_pos/tests/test_standard_flows.py`
- `addons/l10n_in_pos/views/pos_order_line_views.xml`
- `addons/l10n_in_pos/views/pos_payment_method_views.xml`
- `addons/l10n_in_pos/views/product_view.xml`
- `addons/l10n_in_pos/views/report_invoice.xml`
- `addons/l10n_in_pos/views/res_config_settings_views.xml`
- `addons/l10n_in_pos/views/res_partner_views.xml`
