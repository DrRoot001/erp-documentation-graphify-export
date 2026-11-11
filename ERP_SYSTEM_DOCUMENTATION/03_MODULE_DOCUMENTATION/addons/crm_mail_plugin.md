# Module: crm_mail_plugin

- **Module ID:** MOD-058
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/crm_mail_plugin`
- **Manifest:** `addons/crm_mail_plugin/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/CRM`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Turn emails received in your mailbox into leads and log their content as internal notes.

**Manifest description:**

Turn emails received in your mailbox into leads and log their content as internal notes.

**Scope evidence:** The module contains 57 files, including 6 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `crm`, `mail_plugin`.

## 2. Module structure

- Model/business logic files: 0
- Controller/API files: 2
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/crm_mail_plugin/controllers/mail_plugin.py:88`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/crm_mail_plugin/tests/test_crm_mail_plugin.py`, `addons/crm_mail_plugin/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/crm_mail_plugin/__manifest__.py`
- **HTTP entry points:** `addons/crm_mail_plugin/controllers/mail_plugin.py:88`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/crm_mail_plugin/controllers/mail_plugin.py:88`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `crm`, `mail_plugin`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Not found
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/crm_mail_plugin/__init__.py`
- `addons/crm_mail_plugin/__manifest__.py`
- `addons/crm_mail_plugin/controllers/__init__.py`
- `addons/crm_mail_plugin/controllers/mail_plugin.py`
- `addons/crm_mail_plugin/i18n/ar.po`
- `addons/crm_mail_plugin/i18n/az.po`
- `addons/crm_mail_plugin/i18n/bg.po`
- `addons/crm_mail_plugin/i18n/bs.po`
- `addons/crm_mail_plugin/i18n/ca.po`
- `addons/crm_mail_plugin/i18n/crm_mail_plugin.pot`
- `addons/crm_mail_plugin/i18n/cs.po`
- `addons/crm_mail_plugin/i18n/da.po`
- `addons/crm_mail_plugin/i18n/de.po`
- `addons/crm_mail_plugin/i18n/el.po`
- `addons/crm_mail_plugin/i18n/es.po`
- `addons/crm_mail_plugin/i18n/es_419.po`
- `addons/crm_mail_plugin/i18n/et.po`
- `addons/crm_mail_plugin/i18n/fa.po`
- `addons/crm_mail_plugin/i18n/fi.po`
- `addons/crm_mail_plugin/i18n/fr.po`
- `addons/crm_mail_plugin/i18n/he.po`
- `addons/crm_mail_plugin/i18n/hi.po`
- `addons/crm_mail_plugin/i18n/hr.po`
- `addons/crm_mail_plugin/i18n/hu.po`
- `addons/crm_mail_plugin/i18n/id.po`
- `addons/crm_mail_plugin/i18n/it.po`
- `addons/crm_mail_plugin/i18n/ja.po`
- `addons/crm_mail_plugin/i18n/kab.po`
- `addons/crm_mail_plugin/i18n/ko.po`
- `addons/crm_mail_plugin/i18n/ku.po`
- `addons/crm_mail_plugin/i18n/lo.po`
- `addons/crm_mail_plugin/i18n/lt.po`
- `addons/crm_mail_plugin/i18n/lv.po`
- `addons/crm_mail_plugin/i18n/mn.po`
- `addons/crm_mail_plugin/i18n/my.po`
- `addons/crm_mail_plugin/i18n/nb.po`
- `addons/crm_mail_plugin/i18n/nl.po`
- `addons/crm_mail_plugin/i18n/pl.po`
- `addons/crm_mail_plugin/i18n/pt.po`
- `addons/crm_mail_plugin/i18n/pt_BR.po`
- `addons/crm_mail_plugin/i18n/ro.po`
- `addons/crm_mail_plugin/i18n/ru.po`
- `addons/crm_mail_plugin/i18n/sk.po`
- `addons/crm_mail_plugin/i18n/sl.po`
- `addons/crm_mail_plugin/i18n/sr@latin.po`
- `addons/crm_mail_plugin/i18n/sv.po`
- `addons/crm_mail_plugin/i18n/th.po`
- `addons/crm_mail_plugin/i18n/tr.po`
- `addons/crm_mail_plugin/i18n/uk.po`
- `addons/crm_mail_plugin/i18n/uz.po`
- `addons/crm_mail_plugin/i18n/vi.po`
- `addons/crm_mail_plugin/i18n/zh_CN.po`
- `addons/crm_mail_plugin/i18n/zh_TW.po`
- `addons/crm_mail_plugin/static/src/to_translate/translations_gmail.xml`
- `addons/crm_mail_plugin/static/src/to_translate/translations_outlook.xml`
- `addons/crm_mail_plugin/tests/__init__.py`
- `addons/crm_mail_plugin/tests/test_crm_mail_plugin.py`
