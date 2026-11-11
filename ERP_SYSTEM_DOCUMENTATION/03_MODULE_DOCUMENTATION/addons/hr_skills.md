# Module: hr_skills

- **Module ID:** MOD-098
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_skills`
- **Manifest:** `addons/hr_skills/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Human Resources/Employees`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Manage skills, knowledge and resume of your employees

**Manifest description:**

Skills and Resume for HR
========================

This module introduces skills and resume management for employees.

**Scope evidence:** The module contains 139 files, including 29 Python, 27 XML, and 21 JavaScript/TypeScript files. The manifest declares dependencies: `hr`.

## 2. Module structure

- Model/business logic files: 16
- Controller/API files: 2
- XML/data/view/template files: 27
- Browser asset files: 21
- Security files: 1
- Test files: 6
- Scheduled/automation evidence files: 4
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr_skills/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 16 model declarations, 97 methods, 5 constraint handlers, 4 onchange handlers, and 13 dependency declarations.
- **Evidence:** `addons/hr_skills/models/hr_employee_skill.py:6`, `addons/hr_skills/models/hr_resume_line_type.py:7`, `addons/hr_skills/models/hr_skill_type.py:9`, `addons/hr_skills/models/hr_job_skill.py:6`, `addons/hr_skills/models/hr_individual_skill_mixin.py:11`, `addons/hr_skills/models/hr_skill.py:7`, `addons/hr_skills/models/hr_employee_public.py:6`, `addons/hr_skills/models/resource_resource.py:6`, `addons/hr_skills/models/hr_resume_line.py:8`, `addons/hr_skills/models/hr_job.py:5`, `addons/hr_skills/models/hr_employee.py:15`, `addons/hr_skills/models/hr_skill_level.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/hr_skills/controllers/main.py:14`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 27 XML files and 21 JavaScript/TypeScript files; static XML analysis found 258 record/template/menu identifiers.
- **Evidence:** `addons/hr_skills/report/hr_employee_skill_report_views.xml:3`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:16`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:28`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:41`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:62`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:80`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:88`, `addons/hr_skills/report/hr_employee_cv_report.xml:3`, `addons/hr_skills/report/hr_employee_skill_history_report_views.xml:3`, `addons/hr_skills/report/hr_employee_skill_history_report_views.xml:14`, `addons/hr_skills/wizard/hr_employee_cv_wizard_views.xml:3`, `addons/hr_skills/wizard/hr_employee_cv_wizard_views.xml:31`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/hr_skills/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 4 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/hr_skills/__manifest__.py`, `addons/hr_skills/data/ir_actions_server_data.xml`, `addons/hr_skills/data/ir_cron_data.xml`, `addons/hr_skills/views/hr_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/hr_skills/controllers/main.py`, `addons/hr_skills/report/hr_employee_cv_report.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 6 test files are present.
- **Evidence:** `addons/hr_skills/tests/test_employee_skill.py`, `addons/hr_skills/tests/test_resource.py`, `addons/hr_skills/tests/test_report.py`, `addons/hr_skills/tests/test_ui.py`, `addons/hr_skills/tests/__init__.py`, `addons/hr_skills/tests/test_certification_activities.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 27; representative identifiers: `hr_employee_skill_report_view_pivot`, `hr_employee_skill_report_view_graph`, `hr_employee_skill_report_view_list`, `hr_employee_skill_report_view_search`, `hr_employee_skill_report_action`, `action_hr_employee_skill_log_department`, `Skills Inventory`, `action_report_employee_cv`, `hr_employee_skill_history_report_view_graph`, `hr_employee_skill_history_report_view_search`, `hr_employee_cv_wizard_view_form`, `action_hr_employee_cv_wizard`, `action_open_skills_log_department`, `action_print_employees_cv`, `resume_type_experience`, `resume_type_education`, `resume_type_training`, `hr_skill_type_lang`, `hr_skill_type_softskill`, `hr_skill_french`
- Menus: 7; representative evidence: `addons/hr_skills/report/hr_employee_skill_report_views.xml:88`, `addons/hr_skills/views/hr_views.xml:327`, `addons/hr_skills/views/hr_views.xml:334`, `addons/hr_skills/views/hr_views.xml:601`, `addons/hr_skills/views/hr_views.xml:609`, `addons/hr_skills/views/hr_views.xml:616`, `addons/hr_skills/views/hr_views.xml:623`
- Templates: 4; representative evidence: `addons/hr_skills/views/hr_employee_cv_templates.xml:3`, `addons/hr_skills/views/hr_employee_cv_templates.xml:17`, `addons/hr_skills/views/hr_employee_cv_templates.xml:32`, `addons/hr_skills/views/hr_employee_cv_templates.xml:63`
- View/action field declarations: 81; representative evidence: `addons/hr_skills/report/hr_employee_skill_report_views.xml:4`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:5`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:17`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:18`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:29`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:30`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:42`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:43`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:64`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:66`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:82`, `addons/hr_skills/report/hr_employee_skill_report_views.xml:83`
- Browser assets: 21; representative files: `addons/hr_skills/static/tests/many2one_avatar_employee.test.js`, `addons/hr_skills/static/tests/hr_skills_test_helpers.js`, `addons/hr_skills/static/src/views/skills_list_renderer.js`, `addons/hr_skills/static/src/views/skills_graph.js`, `addons/hr_skills/static/src/components/internal_resume_lines/internal_resume_one2many.js`, `addons/hr_skills/static/src/fields/formatted_date/formatted_date.js`, `addons/hr_skills/static/src/fields/one2many_tags_skills/one2many_tags_skills.js`, `addons/hr_skills/static/src/fields/boolean_toggle_load/boolean_toggle_load.js`, `addons/hr_skills/static/src/fields/resume_one2many/resume_one2many.js`, `addons/hr_skills/static/src/fields/many2many_tags_skills/many2many_tags_skills.js`, `addons/hr_skills/static/src/fields/skills_one2many/skills_one2many.js`, `addons/hr_skills/static/src/core/common/hr_employee_model_patch.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_skills/__manifest__.py`
- **HTTP entry points:** `addons/hr_skills/controllers/main.py:14`
- **Scheduled entry points:** `addons/hr_skills/__manifest__.py`, `addons/hr_skills/data/ir_actions_server_data.xml`, `addons/hr_skills/data/ir_cron_data.xml`, `addons/hr_skills/views/hr_views.xml`
- **Report entry points:** `addons/hr_skills/controllers/main.py`, `addons/hr_skills/report/hr_employee_cv_report.xml`

