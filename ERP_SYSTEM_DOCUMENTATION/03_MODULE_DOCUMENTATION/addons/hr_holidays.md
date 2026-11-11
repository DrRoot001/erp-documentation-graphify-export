# Module: hr_holidays

- **Module ID:** MOD-089
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_holidays`
- **Manifest:** `addons/hr_holidays/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Human Resources/Time Off`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Allocate time off and follow leave requests

**Manifest description:**

Manage time off requests and allocations
========================================

This application controls the time off schedule of your company. It allows employees to request time off. Then, managers can review requests for time off and approve or reject them. This way you can control the overall time off planning for the company or department.

You can configure several kinds of time off (sickness, paid days, ...) and allocate time off to an employee or department quickly using time off allocation. An employee can also make a request for more days off by making a new time off allocation. It will increase the total of available days for that time type (if the request is accepted).

You can keep track of time off in different ways by following reports:

* Time Off Summary
* Time Off by Department
* Time Off Analysis

A synchronization with an internal agenda (Meetings of the CRM module) is also possible in order to automatically create a meeting when a time off request is accepted by setting up a type of meeting in time off Type.

**Scope evidence:** The module contains 330 files, including 88 Python, 53 XML, and 74 JavaScript/TypeScript files. The manifest declares dependencies: `hr_work_entry`, `hr_calendar`, `resource`.

## 2. Module structure

- Model/business logic files: 36
- Controller/API files: 3
- XML/data/view/template files: 53
- Browser asset files: 74
- Security files: 2
- Test files: 44
- Scheduled/automation evidence files: 7
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr_holidays/security/ir.access.csv`, `addons/hr_holidays/security/hr_holidays_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 36 model declarations, 949 methods, 19 constraint handlers, 11 onchange handlers, and 84 dependency declarations.
- **Evidence:** `addons/hr_holidays/models/hr_employee_departure.py:8`, `addons/hr_holidays/models/res_partner.py:6`, `addons/hr_holidays/models/res_groups.py:6`, `addons/hr_holidays/models/hr_leave.py:36`, `addons/hr_holidays/models/hr_employee_public.py:8`, `addons/hr_holidays/models/hr_work_entry_type.py:30`, `addons/hr_holidays/models/hr_leave_accrual_plan_level.py:14`, `addons/hr_holidays/models/hr_department.py:12`, `addons/hr_holidays/models/hr_version.py:9`, `addons/hr_holidays/models/hr_time_rule.py:10`, `addons/hr_holidays/models/hr_time_rule.py:32`, `addons/hr_holidays/models/resource_calendar.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 5 route declarations.
- **Evidence:** `addons/hr_holidays/controllers/main.py:10`, `addons/hr_holidays/controllers/main.py:20`, `addons/hr_holidays/controllers/main.py:30`, `addons/hr_holidays/controllers/main.py:40`, `addons/hr_holidays/controllers/main.py:50`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 53 XML files and 74 JavaScript/TypeScript files; static XML analysis found 424 record/template/menu identifiers.
- **Evidence:** `addons/hr_holidays/security/hr_holidays_security.xml:2`, `addons/hr_holidays/security/hr_holidays_security.xml:8`, `addons/hr_holidays/security/hr_holidays_security.xml:15`, `addons/hr_holidays/security/hr_holidays_security.xml:20`, `addons/hr_holidays/security/hr_holidays_security.xml:27`, `addons/hr_holidays/security/hr_holidays_security.xml:38`, `addons/hr_holidays/security/hr_holidays_security.xml:42`, `addons/hr_holidays/report/hr_leave_employee_report_views.xml:4`, `addons/hr_holidays/report/hr_leave_employee_report_views.xml:15`, `addons/hr_holidays/report/hr_leave_employee_report_views.xml:27`, `addons/hr_holidays/report/hr_leave_employee_report_views.xml:84`, `addons/hr_holidays/report/hr_holidays_templates.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/hr_holidays/security/ir.access.csv`, `addons/hr_holidays/security/hr_holidays_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 7 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/hr_holidays/__manifest__.py`, `addons/hr_holidays/models/resource_calendar_leaves.py`, `addons/hr_holidays/models/res_company.py`, `addons/hr_holidays/report/hr_leave_employee_type_report.xml`, `addons/hr_holidays/data/ir_cron_data.xml`, `addons/hr_holidays/tests/test_accrual_allocations.py`, `addons/hr_holidays/tests/test_global_leaves.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/hr_holidays/report/holidays_summary_report.py`, `addons/hr_holidays/report/hr_holidays_reports.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 44 test files are present.
- **Evidence:** `addons/hr_holidays/tests/test_hr_departure.py`, `addons/hr_holidays/tests/test_access_rights.py`, `addons/hr_holidays/tests/test_holidays_mail.py`, `addons/hr_holidays/tests/test_dashboard.py`, `addons/hr_holidays/tests/test_time_off_graph_view_tour.py`, `addons/hr_holidays/tests/test_change_department.py`, `addons/hr_holidays/tests/test_timeoff_overview_my_department_tour.py`, `addons/hr_holidays/tests/test_time_rule_day_types.py`, `addons/hr_holidays/tests/test_leave_requests.py`, `addons/hr_holidays/tests/test_departure.py`, `addons/hr_holidays/tests/test_automatic_leave_dates.py`, `addons/hr_holidays/tests/test_holidays_flow.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 53; representative identifiers: `res_groups_privilege_time_off`, `group_hr_holidays_employee`, `group_hr_holidays_responsible`, `group_hr_holidays_user`, `group_hr_holidays_manager`, `hr.group_hr_user`, `base.default_user_group`, `hr_leave_employee_report_view_pivot`, `hr_leave_employee_report_view_graph`, `hr_leave_employee_report_filter`, `action_hr_leave_employee_report`, `report_holidayssummary`, `view_hr_holidays_filter_report`, `hr_leave_report_tree`, `hr_leave_report_graph`, `hr_leave_report_pivot`, `action_hr_leave_report`, `hr_leave_report_action`, `view_search_hr_holidays_employee_type_report`, `hr_leave_employee_type_report`
- Menus: 19; representative evidence: `addons/hr_holidays/views/hr_holidays_views.xml:4`, `addons/hr_holidays/views/hr_holidays_views.xml:11`, `addons/hr_holidays/views/hr_holidays_views.xml:17`, `addons/hr_holidays/views/hr_holidays_views.xml:25`, `addons/hr_holidays/views/hr_holidays_views.xml:32`, `addons/hr_holidays/views/hr_holidays_views.xml:39`, `addons/hr_holidays/views/hr_holidays_views.xml:46`, `addons/hr_holidays/views/hr_holidays_views.xml:53`, `addons/hr_holidays/views/hr_holidays_views.xml:60`, `addons/hr_holidays/views/hr_holidays_views.xml:67`, `addons/hr_holidays/views/hr_holidays_views.xml:74`, `addons/hr_holidays/views/hr_holidays_views.xml:81`
- Templates: 5; representative evidence: `addons/hr_holidays/report/hr_holidays_templates.xml:4`, `addons/hr_holidays/views/hr_leave_accrual_views.xml:190`, `addons/hr_holidays/views/hr_leave_accrual_views.xml:192`, `addons/hr_holidays/views/hr_leave_accrual_views.xml:199`, `addons/hr_holidays/views/hr_leave_accrual_views.xml:201`
- View/action field declarations: 226; representative evidence: `addons/hr_holidays/report/hr_leave_employee_report_views.xml:5`, `addons/hr_holidays/report/hr_leave_employee_report_views.xml:6`, `addons/hr_holidays/report/hr_leave_employee_report_views.xml:16`, `addons/hr_holidays/report/hr_leave_employee_report_views.xml:17`, `addons/hr_holidays/report/hr_leave_employee_report_views.xml:28`, `addons/hr_holidays/report/hr_leave_employee_report_views.xml:29`, `addons/hr_holidays/report/hr_leave_employee_report_views.xml:86`, `addons/hr_holidays/report/hr_leave_employee_report_views.xml:87`, `addons/hr_holidays/report/hr_leave_reports.xml:6`, `addons/hr_holidays/report/hr_leave_reports.xml:7`, `addons/hr_holidays/report/hr_leave_reports.xml:37`, `addons/hr_holidays/report/hr_leave_reports.xml:38`
- Browser assets: 74; representative files: `addons/hr_holidays/static/src/utils.js`, `addons/hr_holidays/static/tests/accrual_levels_widget.test.js`, `addons/hr_holidays/static/tests/out_of_office_text.test.js`, `addons/hr_holidays/static/tests/calendar_year.test.js`, `addons/hr_holidays/static/tests/leave_stats.test.js`, `addons/hr_holidays/static/tests/dashboard_card_hour_format.test.js`, `addons/hr_holidays/static/tests/chat_window_patch.test.js`, `addons/hr_holidays/static/tests/im_status.test.js`, `addons/hr_holidays/static/tests/thread_icon_patch.test.js`, `addons/hr_holidays/static/tests/hr_presence_status.test.js`, `addons/hr_holidays/static/tests/discuss_content_patch.test.js`, `addons/hr_holidays/static/tests/hr_holidays_test_helpers.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_holidays/__manifest__.py`
- **HTTP entry points:** `addons/hr_holidays/controllers/main.py:10`, `addons/hr_holidays/controllers/main.py:20`, `addons/hr_holidays/controllers/main.py:30`, `addons/hr_holidays/controllers/main.py:40`, `addons/hr_holidays/controllers/main.py:50`
- **Scheduled entry points:** `addons/hr_holidays/__manifest__.py`, `addons/hr_holidays/models/resource_calendar_leaves.py`, `addons/hr_holidays/models/res_company.py`, `addons/hr_holidays/report/hr_leave_employee_type_report.xml`, `addons/hr_holidays/data/ir_cron_data.xml`, `addons/hr_holidays/tests/test_accrual_allocations.py`, `addons/hr_holidays/tests/test_global_leaves.py`
- **Report entry points:** `addons/hr_holidays/report/holidays_summary_report.py`, `addons/hr_holidays/report/hr_holidays_reports.xml`

