# Module: mail_plugin

- **Module ID:** MOD-355
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/mail_plugin`
- **Manifest:** `addons/mail_plugin/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/CRM`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Allows integration with mail plugins.

**Manifest description:**

Integrate Odoo with your mailbox, get information about contacts directly inside your mailbox, log content of emails as internal notes

**Scope evidence:** The module contains 65 files, including 10 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `digest`, `web`, `contacts`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 3
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 1 model declarations, 26 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/mail_plugin/models/ir_http.py:14`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 10 route declarations.
- **Evidence:** `addons/mail_plugin/controllers/authenticate.py:21`, `addons/mail_plugin/controllers/authenticate.py:34`, `addons/mail_plugin/controllers/authenticate.py:58`, `addons/mail_plugin/controllers/authenticate.py:65`, `addons/mail_plugin/controllers/mail_plugin.py:21`, `addons/mail_plugin/controllers/mail_plugin.py:48`, `addons/mail_plugin/controllers/mail_plugin.py:74`, `addons/mail_plugin/controllers/mail_plugin.py:80`, `addons/mail_plugin/controllers/mail_plugin.py:135`, `addons/mail_plugin/controllers/mail_plugin.py:186`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/mail_plugin/data/digest_tips.xml:4`, `addons/mail_plugin/views/mail_plugin_login.xml:3`, `addons/mail_plugin/views/mail_plugin_login.xml:21`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/mail_plugin/tests/test_controller.py`, `addons/mail_plugin/tests/common.py`, `addons/mail_plugin/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `digest_tip_mail_plugin`, `Accept app`, `Accept app`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/mail_plugin/views/mail_plugin_login.xml:3`, `addons/mail_plugin/views/mail_plugin_login.xml:21`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/mail_plugin/__manifest__.py`
- **HTTP entry points:** `addons/mail_plugin/controllers/authenticate.py:21`, `addons/mail_plugin/controllers/authenticate.py:34`, `addons/mail_plugin/controllers/authenticate.py:58`, `addons/mail_plugin/controllers/authenticate.py:65`, `addons/mail_plugin/controllers/mail_plugin.py:21`, `addons/mail_plugin/controllers/mail_plugin.py:48`, `addons/mail_plugin/controllers/mail_plugin.py:74`, `addons/mail_plugin/controllers/mail_plugin.py:80`, `addons/mail_plugin/controllers/mail_plugin.py:135`, `addons/mail_plugin/controllers/mail_plugin.py:186`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `ir.http` (addons/mail_plugin/models/ir_http.py:14)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 10
- Route evidence: `addons/mail_plugin/controllers/authenticate.py:21`, `addons/mail_plugin/controllers/authenticate.py:34`, `addons/mail_plugin/controllers/authenticate.py:58`, `addons/mail_plugin/controllers/authenticate.py:65`, `addons/mail_plugin/controllers/mail_plugin.py:21`, `addons/mail_plugin/controllers/mail_plugin.py:48`, `addons/mail_plugin/controllers/mail_plugin.py:74`, `addons/mail_plugin/controllers/mail_plugin.py:80`, `addons/mail_plugin/controllers/mail_plugin.py:135`, `addons/mail_plugin/controllers/mail_plugin.py:186`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `digest`, `web`, `contacts`
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

- `addons/mail_plugin/__init__.py`
- `addons/mail_plugin/__manifest__.py`
- `addons/mail_plugin/controllers/__init__.py`
- `addons/mail_plugin/controllers/authenticate.py`
- `addons/mail_plugin/controllers/mail_plugin.py`
- `addons/mail_plugin/data/digest_tips.xml`
- `addons/mail_plugin/i18n/ar.po`
- `addons/mail_plugin/i18n/az.po`
- `addons/mail_plugin/i18n/bg.po`
- `addons/mail_plugin/i18n/bs.po`
- `addons/mail_plugin/i18n/ca.po`
- `addons/mail_plugin/i18n/cs.po`
- `addons/mail_plugin/i18n/da.po`
- `addons/mail_plugin/i18n/de.po`
- `addons/mail_plugin/i18n/el.po`
- `addons/mail_plugin/i18n/es.po`
- `addons/mail_plugin/i18n/es_419.po`
- `addons/mail_plugin/i18n/et.po`
- `addons/mail_plugin/i18n/fa.po`
- `addons/mail_plugin/i18n/fi.po`
- `addons/mail_plugin/i18n/fr.po`
- `addons/mail_plugin/i18n/he.po`
- `addons/mail_plugin/i18n/hi.po`
- `addons/mail_plugin/i18n/hr.po`
- `addons/mail_plugin/i18n/hu.po`
- `addons/mail_plugin/i18n/id.po`
- `addons/mail_plugin/i18n/it.po`
- `addons/mail_plugin/i18n/ja.po`
- `addons/mail_plugin/i18n/kab.po`
- `addons/mail_plugin/i18n/ko.po`
- `addons/mail_plugin/i18n/ku.po`
- `addons/mail_plugin/i18n/lo.po`
- `addons/mail_plugin/i18n/lt.po`
- `addons/mail_plugin/i18n/lv.po`
- `addons/mail_plugin/i18n/mail_plugin.pot`
- `addons/mail_plugin/i18n/mn.po`
- `addons/mail_plugin/i18n/my.po`
- `addons/mail_plugin/i18n/nb.po`
- `addons/mail_plugin/i18n/nl.po`
- `addons/mail_plugin/i18n/pl.po`
- `addons/mail_plugin/i18n/pt.po`
- `addons/mail_plugin/i18n/pt_BR.po`
- `addons/mail_plugin/i18n/ro.po`
- `addons/mail_plugin/i18n/ru.po`
- `addons/mail_plugin/i18n/sk.po`
- `addons/mail_plugin/i18n/sl.po`
- `addons/mail_plugin/i18n/sr@latin.po`
- `addons/mail_plugin/i18n/sv.po`
- `addons/mail_plugin/i18n/th.po`
- `addons/mail_plugin/i18n/tr.po`
- `addons/mail_plugin/i18n/uk.po`
- `addons/mail_plugin/i18n/uz.po`
- `addons/mail_plugin/i18n/vi.po`
- `addons/mail_plugin/i18n/zh_CN.po`
- `addons/mail_plugin/i18n/zh_TW.po`
- `addons/mail_plugin/models/__init__.py`
- `addons/mail_plugin/models/ir_http.py`
- `addons/mail_plugin/static/src/img/gmail.png`
- `addons/mail_plugin/static/src/img/outlook.png`
- `addons/mail_plugin/static/src/to_translate/translations_gmail.xml`
- `addons/mail_plugin/static/src/to_translate/translations_outlook.xml`
- `addons/mail_plugin/tests/__init__.py`
- `addons/mail_plugin/tests/common.py`
- `addons/mail_plugin/tests/test_controller.py`
- `addons/mail_plugin/views/mail_plugin_login.xml`
