# Module: project_timesheet_holidays

- **Module ID:** MOD-491
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/project_timesheet_holidays`
- **Manifest:** `addons/project_timesheet_holidays/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Schedule timesheet when on time off

**Manifest description:**

Bridge module to integrate leaves in timesheet
================================================

This module allows to automatically log timesheets when employees are
on leaves. Project and task can be configured company-wide.

**Scope evidence:** The module contains 72 files, including 16 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `hr_timesheet`, `hr_holidays`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 0
- XML/data/view/template files: 3
- Browser asset files: 0
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/project_timesheet_holidays/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 76 methods, 0 constraint handlers, 2 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/project_timesheet_holidays/models/hr_employee_departure.py:4`, `addons/project_timesheet_holidays/models/res_config_settings.py:7`, `addons/project_timesheet_holidays/models/hr_leave.py:8`, `addons/project_timesheet_holidays/models/account_analytic.py:8`, `addons/project_timesheet_holidays/models/project_task.py:7`, `addons/project_timesheet_holidays/models/resource_calendar_leaves.py:9`, `addons/project_timesheet_holidays/models/hr_employee.py:8`, `addons/project_timesheet_holidays/models/res_company.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/project_timesheet_holidays/views/res_config_settings_views.xml:4`, `addons/project_timesheet_holidays/views/project_task_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/project_timesheet_holidays/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/project_timesheet_holidays/tests/test_timesheet_holidays.py`, `addons/project_timesheet_holidays/tests/test_employee.py`, `addons/project_timesheet_holidays/tests/__init__.py`, `addons/project_timesheet_holidays/tests/test_cancel_time_off.py`, `addons/project_timesheet_holidays/tests/test_timesheet_global_time_off.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `res_config_settings_view_form`, `leave_task_form_view`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/project_timesheet_holidays/views/res_config_settings_views.xml:6`, `addons/project_timesheet_holidays/views/res_config_settings_views.xml:8`, `addons/project_timesheet_holidays/views/project_task_views.xml:6`, `addons/project_timesheet_holidays/views/project_task_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/project_timesheet_holidays/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: inherits `hr.employee.departure` (addons/project_timesheet_holidays/models/hr_employee_departure.py:4); inherits `res.config.settings` (addons/project_timesheet_holidays/models/res_config_settings.py:7); inherits `hr.leave` (addons/project_timesheet_holidays/models/hr_leave.py:8); inherits `account.analytic.line` (addons/project_timesheet_holidays/models/account_analytic.py:8); inherits `project.task` (addons/project_timesheet_holidays/models/project_task.py:7); inherits `resource.calendar.leaves` (addons/project_timesheet_holidays/models/resource_calendar_leaves.py:9); inherits `hr.employee` (addons/project_timesheet_holidays/models/hr_employee.py:8); inherits `res.company` (addons/project_timesheet_holidays/models/res_company.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr_timesheet`, `hr_holidays`
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

- `addons/project_timesheet_holidays/__init__.py`
- `addons/project_timesheet_holidays/__manifest__.py`
- `addons/project_timesheet_holidays/data/holiday_timesheets_demo.xml`
- `addons/project_timesheet_holidays/i18n/ar.po`
- `addons/project_timesheet_holidays/i18n/az.po`
- `addons/project_timesheet_holidays/i18n/bg.po`
- `addons/project_timesheet_holidays/i18n/bs.po`
- `addons/project_timesheet_holidays/i18n/ca.po`
- `addons/project_timesheet_holidays/i18n/cs.po`
- `addons/project_timesheet_holidays/i18n/da.po`
- `addons/project_timesheet_holidays/i18n/de.po`
- `addons/project_timesheet_holidays/i18n/el.po`
- `addons/project_timesheet_holidays/i18n/es.po`
- `addons/project_timesheet_holidays/i18n/es_419.po`
- `addons/project_timesheet_holidays/i18n/et.po`
- `addons/project_timesheet_holidays/i18n/fa.po`
- `addons/project_timesheet_holidays/i18n/fi.po`
- `addons/project_timesheet_holidays/i18n/fr.po`
- `addons/project_timesheet_holidays/i18n/gu.po`
- `addons/project_timesheet_holidays/i18n/he.po`
- `addons/project_timesheet_holidays/i18n/hi.po`
- `addons/project_timesheet_holidays/i18n/hr.po`
- `addons/project_timesheet_holidays/i18n/hu.po`
- `addons/project_timesheet_holidays/i18n/id.po`
- `addons/project_timesheet_holidays/i18n/is.po`
- `addons/project_timesheet_holidays/i18n/it.po`
- `addons/project_timesheet_holidays/i18n/ja.po`
- `addons/project_timesheet_holidays/i18n/kab.po`
- `addons/project_timesheet_holidays/i18n/km.po`
- `addons/project_timesheet_holidays/i18n/ko.po`
- `addons/project_timesheet_holidays/i18n/ku.po`
- `addons/project_timesheet_holidays/i18n/lo.po`
- `addons/project_timesheet_holidays/i18n/lt.po`
- `addons/project_timesheet_holidays/i18n/lv.po`
- `addons/project_timesheet_holidays/i18n/mn.po`
- `addons/project_timesheet_holidays/i18n/my.po`
- `addons/project_timesheet_holidays/i18n/nb.po`
- `addons/project_timesheet_holidays/i18n/nl.po`
- `addons/project_timesheet_holidays/i18n/pl.po`
- `addons/project_timesheet_holidays/i18n/project_timesheet_holidays.pot`
- `addons/project_timesheet_holidays/i18n/pt.po`
- `addons/project_timesheet_holidays/i18n/pt_BR.po`
- `addons/project_timesheet_holidays/i18n/ro.po`
- `addons/project_timesheet_holidays/i18n/ru.po`
- `addons/project_timesheet_holidays/i18n/sk.po`
- `addons/project_timesheet_holidays/i18n/sl.po`
- `addons/project_timesheet_holidays/i18n/sr@latin.po`
- `addons/project_timesheet_holidays/i18n/sv.po`
- `addons/project_timesheet_holidays/i18n/th.po`
- `addons/project_timesheet_holidays/i18n/tr.po`
- `addons/project_timesheet_holidays/i18n/uk.po`
- `addons/project_timesheet_holidays/i18n/uz.po`
- `addons/project_timesheet_holidays/i18n/vi.po`
- `addons/project_timesheet_holidays/i18n/zh_CN.po`
- `addons/project_timesheet_holidays/i18n/zh_TW.po`
- `addons/project_timesheet_holidays/models/__init__.py`
- `addons/project_timesheet_holidays/models/account_analytic.py`
- `addons/project_timesheet_holidays/models/hr_employee.py`
- `addons/project_timesheet_holidays/models/hr_employee_departure.py`
- `addons/project_timesheet_holidays/models/hr_leave.py`
- `addons/project_timesheet_holidays/models/project_task.py`
- `addons/project_timesheet_holidays/models/res_company.py`
- `addons/project_timesheet_holidays/models/res_config_settings.py`
- `addons/project_timesheet_holidays/models/resource_calendar_leaves.py`
- `addons/project_timesheet_holidays/security/ir.access.csv`
- `addons/project_timesheet_holidays/tests/__init__.py`
- `addons/project_timesheet_holidays/tests/test_cancel_time_off.py`
- `addons/project_timesheet_holidays/tests/test_employee.py`
- `addons/project_timesheet_holidays/tests/test_timesheet_global_time_off.py`
- `addons/project_timesheet_holidays/tests/test_timesheet_holidays.py`
- `addons/project_timesheet_holidays/views/project_task_views.xml`
- `addons/project_timesheet_holidays/views/res_config_settings_views.xml`