## 7. Database interactions

- Model declarations: 16
- Representative model evidence: `hr.employee.skill` (addons/hr_skills/models/hr_employee_skill.py:6); `hr.resume.line.type` (addons/hr_skills/models/hr_resume_line_type.py:7); `hr.skill.type` (addons/hr_skills/models/hr_skill_type.py:9); `hr.job.skill` (addons/hr_skills/models/hr_job_skill.py:6); `hr.individual.skill.mixin` (addons/hr_skills/models/hr_individual_skill_mixin.py:11); `hr.skill` (addons/hr_skills/models/hr_skill.py:7); inherits `hr.employee.public` (addons/hr_skills/models/hr_employee_public.py:6); inherits `resource.resource` (addons/hr_skills/models/resource_resource.py:6); `hr.resume.line` (addons/hr_skills/models/hr_resume_line.py:8); inherits `hr.job` (addons/hr_skills/models/hr_job.py:5); inherits `hr.employee` (addons/hr_skills/models/hr_employee.py:15); `hr.skill.level` (addons/hr_skills/models/hr_skill_level.py:7); `hr.employee.skill.history.report` (addons/hr_skills/report/hr_employee_skill_history_report.py:6); `report.hr_skills.report_employee_cv` (addons/hr_skills/report/hr_employee_cv_report.py:8); `hr.employee.skill.report` (addons/hr_skills/report/hr_employee_skill_report.py:6); `hr.employee.cv.wizard` (addons/hr_skills/wizard/hr_employee_cv_wizard.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/hr_skills/controllers/main.py:14`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr`
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

- `addons/hr_skills/__init__.py`
- `addons/hr_skills/__manifest__.py`
- `addons/hr_skills/controllers/__init__.py`
- `addons/hr_skills/controllers/main.py`
- `addons/hr_skills/data/hr.employee.skill.csv`
- `addons/hr_skills/data/hr.job.skill.csv`
- `addons/hr_skills/data/hr.resume.line.csv`
- `addons/hr_skills/data/hr_employee_skill_demo.xml`
- `addons/hr_skills/data/hr_job_skill_demo.xml`
- `addons/hr_skills/data/hr_resume_data.xml`
- `addons/hr_skills/data/hr_resume_demo.xml`
- `addons/hr_skills/data/hr_skill_data.xml`
- `addons/hr_skills/data/hr_skill_demo.xml`
- `addons/hr_skills/data/ir_actions_server_data.xml`
- `addons/hr_skills/data/ir_cron_data.xml`
- `addons/hr_skills/data/report_paperformat.xml`
- `addons/hr_skills/data/scenarios/hr_skills_scenario.xml`
- `addons/hr_skills/i18n/ar.po`
- `addons/hr_skills/i18n/az.po`
- `addons/hr_skills/i18n/bg.po`
- `addons/hr_skills/i18n/bs.po`
- `addons/hr_skills/i18n/ca.po`
- `addons/hr_skills/i18n/cs.po`
- `addons/hr_skills/i18n/da.po`
- `addons/hr_skills/i18n/de.po`
- `addons/hr_skills/i18n/el.po`
- `addons/hr_skills/i18n/es.po`
- `addons/hr_skills/i18n/es_419.po`
- `addons/hr_skills/i18n/et.po`
- `addons/hr_skills/i18n/fa.po`
- `addons/hr_skills/i18n/fi.po`
- `addons/hr_skills/i18n/fr.po`
- `addons/hr_skills/i18n/he.po`
- `addons/hr_skills/i18n/hi.po`
- `addons/hr_skills/i18n/hr.po`
- `addons/hr_skills/i18n/hr_skills.pot`
- `addons/hr_skills/i18n/hu.po`
- `addons/hr_skills/i18n/id.po`
- `addons/hr_skills/i18n/it.po`
- `addons/hr_skills/i18n/ja.po`
- `addons/hr_skills/i18n/kab.po`
- `addons/hr_skills/i18n/ko.po`
- `addons/hr_skills/i18n/ku.po`
- `addons/hr_skills/i18n/lo.po`
- `addons/hr_skills/i18n/lt.po`
- `addons/hr_skills/i18n/lv.po`
- `addons/hr_skills/i18n/mn.po`
- `addons/hr_skills/i18n/my.po`
- `addons/hr_skills/i18n/nb.po`
- `addons/hr_skills/i18n/nl.po`
- `addons/hr_skills/i18n/pl.po`
- `addons/hr_skills/i18n/pt.po`
- `addons/hr_skills/i18n/pt_BR.po`
- `addons/hr_skills/i18n/ro.po`
- `addons/hr_skills/i18n/ru.po`
- `addons/hr_skills/i18n/sk.po`
- `addons/hr_skills/i18n/sl.po`
- `addons/hr_skills/i18n/sr@latin.po`
- `addons/hr_skills/i18n/sv.po`
- `addons/hr_skills/i18n/th.po`
- `addons/hr_skills/i18n/tr.po`
- `addons/hr_skills/i18n/uk.po`
- `addons/hr_skills/i18n/uz.po`
- `addons/hr_skills/i18n/vi.po`
- `addons/hr_skills/i18n/zh_CN.po`
- `addons/hr_skills/i18n/zh_TW.po`
- `addons/hr_skills/models/__init__.py`
- `addons/hr_skills/models/hr_employee.py`
- `addons/hr_skills/models/hr_employee_public.py`
- `addons/hr_skills/models/hr_employee_skill.py`
- `addons/hr_skills/models/hr_individual_skill_mixin.py`
- `addons/hr_skills/models/hr_job.py`
- `addons/hr_skills/models/hr_job_skill.py`
- `addons/hr_skills/models/hr_resume_line.py`
- `addons/hr_skills/models/hr_resume_line_type.py`
- `addons/hr_skills/models/hr_skill.py`
- `addons/hr_skills/models/hr_skill_level.py`
- `addons/hr_skills/models/hr_skill_type.py`
- `addons/hr_skills/models/resource_resource.py`
- `addons/hr_skills/report/__init__.py`
- `addons/hr_skills/report/hr_employee_cv_report.py`
- `addons/hr_skills/report/hr_employee_cv_report.xml`
- `addons/hr_skills/report/hr_employee_skill_history_report.py`
- `addons/hr_skills/report/hr_employee_skill_history_report_views.xml`
- `addons/hr_skills/report/hr_employee_skill_report.py`
- `addons/hr_skills/report/hr_employee_skill_report_views.xml`
- `addons/hr_skills/security/ir.access.csv`
- `addons/hr_skills/static/description/icon.png`
- `addons/hr_skills/static/description/icon.svg`
- `addons/hr_skills/static/description/icon_hi.png`
- `addons/hr_skills/static/src/components/internal_resume_lines/internal_resume_one2many.js`
- `addons/hr_skills/static/src/components/internal_resume_lines/internal_resume_one2many.scss`
- `addons/hr_skills/static/src/components/internal_resume_lines/internal_resume_one2many.xml`
- `addons/hr_skills/static/src/core/common/hr_employee_model_patch.js`
- `addons/hr_skills/static/src/core/common/hr_employee_public_model_patch.js`
- `addons/hr_skills/static/src/core/common/hr_employee_skill_model.js`
- `addons/hr_skills/static/src/core/web/avatar_card/avatar_card_patch.js`
- `addons/hr_skills/static/src/core/web/avatar_card/avatar_card_patch.xml`
- `addons/hr_skills/static/src/fields/boolean_toggle_load/boolean_toggle_load.js`
- `addons/hr_skills/static/src/fields/form_view_one2many/form_view_one2many.xml`
- `addons/hr_skills/static/src/fields/formatted_date/formatted_date.js`
- `addons/hr_skills/static/src/fields/formatted_date/formatted_date.xml`
- `addons/hr_skills/static/src/fields/many2many_tags_skills/many2many_tags_skills.js`
- `addons/hr_skills/static/src/fields/many2many_tags_skills/many2many_tags_skills.xml`
- `addons/hr_skills/static/src/fields/one2many_tags_skills/one2many_tags_skills.js`
- `addons/hr_skills/static/src/fields/one2many_tags_skills/one2many_tags_skills.scss`
- `addons/hr_skills/static/src/fields/one2many_tags_skills/one2many_tags_skills.xml`
- `addons/hr_skills/static/src/fields/resume_one2many/resume_one2many.js`
- `addons/hr_skills/static/src/fields/resume_one2many/resume_one2many.scss`
- `addons/hr_skills/static/src/fields/resume_one2many/resume_one2many.xml`
- `addons/hr_skills/static/src/fields/skills_one2many/skills_one2many.js`
- `addons/hr_skills/static/src/fields/skills_one2many/skills_one2many.scss`
- `addons/hr_skills/static/src/fields/skills_one2many/skills_one2many.xml`
- `addons/hr_skills/static/src/scss/hr_employee.scss`
- `addons/hr_skills/static/src/scss/report_employee_cv.scss`
- `addons/hr_skills/static/src/views/skills_graph.js`
- `addons/hr_skills/static/src/views/skills_list_renderer.js`
- `addons/hr_skills/static/tests/hr_skills_test_helpers.js`
- `addons/hr_skills/static/tests/many2one_avatar_employee.test.js`
- `addons/hr_skills/static/tests/mock_server/mock_models/hr_employee.js`
- `addons/hr_skills/static/tests/mock_server/mock_models/hr_employee_skill.js`
- `addons/hr_skills/static/tests/mock_server/mock_models/hr_skill.js`
- `addons/hr_skills/static/tests/mock_server/mock_models/m2o_avatar_employee.js`
- `addons/hr_skills/static/tests/tours/skills_tour.js`
- `addons/hr_skills/static/tests/tours/skills_type_tours.js`
- `addons/hr_skills/tests/__init__.py`
- `addons/hr_skills/tests/test_certification_activities.py`
- `addons/hr_skills/tests/test_employee_skill.py`
- `addons/hr_skills/tests/test_report.py`
- `addons/hr_skills/tests/test_resource.py`
- `addons/hr_skills/tests/test_ui.py`
- `addons/hr_skills/views/hr_department_views.xml`
- `addons/hr_skills/views/hr_employee_cv_templates.xml`
- `addons/hr_skills/views/hr_job_skill_views.xml`
- `addons/hr_skills/views/hr_job_views.xml`
- `addons/hr_skills/views/hr_views.xml`
- `addons/hr_skills/wizard/__init__.py`
- `addons/hr_skills/wizard/hr_employee_cv_wizard.py`
- `addons/hr_skills/wizard/hr_employee_cv_wizard_views.xml`
