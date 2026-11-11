# Module: calendar_sms

- **Module ID:** MOD-047
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/calendar_sms`
- **Manifest:** `addons/calendar_sms/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Productivity/Calendar`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Send text messages as event reminders

**Manifest description:**

Send text messages as event reminders

**Scope evidence:** The module contains 64 files, including 8 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `calendar`, `sms`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 3
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 9 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/calendar_sms/models/calendar_event.py:8`, `addons/calendar_sms/models/calendar_alarm.py:7`, `addons/calendar_sms/models/calendar_alarm_manager.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 5 record/template/menu identifiers.
- **Evidence:** `addons/calendar_sms/data/sms_data.xml:4`, `addons/calendar_sms/views/calendar_alarm_views.xml:2`, `addons/calendar_sms/views/calendar_views.xml:4`, `addons/calendar_sms/views/calendar_views.xml:16`, `addons/calendar_sms/views/calendar_views.xml:28`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/calendar_sms/tests/test_calendar_sms.py`, `addons/calendar_sms/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `sms_template_data_calendar_reminder`, `calendar_alarm_view_kanban`, `calendar_alarm_view_form`, `view_calendar_event_tree_inherited`, `view_calendar_event_form_inherited`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 8; representative evidence: `addons/calendar_sms/views/calendar_alarm_views.xml:4`, `addons/calendar_sms/views/calendar_alarm_views.xml:6`, `addons/calendar_sms/views/calendar_views.xml:6`, `addons/calendar_sms/views/calendar_views.xml:8`, `addons/calendar_sms/views/calendar_views.xml:18`, `addons/calendar_sms/views/calendar_views.xml:20`, `addons/calendar_sms/views/calendar_views.xml:30`, `addons/calendar_sms/views/calendar_views.xml:32`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/calendar_sms/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `calendar.event` (addons/calendar_sms/models/calendar_event.py:8); inherits `calendar.alarm` (addons/calendar_sms/models/calendar_alarm.py:7); inherits `calendar.alarm_manager` (addons/calendar_sms/models/calendar_alarm_manager.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `calendar`, `sms`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/calendar_sms/__init__.py`
- `addons/calendar_sms/__manifest__.py`
- `addons/calendar_sms/data/sms_data.xml`
- `addons/calendar_sms/i18n/af.po`
- `addons/calendar_sms/i18n/ar.po`
- `addons/calendar_sms/i18n/az.po`
- `addons/calendar_sms/i18n/bg.po`
- `addons/calendar_sms/i18n/bs.po`
- `addons/calendar_sms/i18n/ca.po`
- `addons/calendar_sms/i18n/calendar_sms.pot`
- `addons/calendar_sms/i18n/cs.po`
- `addons/calendar_sms/i18n/da.po`
- `addons/calendar_sms/i18n/de.po`
- `addons/calendar_sms/i18n/el.po`
- `addons/calendar_sms/i18n/es.po`
- `addons/calendar_sms/i18n/es_419.po`
- `addons/calendar_sms/i18n/et.po`
- `addons/calendar_sms/i18n/fa.po`
- `addons/calendar_sms/i18n/fi.po`
- `addons/calendar_sms/i18n/fr.po`
- `addons/calendar_sms/i18n/gu.po`
- `addons/calendar_sms/i18n/he.po`
- `addons/calendar_sms/i18n/hi.po`
- `addons/calendar_sms/i18n/hr.po`
- `addons/calendar_sms/i18n/hu.po`
- `addons/calendar_sms/i18n/id.po`
- `addons/calendar_sms/i18n/is.po`
- `addons/calendar_sms/i18n/it.po`
- `addons/calendar_sms/i18n/ja.po`
- `addons/calendar_sms/i18n/kab.po`
- `addons/calendar_sms/i18n/km.po`
- `addons/calendar_sms/i18n/ko.po`
- `addons/calendar_sms/i18n/ku.po`
- `addons/calendar_sms/i18n/lo.po`
- `addons/calendar_sms/i18n/lt.po`
- `addons/calendar_sms/i18n/lv.po`
- `addons/calendar_sms/i18n/mn.po`
- `addons/calendar_sms/i18n/my.po`
- `addons/calendar_sms/i18n/nb.po`
- `addons/calendar_sms/i18n/nl.po`
- `addons/calendar_sms/i18n/pl.po`
- `addons/calendar_sms/i18n/pt.po`
- `addons/calendar_sms/i18n/pt_BR.po`
- `addons/calendar_sms/i18n/ro.po`
- `addons/calendar_sms/i18n/ru.po`
- `addons/calendar_sms/i18n/sk.po`
- `addons/calendar_sms/i18n/sl.po`
- `addons/calendar_sms/i18n/sr@latin.po`
- `addons/calendar_sms/i18n/sv.po`
- `addons/calendar_sms/i18n/th.po`
- `addons/calendar_sms/i18n/tr.po`
- `addons/calendar_sms/i18n/uk.po`
- `addons/calendar_sms/i18n/uz.po`
- `addons/calendar_sms/i18n/vi.po`
- `addons/calendar_sms/i18n/zh_CN.po`
- `addons/calendar_sms/i18n/zh_TW.po`
- `addons/calendar_sms/models/__init__.py`
- `addons/calendar_sms/models/calendar_alarm.py`
- `addons/calendar_sms/models/calendar_alarm_manager.py`
- `addons/calendar_sms/models/calendar_event.py`
- `addons/calendar_sms/tests/__init__.py`
- `addons/calendar_sms/tests/test_calendar_sms.py`
- `addons/calendar_sms/views/calendar_alarm_views.xml`
- `addons/calendar_sms/views/calendar_views.xml`
