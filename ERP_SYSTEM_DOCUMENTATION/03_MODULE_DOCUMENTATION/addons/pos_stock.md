# Module: pos_stock

- **Module ID:** MOD-464
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_stock`
- **Manifest:** `addons/pos_stock/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Stock integration for PoS

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 154 files, including 38 Python, 17 XML, and 48 JavaScript/TypeScript files. The manifest declares dependencies: `point_of_sale`, `stock_account`.

## 2. Module structure

- Model/business logic files: 19
- Controller/API files: 0
- XML/data/view/template files: 17
- Browser asset files: 48
- Security files: 2
- Test files: 16
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/pos_stock/security/pos_stock_security.xml`, `addons/pos_stock/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 19 model declarations, 176 methods, 1 constraint handlers, 0 onchange handlers, and 6 dependency declarations.
- **Evidence:** `addons/pos_stock/models/product_category.py:5`, `addons/pos_stock/models/product_removal.py:4`, `addons/pos_stock/models/product_template.py:5`, `addons/pos_stock/models/pos_config.py:4`, `addons/pos_stock/models/res_config_settings.py:4`, `addons/pos_stock/models/stock_move.py:5`, `addons/pos_stock/models/pos_session.py:8`, `addons/pos_stock/models/pos_pack_operation_lot.py:4`, `addons/pos_stock/models/pos_order.py:4`, `addons/pos_stock/models/stock_picking.py:6`, `addons/pos_stock/models/stock_picking.py:162`, `addons/pos_stock/models/account_move.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 17 XML files and 48 JavaScript/TypeScript files; static XML analysis found 9 record/template/menu identifiers.
- **Evidence:** `addons/pos_stock/security/pos_stock_security.xml:4`, `addons/pos_stock/receipt/pos_order_receipt.xml:4`, `addons/pos_stock/receipt/pos_order_receipt.xml:14`, `addons/pos_stock/views/pos_config_view.xml:4`, `addons/pos_stock/views/stock_reference_views.xml:3`, `addons/pos_stock/views/res_config_settings_views.xml:4`, `addons/pos_stock/views/product_view.xml:4`, `addons/pos_stock/views/pos_session_view.xml:4`, `addons/pos_stock/views/pos_order_view.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/pos_stock/security/pos_stock_security.xml`, `addons/pos_stock/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/pos_stock/models/stock_rule.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 16 test files are present.
- **Evidence:** `addons/pos_stock/tests/test_pos_stock_account.py`, `addons/pos_stock/tests/test_pos_accounting.py`, `addons/pos_stock/tests/test_pos_stock_flow.py`, `addons/pos_stock/tests/test_pos_stock_margin.py`, `addons/pos_stock/tests/test_anglo_saxon.py`, `addons/pos_stock/tests/test_frontend.py`, `addons/pos_stock/tests/test_pos_stock_basic_config.py`, `addons/pos_stock/tests/test_pos_stock.py`, `addons/pos_stock/tests/common.py`, `addons/pos_stock/tests/test_pos_picking_backorder.py`, `addons/pos_stock/tests/test_pos_stock_other_currency_config.py`, `addons/pos_stock/tests/test_pos_stock_order_receipt.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 17; representative identifiers: `point_of_sale.group_pos_manager`, `pos_stock.pos_orderline_receipt_information`, `pos_stock.pos_order_receipt_footer`, `view_pos_config_search`, `stock_reference_view_form`, `res_config_settings_view_form`, `product_template_view_form_normalized_pos`, `view_pos_session_form`, `view_pos_pos_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/pos_stock/receipt/pos_order_receipt.xml:4`, `addons/pos_stock/receipt/pos_order_receipt.xml:14`
- View/action field declarations: 12; representative evidence: `addons/pos_stock/views/pos_config_view.xml:6`, `addons/pos_stock/views/pos_config_view.xml:8`, `addons/pos_stock/views/stock_reference_views.xml:5`, `addons/pos_stock/views/stock_reference_views.xml:7`, `addons/pos_stock/views/res_config_settings_views.xml:6`, `addons/pos_stock/views/res_config_settings_views.xml:8`, `addons/pos_stock/views/product_view.xml:6`, `addons/pos_stock/views/product_view.xml:8`, `addons/pos_stock/views/pos_session_view.xml:6`, `addons/pos_stock/views/pos_session_view.xml:8`, `addons/pos_stock/views/pos_order_view.xml:5`, `addons/pos_stock/views/pos_order_view.xml:7`
- Browser assets: 48; representative files: `addons/pos_stock/static/src/app/services/pos_store.js`, `addons/pos_stock/static/src/app/models/data_service_options.js`, `addons/pos_stock/static/src/app/models/pos_order_line.js`, `addons/pos_stock/static/src/app/models/product_template.js`, `addons/pos_stock/static/src/app/models/pos_order.js`, `addons/pos_stock/static/src/app/utils/order_payment_validation.js`, `addons/pos_stock/static/src/app/utils/generate_printer_data.js`, `addons/pos_stock/static/src/app/models/accounting/product_template_accounting.js`, `addons/pos_stock/static/src/app/screens/ticket_screen/ticket_screen.js`, `addons/pos_stock/static/src/app/screens/payment_screen/payment_screen.js`, `addons/pos_stock/static/src/app/screens/product_screen/order_summary/order_summary.js`, `addons/pos_stock/static/src/app/components/orderline/orderline.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_stock/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/pos_stock/models/stock_rule.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 19
- Representative model evidence: inherits `product.category` (addons/pos_stock/models/product_category.py:5); `product.removal` (addons/pos_stock/models/product_removal.py:4); inherits `product.template` (addons/pos_stock/models/product_template.py:5); inherits `pos.config` (addons/pos_stock/models/pos_config.py:4); inherits `res.config.settings` (addons/pos_stock/models/res_config_settings.py:4); inherits `stock.move` (addons/pos_stock/models/stock_move.py:5); inherits `pos.session` (addons/pos_stock/models/pos_session.py:8); `pos.pack.operation.lot` (addons/pos_stock/models/pos_pack_operation_lot.py:4); inherits `pos.order` (addons/pos_stock/models/pos_order.py:4); inherits `stock.picking` (addons/pos_stock/models/stock_picking.py:6); `stock.picking.type` (addons/pos_stock/models/stock_picking.py:162); inherits `account.move` (addons/pos_stock/models/account_move.py:4); inherits `stock.rule` (addons/pos_stock/models/stock_rule.py:4); inherits `account.move.line` (addons/pos_stock/models/account_move_line.py:4); inherits `pos.order.line` (addons/pos_stock/models/pos_order_line.py:7); inherits `stock.warehouse` (addons/pos_stock/models/stock_warehouse.py:4); inherits `stock.reference` (addons/pos_stock/models/stock_reference.py:4); inherits `res.company` (addons/pos_stock/models/res_company.py:4); inherits `pos.order.receipt` (addons/pos_stock/receipt/pos_order_receipt.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `point_of_sale`, `stock_account`
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

- `addons/pos_stock/__init__.py`
- `addons/pos_stock/__manifest__.py`
- `addons/pos_stock/data/pos_stock_data.xml`
- `addons/pos_stock/i18n/ar.po`
- `addons/pos_stock/i18n/az.po`
- `addons/pos_stock/i18n/bg.po`
- `addons/pos_stock/i18n/bs.po`
- `addons/pos_stock/i18n/ca.po`
- `addons/pos_stock/i18n/cs.po`
- `addons/pos_stock/i18n/da.po`
- `addons/pos_stock/i18n/de.po`
- `addons/pos_stock/i18n/el.po`
- `addons/pos_stock/i18n/es.po`
- `addons/pos_stock/i18n/es_419.po`
- `addons/pos_stock/i18n/et.po`
- `addons/pos_stock/i18n/fa.po`
- `addons/pos_stock/i18n/fi.po`
- `addons/pos_stock/i18n/fr.po`
- `addons/pos_stock/i18n/he.po`
- `addons/pos_stock/i18n/hi.po`
- `addons/pos_stock/i18n/hr.po`
- `addons/pos_stock/i18n/hu.po`
- `addons/pos_stock/i18n/id.po`
- `addons/pos_stock/i18n/it.po`
- `addons/pos_stock/i18n/ja.po`
- `addons/pos_stock/i18n/kab.po`
- `addons/pos_stock/i18n/ko.po`
- `addons/pos_stock/i18n/ku.po`
- `addons/pos_stock/i18n/lo.po`
- `addons/pos_stock/i18n/lt.po`
- `addons/pos_stock/i18n/lv.po`
- `addons/pos_stock/i18n/mn.po`
- `addons/pos_stock/i18n/my.po`
- `addons/pos_stock/i18n/nb.po`
- `addons/pos_stock/i18n/nl.po`
- `addons/pos_stock/i18n/pl.po`
- `addons/pos_stock/i18n/pos_stock.pot`
- `addons/pos_stock/i18n/pt.po`
- `addons/pos_stock/i18n/pt_BR.po`
- `addons/pos_stock/i18n/ro.po`
- `addons/pos_stock/i18n/ru.po`
- `addons/pos_stock/i18n/sk.po`
- `addons/pos_stock/i18n/sl.po`
- `addons/pos_stock/i18n/sr@latin.po`
- `addons/pos_stock/i18n/sv.po`
- `addons/pos_stock/i18n/th.po`
- `addons/pos_stock/i18n/tr.po`
- `addons/pos_stock/i18n/uk.po`
- `addons/pos_stock/i18n/uz.po`
- `addons/pos_stock/i18n/vi.po`
- `addons/pos_stock/i18n/zh_CN.po`
- `addons/pos_stock/i18n/zh_TW.po`
- `addons/pos_stock/models/__init__.py`
- `addons/pos_stock/models/account_move.py`
- `addons/pos_stock/models/account_move_line.py`
- `addons/pos_stock/models/pos_config.py`
- `addons/pos_stock/models/pos_order.py`
- `addons/pos_stock/models/pos_order_line.py`
- `addons/pos_stock/models/pos_pack_operation_lot.py`
- `addons/pos_stock/models/pos_session.py`
- `addons/pos_stock/models/product_category.py`
- `addons/pos_stock/models/product_removal.py`
- `addons/pos_stock/models/product_template.py`
- `addons/pos_stock/models/res_company.py`
- `addons/pos_stock/models/res_config_settings.py`
- `addons/pos_stock/models/stock_move.py`
- `addons/pos_stock/models/stock_picking.py`
- `addons/pos_stock/models/stock_reference.py`
- `addons/pos_stock/models/stock_rule.py`
- `addons/pos_stock/models/stock_warehouse.py`
- `addons/pos_stock/receipt/__init__.py`
- `addons/pos_stock/receipt/pos_order_receipt.py`
- `addons/pos_stock/receipt/pos_order_receipt.xml`
- `addons/pos_stock/security/ir.access.csv`
- `addons/pos_stock/security/pos_stock_security.xml`
- `addons/pos_stock/static/src/app/components/orderline/orderline.js`
- `addons/pos_stock/static/src/app/components/orderline/orderline.xml`
- `addons/pos_stock/static/src/app/components/popups/date_picker_popup/date_picker_popup.js`
- `addons/pos_stock/static/src/app/components/popups/date_picker_popup/date_picker_popup.xml`
- `addons/pos_stock/static/src/app/components/popups/product_info_popup/product_info_popup.xml`
- `addons/pos_stock/static/src/app/components/popups/select_lot_popup/select_lot_popup.js`
- `addons/pos_stock/static/src/app/components/popups/select_lot_popup/select_lot_popup.scss`
- `addons/pos_stock/static/src/app/components/popups/select_lot_popup/select_lot_popup.xml`
- `addons/pos_stock/static/src/app/components/product_info_banner/product_info_banner.js`
- `addons/pos_stock/static/src/app/components/product_info_banner/product_info_banner.xml`
- `addons/pos_stock/static/src/app/models/accounting/product_template_accounting.js`
- `addons/pos_stock/static/src/app/models/data_service_options.js`
- `addons/pos_stock/static/src/app/models/pos_order.js`
- `addons/pos_stock/static/src/app/models/pos_order_line.js`
- `addons/pos_stock/static/src/app/models/product_template.js`
- `addons/pos_stock/static/src/app/screens/payment_screen/payment_screen.js`
- `addons/pos_stock/static/src/app/screens/payment_screen/payment_screen.xml`
- `addons/pos_stock/static/src/app/screens/product_screen/order_summary/order_summary.js`
- `addons/pos_stock/static/src/app/screens/product_screen/order_summary/order_summary.xml`
- `addons/pos_stock/static/src/app/screens/ticket_screen/ticket_screen.js`
- `addons/pos_stock/static/src/app/services/pos_store.js`
- `addons/pos_stock/static/src/app/utils/generate_printer_data.js`
- `addons/pos_stock/static/src/app/utils/order_payment_validation.js`
- `addons/pos_stock/static/src/customer_display/customer_display.xml`
- `addons/pos_stock/static/tests/pos/tours/OrderWithLots_tour.js`
- `addons/pos_stock/static/tests/pos/tours/barcode_scanning_tour.js`
- `addons/pos_stock/static/tests/pos/tours/chrome_tour.js`
- `addons/pos_stock/static/tests/pos/tours/feedback_screen_tour.js`
- `addons/pos_stock/static/tests/pos/tours/order_receipt.js`
- `addons/pos_stock/static/tests/pos/tours/payment_screen_tour.js`
- `addons/pos_stock/static/tests/pos/tours/pos_combo_tour.js`
- `addons/pos_stock/static/tests/pos/tours/product_screen_tour.js`
- `addons/pos_stock/static/tests/pos/tours/shipping_date_tour.js`
- `addons/pos_stock/static/tests/pos/tours/ticket_screen_tour.js`
- `addons/pos_stock/static/tests/pos/tours/utils/feedback_screen_util.js`
- `addons/pos_stock/static/tests/pos/tours/utils/payment_screen_util.js`
- `addons/pos_stock/static/tests/pos/tours/utils/product_screen_util.js`
- `addons/pos_stock/static/tests/unit/accounting/price.test.js`
- `addons/pos_stock/static/tests/unit/components/payment_screen.test.js`
- `addons/pos_stock/static/tests/unit/components/popup/select_lot_popup.test.js`
- `addons/pos_stock/static/tests/unit/customer_display/customer_display.test.js`
- `addons/pos_stock/static/tests/unit/data/decimal_precision.data.js`
- `addons/pos_stock/static/tests/unit/data/generate_model_definitions.js`
- `addons/pos_stock/static/tests/unit/data/pos_config.data.js`
- `addons/pos_stock/static/tests/unit/data/pos_order.data.js`
- `addons/pos_stock/static/tests/unit/data/pos_order_line.data.js`
- `addons/pos_stock/static/tests/unit/data/pos_pack_operation_lot.data.js`
- `addons/pos_stock/static/tests/unit/data/pos_session.data.js`
- `addons/pos_stock/static/tests/unit/data/product_pricelist.data.js`
- `addons/pos_stock/static/tests/unit/data/product_pricelist_item.data.js`
- `addons/pos_stock/static/tests/unit/data/product_product.data.js`
- `addons/pos_stock/static/tests/unit/data/product_template.data.js`
- `addons/pos_stock/static/tests/unit/data/stock_picking_type.data.js`
- `addons/pos_stock/static/tests/unit/data/stock_route.data.js`
- `addons/pos_stock/static/tests/unit/data/stock_warehouse.data.js`
- `addons/pos_stock/static/tests/unit/models/pos_order_line.test.js`
- `addons/pos_stock/static/tests/unit/related_models/orm_serialization.test.js`
- `addons/pos_stock/tests/__init__.py`
- `addons/pos_stock/tests/common.py`
- `addons/pos_stock/tests/test_anglo_saxon.py`
- `addons/pos_stock/tests/test_continental.py`
- `addons/pos_stock/tests/test_frontend.py`
- `addons/pos_stock/tests/test_pos_accounting.py`
- `addons/pos_stock/tests/test_pos_picking_backorder.py`
- `addons/pos_stock/tests/test_pos_stock.py`
- `addons/pos_stock/tests/test_pos_stock_account.py`
- `addons/pos_stock/tests/test_pos_stock_basic_config.py`
- `addons/pos_stock/tests/test_pos_stock_flow.py`
- `addons/pos_stock/tests/test_pos_stock_margin.py`
- `addons/pos_stock/tests/test_pos_stock_order_receipt.py`
- `addons/pos_stock/tests/test_pos_stock_other_currency_config.py`
- `addons/pos_stock/tests/test_pos_stock_products_with_tax.py`
- `addons/pos_stock/tests/test_res_config_settings.py`
- `addons/pos_stock/views/pos_config_view.xml`
- `addons/pos_stock/views/pos_order_view.xml`
- `addons/pos_stock/views/pos_session_view.xml`
- `addons/pos_stock/views/product_view.xml`
- `addons/pos_stock/views/res_config_settings_views.xml`
- `addons/pos_stock/views/stock_reference_views.xml`
