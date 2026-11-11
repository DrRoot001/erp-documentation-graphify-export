# Module: microsoft_calendar

- **Module ID:** MOD-375
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/microsoft_calendar`
- **Manifest:** `addons/microsoft_calendar/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Productivity`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 95 files, including 29 Python, 6 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `microsoft_account`, `calendar`.

## 2. Module structure

- Model/business logic files: 9
- Controller/API files: 3
- XML/data/view/template files: 6
- Browser asset files: 3
- Security files: 1
- Test files: 10
- Scheduled/automation evidence files: 2
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/microsoft_calendar/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 9 model declarations, 303 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/microsoft_calendar/models/res_config_settings.py:6`, `addons/microsoft_calendar/models/res_users_settings.py:6`, `addons/microsoft_calendar/models/calendar_event.py:38`, `addons/microsoft_calendar/models/calendar_attendee.py:7`, `addons/microsoft_calendar/models/microsoft_sync.py:56`, `addons/microsoft_calendar/models/calendar_alarm_manager.py:7`, `addons/microsoft_calendar/models/res_users.py:18`, `addons/microsoft_calendar/models/calendar_recurrence_rule.py:7`, `addons/microsoft_calendar/wizard/reset_account.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 1 route declarations.
- **Evidence:** `addons/microsoft_calendar/controllers/main.py:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 3 JavaScript/TypeScript files; static XML analysis found 8 record/template/menu identifiers.
- **Evidence:** `addons/microsoft_calendar/wizard/reset_account_views.xml:3`, `addons/microsoft_calendar/wizard/reset_account_views.xml:21`, `addons/microsoft_calendar/data/microsoft_calendar_data.xml:4`, `addons/microsoft_calendar/views/microsoft_calendar_views.xml:3`, `addons/microsoft_calendar/views/microsoft_calendar_views.xml:14`, `addons/microsoft_calendar/views/microsoft_calendar_views.xml:48`, `addons/microsoft_calendar/views/res_config_settings_views.xml:3`, `addons/microsoft_calendar/views/res_users_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/microsoft_calendar/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/microsoft_calendar/data/microsoft_calendar_data.xml`, `addons/microsoft_calendar/tests/test_create_events.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 10 test files are present.
- **Evidence:** `addons/microsoft_calendar/tests/test_microsoft_service.py`, `addons/microsoft_calendar/tests/test_answer_events.py`, `addons/microsoft_calendar/tests/test_microsoft_event.py`, `addons/microsoft_calendar/tests/test_multicalendar.py`, `addons/microsoft_calendar/tests/test_update_events.py`, `addons/microsoft_calendar/tests/test_delete_events.py`, `addons/microsoft_calendar/tests/test_sync_odoo2microsoft_mail.py`, `addons/microsoft_calendar/tests/common.py`, `addons/microsoft_calendar/tests/test_create_events.py`, `addons/microsoft_calendar/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `microsoft_calendar_reset_account_view_form`, `microsoft_calendar_reset_account_action`, `ir_cron_sync_all_cals`, `view_microsoft_calendar_event`, `view_microsoft_calendar_event_form`, `calendar_calendar_view_form_inherit_microsoft_calendar`, `res_config_settings_view_form`, `view_users_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 14; representative evidence: `addons/microsoft_calendar/wizard/reset_account_views.xml:5`, `addons/microsoft_calendar/wizard/reset_account_views.xml:6`, `addons/microsoft_calendar/wizard/reset_account_views.xml:23`, `addons/microsoft_calendar/wizard/reset_account_views.xml:24`, `addons/microsoft_calendar/views/microsoft_calendar_views.xml:5`, `addons/microsoft_calendar/views/microsoft_calendar_views.xml:7`, `addons/microsoft_calendar/views/microsoft_calendar_views.xml:16`, `addons/microsoft_calendar/views/microsoft_calendar_views.xml:18`, `addons/microsoft_calendar/views/microsoft_calendar_views.xml:50`, `addons/microsoft_calendar/views/microsoft_calendar_views.xml:52`, `addons/microsoft_calendar/views/res_config_settings_views.xml:5`, `addons/microsoft_calendar/views/res_config_settings_views.xml:7`
- Browser assets: 3; representative files: `addons/microsoft_calendar/static/tests/microsoft_calendar.test.js`, `addons/microsoft_calendar/static/src/views/microsoft_calendar/microsoft_calendar_model.js`, `addons/microsoft_calendar/static/src/views/microsoft_calendar/microsoft_calendar_controller.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/microsoft_calendar/__manifest__.py`
- **HTTP entry points:** `addons/microsoft_calendar/controllers/main.py:15`
- **Scheduled entry points:** `addons/microsoft_calendar/data/microsoft_calendar_data.xml`, `addons/microsoft_calendar/tests/test_create_events.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 9
- Representative model evidence: inherits `res.config.settings` (addons/microsoft_calendar/models/res_config_settings.py:6); inherits `res.users.settings` (addons/microsoft_calendar/models/res_users_settings.py:6); `calendar.event` (addons/microsoft_calendar/models/calendar_event.py:38); inherits `calendar.attendee` (addons/microsoft_calendar/models/calendar_attendee.py:7); `microsoft.calendar.sync` (addons/microsoft_calendar/models/microsoft_sync.py:56); inherits `calendar.alarm_manager` (addons/microsoft_calendar/models/calendar_alarm_manager.py:7); inherits `res.users` (addons/microsoft_calendar/models/res_users.py:18); `calendar.recurrence` (addons/microsoft_calendar/models/calendar_recurrence_rule.py:7); `microsoft.calendar.account.reset` (addons/microsoft_calendar/wizard/reset_account.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 1
- Route evidence: `addons/microsoft_calendar/controllers/main.py:15`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `microsoft_account`, `calendar`
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

- `addons/microsoft_calendar/__init__.py`
- `addons/microsoft_calendar/__manifest__.py`
- `addons/microsoft_calendar/controllers/__init__.py`
- `addons/microsoft_calendar/controllers/main.py`
- `addons/microsoft_calendar/controllers/microsoft_auth.py`
- `addons/microsoft_calendar/data/microsoft_calendar_data.xml`
- `addons/microsoft_calendar/data/neutralize.sql`
- `addons/microsoft_calendar/i18n/ar.po`
- `addons/microsoft_calendar/i18n/az.po`
- `addons/microsoft_calendar/i18n/bg.po`
- `addons/microsoft_calendar/i18n/bs.po`
- `addons/microsoft_calendar/i18n/ca.po`
- `addons/microsoft_calendar/i18n/cs.po`
- `addons/microsoft_calendar/i18n/da.po`
- `addons/microsoft_calendar/i18n/de.po`
- `addons/microsoft_calendar/i18n/el.po`
- `addons/microsoft_calendar/i18n/es.po`
- `addons/microsoft_calendar/i18n/es_419.po`
- `addons/microsoft_calendar/i18n/et.po`
- `addons/microsoft_calendar/i18n/fa.po`
- `addons/microsoft_calendar/i18n/fi.po`
- `addons/microsoft_calendar/i18n/fr.po`
- `addons/microsoft_calendar/i18n/he.po`
- `addons/microsoft_calendar/i18n/hi.po`
- `addons/microsoft_calendar/i18n/hr.po`
- `addons/microsoft_calendar/i18n/hu.po`
- `addons/microsoft_calendar/i18n/id.po`
- `addons/microsoft_calendar/i18n/it.po`
- `addons/microsoft_calendar/i18n/ja.po`
- `addons/microsoft_calendar/i18n/kab.po`
- `addons/microsoft_calendar/i18n/ko.po`
- `addons/microsoft_calendar/i18n/ku.po`
- `addons/microsoft_calendar/i18n/lo.po`
- `addons/microsoft_calendar/i18n/lt.po`
- `addons/microsoft_calendar/i18n/lv.po`
- `addons/microsoft_calendar/i18n/microsoft_calendar.pot`
- `addons/microsoft_calendar/i18n/mn.po`
- `addons/microsoft_calendar/i18n/my.po`
- `addons/microsoft_calendar/i18n/nb.po`
- `addons/microsoft_calendar/i18n/nl.po`
- `addons/microsoft_calendar/i18n/pl.po`
- `addons/microsoft_calendar/i18n/pt.po`
- `addons/microsoft_calendar/i18n/pt_BR.po`
- `addons/microsoft_calendar/i18n/ro.po`
- `addons/microsoft_calendar/i18n/ru.po`
- `addons/microsoft_calendar/i18n/sk.po`
- `addons/microsoft_calendar/i18n/sl.po`
- `addons/microsoft_calendar/i18n/sr@latin.po`
- `addons/microsoft_calendar/i18n/sv.po`
- `addons/microsoft_calendar/i18n/th.po`
- `addons/microsoft_calendar/i18n/tr.po`
- `addons/microsoft_calendar/i18n/uk.po`
- `addons/microsoft_calendar/i18n/uz.po`
- `addons/microsoft_calendar/i18n/vi.po`
- `addons/microsoft_calendar/i18n/zh_CN.po`
- `addons/microsoft_calendar/i18n/zh_TW.po`
- `addons/microsoft_calendar/models/__init__.py`
- `addons/microsoft_calendar/models/calendar_alarm_manager.py`
- `addons/microsoft_calendar/models/calendar_attendee.py`
- `addons/microsoft_calendar/models/calendar_event.py`
- `addons/microsoft_calendar/models/calendar_recurrence_rule.py`
- `addons/microsoft_calendar/models/microsoft_sync.py`
- `addons/microsoft_calendar/models/res_config_settings.py`
- `addons/microsoft_calendar/models/res_users.py`
- `addons/microsoft_calendar/models/res_users_settings.py`
- `addons/microsoft_calendar/security/ir.access.csv`
- `addons/microsoft_calendar/static/description/icon.png`
- `addons/microsoft_calendar/static/description/icon.svg`
- `addons/microsoft_calendar/static/description/icon_hi.png`
- `addons/microsoft_calendar/static/src/img/calendar_outlook_32.png`
- `addons/microsoft_calendar/static/src/img/outlook-calendar.svg`
- `addons/microsoft_calendar/static/src/scss/microsoft_calendar.scss`
- `addons/microsoft_calendar/static/src/views/microsoft_calendar/microsoft_calendar_controller.js`
- `addons/microsoft_calendar/static/src/views/microsoft_calendar/microsoft_calendar_controller.xml`
- `addons/microsoft_calendar/static/src/views/microsoft_calendar/microsoft_calendar_model.js`
- `addons/microsoft_calendar/static/tests/microsoft_calendar.test.js`
- `addons/microsoft_calendar/tests/__init__.py`
- `addons/microsoft_calendar/tests/common.py`
- `addons/microsoft_calendar/tests/test_answer_events.py`
- `addons/microsoft_calendar/tests/test_create_events.py`
- `addons/microsoft_calendar/tests/test_delete_events.py`
- `addons/microsoft_calendar/tests/test_microsoft_event.py`
- `addons/microsoft_calendar/tests/test_microsoft_service.py`
- `addons/microsoft_calendar/tests/test_multicalendar.py`
- `addons/microsoft_calendar/tests/test_sync_odoo2microsoft_mail.py`
- `addons/microsoft_calendar/tests/test_update_events.py`
- `addons/microsoft_calendar/utils/__init__.py`
- `addons/microsoft_calendar/utils/microsoft_calendar.py`
- `addons/microsoft_calendar/utils/microsoft_event.py`
- `addons/microsoft_calendar/views/microsoft_calendar_views.xml`
- `addons/microsoft_calendar/views/res_config_settings_views.xml`
- `addons/microsoft_calendar/views/res_users_views.xml`
- `addons/microsoft_calendar/wizard/__init__.py`
- `addons/microsoft_calendar/wizard/reset_account.py`
- `addons/microsoft_calendar/wizard/reset_account_views.xml`
