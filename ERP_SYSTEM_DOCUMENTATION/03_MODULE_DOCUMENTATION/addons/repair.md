# Module: repair

- **Module ID:** MOD-505
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/repair`
- **Manifest:** `addons/repair/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Supply Chain/Inventory`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Repair damaged products

**Manifest description:**

The aim is to have a complete module to manage all products repairs.
====================================================================

The following topics are covered by this module:
------------------------------------------------------
    * Add/remove products in the reparation
    * Impact for stocks
    * Warranty concept
    * Repair quotation report
    * Notes for the technician and for the final customer

**Scope evidence:** The module contains 111 files, including 24 Python, 14 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `sale_stock`, `sale_management`.

## 2. Module structure

- Model/business logic files: 20
- Controller/API files: 0
- XML/data/view/template files: 14
- Browser asset files: 3
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 2
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/repair/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 20 model declarations, 192 methods, 0 constraint handlers, 2 onchange handlers, and 35 dependency declarations.
- **Evidence:** `addons/repair/models/res_partner.py:4`, `addons/repair/models/sale_order.py:7`, `addons/repair/models/sale_order.py:50`, `addons/repair/models/stock_move_line.py:6`, `addons/repair/models/stock_move.py:14`, `addons/repair/models/product.py:7`, `addons/repair/models/product.py:32`, `addons/repair/models/repair.py:19`, `addons/repair/models/repair.py:812`, `addons/repair/models/stock_picking.py:10`, `addons/repair/models/stock_picking.py:160`, `addons/repair/models/account_move.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 14 XML files and 3 JavaScript/TypeScript files; static XML analysis found 46 record/template/menu identifiers.
- **Evidence:** `addons/repair/report/repair_reports.xml:4`, `addons/repair/report/repair_templates_repair_order.xml:4`, `addons/repair/report/repair_templates_repair_order.xml:75`, `addons/repair/wizard/repair_consumption_warning_views.xml:5`, `addons/repair/wizard/repair_consumption_warning_views.xml:33`, `addons/repair/data/repair_data.xml:9`, `addons/repair/data/repair_data.xml:21`, `addons/repair/data/repair_demo.xml:3`, `addons/repair/data/repair_demo.xml:12`, `addons/repair/data/repair_demo.xml:31`, `addons/repair/data/repair_demo.xml:50`, `addons/repair/views/stock_move_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/repair/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/repair/views/stock_picking_views.xml`, `addons/repair/views/repair_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/repair/report/repair_reports.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/repair/tests/test_repair.py`, `addons/repair/tests/test_rules_installation.py`, `addons/repair/tests/test_anglo_saxon_valuation.py`, `addons/repair/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 14; representative identifiers: `action_report_repair_order`, `report_repairorder`, `report_repairorder2`, `view_repair_consumption_warning_form`, `action_repair_consumption_warning`, `picking_type_warehouse0_repair`, `stock.warehouse0`, `product_service_order_repair`, `repair_r1`, `repair_r0`, `repair_r2`, `action_repair_move_lines`, `repair_view_picking_type_form`, `repair_view_picking_form`, `stock_repair_type_kanban`, `action_create_repair_order`, `view_sale_order_form_inherit_repair`, `view_account_move_form_inherit_repair`, `view_product_template_form_inherit_repair`, `product_view_search_catalog`
- Menus: 7; representative evidence: `addons/repair/views/repair_views.xml:434`, `addons/repair/views/repair_views.xml:437`, `addons/repair/views/repair_views.xml:440`, `addons/repair/views/repair_views.xml:442`, `addons/repair/views/repair_views.xml:444`, `addons/repair/views/repair_views.xml:446`, `addons/repair/views/repair_views.xml:448`
- Templates: 2; representative evidence: `addons/repair/report/repair_templates_repair_order.xml:4`, `addons/repair/report/repair_templates_repair_order.xml:75`
- View/action field declarations: 56; representative evidence: `addons/repair/report/repair_reports.xml:6`, `addons/repair/wizard/repair_consumption_warning_views.xml:7`, `addons/repair/wizard/repair_consumption_warning_views.xml:8`, `addons/repair/wizard/repair_consumption_warning_views.xml:35`, `addons/repair/wizard/repair_consumption_warning_views.xml:36`, `addons/repair/views/stock_move_views.xml:6`, `addons/repair/views/stock_move_views.xml:7`, `addons/repair/views/stock_picking_views.xml:5`, `addons/repair/views/stock_picking_views.xml:7`, `addons/repair/views/stock_picking_views.xml:35`, `addons/repair/views/stock_picking_views.xml:37`, `addons/repair/views/stock_picking_views.xml:51`
- Browser assets: 3; representative files: `addons/repair/static/src/components/product_catalog/kanban_renderer.js`, `addons/repair/static/src/components/product_catalog/kanban_controller.js`, `addons/repair/static/tests/tours/repair_order.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/repair/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/repair/views/stock_picking_views.xml`, `addons/repair/views/repair_views.xml`
- **Report entry points:** `addons/repair/report/repair_reports.xml`

## 7. Database interactions

- Model declarations: 20
- Representative model evidence: inherits `res.partner` (addons/repair/models/res_partner.py:4); inherits `sale.order` (addons/repair/models/sale_order.py:7); inherits `sale.order.line` (addons/repair/models/sale_order.py:50); inherits `stock.move.line` (addons/repair/models/stock_move_line.py:6); inherits `stock.move` (addons/repair/models/stock_move.py:14); inherits `product.product` (addons/repair/models/product.py:7); inherits `product.template` (addons/repair/models/product.py:32); `repair.order` (addons/repair/models/repair.py:19); `repair.tags` (addons/repair/models/repair.py:812); inherits `stock.picking.type` (addons/repair/models/stock_picking.py:10); inherits `stock.picking` (addons/repair/models/stock_picking.py:160); `account.move` (addons/repair/models/account_move.py:4); inherits `account.move.line` (addons/repair/models/account_move_line.py:4); `repair.service.line` (addons/repair/models/repair_service_line.py:5); inherits `stock.lot` (addons/repair/models/stock_lot.py:8); inherits `stock.warehouse` (addons/repair/models/stock_warehouse.py:8); inherits `stock.traceability.report` (addons/repair/report/stock_traceability.py:6); inherits `stock.forecasted_product_product` (addons/repair/report/stock_forecasted.py:7); `repair.consumption.warning` (addons/repair/wizard/repair_consumption_warning.py:4); `repair.consumption.warning.line` (addons/repair/wizard/repair_consumption_warning.py:31)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale_stock`, `sale_management`
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

