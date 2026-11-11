# Module: hr_attendance

- **Module ID:** MOD-083
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_attendance`
- **Manifest:** `addons/hr_attendance/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Human Resources/Attendances`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Track employee attendance

**Manifest description:**

This module aims to manage employee's attendances.
==================================================

Keeps account of the attendances of the employees on the basis of the
actions(Check in/Check out) performed by them.

**Scope evidence:** The module contains 169 files, including 29 Python, 29 XML, and 27 JavaScript/TypeScript files. The manifest declares dependencies: `hr`, `hr_work_entry`, `barcodes`, `base_geolocalize`.

## 2. Module structure

- Model/business logic files: 11
- Controller/API files: 2
- XML/data/view/template files: 29
- Browser asset files: 27
- Security files: 2
- Test files: 13
- Scheduled/automation evidence files: 5
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr_attendance/security/ir.access.csv`, `addons/hr_attendance/security/hr_attendance_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 11 model declarations, 191 methods, 3 constraint handlers, 0 onchange handlers, and 17 dependency declarations.
- **Evidence:** `addons/hr_attendance/models/res_groups.py:6`, `addons/hr_attendance/models/res_config_settings.py:6`, `addons/hr_attendance/models/hr_employee_public.py:7`, `addons/hr_attendance/models/ir_websocket.py:6`, `addons/hr_attendance/models/hr_version.py:6`, `addons/hr_attendance/models/hr_time_rule.py:6`, `addons/hr_attendance/models/hr_attendance.py:22`, `addons/hr_attendance/models/ir_http.py:6`, `addons/hr_attendance/models/res_users.py:7`, `addons/hr_attendance/models/hr_employee.py:13`, `addons/hr_attendance/models/res_company.py:13`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 15 route declarations.
- **Evidence:** `addons/hr_attendance/controllers/main.py:204`, `addons/hr_attendance/controllers/main.py:218`, `addons/hr_attendance/controllers/main.py:234`, `addons/hr_attendance/controllers/main.py:244`, `addons/hr_attendance/controllers/main.py:272`, `addons/hr_attendance/controllers/main.py:293`, `addons/hr_attendance/controllers/main.py:298`, `addons/hr_attendance/controllers/main.py:345`, `addons/hr_attendance/controllers/main.py:355`, `addons/hr_attendance/controllers/main.py:372`, `addons/hr_attendance/controllers/main.py:395`, `addons/hr_attendance/controllers/main.py:438`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 29 XML files and 27 JavaScript/TypeScript files; static XML analysis found 93 record/template/menu identifiers.
- **Evidence:** `addons/hr_attendance/security/hr_attendance_security.xml:2`, `addons/hr_attendance/security/hr_attendance_security.xml:8`, `addons/hr_attendance/security/hr_attendance_security.xml:13`, `addons/hr_attendance/security/hr_attendance_security.xml:17`, `addons/hr_attendance/security/hr_attendance_security.xml:25`, `addons/hr_attendance/security/hr_attendance_security.xml:32`, `addons/hr_attendance/security/hr_attendance_security.xml:40`, `addons/hr_attendance/security/hr_attendance_security.xml:48`, `addons/hr_attendance/data/hr_attendance_data.xml:4`, `addons/hr_attendance/data/hr_attendance_data.xml:13`, `addons/hr_attendance/data/hr_attendance_data.xml:22`, `addons/hr_attendance/data/hr_attendance_data.xml:31`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/hr_attendance/security/ir.access.csv`, `addons/hr_attendance/security/hr_attendance_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 5 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/hr_attendance/models/hr_attendance.py`, `addons/hr_attendance/data/hr_attendance_data.xml`, `addons/hr_attendance/views/hr_attendance_view.xml`, `addons/hr_attendance/views/hr_employee_view.xml`, `addons/hr_attendance/tests/test_hr_attendance_process.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/hr_attendance/controllers/main.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 13 test files are present.
- **Evidence:** `addons/hr_attendance/tests/test_hr_time_rule_pipeline.py`, `addons/hr_attendance/tests/test_load_scenario.py`, `addons/hr_attendance/tests/test_hr_attendance_manager.py`, `addons/hr_attendance/tests/test_hr_attendance_kiosk.py`, `addons/hr_attendance/tests/test_hr_attendance_process.py`, `addons/hr_attendance/tests/test_hr_attendance_domain_translation.py`, `addons/hr_attendance/tests/test_hr_attendance_work_entry_type_domain.py`, `addons/hr_attendance/tests/test_oman_overtime.py`, `addons/hr_attendance/tests/test_hr_attendance_systray.py`, `addons/hr_attendance/tests/__init__.py`, `addons/hr_attendance/tests/test_hr_attendance_constraints.py`, `addons/hr_attendance/tests/test_hr_attendance_access_rights.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 29; representative identifiers: `res_groups_privilege_attendances`, `group_hr_attendance_own_reader`, `base.group_user`, `group_hr_attendance_own`, `group_hr_attendance_officer`, `group_hr_attendance_user`, `group_hr_attendance_manager`, `base.default_user_group`, `hr_attendance_check_out_cron`, `hr_attendance_absence_cron`, `hr_attendance_day_undertime_rules_cron`, `hr_attendance_week_time_rules_cron`, `base.user_demo`, `base.user_light`, `base.default_user_group`, `hr.employee_al`, `hr.employee_admin`, `hr.employee_hne`, `hr.employee_mit`, `hr.employee_chs`
- Menus: 14; representative evidence: `addons/hr_attendance/views/res_config_settings_views.xml:99`, `addons/hr_attendance/views/hr_attendance_view.xml:588`, `addons/hr_attendance/views/hr_attendance_view.xml:590`, `addons/hr_attendance/views/hr_attendance_view.xml:592`, `addons/hr_attendance/views/hr_attendance_view.xml:599`, `addons/hr_attendance/views/hr_attendance_view.xml:606`, `addons/hr_attendance/views/hr_attendance_view.xml:608`, `addons/hr_attendance/views/hr_attendance_view.xml:610`, `addons/hr_attendance/views/hr_attendance_view.xml:612`, `addons/hr_attendance/views/hr_attendance_view.xml:634`, `addons/hr_attendance/views/hr_attendance_view.xml:636`, `addons/hr_attendance/views/hr_attendance_view.xml:638`
- Templates: 1; representative evidence: `addons/hr_attendance/views/hr_attendance_kiosk_templates.xml:3`
- View/action field declarations: 58; representative evidence: `addons/hr_attendance/data/hr_attendance_demo.xml:125`, `addons/hr_attendance/views/res_config_settings_views.xml:5`, `addons/hr_attendance/views/res_config_settings_views.xml:8`, `addons/hr_attendance/views/res_config_settings_views.xml:94`, `addons/hr_attendance/views/res_config_settings_views.xml:95`, `addons/hr_attendance/views/hr_attendance_view.xml:8`, `addons/hr_attendance/views/hr_attendance_view.xml:9`, `addons/hr_attendance/views/hr_attendance_view.xml:53`, `addons/hr_attendance/views/hr_attendance_view.xml:54`, `addons/hr_attendance/views/hr_attendance_view.xml:80`, `addons/hr_attendance/views/hr_attendance_view.xml:82`, `addons/hr_attendance/views/hr_attendance_view.xml:229`
- Browser assets: 27; representative files: `addons/hr_attendance/static/tests/attendance_menu.test.js`, `addons/hr_attendance/static/tests/attendance_calendar_overview.test.js`, `addons/hr_attendance/static/tests/hr_attendance_kiosk_barcode_scanner.test.js`, `addons/hr_attendance/static/tests/greetings.test.js`, `addons/hr_attendance/static/tests/employee_presence_state.test.js`, `addons/hr_attendance/static/src/public_kiosk/public_kiosk_app.js`, `addons/hr_attendance/static/src/views/attendance_list_view.js`, `addons/hr_attendance/static/src/views/attendance_helper_view.js`, `addons/hr_attendance/static/src/components/hr_presence_status/hr_attendance_presence_status.js`, `addons/hr_attendance/static/src/components/attendance_video_stream/attendance_video_stream.js`, `addons/hr_attendance/static/src/components/card_layout/card_layout.js`, `addons/hr_attendance/static/src/components/break_duration_dialog/break_duration_dialog.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_attendance/__manifest__.py`
- **HTTP entry points:** `addons/hr_attendance/controllers/main.py:204`, `addons/hr_attendance/controllers/main.py:218`, `addons/hr_attendance/controllers/main.py:234`, `addons/hr_attendance/controllers/main.py:244`, `addons/hr_attendance/controllers/main.py:272`, `addons/hr_attendance/controllers/main.py:293`, `addons/hr_attendance/controllers/main.py:298`, `addons/hr_attendance/controllers/main.py:345`, `addons/hr_attendance/controllers/main.py:355`, `addons/hr_attendance/controllers/main.py:372`, `addons/hr_attendance/controllers/main.py:395`, `addons/hr_attendance/controllers/main.py:438`
- **Scheduled entry points:** `addons/hr_attendance/models/hr_attendance.py`, `addons/hr_attendance/data/hr_attendance_data.xml`, `addons/hr_attendance/views/hr_attendance_view.xml`, `addons/hr_attendance/views/hr_employee_view.xml`, `addons/hr_attendance/tests/test_hr_attendance_process.py`
- **Report entry points:** `addons/hr_attendance/controllers/main.py`

