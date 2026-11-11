# Module: iap_mail

- **Module ID:** MOD-110
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/iap_mail`
- **Manifest:** `addons/iap_mail/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Bridge between IAP and mail

**Manifest description:**

Bridge between IAP and mail

**Scope evidence:** The module contains 58 files, including 4 Python, 2 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `iap`, `mail`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 1
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 1 model declarations, 4 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/iap_mail/models/iap_account.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 1 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/iap_mail/data/mail_templates.xml:4`, `addons/iap_mail/data/mail_templates.xml:114`, `addons/iap_mail/views/iap_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `enrich_company`, `enrich_company_by_dnb`, `iap_account_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/iap_mail/data/mail_templates.xml:4`, `addons/iap_mail/data/mail_templates.xml:114`
- View/action field declarations: 2; representative evidence: `addons/iap_mail/views/iap_views.xml:6`, `addons/iap_mail/views/iap_views.xml:8`
- Browser assets: 1; representative files: `addons/iap_mail/static/src/js/services/iap_notification_service.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/iap_mail/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: `iap.account` (addons/iap_mail/models/iap_account.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `iap`, `mail`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/iap_mail/__init__.py`
- `addons/iap_mail/__manifest__.py`
- `addons/iap_mail/data/mail_templates.xml`
- `addons/iap_mail/i18n/ar.po`
- `addons/iap_mail/i18n/az.po`
- `addons/iap_mail/i18n/bg.po`
- `addons/iap_mail/i18n/bs.po`
- `addons/iap_mail/i18n/ca.po`
- `addons/iap_mail/i18n/cs.po`
- `addons/iap_mail/i18n/da.po`
- `addons/iap_mail/i18n/de.po`
- `addons/iap_mail/i18n/el.po`
- `addons/iap_mail/i18n/es.po`
- `addons/iap_mail/i18n/es_419.po`
- `addons/iap_mail/i18n/et.po`
- `addons/iap_mail/i18n/fa.po`
- `addons/iap_mail/i18n/fi.po`
- `addons/iap_mail/i18n/fr.po`
- `addons/iap_mail/i18n/he.po`
- `addons/iap_mail/i18n/hi.po`
- `addons/iap_mail/i18n/hr.po`
- `addons/iap_mail/i18n/hu.po`
- `addons/iap_mail/i18n/iap_mail.pot`
- `addons/iap_mail/i18n/id.po`
- `addons/iap_mail/i18n/it.po`
- `addons/iap_mail/i18n/ja.po`
- `addons/iap_mail/i18n/kab.po`
- `addons/iap_mail/i18n/ko.po`
- `addons/iap_mail/i18n/ku.po`
- `addons/iap_mail/i18n/lo.po`
- `addons/iap_mail/i18n/lt.po`
- `addons/iap_mail/i18n/lv.po`
- `addons/iap_mail/i18n/mn.po`
- `addons/iap_mail/i18n/my.po`
- `addons/iap_mail/i18n/nb.po`
- `addons/iap_mail/i18n/nl.po`
- `addons/iap_mail/i18n/pl.po`
- `addons/iap_mail/i18n/pt.po`
- `addons/iap_mail/i18n/pt_BR.po`
- `addons/iap_mail/i18n/ro.po`
- `addons/iap_mail/i18n/ru.po`
- `addons/iap_mail/i18n/sk.po`
- `addons/iap_mail/i18n/sl.po`
- `addons/iap_mail/i18n/sr@latin.po`
- `addons/iap_mail/i18n/sv.po`
- `addons/iap_mail/i18n/th.po`
- `addons/iap_mail/i18n/tr.po`
- `addons/iap_mail/i18n/uk.po`
- `addons/iap_mail/i18n/uz.po`
- `addons/iap_mail/i18n/vi.po`
- `addons/iap_mail/i18n/zh_CN.po`
- `addons/iap_mail/i18n/zh_TW.po`
- `addons/iap_mail/models/__init__.py`
- `addons/iap_mail/models/iap_account.py`
- `addons/iap_mail/static/src/js/services/iap_notification_service.js`
- `addons/iap_mail/static/src/scss/iap_mail.dark.scss`
- `addons/iap_mail/static/src/scss/iap_mail.scss`
- `addons/iap_mail/views/iap_views.xml`
