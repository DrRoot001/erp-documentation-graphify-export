# Module: project

- **Module ID:** MOD-475
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/project`
- **Manifest:** `addons/project/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Services/Project`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Manage tasks and collaborate on projects

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 395 files, including 82 Python, 74 XML, and 145 JavaScript/TypeScript files. The manifest declares dependencies: `analytic`, `base_setup`, `mail`, `portal_rating`, `resource`, `web`, `web_tour`, `digest`.

## 2. Module structure

- Model/business logic files: 33
- Controller/API files: 4
- XML/data/view/template files: 74
- Browser asset files: 145
- Security files: 2
- Test files: 39
- Scheduled/automation evidence files: 6
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/project/security/ir.access.csv`, `addons/project/security/project_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 33 model declarations, 775 methods, 11 constraint handlers, 4 onchange handlers, and 61 dependency declarations.
- **Evidence:** `addons/project/models/res_partner.py:9`, `addons/project/models/mail_message.py:6`, `addons/project/models/mail_activity.py:6`, `addons/project/models/project_role.py:6`, `addons/project/models/project_task_stage_personal.py:7`, `addons/project/models/res_groups.py:6`, `addons/project/models/project_project_stage.py:7`, `addons/project/models/project_task_recurrence.py:10`, `addons/project/models/res_config_settings.py:7`, `addons/project/models/account_analytic_line.py:6`, `addons/project/models/res_users_settings.py:4`, `addons/project/models/project_tags.py:10`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 4 controller files and 9 route declarations.
- **Evidence:** `addons/project/controllers/portal.py:66`, `addons/project/controllers/portal.py:117`, `addons/project/controllers/portal.py:178`, `addons/project/controllers/portal.py:197`, `addons/project/controllers/portal.py:214`, `addons/project/controllers/portal.py:248`, `addons/project/controllers/portal.py:558`, `addons/project/controllers/portal.py:590`, `addons/project/controllers/portal.py:610`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 74 XML files and 145 JavaScript/TypeScript files; static XML analysis found 540 record/template/menu identifiers.
- **Evidence:** `addons/project/security/project_security.xml:3`, `addons/project/security/project_security.xml:9`, `addons/project/security/project_security.xml:17`, `addons/project/security/project_security.xml:26`, `addons/project/security/project_security.xml:30`, `addons/project/security/project_security.xml:34`, `addons/project/security/project_security.xml:38`, `addons/project/security/project_security.xml:45`, `addons/project/report/project_report_views.xml:4`, `addons/project/report/project_report_views.xml:21`, `addons/project/report/project_report_views.xml:32`, `addons/project/report/project_report_views.xml:51`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/project/security/ir.access.csv`, `addons/project/security/project_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 6 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/project/__manifest__.py`, `addons/project/data/ir_cron_data.xml`, `addons/project/views/project_project_stage_views.xml`, `addons/project/views/project_task_type_views.xml`, `addons/project/views/project_task_views.xml`, `addons/project/views/project_project_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 39 test files are present.
- **Evidence:** `addons/project/tests/test_access_rights.py`, `addons/project/tests/test_task_state.py`, `addons/project/tests/test_project_tags.py`, `addons/project/tests/test_project_sharing_portal_access.py`, `addons/project/tests/test_project_update_access_rights.py`, `addons/project/tests/test_task_dependencies.py`, `addons/project/tests/test_project_template_ui.py`, `addons/project/tests/test_project_sharing.py`, `addons/project/tests/test_project_sharing_ui.py`, `addons/project/tests/test_project_recurrence.py`, `addons/project/tests/test_task_templates_ui.py`, `addons/project/tests/test_project_embedded_action_settings.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 74; representative identifiers: `res_groups_privilege_project`, `group_project_user`, `group_project_manager`, `group_project_stages`, `group_project_recurring_tasks`, `group_project_task_dependencies`, `group_project_milestone`, `project_task_rule_portal_project_sharing`, `view_task_project_user_pivot`, `view_task_project_user_fsm_pivot_base`, `view_task_project_user_graph`, `view_task_project_user_fsm_graph_base`, `view_task_project_user_search`, `action_project_task_user_tree`, `project_task_burndown_chart_report_view_search`, `project_task_burndown_chart_report_view_graph`, `action_project_task_burndown_chart_report`, `project_time_by_stage_report_view_search`, `project_time_by_stage_report_view_graph`, `project_time_by_stage_report_view_pivot`
- Menus: 20; representative evidence: `addons/project/views/project_menus.xml:3`, `addons/project/views/project_menus.xml:10`, `addons/project/views/project_menus.xml:16`, `addons/project/views/project_menus.xml:23`, `addons/project/views/project_menus.xml:28`, `addons/project/views/project_menus.xml:34`, `addons/project/views/project_menus.xml:41`, `addons/project/views/project_menus.xml:47`, `addons/project/views/project_menus.xml:53`, `addons/project/views/project_menus.xml:61`, `addons/project/views/project_menus.xml:67`, `addons/project/views/project_menus.xml:74`
- Templates: 19; representative evidence: `addons/project/data/mail_template_data.xml:120`, `addons/project/data/mail_template_data.xml:129`, `addons/project/views/project_update_templates.xml:3`, `addons/project/views/project_update_templates.xml:15`, `addons/project/views/project_sharing_project_task_templates.xml:3`, `addons/project/views/project_portal_project_project_templates.xml:3`, `addons/project/views/project_portal_project_project_templates.xml:41`, `addons/project/views/project_portal_project_project_templates.xml:66`, `addons/project/views/project_task_templates.xml:3`, `addons/project/views/project_portal_project_task_templates.xml:3`, `addons/project/views/project_portal_project_task_templates.xml:12`, `addons/project/views/project_portal_project_task_templates.xml:19`
- View/action field declarations: 428; representative evidence: `addons/project/report/project_report_views.xml:6`, `addons/project/report/project_report_views.xml:7`, `addons/project/report/project_report_views.xml:23`, `addons/project/report/project_report_views.xml:27`, `addons/project/report/project_report_views.xml:34`, `addons/project/report/project_report_views.xml:35`, `addons/project/report/project_report_views.xml:53`, `addons/project/report/project_report_views.xml:57`, `addons/project/report/project_report_views.xml:64`, `addons/project/report/project_report_views.xml:67`, `addons/project/report/project_report_views.xml:79`, `addons/project/report/project_report_views.xml:82`
- Browser assets: 145; representative files: `addons/project/static/tests/project_project_form_view.test.js`, `addons/project/static/tests/project_project_calendar.test.js`, `addons/project/static/tests/project_is_favorite_field.test.js`, `addons/project/static/tests/project_task_priority_switch.test.js`, `addons/project/static/tests/project_project.test.js`, `addons/project/static/tests/project_task_list_view.test.js`, `addons/project/static/tests/project_notebook_task_list.test.js`, `addons/project/static/tests/project_task_subtask.test.js`, `addons/project/static/tests/project_update_with_color.test.js`, `addons/project/static/tests/project_task_calendar.test.js`, `addons/project/static/tests/project_task_groupby.test.js`, `addons/project/static/tests/project_task_analysis.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/project/__manifest__.py`
- **HTTP entry points:** `addons/project/controllers/portal.py:66`, `addons/project/controllers/portal.py:117`, `addons/project/controllers/portal.py:178`, `addons/project/controllers/portal.py:197`, `addons/project/controllers/portal.py:214`, `addons/project/controllers/portal.py:248`, `addons/project/controllers/portal.py:558`, `addons/project/controllers/portal.py:590`, `addons/project/controllers/portal.py:610`
- **Scheduled entry points:** `addons/project/__manifest__.py`, `addons/project/data/ir_cron_data.xml`, `addons/project/views/project_project_stage_views.xml`, `addons/project/views/project_task_type_views.xml`, `addons/project/views/project_task_views.xml`, `addons/project/views/project_project_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 33
- Representative model evidence: inherits `res.partner` (addons/project/models/res_partner.py:9); inherits `mail.message` (addons/project/models/mail_message.py:6); inherits `mail.activity` (addons/project/models/mail_activity.py:6); `project.role` (addons/project/models/project_role.py:6); `project.task.stage.personal` (addons/project/models/project_task_stage_personal.py:7); inherits `res.groups` (addons/project/models/res_groups.py:6); `project.project.stage` (addons/project/models/project_project_stage.py:7); `project.task.recurrence` (addons/project/models/project_task_recurrence.py:10); inherits `res.config.settings` (addons/project/models/res_config_settings.py:7); inherits `account.analytic.line` (addons/project/models/account_analytic_line.py:6); inherits `res.users.settings` (addons/project/models/res_users_settings.py:4); `project.tags` (addons/project/models/project_tags.py:10); `project.update` (addons/project/models/project_update.py:21); inherits `digest.digest` (addons/project/models/digest_digest.py:7); `project.task` (addons/project/models/project_task.py:89); `project.project` (addons/project/models/project_project.py:22); `project.task.type` (addons/project/models/project_task_type.py:11); `project.collaborator` (addons/project/models/project_collaborator.py:6); inherits `res.users` (addons/project/models/res_users.py:4); inherits `account.analytic.account` (addons/project/models/account_analytic_account.py:8); `project.milestone` (addons/project/models/project_milestone.py:12); inherits `ir.ui.menu` (addons/project/models/ir_ui_menu.py:7); `report.project.task.user` (addons/project/report/project_report.py:9); `project.task.burndown.chart.report` (addons/project/report/project_task_burndown_chart_report.py:10); `project.task.stage.report` (addons/project/report/project_time_by_stage_report.py:5); `project.template.create.wizard` (addons/project/wizard/project_template_create_wizard.py:5); `project.template.role.to.users.map` (addons/project/wizard/project_template_create_wizard.py:70); `project.share.collaborator.wizard` (addons/project/wizard/project_share_collaborator_wizard.py:6); `project.share.wizard` (addons/project/wizard/project_share_wizard.py:8); `task.share.wizard` (addons/project/wizard/project_task_share_wizard.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 4
- Route declarations: 9
- Route evidence: `addons/project/controllers/portal.py:66`, `addons/project/controllers/portal.py:117`, `addons/project/controllers/portal.py:178`, `addons/project/controllers/portal.py:197`, `addons/project/controllers/portal.py:214`, `addons/project/controllers/portal.py:248`, `addons/project/controllers/portal.py:558`, `addons/project/controllers/portal.py:590`, `addons/project/controllers/portal.py:610`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `analytic`, `base_setup`, `mail`, `portal_rating`, `resource`, `web`, `web_tour`, `digest`
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

- `addons/project/README.md`
- `addons/project/__init__.py`
- `addons/project/__manifest__.py`
- `addons/project/controllers/__init__.py`
- `addons/project/controllers/portal.py`
- `addons/project/controllers/project_sharing_chatter.py`
- `addons/project/controllers/webmanifest.py`
- `addons/project/data/digest_data.xml`
- `addons/project/data/ir_cron_data.xml`
- `addons/project/data/mail_message_subtype_data.xml`
- `addons/project/data/mail_template_data.xml`
- `addons/project/data/mail_template_demo.xml`
- `addons/project/data/portal_entry_data.xml`
- `addons/project/data/project_data.xml`
- `addons/project/data/project_demo.xml`
- `addons/project/data/project_tour.xml`
- `addons/project/doc/changelog.rst`
- `addons/project/doc/index.rst`
- `addons/project/doc/stage_status.rst`
- `addons/project/i18n/af.po`
- `addons/project/i18n/ar.po`
- `addons/project/i18n/az.po`
- `addons/project/i18n/bg.po`
- `addons/project/i18n/bs.po`
- `addons/project/i18n/ca.po`
- `addons/project/i18n/cs.po`
- `addons/project/i18n/da.po`
- `addons/project/i18n/de.po`
- `addons/project/i18n/el.po`
- `addons/project/i18n/es.po`
- `addons/project/i18n/es_419.po`
- `addons/project/i18n/es_CL.po`
- `addons/project/i18n/et.po`
- `addons/project/i18n/eu.po`
- `addons/project/i18n/fa.po`
- `addons/project/i18n/fi.po`
- `addons/project/i18n/fr.po`
- `addons/project/i18n/gl.po`
- `addons/project/i18n/gu.po`
- `addons/project/i18n/he.po`
- `addons/project/i18n/hi.po`
- `addons/project/i18n/hr.po`
- `addons/project/i18n/hu.po`
- `addons/project/i18n/id.po`
- `addons/project/i18n/is.po`
- `addons/project/i18n/it.po`
- `addons/project/i18n/ja.po`
- `addons/project/i18n/ka.po`
- `addons/project/i18n/kab.po`
- `addons/project/i18n/km.po`
- `addons/project/i18n/ko.po`
- `addons/project/i18n/ku.po`
- `addons/project/i18n/lb.po`
- `addons/project/i18n/lo.po`
- `addons/project/i18n/lt.po`
- `addons/project/i18n/lv.po`
- `addons/project/i18n/mk.po`
- `addons/project/i18n/mn.po`
- `addons/project/i18n/my.po`
- `addons/project/i18n/nb.po`
- `addons/project/i18n/nl.po`
- `addons/project/i18n/pl.po`
- `addons/project/i18n/project.pot`
- `addons/project/i18n/pt.po`
- `addons/project/i18n/pt_BR.po`
- `addons/project/i18n/ro.po`
- `addons/project/i18n/ru.po`
- `addons/project/i18n/sk.po`
- `addons/project/i18n/sl.po`
- `addons/project/i18n/sr@latin.po`
- `addons/project/i18n/sv.po`
- `addons/project/i18n/th.po`
- `addons/project/i18n/tr.po`
- `addons/project/i18n/uk.po`
- `addons/project/i18n/uz.po`
- `addons/project/i18n/vi.po`
- `addons/project/i18n/zh_CN.po`
- `addons/project/i18n/zh_TW.po`
- `addons/project/migrations/1.4/post-migrate.py`
- `addons/project/models/__init__.py`
- `addons/project/models/account_analytic_account.py`
- `addons/project/models/account_analytic_line.py`
- `addons/project/models/digest_digest.py`
- `addons/project/models/ir_ui_menu.py`
- `addons/project/models/mail_activity.py`
- `addons/project/models/mail_message.py`
- `addons/project/models/project_collaborator.py`
- `addons/project/models/project_milestone.py`
- `addons/project/models/project_project.py`
- `addons/project/models/project_project_stage.py`
- `addons/project/models/project_role.py`
- `addons/project/models/project_tags.py`
- `addons/project/models/project_task.py`
- `addons/project/models/project_task_recurrence.py`
- `addons/project/models/project_task_stage_personal.py`
- `addons/project/models/project_task_type.py`
- `addons/project/models/project_update.py`
- `addons/project/models/res_config_settings.py`
- `addons/project/models/res_groups.py`
- `addons/project/models/res_partner.py`
- `addons/project/models/res_users.py`
- `addons/project/models/res_users_settings.py`
- `addons/project/populate/benchmarks.xml`
- `addons/project/populate/populate_demo.xml`
- `addons/project/report/__init__.py`
- `addons/project/report/project_report.py`
- `addons/project/report/project_report_views.xml`
- `addons/project/report/project_task_burndown_chart_report.py`
- `addons/project/report/project_task_burndown_chart_report_views.xml`
- `addons/project/report/project_time_by_stage_report.py`
- `addons/project/report/project_time_by_stage_report_views.xml`
- `addons/project/security/ir.access.csv`
- `addons/project/security/project_security.xml`
- `addons/project/static/description/icon.png`
- `addons/project/static/description/icon.svg`
- `addons/project/static/description/icon_hi.png`
- `addons/project/static/src/actions/client_actions.js`
- `addons/project/static/src/components/done_checkmark/task_done_checkmark.js`
- `addons/project/static/src/components/done_checkmark/task_done_checkmark.scss`
- `addons/project/static/src/components/done_checkmark/task_done_checkmark.xml`
- `addons/project/static/src/components/float_time_days/float_time_field.js`
- `addons/project/static/src/components/notebook_task_one2many_field/notebook_task_list_renderer.js`
- `addons/project/static/src/components/notebook_task_one2many_field/notebook_task_list_renderer.xml`
- `addons/project/static/src/components/notebook_task_one2many_field/notebook_task_one2many_field.js`
- `addons/project/static/src/components/project_configure_project_cog_menu/project_configure_project_cog_menu.js`
- `addons/project/static/src/components/project_configure_project_cog_menu/project_configure_project_cog_menu.xml`
- `addons/project/static/src/components/project_convert_project_to_template_cog_menu/project_convert_project_to_template_cog_menu.js`
- `addons/project/static/src/components/project_convert_project_to_template_cog_menu/project_convert_project_to_template_cog_menu.xml`
- `addons/project/static/src/components/project_is_favorite/project_is_favorite_field.js`
- `addons/project/static/src/components/project_many2one_field/project_many2one_field.js`
- `addons/project/static/src/components/project_many2one_field/project_many2one_field.scss`
- `addons/project/static/src/components/project_many2one_field/project_many2one_field.xml`
- `addons/project/static/src/components/project_state_selection/project_state_selection.js`
- `addons/project/static/src/components/project_state_selection/project_state_selection.scss`
- `addons/project/static/src/components/project_status_with_color_selection/project_status_with_color_selection_field.js`
- `addons/project/static/src/components/project_status_with_color_selection/project_status_with_color_selection_field.xml`
- `addons/project/static/src/components/project_task_name_with_subtask_count_char_field/project_task_name_with_subtask_count_char_field.js`
- `addons/project/static/src/components/project_task_name_with_subtask_count_char_field/project_task_name_with_subtask_count_char_field.xml`
- `addons/project/static/src/components/project_task_priority_switch_field/project_task_priority_switch_field.js`
- `addons/project/static/src/components/project_task_state_selection/project_task_stage_state_selection/project_task_stage_with_state_selection.js`
- `addons/project/static/src/components/project_task_state_selection/project_task_stage_state_selection/project_task_stage_with_state_selection.xml`
- `addons/project/static/src/components/project_task_state_selection/project_task_state_selection.js`
- `addons/project/static/src/components/project_task_state_selection/project_task_state_selection.scss`
- `addons/project/static/src/components/project_task_state_selection/project_task_state_selection.xml`
- `addons/project/static/src/components/subtask_kanban_list/subtask_kanban_create/subtask_kanban_create.js`
- `addons/project/static/src/components/subtask_kanban_list/subtask_kanban_create/subtask_kanban_create.xml`
- `addons/project/static/src/components/subtask_kanban_list/subtask_kanban_list.js`
- `addons/project/static/src/components/subtask_kanban_list/subtask_kanban_list.scss`
- `addons/project/static/src/components/subtask_kanban_list/subtask_kanban_list.xml`
- `addons/project/static/src/components/subtask_one2many_field/subtask_list_renderer.js`
- `addons/project/static/src/components/subtask_one2many_field/subtask_one2many_field.js`
- `addons/project/static/src/components/task_list_renderer.js`
- `addons/project/static/src/core/web/@types/models.d.ts`
- `addons/project/static/src/core/web/activity_menu_patch.js`
- `addons/project/static/src/core/web/follower_list_patch.js`
- `addons/project/static/src/core/web/thread_model_patch.js`
- `addons/project/static/src/css/project.css`
- `addons/project/static/src/img/app_store.png`
- `addons/project/static/src/img/bird.jpg`
- `addons/project/static/src/img/chrome_store.png`
- `addons/project/static/src/img/planner_icon.png`
- `addons/project/static/src/img/play_store.png`
- `addons/project/static/src/img/tasks.svg`
- `addons/project/static/src/img/tasks_icon.png`
- `addons/project/static/src/img/top_left_arrow.png`
- `addons/project/static/src/img/web_planner_email.png`
- `addons/project/static/src/img/web_planner_project.png`
- `addons/project/static/src/img/web_planner_subtype.png`
- `addons/project/static/src/js/tours/project.js`
- `addons/project/static/src/project_sharing/chatter/chatter_patch.js`
- `addons/project/static/src/project_sharing/chatter/composer_actions_patch.js`
- `addons/project/static/src/project_sharing/chatter/composer_patch.js`
- `addons/project/static/src/project_sharing/chatter/message_model_patch.js`
- `addons/project/static/src/project_sharing/chatter/portal_chatter_patch.xml`
- `addons/project/static/src/project_sharing/chatter/project_sharing_plugin.js`
- `addons/project/static/src/project_sharing/chatter/suggestion_service_patch.js`
- `addons/project/static/src/project_sharing/components/depend_on_ids_one2many/depend_on_ids_list_renderer.js`
- `addons/project/static/src/project_sharing/components/depend_on_ids_one2many/depend_on_ids_list_renderer.xml`
- `addons/project/static/src/project_sharing/components/depend_on_ids_one2many/depend_on_ids_one2many_field.js`
- `addons/project/static/src/project_sharing/editor/project_sharing_media_plugin.js`
- `addons/project/static/src/project_sharing/main.js`
- `addons/project/static/src/project_sharing/project_sharing.js`
- `addons/project/static/src/project_sharing/project_sharing.scss`
- `addons/project/static/src/project_sharing/project_sharing.xml`
- `addons/project/static/src/project_sharing/router.js`
- `addons/project/static/src/project_sharing/search/control_panel/control_panel.xml`
- `addons/project/static/src/project_sharing/views/form/project_sharing_form_compiler.js`
- `addons/project/static/src/project_sharing/views/form/project_sharing_form_controller.js`
- `addons/project/static/src/project_sharing/views/form/project_sharing_form_renderer.js`
- `addons/project/static/src/project_sharing/views/form/project_sharing_form_view.js`
- `addons/project/static/src/project_sharing/views/kanban/kanban_view.js`
- `addons/project/static/src/project_sharing/views/list/list_view.js`
- `addons/project/static/src/project_sharing/views/view.js`
- `addons/project/static/src/scss/portal_rating.scss`
- `addons/project/static/src/scss/project_dashboard.scss`
- `addons/project/static/src/scss/project_form.scss`
- `addons/project/static/src/scss/project_widgets.scss`
- `addons/project/static/src/utils/project_utils.js`
- `addons/project/static/src/views/analytic_account_form/analytic_account_form_controller.js`
- `addons/project/static/src/views/analytic_account_form/analytic_account_form_view.js`
- `addons/project/static/src/views/analytic_account_list/analytic_account_list_controller.js`
- `addons/project/static/src/views/analytic_account_list/analytic_account_list_view.js`
- `addons/project/static/src/views/burndown_chart/burndown_chart_model.js`
- `addons/project/static/src/views/burndown_chart/burndown_chart_search_model.js`
- `addons/project/static/src/views/burndown_chart/burndown_chart_view.js`
- `addons/project/static/src/views/burndown_chart/burndown_chart_view.xml`
- `addons/project/static/src/views/components/project_task_template_dropdown.js`
- `addons/project/static/src/views/components/project_task_template_dropdown.xml`
- `addons/project/static/src/views/components/project_template_buttons.js`
- `addons/project/static/src/views/components/project_template_buttons.scss`
- `addons/project/static/src/views/components/project_template_buttons.xml`
- `addons/project/static/src/views/components/project_template_dropdown.js`
- `addons/project/static/src/views/components/project_template_dropdown.xml`
- `addons/project/static/src/views/project_form/project_project_form_controller.js`
- `addons/project/static/src/views/project_form/project_project_form_controller.xml`
- `addons/project/static/src/views/project_form/project_project_form_view.js`
- `addons/project/static/src/views/project_model_mixin.js`
- `addons/project/static/src/views/project_project_activity/project_project_activity_model.js`
- `addons/project/static/src/views/project_project_activity/project_project_activity_view.js`
- `addons/project/static/src/views/project_project_calendar/common/project_common_calendar_popover.js`
- `addons/project/static/src/views/project_project_calendar/common/project_common_calendar_popover.xml`
- `addons/project/static/src/views/project_project_calendar/common/project_common_calendar_renderer.js`
- `addons/project/static/src/views/project_project_calendar/project_project_calendar_controller.js`
- `addons/project/static/src/views/project_project_calendar/project_project_calendar_model.js`
- `addons/project/static/src/views/project_project_calendar/project_project_calendar_renderer.js`
- `addons/project/static/src/views/project_project_calendar/project_project_calendar_view.js`
- `addons/project/static/src/views/project_project_kanban/project_project_group_config_menu.js`
- `addons/project/static/src/views/project_project_kanban/project_project_kanban_controller.js`
- `addons/project/static/src/views/project_project_kanban/project_project_kanban_controller.xml`
- `addons/project/static/src/views/project_project_kanban/project_project_kanban_header.js`
- `addons/project/static/src/views/project_project_kanban/project_project_kanban_renderer.js`
- `addons/project/static/src/views/project_project_kanban/project_task_kanban_view.js`
- `addons/project/static/src/views/project_project_list/project_project_list_controller.js`
- `addons/project/static/src/views/project_project_list/project_project_list_controller.xml`
- `addons/project/static/src/views/project_project_list/project_project_list_renderer.js`
- `addons/project/static/src/views/project_project_list/project_project_list_view.js`
- `addons/project/static/src/views/project_relational_model.js`
- `addons/project/static/src/views/project_task_activity/project_task_activity_model.js`
- `addons/project/static/src/views/project_task_activity/project_task_activity_view.js`
- `addons/project/static/src/views/project_task_analysis_graph/project_task_analysis_graph_model.js`
- `addons/project/static/src/views/project_task_analysis_graph/project_task_analysis_graph_renderer.js`
- `addons/project/static/src/views/project_task_analysis_graph/project_task_analysis_graph_view.js`
- `addons/project/static/src/views/project_task_analysis_pivot/project_task_analysis_pivot_model.js`
- `addons/project/static/src/views/project_task_analysis_pivot/project_task_analysis_pivot_renderer.js`
- `addons/project/static/src/views/project_task_analysis_pivot/project_task_analysis_pivot_view.js`
- `addons/project/static/src/views/project_task_analysis_renderer_mixin.js`
- `addons/project/static/src/views/project_task_calendar/project_task_calendar_common/project_task_calendar_common_renderer.js`
- `addons/project/static/src/views/project_task_calendar/project_task_calendar_controller.js`
- `addons/project/static/src/views/project_task_calendar/project_task_calendar_filter_section/project_task_calendar_filter_section.js`
- `addons/project/static/src/views/project_task_calendar/project_task_calendar_filter_section/project_task_calendar_filter_section.xml`
- Additional source files not expanded in this page: 145; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
