# Module: website_event_booth

- **Module ID:** MOD-607
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_event_booth`
- **Manifest:** `addons/website_event_booth/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Events`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Events, display your booths on your website

**Manifest description:**

Display your booths on your website for the users to register.

**Scope evidence:** The module contains 69 files, including 10 Python, 6 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `website_event`, `event_booth`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 2
- XML/data/view/template files: 6
- Browser asset files: 1
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_event_booth/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 23 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/website_event_booth/models/event_type.py:7`, `addons/website_event_booth/models/website_event_menu.py:7`, `addons/website_event_booth/models/event_event.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 6 route declarations.
- **Evidence:** `addons/website_event_booth/controllers/event_booth.py:15`, `addons/website_event_booth/controllers/event_booth.py:26`, `addons/website_event_booth/controllers/event_booth.py:38`, `addons/website_event_booth/controllers/event_booth.py:78`, `addons/website_event_booth/controllers/event_booth.py:172`, `addons/website_event_booth/controllers/event_booth.py:181`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 1 JavaScript/TypeScript files; static XML analysis found 8 record/template/menu identifiers.
- **Evidence:** `addons/website_event_booth/data/event_demo.xml:4`, `addons/website_event_booth/data/event_demo.xml:10`, `addons/website_event_booth/views/event_booth_templates.xml:4`, `addons/website_event_booth/views/event_booth_templates.xml:44`, `addons/website_event_booth/views/event_booth_templates.xml:122`, `addons/website_event_booth/views/event_booth_registration_templates.xml:4`, `addons/website_event_booth/views/event_event_views.xml:4`, `addons/website_event_booth/views/event_type_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_event_booth/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/website_event_booth/tests/__init__.py`, `addons/website_event_booth/tests/test_event_booth.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `event.event_2`, `event.event_7`, `Event Booth Layout`, `Event Booth Registration`, `event_booth_order_progress`, `Event Booth Registration Details`, `event_event_view_form`, `event_type_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 4; representative evidence: `addons/website_event_booth/views/event_booth_templates.xml:4`, `addons/website_event_booth/views/event_booth_templates.xml:44`, `addons/website_event_booth/views/event_booth_templates.xml:122`, `addons/website_event_booth/views/event_booth_registration_templates.xml:4`
- View/action field declarations: 4; representative evidence: `addons/website_event_booth/views/event_event_views.xml:6`, `addons/website_event_booth/views/event_event_views.xml:8`, `addons/website_event_booth/views/event_type_views.xml:6`, `addons/website_event_booth/views/event_type_views.xml:8`
- Browser assets: 1; representative files: `addons/website_event_booth/static/src/interactions/booth_registration.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_event_booth/__manifest__.py`
- **HTTP entry points:** `addons/website_event_booth/controllers/event_booth.py:15`, `addons/website_event_booth/controllers/event_booth.py:26`, `addons/website_event_booth/controllers/event_booth.py:38`, `addons/website_event_booth/controllers/event_booth.py:78`, `addons/website_event_booth/controllers/event_booth.py:172`, `addons/website_event_booth/controllers/event_booth.py:181`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `event.type` (addons/website_event_booth/models/event_type.py:7); inherits `website.event.menu` (addons/website_event_booth/models/website_event_menu.py:7); inherits `event.event` (addons/website_event_booth/models/event_event.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 6
- Route evidence: `addons/website_event_booth/controllers/event_booth.py:15`, `addons/website_event_booth/controllers/event_booth.py:26`, `addons/website_event_booth/controllers/event_booth.py:38`, `addons/website_event_booth/controllers/event_booth.py:78`, `addons/website_event_booth/controllers/event_booth.py:172`, `addons/website_event_booth/controllers/event_booth.py:181`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_event`, `event_booth`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/website_event_booth/__init__.py`
- `addons/website_event_booth/__manifest__.py`
- `addons/website_event_booth/controllers/__init__.py`
- `addons/website_event_booth/controllers/event_booth.py`
- `addons/website_event_booth/data/event_demo.xml`
- `addons/website_event_booth/i18n/ar.po`
- `addons/website_event_booth/i18n/az.po`
- `addons/website_event_booth/i18n/bg.po`
- `addons/website_event_booth/i18n/bs.po`
- `addons/website_event_booth/i18n/ca.po`
- `addons/website_event_booth/i18n/cs.po`
- `addons/website_event_booth/i18n/da.po`
- `addons/website_event_booth/i18n/de.po`
- `addons/website_event_booth/i18n/el.po`
- `addons/website_event_booth/i18n/es.po`
- `addons/website_event_booth/i18n/es_419.po`
- `addons/website_event_booth/i18n/et.po`
- `addons/website_event_booth/i18n/fa.po`
- `addons/website_event_booth/i18n/fi.po`
- `addons/website_event_booth/i18n/fr.po`
- `addons/website_event_booth/i18n/he.po`
- `addons/website_event_booth/i18n/hi.po`
- `addons/website_event_booth/i18n/hr.po`
- `addons/website_event_booth/i18n/hu.po`
- `addons/website_event_booth/i18n/id.po`
- `addons/website_event_booth/i18n/it.po`
- `addons/website_event_booth/i18n/ja.po`
- `addons/website_event_booth/i18n/kab.po`
- `addons/website_event_booth/i18n/ko.po`
- `addons/website_event_booth/i18n/ku.po`
- `addons/website_event_booth/i18n/lo.po`
- `addons/website_event_booth/i18n/lt.po`
- `addons/website_event_booth/i18n/lv.po`
- `addons/website_event_booth/i18n/mn.po`
- `addons/website_event_booth/i18n/my.po`
- `addons/website_event_booth/i18n/nb.po`
- `addons/website_event_booth/i18n/nl.po`
- `addons/website_event_booth/i18n/pl.po`
- `addons/website_event_booth/i18n/pt.po`
- `addons/website_event_booth/i18n/pt_BR.po`
- `addons/website_event_booth/i18n/ro.po`
- `addons/website_event_booth/i18n/ru.po`
- `addons/website_event_booth/i18n/sk.po`
- `addons/website_event_booth/i18n/sl.po`
- `addons/website_event_booth/i18n/sr@latin.po`
- `addons/website_event_booth/i18n/sv.po`
- `addons/website_event_booth/i18n/th.po`
- `addons/website_event_booth/i18n/tr.po`
- `addons/website_event_booth/i18n/uk.po`
- `addons/website_event_booth/i18n/uz.po`
- `addons/website_event_booth/i18n/vi.po`
- `addons/website_event_booth/i18n/website_event_booth.pot`
- `addons/website_event_booth/i18n/zh_CN.po`
- `addons/website_event_booth/i18n/zh_TW.po`
- `addons/website_event_booth/models/__init__.py`
- `addons/website_event_booth/models/event_event.py`
- `addons/website_event_booth/models/event_type.py`
- `addons/website_event_booth/models/website_event_menu.py`
- `addons/website_event_booth/security/ir.access.csv`
- `addons/website_event_booth/static/src/img/exhibition-map.gif`
- `addons/website_event_booth/static/src/interactions/booth_registration.js`
- `addons/website_event_booth/static/src/scss/website_event_booth.scss`
- `addons/website_event_booth/static/src/xml/event_booth_registration_templates.xml`
- `addons/website_event_booth/tests/__init__.py`
- `addons/website_event_booth/tests/test_event_booth.py`
- `addons/website_event_booth/views/event_booth_registration_templates.xml`
- `addons/website_event_booth/views/event_booth_templates.xml`
- `addons/website_event_booth/views/event_event_views.xml`
- `addons/website_event_booth/views/event_type_views.xml`
