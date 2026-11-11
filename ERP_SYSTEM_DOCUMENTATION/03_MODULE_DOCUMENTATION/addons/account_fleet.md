# Module: account_fleet

- **Module ID:** MOD-007
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/account_fleet`
- **Manifest:** `addons/account_fleet/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Manage accounting with fleets

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 69 files, including 14 Python, 6 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `fleet`, `account`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 0
- Security files: 0
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 34 methods, 0 constraint handlers, 1 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/account_fleet/models/fleet_vehicle_log_services.py:7`, `addons/account_fleet/models/account_tax.py:4`, `addons/account_fleet/models/account_account.py:4`, `addons/account_fleet/models/account_move.py:7`, `addons/account_fleet/models/account_move.py:52`, `addons/account_fleet/models/fleet_vehicle.py:7`, `addons/account_fleet/wizard/account_automatic_entry_wizard.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 0 JavaScript/TypeScript files; static XML analysis found 8 record/template/menu identifiers.
- **Evidence:** `addons/account_fleet/data/fleet_service_type_data.xml:3`, `addons/account_fleet/views/fleet_vehicle_views.xml:3`, `addons/account_fleet/views/report_invoice.xml:4`, `addons/account_fleet/views/account_move_views.xml:4`, `addons/account_fleet/views/account_move_views.xml:29`, `addons/account_fleet/views/account_move_views.xml:44`, `addons/account_fleet/views/account_account_views.xml:3`, `addons/account_fleet/views/fleet_vehicle_log_services_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/account_fleet/tests/test_account_fleet_tax_report.py`, `addons/account_fleet/tests/test_account_fleet.py`, `addons/account_fleet/tests/__init__.py`, `addons/account_fleet/tests/test_fleet_vehicle_log_services.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `data_fleet_service_type_vendor_bill`, `fleet_vehicle_view_form`, `report_invoice_document`, `view_move_form`, `account_move_view_tree`, `view_move_line_tree_fleet`, `view_account_form_fleet_inherit`, `fleet_vehicle_log_services_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/account_fleet/views/report_invoice.xml:4`
- View/action field declarations: 12; representative evidence: `addons/account_fleet/views/fleet_vehicle_views.xml:5`, `addons/account_fleet/views/fleet_vehicle_views.xml:7`, `addons/account_fleet/views/account_move_views.xml:6`, `addons/account_fleet/views/account_move_views.xml:8`, `addons/account_fleet/views/account_move_views.xml:31`, `addons/account_fleet/views/account_move_views.xml:34`, `addons/account_fleet/views/account_move_views.xml:46`, `addons/account_fleet/views/account_move_views.xml:48`, `addons/account_fleet/views/account_account_views.xml:5`, `addons/account_fleet/views/account_account_views.xml:7`, `addons/account_fleet/views/fleet_vehicle_log_services_views.xml:5`, `addons/account_fleet/views/fleet_vehicle_log_services_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/account_fleet/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: inherits `fleet.vehicle.log.services` (addons/account_fleet/models/fleet_vehicle_log_services.py:7); inherits `account.tax` (addons/account_fleet/models/account_tax.py:4); inherits `account.account` (addons/account_fleet/models/account_account.py:4); inherits `account.move` (addons/account_fleet/models/account_move.py:7); inherits `account.move.line` (addons/account_fleet/models/account_move.py:52); inherits `fleet.vehicle` (addons/account_fleet/models/fleet_vehicle.py:7); inherits `account.automatic.entry.wizard` (addons/account_fleet/wizard/account_automatic_entry_wizard.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `fleet`, `account`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/account_fleet/__init__.py`
- `addons/account_fleet/__manifest__.py`
- `addons/account_fleet/data/fleet_service_type_data.xml`
- `addons/account_fleet/i18n/account_fleet.pot`
- `addons/account_fleet/i18n/ar.po`
- `addons/account_fleet/i18n/az.po`
- `addons/account_fleet/i18n/bg.po`
- `addons/account_fleet/i18n/bs.po`
- `addons/account_fleet/i18n/ca.po`
- `addons/account_fleet/i18n/cs.po`
- `addons/account_fleet/i18n/da.po`
- `addons/account_fleet/i18n/de.po`
- `addons/account_fleet/i18n/el.po`
- `addons/account_fleet/i18n/es.po`
- `addons/account_fleet/i18n/es_419.po`
- `addons/account_fleet/i18n/et.po`
- `addons/account_fleet/i18n/fa.po`
- `addons/account_fleet/i18n/fi.po`
- `addons/account_fleet/i18n/fr.po`
- `addons/account_fleet/i18n/he.po`
- `addons/account_fleet/i18n/hi.po`
- `addons/account_fleet/i18n/hr.po`
- `addons/account_fleet/i18n/hu.po`
- `addons/account_fleet/i18n/id.po`
- `addons/account_fleet/i18n/it.po`
- `addons/account_fleet/i18n/ja.po`
- `addons/account_fleet/i18n/kab.po`
- `addons/account_fleet/i18n/ko.po`
- `addons/account_fleet/i18n/ku.po`
- `addons/account_fleet/i18n/lo.po`
- `addons/account_fleet/i18n/lt.po`
- `addons/account_fleet/i18n/lv.po`
- `addons/account_fleet/i18n/mn.po`
- `addons/account_fleet/i18n/my.po`
- `addons/account_fleet/i18n/nb.po`
- `addons/account_fleet/i18n/nl.po`
- `addons/account_fleet/i18n/pl.po`
- `addons/account_fleet/i18n/pt.po`
- `addons/account_fleet/i18n/pt_BR.po`
- `addons/account_fleet/i18n/ro.po`
- `addons/account_fleet/i18n/ru.po`
- `addons/account_fleet/i18n/sk.po`
- `addons/account_fleet/i18n/sl.po`
- `addons/account_fleet/i18n/sr@latin.po`
- `addons/account_fleet/i18n/sv.po`
- `addons/account_fleet/i18n/th.po`
- `addons/account_fleet/i18n/tr.po`
- `addons/account_fleet/i18n/uk.po`
- `addons/account_fleet/i18n/uz.po`
- `addons/account_fleet/i18n/vi.po`
- `addons/account_fleet/i18n/zh_CN.po`
- `addons/account_fleet/i18n/zh_TW.po`
- `addons/account_fleet/models/__init__.py`
- `addons/account_fleet/models/account_account.py`
- `addons/account_fleet/models/account_move.py`
- `addons/account_fleet/models/account_tax.py`
- `addons/account_fleet/models/fleet_vehicle.py`
- `addons/account_fleet/models/fleet_vehicle_log_services.py`
- `addons/account_fleet/tests/__init__.py`
- `addons/account_fleet/tests/test_account_fleet.py`
- `addons/account_fleet/tests/test_account_fleet_tax_report.py`
- `addons/account_fleet/tests/test_fleet_vehicle_log_services.py`
- `addons/account_fleet/views/account_account_views.xml`
- `addons/account_fleet/views/account_move_views.xml`
- `addons/account_fleet/views/fleet_vehicle_log_services_views.xml`
- `addons/account_fleet/views/fleet_vehicle_views.xml`
- `addons/account_fleet/views/report_invoice.xml`
- `addons/account_fleet/wizard/__init__.py`
- `addons/account_fleet/wizard/account_automatic_entry_wizard.py`
