# Module: auth_signup

- **Module ID:** MOD-027
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/auth_signup`
- **Manifest:** `addons/auth_signup/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Allow users to sign up and reset their password
===============================================

**Scope evidence:** The module contains 86 files, including 13 Python, 9 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `base_setup`, `mail`, `web`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 2
- XML/data/view/template files: 9
- Browser asset files: 2
- Security files: 0
- Test files: 4
- Scheduled/automation evidence files: 4
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 54 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/auth_signup/models/res_partner.py:24`, `addons/auth_signup/models/res_config_settings.py:7`, `addons/auth_signup/models/ir_http.py:8`, `addons/auth_signup/models/res_users.py:21`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 5 route declarations.
- **Evidence:** `addons/auth_signup/controllers/main.py:26`, `addons/auth_signup/controllers/main.py:40`, `addons/auth_signup/controllers/main.py:96`, `addons/auth_signup/controllers/main.py:190`, `addons/auth_signup/controllers/main.py:200`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 9 XML files and 2 JavaScript/TypeScript files; static XML analysis found 15 record/template/menu identifiers.
- **Evidence:** `addons/auth_signup/data/mail_template_data.xml:5`, `addons/auth_signup/data/mail_template_data.xml:45`, `addons/auth_signup/data/mail_template_data.xml:73`, `addons/auth_signup/data/mail_template_data.xml:106`, `addons/auth_signup/data/ir_cron_data.xml:3`, `addons/auth_signup/views/res_config_settings_views.xml:4`, `addons/auth_signup/views/webclient_templates.xml:4`, `addons/auth_signup/views/auth_signup_templates_email.xml:3`, `addons/auth_signup/views/auth_signup_login_templates.xml:3`, `addons/auth_signup/views/auth_signup_login_templates.xml:12`, `addons/auth_signup/views/auth_signup_login_templates.xml:38`, `addons/auth_signup/views/auth_signup_login_templates.xml:74`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 4 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/auth_signup/__manifest__.py`, `addons/auth_signup/models/res_users.py`, `addons/auth_signup/data/ir_cron_data.xml`, `addons/auth_signup/views/res_users_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/auth_signup/tests/test_login.py`, `addons/auth_signup/tests/test_reset_password.py`, `addons/auth_signup/tests/test_auth_signup.py`, `addons/auth_signup/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 9; representative identifiers: `set_password_email`, `mail_template_data_unregistered_users`, `mail_template_user_signup_account_created`, `portal_set_password_email`, `ir_cron_auth_signup_send_pending_user_reminder`, `res_config_settings_view_form`, `login_successful`, `User Reset Password`, `Sign up - Reset Password`, `Auth Signup/ResetPassword form fields`, `Sign up login`, `Reset password`, `res_users_view_form`, `view_users_state_tree`, `action_send_password_reset_instructions`
- Menus: 0; representative evidence: Not found in module
- Templates: 6; representative evidence: `addons/auth_signup/views/webclient_templates.xml:4`, `addons/auth_signup/views/auth_signup_templates_email.xml:3`, `addons/auth_signup/views/auth_signup_login_templates.xml:3`, `addons/auth_signup/views/auth_signup_login_templates.xml:12`, `addons/auth_signup/views/auth_signup_login_templates.xml:38`, `addons/auth_signup/views/auth_signup_login_templates.xml:74`
- View/action field declarations: 6; representative evidence: `addons/auth_signup/views/res_config_settings_views.xml:6`, `addons/auth_signup/views/res_config_settings_views.xml:8`, `addons/auth_signup/views/res_users_views.xml:6`, `addons/auth_signup/views/res_users_views.xml:8`, `addons/auth_signup/views/res_users_views.xml:29`, `addons/auth_signup/views/res_users_views.xml:31`
- Browser assets: 2; representative files: `addons/auth_signup/static/src/components/signup.js`, `addons/auth_signup/static/src/interactions/signup.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/auth_signup/__manifest__.py`
- **HTTP entry points:** `addons/auth_signup/controllers/main.py:26`, `addons/auth_signup/controllers/main.py:40`, `addons/auth_signup/controllers/main.py:96`, `addons/auth_signup/controllers/main.py:190`, `addons/auth_signup/controllers/main.py:200`
- **Scheduled entry points:** `addons/auth_signup/__manifest__.py`, `addons/auth_signup/models/res_users.py`, `addons/auth_signup/data/ir_cron_data.xml`, `addons/auth_signup/views/res_users_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `res.partner` (addons/auth_signup/models/res_partner.py:24); inherits `res.config.settings` (addons/auth_signup/models/res_config_settings.py:7); inherits `ir.http` (addons/auth_signup/models/ir_http.py:8); inherits `res.users` (addons/auth_signup/models/res_users.py:21)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 5
- Route evidence: `addons/auth_signup/controllers/main.py:26`, `addons/auth_signup/controllers/main.py:40`, `addons/auth_signup/controllers/main.py:96`, `addons/auth_signup/controllers/main.py:190`, `addons/auth_signup/controllers/main.py:200`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base_setup`, `mail`, `web`
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

- `addons/auth_signup/__init__.py`
- `addons/auth_signup/__manifest__.py`
- `addons/auth_signup/controllers/__init__.py`
- `addons/auth_signup/controllers/main.py`
- `addons/auth_signup/data/ir_config_parameter_data.xml`
- `addons/auth_signup/data/ir_cron_data.xml`
- `addons/auth_signup/data/mail_template_data.xml`
- `addons/auth_signup/i18n/af.po`
- `addons/auth_signup/i18n/am.po`
- `addons/auth_signup/i18n/ar.po`
- `addons/auth_signup/i18n/auth_signup.pot`
- `addons/auth_signup/i18n/az.po`
- `addons/auth_signup/i18n/bg.po`
- `addons/auth_signup/i18n/bs.po`
- `addons/auth_signup/i18n/ca.po`
- `addons/auth_signup/i18n/cs.po`
- `addons/auth_signup/i18n/da.po`
- `addons/auth_signup/i18n/de.po`
- `addons/auth_signup/i18n/el.po`
- `addons/auth_signup/i18n/es.po`
- `addons/auth_signup/i18n/es_419.po`
- `addons/auth_signup/i18n/es_CL.po`
- `addons/auth_signup/i18n/et.po`
- `addons/auth_signup/i18n/eu.po`
- `addons/auth_signup/i18n/fa.po`
- `addons/auth_signup/i18n/fi.po`
- `addons/auth_signup/i18n/fr.po`
- `addons/auth_signup/i18n/fr_BE.po`
- `addons/auth_signup/i18n/fr_CA.po`
- `addons/auth_signup/i18n/gl.po`
- `addons/auth_signup/i18n/gu.po`
- `addons/auth_signup/i18n/he.po`
- `addons/auth_signup/i18n/hi.po`
- `addons/auth_signup/i18n/hr.po`
- `addons/auth_signup/i18n/hu.po`
- `addons/auth_signup/i18n/id.po`
- `addons/auth_signup/i18n/is.po`
- `addons/auth_signup/i18n/it.po`
- `addons/auth_signup/i18n/ja.po`
- `addons/auth_signup/i18n/ka.po`
- `addons/auth_signup/i18n/kab.po`
- `addons/auth_signup/i18n/km.po`
- `addons/auth_signup/i18n/ko.po`
- `addons/auth_signup/i18n/ku.po`
- `addons/auth_signup/i18n/lo.po`
- `addons/auth_signup/i18n/lt.po`
- `addons/auth_signup/i18n/lv.po`
- `addons/auth_signup/i18n/mk.po`
- `addons/auth_signup/i18n/mn.po`
- `addons/auth_signup/i18n/my.po`
- `addons/auth_signup/i18n/nb.po`
- `addons/auth_signup/i18n/nl.po`
- `addons/auth_signup/i18n/pl.po`
- `addons/auth_signup/i18n/pt.po`
- `addons/auth_signup/i18n/pt_BR.po`
- `addons/auth_signup/i18n/ro.po`
- `addons/auth_signup/i18n/ru.po`
- `addons/auth_signup/i18n/sk.po`
- `addons/auth_signup/i18n/sl.po`
- `addons/auth_signup/i18n/sq.po`
- `addons/auth_signup/i18n/sr@latin.po`
- `addons/auth_signup/i18n/sv.po`
- `addons/auth_signup/i18n/th.po`
- `addons/auth_signup/i18n/tr.po`
- `addons/auth_signup/i18n/uk.po`
- `addons/auth_signup/i18n/uz.po`
- `addons/auth_signup/i18n/vi.po`
- `addons/auth_signup/i18n/zh_CN.po`
- `addons/auth_signup/i18n/zh_TW.po`
- `addons/auth_signup/models/__init__.py`
- `addons/auth_signup/models/ir_http.py`
- `addons/auth_signup/models/res_config_settings.py`
- `addons/auth_signup/models/res_partner.py`
- `addons/auth_signup/models/res_users.py`
- `addons/auth_signup/static/src/components/signup.js`
- `addons/auth_signup/static/src/components/signup.xml`
- `addons/auth_signup/static/src/interactions/signup.js`
- `addons/auth_signup/tests/__init__.py`
- `addons/auth_signup/tests/test_auth_signup.py`
- `addons/auth_signup/tests/test_login.py`
- `addons/auth_signup/tests/test_reset_password.py`
- `addons/auth_signup/views/auth_signup_login_templates.xml`
- `addons/auth_signup/views/auth_signup_templates_email.xml`
- `addons/auth_signup/views/res_config_settings_views.xml`
- `addons/auth_signup/views/res_users_views.xml`
- `addons/auth_signup/views/webclient_templates.xml`
