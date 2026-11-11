# Module: auth_timeout

- **Module ID:** MOD-028
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/auth_timeout`
- **Manifest:** `addons/auth_timeout/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Ask for authentication after user inactivity

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 62 files, including 10 Python, 1 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `auth_totp`, `auth_totp_mail`, `auth_passkey`, `bus`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 1
- Browser asset files: 2
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 48 methods, 0 constraint handlers, 4 onchange handlers, and 6 dependency declarations.
- **Evidence:** `addons/auth_timeout/models/res_groups.py:33`, `addons/auth_timeout/models/ir_websocket.py:8`, `addons/auth_timeout/models/ir_http.py:8`, `addons/auth_timeout/models/res_users.py:4`, `addons/auth_timeout/models/auth_totp_device.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 2 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/auth_timeout/views/res_groups_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/auth_timeout/tests/test_auth_timeout.py`, `addons/auth_timeout/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `auth_passkey_groups_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/auth_timeout/views/res_groups_views.xml:5`, `addons/auth_timeout/views/res_groups_views.xml:7`
- Browser assets: 2; representative files: `addons/auth_timeout/static/src/services/check_identity/check_identity.js`, `addons/auth_timeout/static/tests/tours/auth_timeout_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/auth_timeout/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `res.groups` (addons/auth_timeout/models/res_groups.py:33); inherits `ir.websocket` (addons/auth_timeout/models/ir_websocket.py:8); inherits `ir.http` (addons/auth_timeout/models/ir_http.py:8); inherits `res.users` (addons/auth_timeout/models/res_users.py:4); inherits `auth_totp.device` (addons/auth_timeout/models/auth_totp_device.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `auth_totp`, `auth_totp_mail`, `auth_passkey`, `bus`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/auth_timeout/__init__.py`
- `addons/auth_timeout/__manifest__.py`
- `addons/auth_timeout/i18n/ar.po`
- `addons/auth_timeout/i18n/auth_timeout.pot`
- `addons/auth_timeout/i18n/az.po`
- `addons/auth_timeout/i18n/bg.po`
- `addons/auth_timeout/i18n/bs.po`
- `addons/auth_timeout/i18n/ca.po`
- `addons/auth_timeout/i18n/cs.po`
- `addons/auth_timeout/i18n/da.po`
- `addons/auth_timeout/i18n/de.po`
- `addons/auth_timeout/i18n/el.po`
- `addons/auth_timeout/i18n/es.po`
- `addons/auth_timeout/i18n/es_419.po`
- `addons/auth_timeout/i18n/et.po`
- `addons/auth_timeout/i18n/fa.po`
- `addons/auth_timeout/i18n/fi.po`
- `addons/auth_timeout/i18n/fr.po`
- `addons/auth_timeout/i18n/he.po`
- `addons/auth_timeout/i18n/hi.po`
- `addons/auth_timeout/i18n/hr.po`
- `addons/auth_timeout/i18n/hu.po`
- `addons/auth_timeout/i18n/id.po`
- `addons/auth_timeout/i18n/it.po`
- `addons/auth_timeout/i18n/ja.po`
- `addons/auth_timeout/i18n/kab.po`
- `addons/auth_timeout/i18n/ko.po`
- `addons/auth_timeout/i18n/ku.po`
- `addons/auth_timeout/i18n/lo.po`
- `addons/auth_timeout/i18n/lt.po`
- `addons/auth_timeout/i18n/lv.po`
- `addons/auth_timeout/i18n/mn.po`
- `addons/auth_timeout/i18n/my.po`
- `addons/auth_timeout/i18n/nb.po`
- `addons/auth_timeout/i18n/nl.po`
- `addons/auth_timeout/i18n/pl.po`
- `addons/auth_timeout/i18n/pt.po`
- `addons/auth_timeout/i18n/pt_BR.po`
- `addons/auth_timeout/i18n/ro.po`
- `addons/auth_timeout/i18n/ru.po`
- `addons/auth_timeout/i18n/sk.po`
- `addons/auth_timeout/i18n/sl.po`
- `addons/auth_timeout/i18n/sr@latin.po`
- `addons/auth_timeout/i18n/sv.po`
- `addons/auth_timeout/i18n/th.po`
- `addons/auth_timeout/i18n/tr.po`
- `addons/auth_timeout/i18n/uk.po`
- `addons/auth_timeout/i18n/uz.po`
- `addons/auth_timeout/i18n/vi.po`
- `addons/auth_timeout/i18n/zh_CN.po`
- `addons/auth_timeout/i18n/zh_TW.po`
- `addons/auth_timeout/models/__init__.py`
- `addons/auth_timeout/models/auth_totp_device.py`
- `addons/auth_timeout/models/ir_http.py`
- `addons/auth_timeout/models/ir_websocket.py`
- `addons/auth_timeout/models/res_groups.py`
- `addons/auth_timeout/models/res_users.py`
- `addons/auth_timeout/static/src/services/check_identity/check_identity.js`
- `addons/auth_timeout/static/tests/tours/auth_timeout_tour.js`
- `addons/auth_timeout/tests/__init__.py`
- `addons/auth_timeout/tests/test_auth_timeout.py`
- `addons/auth_timeout/views/res_groups_views.xml`
