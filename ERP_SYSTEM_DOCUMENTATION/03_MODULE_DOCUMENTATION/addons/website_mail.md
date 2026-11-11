# Module: website_mail

- **Module ID:** MOD-624
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_mail`
- **Manifest:** `addons/website_mail/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Website Module for Mail

**Manifest description:**

Module holding mail improvements for website. It holds the follow widget.

**Scope evidence:** The module contains 72 files, including 7 Python, 1 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `website`, `mail`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 2
- XML/data/view/template files: 1
- Browser asset files: 2
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 6 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/website_mail/models/ir_http.py:6`, `addons/website_mail/models/update.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 2 route declarations.
- **Evidence:** `addons/website_mail/controllers/main.py:10`, `addons/website_mail/controllers/main.py:59`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 2 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/website_mail/views/website_mail_templates.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `follow`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/website_mail/views/website_mail_templates.xml:3`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 2; representative files: `addons/website_mail/static/src/interactions/follow.js`, `addons/website_mail/static/src/interactions/follow.edit.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_mail/__manifest__.py`
- **HTTP entry points:** `addons/website_mail/controllers/main.py:10`, `addons/website_mail/controllers/main.py:59`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `ir.http` (addons/website_mail/models/ir_http.py:6); inherits `publisher_warranty.contract` (addons/website_mail/models/update.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 2
- Route evidence: `addons/website_mail/controllers/main.py:10`, `addons/website_mail/controllers/main.py:59`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website`, `mail`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/website_mail/__init__.py`
- `addons/website_mail/__manifest__.py`
- `addons/website_mail/controllers/__init__.py`
- `addons/website_mail/controllers/main.py`
- `addons/website_mail/i18n/ar.po`
- `addons/website_mail/i18n/az.po`
- `addons/website_mail/i18n/bg.po`
- `addons/website_mail/i18n/bs.po`
- `addons/website_mail/i18n/ca.po`
- `addons/website_mail/i18n/cs.po`
- `addons/website_mail/i18n/da.po`
- `addons/website_mail/i18n/de.po`
- `addons/website_mail/i18n/el.po`
- `addons/website_mail/i18n/es.po`
- `addons/website_mail/i18n/es_419.po`
- `addons/website_mail/i18n/et.po`
- `addons/website_mail/i18n/fa.po`
- `addons/website_mail/i18n/fi.po`
- `addons/website_mail/i18n/fr.po`
- `addons/website_mail/i18n/gu.po`
- `addons/website_mail/i18n/he.po`
- `addons/website_mail/i18n/hi.po`
- `addons/website_mail/i18n/hr.po`
- `addons/website_mail/i18n/hu.po`
- `addons/website_mail/i18n/id.po`
- `addons/website_mail/i18n/is.po`
- `addons/website_mail/i18n/it.po`
- `addons/website_mail/i18n/ja.po`
- `addons/website_mail/i18n/kab.po`
- `addons/website_mail/i18n/ko.po`
- `addons/website_mail/i18n/ku.po`
- `addons/website_mail/i18n/lo.po`
- `addons/website_mail/i18n/lt.po`
- `addons/website_mail/i18n/lv.po`
- `addons/website_mail/i18n/mk.po`
- `addons/website_mail/i18n/mn.po`
- `addons/website_mail/i18n/my.po`
- `addons/website_mail/i18n/nb.po`
- `addons/website_mail/i18n/nl.po`
- `addons/website_mail/i18n/pl.po`
- `addons/website_mail/i18n/pt.po`
- `addons/website_mail/i18n/pt_BR.po`
- `addons/website_mail/i18n/ro.po`
- `addons/website_mail/i18n/ru.po`
- `addons/website_mail/i18n/sk.po`
- `addons/website_mail/i18n/sl.po`
- `addons/website_mail/i18n/sr@latin.po`
- `addons/website_mail/i18n/sv.po`
- `addons/website_mail/i18n/th.po`
- `addons/website_mail/i18n/tr.po`
- `addons/website_mail/i18n/uk.po`
- `addons/website_mail/i18n/uz.po`
- `addons/website_mail/i18n/vi.po`
- `addons/website_mail/i18n/website_mail.pot`
- `addons/website_mail/i18n/zh_CN.po`
- `addons/website_mail/i18n/zh_TW.po`
- `addons/website_mail/models/__init__.py`
- `addons/website_mail/models/ir_http.py`
- `addons/website_mail/models/update.py`
- `addons/website_mail/static/src/css/website_mail.scss`
- `addons/website_mail/static/src/img/thumbnail/airmail.png`
- `addons/website_mail/static/src/img/thumbnail/basic.png`
- `addons/website_mail/static/src/img/thumbnail/cleave.png`
- `addons/website_mail/static/src/img/thumbnail/go.png`
- `addons/website_mail/static/src/img/thumbnail/narrative.png`
- `addons/website_mail/static/src/img/thumbnail/neopolitan.png`
- `addons/website_mail/static/src/img/thumbnail/skyline.png`
- `addons/website_mail/static/src/img/thumbnail/sunday.png`
- `addons/website_mail/static/src/img/thumbnail/zenflat.png`
- `addons/website_mail/static/src/interactions/follow.edit.js`
- `addons/website_mail/static/src/interactions/follow.js`
- `addons/website_mail/views/website_mail_templates.xml`
