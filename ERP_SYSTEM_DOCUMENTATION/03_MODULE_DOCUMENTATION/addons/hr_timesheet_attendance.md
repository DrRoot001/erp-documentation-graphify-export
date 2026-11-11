# Module: hr_timesheet_attendance

- **Module ID:** MOD-103
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_timesheet_attendance`
- **Manifest:** `addons/hr_timesheet_attendance/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources/Attendances`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Module linking the attendance module to the timesheet app.

**Scope evidence:** The module contains 72 files, including 9 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `hr_timesheet`, `hr_attendance`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 1
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr_timesheet_attendance/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 6 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/hr_timesheet_attendance/models/ir_ui_menu.py:6`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 7 record/template/menu identifiers.
- **Evidence:** `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:4`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:19`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:35`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:46`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:62`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:69`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:75`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/hr_timesheet_attendance/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/hr_timesheet_attendance/tests/test_timesheet_attendance.py`, `addons/hr_timesheet_attendance/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `view_hr_timesheet_attendance_report_search`, `view_hr_timesheet_attendance_report_pivot`, `hr_timesheet_attendance_report_view_graph`, `action_hr_timesheet_attendance_report`, `action_hr_timesheet_attendance_report_pivot`, `action_hr_timesheet_attendance_report_graph`, `Timesheets / Attendance Analysis`
- Menus: 1; representative evidence: `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:75`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 10; representative evidence: `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:6`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:7`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:21`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:22`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:37`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:38`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:48`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:50`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:64`, `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml:70`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_timesheet_attendance/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `ir.ui.menu` (addons/hr_timesheet_attendance/models/ir_ui_menu.py:6); `hr.timesheet.attendance.report` (addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr_timesheet`, `hr_attendance`
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

- `addons/hr_timesheet_attendance/__init__.py`
- `addons/hr_timesheet_attendance/__manifest__.py`
- `addons/hr_timesheet_attendance/i18n/af.po`
- `addons/hr_timesheet_attendance/i18n/ar.po`
- `addons/hr_timesheet_attendance/i18n/az.po`
- `addons/hr_timesheet_attendance/i18n/bg.po`
- `addons/hr_timesheet_attendance/i18n/bs.po`
- `addons/hr_timesheet_attendance/i18n/ca.po`
- `addons/hr_timesheet_attendance/i18n/cs.po`
- `addons/hr_timesheet_attendance/i18n/da.po`
- `addons/hr_timesheet_attendance/i18n/de.po`
- `addons/hr_timesheet_attendance/i18n/el.po`
- `addons/hr_timesheet_attendance/i18n/es.po`
- `addons/hr_timesheet_attendance/i18n/es_419.po`
- `addons/hr_timesheet_attendance/i18n/es_CL.po`
- `addons/hr_timesheet_attendance/i18n/et.po`
- `addons/hr_timesheet_attendance/i18n/eu.po`
- `addons/hr_timesheet_attendance/i18n/fa.po`
- `addons/hr_timesheet_attendance/i18n/fi.po`
- `addons/hr_timesheet_attendance/i18n/fo.po`
- `addons/hr_timesheet_attendance/i18n/fr.po`
- `addons/hr_timesheet_attendance/i18n/fr_CA.po`
- `addons/hr_timesheet_attendance/i18n/gl.po`
- `addons/hr_timesheet_attendance/i18n/gu.po`
- `addons/hr_timesheet_attendance/i18n/he.po`
- `addons/hr_timesheet_attendance/i18n/hi.po`
- `addons/hr_timesheet_attendance/i18n/hr.po`
- `addons/hr_timesheet_attendance/i18n/hr_timesheet_attendance.pot`
- `addons/hr_timesheet_attendance/i18n/hu.po`
- `addons/hr_timesheet_attendance/i18n/id.po`
- `addons/hr_timesheet_attendance/i18n/is.po`
- `addons/hr_timesheet_attendance/i18n/it.po`
- `addons/hr_timesheet_attendance/i18n/ja.po`
- `addons/hr_timesheet_attendance/i18n/ka.po`
- `addons/hr_timesheet_attendance/i18n/kab.po`
- `addons/hr_timesheet_attendance/i18n/km.po`
- `addons/hr_timesheet_attendance/i18n/ko.po`
- `addons/hr_timesheet_attendance/i18n/ku.po`
- `addons/hr_timesheet_attendance/i18n/lo.po`
- `addons/hr_timesheet_attendance/i18n/lt.po`
- `addons/hr_timesheet_attendance/i18n/lv.po`
- `addons/hr_timesheet_attendance/i18n/mk.po`
- `addons/hr_timesheet_attendance/i18n/mn.po`
- `addons/hr_timesheet_attendance/i18n/my.po`
- `addons/hr_timesheet_attendance/i18n/nb.po`
- `addons/hr_timesheet_attendance/i18n/nl.po`
- `addons/hr_timesheet_attendance/i18n/pl.po`
- `addons/hr_timesheet_attendance/i18n/pt.po`
- `addons/hr_timesheet_attendance/i18n/pt_BR.po`
- `addons/hr_timesheet_attendance/i18n/ro.po`
- `addons/hr_timesheet_attendance/i18n/ru.po`
- `addons/hr_timesheet_attendance/i18n/sk.po`
- `addons/hr_timesheet_attendance/i18n/sl.po`
- `addons/hr_timesheet_attendance/i18n/sq.po`
- `addons/hr_timesheet_attendance/i18n/sr@latin.po`
- `addons/hr_timesheet_attendance/i18n/sv.po`
- `addons/hr_timesheet_attendance/i18n/th.po`
- `addons/hr_timesheet_attendance/i18n/tr.po`
- `addons/hr_timesheet_attendance/i18n/uk.po`
- `addons/hr_timesheet_attendance/i18n/uz.po`
- `addons/hr_timesheet_attendance/i18n/vi.po`
- `addons/hr_timesheet_attendance/i18n/zh_CN.po`
- `addons/hr_timesheet_attendance/i18n/zh_TW.po`
- `addons/hr_timesheet_attendance/models/__init__.py`
- `addons/hr_timesheet_attendance/models/ir_ui_menu.py`
- `addons/hr_timesheet_attendance/report/__init__.py`
- `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report.py`
- `addons/hr_timesheet_attendance/report/hr_timesheet_attendance_report_view.xml`
- `addons/hr_timesheet_attendance/security/ir.access.csv`
- `addons/hr_timesheet_attendance/tests/__init__.py`
- `addons/hr_timesheet_attendance/tests/test_timesheet_attendance.py`
- `addons/hr_timesheet_attendance/upgrades/1.1/pre-migrate.py`