- `addons/repair/__init__.py`
- `addons/repair/__manifest__.py`
- `addons/repair/data/repair_data.xml`
- `addons/repair/data/repair_demo.xml`
- `addons/repair/i18n/af.po`
- `addons/repair/i18n/am.po`
- `addons/repair/i18n/ar.po`
- `addons/repair/i18n/az.po`
- `addons/repair/i18n/bg.po`
- `addons/repair/i18n/bs.po`
- `addons/repair/i18n/ca.po`
- `addons/repair/i18n/cs.po`
- `addons/repair/i18n/da.po`
- `addons/repair/i18n/de.po`
- `addons/repair/i18n/el.po`
- `addons/repair/i18n/es.po`
- `addons/repair/i18n/es_419.po`
- `addons/repair/i18n/es_CL.po`
- `addons/repair/i18n/et.po`
- `addons/repair/i18n/eu.po`
- `addons/repair/i18n/fa.po`
- `addons/repair/i18n/fi.po`
- `addons/repair/i18n/fo.po`
- `addons/repair/i18n/fr.po`
- `addons/repair/i18n/fr_BE.po`
- `addons/repair/i18n/fr_CA.po`
- `addons/repair/i18n/gl.po`
- `addons/repair/i18n/gu.po`
- `addons/repair/i18n/he.po`
- `addons/repair/i18n/hi.po`
- `addons/repair/i18n/hr.po`
- `addons/repair/i18n/hu.po`
- `addons/repair/i18n/id.po`
- `addons/repair/i18n/is.po`
- `addons/repair/i18n/it.po`
- `addons/repair/i18n/ja.po`
- `addons/repair/i18n/ka.po`
- `addons/repair/i18n/kab.po`
- `addons/repair/i18n/km.po`
- `addons/repair/i18n/ko.po`
- `addons/repair/i18n/ku.po`
- `addons/repair/i18n/lb.po`
- `addons/repair/i18n/lo.po`
- `addons/repair/i18n/lt.po`
- `addons/repair/i18n/lv.po`
- `addons/repair/i18n/mk.po`
- `addons/repair/i18n/mn.po`
- `addons/repair/i18n/my.po`
- `addons/repair/i18n/nb.po`
- `addons/repair/i18n/nl.po`
- `addons/repair/i18n/pl.po`
- `addons/repair/i18n/pt.po`
- `addons/repair/i18n/pt_BR.po`
- `addons/repair/i18n/repair.pot`
- `addons/repair/i18n/ro.po`
- `addons/repair/i18n/ru.po`
- `addons/repair/i18n/sk.po`
- `addons/repair/i18n/sl.po`
- `addons/repair/i18n/sq.po`
- `addons/repair/i18n/sr@latin.po`
- `addons/repair/i18n/sv.po`
- `addons/repair/i18n/ta.po`
- `addons/repair/i18n/te.po`
- `addons/repair/i18n/th.po`
- `addons/repair/i18n/tr.po`
- `addons/repair/i18n/uk.po`
- `addons/repair/i18n/uz.po`
- `addons/repair/i18n/vi.po`
- `addons/repair/i18n/zh_CN.po`
- `addons/repair/i18n/zh_TW.po`
- `addons/repair/models/__init__.py`
- `addons/repair/models/account_move.py`
- `addons/repair/models/account_move_line.py`
- `addons/repair/models/product.py`
- `addons/repair/models/repair.py`
- `addons/repair/models/repair_service_line.py`
- `addons/repair/models/res_partner.py`
- `addons/repair/models/sale_order.py`
- `addons/repair/models/stock_lot.py`
- `addons/repair/models/stock_move.py`
- `addons/repair/models/stock_move_line.py`
- `addons/repair/models/stock_picking.py`
- `addons/repair/models/stock_warehouse.py`
- `addons/repair/report/__init__.py`
- `addons/repair/report/repair_reports.xml`
- `addons/repair/report/repair_templates_repair_order.xml`
- `addons/repair/report/stock_forecasted.py`
- `addons/repair/report/stock_traceability.py`
- `addons/repair/security/ir.access.csv`
- `addons/repair/static/description/icon.png`
- `addons/repair/static/description/icon.svg`
- `addons/repair/static/description/icon_hi.png`
- `addons/repair/static/src/components/product_catalog/kanban_controller.js`
- `addons/repair/static/src/components/product_catalog/kanban_renderer.js`
- `addons/repair/static/tests/tours/repair_order.js`
- `addons/repair/tests/__init__.py`
- `addons/repair/tests/test_anglo_saxon_valuation.py`
- `addons/repair/tests/test_repair.py`
- `addons/repair/tests/test_rules_installation.py`
- `addons/repair/views/account_move_views.xml`
- `addons/repair/views/product_views.xml`
- `addons/repair/views/repair_views.xml`
- `addons/repair/views/res_partner_views.xml`
- `addons/repair/views/sale_order_views.xml`
- `addons/repair/views/stock_lot_views.xml`
- `addons/repair/views/stock_move_views.xml`
- `addons/repair/views/stock_picking_views.xml`
- `addons/repair/views/stock_warehouse_views.xml`
- `addons/repair/wizard/__init__.py`
- `addons/repair/wizard/repair_consumption_warning.py`
- `addons/repair/wizard/repair_consumption_warning_views.xml`
