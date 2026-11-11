# Module: resource

- **Module ID:** MOD-506
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/resource`
- **Manifest:** `addons/resource/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Module for resource management.
===============================

A resource represent something that can be scheduled (a developer on a task or a
work center on manufacturing orders). This module manages a resource calendar
associated to every resource. It also manages the leaves of every resource.

**Scope evidence:** The module contains 131 files, including 19 Python, 15 XML, and 27 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `web`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 0
- XML/data/view/template files: 15
- Browser asset files: 27
- Security files: 1
- Test files: 8
- Scheduled/automation evidence files: 2
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/resource/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 183 methods, 4 constraint handlers, 5 onchange handlers, and 19 dependency declarations.
- **Evidence:** `addons/resource/models/resource_calendar.py:21`, `addons/resource/models/resource_resource.py:18`, `addons/resource/models/resource_calendar_attendance.py:17`, `addons/resource/models/res_users.py:7`, `addons/resource/models/resource_calendar_leaves.py:13`, `addons/resource/models/resource_mixin.py:10`, `addons/resource/models/res_company.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 15 XML files and 27 JavaScript/TypeScript files; static XML analysis found 31 record/template/menu identifiers.
- **Evidence:** `addons/resource/data/ir_cron.xml:4`, `addons/resource/data/resource_demo.xml:4`, `addons/resource/data/resource_data.xml:4`, `addons/resource/data/resource_data.xml:10`, `addons/resource/views/resource_resource_views.xml:5`, `addons/resource/views/resource_resource_views.xml:29`, `addons/resource/views/resource_resource_views.xml:56`, `addons/resource/views/resource_resource_views.xml:76`, `addons/resource/views/resource_resource_views.xml:85`, `addons/resource/views/resource_resource_views.xml:97`, `addons/resource/views/resource_calendar_leaves_views.xml:3`, `addons/resource/views/resource_calendar_leaves_views.xml:22`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/resource/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/resource/__manifest__.py`, `addons/resource/data/ir_cron.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 8 test files are present.
- **Evidence:** `addons/resource/tests/test_performance.py`, `addons/resource/tests/test_resource_calendar.py`, `addons/resource/tests/test_filter_map_domain.py`, `addons/resource/tests/test_stress_check_collision.py`, `addons/resource/tests/test_utils.py`, `addons/resource/tests/__init__.py`, `addons/resource/tests/test_flexible_resource_calendar.py`, `addons/resource/tests/test_variable_resource_calendar.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 15; representative identifiers: `ir_cron_calendar_clean_up`, `resource_calendar_std_35h`, `resource_calendar_std`, `base.main_company`, `view_resource_resource_search`, `resource_resource_form`, `resource_resource_tree`, `action_resource_resource_tree`, `action_resource_material_from_calendar`, `resource_resource_action_from_calendar`, `view_resource_calendar_leaves_search`, `view_resource_calendar`, `resource_calendar_leave_form`, `resource_calendar_leave_tree`, `action_resource_calendar_leave_tree`, `resource_calendar_leaves_action_from_calendar`, `resource_calendar_closing_days`, `resource_calendar_resources_leaves`, `view_company_form_inherit_resource`, `Resource`
- Menus: 4; representative evidence: `addons/resource/views/menuitems.xml:3`, `addons/resource/views/menuitems.xml:6`, `addons/resource/views/menuitems.xml:10`, `addons/resource/views/menuitems.xml:14`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 46; representative evidence: `addons/resource/views/resource_resource_views.xml:7`, `addons/resource/views/resource_resource_views.xml:8`, `addons/resource/views/resource_resource_views.xml:31`, `addons/resource/views/resource_resource_views.xml:32`, `addons/resource/views/resource_resource_views.xml:58`, `addons/resource/views/resource_resource_views.xml:59`, `addons/resource/views/resource_resource_views.xml:78`, `addons/resource/views/resource_resource_views.xml:79`, `addons/resource/views/resource_resource_views.xml:87`, `addons/resource/views/resource_resource_views.xml:88`, `addons/resource/views/resource_resource_views.xml:99`, `addons/resource/views/resource_resource_views.xml:100`
- Browser assets: 27; representative files: `addons/resource/static/tests/resource_test_helpers.js`, `addons/resource/static/tests/resource_avatar.test.js`, `addons/resource/static/src/plugins/resource_calendar_plugin.js`, `addons/resource/static/src/plugins/resource_calendar_attendance_popover_loader.js`, `addons/resource/static/src/components/resource_avatar/resource_avatar.js`, `addons/resource/static/src/components/resource_calendar_attendance_popover/resource_calendar_attendance_popover.js`, `addons/resource/static/src/views/resource_calendar_attendance_calendar/resource_calendar_attendance_calendar_model.js`, `addons/resource/static/src/views/resource_calendar_attendance_calendar/resource_calendar_attendance_calendar_renderer.js`, `addons/resource/static/src/views/resource_calendar_attendance_calendar/resource_calendar_attendance_calendar_controller.js`, `addons/resource/static/src/views/resource_calendar_attendance_calendar/resource_calendar_attendance_calendar_view.js`, `addons/resource/static/src/views/resource_calendar_attendance_calendar/resource_calendar_attendance_calendar_common_renderer.js`, `addons/resource/static/src/views/form_with_html_expander/form_controller_with_html_expander.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/resource/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/resource/__manifest__.py`, `addons/resource/data/ir_cron.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: `resource.calendar` (addons/resource/models/resource_calendar.py:21); `resource.resource` (addons/resource/models/resource_resource.py:18); `resource.calendar.attendance` (addons/resource/models/resource_calendar_attendance.py:17); inherits `res.users` (addons/resource/models/res_users.py:7); `resource.calendar.leaves` (addons/resource/models/resource_calendar_leaves.py:13); `resource.mixin` (addons/resource/models/resource_mixin.py:10); inherits `res.company` (addons/resource/models/res_company.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `web`
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

- `addons/resource/__init__.py`
- `addons/resource/__manifest__.py`
- `addons/resource/data/ir_cron.xml`
- `addons/resource/data/resource_data.xml`
- `addons/resource/data/resource_demo.xml`
- `addons/resource/i18n/af.po`
- `addons/resource/i18n/am.po`
- `addons/resource/i18n/ar.po`
- `addons/resource/i18n/az.po`
- `addons/resource/i18n/bg.po`
- `addons/resource/i18n/bs.po`
- `addons/resource/i18n/ca.po`
- `addons/resource/i18n/cs.po`
- `addons/resource/i18n/da.po`
- `addons/resource/i18n/de.po`
- `addons/resource/i18n/el.po`
- `addons/resource/i18n/es.po`
- `addons/resource/i18n/es_419.po`
- `addons/resource/i18n/es_CL.po`
- `addons/resource/i18n/et.po`
- `addons/resource/i18n/eu.po`
- `addons/resource/i18n/fa.po`
- `addons/resource/i18n/fi.po`
- `addons/resource/i18n/fo.po`
- `addons/resource/i18n/fr.po`
- `addons/resource/i18n/fr_BE.po`
- `addons/resource/i18n/fr_CA.po`
- `addons/resource/i18n/gl.po`
- `addons/resource/i18n/gu.po`
- `addons/resource/i18n/he.po`
- `addons/resource/i18n/hi.po`
- `addons/resource/i18n/hr.po`
- `addons/resource/i18n/hu.po`
- `addons/resource/i18n/id.po`
- `addons/resource/i18n/is.po`
- `addons/resource/i18n/it.po`
- `addons/resource/i18n/ja.po`
- `addons/resource/i18n/ka.po`
- `addons/resource/i18n/kab.po`
- `addons/resource/i18n/kk.po`
- `addons/resource/i18n/km.po`
- `addons/resource/i18n/ko.po`
- `addons/resource/i18n/ku.po`
- `addons/resource/i18n/ln.po`
- `addons/resource/i18n/lo.po`
- `addons/resource/i18n/lt.po`
- `addons/resource/i18n/lv.po`
- `addons/resource/i18n/mk.po`
- `addons/resource/i18n/mn.po`
- `addons/resource/i18n/my.po`
- `addons/resource/i18n/nb.po`
- `addons/resource/i18n/nl.po`
- `addons/resource/i18n/pl.po`
- `addons/resource/i18n/pt.po`
- `addons/resource/i18n/pt_BR.po`
- `addons/resource/i18n/resource.pot`
- `addons/resource/i18n/ro.po`
- `addons/resource/i18n/ru.po`
- `addons/resource/i18n/sk.po`
- `addons/resource/i18n/sl.po`
- `addons/resource/i18n/sq.po`
- `addons/resource/i18n/sr@latin.po`
- `addons/resource/i18n/sv.po`
- `addons/resource/i18n/ta.po`
- `addons/resource/i18n/th.po`
- `addons/resource/i18n/tr.po`
- `addons/resource/i18n/uk.po`
- `addons/resource/i18n/uz.po`
- `addons/resource/i18n/vi.po`
- `addons/resource/i18n/zh_CN.po`
- `addons/resource/i18n/zh_TW.po`
- `addons/resource/models/__init__.py`
- `addons/resource/models/res_company.py`
- `addons/resource/models/res_users.py`
- `addons/resource/models/resource_calendar.py`
- `addons/resource/models/resource_calendar_attendance.py`
- `addons/resource/models/resource_calendar_leaves.py`
- `addons/resource/models/resource_mixin.py`
- `addons/resource/models/resource_resource.py`
- `addons/resource/models/utils.py`
- `addons/resource/security/ir.access.csv`
- `addons/resource/static/src/components/resource_avatar/resource_avatar.js`
- `addons/resource/static/src/components/resource_avatar/resource_avatar.scss`
- `addons/resource/static/src/components/resource_avatar/resource_avatar.xml`
- `addons/resource/static/src/components/resource_calendar_attendance_popover/resource_calendar_attendance_popover.js`
- `addons/resource/static/src/components/resource_calendar_attendance_popover/resource_calendar_attendance_popover.xml`
- `addons/resource/static/src/plugins/resource_calendar_attendance_popover_loader.js`
- `addons/resource/static/src/plugins/resource_calendar_plugin.js`
- `addons/resource/static/src/scss/resource_form.scss`
- `addons/resource/static/src/scss/resource_list.scss`
- `addons/resource/static/src/views/fields/calendar_type_confirm_radio/calendar_type_confirm_radio_field.js`
- `addons/resource/static/src/views/fields/resource_calendar_attendance_calendar_one2many/resource_calendar_attendance_calendar_one2many_field.js`
- `addons/resource/static/src/views/fields/resource_calendar_attendance_calendar_one2many/resource_calendar_attendance_calendar_one2many_field.xml`
- `addons/resource/static/src/views/fields/resource_calendar_attendance_filtered_one2many/resource_calendar_attendance_filtered_one2many.js`
- `addons/resource/static/src/views/fields/resource_calendar_hours_by_day/resource_calendar_hours_by_day.js`
- `addons/resource/static/src/views/fields/resource_calendar_hours_by_day/resource_calendar_hours_by_day.xml`
- `addons/resource/static/src/views/fields/resource_calendar_many2one/resource_calendar_many2one.js`
- `addons/resource/static/src/views/fields/resource_calendar_many2one/resource_calendar_many2one.xml`
- `addons/resource/static/src/views/form_with_html_expander/form_controller_with_html_expander.js`
- `addons/resource/static/src/views/form_with_html_expander/form_controller_with_html_expander.xml`
- `addons/resource/static/src/views/form_with_html_expander/form_renderer_with_html_expander.js`
- `addons/resource/static/src/views/form_with_html_expander/form_view_with_html_expander.js`
- `addons/resource/static/src/views/resource_calendar_attendance_calendar/resource_calendar_attendance_calendar_common_renderer.js`
- `addons/resource/static/src/views/resource_calendar_attendance_calendar/resource_calendar_attendance_calendar_controller.js`
- `addons/resource/static/src/views/resource_calendar_attendance_calendar/resource_calendar_attendance_calendar_model.js`
- `addons/resource/static/src/views/resource_calendar_attendance_calendar/resource_calendar_attendance_calendar_renderer.js`
- `addons/resource/static/src/views/resource_calendar_attendance_calendar/resource_calendar_attendance_calendar_view.js`
- `addons/resource/static/src/views/view_components/resource_multi_selection_buttons.js`
- `addons/resource/static/tests/mock_server/mock_models/resource_calendar.js`
- `addons/resource/static/tests/mock_server/mock_models/resource_calendar_attendance.js`
- `addons/resource/static/tests/mock_server/mock_models/resource_resource.js`
- `addons/resource/static/tests/mock_server/mock_models/resource_task.js`
- `addons/resource/static/tests/resource_avatar.test.js`
- `addons/resource/static/tests/resource_test_helpers.js`
- `addons/resource/static/tests/views/fields/calendar_one2many_field.test.js`
- `addons/resource/static/tests/views/fields/calendar_type_confirm_radio_field.test.js`
- `addons/resource/static/tests/views/resource_calendar_attendance_calendar_view.test.js`
- `addons/resource/tests/__init__.py`
- `addons/resource/tests/test_filter_map_domain.py`
- `addons/resource/tests/test_flexible_resource_calendar.py`
- `addons/resource/tests/test_performance.py`
- `addons/resource/tests/test_resource_calendar.py`
- `addons/resource/tests/test_stress_check_collision.py`
- `addons/resource/tests/test_utils.py`
- `addons/resource/tests/test_variable_resource_calendar.py`
- `addons/resource/views/menuitems.xml`
- `addons/resource/views/res_company_views.xml`
- `addons/resource/views/resource_calendar_attendance_views.xml`
- `addons/resource/views/resource_calendar_leaves_views.xml`
- `addons/resource/views/resource_calendar_views.xml`
- `addons/resource/views/resource_resource_views.xml`
