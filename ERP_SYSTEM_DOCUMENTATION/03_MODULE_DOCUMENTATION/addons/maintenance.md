# Module: maintenance

- **Module ID:** MOD-359
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/maintenance`
- **Manifest:** `addons/maintenance/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Supply Chain/Maintenance`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Track equipment and manage maintenance requests

**Manifest description:**

Track equipment and maintenance requests

**Scope evidence:** The module contains 98 files, including 9 Python, 9 XML, and 9 JavaScript/TypeScript files. The manifest declares dependencies: `mail`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 0
- XML/data/view/template files: 9
- Browser asset files: 9
- Security files: 2
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/maintenance/security/maintenance.xml`, `addons/maintenance/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 53 methods, 2 constraint handlers, 1 onchange handlers, and 16 dependency declarations.
- **Evidence:** `addons/maintenance/models/maintenance.py:10`, `addons/maintenance/models/maintenance.py:23`, `addons/maintenance/models/maintenance.py:69`, `addons/maintenance/models/maintenance.py:113`, `addons/maintenance/models/maintenance.py:240`, `addons/maintenance/models/maintenance.py:505`, `addons/maintenance/models/res_config_settings.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 9 XML files and 9 JavaScript/TypeScript files; static XML analysis found 90 record/template/menu identifiers.
- **Evidence:** `addons/maintenance/security/maintenance.xml:2`, `addons/maintenance/security/maintenance.xml:8`, `addons/maintenance/data/mail_activity_type_data.xml:5`, `addons/maintenance/data/maintenance_data.xml:6`, `addons/maintenance/data/maintenance_data.xml:11`, `addons/maintenance/data/maintenance_data.xml:16`, `addons/maintenance/data/maintenance_data.xml:21`, `addons/maintenance/data/mail_message_subtype_data.xml:5`, `addons/maintenance/data/mail_message_subtype_data.xml:12`, `addons/maintenance/data/mail_message_subtype_data.xml:20`, `addons/maintenance/data/mail_message_subtype_data.xml:27`, `addons/maintenance/data/mail_message_subtype_data.xml:34`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/maintenance/security/maintenance.xml`, `addons/maintenance/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/maintenance/tests/test_maintenance_multicompany.py`, `addons/maintenance/tests/test_calendar_with_recurrence.py`, `addons/maintenance/tests/test_maintenance.py`, `addons/maintenance/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 9; representative identifiers: `res_groups_privilege_maintenance`, `group_equipment_manager`, `mail_act_maintenance_request`, `stage_0`, `stage_1`, `stage_3`, `stage_4`, `mt_req_created`, `mt_req_status`, `mt_mat_assign`, `mt_cat_req_created`, `mt_cat_mat_assign`, `equipment_team_maintenance`, `equipment_team_metrology`, `equipment_team_subcontractor`, `equipment_computer`, `equipment_software`, `equipment_printer`, `equipment_monitor`, `equipment_phone`
- Menus: 16; representative evidence: `addons/maintenance/views/res_config_settings_views.xml:30`, `addons/maintenance/views/maintenance_views.xml:948`, `addons/maintenance/views/maintenance_views.xml:955`, `addons/maintenance/views/maintenance_views.xml:963`, `addons/maintenance/views/maintenance_views.xml:970`, `addons/maintenance/views/maintenance_views.xml:978`, `addons/maintenance/views/maintenance_views.xml:986`, `addons/maintenance/views/maintenance_views.xml:993`, `addons/maintenance/views/maintenance_views.xml:1000`, `addons/maintenance/views/maintenance_views.xml:1007`, `addons/maintenance/views/maintenance_views.xml:1012`, `addons/maintenance/views/maintenance_views.xml:1017`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 96; representative evidence: `addons/maintenance/data/mail_activity_type_data.xml:9`, `addons/maintenance/data/mail_message_subtype_data.xml:7`, `addons/maintenance/data/mail_message_subtype_data.xml:14`, `addons/maintenance/data/mail_message_subtype_data.xml:22`, `addons/maintenance/data/mail_message_subtype_data.xml:29`, `addons/maintenance/data/mail_message_subtype_data.xml:36`, `addons/maintenance/data/maintenance_demo.xml:42`, `addons/maintenance/data/maintenance_demo.xml:51`, `addons/maintenance/data/maintenance_demo.xml:60`, `addons/maintenance/data/maintenance_demo.xml:70`, `addons/maintenance/data/maintenance_demo.xml:79`, `addons/maintenance/data/maintenance_demo.xml:88`
- Browser assets: 9; representative files: `addons/maintenance/static/src/widgets/maintenance_request_state_selection.js`, `addons/maintenance/static/src/views/calendar_with_recurrence/calendar_with_recurrence_model.js`, `addons/maintenance/static/src/views/calendar_with_recurrence/calendar_with_recurrence_view.js`, `addons/maintenance/static/src/views/calendar_with_recurrence/calendar_with_recurrence_renderer.js`, `addons/maintenance/static/src/views/calendar_with_recurrence/calendar_with_recurrence_year_popover.js`, `addons/maintenance/static/src/views/calendar_with_recurrence/calendar_with_recurrence_year_renderer.js`, `addons/maintenance/static/src/views/calendar_with_recurrence/calendar_with_recurrence_common_renderer.js`, `addons/maintenance/static/src/views/fields/radio/ordered_radio_field.js`, `addons/maintenance/static/tests/tours/tour_calendar_with_recurrence.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/maintenance/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: `maintenance.stage` (addons/maintenance/models/maintenance.py:10); `maintenance.equipment.category` (addons/maintenance/models/maintenance.py:23); `maintenance.mixin` (addons/maintenance/models/maintenance.py:69); `maintenance.equipment` (addons/maintenance/models/maintenance.py:113); `maintenance.request` (addons/maintenance/models/maintenance.py:240); `maintenance.team` (addons/maintenance/models/maintenance.py:505); inherits `res.config.settings` (addons/maintenance/models/res_config_settings.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mail`
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

