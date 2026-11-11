# Module: hr_calendar

- **Module ID:** MOD-084
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_calendar`
- **Manifest:** `addons/hr_calendar/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources/Employees`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 77 files, including 14 Python, 6 XML, and 6 JavaScript/TypeScript files. The manifest declares dependencies: `hr`, `calendar`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 6
- Security files: 1
- Test files: 6
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr_calendar/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 79 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/hr_calendar/models/res_partner.py:16`, `addons/hr_calendar/models/calendar_event.py:12`, `addons/hr_calendar/models/hr_employee.py:11`, `addons/hr_calendar/wizard/homework_location_wizard.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 6 JavaScript/TypeScript files; static XML analysis found 5 record/template/menu identifiers.
- **Evidence:** `addons/hr_calendar/wizard/homework_location_wizard.xml:3`, `addons/hr_calendar/wizard/homework_location_wizard.xml:48`, `addons/hr_calendar/views/calendar_views_calendarApp.xml:3`, `addons/hr_calendar/views/res_partner_views.xml:3`, `addons/hr_calendar/views/calendar_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/hr_calendar/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 6 test files are present.
- **Evidence:** `addons/hr_calendar/tests/test_event_interval.py`, `addons/hr_calendar/tests/test_working_hours.py`, `addons/hr_calendar/tests/common.py`, `addons/hr_calendar/tests/__init__.py`, `addons/hr_calendar/tests/test_working_days.py`, `addons/hr_calendar/tests/test_hr_employee_location.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `homework_location_wizard_view_form`, `set_location_wizard_action`, `view_calendar_event_calendar`, `view_res_partner_filter_inherit_calendar`, `menu_hr_homeworking_location_menu`
- Menus: 1; representative evidence: `addons/hr_calendar/views/calendar_views.xml:3`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 8; representative evidence: `addons/hr_calendar/wizard/homework_location_wizard.xml:5`, `addons/hr_calendar/wizard/homework_location_wizard.xml:6`, `addons/hr_calendar/wizard/homework_location_wizard.xml:50`, `addons/hr_calendar/wizard/homework_location_wizard.xml:51`, `addons/hr_calendar/views/calendar_views_calendarApp.xml:5`, `addons/hr_calendar/views/calendar_views_calendarApp.xml:7`, `addons/hr_calendar/views/res_partner_views.xml:5`, `addons/hr_calendar/views/res_partner_views.xml:8`
- Browser assets: 6; representative files: `addons/hr_calendar/static/tests/calendar_homeworking.test.js`, `addons/hr_calendar/static/src/calendar/common/hr_homeworking_calendar_controller.js`, `addons/hr_calendar/static/src/calendar/common/calendar_model.js`, `addons/hr_calendar/static/src/calendar/common/calendar_year_renderer.js`, `addons/hr_calendar/static/src/calendar/common/calendar_common_renderer.js`, `addons/hr_calendar/static/src/calendar/common/popover/calendar_common_popover.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_calendar/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `res.partner` (addons/hr_calendar/models/res_partner.py:16); inherits `calendar.event` (addons/hr_calendar/models/calendar_event.py:12); inherits `hr.employee` (addons/hr_calendar/models/hr_employee.py:11); `homework.location.wizard` (addons/hr_calendar/wizard/homework_location_wizard.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr`, `calendar`
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

- `addons/hr_calendar/__init__.py`
- `addons/hr_calendar/__manifest__.py`
- `addons/hr_calendar/i18n/ar.po`
- `addons/hr_calendar/i18n/az.po`
- `addons/hr_calendar/i18n/bg.po`
- `addons/hr_calendar/i18n/bs.po`
- `addons/hr_calendar/i18n/ca.po`
- `addons/hr_calendar/i18n/cs.po`
- `addons/hr_calendar/i18n/da.po`
- `addons/hr_calendar/i18n/de.po`
- `addons/hr_calendar/i18n/el.po`
- `addons/hr_calendar/i18n/es.po`
- `addons/hr_calendar/i18n/es_419.po`
- `addons/hr_calendar/i18n/et.po`
- `addons/hr_calendar/i18n/fa.po`
- `addons/hr_calendar/i18n/fi.po`
- `addons/hr_calendar/i18n/fr.po`
- `addons/hr_calendar/i18n/he.po`
- `addons/hr_calendar/i18n/hi.po`
- `addons/hr_calendar/i18n/hr.po`
- `addons/hr_calendar/i18n/hr_calendar.pot`
- `addons/hr_calendar/i18n/hu.po`
- `addons/hr_calendar/i18n/id.po`
- `addons/hr_calendar/i18n/it.po`
- `addons/hr_calendar/i18n/ja.po`
- `addons/hr_calendar/i18n/kab.po`
- `addons/hr_calendar/i18n/ko.po`
- `addons/hr_calendar/i18n/ku.po`
- `addons/hr_calendar/i18n/lo.po`
- `addons/hr_calendar/i18n/lt.po`
- `addons/hr_calendar/i18n/lv.po`
- `addons/hr_calendar/i18n/mn.po`
- `addons/hr_calendar/i18n/my.po`
- `addons/hr_calendar/i18n/nb.po`
- `addons/hr_calendar/i18n/nl.po`
- `addons/hr_calendar/i18n/pl.po`
- `addons/hr_calendar/i18n/pt.po`
- `addons/hr_calendar/i18n/pt_BR.po`
- `addons/hr_calendar/i18n/ro.po`
- `addons/hr_calendar/i18n/ru.po`
- `addons/hr_calendar/i18n/sk.po`
- `addons/hr_calendar/i18n/sl.po`
- `addons/hr_calendar/i18n/sr@latin.po`
- `addons/hr_calendar/i18n/sv.po`
- `addons/hr_calendar/i18n/th.po`
- `addons/hr_calendar/i18n/tr.po`
- `addons/hr_calendar/i18n/uk.po`
- `addons/hr_calendar/i18n/uz.po`
- `addons/hr_calendar/i18n/vi.po`
- `addons/hr_calendar/i18n/zh_CN.po`
- `addons/hr_calendar/i18n/zh_TW.po`
- `addons/hr_calendar/models/__init__.py`
- `addons/hr_calendar/models/calendar_event.py`
- `addons/hr_calendar/models/hr_employee.py`
- `addons/hr_calendar/models/res_partner.py`
- `addons/hr_calendar/security/ir.access.csv`
- `addons/hr_calendar/static/src/calendar/common/calendar_common_renderer.js`
- `addons/hr_calendar/static/src/calendar/common/calendar_common_renderer.scss`
- `addons/hr_calendar/static/src/calendar/common/calendar_common_renderer.xml`
- `addons/hr_calendar/static/src/calendar/common/calendar_model.js`
- `addons/hr_calendar/static/src/calendar/common/calendar_year_renderer.js`
- `addons/hr_calendar/static/src/calendar/common/hr_homeworking_calendar_controller.js`
- `addons/hr_calendar/static/src/calendar/common/popover/calendar_common_popover.js`
- `addons/hr_calendar/static/src/calendar/common/popover/calendar_common_popover.xml`
- `addons/hr_calendar/static/tests/calendar_homeworking.test.js`
- `addons/hr_calendar/tests/__init__.py`
- `addons/hr_calendar/tests/common.py`
- `addons/hr_calendar/tests/test_event_interval.py`
- `addons/hr_calendar/tests/test_hr_employee_location.py`
- `addons/hr_calendar/tests/test_working_days.py`
- `addons/hr_calendar/tests/test_working_hours.py`
- `addons/hr_calendar/views/calendar_views.xml`
- `addons/hr_calendar/views/calendar_views_calendarApp.xml`
- `addons/hr_calendar/views/res_partner_views.xml`
- `addons/hr_calendar/wizard/__init__.py`
- `addons/hr_calendar/wizard/homework_location_wizard.py`
- `addons/hr_calendar/wizard/homework_location_wizard.xml`
