# Module: hr_fleet

- **Module ID:** MOD-087
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_fleet`
- **Manifest:** `addons/hr_fleet/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Get history of driven cars by employees

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 70 files, including 13 Python, 5 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `hr`, `fleet`.

## 2. Module structure

- Model/business logic files: 9
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 2
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr_fleet/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 9 model declarations, 35 methods, 2 constraint handlers, 0 onchange handlers, and 6 dependency declarations.
- **Evidence:** `addons/hr_fleet/models/hr_employee_departure.py:6`, `addons/hr_fleet/models/fleet_vehicle_log_services.py:7`, `addons/hr_fleet/models/fleet_vehicle_assignation_log.py:8`, `addons/hr_fleet/models/fleet_vehicle_odometer.py:7`, `addons/hr_fleet/models/fleet_vehicle_log_contract.py:7`, `addons/hr_fleet/models/hr_employee.py:8`, `addons/hr_fleet/models/hr_employee.py:96`, `addons/hr_fleet/models/fleet_vehicle.py:7`, `addons/hr_fleet/models/ir_attachment.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 2 JavaScript/TypeScript files; static XML analysis found 20 record/template/menu identifiers.
- **Evidence:** `addons/hr_fleet/data/hr_fleet_demo.xml:3`, `addons/hr_fleet/data/hr_fleet_demo.xml:20`, `addons/hr_fleet/data/hr_fleet_demo.xml:28`, `addons/hr_fleet/data/hr_fleet_demo.xml:36`, `addons/hr_fleet/data/hr_fleet_demo.xml:44`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:3`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:24`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:35`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:47`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:58`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:69`, `addons/hr_fleet/views/fleet_vehicle_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/hr_fleet/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/hr_fleet/tests/test_hr_fleet_driver.py`, `addons/hr_fleet/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `fleet.vehicle_1`, `fleet.vehicle_2`, `fleet.vehicle_3`, `fleet.vehicle_4`, `fleet.vehicle_5`, `fleet_vehicle_log_contract_view_form_inherit_hr`, `fleet_vehicle_log_contract_view_tree_inherit_hr`, `fleet_vehicle_log_contract_view_search_inherit_hr`, `fleet_vehicle_log_services_view_form_inherit_hr`, `fleet_vehicle_log_services_view_tree_inherit_hr`, `fleet_vehicle_log_services_view_kanban_inherit_hr`, `fleet_vehicle_odometer_view_tree`, `fleet_vehicle_assignation_log_view_list`, `fleet_vehicle_assignation_log_employee_view_list`, `fleet_vehicle_view_form_inherit_hr`, `fleet_vehicle_view_search_inherit_hr`, `fleet_vehicle_view_tree_inherit_hr`, `view_attachment_kanban_inherit_hr`, `view_employee_form`, `hr_employee_public_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 30; representative evidence: `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:5`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:7`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:26`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:28`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:37`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:39`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:49`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:51`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:60`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:62`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:71`, `addons/hr_fleet/views/fleet_vehicle_cost_views.xml:73`
- Browser assets: 2; representative files: `addons/hr_fleet/static/src/views/hr_fleet_kanban/hr_fleet_kanban_view.js`, `addons/hr_fleet/static/src/views/hr_fleet_kanban/hr_fleet_kanban_controller.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_fleet/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 9
- Representative model evidence: inherits `hr.employee.departure` (addons/hr_fleet/models/hr_employee_departure.py:6); inherits `fleet.vehicle.log.services` (addons/hr_fleet/models/fleet_vehicle_log_services.py:7); inherits `fleet.vehicle.assignation.log` (addons/hr_fleet/models/fleet_vehicle_assignation_log.py:8); inherits `fleet.vehicle.odometer` (addons/hr_fleet/models/fleet_vehicle_odometer.py:7); inherits `fleet.vehicle.log.contract` (addons/hr_fleet/models/fleet_vehicle_log_contract.py:7); inherits `hr.employee` (addons/hr_fleet/models/hr_employee.py:8); inherits `hr.employee.public` (addons/hr_fleet/models/hr_employee.py:96); inherits `fleet.vehicle` (addons/hr_fleet/models/fleet_vehicle.py:7); inherits `ir.attachment` (addons/hr_fleet/models/ir_attachment.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr`, `fleet`
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

- `addons/hr_fleet/__init__.py`
- `addons/hr_fleet/__manifest__.py`
- `addons/hr_fleet/data/hr_fleet_demo.xml`
- `addons/hr_fleet/i18n/ar.po`
- `addons/hr_fleet/i18n/az.po`
- `addons/hr_fleet/i18n/bg.po`
- `addons/hr_fleet/i18n/bs.po`
- `addons/hr_fleet/i18n/ca.po`
- `addons/hr_fleet/i18n/cs.po`
- `addons/hr_fleet/i18n/da.po`
- `addons/hr_fleet/i18n/de.po`
- `addons/hr_fleet/i18n/el.po`
- `addons/hr_fleet/i18n/es.po`
- `addons/hr_fleet/i18n/es_419.po`
- `addons/hr_fleet/i18n/et.po`
- `addons/hr_fleet/i18n/fa.po`
- `addons/hr_fleet/i18n/fi.po`
- `addons/hr_fleet/i18n/fr.po`
- `addons/hr_fleet/i18n/he.po`
- `addons/hr_fleet/i18n/hi.po`
- `addons/hr_fleet/i18n/hr.po`
- `addons/hr_fleet/i18n/hr_fleet.pot`
- `addons/hr_fleet/i18n/hu.po`
- `addons/hr_fleet/i18n/id.po`
- `addons/hr_fleet/i18n/it.po`
- `addons/hr_fleet/i18n/ja.po`
- `addons/hr_fleet/i18n/kab.po`
- `addons/hr_fleet/i18n/ko.po`
- `addons/hr_fleet/i18n/ku.po`
- `addons/hr_fleet/i18n/lo.po`
- `addons/hr_fleet/i18n/lt.po`
- `addons/hr_fleet/i18n/lv.po`
- `addons/hr_fleet/i18n/mn.po`
- `addons/hr_fleet/i18n/my.po`
- `addons/hr_fleet/i18n/nb.po`
- `addons/hr_fleet/i18n/nl.po`
- `addons/hr_fleet/i18n/pl.po`
- `addons/hr_fleet/i18n/pt.po`
- `addons/hr_fleet/i18n/pt_BR.po`
- `addons/hr_fleet/i18n/ro.po`
- `addons/hr_fleet/i18n/ru.po`
- `addons/hr_fleet/i18n/sk.po`
- `addons/hr_fleet/i18n/sl.po`
- `addons/hr_fleet/i18n/sr@latin.po`
- `addons/hr_fleet/i18n/sv.po`
- `addons/hr_fleet/i18n/th.po`
- `addons/hr_fleet/i18n/tr.po`
- `addons/hr_fleet/i18n/uk.po`
- `addons/hr_fleet/i18n/uz.po`
- `addons/hr_fleet/i18n/vi.po`
- `addons/hr_fleet/i18n/zh_CN.po`
- `addons/hr_fleet/i18n/zh_TW.po`
- `addons/hr_fleet/models/__init__.py`
- `addons/hr_fleet/models/fleet_vehicle.py`
- `addons/hr_fleet/models/fleet_vehicle_assignation_log.py`
- `addons/hr_fleet/models/fleet_vehicle_log_contract.py`
- `addons/hr_fleet/models/fleet_vehicle_log_services.py`
- `addons/hr_fleet/models/fleet_vehicle_odometer.py`
- `addons/hr_fleet/models/hr_employee.py`
- `addons/hr_fleet/models/hr_employee_departure.py`
- `addons/hr_fleet/models/ir_attachment.py`
- `addons/hr_fleet/security/ir.access.csv`
- `addons/hr_fleet/static/src/views/hr_fleet_kanban/hr_fleet_kanban_controller.js`
- `addons/hr_fleet/static/src/views/hr_fleet_kanban/hr_fleet_kanban_controller.xml`
- `addons/hr_fleet/static/src/views/hr_fleet_kanban/hr_fleet_kanban_view.js`
- `addons/hr_fleet/tests/__init__.py`
- `addons/hr_fleet/tests/test_hr_fleet_driver.py`
- `addons/hr_fleet/views/fleet_vehicle_cost_views.xml`
- `addons/hr_fleet/views/fleet_vehicle_views.xml`
- `addons/hr_fleet/views/hr_employee_views.xml`