- `addons/maintenance/__init__.py`
- `addons/maintenance/__manifest__.py`
- `addons/maintenance/data/mail_activity_type_data.xml`
- `addons/maintenance/data/mail_message_subtype_data.xml`
- `addons/maintenance/data/maintenance_data.xml`
- `addons/maintenance/data/maintenance_demo.xml`
- `addons/maintenance/i18n/af.po`
- `addons/maintenance/i18n/am.po`
- `addons/maintenance/i18n/ar.po`
- `addons/maintenance/i18n/az.po`
- `addons/maintenance/i18n/bg.po`
- `addons/maintenance/i18n/bs.po`
- `addons/maintenance/i18n/ca.po`
- `addons/maintenance/i18n/cs.po`
- `addons/maintenance/i18n/da.po`
- `addons/maintenance/i18n/de.po`
- `addons/maintenance/i18n/el.po`
- `addons/maintenance/i18n/es.po`
- `addons/maintenance/i18n/es_419.po`
- `addons/maintenance/i18n/es_CL.po`
- `addons/maintenance/i18n/et.po`
- `addons/maintenance/i18n/eu.po`
- `addons/maintenance/i18n/fa.po`
- `addons/maintenance/i18n/fi.po`
- `addons/maintenance/i18n/fo.po`
- `addons/maintenance/i18n/fr.po`
- `addons/maintenance/i18n/fr_BE.po`
- `addons/maintenance/i18n/fr_CA.po`
- `addons/maintenance/i18n/gl.po`
- `addons/maintenance/i18n/gu.po`
- `addons/maintenance/i18n/he.po`
- `addons/maintenance/i18n/hi.po`
- `addons/maintenance/i18n/hr.po`
- `addons/maintenance/i18n/hu.po`
- `addons/maintenance/i18n/id.po`
- `addons/maintenance/i18n/is.po`
- `addons/maintenance/i18n/it.po`
- `addons/maintenance/i18n/ja.po`
- `addons/maintenance/i18n/ka.po`
- `addons/maintenance/i18n/kab.po`
- `addons/maintenance/i18n/kk.po`
- `addons/maintenance/i18n/km.po`
- `addons/maintenance/i18n/ko.po`
- `addons/maintenance/i18n/ku.po`
- `addons/maintenance/i18n/lb.po`
- `addons/maintenance/i18n/lo.po`
- `addons/maintenance/i18n/lt.po`
- `addons/maintenance/i18n/lv.po`
- `addons/maintenance/i18n/maintenance.pot`
- `addons/maintenance/i18n/mk.po`
- `addons/maintenance/i18n/mn.po`
- `addons/maintenance/i18n/my.po`
- `addons/maintenance/i18n/nb.po`
- `addons/maintenance/i18n/nl.po`
- `addons/maintenance/i18n/pl.po`
- `addons/maintenance/i18n/pt.po`
- `addons/maintenance/i18n/pt_BR.po`
- `addons/maintenance/i18n/ro.po`
- `addons/maintenance/i18n/ru.po`
- `addons/maintenance/i18n/sk.po`
- `addons/maintenance/i18n/sl.po`
- `addons/maintenance/i18n/sq.po`
- `addons/maintenance/i18n/sr@latin.po`
- `addons/maintenance/i18n/sv.po`
- `addons/maintenance/i18n/th.po`
- `addons/maintenance/i18n/tr.po`
- `addons/maintenance/i18n/uk.po`
- `addons/maintenance/i18n/uz.po`
- `addons/maintenance/i18n/vi.po`
- `addons/maintenance/i18n/zh_CN.po`
- `addons/maintenance/i18n/zh_TW.po`
- `addons/maintenance/models/__init__.py`
- `addons/maintenance/models/maintenance.py`
- `addons/maintenance/models/res_config_settings.py`
- `addons/maintenance/security/ir.access.csv`
- `addons/maintenance/security/maintenance.xml`
- `addons/maintenance/static/description/icon.png`
- `addons/maintenance/static/description/icon.svg`
- `addons/maintenance/static/description/icon_hi.png`
- `addons/maintenance/static/src/scss/maintenance_team_dashboard.scss`
- `addons/maintenance/static/src/views/calendar_with_recurrence/calendar_with_recurrence_common_renderer.js`
- `addons/maintenance/static/src/views/calendar_with_recurrence/calendar_with_recurrence_model.js`
- `addons/maintenance/static/src/views/calendar_with_recurrence/calendar_with_recurrence_renderer.js`
- `addons/maintenance/static/src/views/calendar_with_recurrence/calendar_with_recurrence_view.js`
- `addons/maintenance/static/src/views/calendar_with_recurrence/calendar_with_recurrence_year_popover.js`
- `addons/maintenance/static/src/views/calendar_with_recurrence/calendar_with_recurrence_year_renderer.js`
- `addons/maintenance/static/src/views/fields/radio/ordered_radio_field.js`
- `addons/maintenance/static/src/widgets/maintenance_request_state_selection.js`
- `addons/maintenance/static/src/widgets/maintenance_request_state_selection.scss`
- `addons/maintenance/static/src/widgets/maintenance_state_selection.xml`
- `addons/maintenance/static/tests/tours/tour_calendar_with_recurrence.js`
- `addons/maintenance/tests/__init__.py`
- `addons/maintenance/tests/test_calendar_with_recurrence.py`
- `addons/maintenance/tests/test_maintenance.py`
- `addons/maintenance/tests/test_maintenance_multicompany.py`
- `addons/maintenance/views/mail_activity_views.xml`
- `addons/maintenance/views/maintenance_views.xml`
- `addons/maintenance/views/res_config_settings_views.xml`
