# Module: mrp_subcontracting

- **Module ID:** MOD-383
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/mrp_subcontracting`
- **Manifest:** `addons/mrp_subcontracting/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Manufacturing`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Subcontract Productions

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 117 files, including 28 Python, 25 XML, and 12 JavaScript/TypeScript files. The manifest declares dependencies: `mrp`.

## 2. Module structure

- Model/business logic files: 18
- Controller/API files: 2
- XML/data/view/template files: 25
- Browser asset files: 12
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/mrp_subcontracting/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 18 model declarations, 159 methods, 2 constraint handlers, 1 onchange handlers, and 7 dependency declarations.
- **Evidence:** `addons/mrp_subcontracting/models/res_partner.py:7`, `addons/mrp_subcontracting/models/stock_location.py:7`, `addons/mrp_subcontracting/models/stock_move_line.py:8`, `addons/mrp_subcontracting/models/stock_move.py:11`, `addons/mrp_subcontracting/models/stock_quant.py:6`, `addons/mrp_subcontracting/models/product.py:7`, `addons/mrp_subcontracting/models/product.py:20`, `addons/mrp_subcontracting/models/mrp_unbuild.py:7`, `addons/mrp_subcontracting/models/stock_picking.py:14`, `addons/mrp_subcontracting/models/mrp_production.py:11`, `addons/mrp_subcontracting/models/stock_rule.py:8`, `addons/mrp_subcontracting/models/mrp_bom.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 3 route declarations.
- **Evidence:** `addons/mrp_subcontracting/controllers/portal.py:26`, `addons/mrp_subcontracting/controllers/portal.py:79`, `addons/mrp_subcontracting/controllers/portal.py:88`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 25 XML files and 12 JavaScript/TypeScript files; static XML analysis found 36 record/template/menu identifiers.
- **Evidence:** `addons/mrp_subcontracting/report/mrp_report_bom_structure.xml:3`, `addons/mrp_subcontracting/report/mrp_report_bom_structure.xml:32`, `addons/mrp_subcontracting/report/mrp_report_mo_overview.xml:4`, `addons/mrp_subcontracting/report/mrp_report_mo_overview.xml:12`, `addons/mrp_subcontracting/report/mrp_report_mo_overview.xml:23`, `addons/mrp_subcontracting/report/mrp_report_mo_overview.xml:29`, `addons/mrp_subcontracting/data/mrp_subcontracting_data.xml:7`, `addons/mrp_subcontracting/data/portal_entry_data.xml:3`, `addons/mrp_subcontracting/data/mrp_subcontracting_demo.xml:4`, `addons/mrp_subcontracting/data/mrp_subcontracting_demo.xml:11`, `addons/mrp_subcontracting/data/mrp_subcontracting_demo.xml:18`, `addons/mrp_subcontracting/views/stock_move_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/mrp_subcontracting/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/mrp_subcontracting/tests/test_subcontracting_portal_ui.py`, `addons/mrp_subcontracting/tests/common.py`, `addons/mrp_subcontracting/tests/test_subcontracting.py`, `addons/mrp_subcontracting/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 25; representative identifiers: `mrp_subcontracting.report_mrp_bom`, `mrp_subcontracting.report_mrp_bom_pdf_line`, `mrp_subcontracting.mo_overview_content`, `mrp_subcontracting.mo_overview_line`, `mrp_subcontracting.mo_overview_operations`, `mrp_subcontracting.mo_overview_byproducts`, `route_resupply_subcontractor_mto`, `portal_manufacturing_orders`, `mrp_bom_subcontract`, `mrp_bom_line_subcontract`, `product_supplierinfo_subcontracting`, `mrp_subcontracting_stock_move_line_tree_view`, `mrp_subcontracting_portal_stock_move_line_tree_view`, `mrp_subcontracting_view_stock_move_line_operation_tree`, `mrp_subcontracting_view_stock_move_operations`, `mrp_subcontracting_move_form_view`, `mrp_subcontracting_portal_move_form_view`, `mrp_subcontracting_move_tree_view`, `stock_picking_form_view`, `mrp_bom_form_view`
- Menus: 0; representative evidence: Not found in module
- Templates: 11; representative evidence: `addons/mrp_subcontracting/report/mrp_report_bom_structure.xml:3`, `addons/mrp_subcontracting/report/mrp_report_bom_structure.xml:32`, `addons/mrp_subcontracting/report/mrp_report_mo_overview.xml:4`, `addons/mrp_subcontracting/report/mrp_report_mo_overview.xml:12`, `addons/mrp_subcontracting/report/mrp_report_mo_overview.xml:23`, `addons/mrp_subcontracting/report/mrp_report_mo_overview.xml:29`, `addons/mrp_subcontracting/views/subcontracting_portal_templates.xml:4`, `addons/mrp_subcontracting/views/subcontracting_portal_templates.xml:18`, `addons/mrp_subcontracting/views/subcontracting_portal_templates.xml:50`, `addons/mrp_subcontracting/views/subcontracting_portal_templates.xml:65`, `addons/mrp_subcontracting/views/subcontracting_portal_templates.xml:69`
- View/action field declarations: 40; representative evidence: `addons/mrp_subcontracting/views/stock_move_views.xml:6`, `addons/mrp_subcontracting/views/stock_move_views.xml:8`, `addons/mrp_subcontracting/views/stock_move_views.xml:32`, `addons/mrp_subcontracting/views/stock_move_views.xml:36`, `addons/mrp_subcontracting/views/stock_move_views.xml:47`, `addons/mrp_subcontracting/views/stock_move_views.xml:51`, `addons/mrp_subcontracting/views/stock_move_views.xml:59`, `addons/mrp_subcontracting/views/stock_move_views.xml:63`, `addons/mrp_subcontracting/views/stock_move_views.xml:72`, `addons/mrp_subcontracting/views/stock_move_views.xml:74`, `addons/mrp_subcontracting/views/stock_move_views.xml:116`, `addons/mrp_subcontracting/views/stock_move_views.xml:120`
- Browser assets: 12; representative files: `addons/mrp_subcontracting/static/src/components/stock_move_line_x2_many_field.js`, `addons/mrp_subcontracting/static/src/components/subcontracting_production_list_controller.js`, `addons/mrp_subcontracting/static/src/components/subcontracting_production_form_controller.js`, `addons/mrp_subcontracting/static/src/subcontracting_portal/move_list_view.js`, `addons/mrp_subcontracting/static/src/subcontracting_portal/main.js`, `addons/mrp_subcontracting/static/src/subcontracting_portal/subcontracting_portal.js`, `addons/mrp_subcontracting/static/src/subcontracting_portal/picking_form_controller.js`, `addons/mrp_subcontracting/static/src/components/bom_overview_table/mrp_bom_overview_table.js`, `addons/mrp_subcontracting/static/src/components/bom_overview_special_line/mrp_bom_overview_special_line.js`, `addons/mrp_subcontracting/static/src/components/bom_overview_components_block/mrp_bom_overview_components_block.js`, `addons/mrp_subcontracting/static/src/components/mo_overview/mrp_mo_overview.js`, `addons/mrp_subcontracting/static/tests/tours/subcontracting_portal_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/mrp_subcontracting/__manifest__.py`
- **HTTP entry points:** `addons/mrp_subcontracting/controllers/portal.py:26`, `addons/mrp_subcontracting/controllers/portal.py:79`, `addons/mrp_subcontracting/controllers/portal.py:88`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 18
- Representative model evidence: inherits `res.partner` (addons/mrp_subcontracting/models/res_partner.py:7); inherits `stock.location` (addons/mrp_subcontracting/models/stock_location.py:7); inherits `stock.move.line` (addons/mrp_subcontracting/models/stock_move_line.py:8); inherits `stock.move` (addons/mrp_subcontracting/models/stock_move.py:11); inherits `stock.quant` (addons/mrp_subcontracting/models/stock_quant.py:6); inherits `product.supplierinfo` (addons/mrp_subcontracting/models/product.py:7); inherits `product.product` (addons/mrp_subcontracting/models/product.py:20); inherits `mrp.production` (addons/mrp_subcontracting/models/mrp_unbuild.py:7); inherits `stock.picking` (addons/mrp_subcontracting/models/stock_picking.py:14); inherits `mrp.production` (addons/mrp_subcontracting/models/mrp_production.py:11); inherits `stock.rule` (addons/mrp_subcontracting/models/stock_rule.py:8); inherits `mrp.bom` (addons/mrp_subcontracting/models/mrp_bom.py:8); inherits `stock.warehouse` (addons/mrp_subcontracting/models/stock_warehouse.py:8); inherits `res.company` (addons/mrp_subcontracting/models/res_company.py:7); inherits `report.mrp.report_mo_overview` (addons/mrp_subcontracting/report/mrp_report_mo_overview.py:4); inherits `report.mrp.report_bom_structure` (addons/mrp_subcontracting/report/mrp_report_bom_structure.py:7); inherits `mrp.production.serials` (addons/mrp_subcontracting/wizard/mrp_production_serial_numbers.py:6); inherits `change.production.qty` (addons/mrp_subcontracting/wizard/change_production_qty.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 3
- Route evidence: `addons/mrp_subcontracting/controllers/portal.py:26`, `addons/mrp_subcontracting/controllers/portal.py:79`, `addons/mrp_subcontracting/controllers/portal.py:88`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mrp`
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

