# Module: auth_totp_mail

- **Module ID:** MOD-030
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/auth_totp_mail`
- **Manifest:** `addons/auth_totp_mail/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Extra Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

2FA Invite mail
===============
Allow the users to invite another user to use Two-Factor authentication
by sending an email to the target user. This email redirects them to:
- the users security settings if the user is internal.
- the portal security settings page if the user is not internal.

**Scope evidence:** The module contains 73 files, including 14 Python, 7 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `auth_totp`, `mail`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 3
- XML/data/view/template files: 7
- Browser asset files: 2
- Security files: 0
- Test files: 4
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 28 methods, 0 constraint handlers, 1 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/auth_totp_mail/models/res_config_settings.py:6`, `addons/auth_totp_mail/models/ir_http.py:8`, `addons/auth_totp_mail/models/res_users.py:18`, `addons/auth_totp_mail/models/auth_totp_device.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 2 route declarations.
- **Evidence:** `addons/auth_totp_mail/controllers/home.py:12`, `addons/auth_totp_mail/controllers/main.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 2 JavaScript/TypeScript files; static XML analysis found 9 record/template/menu identifiers.
- **Evidence:** `addons/auth_totp_mail/data/ir_action_data.xml:4`, `addons/auth_totp_mail/data/ir_action_data.xml:17`, `addons/auth_totp_mail/data/mail_template_data.xml:4`, `addons/auth_totp_mail/data/mail_template_data.xml:33`, `addons/auth_totp_mail/data/security_notifications_template.xml:5`, `addons/auth_totp_mail/views/res_config_settings_views.xml:5`, `addons/auth_totp_mail/views/templates.xml:2`, `addons/auth_totp_mail/views/res_users_views.xml:3`, `addons/auth_totp_mail/views/res_users_views.xml:21`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/auth_totp_mail/data/ir_action_data.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/auth_totp_mail/tests/test_auth_signup.py`, `addons/auth_totp_mail/tests/test_totp.py`, `addons/auth_totp_mail/tests/__init__.py`, `addons/auth_totp_mail/tests/test_notify_security_update_totp.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `action_invite_totp`, `action_activate_two_factor_authentication`, `mail_template_totp_invite`, `mail_template_totp_mail_code`, `account_security_alert`, `res_config_settings_view_form`, `auth_totp_mail_form`, `view_users_form`, `auth_totp_mail.res_users_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/auth_totp_mail/data/security_notifications_template.xml:5`, `addons/auth_totp_mail/views/templates.xml:2`
- View/action field declarations: 6; representative evidence: `addons/auth_totp_mail/views/res_config_settings_views.xml:7`, `addons/auth_totp_mail/views/res_config_settings_views.xml:10`, `addons/auth_totp_mail/views/res_users_views.xml:5`, `addons/auth_totp_mail/views/res_users_views.xml:7`, `addons/auth_totp_mail/views/res_users_views.xml:23`, `addons/auth_totp_mail/views/res_users_views.xml:26`
- Browser assets: 2; representative files: `addons/auth_totp_mail/static/tests/totp_flow.js`, `addons/auth_totp_mail/static/src/services/check_identity/check_identity.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/auth_totp_mail/__manifest__.py`
- **HTTP entry points:** `addons/auth_totp_mail/controllers/home.py:12`, `addons/auth_totp_mail/controllers/main.py:6`
- **Scheduled entry points:** `addons/auth_totp_mail/data/ir_action_data.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `res.config.settings` (addons/auth_totp_mail/models/res_config_settings.py:6); inherits `ir.http` (addons/auth_totp_mail/models/ir_http.py:8); inherits `res.users` (addons/auth_totp_mail/models/res_users.py:18); inherits `auth_totp.device` (addons/auth_totp_mail/models/auth_totp_device.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 2
- Route evidence: `addons/auth_totp_mail/controllers/home.py:12`, `addons/auth_totp_mail/controllers/main.py:6`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `auth_totp`, `mail`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/auth_totp_mail/__init__.py`
- `addons/auth_totp_mail/__manifest__.py`
- `addons/auth_totp_mail/controllers/__init__.py`
- `addons/auth_totp_mail/controllers/home.py`
- `addons/auth_totp_mail/controllers/main.py`
- `addons/auth_totp_mail/data/ir_action_data.xml`
- `addons/auth_totp_mail/data/mail_template_data.xml`
- `addons/auth_totp_mail/data/security_notifications_template.xml`
- `addons/auth_totp_mail/i18n/ar.po`
- `addons/auth_totp_mail/i18n/auth_totp_mail.pot`
- `addons/auth_totp_mail/i18n/az.po`
- `addons/auth_totp_mail/i18n/bg.po`
- `addons/auth_totp_mail/i18n/bs.po`
- `addons/auth_totp_mail/i18n/ca.po`
- `addons/auth_totp_mail/i18n/cs.po`
- `addons/auth_totp_mail/i18n/da.po`
- `addons/auth_totp_mail/i18n/de.po`
- `addons/auth_totp_mail/i18n/el.po`
- `addons/auth_totp_mail/i18n/es.po`
- `addons/auth_totp_mail/i18n/es_419.po`
- `addons/auth_totp_mail/i18n/et.po`
- `addons/auth_totp_mail/i18n/fa.po`
- `addons/auth_totp_mail/i18n/fi.po`
- `addons/auth_totp_mail/i18n/fr.po`
- `addons/auth_totp_mail/i18n/he.po`
- `addons/auth_totp_mail/i18n/hi.po`
- `addons/auth_totp_mail/i18n/hr.po`
- `addons/auth_totp_mail/i18n/hu.po`
- `addons/auth_totp_mail/i18n/id.po`
- `addons/auth_totp_mail/i18n/it.po`
- `addons/auth_totp_mail/i18n/ja.po`
- `addons/auth_totp_mail/i18n/kab.po`
- `addons/auth_totp_mail/i18n/ko.po`
- `addons/auth_totp_mail/i18n/ku.po`
- `addons/auth_totp_mail/i18n/lo.po`
- `addons/auth_totp_mail/i18n/lt.po`
- `addons/auth_totp_mail/i18n/lv.po`
- `addons/auth_totp_mail/i18n/mn.po`
- `addons/auth_totp_mail/i18n/my.po`
- `addons/auth_totp_mail/i18n/nb.po`
- `addons/auth_totp_mail/i18n/nl.po`
- `addons/auth_totp_mail/i18n/pl.po`
- `addons/auth_totp_mail/i18n/pt.po`
- `addons/auth_totp_mail/i18n/pt_BR.po`
- `addons/auth_totp_mail/i18n/ro.po`
- `addons/auth_totp_mail/i18n/ru.po`
- `addons/auth_totp_mail/i18n/sk.po`
- `addons/auth_totp_mail/i18n/sl.po`
- `addons/auth_totp_mail/i18n/sr@latin.po`
- `addons/auth_totp_mail/i18n/sv.po`
- `addons/auth_totp_mail/i18n/th.po`
- `addons/auth_totp_mail/i18n/tr.po`
- `addons/auth_totp_mail/i18n/uk.po`
- `addons/auth_totp_mail/i18n/uz.po`
- `addons/auth_totp_mail/i18n/vi.po`
- `addons/auth_totp_mail/i18n/zh_CN.po`
- `addons/auth_totp_mail/i18n/zh_TW.po`
- `addons/auth_totp_mail/models/__init__.py`
- `addons/auth_totp_mail/models/auth_totp_device.py`
- `addons/auth_totp_mail/models/ir_http.py`
- `addons/auth_totp_mail/models/res_config_settings.py`
- `addons/auth_totp_mail/models/res_users.py`
- `addons/auth_totp_mail/static/src/services/check_identity/check_identity.js`
- `addons/auth_totp_mail/static/src/services/check_identity/check_identity.scss`
- `addons/auth_totp_mail/static/src/services/check_identity/check_identity.xml`
- `addons/auth_totp_mail/static/tests/totp_flow.js`
- `addons/auth_totp_mail/tests/__init__.py`
- `addons/auth_totp_mail/tests/test_auth_signup.py`
- `addons/auth_totp_mail/tests/test_notify_security_update_totp.py`
- `addons/auth_totp_mail/tests/test_totp.py`
- `addons/auth_totp_mail/views/res_config_settings_views.xml`
- `addons/auth_totp_mail/views/res_users_views.xml`
- `addons/auth_totp_mail/views/templates.xml`
