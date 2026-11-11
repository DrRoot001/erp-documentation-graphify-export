# Module: hr_presence

- **Module ID:** MOD-093
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_presence`
- **Manifest:** `addons/hr_presence/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Control Employees Presence
==========================

Based on:
    * The IP Address
    * The User's Session
    * The Sent Emails

Allows to contact directly the employee in case of unjustified absence.

**Scope evidence:** The module contains 68 files, including 9 Python, 6 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `hr`, `hr_holidays`, `sms`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 3
- Security files: 1
- Test files: 0
- Scheduled/automation evidence files: 4
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr_presence/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 10 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/hr_presence/models/res_config_settings.py:4`, `addons/hr_presence/models/hr_employee_public.py:6`, `addons/hr_presence/models/ir_websocket.py:11`, `addons/hr_presence/models/res_users_log.py:6`, `addons/hr_presence/models/hr_employee.py:13`, `addons/hr_presence/models/res_company.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 3 JavaScript/TypeScript files; static XML analysis found 8 record/template/menu identifiers.
- **Evidence:** `addons/hr_presence/data/ir_cron.xml:4`, `addons/hr_presence/data/mail_template_data.xml:4`, `addons/hr_presence/data/sms_data.xml:4`, `addons/hr_presence/views/hr_employee_views.xml:3`, `addons/hr_presence/views/hr_employee_views.xml:14`, `addons/hr_presence/views/hr_employee_views.xml:29`, `addons/hr_presence/views/hr_employee_views.xml:44`, `addons/hr_presence/views/hr_employee_views.xml:58`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/hr_presence/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 4 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/hr_presence/__manifest__.py`, `addons/hr_presence/models/hr_employee.py`, `addons/hr_presence/data/ir_cron.xml`, `addons/hr_presence/views/hr_employee_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `ir_cron_presence_control`, `mail_template_presence`, `sms_template_data_hr_presence`, `hr_employee_view_search`, `action_hr_employee_presence_present`, `action_hr_employee_presence_absent`, `action_hr_employee_presence_sms`, `action_hr_employee_presence_time_off`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/hr_presence/views/hr_employee_views.xml:5`, `addons/hr_presence/views/hr_employee_views.xml:7`
- Browser assets: 3; representative files: `addons/hr_presence/static/src/presence_cog_menu/presence_cog_menu.js`, `addons/hr_presence/static/src/views/hooks.js`, `addons/hr_presence/static/src/search/hr_presence_action_menus/hr_presence_action_menus.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_presence/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/hr_presence/__manifest__.py`, `addons/hr_presence/models/hr_employee.py`, `addons/hr_presence/data/ir_cron.xml`, `addons/hr_presence/views/hr_employee_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `res.config.settings` (addons/hr_presence/models/res_config_settings.py:4); inherits `hr.employee.public` (addons/hr_presence/models/hr_employee_public.py:6); inherits `ir.websocket` (addons/hr_presence/models/ir_websocket.py:11); inherits `res.users.log` (addons/hr_presence/models/res_users_log.py:6); inherits `hr.employee` (addons/hr_presence/models/hr_employee.py:13); inherits `res.company` (addons/hr_presence/models/res_company.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr`, `hr_holidays`, `sms`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Present
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/hr_presence/__init__.py`
- `addons/hr_presence/__manifest__.py`
- `addons/hr_presence/data/ir_cron.xml`
- `addons/hr_presence/data/mail_template_data.xml`
- `addons/hr_presence/data/sms_data.xml`
- `addons/hr_presence/i18n/ar.po`
- `addons/hr_presence/i18n/az.po`
- `addons/hr_presence/i18n/bg.po`
- `addons/hr_presence/i18n/bs.po`
- `addons/hr_presence/i18n/ca.po`
- `addons/hr_presence/i18n/cs.po`
- `addons/hr_presence/i18n/da.po`
- `addons/hr_presence/i18n/de.po`
- `addons/hr_presence/i18n/el.po`
- `addons/hr_presence/i18n/es.po`
- `addons/hr_presence/i18n/es_419.po`
- `addons/hr_presence/i18n/et.po`
- `addons/hr_presence/i18n/fa.po`
- `addons/hr_presence/i18n/fi.po`
- `addons/hr_presence/i18n/fr.po`
- `addons/hr_presence/i18n/he.po`
- `addons/hr_presence/i18n/hi.po`
- `addons/hr_presence/i18n/hr.po`
- `addons/hr_presence/i18n/hr_presence.pot`
- `addons/hr_presence/i18n/hu.po`
- `addons/hr_presence/i18n/id.po`
- `addons/hr_presence/i18n/it.po`
- `addons/hr_presence/i18n/ja.po`
- `addons/hr_presence/i18n/kab.po`
- `addons/hr_presence/i18n/ko.po`
- `addons/hr_presence/i18n/ku.po`
- `addons/hr_presence/i18n/lo.po`
- `addons/hr_presence/i18n/lt.po`
- `addons/hr_presence/i18n/lv.po`
- `addons/hr_presence/i18n/mn.po`
- `addons/hr_presence/i18n/my.po`
- `addons/hr_presence/i18n/nb.po`
- `addons/hr_presence/i18n/nl.po`
- `addons/hr_presence/i18n/pl.po`
- `addons/hr_presence/i18n/pt.po`
- `addons/hr_presence/i18n/pt_BR.po`
- `addons/hr_presence/i18n/ro.po`
- `addons/hr_presence/i18n/ru.po`
- `addons/hr_presence/i18n/sk.po`
- `addons/hr_presence/i18n/sl.po`
- `addons/hr_presence/i18n/sr@latin.po`
- `addons/hr_presence/i18n/sv.po`
- `addons/hr_presence/i18n/th.po`
- `addons/hr_presence/i18n/tr.po`
- `addons/hr_presence/i18n/uk.po`
- `addons/hr_presence/i18n/uz.po`
- `addons/hr_presence/i18n/vi.po`
- `addons/hr_presence/i18n/zh_CN.po`
- `addons/hr_presence/i18n/zh_TW.po`
- `addons/hr_presence/models/__init__.py`
- `addons/hr_presence/models/hr_employee.py`
- `addons/hr_presence/models/hr_employee_public.py`
- `addons/hr_presence/models/ir_websocket.py`
- `addons/hr_presence/models/res_company.py`
- `addons/hr_presence/models/res_config_settings.py`
- `addons/hr_presence/models/res_users_log.py`
- `addons/hr_presence/security/ir.access.csv`
- `addons/hr_presence/static/src/presence_cog_menu/presence_cog_menu.js`
- `addons/hr_presence/static/src/presence_cog_menu/presence_cog_menu.xml`
- `addons/hr_presence/static/src/search/hr_presence_action_menus/hr_presence_action_menus.js`
- `addons/hr_presence/static/src/search/hr_presence_action_menus/hr_presence_action_menus.xml`
- `addons/hr_presence/static/src/views/hooks.js`
- `addons/hr_presence/views/hr_employee_views.xml`
