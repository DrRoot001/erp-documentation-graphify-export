# Module: stock_delivery

- **Module ID:** MOD-561
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/stock_delivery`
- **Manifest:** `addons/stock_delivery/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Shipping Connectors`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Allows you to add delivery methods in pickings.
===============================================

When creating invoices from picking, the system is able to add and compute the shipping line.

**Scope evidence:** The module contains 102 files, including 30 Python, 21 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `printer`, `sale_stock`, `delivery`.

## 2. Module structure

- Model/business logic files: 20
- Controller/API files: 0
- XML/data/view/template files: 21
- Browser asset files: 1
- Security files: 1
- Test files: 8
- Scheduled/automation evidence files: 0
- Reporting evidence files: 3

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/stock_delivery/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 20 model declarations, 145 methods, 0 constraint handlers, 2 onchange handlers, and 12 dependency declarations.
- **Evidence:** `addons/stock_delivery/models/res_partner.py:6`, `addons/stock_delivery/models/sale_order.py:6`, `addons/stock_delivery/models/sale_order.py:43`, `addons/stock_delivery/models/product_product.py:4`, `addons/stock_delivery/models/product_template.py:6`, `addons/stock_delivery/models/delivery_carrier.py:12`, `addons/stock_delivery/models/stock_move.py:8`, `addons/stock_delivery/models/stock_move.py:14`, `addons/stock_delivery/models/stock_move.py:71`, `addons/stock_delivery/models/ir_actions_report.py:13`, `addons/stock_delivery/models/stock_picking_batch.py:6`, `addons/stock_delivery/models/stock_picking_type.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 21 XML files and 1 JavaScript/TypeScript files; static XML analysis found 50 record/template/menu identifiers.
- **Evidence:** `addons/stock_delivery/report/shipping_reports.xml:7`, `addons/stock_delivery/report/shipping_reports.xml:15`, `addons/stock_delivery/report/shipping_reports.xml:5`, `addons/stock_delivery/report/shipping_reports.xml:6`, `addons/stock_delivery/report/product_templates.xml:3`, `addons/stock_delivery/report/product_templates.xml:10`, `addons/stock_delivery/wizard/stock_put_in_pack_views.xml:3`, `addons/stock_delivery/wizard/pay_on_delivery_views.xml:4`, `addons/stock_delivery/wizard/choose_delivery_carrier_views.xml:3`, `addons/stock_delivery/data/mail_template_data.xml:4`, `addons/stock_delivery/data/delivery_demo.xml:6`, `addons/stock_delivery/data/delivery_demo.xml:25`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/stock_delivery/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 3 files contain report-action/template indicators.
- **Evidence:** `addons/stock_delivery/models/ir_actions_report.py`, `addons/stock_delivery/report/shipping_reports.xml`, `addons/stock_delivery/views/ir_actions_report.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 8 test files are present.
- **Evidence:** `addons/stock_delivery/tests/test_pay_on_delivery.py`, `addons/stock_delivery/tests/test_packing_delivery.py`, `addons/stock_delivery/tests/test_delivery_stock_move.py`, `addons/stock_delivery/tests/test_printer_tour.py`, `addons/stock_delivery/tests/test_delivery_picking_batch.py`, `addons/stock_delivery/tests/test_carrier_propagation.py`, `addons/stock_delivery/tests/__init__.py`, `addons/stock_delivery/tests/test_delivery_cost.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 21; representative identifiers: `action_report_shipping_labels`, `action_report_shipping_docs`, `report_shipping_labels`, `report_shipping_docs`, `barcode_normal_label`, `barcode_alternative_label`, `stock_put_in_pack_form`, `pay_on_delivery_form`, `choose_delivery_carrier_view_form`, `delivery.mail_template_data_delivery_note`, `outgoing_shipment_with_carrier_confirmed`, `outgoing_shipment_with_carrier_assigned`, `outgoing_shipment_with_carrier_done`, `printer.zebra_printer_demo`, `product_product_hs_code`, `product_product_hs_code_list`, `stock_package_type_form_delivery`, `stock_package_type_tree_delivery`, `product_template_hs_code`, `view_picking_type_form_delivery`
- Menus: 5; representative evidence: `addons/stock_delivery/views/stock_menu_views.xml:4`, `addons/stock_delivery/views/stock_menu_views.xml:5`, `addons/stock_delivery/views/stock_menu_views.xml:6`, `addons/stock_delivery/views/delivery_view.xml:60`, `addons/stock_delivery/views/delivery_view.xml:61`
- Templates: 14; representative evidence: `addons/stock_delivery/report/shipping_reports.xml:5`, `addons/stock_delivery/report/shipping_reports.xml:6`, `addons/stock_delivery/report/product_templates.xml:3`, `addons/stock_delivery/report/product_templates.xml:10`, `addons/stock_delivery/views/delivery_portal_template.xml:3`, `addons/stock_delivery/views/report_deliveryslip.xml:3`, `addons/stock_delivery/views/report_deliveryslip.xml:37`, `addons/stock_delivery/views/report_deliveryslip.xml:42`, `addons/stock_delivery/views/report_deliveryslip.xml:49`, `addons/stock_delivery/views/report_deliveryslip.xml:68`, `addons/stock_delivery/views/report_package_barcode.xml:3`, `addons/stock_delivery/views/report_package_barcode.xml:33`
- View/action field declarations: 46; representative evidence: `addons/stock_delivery/report/shipping_reports.xml:9`, `addons/stock_delivery/report/shipping_reports.xml:17`, `addons/stock_delivery/wizard/stock_put_in_pack_views.xml:5`, `addons/stock_delivery/wizard/stock_put_in_pack_views.xml:7`, `addons/stock_delivery/wizard/pay_on_delivery_views.xml:6`, `addons/stock_delivery/wizard/pay_on_delivery_views.xml:7`, `addons/stock_delivery/wizard/choose_delivery_carrier_views.xml:5`, `addons/stock_delivery/wizard/choose_delivery_carrier_views.xml:7`, `addons/stock_delivery/views/product_product_view.xml:6`, `addons/stock_delivery/views/product_product_view.xml:8`, `addons/stock_delivery/views/product_product_view.xml:18`, `addons/stock_delivery/views/product_product_view.xml:20`
- Browser assets: 1; representative files: `addons/stock_delivery/static/src/return_order_dialog/return_order_dialog.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/stock_delivery/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/stock_delivery/models/ir_actions_report.py`, `addons/stock_delivery/report/shipping_reports.xml`, `addons/stock_delivery/views/ir_actions_report.xml`

