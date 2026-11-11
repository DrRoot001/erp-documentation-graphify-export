# Module: stock_maintenance

- **Module ID:** MOD-565
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/stock_maintenance`
- **Manifest:** `addons/stock_maintenance/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Inventory`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** See lots used in maintenance

**Manifest description:**

Stock in Maintenance
====================
Open the record of the serial number from an equipment form

**Scope evidence:** The module contains 56 files, including 5 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `stock`, `maintenance`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 4 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/stock_maintenance/models/stock_location.py:4`, `addons/stock_maintenance/models/maintenance.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/stock_maintenance/views/stock_location.xml:3`, `addons/stock_maintenance/views/maintenance_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `stock_location_form_maintenance_equipments`, `maintenance_stock_equipment_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/stock_maintenance/views/stock_location.xml:5`, `addons/stock_maintenance/views/stock_location.xml:7`, `addons/stock_maintenance/views/maintenance_views.xml:6`, `addons/stock_maintenance/views/maintenance_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/stock_maintenance/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `stock.location` (addons/stock_maintenance/models/stock_location.py:4); inherits `maintenance.equipment` (addons/stock_maintenance/models/maintenance.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `stock`, `maintenance`
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

- `addons/stock_maintenance/__init__.py`
- `addons/stock_maintenance/__manifest__.py`
- `addons/stock_maintenance/i18n/ar.po`
- `addons/stock_maintenance/i18n/az.po`
- `addons/stock_maintenance/i18n/bg.po`
- `addons/stock_maintenance/i18n/bs.po`
- `addons/stock_maintenance/i18n/ca.po`
- `addons/stock_maintenance/i18n/cs.po`
- `addons/stock_maintenance/i18n/da.po`
- `addons/stock_maintenance/i18n/de.po`
- `addons/stock_maintenance/i18n/el.po`
- `addons/stock_maintenance/i18n/es.po`
- `addons/stock_maintenance/i18n/es_419.po`
- `addons/stock_maintenance/i18n/et.po`
- `addons/stock_maintenance/i18n/fa.po`
- `addons/stock_maintenance/i18n/fi.po`
- `addons/stock_maintenance/i18n/fr.po`
- `addons/stock_maintenance/i18n/he.po`
- `addons/stock_maintenance/i18n/hi.po`
- `addons/stock_maintenance/i18n/hr.po`
- `addons/stock_maintenance/i18n/hu.po`
- `addons/stock_maintenance/i18n/id.po`
- `addons/stock_maintenance/i18n/it.po`
- `addons/stock_maintenance/i18n/ja.po`
- `addons/stock_maintenance/i18n/kab.po`
- `addons/stock_maintenance/i18n/ko.po`
- `addons/stock_maintenance/i18n/ku.po`
- `addons/stock_maintenance/i18n/lo.po`
- `addons/stock_maintenance/i18n/lt.po`
- `addons/stock_maintenance/i18n/lv.po`
- `addons/stock_maintenance/i18n/mn.po`
- `addons/stock_maintenance/i18n/my.po`
- `addons/stock_maintenance/i18n/nb.po`
- `addons/stock_maintenance/i18n/nl.po`
- `addons/stock_maintenance/i18n/pl.po`
- `addons/stock_maintenance/i18n/pt.po`
- `addons/stock_maintenance/i18n/pt_BR.po`
- `addons/stock_maintenance/i18n/ro.po`
- `addons/stock_maintenance/i18n/ru.po`
- `addons/stock_maintenance/i18n/sk.po`
- `addons/stock_maintenance/i18n/sl.po`
- `addons/stock_maintenance/i18n/sr@latin.po`
- `addons/stock_maintenance/i18n/stock_maintenance.pot`
- `addons/stock_maintenance/i18n/sv.po`
- `addons/stock_maintenance/i18n/th.po`
- `addons/stock_maintenance/i18n/tr.po`
- `addons/stock_maintenance/i18n/uk.po`
- `addons/stock_maintenance/i18n/uz.po`
- `addons/stock_maintenance/i18n/vi.po`
- `addons/stock_maintenance/i18n/zh_CN.po`
- `addons/stock_maintenance/i18n/zh_TW.po`
- `addons/stock_maintenance/models/__init__.py`
- `addons/stock_maintenance/models/maintenance.py`
- `addons/stock_maintenance/models/stock_location.py`
- `addons/stock_maintenance/views/maintenance_views.xml`
- `addons/stock_maintenance/views/stock_location.xml`
