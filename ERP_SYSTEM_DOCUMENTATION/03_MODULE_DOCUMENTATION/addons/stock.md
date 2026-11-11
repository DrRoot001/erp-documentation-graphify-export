# Module: stock

- **Module ID:** MOD-559
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/stock`
- **Manifest:** `addons/stock/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Supply Chain/Inventory`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Manage your stock and logistics activities

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 345 files, including 96 Python, 107 XML, and 55 JavaScript/TypeScript files. The manifest declares dependencies: `product`, `barcodes_gs1_nomenclature`, `digest`.

## 2. Module structure

- Model/business logic files: 66
- Controller/API files: 2
- XML/data/view/template files: 107
- Browser asset files: 55
- Security files: 2
- Test files: 32
- Scheduled/automation evidence files: 15
- Reporting evidence files: 9

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/stock/security/ir.access.csv`, `addons/stock/security/stock_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 66 model declarations, 1805 methods, 12 constraint handlers, 37 onchange handlers, and 173 dependency declarations.
- **Evidence:** `addons/stock/models/res_partner.py:7`, `addons/stock/models/stock_location.py:13`, `addons/stock/models/stock_location.py:513`, `addons/stock/models/digest.py:6`, `addons/stock/models/stock_storage_category.py:7`, `addons/stock/models/stock_storage_category.py:44`, `addons/stock/models/stock_move_line.py:16`, `addons/stock/models/product_strategy.py:8`, `addons/stock/models/product_strategy.py:16`, `addons/stock/models/res_groups.py:6`, `addons/stock/models/res_config_settings.py:8`, `addons/stock/models/stock_move.py:17`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/stock/controllers/main.py:13`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 107 XML files and 55 JavaScript/TypeScript files; static XML analysis found 515 record/template/menu identifiers.
- **Evidence:** `addons/stock/security/stock_security.xml:4`, `addons/stock/security/stock_security.xml:9`, `addons/stock/security/stock_security.xml:15`, `addons/stock/security/stock_security.xml:25`, `addons/stock/security/stock_security.xml:29`, `addons/stock/security/stock_security.xml:32`, `addons/stock/security/stock_security.xml:36`, `addons/stock/security/stock_security.xml:40`, `addons/stock/security/stock_security.xml:44`, `addons/stock/security/stock_security.xml:48`, `addons/stock/security/stock_security.xml:52`, `addons/stock/security/stock_security.xml:56`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/stock/security/ir.access.csv`, `addons/stock/security/stock_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 15 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/stock/models/stock_orderpoint.py`, `addons/stock/models/stock_rule.py`, `addons/stock/data/stock_sequence_data.xml`, `addons/stock/views/stock_package_history_views.xml`, `addons/stock/views/stock_picking_views.xml`, `addons/stock/views/stock_package_views.xml`, `addons/stock/views/stock_location_views.xml`, `addons/stock/views/stock_picking_batch_views.xml`, `addons/stock/views/stock_picking_type_views.xml`, `addons/stock/views/stock_quant_views.xml`, `addons/stock/views/stock_rule_views.xml`, `addons/stock/views/product_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 9 files contain report-action/template indicators.
- **Evidence:** `addons/stock/models/ir_actions_report.py`, `addons/stock/models/stock_picking_type.py`, `addons/stock/models/stock_picking.py`, `addons/stock/controllers/main.py`, `addons/stock/report/stock_traceability.py`, `addons/stock/report/report_return_slip.xml`, `addons/stock/report/report_picking_batch.xml`, `addons/stock/report/stock_report_views.xml`, `addons/stock/tests/test_report.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 32 test files are present.
- **Evidence:** `addons/stock/tests/test_move.py`, `addons/stock/tests/test_immediate.py`, `addons/stock/tests/test_stock_flow.py`, `addons/stock/tests/test_quant.py`, `addons/stock/tests/test_stock_location_search.py`, `addons/stock/tests/test_stock_return_picking.py`, `addons/stock/tests/test_packing_neg.py`, `addons/stock/tests/test_stock_order_point.py`, `addons/stock/tests/test_warehouse.py`, `addons/stock/tests/test_replenish.py`, `addons/stock/tests/test_product.py`, `addons/stock/tests/test_report_tours.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 107; representative identifiers: `res_groups_privilege_inventory`, `group_stock_user`, `group_stock_manager`, `group_stock_multi_locations`, `group_stock_multi_warehouses`, `group_stock_picking_batch`, `group_production_lot`, `group_stock_lot_print_gs1`, `group_lot_on_delivery_slip`, `group_tracking_lot`, `group_adv_location`, `group_tracking_owner`, `group_warning_stock`, `group_stock_sign_delivery`, `report_inventory`, `report_reception_report_label`, `return_label_report`, `stock.report_return_slip`, `return_label_header`, `report_return_document`
- Menus: 43; representative evidence: `addons/stock/views/stock_package_type_view.xml:95`, `addons/stock/views/stock_package_type_view.xml:96`, `addons/stock/views/stock_move_views.xml:599`, `addons/stock/views/stock_move_views.xml:600`, `addons/stock/views/stock_storage_category_views.xml:100`, `addons/stock/views/product_strategy_views.xml:117`, `addons/stock/views/stock_picking_views.xml:653`, `addons/stock/views/stock_picking_views.xml:656`, `addons/stock/views/stock_picking_views.xml:659`, `addons/stock/views/stock_package_views.xml:164`, `addons/stock/views/stock_reference_views.xml:55`, `addons/stock/views/res_config_settings_views.xml:208`
- Templates: 40; representative evidence: `addons/stock/report/report_stockinventory.xml:4`, `addons/stock/report/report_stock_reception.xml:3`, `addons/stock/report/report_return_slip.xml:3`, `addons/stock/report/report_return_slip.xml:34`, `addons/stock/report/report_return_slip.xml:53`, `addons/stock/report/report_location_barcode.xml:3`, `addons/stock/report/report_location_barcode.xml:25`, `addons/stock/report/report_stock_rule.xml:3`, `addons/stock/report/report_stock_rule.xml:146`, `addons/stock/report/report_stock_rule.xml:153`, `addons/stock/report/report_stock_rule.xml:160`, `addons/stock/report/report_stock_rule.xml:167`
- View/action field declarations: 404; representative evidence: `addons/stock/report/report_return_slip.xml:61`, `addons/stock/report/report_picking_batch.xml:127`, `addons/stock/report/report_stock_quantity.xml:6`, `addons/stock/report/report_stock_quantity.xml:7`, `addons/stock/report/stock_allocation_report.xml:6`, `addons/stock/report/stock_report_views.xml:6`, `addons/stock/report/stock_report_views.xml:15`, `addons/stock/report/stock_report_views.xml:24`, `addons/stock/report/stock_report_views.xml:34`, `addons/stock/report/stock_report_views.xml:43`, `addons/stock/report/stock_report_views.xml:51`, `addons/stock/report/stock_report_views.xml:59`
- Browser assets: 55; representative files: `addons/stock/static/src/stock_warehouse_service.js`, `addons/stock/static/src/stock_picking_many2many_field.js`, `addons/stock/static/tests/counted_quantity_widget.test.js`, `addons/stock/static/tests/stock_traceability_report_backend.test.js`, `addons/stock/static/tests/popover_widget.test.js`, `addons/stock/static/tests/stock_kanban_dashboard.test.js`, `addons/stock/static/tests/forecasted_details.test.js`, `addons/stock/static/tests/inventory_report_list.test.js`, `addons/stock/static/src/picking_type_dashboard_graph/picking_type_dashboard_graph_field.js`, `addons/stock/static/src/allocation_report/allocation_report.js`, `addons/stock/static/src/widgets/popover_widget.js`, `addons/stock/static/src/widgets/max_qty_to_order_field.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/stock/__manifest__.py`
- **HTTP entry points:** `addons/stock/controllers/main.py:13`
- **Scheduled entry points:** `addons/stock/models/stock_orderpoint.py`, `addons/stock/models/stock_rule.py`, `addons/stock/data/stock_sequence_data.xml`, `addons/stock/views/stock_package_history_views.xml`, `addons/stock/views/stock_picking_views.xml`, `addons/stock/views/stock_package_views.xml`, `addons/stock/views/stock_location_views.xml`, `addons/stock/views/stock_picking_batch_views.xml`, `addons/stock/views/stock_picking_type_views.xml`, `addons/stock/views/stock_quant_views.xml`, `addons/stock/views/stock_rule_views.xml`, `addons/stock/views/product_views.xml`
- **Report entry points:** `addons/stock/models/ir_actions_report.py`, `addons/stock/models/stock_picking_type.py`, `addons/stock/models/stock_picking.py`, `addons/stock/controllers/main.py`, `addons/stock/report/stock_traceability.py`, `addons/stock/report/report_return_slip.xml`, `addons/stock/report/report_picking_batch.xml`, `addons/stock/report/stock_report_views.xml`, `addons/stock/tests/test_report.py`

