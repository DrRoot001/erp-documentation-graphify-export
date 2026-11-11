# Module: hr_maintenance

- **Module ID:** MOD-092
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_maintenance`
- **Manifest:** `addons/hr_maintenance/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Equipment, Assets, Internal Hardware, Allocation Tracking

**Manifest description:**

Bridge between HR and Maintenance.

**Scope evidence:** The module contains 65 files, including 9 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `hr`, `maintenance`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 3
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr_maintenance/security/equipment.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 16 methods, 0 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/hr_maintenance/models/hr_employee_departure.py:6`, `addons/hr_maintenance/models/equipment.py:7`, `addons/hr_maintenance/models/equipment.py:95`, `addons/hr_maintenance/models/hr_employee_public.py:6`, `addons/hr_maintenance/models/hr_employee.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 12 record/template/menu identifiers.
- **Evidence:** `addons/hr_maintenance/security/equipment.xml:4`, `addons/hr_maintenance/views/hr_views.xml:4`, `addons/hr_maintenance/views/hr_views.xml:10`, `addons/hr_maintenance/views/hr_views.xml:29`, `addons/hr_maintenance/views/maintenance_views.xml:5`, `addons/hr_maintenance/views/maintenance_views.xml:22`, `addons/hr_maintenance/views/maintenance_views.xml:35`, `addons/hr_maintenance/views/maintenance_views.xml:46`, `addons/hr_maintenance/views/maintenance_views.xml:58`, `addons/hr_maintenance/views/maintenance_views.xml:74`, `addons/hr_maintenance/views/maintenance_views.xml:94`, `addons/hr_maintenance/views/maintenance_views.xml:115`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/hr_maintenance/security/equipment.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/hr_maintenance/tests/__init__.py`, `addons/hr_maintenance/tests/test_employee_departure_maintenance.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `hr.group_hr_user`, `equipment_action`, `hr_employee_view_form`, `hr_employee_public_view_form`, `maintenance_request_view_search_inherit_hr`, `maintenance_request_view_form_inherit_hr`, `maintenance_request_view_card_inherit_hr`, `maintenance_request_view_tree_inherit_hr`, `maintenance_equipment_view_search_inherit_hr`, `maintenance_equipment_view_form_inherit_hr`, `maintenance_equipment_view_kanban_inherit_hr`, `maintenance_equipment_view_tree_inherit_hr`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 22; representative evidence: `addons/hr_maintenance/views/hr_views.xml:6`, `addons/hr_maintenance/views/hr_views.xml:7`, `addons/hr_maintenance/views/hr_views.xml:12`, `addons/hr_maintenance/views/hr_views.xml:15`, `addons/hr_maintenance/views/hr_views.xml:31`, `addons/hr_maintenance/views/hr_views.xml:33`, `addons/hr_maintenance/views/maintenance_views.xml:7`, `addons/hr_maintenance/views/maintenance_views.xml:9`, `addons/hr_maintenance/views/maintenance_views.xml:24`, `addons/hr_maintenance/views/maintenance_views.xml:26`, `addons/hr_maintenance/views/maintenance_views.xml:37`, `addons/hr_maintenance/views/maintenance_views.xml:39`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_maintenance/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `hr.employee.departure` (addons/hr_maintenance/models/hr_employee_departure.py:6); inherits `maintenance.equipment` (addons/hr_maintenance/models/equipment.py:7); inherits `maintenance.request` (addons/hr_maintenance/models/equipment.py:95); inherits `hr.employee.public` (addons/hr_maintenance/models/hr_employee_public.py:6); inherits `hr.employee` (addons/hr_maintenance/models/hr_employee.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr`, `maintenance`
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

- `addons/hr_maintenance/__init__.py`
- `addons/hr_maintenance/__manifest__.py`
- `addons/hr_maintenance/i18n/af.po`
- `addons/hr_maintenance/i18n/ar.po`
- `addons/hr_maintenance/i18n/az.po`
- `addons/hr_maintenance/i18n/bg.po`
- `addons/hr_maintenance/i18n/bs.po`
- `addons/hr_maintenance/i18n/ca.po`
- `addons/hr_maintenance/i18n/cs.po`
- `addons/hr_maintenance/i18n/da.po`
- `addons/hr_maintenance/i18n/de.po`
- `addons/hr_maintenance/i18n/el.po`
- `addons/hr_maintenance/i18n/es.po`
- `addons/hr_maintenance/i18n/es_419.po`
- `addons/hr_maintenance/i18n/et.po`
- `addons/hr_maintenance/i18n/fa.po`
- `addons/hr_maintenance/i18n/fi.po`
- `addons/hr_maintenance/i18n/fr.po`
- `addons/hr_maintenance/i18n/gu.po`
- `addons/hr_maintenance/i18n/he.po`
- `addons/hr_maintenance/i18n/hi.po`
- `addons/hr_maintenance/i18n/hr.po`
- `addons/hr_maintenance/i18n/hr_maintenance.pot`
- `addons/hr_maintenance/i18n/hu.po`
- `addons/hr_maintenance/i18n/id.po`
- `addons/hr_maintenance/i18n/is.po`
- `addons/hr_maintenance/i18n/it.po`
- `addons/hr_maintenance/i18n/ja.po`
- `addons/hr_maintenance/i18n/kab.po`
- `addons/hr_maintenance/i18n/km.po`
- `addons/hr_maintenance/i18n/ko.po`
- `addons/hr_maintenance/i18n/ku.po`
- `addons/hr_maintenance/i18n/lo.po`
- `addons/hr_maintenance/i18n/lt.po`
- `addons/hr_maintenance/i18n/lv.po`
- `addons/hr_maintenance/i18n/mn.po`
- `addons/hr_maintenance/i18n/my.po`
- `addons/hr_maintenance/i18n/nb.po`
- `addons/hr_maintenance/i18n/nl.po`
- `addons/hr_maintenance/i18n/pl.po`
- `addons/hr_maintenance/i18n/pt.po`
- `addons/hr_maintenance/i18n/pt_BR.po`
- `addons/hr_maintenance/i18n/ro.po`
- `addons/hr_maintenance/i18n/ru.po`
- `addons/hr_maintenance/i18n/sk.po`
- `addons/hr_maintenance/i18n/sl.po`
- `addons/hr_maintenance/i18n/sr@latin.po`
- `addons/hr_maintenance/i18n/sv.po`
- `addons/hr_maintenance/i18n/th.po`
- `addons/hr_maintenance/i18n/tr.po`
- `addons/hr_maintenance/i18n/uk.po`
- `addons/hr_maintenance/i18n/uz.po`
- `addons/hr_maintenance/i18n/vi.po`
- `addons/hr_maintenance/i18n/zh_CN.po`
- `addons/hr_maintenance/i18n/zh_TW.po`
- `addons/hr_maintenance/models/__init__.py`
- `addons/hr_maintenance/models/equipment.py`
- `addons/hr_maintenance/models/hr_employee.py`
- `addons/hr_maintenance/models/hr_employee_departure.py`
- `addons/hr_maintenance/models/hr_employee_public.py`
- `addons/hr_maintenance/security/equipment.xml`
- `addons/hr_maintenance/tests/__init__.py`
- `addons/hr_maintenance/tests/test_employee_departure_maintenance.py`
- `addons/hr_maintenance/views/hr_views.xml`
- `addons/hr_maintenance/views/maintenance_views.xml`