## 7. Database interactions

- Model declarations: 20
- Representative model evidence: inherits `res.partner` (addons/stock_delivery/models/res_partner.py:6); inherits `sale.order` (addons/stock_delivery/models/sale_order.py:6); inherits `sale.order.line` (addons/stock_delivery/models/sale_order.py:43); inherits `product.product` (addons/stock_delivery/models/product_product.py:4); inherits `product.template` (addons/stock_delivery/models/product_template.py:6); inherits `delivery.carrier` (addons/stock_delivery/models/delivery_carrier.py:12); inherits `stock.route` (addons/stock_delivery/models/stock_move.py:8); inherits `stock.move` (addons/stock_delivery/models/stock_move.py:14); inherits `stock.move.line` (addons/stock_delivery/models/stock_move.py:71); inherits `ir.actions.report` (addons/stock_delivery/models/ir_actions_report.py:13); inherits `stock.picking.batch` (addons/stock_delivery/models/stock_picking_batch.py:6); inherits `stock.picking.type` (addons/stock_delivery/models/stock_picking_type.py:6); inherits `stock.package.type` (addons/stock_delivery/models/stock_package_type.py:6); inherits `stock.picking` (addons/stock_delivery/models/stock_picking.py:13); inherits `stock.package` (addons/stock_delivery/models/stock_package.py:6); `pay.on.delivery` (addons/stock_delivery/wizard/pay_on_delivery.py:7); inherits `product.label.layout` (addons/stock_delivery/wizard/product_label_layout.py:4); inherits `stock.package.label.layout` (addons/stock_delivery/wizard/stock_package_label_layout.py:4); inherits `stock.put.in.pack` (addons/stock_delivery/wizard/stock_put_in_pack.py:6); inherits `choose.delivery.carrier` (addons/stock_delivery/wizard/choose_delivery_carrier.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `printer`, `sale_stock`, `delivery`
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

- `addons/stock_delivery/__init__.py`
- `addons/stock_delivery/__manifest__.py`
- `addons/stock_delivery/data/delivery_demo.xml`
- `addons/stock_delivery/data/mail_template_data.xml`
- `addons/stock_delivery/i18n/ar.po`
- `addons/stock_delivery/i18n/az.po`
- `addons/stock_delivery/i18n/bg.po`
- `addons/stock_delivery/i18n/bs.po`
- `addons/stock_delivery/i18n/ca.po`
- `addons/stock_delivery/i18n/cs.po`
- `addons/stock_delivery/i18n/da.po`
- `addons/stock_delivery/i18n/de.po`
- `addons/stock_delivery/i18n/el.po`
- `addons/stock_delivery/i18n/es.po`
- `addons/stock_delivery/i18n/es_419.po`
- `addons/stock_delivery/i18n/et.po`
- `addons/stock_delivery/i18n/fa.po`
- `addons/stock_delivery/i18n/fi.po`
- `addons/stock_delivery/i18n/fr.po`
- `addons/stock_delivery/i18n/he.po`
- `addons/stock_delivery/i18n/hi.po`
- `addons/stock_delivery/i18n/hr.po`
- `addons/stock_delivery/i18n/hu.po`
- `addons/stock_delivery/i18n/id.po`
- `addons/stock_delivery/i18n/it.po`
- `addons/stock_delivery/i18n/ja.po`
- `addons/stock_delivery/i18n/kab.po`
- `addons/stock_delivery/i18n/ko.po`
- `addons/stock_delivery/i18n/ku.po`
- `addons/stock_delivery/i18n/lo.po`
- `addons/stock_delivery/i18n/lt.po`
- `addons/stock_delivery/i18n/lv.po`
- `addons/stock_delivery/i18n/mn.po`
- `addons/stock_delivery/i18n/my.po`
- `addons/stock_delivery/i18n/nb.po`
- `addons/stock_delivery/i18n/nl.po`
- `addons/stock_delivery/i18n/pl.po`
- `addons/stock_delivery/i18n/pt.po`
- `addons/stock_delivery/i18n/pt_BR.po`
- `addons/stock_delivery/i18n/ro.po`
- `addons/stock_delivery/i18n/ru.po`
- `addons/stock_delivery/i18n/sk.po`
- `addons/stock_delivery/i18n/sl.po`
- `addons/stock_delivery/i18n/sr@latin.po`
- `addons/stock_delivery/i18n/stock_delivery.pot`
- `addons/stock_delivery/i18n/sv.po`
- `addons/stock_delivery/i18n/th.po`
- `addons/stock_delivery/i18n/tr.po`
- `addons/stock_delivery/i18n/uk.po`
- `addons/stock_delivery/i18n/uz.po`
- `addons/stock_delivery/i18n/vi.po`
- `addons/stock_delivery/i18n/zh_CN.po`
- `addons/stock_delivery/i18n/zh_TW.po`
- `addons/stock_delivery/models/__init__.py`
- `addons/stock_delivery/models/delivery_carrier.py`
- `addons/stock_delivery/models/delivery_request_objects.py`
- `addons/stock_delivery/models/ir_actions_report.py`
- `addons/stock_delivery/models/product_product.py`
- `addons/stock_delivery/models/product_template.py`
- `addons/stock_delivery/models/res_partner.py`
- `addons/stock_delivery/models/sale_order.py`
- `addons/stock_delivery/models/stock_move.py`
- `addons/stock_delivery/models/stock_package.py`
- `addons/stock_delivery/models/stock_package_type.py`
- `addons/stock_delivery/models/stock_picking.py`
- `addons/stock_delivery/models/stock_picking_batch.py`
- `addons/stock_delivery/models/stock_picking_type.py`
- `addons/stock_delivery/report/product_templates.xml`
- `addons/stock_delivery/report/shipping_reports.xml`
- `addons/stock_delivery/security/ir.access.csv`
- `addons/stock_delivery/static/src/return_order_dialog/return_label_info.xml`
- `addons/stock_delivery/static/src/return_order_dialog/return_order_dialog.js`
- `addons/stock_delivery/tests/__init__.py`
- `addons/stock_delivery/tests/test_carrier_propagation.py`
- `addons/stock_delivery/tests/test_delivery_cost.py`
- `addons/stock_delivery/tests/test_delivery_picking_batch.py`
- `addons/stock_delivery/tests/test_delivery_stock_move.py`
- `addons/stock_delivery/tests/test_packing_delivery.py`
- `addons/stock_delivery/tests/test_pay_on_delivery.py`
- `addons/stock_delivery/tests/test_printer_tour.py`
- `addons/stock_delivery/views/delivery_portal_template.xml`
- `addons/stock_delivery/views/delivery_view.xml`
- `addons/stock_delivery/views/ir_actions_report.xml`
- `addons/stock_delivery/views/product_product_view.xml`
- `addons/stock_delivery/views/product_template_view.xml`
- `addons/stock_delivery/views/report_deliveryslip.xml`
- `addons/stock_delivery/views/report_package_barcode.xml`
- `addons/stock_delivery/views/report_shipping.xml`
- `addons/stock_delivery/views/stock_menu_views.xml`
- `addons/stock_delivery/views/stock_move_line_views.xml`
- `addons/stock_delivery/views/stock_package_type_views.xml`
- `addons/stock_delivery/views/stock_picking_type_views.xml`
- `addons/stock_delivery/views/stock_rule_views.xml`
- `addons/stock_delivery/wizard/__init__.py`
- `addons/stock_delivery/wizard/choose_delivery_carrier.py`
- `addons/stock_delivery/wizard/choose_delivery_carrier_views.xml`
- `addons/stock_delivery/wizard/pay_on_delivery.py`
- `addons/stock_delivery/wizard/pay_on_delivery_views.xml`
- `addons/stock_delivery/wizard/product_label_layout.py`
- `addons/stock_delivery/wizard/stock_package_label_layout.py`
- `addons/stock_delivery/wizard/stock_put_in_pack.py`
- `addons/stock_delivery/wizard/stock_put_in_pack_views.xml`
