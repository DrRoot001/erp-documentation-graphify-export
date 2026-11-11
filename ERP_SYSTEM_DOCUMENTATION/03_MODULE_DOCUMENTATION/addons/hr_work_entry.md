# Module: hr_work_entry

- **Module ID:** MOD-104
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_work_entry`
- **Manifest:** `addons/hr_work_entry/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources/Employees`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Manage work entries

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 97 files, including 23 Python, 15 XML, and 5 JavaScript/TypeScript files. The manifest declares dependencies: `hr`.

## 2. Module structure

- Model/business logic files: 13
- Controller/API files: 2
- XML/data/view/template files: 15
- Browser asset files: 5
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 2
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr_work_entry/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 13 model declarations, 135 methods, 4 constraint handlers, 0 onchange handlers, and 18 dependency declarations.
- **Evidence:** `addons/hr_work_entry/models/hr_time_rule_source_mixin.py:28`, `addons/hr_work_entry/models/res_config_settings.py:6`, `addons/hr_work_entry/models/hr_work_entry_type.py:9`, `addons/hr_work_entry/models/hr_version.py:17`, `addons/hr_work_entry/models/hr_time_rule.py:133`, `addons/hr_work_entry/models/resource_calendar.py:6`, `addons/hr_work_entry/models/resource_calendar_attendance.py:10`, `addons/hr_work_entry/models/hr_user_work_entry_employee.py:6`, `addons/hr_work_entry/models/resource_calendar_leaves.py:6`, `addons/hr_work_entry/models/hr_employee.py:6`, `addons/hr_work_entry/models/res_company.py:6`, `addons/hr_work_entry/wizard/hr_export_work_entries.py:11`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/hr_work_entry/controllers/main.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 15 XML files and 5 JavaScript/TypeScript files; static XML analysis found 712 record/template/menu identifiers.
- **Evidence:** `addons/hr_work_entry/wizard/hr_work_entry_export_views.xml:4`, `addons/hr_work_entry/wizard/hr_work_entry_export_views.xml:13`, `addons/hr_work_entry/data/hr_time_rule_data.xml:4`, `addons/hr_work_entry/data/hr_time_rule_data.xml:19`, `addons/hr_work_entry/data/hr_time_rule_data.xml:30`, `addons/hr_work_entry/data/hr_time_rule_data.xml:46`, `addons/hr_work_entry/data/hr_time_rule_data.xml:69`, `addons/hr_work_entry/data/hr_time_rule_data.xml:89`, `addons/hr_work_entry/data/hr_time_rule_data.xml:109`, `addons/hr_work_entry/data/hr_time_rule_data.xml:133`, `addons/hr_work_entry/data/hr_time_rule_data.xml:153`, `addons/hr_work_entry/data/hr_time_rule_data.xml:173`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/hr_work_entry/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/hr_work_entry/models/hr_time_rule_source_mixin.py`, `addons/hr_work_entry/views/hr_employee_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/hr_work_entry/tests/test_work_entry.py`, `addons/hr_work_entry/tests/test_work_entry_type.py`, `addons/hr_work_entry/tests/test_work_entry_type_data.py`, `addons/hr_work_entry/tests/common.py`, `addons/hr_work_entry/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 15; representative identifiers: `action_open_export_wizard`, `hr_export_work_entries_wizard`, `hr_time_rule_employee_schedule`, `hr_time_rule_l10n_id_beyond_first_hour`, `hr_time_rule_l10n_id_first_hour`, `hr_time_rule_l10n_sa_workdays`, `hr_time_rule_l10n_jo_public_holidays`, `hr_time_rule_l10n_jo_rest_days`, `hr_time_rule_l10n_jo_week_days`, `hr_time_rule_l10n_eg_work_days_daytime`, `hr_time_rule_l10n_eg_work_days_nighttime_evening`, `hr_time_rule_l10n_eg_work_days_nighttime_early`, `hr_time_rule_l10n_eg_public_holidays`, `hr_time_rule_l10n_eg_rest_days`, `hr_time_rule_l10n_iq_day_time_1`, `hr_time_rule_l10n_iq_day_time_2`, `hr_time_rule_l10n_iq_night_time_1`, `hr_time_rule_l10n_iq_night_time_2`, `hr_time_rule_l10n_ae_day_time`, `hr_time_rule_l10n_ae_night_time_1`
- Menus: 1; representative evidence: `addons/hr_work_entry/views/menuitems.xml:4`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 40; representative evidence: `addons/hr_work_entry/wizard/hr_work_entry_export_views.xml:6`, `addons/hr_work_entry/wizard/hr_work_entry_export_views.xml:7`, `addons/hr_work_entry/wizard/hr_work_entry_export_views.xml:15`, `addons/hr_work_entry/wizard/hr_work_entry_export_views.xml:16`, `addons/hr_work_entry/views/hr_time_rule_views.xml:5`, `addons/hr_work_entry/views/hr_time_rule_views.xml:6`, `addons/hr_work_entry/views/hr_time_rule_views.xml:12`, `addons/hr_work_entry/views/hr_time_rule_views.xml:13`, `addons/hr_work_entry/views/hr_time_rule_views.xml:123`, `addons/hr_work_entry/views/hr_time_rule_views.xml:124`, `addons/hr_work_entry/views/hr_time_rule_views.xml:140`, `addons/hr_work_entry/views/hr_time_rule_views.xml:141`
- Browser assets: 5; representative files: `addons/hr_work_entry/static/tests/work_entry_type_field.test.js`, `addons/hr_work_entry/static/src/export_cog_menu/export_cog_menu.js`, `addons/hr_work_entry/static/src/components/work_entry_type_field/work_entry_type_field.js`, `addons/hr_work_entry/static/src/components/domain_count_field/domain_count_field.js`, `addons/hr_work_entry/static/src/search/hr_work_entry_action_menus/hr_work_entry_action_menus.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_work_entry/__manifest__.py`
- **HTTP entry points:** `addons/hr_work_entry/controllers/main.py:7`
- **Scheduled entry points:** `addons/hr_work_entry/models/hr_time_rule_source_mixin.py`, `addons/hr_work_entry/views/hr_employee_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 13
- Representative model evidence: `hr.time.rule.source.mixin` (addons/hr_work_entry/models/hr_time_rule_source_mixin.py:28); inherits `res.config.settings` (addons/hr_work_entry/models/res_config_settings.py:6); `hr.work.entry.type` (addons/hr_work_entry/models/hr_work_entry_type.py:9); inherits `hr.version` (addons/hr_work_entry/models/hr_version.py:17); `hr.time.rule` (addons/hr_work_entry/models/hr_time_rule.py:133); inherits `resource.calendar` (addons/hr_work_entry/models/resource_calendar.py:6); inherits `resource.calendar.attendance` (addons/hr_work_entry/models/resource_calendar_attendance.py:10); `hr.user.work.entry.employee` (addons/hr_work_entry/models/hr_user_work_entry_employee.py:6); inherits `resource.calendar.leaves` (addons/hr_work_entry/models/resource_calendar_leaves.py:6); inherits `hr.employee` (addons/hr_work_entry/models/hr_employee.py:6); inherits `res.company` (addons/hr_work_entry/models/res_company.py:6); `hr.export.work.entries` (addons/hr_work_entry/wizard/hr_export_work_entries.py:11); `hr.export.work.entries.employee` (addons/hr_work_entry/wizard/hr_export_work_entries.py:176)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/hr_work_entry/controllers/main.py:7`
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

- `addons/hr_work_entry/__init__.py`
- `addons/hr_work_entry/__manifest__.py`
- `addons/hr_work_entry/controllers/__init__.py`
- `addons/hr_work_entry/controllers/main.py`
- `addons/hr_work_entry/data/hr_time_rule_data.xml`
- `addons/hr_work_entry/data/hr_work_entry_demo.xml`
- `addons/hr_work_entry/data/hr_work_entry_type_data.xml`
- `addons/hr_work_entry/i18n/ar.po`
- `addons/hr_work_entry/i18n/az.po`
- `addons/hr_work_entry/i18n/bg.po`
- `addons/hr_work_entry/i18n/bs.po`
- `addons/hr_work_entry/i18n/ca.po`
- `addons/hr_work_entry/i18n/cs.po`
- `addons/hr_work_entry/i18n/da.po`
- `addons/hr_work_entry/i18n/de.po`
- `addons/hr_work_entry/i18n/el.po`
- `addons/hr_work_entry/i18n/en_AU.po`
- `addons/hr_work_entry/i18n/es.po`
- `addons/hr_work_entry/i18n/es_419.po`
- `addons/hr_work_entry/i18n/et.po`
- `addons/hr_work_entry/i18n/fa.po`
- `addons/hr_work_entry/i18n/fi.po`
- `addons/hr_work_entry/i18n/fr.po`
- `addons/hr_work_entry/i18n/he.po`
- `addons/hr_work_entry/i18n/hi.po`
- `addons/hr_work_entry/i18n/hr.po`
- `addons/hr_work_entry/i18n/hr_work_entry.pot`
- `addons/hr_work_entry/i18n/hu.po`
- `addons/hr_work_entry/i18n/id.po`
- `addons/hr_work_entry/i18n/it.po`
- `addons/hr_work_entry/i18n/ja.po`
- `addons/hr_work_entry/i18n/kab.po`
- `addons/hr_work_entry/i18n/ko.po`
- `addons/hr_work_entry/i18n/ku.po`
- `addons/hr_work_entry/i18n/lo.po`
- `addons/hr_work_entry/i18n/lt.po`
- `addons/hr_work_entry/i18n/lv.po`
- `addons/hr_work_entry/i18n/mn.po`
- `addons/hr_work_entry/i18n/my.po`
- `addons/hr_work_entry/i18n/nb.po`
- `addons/hr_work_entry/i18n/nl.po`
- `addons/hr_work_entry/i18n/pl.po`
- `addons/hr_work_entry/i18n/pt.po`
- `addons/hr_work_entry/i18n/pt_BR.po`
- `addons/hr_work_entry/i18n/ro.po`
- `addons/hr_work_entry/i18n/ru.po`
- `addons/hr_work_entry/i18n/sk.po`
- `addons/hr_work_entry/i18n/sl.po`
- `addons/hr_work_entry/i18n/sr@latin.po`
- `addons/hr_work_entry/i18n/sv.po`
- `addons/hr_work_entry/i18n/th.po`
- `addons/hr_work_entry/i18n/tr.po`
- `addons/hr_work_entry/i18n/uk.po`
- `addons/hr_work_entry/i18n/uz.po`
- `addons/hr_work_entry/i18n/vi.po`
- `addons/hr_work_entry/i18n/zh_CN.po`
- `addons/hr_work_entry/i18n/zh_TW.po`
- `addons/hr_work_entry/models/__init__.py`
- `addons/hr_work_entry/models/hr_employee.py`
- `addons/hr_work_entry/models/hr_time_rule.py`
- `addons/hr_work_entry/models/hr_time_rule_source_mixin.py`
- `addons/hr_work_entry/models/hr_user_work_entry_employee.py`
- `addons/hr_work_entry/models/hr_version.py`
- `addons/hr_work_entry/models/hr_work_entry_type.py`
- `addons/hr_work_entry/models/res_company.py`
- `addons/hr_work_entry/models/res_config_settings.py`
- `addons/hr_work_entry/models/resource_calendar.py`
- `addons/hr_work_entry/models/resource_calendar_attendance.py`
- `addons/hr_work_entry/models/resource_calendar_leaves.py`
- `addons/hr_work_entry/security/ir.access.csv`
- `addons/hr_work_entry/static/description/icon.png`
- `addons/hr_work_entry/static/description/icon.svg`
- `addons/hr_work_entry/static/description/icon_hi.png`
- `addons/hr_work_entry/static/src/components/domain_count_field/domain_count_field.js`
- `addons/hr_work_entry/static/src/components/domain_count_field/domain_count_field.xml`
- `addons/hr_work_entry/static/src/components/resource_calendar_attendance_popover/resource_calendar_attendance_popover.xml`
- `addons/hr_work_entry/static/src/components/work_entry_type_field/work_entry_type_field.js`
- `addons/hr_work_entry/static/src/components/work_entry_type_field/work_entry_type_field.xml`
- `addons/hr_work_entry/static/src/export_cog_menu/export_cog_menu.js`
- `addons/hr_work_entry/static/src/export_cog_menu/export_cog_menu.xml`
- `addons/hr_work_entry/static/src/search/hr_work_entry_action_menus/hr_work_entry_action_menus.js`
- `addons/hr_work_entry/static/src/search/hr_work_entry_action_menus/hr_work_entry_action_menus.xml`
- `addons/hr_work_entry/static/tests/work_entry_type_field.test.js`
- `addons/hr_work_entry/tests/__init__.py`
- `addons/hr_work_entry/tests/common.py`
- `addons/hr_work_entry/tests/test_work_entry.py`
- `addons/hr_work_entry/tests/test_work_entry_type.py`
- `addons/hr_work_entry/tests/test_work_entry_type_data.py`
- `addons/hr_work_entry/views/hr_employee_views.xml`
- `addons/hr_work_entry/views/hr_time_rule_views.xml`
- `addons/hr_work_entry/views/hr_work_entry_type_views.xml`
- `addons/hr_work_entry/views/menuitems.xml`
- `addons/hr_work_entry/views/res_company_views.xml`
- `addons/hr_work_entry/views/resource_calendar_views.xml`
- `addons/hr_work_entry/wizard/__init__.py`
- `addons/hr_work_entry/wizard/hr_export_work_entries.py`
- `addons/hr_work_entry/wizard/hr_work_entry_export_views.xml`
