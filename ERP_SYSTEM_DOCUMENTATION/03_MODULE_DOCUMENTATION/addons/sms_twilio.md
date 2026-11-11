# Module: sms_twilio

- **Module ID:** MOD-540
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sms_twilio`
- **Manifest:** `addons/sms_twilio/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Send SMS messages using Twilio

**Manifest description:**

This module allows using Twilio as a provider for SMS messaging.
The user has to create an account on twilio.com and top
up their account to start sending SMS messages.

**Scope evidence:** The module contains 77 files, including 22 Python, 3 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `sms`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 2
- XML/data/view/template files: 3
- Browser asset files: 1
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/sms_twilio/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 41 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/sms_twilio/models/sms_sms.py:6`, `addons/sms_twilio/models/res_config_settings.py:4`, `addons/sms_twilio/models/sms_twilio_number.py:4`, `addons/sms_twilio/models/sms_composer.py:4`, `addons/sms_twilio/models/mail_notification.py:4`, `addons/sms_twilio/models/res_company.py:9`, `addons/sms_twilio/models/sms_tracker.py:4`, `addons/sms_twilio/wizard/sms_twilio_account_manage.py:12`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/sms_twilio/controllers/controllers.py:44`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 1 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/sms_twilio/wizard/sms_twilio_account_manage_views.xml:3`, `addons/sms_twilio/views/res_config_settings_views.xml:4`, `addons/sms_twilio/views/sms_sms_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/sms_twilio/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/sms_twilio/tests/test_sms_twilio.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/sms_twilio/tests/test_sms_twilio_controller.py`, `addons/sms_twilio/tests/test_twilio_account_manage.py`, `addons/sms_twilio/tests/common.py`, `addons/sms_twilio/tests/__init__.py`, `addons/sms_twilio/tests/test_sms_twilio.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `sms_twilio_account_manage_view_form`, `res_config_settings_view_form`, `sms_sms_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/sms_twilio/wizard/sms_twilio_account_manage_views.xml:5`, `addons/sms_twilio/wizard/sms_twilio_account_manage_views.xml:7`, `addons/sms_twilio/views/res_config_settings_views.xml:6`, `addons/sms_twilio/views/res_config_settings_views.xml:9`, `addons/sms_twilio/views/sms_sms_views.xml:6`, `addons/sms_twilio/views/sms_sms_views.xml:8`
- Browser assets: 1; representative files: `addons/sms_twilio/static/src/core/notification_model.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sms_twilio/__manifest__.py`
- **HTTP entry points:** `addons/sms_twilio/controllers/controllers.py:44`
- **Scheduled entry points:** `addons/sms_twilio/tests/test_sms_twilio.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: inherits `sms.sms` (addons/sms_twilio/models/sms_sms.py:6); inherits `res.config.settings` (addons/sms_twilio/models/res_config_settings.py:4); `sms.twilio.number` (addons/sms_twilio/models/sms_twilio_number.py:4); inherits `sms.composer` (addons/sms_twilio/models/sms_composer.py:4); inherits `mail.notification` (addons/sms_twilio/models/mail_notification.py:4); inherits `res.company` (addons/sms_twilio/models/res_company.py:9); inherits `sms.tracker` (addons/sms_twilio/models/sms_tracker.py:4); `sms.twilio.account.manage` (addons/sms_twilio/wizard/sms_twilio_account_manage.py:12)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/sms_twilio/controllers/controllers.py:44`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sms`
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

- `addons/sms_twilio/__init__.py`
- `addons/sms_twilio/__manifest__.py`
- `addons/sms_twilio/controllers/__init__.py`
- `addons/sms_twilio/controllers/controllers.py`
- `addons/sms_twilio/data/neutralize.sql`
- `addons/sms_twilio/i18n/ar.po`
- `addons/sms_twilio/i18n/az.po`
- `addons/sms_twilio/i18n/bg.po`
- `addons/sms_twilio/i18n/bs.po`
- `addons/sms_twilio/i18n/ca.po`
- `addons/sms_twilio/i18n/cs.po`
- `addons/sms_twilio/i18n/da.po`
- `addons/sms_twilio/i18n/de.po`
- `addons/sms_twilio/i18n/el.po`
- `addons/sms_twilio/i18n/es.po`
- `addons/sms_twilio/i18n/es_419.po`
- `addons/sms_twilio/i18n/et.po`
- `addons/sms_twilio/i18n/fa.po`
- `addons/sms_twilio/i18n/fi.po`
- `addons/sms_twilio/i18n/fr.po`
- `addons/sms_twilio/i18n/he.po`
- `addons/sms_twilio/i18n/hi.po`
- `addons/sms_twilio/i18n/hr.po`
- `addons/sms_twilio/i18n/hu.po`
- `addons/sms_twilio/i18n/id.po`
- `addons/sms_twilio/i18n/it.po`
- `addons/sms_twilio/i18n/ja.po`
- `addons/sms_twilio/i18n/kab.po`
- `addons/sms_twilio/i18n/ko.po`
- `addons/sms_twilio/i18n/ku.po`
- `addons/sms_twilio/i18n/lo.po`
- `addons/sms_twilio/i18n/lt.po`
- `addons/sms_twilio/i18n/lv.po`
- `addons/sms_twilio/i18n/mn.po`
- `addons/sms_twilio/i18n/my.po`
- `addons/sms_twilio/i18n/nb.po`
- `addons/sms_twilio/i18n/nl.po`
- `addons/sms_twilio/i18n/pl.po`
- `addons/sms_twilio/i18n/pt.po`
- `addons/sms_twilio/i18n/pt_BR.po`
- `addons/sms_twilio/i18n/ro.po`
- `addons/sms_twilio/i18n/ru.po`
- `addons/sms_twilio/i18n/sk.po`
- `addons/sms_twilio/i18n/sl.po`
- `addons/sms_twilio/i18n/sms_twilio.pot`
- `addons/sms_twilio/i18n/sr@latin.po`
- `addons/sms_twilio/i18n/sv.po`
- `addons/sms_twilio/i18n/th.po`
- `addons/sms_twilio/i18n/tr.po`
- `addons/sms_twilio/i18n/uk.po`
- `addons/sms_twilio/i18n/uz.po`
- `addons/sms_twilio/i18n/vi.po`
- `addons/sms_twilio/i18n/zh_CN.po`
- `addons/sms_twilio/i18n/zh_TW.po`
- `addons/sms_twilio/models/__init__.py`
- `addons/sms_twilio/models/mail_notification.py`
- `addons/sms_twilio/models/res_company.py`
- `addons/sms_twilio/models/res_config_settings.py`
- `addons/sms_twilio/models/sms_composer.py`
- `addons/sms_twilio/models/sms_sms.py`
- `addons/sms_twilio/models/sms_tracker.py`
- `addons/sms_twilio/models/sms_twilio_number.py`
- `addons/sms_twilio/security/ir.access.csv`
- `addons/sms_twilio/static/src/core/notification_model.js`
- `addons/sms_twilio/tests/__init__.py`
- `addons/sms_twilio/tests/common.py`
- `addons/sms_twilio/tests/test_sms_twilio.py`
- `addons/sms_twilio/tests/test_sms_twilio_controller.py`
- `addons/sms_twilio/tests/test_twilio_account_manage.py`
- `addons/sms_twilio/tools/__init__.py`
- `addons/sms_twilio/tools/sms_api.py`
- `addons/sms_twilio/tools/sms_twilio.py`
- `addons/sms_twilio/views/res_config_settings_views.xml`
- `addons/sms_twilio/views/sms_sms_views.xml`
- `addons/sms_twilio/wizard/__init__.py`
- `addons/sms_twilio/wizard/sms_twilio_account_manage.py`
- `addons/sms_twilio/wizard/sms_twilio_account_manage_views.xml`
