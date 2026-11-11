# Module: mrp

- **Module ID:** MOD-377
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/mrp`
- **Manifest:** `addons/mrp/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Supply Chain/Manufacturing`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Manufacturing Orders & BOMs

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 283 files, including 69 Python, 62 XML, and 52 JavaScript/TypeScript files. The manifest declares dependencies: `product`, `stock`, `resource`.

## 2. Module structure

- Model/business logic files: 55
- Controller/API files: 0
- XML/data/view/template files: 62
- Browser asset files: 52
- Security files: 2
- Test files: 25
- Scheduled/automation evidence files: 4
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/mrp/security/mrp_security.xml`, `addons/mrp/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 55 model declarations, 1173 methods, 16 constraint handlers, 17 onchange handlers, and 129 dependency declarations.
- **Evidence:** `addons/mrp/models/stock_move_line.py:7`, `addons/mrp/models/res_groups.py:6`, `addons/mrp/models/product_uom.py:4`, `addons/mrp/models/res_config_settings.py:7`, `addons/mrp/models/stock_move.py:9`, `addons/mrp/models/stock_quant.py:5`, `addons/mrp/models/mrp_routing.py:9`, `addons/mrp/models/product.py:22`, `addons/mrp/models/product.py:121`, `addons/mrp/models/mrp_workcenter.py:21`, `addons/mrp/models/mrp_workcenter.py:450`, `addons/mrp/models/mrp_workcenter.py:467`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 62 XML files and 52 JavaScript/TypeScript files; static XML analysis found 315 record/template/menu identifiers.
- **Evidence:** `addons/mrp/security/mrp_security.xml:4`, `addons/mrp/security/mrp_security.xml:10`, `addons/mrp/security/mrp_security.xml:16`, `addons/mrp/security/mrp_security.xml:26`, `addons/mrp/security/mrp_security.xml:30`, `addons/mrp/security/mrp_security.xml:34`, `addons/mrp/report/mrp_zebra_production_templates.xml:4`, `addons/mrp/report/mrp_production_templates.xml:3`, `addons/mrp/report/mrp_production_templates.xml:125`, `addons/mrp/report/mrp_production_templates.xml:174`, `addons/mrp/report/mrp_production_templates.xml:208`, `addons/mrp/report/mrp_workorder_templates.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/mrp/security/mrp_security.xml`, `addons/mrp/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 4 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/mrp/views/stock_move_views.xml`, `addons/mrp/views/mrp_bom_views.xml`, `addons/mrp/views/mrp_production_views.xml`, `addons/mrp/views/mrp_workorder_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/mrp/report/mrp_report_views_main.xml`, `addons/mrp/tests/test_stock_report.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 25 test files are present.
- **Evidence:** `addons/mrp/tests/test_cancel_mo.py`, `addons/mrp/tests/test_mrp_reports.py`, `addons/mrp/tests/test_performance.py`, `addons/mrp/tests/test_quant.py`, `addons/mrp/tests/test_consumption_warning.py`, `addons/mrp/tests/test_warehouse_multistep_manufacturing.py`, `addons/mrp/tests/test_manual_consumption.py`, `addons/mrp/tests/test_unbuild.py`, `addons/mrp/tests/test_replenish.py`, `addons/mrp/tests/test_bom.py`, `addons/mrp/tests/test_oee.py`, `addons/mrp/tests/test_stock_report.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 62; representative identifiers: `res_groups_privilege_manufacturing`, `group_mrp_user`, `group_mrp_manager`, `group_mrp_routings`, `group_mrp_byproducts`, `group_unlocked_by_default`, `finished_product_zpl_label`, `report_mrporder`, `report_mrp_production_components`, `finished_product_4x12_label`, `report_mrp_packages`, `report_mrp_workorder`, `mrp_report_stock_rule`, `action_report_production_order`, `action_report_bom_structure`, `action_report_mrp_mo_overview`, `action_report_workorder`, `action_report_mrp_packages`, `stock_report_delivery_document_inherit_mrp`, `stock_report_delivery_kit_sections`
- Menus: 20; representative evidence: `addons/mrp/views/stock_move_views.xml:97`, `addons/mrp/views/stock_move_views.xml:104`, `addons/mrp/views/stock_move_views.xml:110`, `addons/mrp/views/mrp_workcenter_views.xml:423`, `addons/mrp/views/mrp_workcenter_views.xml:591`, `addons/mrp/views/stock_picking_views.xml:211`, `addons/mrp/views/res_config_settings_views.xml:66`, `addons/mrp/views/mrp_bom_views.xml:391`, `addons/mrp/views/mrp_production_views.xml:922`, `addons/mrp/views/mrp_production_views.xml:927`, `addons/mrp/views/mrp_production_views.xml:933`, `addons/mrp/views/mrp_unbuild_views.xml:168`
- Templates: 22; representative evidence: `addons/mrp/report/mrp_zebra_production_templates.xml:4`, `addons/mrp/report/mrp_production_templates.xml:3`, `addons/mrp/report/mrp_production_templates.xml:125`, `addons/mrp/report/mrp_production_templates.xml:174`, `addons/mrp/report/mrp_production_templates.xml:208`, `addons/mrp/report/mrp_workorder_templates.xml:3`, `addons/mrp/report/report_stock_rule.xml:3`, `addons/mrp/report/report_deliveryslip.xml:3`, `addons/mrp/report/report_deliveryslip.xml:29`, `addons/mrp/report/report_deliveryslip.xml:67`, `addons/mrp/report/mrp_report_bom_structure.xml:3`, `addons/mrp/report/mrp_report_bom_structure.xml:98`
- View/action field declarations: 259; representative evidence: `addons/mrp/report/mrp_report_views_main.xml:6`, `addons/mrp/report/mrp_report_views_main.xml:15`, `addons/mrp/report/mrp_report_views_main.xml:24`, `addons/mrp/report/mrp_report_views_main.xml:32`, `addons/mrp/report/mrp_report_views_main.xml:42`, `addons/mrp/wizard/mrp_production_serial_numbers.xml:6`, `addons/mrp/wizard/mrp_production_serial_numbers.xml:7`, `addons/mrp/wizard/mrp_production_serial_numbers.xml:43`, `addons/mrp/wizard/mrp_production_serial_numbers.xml:45`, `addons/mrp/wizard/mrp_production_split.xml:7`, `addons/mrp/wizard/mrp_production_split.xml:8`, `addons/mrp/wizard/mrp_production_split.xml:29`
- Browser assets: 52; representative files: `addons/mrp/static/tests/mrp_test_helpers.js`, `addons/mrp/static/tests/mrp_widgets.test.js`, `addons/mrp/static/src/mrp_production_kanban/mrp_production_kanban_view.js`, `addons/mrp/static/src/mrp_production_kanban/mrp_production_kanban_column_progress.js`, `addons/mrp/static/src/mrp_production_kanban/mrp_production_kanban_animated_number.js`, `addons/mrp/static/src/mrp_production_kanban/mrp_production_kanban_header.js`, `addons/mrp/static/src/mrp_production_kanban/mrp_production_kanban_renderer.js`, `addons/mrp/static/src/mrp_forecasted/forecasted_buttons.js`, `addons/mrp/static/src/mrp_forecasted/forecasted_details.js`, `addons/mrp/static/src/allocation_report/allocation_report.js`, `addons/mrp/static/src/widgets/mrp_bom_popover.js`, `addons/mrp/static/src/widgets/mrp_relative_date_unformatted_field.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/mrp/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/mrp/views/stock_move_views.xml`, `addons/mrp/views/mrp_bom_views.xml`, `addons/mrp/views/mrp_production_views.xml`, `addons/mrp/views/mrp_workorder_views.xml`
- **Report entry points:** `addons/mrp/report/mrp_report_views_main.xml`, `addons/mrp/tests/test_stock_report.py`

## 7. Database interactions

- Model declarations: 55
- Representative model evidence: inherits `stock.move.line` (addons/mrp/models/stock_move_line.py:7); inherits `res.groups` (addons/mrp/models/res_groups.py:6); inherits `product.uom` (addons/mrp/models/product_uom.py:4); inherits `res.config.settings` (addons/mrp/models/res_config_settings.py:7); inherits `stock.move` (addons/mrp/models/stock_move.py:9); inherits `stock.quant` (addons/mrp/models/stock_quant.py:5); `mrp.routing.workcenter` (addons/mrp/models/mrp_routing.py:9); inherits `product.template` (addons/mrp/models/product.py:22); inherits `product.product` (addons/mrp/models/product.py:121); `mrp.workcenter` (addons/mrp/models/mrp_workcenter.py:21); `mrp.workcenter.tag` (addons/mrp/models/mrp_workcenter.py:450); `mrp.workcenter.productivity.loss.type` (addons/mrp/models/mrp_workcenter.py:467); `mrp.workcenter.productivity.loss` (addons/mrp/models/mrp_workcenter.py:487); `mrp.workcenter.productivity` (addons/mrp/models/mrp_workcenter.py:514); `mrp.workcenter.capacity` (addons/mrp/models/mrp_workcenter.py:626); inherits `stock.package.history` (addons/mrp/models/stock_package_history.py:4); inherits `stock.warehouse.orderpoint` (addons/mrp/models/stock_orderpoint.py:10); inherits `stock.replenish.mixin` (addons/mrp/models/stock_replenish_mixin.py:6); `mrp.unbuild` (addons/mrp/models/mrp_unbuild.py:11); `mrp.workorder` (addons/mrp/models/mrp_workorder.py:15); inherits `stock.picking.type` (addons/mrp/models/stock_picking.py:10); inherits `stock.picking` (addons/mrp/models/stock_picking.py:140); `mrp.production.group` (addons/mrp/models/mrp_production.py:24); `mrp.production` (addons/mrp/models/mrp_production.py:38); inherits `stock.rule` (addons/mrp/models/stock_rule.py:12); inherits `stock.route` (addons/mrp/models/stock_rule.py:256); `mrp.bom` (addons/mrp/models/mrp_bom.py:13); `mrp.bom.line` (addons/mrp/models/mrp_bom.py:659); `mrp.bom.byproduct` (addons/mrp/models/mrp_bom.py:831); inherits `stock.lot` (addons/mrp/models/stock_lot.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `product`, `stock`, `resource`
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

- `addons/mrp/README.md`
- `addons/mrp/__init__.py`
- `addons/mrp/__manifest__.py`
- `addons/mrp/data/digest_data.xml`
- `addons/mrp/data/mail_message_subtype_data.xml`
- `addons/mrp/data/mail_templates.xml`
- `addons/mrp/data/mrp_data.xml`
- `addons/mrp/data/mrp_demo.xml`
- `addons/mrp/i18n/af.po`
- `addons/mrp/i18n/am.po`
- `addons/mrp/i18n/ar.po`
- `addons/mrp/i18n/az.po`
- `addons/mrp/i18n/bg.po`
- `addons/mrp/i18n/bs.po`
- `addons/mrp/i18n/ca.po`
- `addons/mrp/i18n/cs.po`
- `addons/mrp/i18n/da.po`
- `addons/mrp/i18n/de.po`
- `addons/mrp/i18n/el.po`
- `addons/mrp/i18n/es.po`
- `addons/mrp/i18n/es_419.po`
- `addons/mrp/i18n/es_CL.po`
- `addons/mrp/i18n/et.po`
- `addons/mrp/i18n/eu.po`
- `addons/mrp/i18n/fa.po`
- `addons/mrp/i18n/fi.po`
- `addons/mrp/i18n/fo.po`
- `addons/mrp/i18n/fr.po`
- `addons/mrp/i18n/fr_CA.po`
- `addons/mrp/i18n/gl.po`
- `addons/mrp/i18n/gu.po`
- `addons/mrp/i18n/he.po`
- `addons/mrp/i18n/hi.po`
- `addons/mrp/i18n/hr.po`
- `addons/mrp/i18n/hu.po`
- `addons/mrp/i18n/id.po`
- `addons/mrp/i18n/is.po`
- `addons/mrp/i18n/it.po`
- `addons/mrp/i18n/ja.po`
- `addons/mrp/i18n/ka.po`
- `addons/mrp/i18n/kab.po`
- `addons/mrp/i18n/km.po`
- `addons/mrp/i18n/ko.po`
- `addons/mrp/i18n/ku.po`
- `addons/mrp/i18n/lb.po`
- `addons/mrp/i18n/lo.po`
- `addons/mrp/i18n/lt.po`
- `addons/mrp/i18n/lv.po`
- `addons/mrp/i18n/mk.po`
- `addons/mrp/i18n/mn.po`
- `addons/mrp/i18n/mrp.pot`
- `addons/mrp/i18n/my.po`
- `addons/mrp/i18n/nb.po`
- `addons/mrp/i18n/nl.po`
- `addons/mrp/i18n/pl.po`
- `addons/mrp/i18n/pt.po`
- `addons/mrp/i18n/pt_BR.po`
- `addons/mrp/i18n/ro.po`
- `addons/mrp/i18n/ru.po`
- `addons/mrp/i18n/sk.po`
- `addons/mrp/i18n/sl.po`
- `addons/mrp/i18n/sq.po`
- `addons/mrp/i18n/sr@latin.po`
- `addons/mrp/i18n/sv.po`
- `addons/mrp/i18n/th.po`
- `addons/mrp/i18n/tr.po`
- `addons/mrp/i18n/uk.po`
- `addons/mrp/i18n/uz.po`
- `addons/mrp/i18n/vi.po`
- `addons/mrp/i18n/zh_CN.po`
- `addons/mrp/i18n/zh_TW.po`
- `addons/mrp/models/__init__.py`
- `addons/mrp/models/mrp_bom.py`
- `addons/mrp/models/mrp_production.py`
- `addons/mrp/models/mrp_routing.py`
- `addons/mrp/models/mrp_unbuild.py`
- `addons/mrp/models/mrp_workcenter.py`
- `addons/mrp/models/mrp_workorder.py`
- `addons/mrp/models/product.py`
- `addons/mrp/models/product_uom.py`
- `addons/mrp/models/res_company.py`
- `addons/mrp/models/res_config_settings.py`
- `addons/mrp/models/res_groups.py`
- `addons/mrp/models/stock_lot.py`
- `addons/mrp/models/stock_move.py`
- `addons/mrp/models/stock_move_line.py`
- `addons/mrp/models/stock_orderpoint.py`
- `addons/mrp/models/stock_package.py`
- `addons/mrp/models/stock_package_history.py`
- `addons/mrp/models/stock_picking.py`
- `addons/mrp/models/stock_quant.py`
- `addons/mrp/models/stock_reference.py`
- `addons/mrp/models/stock_replenish_mixin.py`
- `addons/mrp/models/stock_rule.py`
- `addons/mrp/models/stock_warehouse.py`
- `addons/mrp/report/__init__.py`
- `addons/mrp/report/mrp_production_templates.xml`
- `addons/mrp/report/mrp_report_bom_structure.py`
- `addons/mrp/report/mrp_report_bom_structure.xml`
- `addons/mrp/report/mrp_report_mo_overview.py`
- `addons/mrp/report/mrp_report_mo_overview.xml`
- `addons/mrp/report/mrp_report_views_main.xml`
- `addons/mrp/report/mrp_workorder_templates.xml`
- `addons/mrp/report/mrp_zebra_production_templates.xml`
- `addons/mrp/report/report_deliveryslip.xml`
- `addons/mrp/report/report_stock_rule.py`
- `addons/mrp/report/report_stock_rule.xml`
- `addons/mrp/report/stock_allocation_report.py`
- `addons/mrp/report/stock_forecasted.py`
- `addons/mrp/report/stock_traceability.py`
- `addons/mrp/security/ir.access.csv`
- `addons/mrp/security/mrp_security.xml`
- `addons/mrp/static/description/icon.png`
- `addons/mrp/static/description/icon.svg`
- `addons/mrp/static/description/icon_hi.png`
- `addons/mrp/static/img/assebly-worksheet.pdf`
- `addons/mrp/static/img/cutting-worksheet-1.pdf`
- `addons/mrp/static/img/cutting-worksheet-2.pdf`
- `addons/mrp/static/img/cutting-worksheet-3.pdf`
- `addons/mrp/static/img/cutting-worksheet-4.pdf`
- `addons/mrp/static/img/product_product_computer_desk_bolt.png`
- `addons/mrp/static/img/product_product_computer_desk_screw.png`
- `addons/mrp/static/img/product_product_drawer_black.png`
- `addons/mrp/static/img/product_product_drawer_case_black.png`
- `addons/mrp/static/img/product_product_plastic_laminate.png`
- `addons/mrp/static/img/product_product_ply_veneer.png`
- `addons/mrp/static/img/product_product_table_kit.png`
- `addons/mrp/static/img/product_product_wood_panel.png`
- `addons/mrp/static/img/product_product_wood_ply.png`
- `addons/mrp/static/img/product_product_wood_wear.png`
- `addons/mrp/static/img/routing.svg`
- `addons/mrp/static/img/routing_shopfloor.png`
- `addons/mrp/static/img/table.png`
- `addons/mrp/static/img/table_leg.png`
- `addons/mrp/static/img/table_top.png`
- `addons/mrp/static/src/allocation_report/allocation_report.js`
- `addons/mrp/static/src/components/bom_overview/mrp_bom_overview.js`
- `addons/mrp/static/src/components/bom_overview/mrp_bom_overview.xml`
- `addons/mrp/static/src/components/bom_overview_components_block/mrp_bom_overview_components_block.js`
- `addons/mrp/static/src/components/bom_overview_components_block/mrp_bom_overview_components_block.xml`
- `addons/mrp/static/src/components/bom_overview_control_panel/mrp_bom_overview_control_panel.js`
- `addons/mrp/static/src/components/bom_overview_control_panel/mrp_bom_overview_control_panel.xml`
- `addons/mrp/static/src/components/bom_overview_display_filter/mrp_bom_overview_display_filter.js`
- `addons/mrp/static/src/components/bom_overview_display_filter/mrp_bom_overview_display_filter.xml`
- `addons/mrp/static/src/components/bom_overview_extra_block/mrp_bom_overview_extra_block.js`
- `addons/mrp/static/src/components/bom_overview_extra_block/mrp_bom_overview_extra_block.xml`
- `addons/mrp/static/src/components/bom_overview_line/mrp_bom_overview_line.js`
- `addons/mrp/static/src/components/bom_overview_line/mrp_bom_overview_line.xml`
- `addons/mrp/static/src/components/bom_overview_special_line/mrp_bom_overview_special_line.js`
- `addons/mrp/static/src/components/bom_overview_special_line/mrp_bom_overview_special_line.xml`
- `addons/mrp/static/src/components/bom_overview_table/mrp_bom_overview_table.js`
- `addons/mrp/static/src/components/bom_overview_table/mrp_bom_overview_table.xml`
- `addons/mrp/static/src/components/mo_overview/mrp_mo_overview.js`
- `addons/mrp/static/src/components/mo_overview/mrp_mo_overview.xml`
- `addons/mrp/static/src/components/mo_overview_byproducts_block/mrp_mo_overview_byproducts_block.js`
- `addons/mrp/static/src/components/mo_overview_byproducts_block/mrp_mo_overview_byproducts_block.xml`
- `addons/mrp/static/src/components/mo_overview_components_block/mrp_mo_overview_components_block.js`
- `addons/mrp/static/src/components/mo_overview_components_block/mrp_mo_overview_components_block.xml`
- `addons/mrp/static/src/components/mo_overview_display_filter/mrp_mo_overview_display_filter.js`
- `addons/mrp/static/src/components/mo_overview_line/mo_overview_colors.js`
- `addons/mrp/static/src/components/mo_overview_line/mrp_mo_overview_line.js`
- `addons/mrp/static/src/components/mo_overview_line/mrp_mo_overview_line.scss`
- `addons/mrp/static/src/components/mo_overview_line/mrp_mo_overview_line.xml`
- `addons/mrp/static/src/components/mo_overview_operations_block/mrp_mo_overview_operations_block.js`
- `addons/mrp/static/src/components/mo_overview_operations_block/mrp_mo_overview_operations_block.xml`
- `addons/mrp/static/src/components/product_catalog/kanban_controller.js`
- `addons/mrp/static/src/components/wo_list_view_dropdown/wo_list_view_dropdown.js`
- `addons/mrp/static/src/components/wo_list_view_dropdown/wo_list_view_dropdown.scss`
- `addons/mrp/static/src/components/wo_list_view_dropdown/wo_list_view_dropdown.xml`
- `addons/mrp/static/src/img/milk-mrp-tablet.png`
- `addons/mrp/static/src/mrp_forecasted/forecasted_buttons.js`
- `addons/mrp/static/src/mrp_forecasted/forecasted_buttons.xml`
- `addons/mrp/static/src/mrp_forecasted/forecasted_details.js`
- `addons/mrp/static/src/mrp_forecasted/forecasted_details.xml`
- `addons/mrp/static/src/mrp_production_kanban/mrp_production_kanban_animated_number.js`
- `addons/mrp/static/src/mrp_production_kanban/mrp_production_kanban_column_progress.js`
- `addons/mrp/static/src/mrp_production_kanban/mrp_production_kanban_header.js`
- `addons/mrp/static/src/mrp_production_kanban/mrp_production_kanban_renderer.js`
- `addons/mrp/static/src/mrp_production_kanban/mrp_production_kanban_view.js`
- `addons/mrp/static/src/scss/mrp_bom_overview.scss`
- `addons/mrp/static/src/scss/mrp_document_kanban_view.scss`
- `addons/mrp/static/src/scss/mrp_fields.scss`
- `addons/mrp/static/src/scss/mrp_mo_overview.scss`
- `addons/mrp/static/src/scss/mrp_report_bom_structure.scss`
- `addons/mrp/static/src/scss/mrp_report_mo.scss`
- `addons/mrp/static/src/scss/mrp_routing.scss`
- `addons/mrp/static/src/scss/mrp_workorder_kanban.scss`
- `addons/mrp/static/src/views/calendar/common/mrp_calendar_common_renderer.js`
- `addons/mrp/static/src/views/calendar/common/mrp_calendar_common_renderer.xml`
- `addons/mrp/static/src/views/calendar/mrp_calendar_renderer.js`
- `addons/mrp/static/src/views/calendar/mrp_calendar_view.js`
- `addons/mrp/static/src/views/mrp_workorder_kanban/mrp_workorder_kanban_controller.js`
- `addons/mrp/static/src/views/mrp_workorder_kanban/mrp_workorder_kanban_controller.xml`
- `addons/mrp/static/src/views/mrp_workorder_kanban/mrp_workorder_kanban_header.js`
- `addons/mrp/static/src/views/mrp_workorder_kanban/mrp_workorder_kanban_header.xml`
- `addons/mrp/static/src/views/mrp_workorder_kanban/mrp_workorder_kanban_record.js`
- `addons/mrp/static/src/views/mrp_workorder_kanban/mrp_workorder_kanban_renderer.js`
- `addons/mrp/static/src/views/mrp_workorder_kanban/mrp_workorder_kanban_view.js`
- `addons/mrp/static/src/widgets/external_placeholder_float_field.js`
- `addons/mrp/static/src/widgets/external_placeholder_float_field.xml`
- `addons/mrp/static/src/widgets/mrp_bom_popover.js`
- `addons/mrp/static/src/widgets/mrp_bom_popover.xml`
- `addons/mrp/static/src/widgets/mrp_boolean_icon_field.js`
- `addons/mrp/static/src/widgets/mrp_boolean_icon_field.xml`
- `addons/mrp/static/src/widgets/mrp_relative_date_unformatted_field.js`
- `addons/mrp/static/src/widgets/mrp_relative_date_unformatted_field.xml`
- `addons/mrp/static/src/widgets/mrp_should_consume.js`
- `addons/mrp/static/src/widgets/mrp_should_consume.xml`
- `addons/mrp/static/src/widgets/stock_pick_from.js`
- `addons/mrp/static/src/widgets/timer.js`
- `addons/mrp/static/src/widgets/timer.xml`
- `addons/mrp/static/src/widgets/workorder_planning_status.js`
- `addons/mrp/static/src/widgets/workorder_planning_status.xml`
- `addons/mrp/static/src/workcenter_dashboard_graph/workcenter_dashboard_graph_field.js`
- `addons/mrp/static/tests/mock_server/mock_models/res_fake.js`
- `addons/mrp/static/tests/mrp_test_helpers.js`
- `addons/mrp/static/tests/mrp_widgets.test.js`
- `addons/mrp/static/tests/tours/mrp_manual_consumption.js`
- `addons/mrp/static/tests/tours/mrp_manufacture_from_bom.js`
- `addons/mrp/static/tests/tours/mrp_mo_operation_mobile.js`
- `addons/mrp/static/tests/tours/mrp_mo_overview.js`
- `addons/mrp/static/tests/tours/mrp_product_catalog.js`
- `addons/mrp/static/tests/tours/mrp_report.js`
- `addons/mrp/static/tests/tours/mrp_sm_sml_synchronization.js`
- `addons/mrp/static/xls/mrp_bom.xls`
- `addons/mrp/tests/__init__.py`
- `addons/mrp/tests/common.py`
- `addons/mrp/tests/test_backorder.py`
- `addons/mrp/tests/test_bom.py`
- `addons/mrp/tests/test_byproduct.py`
- `addons/mrp/tests/test_cancel_mo.py`
- `addons/mrp/tests/test_consume_component.py`
- `addons/mrp/tests/test_consumption_warning.py`
- `addons/mrp/tests/test_manual_consumption.py`
- `addons/mrp/tests/test_mrp_product_qty.py`
- `addons/mrp/tests/test_mrp_reports.py`
- `addons/mrp/tests/test_multicompany.py`
- `addons/mrp/tests/test_oee.py`
- `addons/mrp/tests/test_order.py`
- `addons/mrp/tests/test_performance.py`
- `addons/mrp/tests/test_procurement.py`
- `addons/mrp/tests/test_quant.py`
- `addons/mrp/tests/test_replenish.py`
- `addons/mrp/tests/test_stock.py`
- `addons/mrp/tests/test_stock_report.py`
- `addons/mrp/tests/test_traceability.py`
- `addons/mrp/tests/test_unbuild.py`
- `addons/mrp/tests/test_warehouse_multistep_manufacturing.py`
- `addons/mrp/tests/test_workcenter.py`
- `addons/mrp/tests/test_workorder.py`
- Additional source files not expanded in this page: 33; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
