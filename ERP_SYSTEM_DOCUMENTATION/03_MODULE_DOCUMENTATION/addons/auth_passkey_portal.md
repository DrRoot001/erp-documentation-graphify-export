# Module: auth_passkey_portal

- **Module ID:** MOD-023
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/auth_passkey_portal`
- **Manifest:** `addons/auth_passkey_portal/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Passkeys for portal users

**Manifest description:**

The implementation of Passkeys using the webauthn protocol.
===========================================================

Passkeys are a secure alternative to a username and a password.
When a user logs in with a Passkey, MFA will not be required.

**Scope evidence:** The module contains 58 files, including 4 Python, 2 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `auth_passkey`, `portal`.

## 2. Module structure

- Model/business logic files: 0
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 3
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### User interface and data

- **Description:** 2 XML files and 3 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/auth_passkey_portal/views/templates.xml:2`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/auth_passkey_portal/tests/test_passkey_portal.py`, `addons/auth_passkey_portal/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `Passkeys Portal hook`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/auth_passkey_portal/views/templates.xml:2`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 3; representative files: `addons/auth_passkey_portal/static/src/js/passkeys_portal.js`, `addons/auth_passkey_portal/static/src/js/passkeys_portal_create.js`, `addons/auth_passkey_portal/static/tests/tours/test_passkey_portal.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/auth_passkey_portal/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `auth_passkey`, `portal`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Not found
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/auth_passkey_portal/__init__.py`
- `addons/auth_passkey_portal/__manifest__.py`
- `addons/auth_passkey_portal/i18n/ar.po`
- `addons/auth_passkey_portal/i18n/auth_passkey_portal.pot`
- `addons/auth_passkey_portal/i18n/az.po`
- `addons/auth_passkey_portal/i18n/bg.po`
- `addons/auth_passkey_portal/i18n/bs.po`
- `addons/auth_passkey_portal/i18n/ca.po`
- `addons/auth_passkey_portal/i18n/cs.po`
- `addons/auth_passkey_portal/i18n/da.po`
- `addons/auth_passkey_portal/i18n/de.po`
- `addons/auth_passkey_portal/i18n/el.po`
- `addons/auth_passkey_portal/i18n/es.po`
- `addons/auth_passkey_portal/i18n/es_419.po`
- `addons/auth_passkey_portal/i18n/et.po`
- `addons/auth_passkey_portal/i18n/fa.po`
- `addons/auth_passkey_portal/i18n/fi.po`
- `addons/auth_passkey_portal/i18n/fr.po`
- `addons/auth_passkey_portal/i18n/he.po`
- `addons/auth_passkey_portal/i18n/hi.po`
- `addons/auth_passkey_portal/i18n/hr.po`
- `addons/auth_passkey_portal/i18n/hu.po`
- `addons/auth_passkey_portal/i18n/id.po`
- `addons/auth_passkey_portal/i18n/it.po`
- `addons/auth_passkey_portal/i18n/ja.po`
- `addons/auth_passkey_portal/i18n/kab.po`
- `addons/auth_passkey_portal/i18n/ko.po`
- `addons/auth_passkey_portal/i18n/ku.po`
- `addons/auth_passkey_portal/i18n/lo.po`
- `addons/auth_passkey_portal/i18n/lt.po`
- `addons/auth_passkey_portal/i18n/lv.po`
- `addons/auth_passkey_portal/i18n/mn.po`
- `addons/auth_passkey_portal/i18n/my.po`
- `addons/auth_passkey_portal/i18n/nb.po`
- `addons/auth_passkey_portal/i18n/nl.po`
- `addons/auth_passkey_portal/i18n/pl.po`
- `addons/auth_passkey_portal/i18n/pt.po`
- `addons/auth_passkey_portal/i18n/pt_BR.po`
- `addons/auth_passkey_portal/i18n/ro.po`
- `addons/auth_passkey_portal/i18n/ru.po`
- `addons/auth_passkey_portal/i18n/sk.po`
- `addons/auth_passkey_portal/i18n/sl.po`
- `addons/auth_passkey_portal/i18n/sr@latin.po`
- `addons/auth_passkey_portal/i18n/sv.po`
- `addons/auth_passkey_portal/i18n/th.po`
- `addons/auth_passkey_portal/i18n/tr.po`
- `addons/auth_passkey_portal/i18n/uk.po`
- `addons/auth_passkey_portal/i18n/uz.po`
- `addons/auth_passkey_portal/i18n/vi.po`
- `addons/auth_passkey_portal/i18n/zh_CN.po`
- `addons/auth_passkey_portal/i18n/zh_TW.po`
- `addons/auth_passkey_portal/static/src/js/passkeys_portal.js`
- `addons/auth_passkey_portal/static/src/js/passkeys_portal_create.js`
- `addons/auth_passkey_portal/static/src/xml/passkeys_portal_popups.xml`
- `addons/auth_passkey_portal/static/tests/tours/test_passkey_portal.js`
- `addons/auth_passkey_portal/tests/__init__.py`
- `addons/auth_passkey_portal/tests/test_passkey_portal.py`
- `addons/auth_passkey_portal/views/templates.xml`