## 7. Database interactions

- Model declarations: 36
- Representative model evidence: inherits `hr.employee.departure` (addons/hr_holidays/models/hr_employee_departure.py:8); inherits `res.partner` (addons/hr_holidays/models/res_partner.py:6); inherits `res.groups` (addons/hr_holidays/models/res_groups.py:6); `hr.leave` (addons/hr_holidays/models/hr_leave.py:36); inherits `hr.employee.public` (addons/hr_holidays/models/hr_employee_public.py:8); inherits `hr.work.entry.type` (addons/hr_holidays/models/hr_work_entry_type.py:30); `hr.leave.accrual.level` (addons/hr_holidays/models/hr_leave_accrual_plan_level.py:14); inherits `hr.department` (addons/hr_holidays/models/hr_department.py:12); inherits `hr.version` (addons/hr_holidays/models/hr_version.py:9); inherits `hr.time.rule.source.mixin` (addons/hr_holidays/models/hr_time_rule.py:10); inherits `hr.time.rule` (addons/hr_holidays/models/hr_time_rule.py:32); inherits `resource.calendar` (addons/hr_holidays/models/resource_calendar.py:6); inherits `resource.resource` (addons/hr_holidays/models/resource_resource.py:11); inherits `calendar.event` (addons/hr_holidays/models/calendar_event.py:4); `hr.leave.display.name.mixin` (addons/hr_holidays/models/hr_leave_display_name_mixin.py:6); inherits `mail.activity.type` (addons/hr_holidays/models/mail_activity_type.py:4); `hr.leave.allocation` (addons/hr_holidays/models/hr_leave_allocation.py:17); inherits `res.users` (addons/hr_holidays/models/res_users.py:9); inherits `resource.calendar.leaves` (addons/hr_holidays/models/resource_calendar_leaves.py:14); `hr.leave.mandatory.day` (addons/hr_holidays/models/hr_leave_mandatory_day.py:7); inherits `hr.employee` (addons/hr_holidays/models/hr_employee.py:17); inherits `mail.message.subtype` (addons/hr_holidays/models/mail_message_subtype.py:11); `hr.time.rule.allocation.log` (addons/hr_holidays/models/hr_time_rule_allocation_log.py:6); `hr.leave.accrual.plan` (addons/hr_holidays/models/hr_leave_accrual_plan.py:11); inherits `res.company` (addons/hr_holidays/models/res_company.py:5); `hr.leave.employee.report` (addons/hr_holidays/report/hr_leave_employee_report.py:14); `hr.leave.employee.type.report` (addons/hr_holidays/report/hr_leave_employee_type_report.py:7); `hr.leave.report.calendar` (addons/hr_holidays/report/hr_leave_report_calendar.py:10); `hr.leave.report` (addons/hr_holidays/report/hr_leave_report.py:5); `report.hr_holidays.report_holidayssummary` (addons/hr_holidays/report/holidays_summary_report.py:29)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 5
- Route evidence: `addons/hr_holidays/controllers/main.py:10`, `addons/hr_holidays/controllers/main.py:20`, `addons/hr_holidays/controllers/main.py:30`, `addons/hr_holidays/controllers/main.py:40`, `addons/hr_holidays/controllers/main.py:50`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr_work_entry`, `hr_calendar`, `resource`
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

- `addons/hr_holidays/__init__.py`
- `addons/hr_holidays/__manifest__.py`
- `addons/hr_holidays/controllers/__init__.py`
- `addons/hr_holidays/controllers/main.py`
- `addons/hr_holidays/controllers/webmanifest.py`
- `addons/hr_holidays/data/hr_holidays_demo.xml`
- `addons/hr_holidays/data/hr_holidays_tour.xml`
- `addons/hr_holidays/data/hr_time_rule_data.xml`
- `addons/hr_holidays/data/hr_work_entry_type_data.xml`
- `addons/hr_holidays/data/ir_cron_data.xml`
- `addons/hr_holidays/data/mail_activity_type_data.xml`
- `addons/hr_holidays/data/mail_message_subtype_data.xml`
- `addons/hr_holidays/data/mail_template_data.xml`
- `addons/hr_holidays/data/public_holidays/public_holidays_ar.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_au.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_be.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_br.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_ca.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_ch.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_cl.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_co.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_do.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_ec.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_eg.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_gt.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_hk.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_in.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_jo.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_ke.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_lt.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_lu.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_ma.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_mx.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_my.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_nl.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_pa.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_pe.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_pl.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_ro.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_sa.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_sk.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_tr.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_us.csv`
- `addons/hr_holidays/data/public_holidays/public_holidays_uy.csv`
- `addons/hr_holidays/data/report_paperformat.xml`
- `addons/hr_holidays/i18n/af.po`
- `addons/hr_holidays/i18n/am.po`
- `addons/hr_holidays/i18n/ar.po`
- `addons/hr_holidays/i18n/az.po`
- `addons/hr_holidays/i18n/bg.po`
- `addons/hr_holidays/i18n/bs.po`
- `addons/hr_holidays/i18n/ca.po`
- `addons/hr_holidays/i18n/cs.po`
- `addons/hr_holidays/i18n/da.po`
- `addons/hr_holidays/i18n/de.po`
- `addons/hr_holidays/i18n/el.po`
- `addons/hr_holidays/i18n/es.po`
- `addons/hr_holidays/i18n/es_419.po`
- `addons/hr_holidays/i18n/es_CL.po`
- `addons/hr_holidays/i18n/et.po`
- `addons/hr_holidays/i18n/eu.po`
- `addons/hr_holidays/i18n/fa.po`
- `addons/hr_holidays/i18n/fi.po`
- `addons/hr_holidays/i18n/fo.po`
- `addons/hr_holidays/i18n/fr.po`
- `addons/hr_holidays/i18n/fr_BE.po`
- `addons/hr_holidays/i18n/fr_CA.po`
- `addons/hr_holidays/i18n/gl.po`
- `addons/hr_holidays/i18n/gu.po`
- `addons/hr_holidays/i18n/he.po`
- `addons/hr_holidays/i18n/hi.po`
- `addons/hr_holidays/i18n/hr.po`
- `addons/hr_holidays/i18n/hr_holidays.pot`
- `addons/hr_holidays/i18n/hu.po`
- `addons/hr_holidays/i18n/id.po`
- `addons/hr_holidays/i18n/is.po`
- `addons/hr_holidays/i18n/it.po`
- `addons/hr_holidays/i18n/ja.po`
- `addons/hr_holidays/i18n/ka.po`
- `addons/hr_holidays/i18n/kab.po`
- `addons/hr_holidays/i18n/km.po`
- `addons/hr_holidays/i18n/ko.po`
- `addons/hr_holidays/i18n/ku.po`
- `addons/hr_holidays/i18n/lb.po`
- `addons/hr_holidays/i18n/lo.po`
- `addons/hr_holidays/i18n/lt.po`
- `addons/hr_holidays/i18n/lv.po`
- `addons/hr_holidays/i18n/mk.po`
- `addons/hr_holidays/i18n/mn.po`
- `addons/hr_holidays/i18n/my.po`
- `addons/hr_holidays/i18n/nb.po`
- `addons/hr_holidays/i18n/nl.po`
- `addons/hr_holidays/i18n/pl.po`
- `addons/hr_holidays/i18n/pt.po`
- `addons/hr_holidays/i18n/pt_BR.po`
- `addons/hr_holidays/i18n/ro.po`
- `addons/hr_holidays/i18n/ru.po`
- `addons/hr_holidays/i18n/sk.po`
- `addons/hr_holidays/i18n/sl.po`
- `addons/hr_holidays/i18n/sq.po`
- `addons/hr_holidays/i18n/sr@latin.po`
- `addons/hr_holidays/i18n/sv.po`
- `addons/hr_holidays/i18n/th.po`
- `addons/hr_holidays/i18n/tr.po`
- `addons/hr_holidays/i18n/uk.po`
- `addons/hr_holidays/i18n/uz.po`
- `addons/hr_holidays/i18n/vi.po`
- `addons/hr_holidays/i18n/zh_CN.po`
- `addons/hr_holidays/i18n/zh_TW.po`
- `addons/hr_holidays/models/__init__.py`
- `addons/hr_holidays/models/calendar_event.py`
- `addons/hr_holidays/models/hr_department.py`
- `addons/hr_holidays/models/hr_employee.py`
- `addons/hr_holidays/models/hr_employee_departure.py`
- `addons/hr_holidays/models/hr_employee_public.py`
- `addons/hr_holidays/models/hr_leave.py`
- `addons/hr_holidays/models/hr_leave_accrual_plan.py`
- `addons/hr_holidays/models/hr_leave_accrual_plan_level.py`
- `addons/hr_holidays/models/hr_leave_allocation.py`
- `addons/hr_holidays/models/hr_leave_display_name_mixin.py`
- `addons/hr_holidays/models/hr_leave_mandatory_day.py`
- `addons/hr_holidays/models/hr_time_rule.py`
- `addons/hr_holidays/models/hr_time_rule_allocation_log.py`
- `addons/hr_holidays/models/hr_version.py`
- `addons/hr_holidays/models/hr_work_entry_type.py`
- `addons/hr_holidays/models/mail_activity_type.py`
- `addons/hr_holidays/models/mail_message_subtype.py`
- `addons/hr_holidays/models/res_company.py`
- `addons/hr_holidays/models/res_groups.py`
- `addons/hr_holidays/models/res_partner.py`
- `addons/hr_holidays/models/res_users.py`
- `addons/hr_holidays/models/resource_calendar.py`
- `addons/hr_holidays/models/resource_calendar_leaves.py`
- `addons/hr_holidays/models/resource_resource.py`
- `addons/hr_holidays/report/__init__.py`
- `addons/hr_holidays/report/holidays_summary_report.py`
- `addons/hr_holidays/report/hr_holidays_reports.xml`
- `addons/hr_holidays/report/hr_holidays_templates.xml`
- `addons/hr_holidays/report/hr_leave_employee_report.py`
- `addons/hr_holidays/report/hr_leave_employee_report_views.xml`
- `addons/hr_holidays/report/hr_leave_employee_type_report.py`
- `addons/hr_holidays/report/hr_leave_employee_type_report.xml`
- `addons/hr_holidays/report/hr_leave_report.py`
- `addons/hr_holidays/report/hr_leave_report_calendar.py`
- `addons/hr_holidays/report/hr_leave_report_calendar.xml`
- `addons/hr_holidays/report/hr_leave_reports.xml`
- `addons/hr_holidays/security/hr_holidays_security.xml`
- `addons/hr_holidays/security/ir.access.csv`
- `addons/hr_holidays/static/description/icon.png`
- `addons/hr_holidays/static/description/icon.svg`
- `addons/hr_holidays/static/description/icon_hi.png`
- `addons/hr_holidays/static/src/components/accrual_level/accrual_levels.js`
- `addons/hr_holidays/static/src/components/accrual_level/accrual_levels.scss`
- `addons/hr_holidays/static/src/components/accrual_level/accrual_levels.xml`
- `addons/hr_holidays/static/src/components/day_selection/day_selection.js`
- `addons/hr_holidays/static/src/components/hr_leave_chatter_patch/hr_leave_chatter_patch.js`
- `addons/hr_holidays/static/src/components/hr_presence_status/hr_presence_status.js`
- `addons/hr_holidays/static/src/components/selection_badge_with_filter/selection_badge_with_filter.js`
- `addons/hr_holidays/static/src/core/common/@types/models.d.ts`
- `addons/hr_holidays/static/src/core/common/chat_window_patch.js`
- `addons/hr_holidays/static/src/core/common/chat_window_patch.xml`
- `addons/hr_holidays/static/src/core/common/composer_patch.xml`
- `addons/hr_holidays/static/src/core/common/hr_employee_model_patch.js`
- `addons/hr_holidays/static/src/core/common/im_status_patch.js`
- `addons/hr_holidays/static/src/core/common/res_partner_model_patch.js`
- `addons/hr_holidays/static/src/core/common/res_users_model_patch.js`
- `addons/hr_holidays/static/src/core/web/activity_menu_patch.js`
- `addons/hr_holidays/static/src/core/web/avatar_card/avatar_card_patch.xml`
- `addons/hr_holidays/static/src/dashboard/time_off_card.dark.scss`
- `addons/hr_holidays/static/src/dashboard/time_off_card.js`
- `addons/hr_holidays/static/src/dashboard/time_off_card.scss`
- `addons/hr_holidays/static/src/dashboard/time_off_card.xml`
- `addons/hr_holidays/static/src/dashboard/time_off_dashboard.js`
- `addons/hr_holidays/static/src/dashboard/time_off_dashboard.scss`
- `addons/hr_holidays/static/src/dashboard/time_off_dashboard.xml`
- `addons/hr_holidays/static/src/discuss/core/common/channel_member_patch.xml`
- `addons/hr_holidays/static/src/discuss/core/public_web/discuss_command_palette_patch.xml`
- `addons/hr_holidays/static/src/discuss/core/public_web/discuss_content_patch.js`
- `addons/hr_holidays/static/src/discuss/core/public_web/discuss_content_patch.xml`
- `addons/hr_holidays/static/src/discuss/core/public_web/messaging_menu_item_patch.xml`
- `addons/hr_holidays/static/src/img/icons/Annual_Time_Off.svg`
- `addons/hr_holidays/static/src/img/icons/Compensatory_Time_Off.svg`
- `addons/hr_holidays/static/src/img/icons/Paid_Time_Off.svg`
- `addons/hr_holidays/static/src/img/icons/Parental_Time_Off.svg`
- `addons/hr_holidays/static/src/img/icons/Recovery_Bank_Holiday.svg`
- `addons/hr_holidays/static/src/img/icons/Sick_Time_Off.svg`
- `addons/hr_holidays/static/src/img/icons/Training_Time_Off.svg`
- `addons/hr_holidays/static/src/img/icons/Unpaid_Time_Off.svg`
- `addons/hr_holidays/static/src/leave_stats/leave_stats.js`
- `addons/hr_holidays/static/src/leave_stats/leave_stats.xml`
- `addons/hr_holidays/static/src/scss/time_off.scss`
- `addons/hr_holidays/static/src/search/hr_holidays_search_model.js`
- `addons/hr_holidays/static/src/tours/hr_holidays_tour.js`
- `addons/hr_holidays/static/src/utils.js`
- `addons/hr_holidays/static/src/views/calendar/calendar_controller.js`
- `addons/hr_holidays/static/src/views/calendar/calendar_controller.xml`
- `addons/hr_holidays/static/src/views/calendar/calendar_filter_panel/calendar_mobile_filter_panel.js`
- `addons/hr_holidays/static/src/views/calendar/calendar_filter_panel/calendar_mobile_filter_panel.xml`
- `addons/hr_holidays/static/src/views/calendar/calendar_model.js`
- `addons/hr_holidays/static/src/views/calendar/calendar_renderer.js`
- `addons/hr_holidays/static/src/views/calendar/calendar_renderer.scss`
- `addons/hr_holidays/static/src/views/calendar/calendar_renderer.xml`
- `addons/hr_holidays/static/src/views/calendar/calendar_side_panel/calendar_side_panel.js`
- `addons/hr_holidays/static/src/views/calendar/calendar_side_panel/calendar_side_panel.xml`
- `addons/hr_holidays/static/src/views/calendar/calendar_view.js`
- `addons/hr_holidays/static/src/views/calendar/common/calendar_common_renderer.js`
- `addons/hr_holidays/static/src/views/calendar/filter_section/calendar_filter_section.dark.scss`
- `addons/hr_holidays/static/src/views/calendar/filter_section/calendar_filter_section.scss`
- `addons/hr_holidays/static/src/views/calendar/time_off_report_calendar_controller.js`
- `addons/hr_holidays/static/src/views/calendar/time_off_report_calendar_view.js`
- `addons/hr_holidays/static/src/views/calendar/utils.js`
- `addons/hr_holidays/static/src/views/calendar/year/calendar_year_popover.js`
- `addons/hr_holidays/static/src/views/calendar/year/calendar_year_popover.xml`
- `addons/hr_holidays/static/src/views/calendar/year/calendar_year_renderer.js`
- `addons/hr_holidays/static/src/views/graph/hr_holidays_graph_controller.xml`
- `addons/hr_holidays/static/src/views/graph/hr_holidays_graph_model.js`
- `addons/hr_holidays/static/src/views/graph/hr_holidays_graph_renderer.js`
- `addons/hr_holidays/static/src/views/graph/hr_holidays_graph_view.js`
- `addons/hr_holidays/static/src/views/hooks.js`
- `addons/hr_holidays/static/src/views/hr_leave_export.js`
- `addons/hr_holidays/static/src/views/kanban/kanban_controller.js`
- `addons/hr_holidays/static/src/views/kanban/kanban_renderer.js`
- `addons/hr_holidays/static/src/views/kanban/kanban_renderer.xml`
- `addons/hr_holidays/static/src/views/kanban/kanban_view.js`
- `addons/hr_holidays/static/src/views/list/holidays_list_controller.js`
- `addons/hr_holidays/static/src/views/list/holidays_list_controller.xml`
- `addons/hr_holidays/static/src/views/many2one_no_save.js`
- `addons/hr_holidays/static/src/views/time_off_plugin.js`
- `addons/hr_holidays/static/src/views/view_dialog/allocation_form_view_dialog.js`
- `addons/hr_holidays/static/src/views/view_dialog/allocation_form_view_dialog.xml`
- `addons/hr_holidays/static/src/views/view_dialog/form_view_dialog.js`
- `addons/hr_holidays/static/src/views/view_dialog/form_view_dialog.xml`
- `addons/hr_holidays/static/src/webclient/share_target/hr_holiday_share_target_item.js`
- `addons/hr_holidays/static/tests/accrual_levels_widget.test.js`
- `addons/hr_holidays/static/tests/calendar_year.test.js`
- `addons/hr_holidays/static/tests/channel_member_list.test.js`
- `addons/hr_holidays/static/tests/chat_window_patch.test.js`
- `addons/hr_holidays/static/tests/dashboard_card_hour_format.test.js`
- `addons/hr_holidays/static/tests/discuss_content_patch.test.js`
- `addons/hr_holidays/static/tests/hr_holidays_test_helpers.js`
- `addons/hr_holidays/static/tests/hr_presence_status.test.js`
- `addons/hr_holidays/static/tests/im_status.test.js`
- `addons/hr_holidays/static/tests/im_status_patch.test.js`
- `addons/hr_holidays/static/tests/leave_card.test.js`
- `addons/hr_holidays/static/tests/leave_stats.test.js`
- `addons/hr_holidays/static/tests/mock_server/mock_models/hr_department.js`
- `addons/hr_holidays/static/tests/mock_server/mock_models/hr_employee.js`
- `addons/hr_holidays/static/tests/mock_server/mock_models/hr_leave.js`
- `addons/hr_holidays/static/tests/mock_server/mock_models/hr_leave_accrual_level.js`
- `addons/hr_holidays/static/tests/mock_server/mock_models/hr_leave_accrual_plan.js`
- Additional source files not expanded in this page: 80; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
