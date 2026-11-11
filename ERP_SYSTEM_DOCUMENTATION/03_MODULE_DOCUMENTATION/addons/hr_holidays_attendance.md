# Module: hr_holidays_attendance

- **Module ID:** MOD-090
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_holidays_attendance`
- **Manifest:** `addons/hr_holidays_attendance/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Attendance Holidays

**Manifest description:**

Convert employee's extra hours to leave allocations.

**Scope evidence:** The module contains 83 files, including 26 Python, 7 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `hr_attendance`, `hr_holidays`.

## 2. Module structure

- Model/business logic files: 11
- Controller/API files: 2
- XML/data/view/template files: 7
- Browser asset files: 0
- Security files: 1
- Test files: 9
- Scheduled/automation evidence files: 2
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr_holidays_attendance/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 11 model declarations, 250 methods, 1 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/hr_holidays_attendance/models/hr_leave.py:6`, `addons/hr_holidays_attendance/models/hr_leave_accrual_plan_level.py:6`, `addons/hr_holidays_attendance/models/hr_version.py:12`, `addons/hr_holidays_attendance/models/hr_time_rule.py:6`, `addons/hr_holidays_attendance/models/hr_attendance.py:12`, `addons/hr_holidays_attendance/models/hr_leave_allocation.py:10`, `addons/hr_holidays_attendance/models/resource_calendar_leaves.py:7`, `addons/hr_holidays_attendance/models/hr_employee.py:8`, `addons/hr_holidays_attendance/models/ir_ui_menu.py:6`, `addons/hr_holidays_attendance/models/res_company.py:6`, `addons/hr_holidays_attendance/report/hr_leave_attendance_report.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/hr_holidays_attendance/controllers/main.py`, `addons/hr_holidays_attendance/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 0 JavaScript/TypeScript files; static XML analysis found 12 record/template/menu identifiers.
- **Evidence:** `addons/hr_holidays_attendance/views/hr_attendance_views.xml:5`, `addons/hr_holidays_attendance/views/hr_attendance_views.xml:17`, `addons/hr_holidays_attendance/views/hr_leave_allocation_views.xml:3`, `addons/hr_holidays_attendance/views/hr_leave_allocation_views.xml:24`, `addons/hr_holidays_attendance/views/hr_leave_accrual_level_views.xml:3`, `addons/hr_holidays_attendance/views/hr_leave_attendance_report_views.xml:4`, `addons/hr_holidays_attendance/views/hr_leave_attendance_report_views.xml:22`, `addons/hr_holidays_attendance/views/hr_leave_attendance_report_views.xml:37`, `addons/hr_holidays_attendance/views/hr_leave_attendance_report_views.xml:83`, `addons/hr_holidays_attendance/views/hr_leave_attendance_report_views.xml:111`, `addons/hr_holidays_attendance/views/hr_leave_attendance_report_views.xml:125`, `addons/hr_holidays_attendance/views/hr_attendance_overtime_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/hr_holidays_attendance/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/hr_holidays_attendance/tests/test_leave_attendance_report.py`, `addons/hr_holidays_attendance/tests/test_time_rule_pipeline.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 9 test files are present.
- **Evidence:** `addons/hr_holidays_attendance/tests/test_leave_attendance_report.py`, `addons/hr_holidays_attendance/tests/test_performance.py`, `addons/hr_holidays_attendance/tests/test_work_entry_attendance.py`, `addons/hr_holidays_attendance/tests/common.py`, `addons/hr_holidays_attendance/tests/test_accrual_allocations.py`, `addons/hr_holidays_attendance/tests/test_time_rule_allocation_log.py`, `addons/hr_holidays_attendance/tests/test_time_rule_pipeline.py`, `addons/hr_holidays_attendance/tests/test_holidays_overtime.py`, `addons/hr_holidays_attendance/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `view_attendance_tree_inherit_holidays`, `view_attendance_search_inherit_holidays`, `hr_leave_allocation_overtime_manager_view_form`, `hr_leave_allocation_overtime_manager_action`, `hr_leave_accrual_level_view_form`, `hr_leave_attendance_report_view_list`, `hr_leave_attendance_report_view_pivot`, `hr_leave_attendance_report_view_form`, `hr_leave_attendance_report_view_search`, `hr_leave_attendance_report_action`, `Time Off Ledger`, `view_attendance_overtime_leave_form`
- Menus: 1; representative evidence: `addons/hr_holidays_attendance/views/hr_leave_attendance_report_views.xml:125`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 22; representative evidence: `addons/hr_holidays_attendance/views/hr_attendance_views.xml:7`, `addons/hr_holidays_attendance/views/hr_attendance_views.xml:9`, `addons/hr_holidays_attendance/views/hr_attendance_views.xml:19`, `addons/hr_holidays_attendance/views/hr_attendance_views.xml:21`, `addons/hr_holidays_attendance/views/hr_leave_allocation_views.xml:4`, `addons/hr_holidays_attendance/views/hr_leave_allocation_views.xml:8`, `addons/hr_holidays_attendance/views/hr_leave_allocation_views.xml:26`, `addons/hr_holidays_attendance/views/hr_leave_allocation_views.xml:27`, `addons/hr_holidays_attendance/views/hr_leave_accrual_level_views.xml:5`, `addons/hr_holidays_attendance/views/hr_leave_accrual_level_views.xml:7`, `addons/hr_holidays_attendance/views/hr_leave_attendance_report_views.xml:6`, `addons/hr_holidays_attendance/views/hr_leave_attendance_report_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_holidays_attendance/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/hr_holidays_attendance/tests/test_leave_attendance_report.py`, `addons/hr_holidays_attendance/tests/test_time_rule_pipeline.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 11
- Representative model evidence: inherits `hr.leave` (addons/hr_holidays_attendance/models/hr_leave.py:6); inherits `hr.leave.accrual.level` (addons/hr_holidays_attendance/models/hr_leave_accrual_plan_level.py:6); inherits `hr.version` (addons/hr_holidays_attendance/models/hr_version.py:12); inherits `hr.time.rule` (addons/hr_holidays_attendance/models/hr_time_rule.py:6); inherits `hr.attendance` (addons/hr_holidays_attendance/models/hr_attendance.py:12); inherits `hr.leave.allocation` (addons/hr_holidays_attendance/models/hr_leave_allocation.py:10); inherits `resource.calendar.leaves` (addons/hr_holidays_attendance/models/resource_calendar_leaves.py:7); inherits `hr.employee` (addons/hr_holidays_attendance/models/hr_employee.py:8); inherits `ir.ui.menu` (addons/hr_holidays_attendance/models/ir_ui_menu.py:6); inherits `res.company` (addons/hr_holidays_attendance/models/res_company.py:6); `hr.leave.attendance.report` (addons/hr_holidays_attendance/report/hr_leave_attendance_report.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr_attendance`, `hr_holidays`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/hr_holidays_attendance/__init__.py`
- `addons/hr_holidays_attendance/__manifest__.py`
- `addons/hr_holidays_attendance/controllers/__init__.py`
- `addons/hr_holidays_attendance/controllers/main.py`
- `addons/hr_holidays_attendance/data/hr_holidays_attendance_demo.xml`
- `addons/hr_holidays_attendance/i18n/ar.po`
- `addons/hr_holidays_attendance/i18n/az.po`
- `addons/hr_holidays_attendance/i18n/bg.po`
- `addons/hr_holidays_attendance/i18n/bs.po`
- `addons/hr_holidays_attendance/i18n/ca.po`
- `addons/hr_holidays_attendance/i18n/cs.po`
- `addons/hr_holidays_attendance/i18n/da.po`
- `addons/hr_holidays_attendance/i18n/de.po`
- `addons/hr_holidays_attendance/i18n/el.po`
- `addons/hr_holidays_attendance/i18n/es.po`
- `addons/hr_holidays_attendance/i18n/es_419.po`
- `addons/hr_holidays_attendance/i18n/et.po`
- `addons/hr_holidays_attendance/i18n/fa.po`
- `addons/hr_holidays_attendance/i18n/fi.po`
- `addons/hr_holidays_attendance/i18n/fr.po`
- `addons/hr_holidays_attendance/i18n/he.po`
- `addons/hr_holidays_attendance/i18n/hi.po`
- `addons/hr_holidays_attendance/i18n/hr.po`
- `addons/hr_holidays_attendance/i18n/hr_holidays_attendance.pot`
- `addons/hr_holidays_attendance/i18n/hu.po`
- `addons/hr_holidays_attendance/i18n/id.po`
- `addons/hr_holidays_attendance/i18n/it.po`
- `addons/hr_holidays_attendance/i18n/ja.po`
- `addons/hr_holidays_attendance/i18n/kab.po`
- `addons/hr_holidays_attendance/i18n/ko.po`
- `addons/hr_holidays_attendance/i18n/ku.po`
- `addons/hr_holidays_attendance/i18n/lo.po`
- `addons/hr_holidays_attendance/i18n/lt.po`
- `addons/hr_holidays_attendance/i18n/lv.po`
- `addons/hr_holidays_attendance/i18n/mn.po`
- `addons/hr_holidays_attendance/i18n/my.po`
- `addons/hr_holidays_attendance/i18n/nb.po`
- `addons/hr_holidays_attendance/i18n/nl.po`
- `addons/hr_holidays_attendance/i18n/pl.po`
- `addons/hr_holidays_attendance/i18n/pt.po`
- `addons/hr_holidays_attendance/i18n/pt_BR.po`
- `addons/hr_holidays_attendance/i18n/ro.po`
- `addons/hr_holidays_attendance/i18n/ru.po`
- `addons/hr_holidays_attendance/i18n/sk.po`
- `addons/hr_holidays_attendance/i18n/sl.po`
- `addons/hr_holidays_attendance/i18n/sr@latin.po`
- `addons/hr_holidays_attendance/i18n/sv.po`
- `addons/hr_holidays_attendance/i18n/th.po`
- `addons/hr_holidays_attendance/i18n/tr.po`
- `addons/hr_holidays_attendance/i18n/uk.po`
- `addons/hr_holidays_attendance/i18n/uz.po`
- `addons/hr_holidays_attendance/i18n/vi.po`
- `addons/hr_holidays_attendance/i18n/zh_CN.po`
- `addons/hr_holidays_attendance/i18n/zh_TW.po`
- `addons/hr_holidays_attendance/models/__init__.py`
- `addons/hr_holidays_attendance/models/hr_attendance.py`
- `addons/hr_holidays_attendance/models/hr_employee.py`
- `addons/hr_holidays_attendance/models/hr_leave.py`
- `addons/hr_holidays_attendance/models/hr_leave_accrual_plan_level.py`
- `addons/hr_holidays_attendance/models/hr_leave_allocation.py`
- `addons/hr_holidays_attendance/models/hr_time_rule.py`
- `addons/hr_holidays_attendance/models/hr_version.py`
- `addons/hr_holidays_attendance/models/ir_ui_menu.py`
- `addons/hr_holidays_attendance/models/res_company.py`
- `addons/hr_holidays_attendance/models/resource_calendar_leaves.py`
- `addons/hr_holidays_attendance/report/__init__.py`
- `addons/hr_holidays_attendance/report/hr_leave_attendance_report.py`
- `addons/hr_holidays_attendance/security/ir.access.csv`
- `addons/hr_holidays_attendance/static/src/components/accrual_levels/accrual_levels.xml`
- `addons/hr_holidays_attendance/tests/__init__.py`
- `addons/hr_holidays_attendance/tests/common.py`
- `addons/hr_holidays_attendance/tests/test_accrual_allocations.py`
- `addons/hr_holidays_attendance/tests/test_holidays_overtime.py`
- `addons/hr_holidays_attendance/tests/test_leave_attendance_report.py`
- `addons/hr_holidays_attendance/tests/test_performance.py`
- `addons/hr_holidays_attendance/tests/test_time_rule_allocation_log.py`
- `addons/hr_holidays_attendance/tests/test_time_rule_pipeline.py`
- `addons/hr_holidays_attendance/tests/test_work_entry_attendance.py`
- `addons/hr_holidays_attendance/views/hr_attendance_overtime_views.xml`
- `addons/hr_holidays_attendance/views/hr_attendance_views.xml`
- `addons/hr_holidays_attendance/views/hr_leave_accrual_level_views.xml`
- `addons/hr_holidays_attendance/views/hr_leave_allocation_views.xml`
- `addons/hr_holidays_attendance/views/hr_leave_attendance_report_views.xml`