- `addons/mrp_subcontracting/__init__.py`
- `addons/mrp_subcontracting/__manifest__.py`
- `addons/mrp_subcontracting/controllers/__init__.py`
- `addons/mrp_subcontracting/controllers/portal.py`
- `addons/mrp_subcontracting/data/mrp_subcontracting_data.xml`
- `addons/mrp_subcontracting/data/mrp_subcontracting_demo.xml`
- `addons/mrp_subcontracting/data/portal_entry_data.xml`
- `addons/mrp_subcontracting/i18n/ar.po`
- `addons/mrp_subcontracting/i18n/az.po`
- `addons/mrp_subcontracting/i18n/bg.po`
- `addons/mrp_subcontracting/i18n/bs.po`
- `addons/mrp_subcontracting/i18n/ca.po`
- `addons/mrp_subcontracting/i18n/cs.po`
- `addons/mrp_subcontracting/i18n/da.po`
- `addons/mrp_subcontracting/i18n/de.po`
- `addons/mrp_subcontracting/i18n/el.po`
- `addons/mrp_subcontracting/i18n/es.po`
- `addons/mrp_subcontracting/i18n/es_419.po`
- `addons/mrp_subcontracting/i18n/et.po`
- `addons/mrp_subcontracting/i18n/fa.po`
- `addons/mrp_subcontracting/i18n/fi.po`
- `addons/mrp_subcontracting/i18n/fr.po`
- `addons/mrp_subcontracting/i18n/he.po`
- `addons/mrp_subcontracting/i18n/hi.po`
- `addons/mrp_subcontracting/i18n/hr.po`
- `addons/mrp_subcontracting/i18n/hu.po`
- `addons/mrp_subcontracting/i18n/id.po`
- `addons/mrp_subcontracting/i18n/it.po`
- `addons/mrp_subcontracting/i18n/ja.po`
- `addons/mrp_subcontracting/i18n/kab.po`
- `addons/mrp_subcontracting/i18n/ko.po`
- `addons/mrp_subcontracting/i18n/ku.po`
- `addons/mrp_subcontracting/i18n/lo.po`
- `addons/mrp_subcontracting/i18n/lt.po`
- `addons/mrp_subcontracting/i18n/lv.po`
- `addons/mrp_subcontracting/i18n/mn.po`
- `addons/mrp_subcontracting/i18n/mrp_subcontracting.pot`
- `addons/mrp_subcontracting/i18n/my.po`
- `addons/mrp_subcontracting/i18n/nb.po`
- `addons/mrp_subcontracting/i18n/nl.po`
- `addons/mrp_subcontracting/i18n/pl.po`
- `addons/mrp_subcontracting/i18n/pt.po`
- `addons/mrp_subcontracting/i18n/pt_BR.po`
- `addons/mrp_subcontracting/i18n/ro.po`
- `addons/mrp_subcontracting/i18n/ru.po`
- `addons/mrp_subcontracting/i18n/sk.po`
- `addons/mrp_subcontracting/i18n/sl.po`
- `addons/mrp_subcontracting/i18n/sr@latin.po`
- `addons/mrp_subcontracting/i18n/sv.po`
- `addons/mrp_subcontracting/i18n/th.po`
- `addons/mrp_subcontracting/i18n/tr.po`
- `addons/mrp_subcontracting/i18n/uk.po`
- `addons/mrp_subcontracting/i18n/uz.po`
- `addons/mrp_subcontracting/i18n/vi.po`
- `addons/mrp_subcontracting/i18n/zh_CN.po`
- `addons/mrp_subcontracting/i18n/zh_TW.po`
- `addons/mrp_subcontracting/models/__init__.py`
- `addons/mrp_subcontracting/models/mrp_bom.py`
- `addons/mrp_subcontracting/models/mrp_production.py`
- `addons/mrp_subcontracting/models/mrp_unbuild.py`
- `addons/mrp_subcontracting/models/product.py`
- `addons/mrp_subcontracting/models/res_company.py`
- `addons/mrp_subcontracting/models/res_partner.py`
- `addons/mrp_subcontracting/models/stock_location.py`
- `addons/mrp_subcontracting/models/stock_move.py`
- `addons/mrp_subcontracting/models/stock_move_line.py`
- `addons/mrp_subcontracting/models/stock_picking.py`
- `addons/mrp_subcontracting/models/stock_quant.py`
- `addons/mrp_subcontracting/models/stock_rule.py`
- `addons/mrp_subcontracting/models/stock_warehouse.py`
- `addons/mrp_subcontracting/report/__init__.py`
- `addons/mrp_subcontracting/report/mrp_report_bom_structure.py`
- `addons/mrp_subcontracting/report/mrp_report_bom_structure.xml`
- `addons/mrp_subcontracting/report/mrp_report_mo_overview.py`
- `addons/mrp_subcontracting/report/mrp_report_mo_overview.xml`
- `addons/mrp_subcontracting/security/ir.access.csv`
- `addons/mrp_subcontracting/static/src/components/bom_overview_components_block/mrp_bom_overview_components_block.js`
- `addons/mrp_subcontracting/static/src/components/bom_overview_components_block/mrp_bom_overview_components_block.xml`
- `addons/mrp_subcontracting/static/src/components/bom_overview_line/mrp_bom_overview_line.xml`
- `addons/mrp_subcontracting/static/src/components/bom_overview_special_line/mrp_bom_overview_special_line.js`
- `addons/mrp_subcontracting/static/src/components/bom_overview_special_line/mrp_bom_overview_special_line.xml`
- `addons/mrp_subcontracting/static/src/components/bom_overview_table/mrp_bom_overview_table.js`
- `addons/mrp_subcontracting/static/src/components/bom_overview_table/mrp_bom_overview_table.xml`
- `addons/mrp_subcontracting/static/src/components/mo_overview/mrp_mo_overview.js`
- `addons/mrp_subcontracting/static/src/components/mo_overview/mrp_mo_overview.xml`
- `addons/mrp_subcontracting/static/src/components/mo_overview_byproducts_block/mo_overview_byproducts_block.xml`
- `addons/mrp_subcontracting/static/src/components/mo_overview_line/mrp_mo_overview_line.xml`
- `addons/mrp_subcontracting/static/src/components/mo_overview_operations_block/mo_overview_operations_block.xml`
- `addons/mrp_subcontracting/static/src/components/stock_move_line_x2_many_field.js`
- `addons/mrp_subcontracting/static/src/components/subcontracting_production_form_controller.js`
- `addons/mrp_subcontracting/static/src/components/subcontracting_production_list_controller.js`
- `addons/mrp_subcontracting/static/src/img/manufacturing.svg`
- `addons/mrp_subcontracting/static/src/scss/subcontracting_portal.scss`
- `addons/mrp_subcontracting/static/src/subcontracting_portal/main.js`
- `addons/mrp_subcontracting/static/src/subcontracting_portal/move_list_view.js`
- `addons/mrp_subcontracting/static/src/subcontracting_portal/picking_form_controller.js`
- `addons/mrp_subcontracting/static/src/subcontracting_portal/picking_form_controller.xml`
- `addons/mrp_subcontracting/static/src/subcontracting_portal/subcontracting_portal.js`
- `addons/mrp_subcontracting/static/src/subcontracting_portal/subcontracting_portal.xml`
- `addons/mrp_subcontracting/static/tests/tours/subcontracting_portal_tour.js`
- `addons/mrp_subcontracting/tests/__init__.py`
- `addons/mrp_subcontracting/tests/common.py`
- `addons/mrp_subcontracting/tests/test_subcontracting.py`
- `addons/mrp_subcontracting/tests/test_subcontracting_portal_ui.py`
- `addons/mrp_subcontracting/views/mrp_bom_views.xml`
- `addons/mrp_subcontracting/views/mrp_production_views.xml`
- `addons/mrp_subcontracting/views/res_partner_views.xml`
- `addons/mrp_subcontracting/views/stock_move_views.xml`
- `addons/mrp_subcontracting/views/stock_picking_views.xml`
- `addons/mrp_subcontracting/views/stock_quant_views.xml`
- `addons/mrp_subcontracting/views/stock_warehouse_views.xml`
- `addons/mrp_subcontracting/views/subcontracting_portal_templates.xml`
- `addons/mrp_subcontracting/views/subcontracting_portal_views.xml`
- `addons/mrp_subcontracting/views/supplier_info_views.xml`
- `addons/mrp_subcontracting/wizard/__init__.py`
- `addons/mrp_subcontracting/wizard/change_production_qty.py`
- `addons/mrp_subcontracting/wizard/mrp_production_serial_numbers.py`
