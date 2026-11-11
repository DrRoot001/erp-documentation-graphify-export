# Module: auth_totp

- **Module ID:** MOD-029
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/auth_totp`
- **Manifest:** `addons/auth_totp/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Extra Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Two-Factor Authentication (TOTP)
================================
Allows users to configure two-factor authentication on their user account
for extra security, using time-based one-time passwords (TOTP).

Once enabled, the user will need to enter a 6-digit code as provided
by their authenticator app before being granted access to the system.
All popular authenticator apps are supported.

Note: logically, two-factor prevents password-based RPC access for users
where it is enabled. In order to be able to execute RPC scripts, the user
can setup API keys to replace their main password.

**Scope evidence:** The module contains 74 files, including 15 Python, 5 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `web`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 2
- XML/data/view/template files: 5
- Browser asset files: 3
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/auth_totp/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 40 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/auth_totp/models/auth_totp_rate_limit_log.py:4`, `addons/auth_totp/models/ir_http.py:8`, `addons/auth_totp/models/res_users.py:30`, `addons/auth_totp/models/auth_totp.py:9`, `addons/auth_totp/wizard/auth_totp_wizard.py:20`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/auth_totp/controllers/home.py:17`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 3 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/auth_totp/wizard/auth_totp_wizard_views.xml:3`, `addons/auth_totp/data/ir_action_data.xml:4`, `addons/auth_totp/views/templates.xml:3`, `addons/auth_totp/views/res_users_views.xml:3`, `addons/auth_totp/views/res_users_views.xml:16`, `addons/auth_totp/views/res_users_views.xml:53`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/auth_totp/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/auth_totp/data/ir_action_data.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/auth_totp/tests/test_totp.py`, `addons/auth_totp/tests/test_apikeys.py`, `addons/auth_totp/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `view_totp_wizard`, `action_disable_totp`, `Two-Factor Authentication`, `res_users_view_search`, `view_totp_form`, `view_totp_field`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/auth_totp/views/templates.xml:3`
- View/action field declarations: 8; representative evidence: `addons/auth_totp/wizard/auth_totp_wizard_views.xml:5`, `addons/auth_totp/wizard/auth_totp_wizard_views.xml:6`, `addons/auth_totp/views/res_users_views.xml:5`, `addons/auth_totp/views/res_users_views.xml:7`, `addons/auth_totp/views/res_users_views.xml:18`, `addons/auth_totp/views/res_users_views.xml:20`, `addons/auth_totp/views/res_users_views.xml:55`, `addons/auth_totp/views/res_users_views.xml:57`
- Browser assets: 3; representative files: `addons/auth_totp/static/tests/apikeys_flow.js`, `addons/auth_totp/static/tests/totp_flow.js`, `addons/auth_totp/static/src/services/check_identity/check_identity.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/auth_totp/__manifest__.py`
- **HTTP entry points:** `addons/auth_totp/controllers/home.py:17`
- **Scheduled entry points:** `addons/auth_totp/data/ir_action_data.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: `auth.totp.rate.limit.log` (addons/auth_totp/models/auth_totp_rate_limit_log.py:4); inherits `ir.http` (addons/auth_totp/models/ir_http.py:8); inherits `res.users` (addons/auth_totp/models/res_users.py:30); `auth_totp.device` (addons/auth_totp/models/auth_totp.py:9); `auth_totp.wizard` (addons/auth_totp/wizard/auth_totp_wizard.py:20)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/auth_totp/controllers/home.py:17`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `web`
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

- `addons/auth_totp/__init__.py`
- `addons/auth_totp/__manifest__.py`
- `addons/auth_totp/controllers/__init__.py`
- `addons/auth_totp/controllers/home.py`
- `addons/auth_totp/data/ir_action_data.xml`
- `addons/auth_totp/i18n/ar.po`
- `addons/auth_totp/i18n/auth_totp.pot`
- `addons/auth_totp/i18n/az.po`
- `addons/auth_totp/i18n/bg.po`
- `addons/auth_totp/i18n/bs.po`
- `addons/auth_totp/i18n/ca.po`
- `addons/auth_totp/i18n/cs.po`
- `addons/auth_totp/i18n/da.po`
- `addons/auth_totp/i18n/de.po`
- `addons/auth_totp/i18n/el.po`
- `addons/auth_totp/i18n/es.po`
- `addons/auth_totp/i18n/es_419.po`
- `addons/auth_totp/i18n/et.po`
- `addons/auth_totp/i18n/fa.po`
- `addons/auth_totp/i18n/fi.po`
- `addons/auth_totp/i18n/fr.po`
- `addons/auth_totp/i18n/he.po`
- `addons/auth_totp/i18n/hi.po`
- `addons/auth_totp/i18n/hr.po`
- `addons/auth_totp/i18n/hu.po`
- `addons/auth_totp/i18n/id.po`
- `addons/auth_totp/i18n/it.po`
- `addons/auth_totp/i18n/ja.po`
- `addons/auth_totp/i18n/kab.po`
- `addons/auth_totp/i18n/ko.po`
- `addons/auth_totp/i18n/ku.po`
- `addons/auth_totp/i18n/lo.po`
- `addons/auth_totp/i18n/lt.po`
- `addons/auth_totp/i18n/lv.po`
- `addons/auth_totp/i18n/mn.po`
- `addons/auth_totp/i18n/my.po`
- `addons/auth_totp/i18n/nb.po`
- `addons/auth_totp/i18n/nl.po`
- `addons/auth_totp/i18n/pl.po`
- `addons/auth_totp/i18n/pt.po`
- `addons/auth_totp/i18n/pt_BR.po`
- `addons/auth_totp/i18n/ro.po`
- `addons/auth_totp/i18n/ru.po`
- `addons/auth_totp/i18n/sk.po`
- `addons/auth_totp/i18n/sl.po`
- `addons/auth_totp/i18n/sr@latin.po`
- `addons/auth_totp/i18n/sv.po`
- `addons/auth_totp/i18n/th.po`
- `addons/auth_totp/i18n/tr.po`
- `addons/auth_totp/i18n/uk.po`
- `addons/auth_totp/i18n/uz.po`
- `addons/auth_totp/i18n/vi.po`
- `addons/auth_totp/i18n/zh_CN.po`
- `addons/auth_totp/i18n/zh_TW.po`
- `addons/auth_totp/models/__init__.py`
- `addons/auth_totp/models/auth_totp.py`
- `addons/auth_totp/models/auth_totp_rate_limit_log.py`
- `addons/auth_totp/models/ir_http.py`
- `addons/auth_totp/models/res_users.py`
- `addons/auth_totp/models/totp.py`
- `addons/auth_totp/security/ir.access.csv`
- `addons/auth_totp/static/src/scss/res_users_view_form.scss`
- `addons/auth_totp/static/src/services/check_identity/check_identity.js`
- `addons/auth_totp/static/src/services/check_identity/check_identity.xml`
- `addons/auth_totp/static/tests/apikeys_flow.js`
- `addons/auth_totp/static/tests/totp_flow.js`
- `addons/auth_totp/tests/__init__.py`
- `addons/auth_totp/tests/test_apikeys.py`
- `addons/auth_totp/tests/test_totp.py`
- `addons/auth_totp/views/res_users_views.xml`
- `addons/auth_totp/views/templates.xml`
- `addons/auth_totp/wizard/__init__.py`
- `addons/auth_totp/wizard/auth_totp_wizard.py`
- `addons/auth_totp/wizard/auth_totp_wizard_views.xml`
