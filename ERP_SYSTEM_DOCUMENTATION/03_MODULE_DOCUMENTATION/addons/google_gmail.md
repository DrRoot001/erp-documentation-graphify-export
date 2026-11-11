# Module: google_gmail

- **Module ID:** MOD-079
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/google_gmail`
- **Manifest:** `addons/google_gmail/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Gmail support for incoming / outgoing mail servers

**Scope evidence:** The module contains 69 files, including 13 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `mail`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 2
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 29 methods, 2 constraint handlers, 4 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/google_gmail/models/res_config_settings.py:7`, `addons/google_gmail/models/ir_mail_server.py:10`, `addons/google_gmail/models/fetchmail_server.py:8`, `addons/google_gmail/models/res_users.py:6`, `addons/google_gmail/models/google_gmail_mixin.py:25`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 2 route declarations.
- **Evidence:** `addons/google_gmail/controllers/main.py:20`, `addons/google_gmail/controllers/main.py:56`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 4 record/template/menu identifiers.
- **Evidence:** `addons/google_gmail/views/fetchmail_server_views.xml:3`, `addons/google_gmail/views/res_config_settings_views.xml:4`, `addons/google_gmail/views/ir_mail_server_views.xml:3`, `addons/google_gmail/views/templates.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/google_gmail/tests/test_google_gmail.py`, `addons/google_gmail/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `fetchmail_server_view_form`, `res_config_settings_view_form`, `ir_mail_server_view_form`, `google_gmail_oauth_error`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/google_gmail/views/templates.xml:3`
- View/action field declarations: 6; representative evidence: `addons/google_gmail/views/fetchmail_server_views.xml:5`, `addons/google_gmail/views/fetchmail_server_views.xml:8`, `addons/google_gmail/views/res_config_settings_views.xml:6`, `addons/google_gmail/views/res_config_settings_views.xml:8`, `addons/google_gmail/views/ir_mail_server_views.xml:5`, `addons/google_gmail/views/ir_mail_server_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/google_gmail/__manifest__.py`
- **HTTP entry points:** `addons/google_gmail/controllers/main.py:20`, `addons/google_gmail/controllers/main.py:56`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `res.config.settings` (addons/google_gmail/models/res_config_settings.py:7); `ir.mail_server` (addons/google_gmail/models/ir_mail_server.py:10); `fetchmail.server` (addons/google_gmail/models/fetchmail_server.py:8); inherits `res.users` (addons/google_gmail/models/res_users.py:6); `google.gmail.mixin` (addons/google_gmail/models/google_gmail_mixin.py:25)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 2
- Route evidence: `addons/google_gmail/controllers/main.py:20`, `addons/google_gmail/controllers/main.py:56`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mail`
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

- `addons/google_gmail/__init__.py`
- `addons/google_gmail/__manifest__.py`
- `addons/google_gmail/controllers/__init__.py`
- `addons/google_gmail/controllers/main.py`
- `addons/google_gmail/i18n/ar.po`
- `addons/google_gmail/i18n/az.po`
- `addons/google_gmail/i18n/bg.po`
- `addons/google_gmail/i18n/bs.po`
- `addons/google_gmail/i18n/ca.po`
- `addons/google_gmail/i18n/cs.po`
- `addons/google_gmail/i18n/da.po`
- `addons/google_gmail/i18n/de.po`
- `addons/google_gmail/i18n/el.po`
- `addons/google_gmail/i18n/es.po`
- `addons/google_gmail/i18n/es_419.po`
- `addons/google_gmail/i18n/et.po`
- `addons/google_gmail/i18n/fa.po`
- `addons/google_gmail/i18n/fi.po`
- `addons/google_gmail/i18n/fr.po`
- `addons/google_gmail/i18n/google_gmail.pot`
- `addons/google_gmail/i18n/he.po`
- `addons/google_gmail/i18n/hi.po`
- `addons/google_gmail/i18n/hr.po`
- `addons/google_gmail/i18n/hu.po`
- `addons/google_gmail/i18n/id.po`
- `addons/google_gmail/i18n/it.po`
- `addons/google_gmail/i18n/ja.po`
- `addons/google_gmail/i18n/kab.po`
- `addons/google_gmail/i18n/ko.po`
- `addons/google_gmail/i18n/ku.po`
- `addons/google_gmail/i18n/lo.po`
- `addons/google_gmail/i18n/lt.po`
- `addons/google_gmail/i18n/lv.po`
- `addons/google_gmail/i18n/mn.po`
- `addons/google_gmail/i18n/my.po`
- `addons/google_gmail/i18n/nb.po`
- `addons/google_gmail/i18n/nl.po`
- `addons/google_gmail/i18n/pl.po`
- `addons/google_gmail/i18n/pt.po`
- `addons/google_gmail/i18n/pt_BR.po`
- `addons/google_gmail/i18n/ro.po`
- `addons/google_gmail/i18n/ru.po`
- `addons/google_gmail/i18n/sk.po`
- `addons/google_gmail/i18n/sl.po`
- `addons/google_gmail/i18n/sr@latin.po`
- `addons/google_gmail/i18n/sv.po`
- `addons/google_gmail/i18n/th.po`
- `addons/google_gmail/i18n/tr.po`
- `addons/google_gmail/i18n/uk.po`
- `addons/google_gmail/i18n/uz.po`
- `addons/google_gmail/i18n/vi.po`
- `addons/google_gmail/i18n/zh_CN.po`
- `addons/google_gmail/i18n/zh_TW.po`
- `addons/google_gmail/models/__init__.py`
- `addons/google_gmail/models/fetchmail_server.py`
- `addons/google_gmail/models/google_gmail_mixin.py`
- `addons/google_gmail/models/ir_mail_server.py`
- `addons/google_gmail/models/res_config_settings.py`
- `addons/google_gmail/models/res_users.py`
- `addons/google_gmail/static/description/icon.png`
- `addons/google_gmail/static/description/icon.svg`
- `addons/google_gmail/static/description/icon_hi.png`
- `addons/google_gmail/tests/__init__.py`
- `addons/google_gmail/tests/test_google_gmail.py`
- `addons/google_gmail/tools.py`
- `addons/google_gmail/views/fetchmail_server_views.xml`
- `addons/google_gmail/views/ir_mail_server_views.xml`
- `addons/google_gmail/views/res_config_settings_views.xml`
- `addons/google_gmail/views/templates.xml`
