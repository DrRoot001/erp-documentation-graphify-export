# Module: fleet_maintenance

- **Module ID:** MOD-073
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/fleet_maintenance`
- **Manifest:** `addons/fleet_maintenance/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Integrates Fleet and Maintenance

**Manifest description:**

Bridge between Fleet and Maintenance.

**Scope evidence:** The module contains 57 files, including 5 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `fleet`, `maintenance`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 3
- Browser asset files: 0
- Security files: 1
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/fleet_maintenance/security/fleet_maintenance_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 6 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/fleet_maintenance/models/maintenance_equipment.py:7`, `addons/fleet_maintenance/models/fleet_vehicle.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/fleet_maintenance/security/fleet_maintenance_security.xml:4`, `addons/fleet_maintenance/views/fleet_vehicle_views.xml:3`, `addons/fleet_maintenance/views/maintenance_equipment_views.xml:3`, `addons/fleet_maintenance/views/maintenance_equipment_views.xml:21`, `addons/fleet_maintenance/views/maintenance_equipment_views.xml:35`, `addons/fleet_maintenance/views/maintenance_equipment_views.xml:52`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/fleet_maintenance/security/fleet_maintenance_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `fleet.fleet_group_user`, `fleet_vehicle_view_form`, `maintenance_equipment_view_form_inherit_fleet`, `maintenance_equipment_view_search_inherit_fleet`, `maintenance_equipment_view_kanban_inherit_fleet`, `maintenance_equipment_view_tree_inherit_fleet`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 10; representative evidence: `addons/fleet_maintenance/views/fleet_vehicle_views.xml:5`, `addons/fleet_maintenance/views/fleet_vehicle_views.xml:7`, `addons/fleet_maintenance/views/maintenance_equipment_views.xml:5`, `addons/fleet_maintenance/views/maintenance_equipment_views.xml:7`, `addons/fleet_maintenance/views/maintenance_equipment_views.xml:23`, `addons/fleet_maintenance/views/maintenance_equipment_views.xml:25`, `addons/fleet_maintenance/views/maintenance_equipment_views.xml:37`, `addons/fleet_maintenance/views/maintenance_equipment_views.xml:39`, `addons/fleet_maintenance/views/maintenance_equipment_views.xml:54`, `addons/fleet_maintenance/views/maintenance_equipment_views.xml:56`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/fleet_maintenance/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `maintenance.equipment` (addons/fleet_maintenance/models/maintenance_equipment.py:7); inherits `fleet.vehicle` (addons/fleet_maintenance/models/fleet_vehicle.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `fleet`, `maintenance`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Present
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/fleet_maintenance/__init__.py`
- `addons/fleet_maintenance/__manifest__.py`
- `addons/fleet_maintenance/i18n/ar.po`
- `addons/fleet_maintenance/i18n/az.po`
- `addons/fleet_maintenance/i18n/bg.po`
- `addons/fleet_maintenance/i18n/bs.po`
- `addons/fleet_maintenance/i18n/ca.po`
- `addons/fleet_maintenance/i18n/cs.po`
- `addons/fleet_maintenance/i18n/da.po`
- `addons/fleet_maintenance/i18n/de.po`
- `addons/fleet_maintenance/i18n/el.po`
- `addons/fleet_maintenance/i18n/es.po`
- `addons/fleet_maintenance/i18n/es_419.po`
- `addons/fleet_maintenance/i18n/et.po`
- `addons/fleet_maintenance/i18n/fa.po`
- `addons/fleet_maintenance/i18n/fi.po`
- `addons/fleet_maintenance/i18n/fleet_maintenance.pot`
- `addons/fleet_maintenance/i18n/fr.po`
- `addons/fleet_maintenance/i18n/he.po`
- `addons/fleet_maintenance/i18n/hi.po`
- `addons/fleet_maintenance/i18n/hr.po`
- `addons/fleet_maintenance/i18n/hu.po`
- `addons/fleet_maintenance/i18n/id.po`
- `addons/fleet_maintenance/i18n/it.po`
- `addons/fleet_maintenance/i18n/ja.po`
- `addons/fleet_maintenance/i18n/kab.po`
- `addons/fleet_maintenance/i18n/ko.po`
- `addons/fleet_maintenance/i18n/ku.po`
- `addons/fleet_maintenance/i18n/lo.po`
- `addons/fleet_maintenance/i18n/lt.po`
- `addons/fleet_maintenance/i18n/lv.po`
- `addons/fleet_maintenance/i18n/mn.po`
- `addons/fleet_maintenance/i18n/my.po`
- `addons/fleet_maintenance/i18n/nb.po`
- `addons/fleet_maintenance/i18n/nl.po`
- `addons/fleet_maintenance/i18n/pl.po`
- `addons/fleet_maintenance/i18n/pt.po`
- `addons/fleet_maintenance/i18n/pt_BR.po`
- `addons/fleet_maintenance/i18n/ro.po`
- `addons/fleet_maintenance/i18n/ru.po`
- `addons/fleet_maintenance/i18n/sk.po`
- `addons/fleet_maintenance/i18n/sl.po`
- `addons/fleet_maintenance/i18n/sr@latin.po`
- `addons/fleet_maintenance/i18n/sv.po`
- `addons/fleet_maintenance/i18n/th.po`
- `addons/fleet_maintenance/i18n/tr.po`
- `addons/fleet_maintenance/i18n/uk.po`
- `addons/fleet_maintenance/i18n/uz.po`
- `addons/fleet_maintenance/i18n/vi.po`
- `addons/fleet_maintenance/i18n/zh_CN.po`
- `addons/fleet_maintenance/i18n/zh_TW.po`
- `addons/fleet_maintenance/models/__init__.py`
- `addons/fleet_maintenance/models/fleet_vehicle.py`
- `addons/fleet_maintenance/models/maintenance_equipment.py`
- `addons/fleet_maintenance/security/fleet_maintenance_security.xml`
- `addons/fleet_maintenance/views/fleet_vehicle_views.xml`
- `addons/fleet_maintenance/views/maintenance_equipment_views.xml`
