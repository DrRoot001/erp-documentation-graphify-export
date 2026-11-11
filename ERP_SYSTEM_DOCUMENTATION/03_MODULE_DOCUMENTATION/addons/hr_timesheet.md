# Module: hr_timesheet

- **Module ID:** MOD-102
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_timesheet`
- **Manifest:** `addons/hr_timesheet/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Services/Timesheets`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Track employee time on tasks

**Manifest description:**

This module implements a timesheet system.
==========================================

Each employee can encode and track their time spent on the different projects.

Lots of reporting on time and employee tracking are provided.

It is completely integrated with the cost accounting module. It allows you to set
up a management by affair.

**Scope evidence:** The module contains 164 files, including 38 Python, 22 XML, and 21 JavaScript/TypeScript files. The manifest declares dependencies: `hr`, `analytic`, `project`, `uom`.

## 2. Module structure

- Model/business logic files: 18
- Controller/API files: 3
- XML/data/view/template files: 22
- Browser asset files: 21
- Security files: 2
- Test files: 12
- Scheduled/automation evidence files: 2
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr_timesheet/security/hr_timesheet_security.xml`, `addons/hr_timesheet/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 18 model declarations, 215 methods, 3 constraint handlers, 1 onchange handlers, and 29 dependency declarations.
- **Evidence:** `addons/hr_timesheet/models/hr_employee_departure.py:5`, `addons/hr_timesheet/models/uom_uom.py:7`, `addons/hr_timesheet/models/res_config_settings.py:7`, `addons/hr_timesheet/models/hr_employee_public.py:6`, `addons/hr_timesheet/models/account_analytic_line.py:13`, `addons/hr_timesheet/models/project_update.py:6`, `addons/hr_timesheet/models/ir_http.py:7`, `addons/hr_timesheet/models/project_task.py:31`, `addons/hr_timesheet/models/project_project.py:10`, `addons/hr_timesheet/models/project_collaborator.py:7`, `addons/hr_timesheet/models/analytic_applicability.py:6`, `addons/hr_timesheet/models/account_analytic_line_calendar_employee.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 1 route declarations.
- **Evidence:** `addons/hr_timesheet/controllers/portal.py:68`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 22 XML files and 21 JavaScript/TypeScript files; static XML analysis found 502 record/template/menu identifiers.
- **Evidence:** `addons/hr_timesheet/security/hr_timesheet_security.xml:3`, `addons/hr_timesheet/security/hr_timesheet_security.xml:9`, `addons/hr_timesheet/security/hr_timesheet_security.xml:18`, `addons/hr_timesheet/security/hr_timesheet_security.xml:26`, `addons/hr_timesheet/security/hr_timesheet_security.xml:35`, `addons/hr_timesheet/security/hr_timesheet_security.xml:48`, `addons/hr_timesheet/security/hr_timesheet_security.xml:52`, `addons/hr_timesheet/report/project_report_view.xml:4`, `addons/hr_timesheet/report/project_report_view.xml:19`, `addons/hr_timesheet/report/report_timesheet_templates.xml:188`, `addons/hr_timesheet/report/report_timesheet_templates.xml:202`, `addons/hr_timesheet/report/report_timesheet_templates.xml:211`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/hr_timesheet/security/hr_timesheet_security.xml`, `addons/hr_timesheet/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/hr_timesheet/report/report_timesheet_templates.xml`, `addons/hr_timesheet/views/hr_employee_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/hr_timesheet/report/report_timesheet_templates.xml`, `addons/hr_timesheet/tests/test_report_timesheet.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 12 test files are present.
- **Evidence:** `addons/hr_timesheet/tests/test_project_sharing.py`, `addons/hr_timesheet/tests/test_task_templates.py`, `addons/hr_timesheet/tests/test_task_analysis.py`, `addons/hr_timesheet/tests/test_employee_delete_wizard.py`, `addons/hr_timesheet/tests/test_project_task_quick_create.py`, `addons/hr_timesheet/tests/test_project_project.py`, `addons/hr_timesheet/tests/test_portal_timesheet.py`, `addons/hr_timesheet/tests/test_timesheet.py`, `addons/hr_timesheet/tests/test_timesheet_import_template.py`, `addons/hr_timesheet/tests/__init__.py`, `addons/hr_timesheet/tests/test_report_timesheet.py`, `addons/hr_timesheet/tests/test_project_template.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 22; representative identifiers: `res_groups_privilege_timesheets`, `group_hr_timesheet_user`, `group_hr_timesheet_approver`, `group_timesheet_manager`, `timesheet_line_rule_portal_user`, `project.account_analytic_line_rule_manager`, `project.group_project_manager`, `view_task_project_user_graph_inherited`, `view_task_project_user_pivot_inherited`, `timesheet_report`, `timesheet_report_task`, `action_server_print_task_timesheets`, `timesheet_report_project`, `action_server_print_project_timesheets`, `timesheet_report_task_timesheets`, `hr_timesheet.timesheet_table`, `hr_timesheet.timesheet_project_task_page`, `timesheet_report_subtask`, `report_timesheet`, `report_timesheet_task`
- Menus: 11; representative evidence: `addons/hr_timesheet/views/hr_timesheet_menus.xml:3`, `addons/hr_timesheet/views/hr_timesheet_menus.xml:9`, `addons/hr_timesheet/views/hr_timesheet_menus.xml:14`, `addons/hr_timesheet/views/hr_timesheet_menus.xml:19`, `addons/hr_timesheet/views/hr_timesheet_menus.xml:24`, `addons/hr_timesheet/views/hr_timesheet_menus.xml:30`, `addons/hr_timesheet/views/hr_timesheet_menus.xml:35`, `addons/hr_timesheet/views/hr_timesheet_menus.xml:39`, `addons/hr_timesheet/views/hr_timesheet_menus.xml:45`, `addons/hr_timesheet/views/hr_timesheet_menus.xml:50`, `addons/hr_timesheet/views/hr_timesheet_menus.xml:57`
- Templates: 14; representative evidence: `addons/hr_timesheet/report/report_timesheet_templates.xml:3`, `addons/hr_timesheet/report/report_timesheet_templates.xml:76`, `addons/hr_timesheet/report/report_timesheet_templates.xml:117`, `addons/hr_timesheet/report/report_timesheet_templates.xml:133`, `addons/hr_timesheet/report/report_timesheet_templates.xml:161`, `addons/hr_timesheet/report/report_timesheet_templates.xml:198`, `addons/hr_timesheet/report/report_timesheet_templates.xml:224`, `addons/hr_timesheet/views/project_task_portal_templates.xml:4`, `addons/hr_timesheet/views/project_task_portal_templates.xml:37`, `addons/hr_timesheet/views/project_task_portal_templates.xml:46`, `addons/hr_timesheet/views/hr_timesheet_portal_templates.xml:3`, `addons/hr_timesheet/views/hr_timesheet_portal_templates.xml:11`
- View/action field declarations: 158; representative evidence: `addons/hr_timesheet/report/project_report_view.xml:6`, `addons/hr_timesheet/report/project_report_view.xml:8`, `addons/hr_timesheet/report/project_report_view.xml:21`, `addons/hr_timesheet/report/project_report_view.xml:23`, `addons/hr_timesheet/report/report_timesheet_templates.xml:190`, `addons/hr_timesheet/report/report_timesheet_templates.xml:204`, `addons/hr_timesheet/report/report_timesheet_templates.xml:231`, `addons/hr_timesheet/report/report_timesheet_templates.xml:252`, `addons/hr_timesheet/report/hr_timesheet_report_view.xml:6`, `addons/hr_timesheet/report/hr_timesheet_report_view.xml:7`, `addons/hr_timesheet/report/hr_timesheet_report_view.xml:25`, `addons/hr_timesheet/report/hr_timesheet_report_view.xml:26`
- Browser assets: 21; representative files: `addons/hr_timesheet/static/tests/timesheet_uom_no_toggle.test.js`, `addons/hr_timesheet/static/tests/timesheet_graph.test.js`, `addons/hr_timesheet/static/tests/task_with_hours.test.js`, `addons/hr_timesheet/static/tests/timesheet_uom.test.js`, `addons/hr_timesheet/static/tests/hr_timesheet_models.js`, `addons/hr_timesheet/static/src/services/timesheet_uom_service.js`, `addons/hr_timesheet/static/src/views/graph_model_patch.js`, `addons/hr_timesheet/static/src/components/progress_bar/project_task_progress_bar_field.js`, `addons/hr_timesheet/static/src/components/timesheet_duration_uom/timesheet_duration_uom.js`, `addons/hr_timesheet/static/src/components/time_hour_field/time_hour_field.js`, `addons/hr_timesheet/static/src/components/task_with_hours/task_with_hours.js`, `addons/hr_timesheet/static/src/components/timesheet_uom/timesheet_uom.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_timesheet/__manifest__.py`
- **HTTP entry points:** `addons/hr_timesheet/controllers/portal.py:68`
- **Scheduled entry points:** `addons/hr_timesheet/report/report_timesheet_templates.xml`, `addons/hr_timesheet/views/hr_employee_views.xml`
- **Report entry points:** `addons/hr_timesheet/report/report_timesheet_templates.xml`, `addons/hr_timesheet/tests/test_report_timesheet.py`

## 7. Database interactions

- Model declarations: 18
- Representative model evidence: inherits `hr.employee.departure` (addons/hr_timesheet/models/hr_employee_departure.py:5); inherits `uom.uom` (addons/hr_timesheet/models/uom_uom.py:7); inherits `res.config.settings` (addons/hr_timesheet/models/res_config_settings.py:7); inherits `hr.employee.public` (addons/hr_timesheet/models/hr_employee_public.py:6); inherits `account.analytic.line` (addons/hr_timesheet/models/account_analytic_line.py:13); inherits `project.update` (addons/hr_timesheet/models/project_update.py:6); inherits `ir.http` (addons/hr_timesheet/models/ir_http.py:7); inherits `project.task` (addons/hr_timesheet/models/project_task.py:31); inherits `project.project` (addons/hr_timesheet/models/project_project.py:10); inherits `project.collaborator` (addons/hr_timesheet/models/project_collaborator.py:7); inherits `account.analytic.applicability` (addons/hr_timesheet/models/analytic_applicability.py:6); `account.analytic.line.calendar.employee` (addons/hr_timesheet/models/account_analytic_line_calendar_employee.py:4); inherits `hr.employee` (addons/hr_timesheet/models/hr_employee.py:10); inherits `ir.ui.menu` (addons/hr_timesheet/models/ir_ui_menu.py:6); inherits `res.company` (addons/hr_timesheet/models/res_company.py:8); inherits `report.project.task.user` (addons/hr_timesheet/report/project_report.py:7); `timesheets.analysis.report` (addons/hr_timesheet/report/timesheets_analysis_report.py:8); `hr.employee.delete.wizard` (addons/hr_timesheet/wizard/hr_employee_delete_wizard.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 1
- Route evidence: `addons/hr_timesheet/controllers/portal.py:68`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr`, `analytic`, `project`, `uom`
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