## 7. Database interactions

- Model declarations: 11
- Representative model evidence: inherits `res.groups` (addons/hr_attendance/models/res_groups.py:6); inherits `res.config.settings` (addons/hr_attendance/models/res_config_settings.py:6); inherits `hr.employee.public` (addons/hr_attendance/models/hr_employee_public.py:7); inherits `ir.websocket` (addons/hr_attendance/models/ir_websocket.py:6); `hr.version` (addons/hr_attendance/models/hr_version.py:6); inherits `hr.time.rule` (addons/hr_attendance/models/hr_time_rule.py:6); `hr.attendance` (addons/hr_attendance/models/hr_attendance.py:22); inherits `ir.http` (addons/hr_attendance/models/ir_http.py:6); inherits `res.users` (addons/hr_attendance/models/res_users.py:7); inherits `hr.employee` (addons/hr_attendance/models/hr_employee.py:13); inherits `res.company` (addons/hr_attendance/models/res_company.py:13)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 15
- Route evidence: `addons/hr_attendance/controllers/main.py:204`, `addons/hr_attendance/controllers/main.py:218`, `addons/hr_attendance/controllers/main.py:234`, `addons/hr_attendance/controllers/main.py:244`, `addons/hr_attendance/controllers/main.py:272`, `addons/hr_attendance/controllers/main.py:293`, `addons/hr_attendance/controllers/main.py:298`, `addons/hr_attendance/controllers/main.py:345`, `addons/hr_attendance/controllers/main.py:355`, `addons/hr_attendance/controllers/main.py:372`, `addons/hr_attendance/controllers/main.py:395`, `addons/hr_attendance/controllers/main.py:438`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr`, `hr_work_entry`, `barcodes`, `base_geolocalize`
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

- `addons/hr_attendance/__init__.py`
- `addons/hr_attendance/__manifest__.py`
- `addons/hr_attendance/controllers/__init__.py`
- `addons/hr_attendance/controllers/main.py`
- `addons/hr_attendance/data/hr_attendance_data.xml`
- `addons/hr_attendance/data/hr_attendance_demo.xml`
- `addons/hr_attendance/data/scenarios/hr_attendance_scenario.xml`
- `addons/hr_attendance/i18n/af.po`
- `addons/hr_attendance/i18n/am.po`
- `addons/hr_attendance/i18n/ar.po`
- `addons/hr_attendance/i18n/az.po`
- `addons/hr_attendance/i18n/bg.po`
- `addons/hr_attendance/i18n/bs.po`
- `addons/hr_attendance/i18n/ca.po`
- `addons/hr_attendance/i18n/cs.po`
- `addons/hr_attendance/i18n/da.po`
- `addons/hr_attendance/i18n/de.po`
- `addons/hr_attendance/i18n/el.po`
- `addons/hr_attendance/i18n/es.po`
- `addons/hr_attendance/i18n/es_419.po`
- `addons/hr_attendance/i18n/es_CL.po`
- `addons/hr_attendance/i18n/et.po`
- `addons/hr_attendance/i18n/eu.po`
- `addons/hr_attendance/i18n/fa.po`
- `addons/hr_attendance/i18n/fi.po`
- `addons/hr_attendance/i18n/fo.po`
- `addons/hr_attendance/i18n/fr.po`
- `addons/hr_attendance/i18n/fr_BE.po`
- `addons/hr_attendance/i18n/fr_CA.po`
- `addons/hr_attendance/i18n/gl.po`
- `addons/hr_attendance/i18n/gu.po`
- `addons/hr_attendance/i18n/he.po`
- `addons/hr_attendance/i18n/hi.po`
- `addons/hr_attendance/i18n/hr.po`
- `addons/hr_attendance/i18n/hr_attendance.pot`
- `addons/hr_attendance/i18n/hu.po`
- `addons/hr_attendance/i18n/hy.po`
- `addons/hr_attendance/i18n/id.po`
- `addons/hr_attendance/i18n/is.po`
- `addons/hr_attendance/i18n/it.po`
- `addons/hr_attendance/i18n/ja.po`
- `addons/hr_attendance/i18n/ka.po`
- `addons/hr_attendance/i18n/kab.po`
- `addons/hr_attendance/i18n/km.po`
- `addons/hr_attendance/i18n/ko.po`
- `addons/hr_attendance/i18n/ku.po`
- `addons/hr_attendance/i18n/lb.po`
- `addons/hr_attendance/i18n/lo.po`
- `addons/hr_attendance/i18n/lt.po`
- `addons/hr_attendance/i18n/lv.po`
- `addons/hr_attendance/i18n/mk.po`
- `addons/hr_attendance/i18n/mn.po`
- `addons/hr_attendance/i18n/my.po`
- `addons/hr_attendance/i18n/nb.po`
- `addons/hr_attendance/i18n/nl.po`
- `addons/hr_attendance/i18n/pl.po`
- `addons/hr_attendance/i18n/pt.po`
- `addons/hr_attendance/i18n/pt_BR.po`
- `addons/hr_attendance/i18n/ro.po`
- `addons/hr_attendance/i18n/ru.po`
- `addons/hr_attendance/i18n/sk.po`
- `addons/hr_attendance/i18n/sl.po`
- `addons/hr_attendance/i18n/sq.po`
- `addons/hr_attendance/i18n/sr@latin.po`
- `addons/hr_attendance/i18n/sv.po`
- `addons/hr_attendance/i18n/ta.po`
- `addons/hr_attendance/i18n/th.po`
- `addons/hr_attendance/i18n/tr.po`
- `addons/hr_attendance/i18n/uk.po`
- `addons/hr_attendance/i18n/uz.po`
- `addons/hr_attendance/i18n/vi.po`
- `addons/hr_attendance/i18n/zh_CN.po`
- `addons/hr_attendance/i18n/zh_TW.po`
- `addons/hr_attendance/models/__init__.py`
- `addons/hr_attendance/models/hr_attendance.py`
- `addons/hr_attendance/models/hr_employee.py`
- `addons/hr_attendance/models/hr_employee_public.py`
- `addons/hr_attendance/models/hr_time_rule.py`
- `addons/hr_attendance/models/hr_version.py`
- `addons/hr_attendance/models/ir_http.py`
- `addons/hr_attendance/models/ir_websocket.py`
- `addons/hr_attendance/models/res_company.py`
- `addons/hr_attendance/models/res_config_settings.py`
- `addons/hr_attendance/models/res_groups.py`
- `addons/hr_attendance/models/res_users.py`
- `addons/hr_attendance/security/hr_attendance_security.xml`
- `addons/hr_attendance/security/ir.access.csv`
- `addons/hr_attendance/static/description/icon.png`
- `addons/hr_attendance/static/description/icon.svg`
- `addons/hr_attendance/static/description/icon_hi.png`
- `addons/hr_attendance/static/img/attendance_dot.gif`
- `addons/hr_attendance/static/img/background-light.svg`
- `addons/hr_attendance/static/img/employee_awa-image.jpg`
- `addons/hr_attendance/static/img/mock-tablet.png`
- `addons/hr_attendance/static/img/partner_root-image.jpg`
- `addons/hr_attendance/static/img/tablet-cam.svg`
- `addons/hr_attendance/static/img/tablet-pin.svg`
- `addons/hr_attendance/static/img/tablet-rfid.svg`
- `addons/hr_attendance/static/src/components/attendance_calendar/attendance_calendar_overview.js`
- `addons/hr_attendance/static/src/components/attendance_calendar/attendance_calendar_overview.xml`
- `addons/hr_attendance/static/src/components/attendance_inline_form/attendance_inline_form.js`
- `addons/hr_attendance/static/src/components/attendance_inline_form/attendance_inline_form.xml`
- `addons/hr_attendance/static/src/components/attendance_menu/attendance_menu.js`
- `addons/hr_attendance/static/src/components/attendance_menu/attendance_menu.xml`
- `addons/hr_attendance/static/src/components/attendance_video_stream/attendance_video_steam.xml`
- `addons/hr_attendance/static/src/components/attendance_video_stream/attendance_video_stream.js`
- `addons/hr_attendance/static/src/components/break_duration_dialog/break_duration_dialog.js`
- `addons/hr_attendance/static/src/components/break_duration_dialog/break_duration_dialog.xml`
- `addons/hr_attendance/static/src/components/card_layout/card_layout.js`
- `addons/hr_attendance/static/src/components/card_layout/card_layout.xml`
- `addons/hr_attendance/static/src/components/confirmation/confirmation.js`
- `addons/hr_attendance/static/src/components/confirmation/confirmation.xml`
- `addons/hr_attendance/static/src/components/greetings/greetings.js`
- `addons/hr_attendance/static/src/components/greetings/greetings.xml`
- `addons/hr_attendance/static/src/components/hooks/use_camera.js`
- `addons/hr_attendance/static/src/components/hr_presence_status/hr_attendance_presence_status.js`
- `addons/hr_attendance/static/src/components/kiosk_barcode/kiosk_barcode.js`
- `addons/hr_attendance/static/src/components/manual_selection/manual_selection.js`
- `addons/hr_attendance/static/src/components/manual_selection/manual_selection.xml`
- `addons/hr_attendance/static/src/components/new_employee_dialog/many2one/many2one.js`
- `addons/hr_attendance/static/src/components/new_employee_dialog/many2one/many2one.xml`
- `addons/hr_attendance/static/src/components/new_employee_dialog/new_employee_dialog.js`
- `addons/hr_attendance/static/src/components/new_employee_dialog/new_employee_dialog.xml`
- `addons/hr_attendance/static/src/components/pin_code/pin_code.js`
- `addons/hr_attendance/static/src/components/pin_code/pin_code.xml`
- `addons/hr_attendance/static/src/public_kiosk/public_kiosk_app.js`
- `addons/hr_attendance/static/src/public_kiosk/public_kiosk_app.xml`
- `addons/hr_attendance/static/src/scss/kiosk/bootstrap_overridden.scss`
- `addons/hr_attendance/static/src/scss/kiosk/hr_attendance.scss`
- `addons/hr_attendance/static/src/scss/kiosk/primary_variables.scss`
- `addons/hr_attendance/static/src/scss/views/attendance_calendar.scss`
- `addons/hr_attendance/static/src/scss/views/badge_scanner.scss`
- `addons/hr_attendance/static/src/scss/views/hr_attendance.scss`
- `addons/hr_attendance/static/src/views/attendance_helper_view.js`
- `addons/hr_attendance/static/src/views/attendance_helper_view.xml`
- `addons/hr_attendance/static/src/views/attendance_list_view.js`
- `addons/hr_attendance/static/src/views/attendance_list_view.xml`
- `addons/hr_attendance/static/src/views/badge_scanner/badge_scanner.js`
- `addons/hr_attendance/static/src/views/badge_scanner/badge_scanner.xml`
- `addons/hr_attendance/static/src/views/calendar/attendance_calendar_controller.js`
- `addons/hr_attendance/static/src/views/calendar/attendance_calendar_renderer.js`
- `addons/hr_attendance/static/src/views/calendar/attendance_calendar_renderer.xml`
- `addons/hr_attendance/static/src/views/calendar/attendance_calendar_view.js`
- `addons/hr_attendance/static/tests/attendance_calendar_overview.test.js`
- `addons/hr_attendance/static/tests/attendance_menu.test.js`
- `addons/hr_attendance/static/tests/employee_presence_state.test.js`
- `addons/hr_attendance/static/tests/greetings.test.js`
- `addons/hr_attendance/static/tests/hr_attendance_kiosk_barcode_scanner.test.js`
- `addons/hr_attendance/tests/__init__.py`
- `addons/hr_attendance/tests/test_hr_attendance_access_rights.py`
- `addons/hr_attendance/tests/test_hr_attendance_constraints.py`
- `addons/hr_attendance/tests/test_hr_attendance_domain_translation.py`
- `addons/hr_attendance/tests/test_hr_attendance_kiosk.py`
- `addons/hr_attendance/tests/test_hr_attendance_manager.py`
- `addons/hr_attendance/tests/test_hr_attendance_process.py`
- `addons/hr_attendance/tests/test_hr_attendance_self_edit_role.py`
- `addons/hr_attendance/tests/test_hr_attendance_systray.py`
- `addons/hr_attendance/tests/test_hr_attendance_work_entry_type_domain.py`
- `addons/hr_attendance/tests/test_hr_time_rule_pipeline.py`
- `addons/hr_attendance/tests/test_load_scenario.py`
- `addons/hr_attendance/tests/test_oman_overtime.py`
- `addons/hr_attendance/views/hr_attendance_kiosk_templates.xml`
- `addons/hr_attendance/views/hr_attendance_view.xml`
- `addons/hr_attendance/views/hr_contract_template_views.xml`
- `addons/hr_attendance/views/hr_department_view.xml`
- `addons/hr_attendance/views/hr_employee_public_views.xml`
- `addons/hr_attendance/views/hr_employee_view.xml`
- `addons/hr_attendance/views/hr_version_views.xml`
- `addons/hr_attendance/views/res_config_settings_views.xml`
