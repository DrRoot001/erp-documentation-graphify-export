# Module: google_calendar

- **Module ID:** MOD-078
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/google_calendar`
- **Manifest:** `addons/google_calendar/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Productivity`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 125 files, including 35 Python, 6 XML, and 4 JavaScript/TypeScript files. The manifest declares dependencies: `google_account`, `calendar`.

## 2. Module structure

- Model/business logic files: 12
- Controller/API files: 3
- XML/data/view/template files: 6
- Browser asset files: 4
- Security files: 1
- Test files: 11
- Scheduled/automation evidence files: 2
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/google_calendar/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 12 model declarations, 343 methods, 0 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/google_calendar/models/res_config_settings.py:6`, `addons/google_calendar/models/res_users_settings.py:15`, `addons/google_calendar/models/google_event_sync.py:21`, `addons/google_calendar/models/calendar_event.py:15`, `addons/google_calendar/models/google_sync.py:46`, `addons/google_calendar/models/calendar_user.py:4`, `addons/google_calendar/models/calendar_attendee.py:8`, `addons/google_calendar/models/calendar_calendar.py:25`, `addons/google_calendar/models/calendar_alarm_manager.py:7`, `addons/google_calendar/models/res_users.py:17`, `addons/google_calendar/models/calendar_recurrence_rule.py:15`, `addons/google_calendar/wizard/reset_account.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 1 route declarations.
- **Evidence:** `addons/google_calendar/controllers/main.py:16`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 4 JavaScript/TypeScript files; static XML analysis found 9 record/template/menu identifiers.
- **Evidence:** `addons/google_calendar/wizard/reset_account_views.xml:3`, `addons/google_calendar/wizard/reset_account_views.xml:21`, `addons/google_calendar/data/google_calendar_data.xml:4`, `addons/google_calendar/views/res_config_settings_views.xml:3`, `addons/google_calendar/views/google_calendar_views.xml:3`, `addons/google_calendar/views/google_calendar_views.xml:14`, `addons/google_calendar/views/google_calendar_views.xml:25`, `addons/google_calendar/views/google_calendar_views.xml:36`, `addons/google_calendar/views/res_users_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/google_calendar/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/google_calendar/data/google_calendar_data.xml`, `addons/google_calendar/tests/test_sync_google2odoo.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 11 test files are present.
- **Evidence:** `addons/google_calendar/tests/test_sync_common.py`, `addons/google_calendar/tests/test_sync_odoo2google.py`, `addons/google_calendar/tests/test_google_event.py`, `addons/google_calendar/tests/test_google_access_roles.py`, `addons/google_calendar/tests/test_sync_google2odoo.py`, `addons/google_calendar/tests/test_sync_calendars_google2odoo.py`, `addons/google_calendar/tests/test_token_access.py`, `addons/google_calendar/tests/test_sync_odoo2google_mail.py`, `addons/google_calendar/tests/test_multi_calendar_sync.py`, `addons/google_calendar/tests/__init__.py`, `addons/google_calendar/tests/test_sync_calendars_odoo2google.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `google_calendar_reset_account_view_form`, `google_calendar_reset_account_action`, `ir_cron_sync_all_cals`, `res_config_settings_view_form`, `view_google_calendar_event`, `calendar_calendar_view_form_inherit_google_calendar`, `calendar_user_view_form_inherit_google_calendar`, `calendar_calendar_view_list_inherit_google_calendar`, `view_users_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 16; representative evidence: `addons/google_calendar/wizard/reset_account_views.xml:5`, `addons/google_calendar/wizard/reset_account_views.xml:6`, `addons/google_calendar/wizard/reset_account_views.xml:23`, `addons/google_calendar/wizard/reset_account_views.xml:24`, `addons/google_calendar/views/res_config_settings_views.xml:5`, `addons/google_calendar/views/res_config_settings_views.xml:7`, `addons/google_calendar/views/google_calendar_views.xml:5`, `addons/google_calendar/views/google_calendar_views.xml:7`, `addons/google_calendar/views/google_calendar_views.xml:16`, `addons/google_calendar/views/google_calendar_views.xml:18`, `addons/google_calendar/views/google_calendar_views.xml:27`, `addons/google_calendar/views/google_calendar_views.xml:29`
- Browser assets: 4; representative files: `addons/google_calendar/static/tests/google_calendar.test.js`, `addons/google_calendar/static/src/views/google_calendar/google_calendar_model.js`, `addons/google_calendar/static/src/views/google_calendar/google_calendar_controller.js`, `addons/google_calendar/static/src/views/google_calendar/attendee_calendar/attendee_calendar_filter_section.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/google_calendar/__manifest__.py`
- **HTTP entry points:** `addons/google_calendar/controllers/main.py:16`
- **Scheduled entry points:** `addons/google_calendar/data/google_calendar_data.xml`, `addons/google_calendar/tests/test_sync_google2odoo.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 12
- Representative model evidence: inherits `res.config.settings` (addons/google_calendar/models/res_config_settings.py:6); inherits `res.users.settings` (addons/google_calendar/models/res_users_settings.py:15); `google.event.sync` (addons/google_calendar/models/google_event_sync.py:21); `calendar.event` (addons/google_calendar/models/calendar_event.py:15); `google.sync` (addons/google_calendar/models/google_sync.py:46); inherits `calendar.user` (addons/google_calendar/models/calendar_user.py:4); inherits `calendar.attendee` (addons/google_calendar/models/calendar_attendee.py:8); `calendar.calendar` (addons/google_calendar/models/calendar_calendar.py:25); inherits `calendar.alarm_manager` (addons/google_calendar/models/calendar_alarm_manager.py:7); inherits `res.users` (addons/google_calendar/models/res_users.py:17); `calendar.recurrence` (addons/google_calendar/models/calendar_recurrence_rule.py:15); `google.calendar.account.reset` (addons/google_calendar/wizard/reset_account.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 1
- Route evidence: `addons/google_calendar/controllers/main.py:16`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `google_account`, `calendar`
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

- `addons/google_calendar/__init__.py`
- `addons/google_calendar/__manifest__.py`
- `addons/google_calendar/controllers/__init__.py`
- `addons/google_calendar/controllers/google_auth.py`
- `addons/google_calendar/controllers/main.py`
- `addons/google_calendar/data/google_calendar_data.xml`
- `addons/google_calendar/data/neutralize.sql`
- `addons/google_calendar/i18n/af.po`
- `addons/google_calendar/i18n/ar.po`
- `addons/google_calendar/i18n/az.po`
- `addons/google_calendar/i18n/bg.po`
- `addons/google_calendar/i18n/bs.po`
- `addons/google_calendar/i18n/ca.po`
- `addons/google_calendar/i18n/cs.po`
- `addons/google_calendar/i18n/da.po`
- `addons/google_calendar/i18n/de.po`
- `addons/google_calendar/i18n/el.po`
- `addons/google_calendar/i18n/es.po`
- `addons/google_calendar/i18n/es_419.po`
- `addons/google_calendar/i18n/es_CL.po`
- `addons/google_calendar/i18n/et.po`
- `addons/google_calendar/i18n/eu.po`
- `addons/google_calendar/i18n/fa.po`
- `addons/google_calendar/i18n/fi.po`
- `addons/google_calendar/i18n/fo.po`
- `addons/google_calendar/i18n/fr.po`
- `addons/google_calendar/i18n/fr_BE.po`
- `addons/google_calendar/i18n/fr_CA.po`
- `addons/google_calendar/i18n/gl.po`
- `addons/google_calendar/i18n/google_calendar.pot`
- `addons/google_calendar/i18n/gu.po`
- `addons/google_calendar/i18n/he.po`
- `addons/google_calendar/i18n/hi.po`
- `addons/google_calendar/i18n/hr.po`
- `addons/google_calendar/i18n/hu.po`
- `addons/google_calendar/i18n/id.po`
- `addons/google_calendar/i18n/is.po`
- `addons/google_calendar/i18n/it.po`
- `addons/google_calendar/i18n/ja.po`
- `addons/google_calendar/i18n/ka.po`
- `addons/google_calendar/i18n/kab.po`
- `addons/google_calendar/i18n/km.po`
- `addons/google_calendar/i18n/ko.po`
- `addons/google_calendar/i18n/ku.po`
- `addons/google_calendar/i18n/lb.po`
- `addons/google_calendar/i18n/lo.po`
- `addons/google_calendar/i18n/lt.po`
- `addons/google_calendar/i18n/lv.po`
- `addons/google_calendar/i18n/mk.po`
- `addons/google_calendar/i18n/mn.po`
- `addons/google_calendar/i18n/my.po`
- `addons/google_calendar/i18n/nb.po`
- `addons/google_calendar/i18n/nl.po`
- `addons/google_calendar/i18n/pl.po`
- `addons/google_calendar/i18n/pt.po`
- `addons/google_calendar/i18n/pt_BR.po`
- `addons/google_calendar/i18n/ro.po`
- `addons/google_calendar/i18n/ru.po`
- `addons/google_calendar/i18n/sk.po`
- `addons/google_calendar/i18n/sl.po`
- `addons/google_calendar/i18n/sq.po`
- `addons/google_calendar/i18n/sr@latin.po`
- `addons/google_calendar/i18n/sv.po`
- `addons/google_calendar/i18n/th.po`
- `addons/google_calendar/i18n/tr.po`
- `addons/google_calendar/i18n/uk.po`
- `addons/google_calendar/i18n/uz.po`
- `addons/google_calendar/i18n/vi.po`
- `addons/google_calendar/i18n/zh_CN.po`
- `addons/google_calendar/i18n/zh_TW.po`
- `addons/google_calendar/models/__init__.py`
- `addons/google_calendar/models/calendar_alarm_manager.py`
- `addons/google_calendar/models/calendar_attendee.py`
- `addons/google_calendar/models/calendar_calendar.py`
- `addons/google_calendar/models/calendar_event.py`
- `addons/google_calendar/models/calendar_recurrence_rule.py`
- `addons/google_calendar/models/calendar_user.py`
- `addons/google_calendar/models/google_event_sync.py`
- `addons/google_calendar/models/google_sync.py`
- `addons/google_calendar/models/res_config_settings.py`
- `addons/google_calendar/models/res_users.py`
- `addons/google_calendar/models/res_users_settings.py`
- `addons/google_calendar/security/ir.access.csv`
- `addons/google_calendar/static/description/an_event.png`
- `addons/google_calendar/static/description/calendar_in_action.png`
- `addons/google_calendar/static/description/coworker.png`
- `addons/google_calendar/static/description/create_quick.png`
- `addons/google_calendar/static/description/email.png`
- `addons/google_calendar/static/description/icon.png`
- `addons/google_calendar/static/description/icon.svg`
- `addons/google_calendar/static/description/icon_hi.png`
- `addons/google_calendar/static/description/index.html`
- `addons/google_calendar/static/description/notification.png`
- `addons/google_calendar/static/description/recurrent.png`
- `addons/google_calendar/static/description/the_calendar.png`
- `addons/google_calendar/static/src/img/calendar_32.png`
- `addons/google_calendar/static/src/img/google-calendar.svg`
- `addons/google_calendar/static/src/scss/google_calendar.scss`
- `addons/google_calendar/static/src/views/google_calendar/attendee_calendar/attendee_calendar_filter_section.js`
- `addons/google_calendar/static/src/views/google_calendar/google_calendar_controller.js`
- `addons/google_calendar/static/src/views/google_calendar/google_calendar_controller.xml`
- `addons/google_calendar/static/src/views/google_calendar/google_calendar_model.js`
- `addons/google_calendar/static/tests/google_calendar.test.js`
- `addons/google_calendar/tests/__init__.py`
- `addons/google_calendar/tests/test_google_access_roles.py`
- `addons/google_calendar/tests/test_google_event.py`
- `addons/google_calendar/tests/test_multi_calendar_sync.py`
- `addons/google_calendar/tests/test_sync_calendars_google2odoo.py`
- `addons/google_calendar/tests/test_sync_calendars_odoo2google.py`
- `addons/google_calendar/tests/test_sync_common.py`
- `addons/google_calendar/tests/test_sync_google2odoo.py`
- `addons/google_calendar/tests/test_sync_odoo2google.py`
- `addons/google_calendar/tests/test_sync_odoo2google_mail.py`
- `addons/google_calendar/tests/test_token_access.py`
- `addons/google_calendar/utils/__init__.py`
- `addons/google_calendar/utils/google_api_resource.py`
- `addons/google_calendar/utils/google_calendar.py`
- `addons/google_calendar/utils/google_calendar_service.py`
- `addons/google_calendar/utils/google_event.py`
- `addons/google_calendar/views/google_calendar_views.xml`
- `addons/google_calendar/views/res_config_settings_views.xml`
- `addons/google_calendar/views/res_users_views.xml`
- `addons/google_calendar/wizard/__init__.py`
- `addons/google_calendar/wizard/reset_account.py`
- `addons/google_calendar/wizard/reset_account_views.xml`
