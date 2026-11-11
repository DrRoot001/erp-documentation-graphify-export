# Module: purchase_stock

- **Module ID:** MOD-503
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/purchase_stock`
- **Manifest:** `addons/purchase_stock/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Purchase`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Purchase Orders, Receipts, Vendor Bills for Stock

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 140 files, including 48 Python, 22 XML, and 16 JavaScript/TypeScript files. The manifest declares dependencies: `stock_account`, `purchase`.

## 2. Module structure

- Model/business logic files: 26
- Controller/API files: 0
- XML/data/view/template files: 22
- Browser asset files: 16
- Security files: 1
- Test files: 24
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/purchase_stock/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 26 model declarations, 454 methods, 0 constraint handlers, 5 onchange handlers, and 33 dependency declarations.
- **Evidence:** `addons/purchase_stock/models/res_partner.py:10`, `addons/purchase_stock/models/purchase_order.py:13`, `addons/purchase_stock/models/purchase_order_line.py:11`, `addons/purchase_stock/models/res_config_settings.py:7`, `addons/purchase_stock/models/stock_move.py:10`, `addons/purchase_stock/models/product.py:13`, `addons/purchase_stock/models/product.py:34`, `addons/purchase_stock/models/product.py:256`, `addons/purchase_stock/models/stock.py:10`, `addons/purchase_stock/models/stock.py:74`, `addons/purchase_stock/models/stock.py:155`, `addons/purchase_stock/models/stock.py:364`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 22 XML files and 16 JavaScript/TypeScript files; static XML analysis found 71 record/template/menu identifiers.
- **Evidence:** `addons/purchase_stock/report/vendor_delay_report.xml:3`, `addons/purchase_stock/report/vendor_delay_report.xml:15`, `addons/purchase_stock/report/vendor_delay_report.xml:26`, `addons/purchase_stock/report/purchase_report_templates.xml:4`, `addons/purchase_stock/report/purchase_report_templates.xml:18`, `addons/purchase_stock/report/report_stock_rule.xml:3`, `addons/purchase_stock/report/purchase_report_views.xml:4`, `addons/purchase_stock/wizard/product_replenish_views.xml:3`, `addons/purchase_stock/wizard/stock_replenishment_info.xml:4`, `addons/purchase_stock/wizard/stock_replenishment_info.xml:40`, `addons/purchase_stock/data/purchase_stock_data.xml:10`, `addons/purchase_stock/data/purchase_stock_data.xml:20`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/purchase_stock/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 24 test files are present.
- **Evidence:** `addons/purchase_stock/tests/test_move_cancel_propagation.py`, `addons/purchase_stock/tests/test_stock_valuation.py`, `addons/purchase_stock/tests/test_purchase_stock_accrued_entries.py`, `addons/purchase_stock/tests/test_account.py`, `addons/purchase_stock/tests/test_onchange_product.py`, `addons/purchase_stock/tests/test_supplier.py`, `addons/purchase_stock/tests/test_purchase_stock_report.py`, `addons/purchase_stock/tests/test_routes.py`, `addons/purchase_stock/tests/test_purchase_lead_time.py`, `addons/purchase_stock/tests/test_old_rules.py`, `addons/purchase_stock/tests/test_stock.py`, `addons/purchase_stock/tests/common.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 22; representative identifiers: `vendor_delay_report_filter`, `vendor_delay_report_view_graph`, `action_purchase_vendor_delay_report`, `report_purchaseorder_document`, `report_purchasequotation_document`, `purchase_report_stock_rule`, `purchase_report_view_search`, `view_product_replenish_form_inherit_stock`, `product_supplierinfo_replenishment_tree_view`, `view_stock_replenishment_info_stock_purchase_inherit`, `route_warehouse0_buy`, `stock.warehouse0`, `product.product_product_20`, `purchase_order_8`, `purchase_bill_8`, `purchase_order_9_pallet`, `stock_inventory_product_product_8`, `stock_inventory_product_delivery_01`, `picking_delivery_1`, `picking_delivery_2`
- Menus: 0; representative evidence: Not found in module
- Templates: 6; representative evidence: `addons/purchase_stock/report/purchase_report_templates.xml:4`, `addons/purchase_stock/report/purchase_report_templates.xml:18`, `addons/purchase_stock/report/report_stock_rule.xml:3`, `addons/purchase_stock/data/mail_templates.xml:3`, `addons/purchase_stock/data/mail_templates.xml:31`, `addons/purchase_stock/views/stock_picking_views.xml:4`
- View/action field declarations: 50; representative evidence: `addons/purchase_stock/report/vendor_delay_report.xml:5`, `addons/purchase_stock/report/vendor_delay_report.xml:6`, `addons/purchase_stock/report/vendor_delay_report.xml:17`, `addons/purchase_stock/report/vendor_delay_report.xml:18`, `addons/purchase_stock/report/vendor_delay_report.xml:28`, `addons/purchase_stock/report/vendor_delay_report.xml:29`, `addons/purchase_stock/report/purchase_report_views.xml:6`, `addons/purchase_stock/report/purchase_report_views.xml:8`, `addons/purchase_stock/wizard/product_replenish_views.xml:5`, `addons/purchase_stock/wizard/product_replenish_views.xml:7`, `addons/purchase_stock/wizard/stock_replenishment_info.xml:6`, `addons/purchase_stock/wizard/stock_replenishment_info.xml:10`
- Browser assets: 16; representative files: `addons/purchase_stock/static/tests/product_catalog.test.js`, `addons/purchase_stock/static/tests/purchase_stock.test.js`, `addons/purchase_stock/static/src/product_catalog/kanban_model.js`, `addons/purchase_stock/static/src/product_catalog/kanban_renderer.js`, `addons/purchase_stock/static/src/product_catalog/utils.js`, `addons/purchase_stock/static/src/product_catalog/kanban_view.js`, `addons/purchase_stock/static/src/product_catalog/kanban_controller.js`, `addons/purchase_stock/static/src/js/tours/purchase_stock.js`, `addons/purchase_stock/static/src/product_catalog/record/kanban_record.js`, `addons/purchase_stock/static/src/product_catalog/record/purchase_order_line.js`, `addons/purchase_stock/static/src/product_catalog/search/time_period_selection_fields.js`, `addons/purchase_stock/static/src/product_catalog/search/search_model.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/purchase_stock/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 26
- Representative model evidence: inherits `res.partner` (addons/purchase_stock/models/res_partner.py:10); inherits `purchase.order` (addons/purchase_stock/models/purchase_order.py:13); inherits `purchase.order.line` (addons/purchase_stock/models/purchase_order_line.py:11); inherits `res.config.settings` (addons/purchase_stock/models/res_config_settings.py:7); inherits `stock.move` (addons/purchase_stock/models/stock_move.py:10); inherits `product.template` (addons/purchase_stock/models/product.py:13); inherits `product.product` (addons/purchase_stock/models/product.py:34); inherits `product.supplierinfo` (addons/purchase_stock/models/product.py:256); inherits `stock.picking` (addons/purchase_stock/models/stock.py:10); inherits `stock.warehouse` (addons/purchase_stock/models/stock.py:74); inherits `stock.warehouse.orderpoint` (addons/purchase_stock/models/stock.py:155); inherits `stock.lot` (addons/purchase_stock/models/stock.py:364); inherits `stock.replenish.mixin` (addons/purchase_stock/models/stock_replenish_mixin.py:6); inherits `stock.rule` (addons/purchase_stock/models/stock_rule.py:15); inherits `stock.route` (addons/purchase_stock/models/stock_rule.py:413); inherits `account.move.line` (addons/purchase_stock/models/account_move_line.py:7); inherits `stock.reference` (addons/purchase_stock/models/stock_reference.py:4); inherits `res.company` (addons/purchase_stock/models/res_company.py:7); inherits `purchase.report` (addons/purchase_stock/report/purchase_report.py:8); inherits `report.stock.report_stock_rule` (addons/purchase_stock/report/report_stock_rule.py:7); inherits `stock.allocation.report` (addons/purchase_stock/report/stock_allocation_report.py:4); inherits `stock.forecasted_product_product` (addons/purchase_stock/report/stock_forecasted.py:7); `vendor.delay.report` (addons/purchase_stock/report/vendor_delay_report.py:8); inherits `stock.replenishment.info` (addons/purchase_stock/wizard/stock_replenishment_info.py:7); inherits `stock.replenishment.option` (addons/purchase_stock/wizard/stock_replenishment_info.py:30); inherits `product.replenish` (addons/purchase_stock/wizard/product_replenish.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `stock_account`, `purchase`
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

- `addons/purchase_stock/__init__.py`
- `addons/purchase_stock/__manifest__.py`
- `addons/purchase_stock/data/mail_templates.xml`
- `addons/purchase_stock/data/purchase_stock_data.xml`
- `addons/purchase_stock/data/purchase_stock_demo.xml`
- `addons/purchase_stock/i18n/ar.po`
- `addons/purchase_stock/i18n/az.po`
- `addons/purchase_stock/i18n/bg.po`
- `addons/purchase_stock/i18n/bs.po`
- `addons/purchase_stock/i18n/ca.po`
- `addons/purchase_stock/i18n/cs.po`
- `addons/purchase_stock/i18n/da.po`
- `addons/purchase_stock/i18n/de.po`
- `addons/purchase_stock/i18n/el.po`
- `addons/purchase_stock/i18n/es.po`
- `addons/purchase_stock/i18n/es_419.po`
- `addons/purchase_stock/i18n/et.po`
- `addons/purchase_stock/i18n/fa.po`
- `addons/purchase_stock/i18n/fi.po`
- `addons/purchase_stock/i18n/fr.po`
- `addons/purchase_stock/i18n/gu.po`
- `addons/purchase_stock/i18n/he.po`
- `addons/purchase_stock/i18n/hi.po`
- `addons/purchase_stock/i18n/hr.po`
- `addons/purchase_stock/i18n/hu.po`
- `addons/purchase_stock/i18n/id.po`
- `addons/purchase_stock/i18n/is.po`
- `addons/purchase_stock/i18n/it.po`
- `addons/purchase_stock/i18n/ja.po`
- `addons/purchase_stock/i18n/kab.po`
- `addons/purchase_stock/i18n/ko.po`
- `addons/purchase_stock/i18n/ku.po`
- `addons/purchase_stock/i18n/lo.po`
- `addons/purchase_stock/i18n/lt.po`
- `addons/purchase_stock/i18n/lv.po`
- `addons/purchase_stock/i18n/mn.po`
- `addons/purchase_stock/i18n/my.po`
- `addons/purchase_stock/i18n/nb.po`
- `addons/purchase_stock/i18n/nl.po`
- `addons/purchase_stock/i18n/pl.po`
- `addons/purchase_stock/i18n/pt.po`
- `addons/purchase_stock/i18n/pt_BR.po`
- `addons/purchase_stock/i18n/purchase_stock.pot`
- `addons/purchase_stock/i18n/ro.po`
- `addons/purchase_stock/i18n/ru.po`
- `addons/purchase_stock/i18n/sk.po`
- `addons/purchase_stock/i18n/sl.po`
- `addons/purchase_stock/i18n/sr@latin.po`
- `addons/purchase_stock/i18n/sv.po`
- `addons/purchase_stock/i18n/th.po`
- `addons/purchase_stock/i18n/tr.po`
- `addons/purchase_stock/i18n/uk.po`
- `addons/purchase_stock/i18n/uz.po`
- `addons/purchase_stock/i18n/vi.po`
- `addons/purchase_stock/i18n/zh_CN.po`
- `addons/purchase_stock/i18n/zh_TW.po`
- `addons/purchase_stock/models/__init__.py`
- `addons/purchase_stock/models/account_move_line.py`
- `addons/purchase_stock/models/product.py`
- `addons/purchase_stock/models/purchase_order.py`
- `addons/purchase_stock/models/purchase_order_line.py`
- `addons/purchase_stock/models/res_company.py`
- `addons/purchase_stock/models/res_config_settings.py`
- `addons/purchase_stock/models/res_partner.py`
- `addons/purchase_stock/models/stock.py`
- `addons/purchase_stock/models/stock_move.py`
- `addons/purchase_stock/models/stock_reference.py`
- `addons/purchase_stock/models/stock_replenish_mixin.py`
- `addons/purchase_stock/models/stock_rule.py`
- `addons/purchase_stock/report/__init__.py`
- `addons/purchase_stock/report/purchase_report.py`
- `addons/purchase_stock/report/purchase_report_templates.xml`
- `addons/purchase_stock/report/purchase_report_views.xml`
- `addons/purchase_stock/report/report_stock_rule.py`
- `addons/purchase_stock/report/report_stock_rule.xml`
- `addons/purchase_stock/report/stock_allocation_report.py`
- `addons/purchase_stock/report/stock_forecasted.py`
- `addons/purchase_stock/report/vendor_delay_report.py`
- `addons/purchase_stock/report/vendor_delay_report.xml`
- `addons/purchase_stock/security/ir.access.csv`
- `addons/purchase_stock/static/src/js/tours/purchase_stock.js`
- `addons/purchase_stock/static/src/product_catalog/kanban_controller.js`
- `addons/purchase_stock/static/src/product_catalog/kanban_model.js`
- `addons/purchase_stock/static/src/product_catalog/kanban_renderer.js`
- `addons/purchase_stock/static/src/product_catalog/kanban_view.js`
- `addons/purchase_stock/static/src/product_catalog/record/kanban_record.js`
- `addons/purchase_stock/static/src/product_catalog/record/kanban_record.scss`
- `addons/purchase_stock/static/src/product_catalog/record/purchase_order_line.js`
- `addons/purchase_stock/static/src/product_catalog/search/search_model.js`
- `addons/purchase_stock/static/src/product_catalog/search/search_panel.js`
- `addons/purchase_stock/static/src/product_catalog/search/search_panel.scss`
- `addons/purchase_stock/static/src/product_catalog/search/search_panel.xml`
- `addons/purchase_stock/static/src/product_catalog/search/time_period_selection_fields.js`
- `addons/purchase_stock/static/src/product_catalog/utils.js`
- `addons/purchase_stock/static/src/purchase_dashboard/purchase_dashboard.xml`
- `addons/purchase_stock/static/src/purchase_stock_forecasted/forecasted_details.xml`
- `addons/purchase_stock/static/tests/product_catalog.test.js`
- `addons/purchase_stock/static/tests/purchase_stock.test.js`
- `addons/purchase_stock/static/tests/tours/product_replenishment.js`
- `addons/purchase_stock/static/tests/tours/purchase_catalog_suggest.js`
- `addons/purchase_stock/static/tests/tours/tour_helper.js`
- `addons/purchase_stock/tests/__init__.py`
- `addons/purchase_stock/tests/common.py`
- `addons/purchase_stock/tests/test_account.py`
- `addons/purchase_stock/tests/test_create_picking.py`
- `addons/purchase_stock/tests/test_move_cancel_propagation.py`
- `addons/purchase_stock/tests/test_old_rules.py`
- `addons/purchase_stock/tests/test_onchange_product.py`
- `addons/purchase_stock/tests/test_product_template.py`
- `addons/purchase_stock/tests/test_purchase_delete_order.py`
- `addons/purchase_stock/tests/test_purchase_lead_time.py`
- `addons/purchase_stock/tests/test_purchase_order.py`
- `addons/purchase_stock/tests/test_purchase_order_process.py`
- `addons/purchase_stock/tests/test_purchase_order_suggest.py`
- `addons/purchase_stock/tests/test_purchase_stock_accrued_entries.py`
- `addons/purchase_stock/tests/test_purchase_stock_report.py`
- `addons/purchase_stock/tests/test_reordering_rule.py`
- `addons/purchase_stock/tests/test_replenish_wizard.py`
- `addons/purchase_stock/tests/test_routes.py`
- `addons/purchase_stock/tests/test_stock.py`
- `addons/purchase_stock/tests/test_stock_orderpoint.py`
- `addons/purchase_stock/tests/test_stock_valuation.py`
- `addons/purchase_stock/tests/test_stockvaluation.py`
- `addons/purchase_stock/tests/test_supplier.py`
- `addons/purchase_stock/tests/test_uninstall.py`
- `addons/purchase_stock/views/product_views.xml`
- `addons/purchase_stock/views/purchase_views.xml`
- `addons/purchase_stock/views/res_config_settings_views.xml`
- `addons/purchase_stock/views/res_partner_views.xml`
- `addons/purchase_stock/views/stock_lot_views.xml`
- `addons/purchase_stock/views/stock_orderpoint_views.xml`
- `addons/purchase_stock/views/stock_picking_views.xml`
- `addons/purchase_stock/views/stock_reference_views.xml`
- `addons/purchase_stock/views/stock_rule_views.xml`
- `addons/purchase_stock/views/stock_views.xml`
- `addons/purchase_stock/wizard/__init__.py`
- `addons/purchase_stock/wizard/product_replenish.py`
- `addons/purchase_stock/wizard/product_replenish_views.xml`
- `addons/purchase_stock/wizard/stock_replenishment_info.py`
- `addons/purchase_stock/wizard/stock_replenishment_info.xml`
