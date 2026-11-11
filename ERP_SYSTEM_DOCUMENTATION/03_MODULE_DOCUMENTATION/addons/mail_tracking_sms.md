# Module: mail_tracking_sms

- **Module ID:** MOD-358
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/mail_tracking_sms`
- **Manifest:** `addons/mail_tracking_sms/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Productivity/Discuss`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Track source of messages by sms

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 57 files, including 7 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `mail_tracking`, `sms`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 1
- Browser asset files: 0
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 4 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/mail_tracking_sms/models/mail_message.py:4`, `addons/mail_tracking_sms/models/mail_thread.py:4`, `addons/mail_tracking_sms/wizard/sms_composer.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/mail_tracking_sms/views/mail_message_views.xml:4`, `addons/mail_tracking_sms/views/mail_message_views.xml:15`, `addons/mail_tracking_sms/views/mail_message_views.xml:26`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `mail_message_view_list`, `mail_message_view_form`, `mail_message_view_search`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/mail_tracking_sms/views/mail_message_views.xml:6`, `addons/mail_tracking_sms/views/mail_message_views.xml:8`, `addons/mail_tracking_sms/views/mail_message_views.xml:17`, `addons/mail_tracking_sms/views/mail_message_views.xml:19`, `addons/mail_tracking_sms/views/mail_message_views.xml:28`, `addons/mail_tracking_sms/views/mail_message_views.xml:30`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/mail_tracking_sms/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `mail.message` (addons/mail_tracking_sms/models/mail_message.py:4); inherits `mail.thread` (addons/mail_tracking_sms/models/mail_thread.py:4); inherits `sms.composer` (addons/mail_tracking_sms/wizard/sms_composer.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mail_tracking`, `sms`
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

- `addons/mail_tracking_sms/__init__.py`
- `addons/mail_tracking_sms/__manifest__.py`
- `addons/mail_tracking_sms/i18n/ar.po`
- `addons/mail_tracking_sms/i18n/az.po`
- `addons/mail_tracking_sms/i18n/bg.po`
- `addons/mail_tracking_sms/i18n/bs.po`
- `addons/mail_tracking_sms/i18n/ca.po`
- `addons/mail_tracking_sms/i18n/cs.po`
- `addons/mail_tracking_sms/i18n/da.po`
- `addons/mail_tracking_sms/i18n/de.po`
- `addons/mail_tracking_sms/i18n/el.po`
- `addons/mail_tracking_sms/i18n/es.po`
- `addons/mail_tracking_sms/i18n/es_419.po`
- `addons/mail_tracking_sms/i18n/et.po`
- `addons/mail_tracking_sms/i18n/fa.po`
- `addons/mail_tracking_sms/i18n/fi.po`
- `addons/mail_tracking_sms/i18n/fr.po`
- `addons/mail_tracking_sms/i18n/he.po`
- `addons/mail_tracking_sms/i18n/hi.po`
- `addons/mail_tracking_sms/i18n/hr.po`
- `addons/mail_tracking_sms/i18n/hu.po`
- `addons/mail_tracking_sms/i18n/id.po`
- `addons/mail_tracking_sms/i18n/it.po`
- `addons/mail_tracking_sms/i18n/ja.po`
- `addons/mail_tracking_sms/i18n/kab.po`
- `addons/mail_tracking_sms/i18n/ko.po`
- `addons/mail_tracking_sms/i18n/ku.po`
- `addons/mail_tracking_sms/i18n/lo.po`
- `addons/mail_tracking_sms/i18n/lt.po`
- `addons/mail_tracking_sms/i18n/lv.po`
- `addons/mail_tracking_sms/i18n/mail_tracking_sms.pot`
- `addons/mail_tracking_sms/i18n/mn.po`
- `addons/mail_tracking_sms/i18n/my.po`
- `addons/mail_tracking_sms/i18n/nb.po`
- `addons/mail_tracking_sms/i18n/nl.po`
- `addons/mail_tracking_sms/i18n/pl.po`
- `addons/mail_tracking_sms/i18n/pt.po`
- `addons/mail_tracking_sms/i18n/pt_BR.po`
- `addons/mail_tracking_sms/i18n/ro.po`
- `addons/mail_tracking_sms/i18n/ru.po`
- `addons/mail_tracking_sms/i18n/sk.po`
- `addons/mail_tracking_sms/i18n/sl.po`
- `addons/mail_tracking_sms/i18n/sr@latin.po`
- `addons/mail_tracking_sms/i18n/sv.po`
- `addons/mail_tracking_sms/i18n/th.po`
- `addons/mail_tracking_sms/i18n/tr.po`
- `addons/mail_tracking_sms/i18n/uk.po`
- `addons/mail_tracking_sms/i18n/uz.po`
- `addons/mail_tracking_sms/i18n/vi.po`
- `addons/mail_tracking_sms/i18n/zh_CN.po`
- `addons/mail_tracking_sms/i18n/zh_TW.po`
- `addons/mail_tracking_sms/models/__init__.py`
- `addons/mail_tracking_sms/models/mail_message.py`
- `addons/mail_tracking_sms/models/mail_thread.py`
- `addons/mail_tracking_sms/views/mail_message_views.xml`
- `addons/mail_tracking_sms/wizard/__init__.py`
- `addons/mail_tracking_sms/wizard/sms_composer.py`
