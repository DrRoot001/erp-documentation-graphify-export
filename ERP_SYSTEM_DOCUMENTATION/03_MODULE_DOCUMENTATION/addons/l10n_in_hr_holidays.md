# Module: l10n_in_hr_holidays

- **Module ID:** MOD-233
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_in_hr_holidays`
- **Manifest:** `addons/l10n_in_hr_holidays/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources/Time Off`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Leave Management of Indian Localization

**Manifest description:**

The Indian Time Off module provides additional features to the application. With it, you'll be able to define Sandwich Leaves on your time type, including weekends or holidays in the duration of the employee leave's request.

**Scope evidence:** The module contains 18 files, including 10 Python, 4 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `hr_holidays`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 1
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_in_hr_holidays/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 58 methods, 1 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/l10n_in_hr_holidays/models/hr_leave.py:13`, `addons/l10n_in_hr_holidays/models/hr_work_entry_type.py:6`, `addons/l10n_in_hr_holidays/models/hr_employee.py:6`, `addons/l10n_in_hr_holidays/models/l10n_in_hr_leave_optional_holiday.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 1 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/l10n_in_hr_holidays/views/l10n_in_hr_leave_optional_holiday_views.xml:3`, `addons/l10n_in_hr_holidays/views/l10n_in_hr_leave_optional_holiday_views.xml:14`, `addons/l10n_in_hr_holidays/views/l10n_in_hr_leave_optional_holiday_views.xml:31`, `addons/l10n_in_hr_holidays/views/l10n_in_hr_leave_optional_holiday_views.xml:38`, `addons/l10n_in_hr_holidays/views/hr_leave_views.xml:4`, `addons/l10n_in_hr_holidays/views/hr_work_entry_type_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_in_hr_holidays/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_in_hr_holidays/tests/test_sandwich_leave.py`, `addons/l10n_in_hr_holidays/tests/__init__.py`, `addons/l10n_in_hr_holidays/tests/test_optional_holiday.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `l10n_in_hr_leave_optional_holiday_view_list`, `l10n_in_hr_leave_optional_holiday_view_search`, `l10n_in_hr_leave_optional_holiday_action`, `Optional Holidays`, `hr_leave_view_form_inherit`, `hr_work_entry_type_view_form_inherit`
- Menus: 1; representative evidence: `addons/l10n_in_hr_holidays/views/l10n_in_hr_leave_optional_holiday_views.xml:38`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 10; representative evidence: `addons/l10n_in_hr_holidays/views/l10n_in_hr_leave_optional_holiday_views.xml:4`, `addons/l10n_in_hr_holidays/views/l10n_in_hr_leave_optional_holiday_views.xml:5`, `addons/l10n_in_hr_holidays/views/l10n_in_hr_leave_optional_holiday_views.xml:15`, `addons/l10n_in_hr_holidays/views/l10n_in_hr_leave_optional_holiday_views.xml:16`, `addons/l10n_in_hr_holidays/views/l10n_in_hr_leave_optional_holiday_views.xml:33`, `addons/l10n_in_hr_holidays/views/l10n_in_hr_leave_optional_holiday_views.xml:34`, `addons/l10n_in_hr_holidays/views/hr_leave_views.xml:6`, `addons/l10n_in_hr_holidays/views/hr_leave_views.xml:8`, `addons/l10n_in_hr_holidays/views/hr_work_entry_type_views.xml:6`, `addons/l10n_in_hr_holidays/views/hr_work_entry_type_views.xml:9`
- Browser assets: 1; representative files: `addons/l10n_in_hr_holidays/static/src/views/calendar/side_panel/calendar_side_panel.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_in_hr_holidays/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `hr.leave` (addons/l10n_in_hr_holidays/models/hr_leave.py:13); inherits `hr.work.entry.type` (addons/l10n_in_hr_holidays/models/hr_work_entry_type.py:6); inherits `hr.employee` (addons/l10n_in_hr_holidays/models/hr_employee.py:6); `l10n.in.hr.leave.optional.holiday` (addons/l10n_in_hr_holidays/models/l10n_in_hr_leave_optional_holiday.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr_holidays`
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

- `addons/l10n_in_hr_holidays/__init__.py`
- `addons/l10n_in_hr_holidays/__manifest__.py`
- `addons/l10n_in_hr_holidays/i18n/hi.po`
- `addons/l10n_in_hr_holidays/i18n/l10n_in_hr_holidays.pot`
- `addons/l10n_in_hr_holidays/models/__init__.py`
- `addons/l10n_in_hr_holidays/models/hr_employee.py`
- `addons/l10n_in_hr_holidays/models/hr_leave.py`
- `addons/l10n_in_hr_holidays/models/hr_work_entry_type.py`
- `addons/l10n_in_hr_holidays/models/l10n_in_hr_leave_optional_holiday.py`
- `addons/l10n_in_hr_holidays/security/ir.access.csv`
- `addons/l10n_in_hr_holidays/static/src/views/calendar/side_panel/calendar_side_panel.js`
- `addons/l10n_in_hr_holidays/static/src/views/calendar/side_panel/calendar_side_panel.xml`
- `addons/l10n_in_hr_holidays/tests/__init__.py`
- `addons/l10n_in_hr_holidays/tests/test_optional_holiday.py`
- `addons/l10n_in_hr_holidays/tests/test_sandwich_leave.py`
- `addons/l10n_in_hr_holidays/views/hr_leave_views.xml`
- `addons/l10n_in_hr_holidays/views/hr_work_entry_type_views.xml`
- `addons/l10n_in_hr_holidays/views/l10n_in_hr_leave_optional_holiday_views.xml`
