# Module: auth_oauth

- **Module ID:** MOD-021
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/auth_oauth`
- **Manifest:** `addons/auth_oauth/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Allow users to login through OAuth2 Provider.
=============================================

**Scope evidence:** The module contains 80 files, including 9 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `web`, `base_setup`, `auth_signup`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 2
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 1
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/auth_oauth/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 19 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/auth_oauth/models/ir_config_parameter.py:7`, `addons/auth_oauth/models/res_config_settings.py:7`, `addons/auth_oauth/models/auth_oauth.py:6`, `addons/auth_oauth/models/res_users.py:19`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 3 route declarations.
- **Evidence:** `addons/auth_oauth/controllers/main.py:60`, `addons/auth_oauth/controllers/main.py:94`, `addons/auth_oauth/controllers/main.py:151`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 9 record/template/menu identifiers.
- **Evidence:** `addons/auth_oauth/data/auth_oauth_data.xml:4`, `addons/auth_oauth/data/auth_oauth_data.xml:13`, `addons/auth_oauth/data/auth_oauth_data.xml:22`, `addons/auth_oauth/views/auth_oauth_templates.xml:3`, `addons/auth_oauth/views/res_config_settings_views.xml:3`, `addons/auth_oauth/views/auth_oauth_views.xml:3`, `addons/auth_oauth/views/auth_oauth_views.xml:27`, `addons/auth_oauth/views/auth_oauth_views.xml:39`, `addons/auth_oauth/views/auth_oauth_views.xml:44`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/auth_oauth/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `provider_openerp`, `provider_facebook`, `provider_google`, `OAuth Providers`, `res_config_settings_view_form`, `view_oauth_provider_form`, `view_oauth_provider_tree`, `action_oauth_provider`, `OAuth Providers`
- Menus: 1; representative evidence: `addons/auth_oauth/views/auth_oauth_views.xml:44`
- Templates: 1; representative evidence: `addons/auth_oauth/views/auth_oauth_templates.xml:3`
- View/action field declarations: 8; representative evidence: `addons/auth_oauth/views/res_config_settings_views.xml:5`, `addons/auth_oauth/views/res_config_settings_views.xml:7`, `addons/auth_oauth/views/auth_oauth_views.xml:5`, `addons/auth_oauth/views/auth_oauth_views.xml:6`, `addons/auth_oauth/views/auth_oauth_views.xml:29`, `addons/auth_oauth/views/auth_oauth_views.xml:30`, `addons/auth_oauth/views/auth_oauth_views.xml:41`, `addons/auth_oauth/views/auth_oauth_views.xml:42`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/auth_oauth/__manifest__.py`
- **HTTP entry points:** `addons/auth_oauth/controllers/main.py:60`, `addons/auth_oauth/controllers/main.py:94`, `addons/auth_oauth/controllers/main.py:151`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `ir.config_parameter` (addons/auth_oauth/models/ir_config_parameter.py:7); inherits `res.config.settings` (addons/auth_oauth/models/res_config_settings.py:7); `auth.oauth.provider` (addons/auth_oauth/models/auth_oauth.py:6); inherits `res.users` (addons/auth_oauth/models/res_users.py:19)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 3
- Route evidence: `addons/auth_oauth/controllers/main.py:60`, `addons/auth_oauth/controllers/main.py:94`, `addons/auth_oauth/controllers/main.py:151`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `web`, `base_setup`, `auth_signup`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/auth_oauth/__init__.py`
- `addons/auth_oauth/__manifest__.py`
- `addons/auth_oauth/controllers/__init__.py`
- `addons/auth_oauth/controllers/main.py`
- `addons/auth_oauth/data/auth_oauth_data.xml`
- `addons/auth_oauth/data/neutralize.sql`
- `addons/auth_oauth/i18n/af.po`
- `addons/auth_oauth/i18n/am.po`
- `addons/auth_oauth/i18n/ar.po`
- `addons/auth_oauth/i18n/auth_oauth.pot`
- `addons/auth_oauth/i18n/az.po`
- `addons/auth_oauth/i18n/bg.po`
- `addons/auth_oauth/i18n/bs.po`
- `addons/auth_oauth/i18n/ca.po`
- `addons/auth_oauth/i18n/cs.po`
- `addons/auth_oauth/i18n/da.po`
- `addons/auth_oauth/i18n/de.po`
- `addons/auth_oauth/i18n/el.po`
- `addons/auth_oauth/i18n/es.po`
- `addons/auth_oauth/i18n/es_419.po`
- `addons/auth_oauth/i18n/es_CL.po`
- `addons/auth_oauth/i18n/et.po`
- `addons/auth_oauth/i18n/eu.po`
- `addons/auth_oauth/i18n/fa.po`
- `addons/auth_oauth/i18n/fi.po`
- `addons/auth_oauth/i18n/fo.po`
- `addons/auth_oauth/i18n/fr.po`
- `addons/auth_oauth/i18n/fr_BE.po`
- `addons/auth_oauth/i18n/fr_CA.po`
- `addons/auth_oauth/i18n/gl.po`
- `addons/auth_oauth/i18n/gu.po`
- `addons/auth_oauth/i18n/he.po`
- `addons/auth_oauth/i18n/hi.po`
- `addons/auth_oauth/i18n/hr.po`
- `addons/auth_oauth/i18n/hu.po`
- `addons/auth_oauth/i18n/id.po`
- `addons/auth_oauth/i18n/is.po`
- `addons/auth_oauth/i18n/it.po`
- `addons/auth_oauth/i18n/ja.po`
- `addons/auth_oauth/i18n/ka.po`
- `addons/auth_oauth/i18n/kab.po`
- `addons/auth_oauth/i18n/km.po`
- `addons/auth_oauth/i18n/ko.po`
- `addons/auth_oauth/i18n/ku.po`
- `addons/auth_oauth/i18n/lo.po`
- `addons/auth_oauth/i18n/lt.po`
- `addons/auth_oauth/i18n/lv.po`
- `addons/auth_oauth/i18n/mk.po`
- `addons/auth_oauth/i18n/mn.po`
- `addons/auth_oauth/i18n/my.po`
- `addons/auth_oauth/i18n/nb.po`
- `addons/auth_oauth/i18n/nl.po`
- `addons/auth_oauth/i18n/pl.po`
- `addons/auth_oauth/i18n/pt.po`
- `addons/auth_oauth/i18n/pt_BR.po`
- `addons/auth_oauth/i18n/ro.po`
- `addons/auth_oauth/i18n/ru.po`
- `addons/auth_oauth/i18n/sk.po`
- `addons/auth_oauth/i18n/sl.po`
- `addons/auth_oauth/i18n/sq.po`
- `addons/auth_oauth/i18n/sr@latin.po`
- `addons/auth_oauth/i18n/sv.po`
- `addons/auth_oauth/i18n/ta.po`
- `addons/auth_oauth/i18n/th.po`
- `addons/auth_oauth/i18n/tr.po`
- `addons/auth_oauth/i18n/uk.po`
- `addons/auth_oauth/i18n/uz.po`
- `addons/auth_oauth/i18n/vi.po`
- `addons/auth_oauth/i18n/zh_CN.po`
- `addons/auth_oauth/i18n/zh_TW.po`
- `addons/auth_oauth/models/__init__.py`
- `addons/auth_oauth/models/auth_oauth.py`
- `addons/auth_oauth/models/ir_config_parameter.py`
- `addons/auth_oauth/models/res_config_settings.py`
- `addons/auth_oauth/models/res_users.py`
- `addons/auth_oauth/security/ir.access.csv`
- `addons/auth_oauth/static/src/scss/auth_oauth.scss`
- `addons/auth_oauth/views/auth_oauth_templates.xml`
- `addons/auth_oauth/views/auth_oauth_views.xml`
- `addons/auth_oauth/views/res_config_settings_views.xml`
