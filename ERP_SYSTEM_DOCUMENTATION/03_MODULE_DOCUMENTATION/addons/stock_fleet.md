# Module: stock_fleet

- **Module ID:** MOD-563
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/stock_fleet`
- **Manifest:** `addons/stock_fleet/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `not declared`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Stock Transport Management

**Manifest description:**

Allows organizing deliveries by dock, assigning drivers and vehicles, and printing the associated consignment notes.

**Scope evidence:** The module contains 68 files, including 9 Python, 9 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `stock`, `fleet`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 0
- XML/data/view/template files: 9
- Browser asset files: 0
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 24 methods, 0 constraint handlers, 0 onchange handlers, and 6 dependency declarations.
- **Evidence:** `addons/stock_fleet/models/fleet_vehicle_model.py:7`, `addons/stock_fleet/models/stock_picking_batch.py:8`, `addons/stock_fleet/models/stock_picking.py:9`, `addons/stock_fleet/models/stock_picking.py:34`, `addons/stock_fleet/models/stock_warehouse.py:4`, `addons/stock_fleet/report/report_picking_cmr.py:6`, `addons/stock_fleet/report/report_picking_cmr.py:30`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 9 XML files and 0 JavaScript/TypeScript files; static XML analysis found 29 record/template/menu identifiers.
- **Evidence:** `addons/stock_fleet/report/stock_fleet_reports.xml:4`, `addons/stock_fleet/report/stock_fleet_reports.xml:15`, `addons/stock_fleet/report/stock_fleet_reports.xml:27`, `addons/stock_fleet/report/report_picking_cmr.xml:5`, `addons/stock_fleet/report/report_picking_cmr.xml:14`, `addons/stock_fleet/report/report_picking_cmr.xml:40`, `addons/stock_fleet/report/report_picking_cmr.xml:97`, `addons/stock_fleet/report/report_picking_cmr.xml:181`, `addons/stock_fleet/report/report_picking_batch.xml:2`, `addons/stock_fleet/report/report_picking_batch.xml:27`, `addons/stock_fleet/data/stock_fleet_demo.xml:3`, `addons/stock_fleet/data/stock_fleet_demo.xml:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/stock_fleet/report/stock_fleet_reports.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 9; representative identifiers: `paperformat_cmr`, `action_report_cmr`, `action_report_cmr_batch`, `report_cmr`, `report_cmr_picking_copies`, `report_cmr_translated_label`, `report_cmr_goods_table`, `report_cmr_document`, `report_picking_batch_inherit`, `report_cmr_batch`, `vehicle_tag_transport`, `model_category_truck`, `model_category_van`, `model_volvo_fm`, `model_ford_transit`, `vehicle_truck_volvo`, `stock_location_form_stock_fleet`, `stock_picking_type_kanban_inherit_stock_fleet`, `view_picking_type_form`, `stock_picking_batch_pivot`
- Menus: 0; representative evidence: Not found in module
- Templates: 7; representative evidence: `addons/stock_fleet/report/report_picking_cmr.xml:5`, `addons/stock_fleet/report/report_picking_cmr.xml:14`, `addons/stock_fleet/report/report_picking_cmr.xml:40`, `addons/stock_fleet/report/report_picking_cmr.xml:97`, `addons/stock_fleet/report/report_picking_cmr.xml:181`, `addons/stock_fleet/report/report_picking_batch.xml:2`, `addons/stock_fleet/report/report_picking_batch.xml:27`
- View/action field declarations: 28; representative evidence: `addons/stock_fleet/report/stock_fleet_reports.xml:17`, `addons/stock_fleet/report/stock_fleet_reports.xml:29`, `addons/stock_fleet/views/stock_location.xml:5`, `addons/stock_fleet/views/stock_location.xml:7`, `addons/stock_fleet/views/stock_picking_type.xml:6`, `addons/stock_fleet/views/stock_picking_type.xml:8`, `addons/stock_fleet/views/stock_picking_type.xml:44`, `addons/stock_fleet/views/stock_picking_type.xml:46`, `addons/stock_fleet/views/stock_picking_batch.xml:4`, `addons/stock_fleet/views/stock_picking_batch.xml:5`, `addons/stock_fleet/views/stock_picking_batch.xml:15`, `addons/stock_fleet/views/stock_picking_batch.xml:16`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/stock_fleet/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/stock_fleet/report/stock_fleet_reports.xml`

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: inherits `fleet.vehicle.model.category` (addons/stock_fleet/models/fleet_vehicle_model.py:7); inherits `stock.picking.batch` (addons/stock_fleet/models/stock_picking_batch.py:8); inherits `stock.picking.type` (addons/stock_fleet/models/stock_picking.py:9); inherits `stock.picking` (addons/stock_fleet/models/stock_picking.py:34); inherits `stock.warehouse` (addons/stock_fleet/models/stock_warehouse.py:4); `report.stock_fleet.report_cmr_batch` (addons/stock_fleet/report/report_picking_cmr.py:6); `report.stock_fleet.report_cmr` (addons/stock_fleet/report/report_picking_cmr.py:30)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `stock`, `fleet`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/stock_fleet/__init__.py`
- `addons/stock_fleet/__manifest__.py`
- `addons/stock_fleet/data/stock_fleet_demo.xml`
- `addons/stock_fleet/i18n/ar.po`
- `addons/stock_fleet/i18n/az.po`
- `addons/stock_fleet/i18n/bg.po`
- `addons/stock_fleet/i18n/bs.po`
- `addons/stock_fleet/i18n/ca.po`
- `addons/stock_fleet/i18n/cs.po`
- `addons/stock_fleet/i18n/da.po`
- `addons/stock_fleet/i18n/de.po`
- `addons/stock_fleet/i18n/el.po`
- `addons/stock_fleet/i18n/es.po`
- `addons/stock_fleet/i18n/es_419.po`
- `addons/stock_fleet/i18n/et.po`
- `addons/stock_fleet/i18n/fa.po`
- `addons/stock_fleet/i18n/fi.po`
- `addons/stock_fleet/i18n/fr.po`
- `addons/stock_fleet/i18n/he.po`
- `addons/stock_fleet/i18n/hi.po`
- `addons/stock_fleet/i18n/hr.po`
- `addons/stock_fleet/i18n/hu.po`
- `addons/stock_fleet/i18n/id.po`
- `addons/stock_fleet/i18n/it.po`
- `addons/stock_fleet/i18n/ja.po`
- `addons/stock_fleet/i18n/kab.po`
- `addons/stock_fleet/i18n/ko.po`
- `addons/stock_fleet/i18n/ku.po`
- `addons/stock_fleet/i18n/lo.po`
- `addons/stock_fleet/i18n/lt.po`
- `addons/stock_fleet/i18n/lv.po`
- `addons/stock_fleet/i18n/mn.po`
- `addons/stock_fleet/i18n/my.po`
- `addons/stock_fleet/i18n/nb.po`
- `addons/stock_fleet/i18n/nl.po`
- `addons/stock_fleet/i18n/pl.po`
- `addons/stock_fleet/i18n/pt.po`
- `addons/stock_fleet/i18n/pt_BR.po`
- `addons/stock_fleet/i18n/ro.po`
- `addons/stock_fleet/i18n/ru.po`
- `addons/stock_fleet/i18n/sk.po`
- `addons/stock_fleet/i18n/sl.po`
- `addons/stock_fleet/i18n/sr@latin.po`
- `addons/stock_fleet/i18n/stock_fleet.pot`
- `addons/stock_fleet/i18n/sv.po`
- `addons/stock_fleet/i18n/th.po`
- `addons/stock_fleet/i18n/tr.po`
- `addons/stock_fleet/i18n/uk.po`
- `addons/stock_fleet/i18n/uz.po`
- `addons/stock_fleet/i18n/vi.po`
- `addons/stock_fleet/i18n/zh_CN.po`
- `addons/stock_fleet/i18n/zh_TW.po`
- `addons/stock_fleet/models/__init__.py`
- `addons/stock_fleet/models/fleet_vehicle_model.py`
- `addons/stock_fleet/models/stock_picking.py`
- `addons/stock_fleet/models/stock_picking_batch.py`
- `addons/stock_fleet/models/stock_warehouse.py`
- `addons/stock_fleet/report/__init__.py`
- `addons/stock_fleet/report/report_picking_batch.xml`
- `addons/stock_fleet/report/report_picking_cmr.py`
- `addons/stock_fleet/report/report_picking_cmr.xml`
- `addons/stock_fleet/report/stock_fleet_reports.xml`
- `addons/stock_fleet/static/src/scss/report_picking_cmr.scss`
- `addons/stock_fleet/views/fleet_vehicle_model.xml`
- `addons/stock_fleet/views/stock_location.xml`
- `addons/stock_fleet/views/stock_picking_batch.xml`
- `addons/stock_fleet/views/stock_picking_type.xml`
- `addons/stock_fleet/views/stock_picking_view.xml`
