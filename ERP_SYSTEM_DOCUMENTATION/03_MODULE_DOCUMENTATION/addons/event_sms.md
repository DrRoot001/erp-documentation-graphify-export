# Module: event_sms

- **Module ID:** MOD-071
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/event_sms`
- **Manifest:** `addons/event_sms/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Events`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Schedule SMS in event management

**Scope evidence:** The module contains 62 files, including 9 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `event`, `sms`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/event_sms/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 11 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/event_sms/models/event_mail_registration.py:4`, `addons/event_sms/models/event_mail.py:4`, `addons/event_sms/models/event_type_mail.py:4`, `addons/event_sms/models/sms_template.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/event_sms/data/sms_data.xml:4`, `addons/event_sms/data/sms_data.xml:10`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/event_sms/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/event_sms/tests/test_sms_schedule.py`, `addons/event_sms/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `sms_template_data_event_registration`, `sms_template_data_event_reminder`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/event_sms/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `event.mail.registration` (addons/event_sms/models/event_mail_registration.py:4); inherits `event.mail` (addons/event_sms/models/event_mail.py:4); inherits `event.type.mail` (addons/event_sms/models/event_type_mail.py:4); inherits `sms.template` (addons/event_sms/models/sms_template.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `event`, `sms`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/event_sms/__init__.py`
- `addons/event_sms/__manifest__.py`
- `addons/event_sms/data/sms_data.xml`
- `addons/event_sms/i18n/ar.po`
- `addons/event_sms/i18n/az.po`
- `addons/event_sms/i18n/bg.po`
- `addons/event_sms/i18n/bs.po`
- `addons/event_sms/i18n/ca.po`
- `addons/event_sms/i18n/cs.po`
- `addons/event_sms/i18n/da.po`
- `addons/event_sms/i18n/de.po`
- `addons/event_sms/i18n/el.po`
- `addons/event_sms/i18n/es.po`
- `addons/event_sms/i18n/es_419.po`
- `addons/event_sms/i18n/et.po`
- `addons/event_sms/i18n/event_sms.pot`
- `addons/event_sms/i18n/fa.po`
- `addons/event_sms/i18n/fi.po`
- `addons/event_sms/i18n/fr.po`
- `addons/event_sms/i18n/he.po`
- `addons/event_sms/i18n/hi.po`
- `addons/event_sms/i18n/hr.po`
- `addons/event_sms/i18n/hu.po`
- `addons/event_sms/i18n/id.po`
- `addons/event_sms/i18n/it.po`
- `addons/event_sms/i18n/ja.po`
- `addons/event_sms/i18n/kab.po`
- `addons/event_sms/i18n/ko.po`
- `addons/event_sms/i18n/ku.po`
- `addons/event_sms/i18n/lo.po`
- `addons/event_sms/i18n/lt.po`
- `addons/event_sms/i18n/lv.po`
- `addons/event_sms/i18n/mn.po`
- `addons/event_sms/i18n/my.po`
- `addons/event_sms/i18n/nb.po`
- `addons/event_sms/i18n/nl.po`
- `addons/event_sms/i18n/pl.po`
- `addons/event_sms/i18n/pt.po`
- `addons/event_sms/i18n/pt_BR.po`
- `addons/event_sms/i18n/ro.po`
- `addons/event_sms/i18n/ru.po`
- `addons/event_sms/i18n/sk.po`
- `addons/event_sms/i18n/sl.po`
- `addons/event_sms/i18n/sr@latin.po`
- `addons/event_sms/i18n/sv.po`
- `addons/event_sms/i18n/th.po`
- `addons/event_sms/i18n/tr.po`
- `addons/event_sms/i18n/uk.po`
- `addons/event_sms/i18n/uz.po`
- `addons/event_sms/i18n/vi.po`
- `addons/event_sms/i18n/zh_CN.po`
- `addons/event_sms/i18n/zh_TW.po`
- `addons/event_sms/models/__init__.py`
- `addons/event_sms/models/event_mail.py`
- `addons/event_sms/models/event_mail_registration.py`
- `addons/event_sms/models/event_type_mail.py`
- `addons/event_sms/models/sms_template.py`
- `addons/event_sms/security/ir.access.csv`
- `addons/event_sms/static/src/template_reference_field/field_event_mail_template_reference.scss`
- `addons/event_sms/static/src/template_reference_field/field_event_mail_template_reference.xml`
- `addons/event_sms/tests/__init__.py`
- `addons/event_sms/tests/test_sms_schedule.py`