## 7. Database interactions

- Model declarations: 66
- Representative model evidence: inherits `res.partner` (addons/stock/models/res_partner.py:7); `stock.location` (addons/stock/models/stock_location.py:13); `stock.route` (addons/stock/models/stock_location.py:513); inherits `digest.digest` (addons/stock/models/digest.py:6); `stock.storage.category` (addons/stock/models/stock_storage_category.py:7); `stock.storage.category.capacity` (addons/stock/models/stock_storage_category.py:44); `stock.move.line` (addons/stock/models/stock_move_line.py:16); `product.removal` (addons/stock/models/product_strategy.py:8); `stock.putaway.rule` (addons/stock/models/product_strategy.py:16); inherits `res.groups` (addons/stock/models/res_groups.py:6); inherits `res.config.settings` (addons/stock/models/res_config_settings.py:8); `stock.move` (addons/stock/models/stock_move.py:17); `stock.quant` (addons/stock/models/stock_quant.py:20); inherits `barcode.rule` (addons/stock/models/barcode.py:7); inherits `ir.actions.report` (addons/stock/models/ir_actions_report.py:4); `stock.scrap.reason.tag` (addons/stock/models/stock_scrap_reason_tag.py:4); `stock.picking.batch` (addons/stock/models/stock_picking_batch.py:12); inherits `product.product` (addons/stock/models/product.py:44); inherits `product.template` (addons/stock/models/product.py:811); inherits `product.category` (addons/stock/models/product.py:1274); inherits `uom.uom` (addons/stock/models/product.py:1338); `stock.package.history` (addons/stock/models/stock_package_history.py:6); `stock.picking.type` (addons/stock/models/stock_picking_type.py:45); `stock.warehouse.orderpoint` (addons/stock/models/stock_orderpoint.py:22); `stock.replenish.mixin` (addons/stock/models/stock_replenish_mixin.py:7); `stock.package.type` (addons/stock/models/stock_package_type.py:7); `stock.picking` (addons/stock/models/stock_picking.py:17); inherits `res.users` (addons/stock/models/res_users.py:6); `stock.rule` (addons/stock/models/stock_rule.py:42); `stock.lot` (addons/stock/models/stock_lot.py:24)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/stock/controllers/main.py:13`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `product`, `barcodes_gs1_nomenclature`, `digest`
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

- `addons/stock/__init__.py`
- `addons/stock/__manifest__.py`
- `addons/stock/controllers/__init__.py`
- `addons/stock/controllers/main.py`
- `addons/stock/data/default_barcode_patterns.xml`
- `addons/stock/data/digest_data.xml`
- `addons/stock/data/mail_message_subtype_data.xml`
- `addons/stock/data/mail_template_data.xml`
- `addons/stock/data/mail_templates.xml`
- `addons/stock/data/stock_data.xml`
- `addons/stock/data/stock_demo.xml`
- `addons/stock/data/stock_demo2.xml`
- `addons/stock/data/stock_demo3_batch.xml`
- `addons/stock/data/stock_demo_pre.xml`
- `addons/stock/data/stock_orderpoint_demo.xml`
- `addons/stock/data/stock_sequence_data.xml`
- `addons/stock/data/stock_storage_category_demo.xml`
- `addons/stock/data/stock_traceability_report_data.xml`
- `addons/stock/i18n/af.po`
- `addons/stock/i18n/ar.po`
- `addons/stock/i18n/az.po`
- `addons/stock/i18n/bg.po`
- `addons/stock/i18n/bs.po`
- `addons/stock/i18n/ca.po`
- `addons/stock/i18n/cs.po`
- `addons/stock/i18n/da.po`
- `addons/stock/i18n/de.po`
- `addons/stock/i18n/el.po`
- `addons/stock/i18n/es.po`
- `addons/stock/i18n/es_419.po`
- `addons/stock/i18n/es_CL.po`
- `addons/stock/i18n/et.po`
- `addons/stock/i18n/fa.po`
- `addons/stock/i18n/fi.po`
- `addons/stock/i18n/fr.po`
- `addons/stock/i18n/gl.po`
- `addons/stock/i18n/gu.po`
- `addons/stock/i18n/he.po`
- `addons/stock/i18n/hi.po`
- `addons/stock/i18n/hr.po`
- `addons/stock/i18n/hu.po`
- `addons/stock/i18n/id.po`
- `addons/stock/i18n/is.po`
- `addons/stock/i18n/it.po`
- `addons/stock/i18n/ja.po`
- `addons/stock/i18n/kab.po`
- `addons/stock/i18n/km.po`
- `addons/stock/i18n/ko.po`
- `addons/stock/i18n/ku.po`
- `addons/stock/i18n/lb.po`
- `addons/stock/i18n/lo.po`
- `addons/stock/i18n/lt.po`
- `addons/stock/i18n/lv.po`
- `addons/stock/i18n/mk.po`
- `addons/stock/i18n/mn.po`
- `addons/stock/i18n/my.po`
- `addons/stock/i18n/nb.po`
- `addons/stock/i18n/nl.po`
- `addons/stock/i18n/pl.po`
- `addons/stock/i18n/pt.po`
- `addons/stock/i18n/pt_BR.po`
- `addons/stock/i18n/ro.po`
- `addons/stock/i18n/ru.po`
- `addons/stock/i18n/sk.po`
- `addons/stock/i18n/sl.po`
- `addons/stock/i18n/sr@latin.po`
- `addons/stock/i18n/stock.pot`
- `addons/stock/i18n/sv.po`
- `addons/stock/i18n/th.po`
- `addons/stock/i18n/tr.po`
- `addons/stock/i18n/uk.po`
- `addons/stock/i18n/uz.po`
- `addons/stock/i18n/vi.po`
- `addons/stock/i18n/zh_CN.po`
- `addons/stock/i18n/zh_TW.po`
- `addons/stock/models/__init__.py`
- `addons/stock/models/barcode.py`
- `addons/stock/models/digest.py`
- `addons/stock/models/ir_actions_report.py`
- `addons/stock/models/product.py`
- `addons/stock/models/product_strategy.py`
- `addons/stock/models/res_company.py`
- `addons/stock/models/res_config_settings.py`
- `addons/stock/models/res_groups.py`
- `addons/stock/models/res_partner.py`
- `addons/stock/models/res_users.py`
- `addons/stock/models/stock_location.py`
- `addons/stock/models/stock_lot.py`
- `addons/stock/models/stock_move.py`
- `addons/stock/models/stock_move_line.py`
- `addons/stock/models/stock_orderpoint.py`
- `addons/stock/models/stock_package.py`
- `addons/stock/models/stock_package_history.py`
- `addons/stock/models/stock_package_type.py`
- `addons/stock/models/stock_picking.py`
- `addons/stock/models/stock_picking_batch.py`
- `addons/stock/models/stock_picking_type.py`
- `addons/stock/models/stock_quant.py`
- `addons/stock/models/stock_reference.py`
- `addons/stock/models/stock_replenish_mixin.py`
- `addons/stock/models/stock_rule.py`
- `addons/stock/models/stock_scrap_reason_tag.py`
- `addons/stock/models/stock_storage_category.py`
- `addons/stock/models/stock_warehouse.py`
- `addons/stock/populate/benchmarks.xml`
- `addons/stock/populate/populate_demo.xml`
- `addons/stock/report/__init__.py`
- `addons/stock/report/package_templates.xml`
- `addons/stock/report/picking_templates.xml`
- `addons/stock/report/product_templates.xml`
- `addons/stock/report/report_deliveryslip.xml`
- `addons/stock/report/report_location_barcode.xml`
- `addons/stock/report/report_lot_barcode.xml`
- `addons/stock/report/report_package_barcode.xml`
- `addons/stock/report/report_picking_batch.xml`
- `addons/stock/report/report_return_slip.xml`
- `addons/stock/report/report_stock_quantity.py`
- `addons/stock/report/report_stock_quantity.xml`
- `addons/stock/report/report_stock_reception.xml`
- `addons/stock/report/report_stock_rule.py`
- `addons/stock/report/report_stock_rule.xml`
- `addons/stock/report/report_stockinventory.xml`
- `addons/stock/report/report_stockpicking_operations.xml`
- `addons/stock/report/stock_allocation_report.py`
- `addons/stock/report/stock_allocation_report.xml`
- `addons/stock/report/stock_forecasted.py`
- `addons/stock/report/stock_report_views.xml`
- `addons/stock/report/stock_traceability.py`
- `addons/stock/security/ir.access.csv`
- `addons/stock/security/stock_security.xml`
- `addons/stock/static/description/icon.png`
- `addons/stock/static/description/icon.svg`
- `addons/stock/static/description/icon_hi.png`
- `addons/stock/static/img/barcode_scanner.png`
- `addons/stock/static/img/cable_management.jpg`
- `addons/stock/static/img/empty_list.png`
- `addons/stock/static/img/replenishment.svg`
- `addons/stock/static/img/res_partner_address_41.webp`
- `addons/stock/static/img/shapes/batch-picking.svg`
- `addons/stock/static/img/shapes/cluster-picking.svg`
- `addons/stock/static/img/shapes/wave-picking.svg`
- `addons/stock/static/src/allocation_report/allocation_report.js`
- `addons/stock/static/src/allocation_report/allocation_report.scss`
- `addons/stock/static/src/allocation_report/allocation_report.xml`
- `addons/stock/static/src/allocation_report/out_line/out_line.js`
- `addons/stock/static/src/allocation_report/out_line/out_line.xml`
- `addons/stock/static/src/allocation_report/product_line/product_line.js`
- `addons/stock/static/src/allocation_report/product_line/product_line.xml`
- `addons/stock/static/src/client_actions/multi_print.js`
- `addons/stock/static/src/client_actions/stock_traceability_report_backend.js`
- `addons/stock/static/src/client_actions/stock_traceability_report_backend.xml`
- `addons/stock/static/src/components/stock_overview/stock_overview.js`
- `addons/stock/static/src/fields/stock_action_field.js`
- `addons/stock/static/src/fields/stock_action_field.xml`
- `addons/stock/static/src/fields/stock_move_line_x2_many_field.js`
- `addons/stock/static/src/fields/stock_picking_locked_statusbar_field.js`
- `addons/stock/static/src/fields/stock_picking_locked_statusbar_field.xml`
- `addons/stock/static/src/img/barcode.gif`
- `addons/stock/static/src/picking_type_dashboard_graph/picking_type_dashboard_graph_field.js`
- `addons/stock/static/src/picking_type_dashboard_graph/picking_type_dashboard_graph_field.scss`
- `addons/stock/static/src/scss/forecast_widget.scss`
- `addons/stock/static/src/scss/forecasted_details.scss`
- `addons/stock/static/src/scss/product_form.scss`
- `addons/stock/static/src/scss/report_stock_reception_labels.scss`
- `addons/stock/static/src/scss/report_stock_rule.scss`
- `addons/stock/static/src/scss/report_stockpicking_operations.scss`
- `addons/stock/static/src/scss/stock_empty_screen.scss`
- `addons/stock/static/src/scss/stock_forecasted.scss`
- `addons/stock/static/src/scss/stock_move_list.scss`
- `addons/stock/static/src/scss/stock_move_operations.scss`
- `addons/stock/static/src/scss/stock_overview.scss`
- `addons/stock/static/src/scss/stock_picking_batch_empty_screen.scss`
- `addons/stock/static/src/scss/stock_replenishment_info.scss`
- `addons/stock/static/src/scss/stock_traceability_report.scss`
- `addons/stock/static/src/stock_forecasted/forecasted_buttons.js`
- `addons/stock/static/src/stock_forecasted/forecasted_buttons.xml`
- `addons/stock/static/src/stock_forecasted/forecasted_details.js`
- `addons/stock/static/src/stock_forecasted/forecasted_details.xml`
- `addons/stock/static/src/stock_forecasted/forecasted_graph.js`
- `addons/stock/static/src/stock_forecasted/forecasted_graph.xml`
- `addons/stock/static/src/stock_forecasted/forecasted_header.js`
- `addons/stock/static/src/stock_forecasted/forecasted_header.xml`
- `addons/stock/static/src/stock_forecasted/forecasted_warehouse_filter.js`
- `addons/stock/static/src/stock_forecasted/forecasted_warehouse_filter.xml`
- `addons/stock/static/src/stock_forecasted/stock_forecasted.js`
- `addons/stock/static/src/stock_forecasted/stock_forecasted.xml`
- `addons/stock/static/src/stock_picking_many2many_field.js`
- `addons/stock/static/src/stock_warehouse_service.js`
- `addons/stock/static/src/views/list/inventory_report_list_model.js`
- `addons/stock/static/src/views/list/inventory_report_list_view.js`
- `addons/stock/static/src/views/list/stock_add_package_list_view.js`
- `addons/stock/static/src/views/list/stock_report_list_view.js`
- `addons/stock/static/src/views/picking_form/stock_move_description_picking.js`
- `addons/stock/static/src/views/picking_form/stock_move_one2many.js`
- `addons/stock/static/src/views/picking_form/stock_move_one2many.xml`
- `addons/stock/static/src/views/search/stock_orderpoint_search_model.js`
- `addons/stock/static/src/views/search/stock_orderpoint_search_panel.js`
- `addons/stock/static/src/views/search/stock_orderpoint_search_panel.xml`
- `addons/stock/static/src/views/search/stock_report_search_model.js`
- `addons/stock/static/src/views/search/stock_report_search_panel.js`
- `addons/stock/static/src/views/search/stock_report_search_panel.xml`
- `addons/stock/static/src/views/stock_empty_list_help.js`
- `addons/stock/static/src/views/stock_empty_list_help.xml`
- `addons/stock/static/src/views/stock_orderpoint_list_controller.js`
- `addons/stock/static/src/views/stock_orderpoint_list_view.js`
- `addons/stock/static/src/views/stock_orderpoint_list_view.xml`
- `addons/stock/static/src/widgets/counted_quantity_widget.js`
- `addons/stock/static/src/widgets/external_placeholder_integer_field.js`
- `addons/stock/static/src/widgets/external_placeholder_integer_field.xml`
- `addons/stock/static/src/widgets/forced_placeholder.js`
- `addons/stock/static/src/widgets/forced_placeholder.xml`
- `addons/stock/static/src/widgets/forecast_widget.js`
- `addons/stock/static/src/widgets/forecast_widget.xml`
- `addons/stock/static/src/widgets/generate_serial.js`
- `addons/stock/static/src/widgets/json_widget.js`
- `addons/stock/static/src/widgets/json_widget.xml`
- `addons/stock/static/src/widgets/lots_dialog.xml`
- `addons/stock/static/src/widgets/many2many_barcode_tags.js`
- `addons/stock/static/src/widgets/max_qty_to_order_field.js`
- `addons/stock/static/src/widgets/popover_widget.js`
- `addons/stock/static/src/widgets/popover_widget.xml`
- `addons/stock/static/src/widgets/stock_package_m2m.js`
- `addons/stock/static/src/widgets/stock_package_m2o.js`
- `addons/stock/static/src/widgets/stock_package_m2o.xml`
- `addons/stock/static/src/widgets/stock_pick_from.js`
- `addons/stock/static/src/widgets/stock_pick_from.xml`
- `addons/stock/static/src/widgets/stock_rescheduling_popover.js`
- `addons/stock/static/src/widgets/stock_rescheduling_popover.xml`
- `addons/stock/static/src/xml/inventory_lines.xml`
- `addons/stock/static/tests/counted_quantity_widget.test.js`
- `addons/stock/static/tests/forecasted_details.test.js`
- `addons/stock/static/tests/inventory_report_list.test.js`
- `addons/stock/static/tests/popover_widget.test.js`
- `addons/stock/static/tests/stock_kanban_dashboard.test.js`
- `addons/stock/static/tests/stock_traceability_report_backend.test.js`
- `addons/stock/static/tests/tours/stock_flow_tour.js`
- `addons/stock/static/tests/tours/stock_picking_batch_tour.js`
- `addons/stock/static/tests/tours/stock_picking_tour.js`
- `addons/stock/static/tests/tours/stock_report_tests.js`
- `addons/stock/static/tests/tours/tour_helper.js`
- `addons/stock/static/xlsx/stock_quant.xlsx`
- `addons/stock/tests/__init__.py`
- `addons/stock/tests/common.py`
- `addons/stock/tests/test_auto_waving.py`
- `addons/stock/tests/test_batch_picking.py`
- `addons/stock/tests/test_generate_serial_numbers.py`
- `addons/stock/tests/test_immediate.py`
- `addons/stock/tests/test_inventory.py`
- `addons/stock/tests/test_move.py`
- `addons/stock/tests/test_move2.py`
- Additional source files not expanded in this page: 95; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
