# Module: event_booth

- **Module ID:** MOD-065
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/event_booth`
- **Manifest:** `addons/event_booth/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Events`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Manage event booths

**Manifest description:**

Create booths for your favorite event.

**Scope evidence:** The module contains 76 files, including 12 Python, 11 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `event`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 11
- Browser asset files: 0
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/event_booth/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 20 methods, 0 constraint handlers, 0 onchange handlers, and 8 dependency declarations.
- **Evidence:** `addons/event_booth/models/event_booth_category.py:7`, `addons/event_booth/models/event_type_booth.py:7`, `addons/event_booth/models/event_type.py:7`, `addons/event_booth/models/event_event.py:9`, `addons/event_booth/models/event_booth.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 11 XML files and 0 JavaScript/TypeScript files; static XML analysis found 63 record/template/menu identifiers.
- **Evidence:** `addons/event_booth/data/event_booth_demo.xml:5`, `addons/event_booth/data/event_booth_demo.xml:10`, `addons/event_booth/data/event_booth_demo.xml:15`, `addons/event_booth/data/event_booth_demo.xml:20`, `addons/event_booth/data/event_booth_demo.xml:25`, `addons/event_booth/data/event_booth_demo.xml:32`, `addons/event_booth/data/event_booth_demo.xml:35`, `addons/event_booth/data/event_booth_demo.xml:40`, `addons/event_booth/data/event_booth_demo.xml:45`, `addons/event_booth/data/event_booth_demo.xml:50`, `addons/event_booth/data/event_booth_demo.xml:57`, `addons/event_booth/data/event_booth_demo.xml:60`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/event_booth/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/event_booth/tests/common.py`, `addons/event_booth/tests/test_event_internals.py`, `addons/event_booth/tests/__init__.py`, `addons/event_booth/tests/test_event_booth_internals.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 11; representative identifiers: `event_booth_0_event_0`, `event_booth_1_event_0`, `event_booth_2_event_0`, `event_booth_3_event_0`, `event_booth_4_event_0`, `event.event_2`, `event_booth_0_event_2`, `event_booth_1_event_2`, `event_booth_2_event_2`, `event_booth_3_event_2`, `event.event_3`, `event_booth_0_event_3`, `event_booth_1_event_3`, `event_booth_2_event_3`, `event_booth_3_event_3`, `event_booth_00_event_7`, `event_booth_01_event_7`, `event_booth_02_event_7`, `event_booth_10_event_7`, `event_booth_11_event_7`
- Menus: 2; representative evidence: `addons/event_booth/views/event_menus.xml:4`, `addons/event_booth/views/event_menus.xml:9`
- Templates: 1; representative evidence: `addons/event_booth/data/mail_templates.xml:6`
- View/action field declarations: 54; representative evidence: `addons/event_booth/data/mail_message_subtype_data.xml:6`, `addons/event_booth/views/event_booth_views.xml:6`, `addons/event_booth/views/event_booth_views.xml:8`, `addons/event_booth/views/event_booth_views.xml:38`, `addons/event_booth/views/event_booth_views.xml:42`, `addons/event_booth/views/event_booth_views.xml:51`, `addons/event_booth/views/event_booth_views.xml:55`, `addons/event_booth/views/event_booth_views.xml:63`, `addons/event_booth/views/event_booth_views.xml:65`, `addons/event_booth/views/event_booth_views.xml:82`, `addons/event_booth/views/event_booth_views.xml:86`, `addons/event_booth/views/event_booth_views.xml:95`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/event_booth/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: `event.booth.category` (addons/event_booth/models/event_booth_category.py:7); `event.type.booth` (addons/event_booth/models/event_type_booth.py:7); inherits `event.type` (addons/event_booth/models/event_type.py:7); inherits `event.event` (addons/event_booth/models/event_event.py:9); `event.booth` (addons/event_booth/models/event_booth.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `event`
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

- `addons/event_booth/__init__.py`
- `addons/event_booth/__manifest__.py`
- `addons/event_booth/data/event_booth_category_data.xml`
- `addons/event_booth/data/event_booth_demo.xml`
- `addons/event_booth/data/event_type_demo.xml`
- `addons/event_booth/data/mail_message_subtype_data.xml`
- `addons/event_booth/data/mail_templates.xml`
- `addons/event_booth/i18n/ar.po`
- `addons/event_booth/i18n/az.po`
- `addons/event_booth/i18n/bg.po`
- `addons/event_booth/i18n/bs.po`
- `addons/event_booth/i18n/ca.po`
- `addons/event_booth/i18n/cs.po`
- `addons/event_booth/i18n/da.po`
- `addons/event_booth/i18n/de.po`
- `addons/event_booth/i18n/el.po`
- `addons/event_booth/i18n/es.po`
- `addons/event_booth/i18n/es_419.po`
- `addons/event_booth/i18n/et.po`
- `addons/event_booth/i18n/event_booth.pot`
- `addons/event_booth/i18n/fa.po`
- `addons/event_booth/i18n/fi.po`
- `addons/event_booth/i18n/fr.po`
- `addons/event_booth/i18n/he.po`
- `addons/event_booth/i18n/hi.po`
- `addons/event_booth/i18n/hr.po`
- `addons/event_booth/i18n/hu.po`
- `addons/event_booth/i18n/id.po`
- `addons/event_booth/i18n/it.po`
- `addons/event_booth/i18n/ja.po`
- `addons/event_booth/i18n/kab.po`
- `addons/event_booth/i18n/ko.po`
- `addons/event_booth/i18n/ku.po`
- `addons/event_booth/i18n/lo.po`
- `addons/event_booth/i18n/lt.po`
- `addons/event_booth/i18n/lv.po`
- `addons/event_booth/i18n/mn.po`
- `addons/event_booth/i18n/my.po`
- `addons/event_booth/i18n/nb.po`
- `addons/event_booth/i18n/nl.po`
- `addons/event_booth/i18n/pl.po`
- `addons/event_booth/i18n/pt.po`
- `addons/event_booth/i18n/pt_BR.po`
- `addons/event_booth/i18n/ro.po`
- `addons/event_booth/i18n/ru.po`
- `addons/event_booth/i18n/sk.po`
- `addons/event_booth/i18n/sl.po`
- `addons/event_booth/i18n/sr@latin.po`
- `addons/event_booth/i18n/sv.po`
- `addons/event_booth/i18n/th.po`
- `addons/event_booth/i18n/tr.po`
- `addons/event_booth/i18n/uk.po`
- `addons/event_booth/i18n/uz.po`
- `addons/event_booth/i18n/vi.po`
- `addons/event_booth/i18n/zh_CN.po`
- `addons/event_booth/i18n/zh_TW.po`
- `addons/event_booth/models/__init__.py`
- `addons/event_booth/models/event_booth.py`
- `addons/event_booth/models/event_booth_category.py`
- `addons/event_booth/models/event_event.py`
- `addons/event_booth/models/event_type.py`
- `addons/event_booth/models/event_type_booth.py`
- `addons/event_booth/security/ir.access.csv`
- `addons/event_booth/static/src/img/premium-booth.jpeg`
- `addons/event_booth/static/src/img/standard-booth.jpeg`
- `addons/event_booth/static/src/img/vip-booth.jpeg`
- `addons/event_booth/tests/__init__.py`
- `addons/event_booth/tests/common.py`
- `addons/event_booth/tests/test_event_booth_internals.py`
- `addons/event_booth/tests/test_event_internals.py`
- `addons/event_booth/views/event_booth_category_views.xml`
- `addons/event_booth/views/event_booth_views.xml`
- `addons/event_booth/views/event_event_views.xml`
- `addons/event_booth/views/event_menus.xml`
- `addons/event_booth/views/event_type_booth_views.xml`
- `addons/event_booth/views/event_type_views.xml`