- `addons/hr_timesheet/__init__.py`
- `addons/hr_timesheet/__manifest__.py`
- `addons/hr_timesheet/controllers/__init__.py`
- `addons/hr_timesheet/controllers/portal.py`
- `addons/hr_timesheet/controllers/project.py`
- `addons/hr_timesheet/data/hr_timesheet_data.xml`
- `addons/hr_timesheet/data/hr_timesheet_demo.xml`
- `addons/hr_timesheet/data/portal_entry_data.xml`
- `addons/hr_timesheet/i18n/af.po`
- `addons/hr_timesheet/i18n/am.po`
- `addons/hr_timesheet/i18n/ar.po`
- `addons/hr_timesheet/i18n/az.po`
- `addons/hr_timesheet/i18n/bg.po`
- `addons/hr_timesheet/i18n/bs.po`
- `addons/hr_timesheet/i18n/ca.po`
- `addons/hr_timesheet/i18n/cs.po`
- `addons/hr_timesheet/i18n/da.po`
- `addons/hr_timesheet/i18n/de.po`
- `addons/hr_timesheet/i18n/el.po`
- `addons/hr_timesheet/i18n/es.po`
- `addons/hr_timesheet/i18n/es_419.po`
- `addons/hr_timesheet/i18n/es_CL.po`
- `addons/hr_timesheet/i18n/et.po`
- `addons/hr_timesheet/i18n/eu.po`
- `addons/hr_timesheet/i18n/fa.po`
- `addons/hr_timesheet/i18n/fi.po`
- `addons/hr_timesheet/i18n/fo.po`
- `addons/hr_timesheet/i18n/fr.po`
- `addons/hr_timesheet/i18n/fr_BE.po`
- `addons/hr_timesheet/i18n/fr_CA.po`
- `addons/hr_timesheet/i18n/gl.po`
- `addons/hr_timesheet/i18n/gu.po`
- `addons/hr_timesheet/i18n/he.po`
- `addons/hr_timesheet/i18n/hi.po`
- `addons/hr_timesheet/i18n/hr.po`
- `addons/hr_timesheet/i18n/hr_timesheet.pot`
- `addons/hr_timesheet/i18n/hu.po`
- `addons/hr_timesheet/i18n/hy.po`
- `addons/hr_timesheet/i18n/id.po`
- `addons/hr_timesheet/i18n/is.po`
- `addons/hr_timesheet/i18n/it.po`
- `addons/hr_timesheet/i18n/ja.po`
- `addons/hr_timesheet/i18n/ka.po`
- `addons/hr_timesheet/i18n/kab.po`
- `addons/hr_timesheet/i18n/kk.po`
- `addons/hr_timesheet/i18n/km.po`
- `addons/hr_timesheet/i18n/ko.po`
- `addons/hr_timesheet/i18n/ku.po`
- `addons/hr_timesheet/i18n/lb.po`
- `addons/hr_timesheet/i18n/lo.po`
- `addons/hr_timesheet/i18n/lt.po`
- `addons/hr_timesheet/i18n/lv.po`
- `addons/hr_timesheet/i18n/mk.po`
- `addons/hr_timesheet/i18n/mn.po`
- `addons/hr_timesheet/i18n/my.po`
- `addons/hr_timesheet/i18n/nb.po`
- `addons/hr_timesheet/i18n/nl.po`
- `addons/hr_timesheet/i18n/pl.po`
- `addons/hr_timesheet/i18n/pt.po`
- `addons/hr_timesheet/i18n/pt_BR.po`
- `addons/hr_timesheet/i18n/ro.po`
- `addons/hr_timesheet/i18n/ru.po`
- `addons/hr_timesheet/i18n/sk.po`
- `addons/hr_timesheet/i18n/sl.po`
- `addons/hr_timesheet/i18n/sq.po`
- `addons/hr_timesheet/i18n/sr@latin.po`
- `addons/hr_timesheet/i18n/sv.po`
- `addons/hr_timesheet/i18n/ta.po`
- `addons/hr_timesheet/i18n/te.po`
- `addons/hr_timesheet/i18n/th.po`
- `addons/hr_timesheet/i18n/tr.po`
- `addons/hr_timesheet/i18n/uk.po`
- `addons/hr_timesheet/i18n/uz.po`
- `addons/hr_timesheet/i18n/vi.po`
- `addons/hr_timesheet/i18n/zh_CN.po`
- `addons/hr_timesheet/i18n/zh_TW.po`
- `addons/hr_timesheet/models/__init__.py`
- `addons/hr_timesheet/models/account_analytic_line.py`
- `addons/hr_timesheet/models/account_analytic_line_calendar_employee.py`
- `addons/hr_timesheet/models/analytic_applicability.py`
- `addons/hr_timesheet/models/hr_employee.py`
- `addons/hr_timesheet/models/hr_employee_departure.py`
- `addons/hr_timesheet/models/hr_employee_public.py`
- `addons/hr_timesheet/models/ir_http.py`
- `addons/hr_timesheet/models/ir_ui_menu.py`
- `addons/hr_timesheet/models/project_collaborator.py`
- `addons/hr_timesheet/models/project_project.py`
- `addons/hr_timesheet/models/project_task.py`
- `addons/hr_timesheet/models/project_update.py`
- `addons/hr_timesheet/models/res_company.py`
- `addons/hr_timesheet/models/res_config_settings.py`
- `addons/hr_timesheet/models/uom_uom.py`
- `addons/hr_timesheet/report/__init__.py`
- `addons/hr_timesheet/report/hr_timesheet_report_view.xml`
- `addons/hr_timesheet/report/project_report.py`
- `addons/hr_timesheet/report/project_report_view.xml`
- `addons/hr_timesheet/report/report_timesheet_templates.xml`
- `addons/hr_timesheet/report/timesheets_analysis_report.py`
- `addons/hr_timesheet/security/hr_timesheet_security.xml`
- `addons/hr_timesheet/security/ir.access.csv`
- `addons/hr_timesheet/static/description/icon.png`
- `addons/hr_timesheet/static/description/icon.svg`
- `addons/hr_timesheet/static/description/icon_hi.png`
- `addons/hr_timesheet/static/description/icon_timesheet.png`
- `addons/hr_timesheet/static/img/digest_tip_timesheets_hotkeys.gif`
- `addons/hr_timesheet/static/img/employee7-image.jpg`
- `addons/hr_timesheet/static/img/employee_phu-image.jpg`
- `addons/hr_timesheet/static/img/product_product_consultant-image.jpg`
- `addons/hr_timesheet/static/img/timesheet.svg`
- `addons/hr_timesheet/static/src/components/progress_bar/project_task_progress_bar_field.js`
- `addons/hr_timesheet/static/src/components/task_with_hours/task_with_hours.js`
- `addons/hr_timesheet/static/src/components/task_with_hours/task_with_hours.xml`
- `addons/hr_timesheet/static/src/components/time_hour_field/time_hour_field.js`
- `addons/hr_timesheet/static/src/components/timesheet_duration_uom/timesheet_duration_uom.js`
- `addons/hr_timesheet/static/src/components/timesheet_duration_uom/timesheet_duration_uom.scss`
- `addons/hr_timesheet/static/src/components/timesheet_uom/timesheet_uom.js`
- `addons/hr_timesheet/static/src/components/timesheet_uom/timesheet_uom.scss`
- `addons/hr_timesheet/static/src/components/timesheet_uom/timesheet_uom.xml`
- `addons/hr_timesheet/static/src/components/timesheet_uom_no_toggle/timesheet_uom_no_toggle.js`
- `addons/hr_timesheet/static/src/scss/timesheet_kanban.scss`
- `addons/hr_timesheet/static/src/scss/timesheets_task_form.scss`
- `addons/hr_timesheet/static/src/services/timesheet_uom_service.js`
- `addons/hr_timesheet/static/src/views/graph_model_patch.js`
- `addons/hr_timesheet/static/src/views/project_task_analysis_graph/project_task_analysis_graph_model.js`
- `addons/hr_timesheet/static/src/views/project_task_graph/project_task_graph_model.js`
- `addons/hr_timesheet/static/src/views/timesheet_calendar/timesheet_calendar_model.js`
- `addons/hr_timesheet/static/src/views/timesheet_calendar/timesheet_calendar_view.js`
- `addons/hr_timesheet/static/src/views/timesheet_calendar_my_timesheets/timesheet_calendar_my_timesheets_model.js`
- `addons/hr_timesheet/static/src/views/timesheet_calendar_my_timesheets/timesheet_calendar_my_timesheets_view.js`
- `addons/hr_timesheet/static/src/views/timesheet_graph/timesheet_graph_model.js`
- `addons/hr_timesheet/static/src/views/timesheet_graph/timesheet_graph_view.js`
- `addons/hr_timesheet/static/tests/hr_timesheet_models.js`
- `addons/hr_timesheet/static/tests/task_with_hours.test.js`
- `addons/hr_timesheet/static/tests/timesheet_graph.test.js`
- `addons/hr_timesheet/static/tests/timesheet_uom.test.js`
- `addons/hr_timesheet/static/tests/timesheet_uom_no_toggle.test.js`
- `addons/hr_timesheet/static/xls/timesheets_import_template.xlsx`
- `addons/hr_timesheet/tests/__init__.py`
- `addons/hr_timesheet/tests/test_employee_delete_wizard.py`
- `addons/hr_timesheet/tests/test_portal_timesheet.py`
- `addons/hr_timesheet/tests/test_project_project.py`
- `addons/hr_timesheet/tests/test_project_sharing.py`
- `addons/hr_timesheet/tests/test_project_task_quick_create.py`
- `addons/hr_timesheet/tests/test_project_template.py`
- `addons/hr_timesheet/tests/test_report_timesheet.py`
- `addons/hr_timesheet/tests/test_task_analysis.py`
- `addons/hr_timesheet/tests/test_task_templates.py`
- `addons/hr_timesheet/tests/test_timesheet.py`
- `addons/hr_timesheet/tests/test_timesheet_import_template.py`
- `addons/hr_timesheet/views/account_analytic_line_views.xml`
- `addons/hr_timesheet/views/hr_department_views.xml`
- `addons/hr_timesheet/views/hr_employee_public_views.xml`
- `addons/hr_timesheet/views/hr_employee_views.xml`
- `addons/hr_timesheet/views/hr_timesheet_menus.xml`
- `addons/hr_timesheet/views/hr_timesheet_portal_templates.xml`
- `addons/hr_timesheet/views/project_project_views.xml`
- `addons/hr_timesheet/views/project_task_portal_templates.xml`
- `addons/hr_timesheet/views/project_task_sharing_views.xml`
- `addons/hr_timesheet/views/project_task_views.xml`
- `addons/hr_timesheet/views/project_update_views.xml`
- `addons/hr_timesheet/views/res_config_settings_views.xml`
- `addons/hr_timesheet/wizard/__init__.py`
- `addons/hr_timesheet/wizard/hr_employee_delete_wizard.py`
- `addons/hr_timesheet/wizard/hr_employee_delete_wizard_views.xml`
