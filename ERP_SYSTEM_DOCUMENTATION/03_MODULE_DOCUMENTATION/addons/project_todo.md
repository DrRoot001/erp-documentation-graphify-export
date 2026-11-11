# Module: project_todo

- **Module ID:** MOD-492
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/project_todo`
- **Manifest:** `addons/project_todo/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Productivity/To-Do`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Organize your work with memos and to-do lists

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 112 files, including 17 Python, 8 XML, and 28 JavaScript/TypeScript files. The manifest declares dependencies: `project`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 8
- Browser asset files: 28
- Security files: 1
- Test files: 10
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/project_todo/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 30 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/project_todo/models/project_task.py:8`, `addons/project_todo/models/res_users.py:7`, `addons/project_todo/wizard/mail_activity_todo_create.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 8 XML files and 28 JavaScript/TypeScript files; static XML analysis found 20 record/template/menu identifiers.
- **Evidence:** `addons/project_todo/wizard/mail_activity_todo_create.xml:3`, `addons/project_todo/data/digest_data.xml:4`, `addons/project_todo/data/todo_template.xml:5`, `addons/project_todo/views/project_todo_menus.xml:3`, `addons/project_todo/views/project_task_views.xml:5`, `addons/project_todo/views/project_task_views.xml:56`, `addons/project_todo/views/project_task_views.xml:79`, `addons/project_todo/views/project_task_views.xml:137`, `addons/project_todo/views/project_task_views.xml:163`, `addons/project_todo/views/project_task_views.xml:198`, `addons/project_todo/views/project_task_views.xml:216`, `addons/project_todo/views/project_task_views.xml:238`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/project_todo/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 10 test files are present.
- **Evidence:** `addons/project_todo/tests/test_access_rights.py`, `addons/project_todo/tests/test_project_tags.py`, `addons/project_todo/tests/test_todo_ui.py`, `addons/project_todo/tests/test_todo_onboarding_for_users.py`, `addons/project_todo/tests/test_mail_activity_todo_create.py`, `addons/project_todo/tests/test_todo_mail_features.py`, `addons/project_todo/tests/test_todo_quick_create.py`, `addons/project_todo/tests/test_mail_activity_systray_counter.py`, `addons/project_todo/tests/__init__.py`, `addons/project_todo/tests/test_project_task_type.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 8; representative identifiers: `mail_activity_todo_create_popup`, `digest_tip_project_todo_0`, `todo_user_onboarding`, `To-do`, `project_task_view_todo_kanban`, `project_task_view_todo_tree`, `project_task_view_todo_form`, `project_task_view_todo_quick_create_form`, `project_task_view_todo_conversion_form`, `project_task_view_todo_calendar`, `project_task_view_todo_activity`, `project_task_view_todo_search`, `project_task_action_todo`, `project_task_action_todo_kanban_view`, `project_task_action_todo_form_view`, `project_task_action_todo_tree_view`, `project_task_action_todo_calendar_view`, `project_task_action_todo_activity_view`, `project_task_action_convert_todo_to_task`, `project_task_action_convert_todo_to_task_form_view`
- Menus: 1; representative evidence: `addons/project_todo/views/project_todo_menus.xml:3`
- Templates: 1; representative evidence: `addons/project_todo/data/todo_template.xml:5`
- View/action field declarations: 28; representative evidence: `addons/project_todo/wizard/mail_activity_todo_create.xml:5`, `addons/project_todo/wizard/mail_activity_todo_create.xml:6`, `addons/project_todo/views/project_task_views.xml:7`, `addons/project_todo/views/project_task_views.xml:9`, `addons/project_todo/views/project_task_views.xml:58`, `addons/project_todo/views/project_task_views.xml:59`, `addons/project_todo/views/project_task_views.xml:81`, `addons/project_todo/views/project_task_views.xml:82`, `addons/project_todo/views/project_task_views.xml:139`, `addons/project_todo/views/project_task_views.xml:141`, `addons/project_todo/views/project_task_views.xml:164`, `addons/project_todo/views/project_task_views.xml:167`
- Browser assets: 28; representative files: `addons/project_todo/static/tests/todo_test_helpers.js`, `addons/project_todo/static/tests/todo_activity_wizard_view.test.js`, `addons/project_todo/static/tests/todo_list_view.test.js`, `addons/project_todo/static/tests/todo_calendar_view.test.js`, `addons/project_todo/static/tests/todo_done_checkmark.test.js`, `addons/project_todo/static/tests/todo_conversion_form_view.test.js`, `addons/project_todo/static/tests/todo_form_view.test.js`, `addons/project_todo/static/src/webclient/share_target/todo_share_target_item.js`, `addons/project_todo/static/src/components/todo_chatter_panel/todo_chatter_panel.js`, `addons/project_todo/static/src/components/todo_done_checkmark/todo_done_checkmark.js`, `addons/project_todo/static/src/core/web/activity_menu_patch.js`, `addons/project_todo/static/src/views/todo_activity_wizard/todo_activity_wizard_view.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/project_todo/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `project.task` (addons/project_todo/models/project_task.py:8); inherits `res.users` (addons/project_todo/models/res_users.py:7); `mail.activity.todo.create` (addons/project_todo/wizard/mail_activity_todo_create.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `project`
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

- `addons/project_todo/__init__.py`
- `addons/project_todo/__manifest__.py`
- `addons/project_todo/data/digest_data.xml`
- `addons/project_todo/data/todo_template.xml`
- `addons/project_todo/i18n/ar.po`
- `addons/project_todo/i18n/az.po`
- `addons/project_todo/i18n/bg.po`
- `addons/project_todo/i18n/bs.po`
- `addons/project_todo/i18n/ca.po`
- `addons/project_todo/i18n/cs.po`
- `addons/project_todo/i18n/da.po`
- `addons/project_todo/i18n/de.po`
- `addons/project_todo/i18n/el.po`
- `addons/project_todo/i18n/es.po`
- `addons/project_todo/i18n/es_419.po`
- `addons/project_todo/i18n/et.po`
- `addons/project_todo/i18n/fa.po`
- `addons/project_todo/i18n/fi.po`
- `addons/project_todo/i18n/fr.po`
- `addons/project_todo/i18n/he.po`
- `addons/project_todo/i18n/hi.po`
- `addons/project_todo/i18n/hr.po`
- `addons/project_todo/i18n/hu.po`
- `addons/project_todo/i18n/id.po`
- `addons/project_todo/i18n/it.po`
- `addons/project_todo/i18n/ja.po`
- `addons/project_todo/i18n/kab.po`
- `addons/project_todo/i18n/ko.po`
- `addons/project_todo/i18n/ku.po`
- `addons/project_todo/i18n/lo.po`
- `addons/project_todo/i18n/lt.po`
- `addons/project_todo/i18n/lv.po`
- `addons/project_todo/i18n/mn.po`
- `addons/project_todo/i18n/my.po`
- `addons/project_todo/i18n/nb.po`
- `addons/project_todo/i18n/nl.po`
- `addons/project_todo/i18n/pl.po`
- `addons/project_todo/i18n/project_todo.pot`
- `addons/project_todo/i18n/pt.po`
- `addons/project_todo/i18n/pt_BR.po`
- `addons/project_todo/i18n/ro.po`
- `addons/project_todo/i18n/ru.po`
- `addons/project_todo/i18n/sk.po`
- `addons/project_todo/i18n/sl.po`
- `addons/project_todo/i18n/sr@latin.po`
- `addons/project_todo/i18n/sv.po`
- `addons/project_todo/i18n/th.po`
- `addons/project_todo/i18n/tr.po`
- `addons/project_todo/i18n/uk.po`
- `addons/project_todo/i18n/uz.po`
- `addons/project_todo/i18n/vi.po`
- `addons/project_todo/i18n/zh_CN.po`
- `addons/project_todo/i18n/zh_TW.po`
- `addons/project_todo/models/__init__.py`
- `addons/project_todo/models/project_task.py`
- `addons/project_todo/models/res_users.py`
- `addons/project_todo/security/ir.access.csv`
- `addons/project_todo/static/description/icon.png`
- `addons/project_todo/static/description/icon.svg`
- `addons/project_todo/static/description/icon_hi.png`
- `addons/project_todo/static/img/convert_todo.png`
- `addons/project_todo/static/img/todo_access.png`
- `addons/project_todo/static/src/components/todo_chatter_panel/todo_chatter_panel.js`
- `addons/project_todo/static/src/components/todo_chatter_panel/todo_chatter_panel.scss`
- `addons/project_todo/static/src/components/todo_chatter_panel/todo_chatter_panel.xml`
- `addons/project_todo/static/src/components/todo_done_checkmark/todo_done_checkmark.js`
- `addons/project_todo/static/src/components/todo_done_checkmark/todo_done_checkmark.scss`
- `addons/project_todo/static/src/components/todo_done_checkmark/todo_done_checkmark.xml`
- `addons/project_todo/static/src/core/web/activity_menu_patch.js`
- `addons/project_todo/static/src/scss/todo.scss`
- `addons/project_todo/static/src/views/todo_activity_wizard/todo_activity_wizard_controller.js`
- `addons/project_todo/static/src/views/todo_activity_wizard/todo_activity_wizard_view.js`
- `addons/project_todo/static/src/views/todo_conversion_form/todo_conversion_form_controller.js`
- `addons/project_todo/static/src/views/todo_conversion_form/todo_conversion_form_view.js`
- `addons/project_todo/static/src/views/todo_form/todo_form_cog_menu.js`
- `addons/project_todo/static/src/views/todo_form/todo_form_control_panel.js`
- `addons/project_todo/static/src/views/todo_form/todo_form_control_panel.xml`
- `addons/project_todo/static/src/views/todo_form/todo_form_controller.js`
- `addons/project_todo/static/src/views/todo_form/todo_form_controller.scss`
- `addons/project_todo/static/src/views/todo_form/todo_form_renderer.js`
- `addons/project_todo/static/src/views/todo_form/todo_form_view.js`
- `addons/project_todo/static/src/views/todo_list/todo_list_controller.js`
- `addons/project_todo/static/src/views/todo_list/todo_list_view.js`
- `addons/project_todo/static/src/webclient/share_target/todo_share_target_item.js`
- `addons/project_todo/static/tests/mock_server/mock_models/mail_activity_todo_create.js`
- `addons/project_todo/static/tests/mock_server/mock_models/project_tags.js`
- `addons/project_todo/static/tests/mock_server/mock_models/project_task.js`
- `addons/project_todo/static/tests/todo_activity_wizard_view.test.js`
- `addons/project_todo/static/tests/todo_calendar_view.test.js`
- `addons/project_todo/static/tests/todo_conversion_form_view.test.js`
- `addons/project_todo/static/tests/todo_done_checkmark.test.js`
- `addons/project_todo/static/tests/todo_form_view.test.js`
- `addons/project_todo/static/tests/todo_list_view.test.js`
- `addons/project_todo/static/tests/todo_test_helpers.js`
- `addons/project_todo/static/tests/tours/project_task_activities_split.js`
- `addons/project_todo/static/tests/tours/project_todo_history.js`
- `addons/project_todo/static/tests/tours/project_todo_main_functions.js`
- `addons/project_todo/tests/__init__.py`
- `addons/project_todo/tests/test_access_rights.py`
- `addons/project_todo/tests/test_mail_activity_systray_counter.py`
- `addons/project_todo/tests/test_mail_activity_todo_create.py`
- `addons/project_todo/tests/test_project_tags.py`
- `addons/project_todo/tests/test_project_task_type.py`
- `addons/project_todo/tests/test_todo_mail_features.py`
- `addons/project_todo/tests/test_todo_onboarding_for_users.py`
- `addons/project_todo/tests/test_todo_quick_create.py`
- `addons/project_todo/tests/test_todo_ui.py`
- `addons/project_todo/views/project_task_views.xml`
- `addons/project_todo/views/project_todo_menus.xml`
- `addons/project_todo/wizard/__init__.py`
- `addons/project_todo/wizard/mail_activity_todo_create.py`
- `addons/project_todo/wizard/mail_activity_todo_create.xml`
