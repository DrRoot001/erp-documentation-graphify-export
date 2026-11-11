# Module: website_event_booth_exhibitor

- **Module ID:** MOD-608
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_event_booth_exhibitor`
- **Manifest:** `addons/website_event_booth_exhibitor/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Events`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Event Booths, automatically create a sponsor.

**Manifest description:**

Automatically create a sponsor when renting a booth.

**Scope evidence:** The module contains 67 files, including 9 Python, 6 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `website_event_exhibitor`, `website_event_booth`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 2
- XML/data/view/template files: 6
- Browser asset files: 3
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 10 methods, 0 constraint handlers, 1 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/website_event_booth_exhibitor/models/event_booth_category.py:7`, `addons/website_event_booth_exhibitor/models/event_booth.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/website_event_booth_exhibitor/controllers/__init__.py`, `addons/website_event_booth_exhibitor/controllers/event_booth.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 3 JavaScript/TypeScript files; static XML analysis found 9 record/template/menu identifiers.
- **Evidence:** `addons/website_event_booth_exhibitor/data/event_booth_category_data.xml:4`, `addons/website_event_booth_exhibitor/data/event_booth_category_data.xml:10`, `addons/website_event_booth_exhibitor/views/event_booth_views.xml:4`, `addons/website_event_booth_exhibitor/views/event_booth_templates.xml:4`, `addons/website_event_booth_exhibitor/views/event_booth_category_views.xml:4`, `addons/website_event_booth_exhibitor/views/event_booth_category_views.xml:20`, `addons/website_event_booth_exhibitor/views/event_booth_category_views.xml:34`, `addons/website_event_booth_exhibitor/views/event_booth_registration_templates.xml:4`, `addons/website_event_booth_exhibitor/views/mail_templates.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/website_event_booth_exhibitor/tests/__init__.py`, `addons/website_event_booth_exhibitor/tests/test_wevent_booth_exhibitor.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `event_booth.event_booth_category_premium`, `event_booth.event_booth_category_vip`, `event_booth_view_form_from_event`, `event_booth_registration`, `event_booth_category_view_form`, `event_booth_category_view_tree`, `event_booth_category_view_search`, `event_booth_registration_details`, `event_booth_booked_template`
- Menus: 0; representative evidence: Not found in module
- Templates: 3; representative evidence: `addons/website_event_booth_exhibitor/views/event_booth_templates.xml:4`, `addons/website_event_booth_exhibitor/views/event_booth_registration_templates.xml:4`, `addons/website_event_booth_exhibitor/views/mail_templates.xml:4`
- View/action field declarations: 8; representative evidence: `addons/website_event_booth_exhibitor/views/event_booth_views.xml:6`, `addons/website_event_booth_exhibitor/views/event_booth_views.xml:9`, `addons/website_event_booth_exhibitor/views/event_booth_category_views.xml:6`, `addons/website_event_booth_exhibitor/views/event_booth_category_views.xml:9`, `addons/website_event_booth_exhibitor/views/event_booth_category_views.xml:22`, `addons/website_event_booth_exhibitor/views/event_booth_category_views.xml:25`, `addons/website_event_booth_exhibitor/views/event_booth_category_views.xml:36`, `addons/website_event_booth_exhibitor/views/event_booth_category_views.xml:38`
- Browser assets: 3; representative files: `addons/website_event_booth_exhibitor/static/src/interactions/booth_sponsor_details.js`, `addons/website_event_booth_exhibitor/static/tests/tours/website_event_booth_exhibitor.js`, `addons/website_event_booth_exhibitor/static/tests/tours/website_event_booth_exhibitor_steps.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_event_booth_exhibitor/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `event.booth.category` (addons/website_event_booth_exhibitor/models/event_booth_category.py:7); inherits `event.booth` (addons/website_event_booth_exhibitor/models/event_booth.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_event_exhibitor`, `website_event_booth`
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

- `addons/website_event_booth_exhibitor/__init__.py`
- `addons/website_event_booth_exhibitor/__manifest__.py`
- `addons/website_event_booth_exhibitor/controllers/__init__.py`
- `addons/website_event_booth_exhibitor/controllers/event_booth.py`
- `addons/website_event_booth_exhibitor/data/event_booth_category_data.xml`
- `addons/website_event_booth_exhibitor/i18n/ar.po`
- `addons/website_event_booth_exhibitor/i18n/az.po`
- `addons/website_event_booth_exhibitor/i18n/bg.po`
- `addons/website_event_booth_exhibitor/i18n/bs.po`
- `addons/website_event_booth_exhibitor/i18n/ca.po`
- `addons/website_event_booth_exhibitor/i18n/cs.po`
- `addons/website_event_booth_exhibitor/i18n/da.po`
- `addons/website_event_booth_exhibitor/i18n/de.po`
- `addons/website_event_booth_exhibitor/i18n/el.po`
- `addons/website_event_booth_exhibitor/i18n/es.po`
- `addons/website_event_booth_exhibitor/i18n/es_419.po`
- `addons/website_event_booth_exhibitor/i18n/et.po`
- `addons/website_event_booth_exhibitor/i18n/fa.po`
- `addons/website_event_booth_exhibitor/i18n/fi.po`
- `addons/website_event_booth_exhibitor/i18n/fr.po`
- `addons/website_event_booth_exhibitor/i18n/he.po`
- `addons/website_event_booth_exhibitor/i18n/hi.po`
- `addons/website_event_booth_exhibitor/i18n/hr.po`
- `addons/website_event_booth_exhibitor/i18n/hu.po`
- `addons/website_event_booth_exhibitor/i18n/id.po`
- `addons/website_event_booth_exhibitor/i18n/it.po`
- `addons/website_event_booth_exhibitor/i18n/ja.po`
- `addons/website_event_booth_exhibitor/i18n/kab.po`
- `addons/website_event_booth_exhibitor/i18n/ko.po`
- `addons/website_event_booth_exhibitor/i18n/ku.po`
- `addons/website_event_booth_exhibitor/i18n/lo.po`
- `addons/website_event_booth_exhibitor/i18n/lt.po`
- `addons/website_event_booth_exhibitor/i18n/lv.po`
- `addons/website_event_booth_exhibitor/i18n/mn.po`
- `addons/website_event_booth_exhibitor/i18n/my.po`
- `addons/website_event_booth_exhibitor/i18n/nb.po`
- `addons/website_event_booth_exhibitor/i18n/nl.po`
- `addons/website_event_booth_exhibitor/i18n/pl.po`
- `addons/website_event_booth_exhibitor/i18n/pt.po`
- `addons/website_event_booth_exhibitor/i18n/pt_BR.po`
- `addons/website_event_booth_exhibitor/i18n/ro.po`
- `addons/website_event_booth_exhibitor/i18n/ru.po`
- `addons/website_event_booth_exhibitor/i18n/sk.po`
- `addons/website_event_booth_exhibitor/i18n/sl.po`
- `addons/website_event_booth_exhibitor/i18n/sr@latin.po`
- `addons/website_event_booth_exhibitor/i18n/sv.po`
- `addons/website_event_booth_exhibitor/i18n/th.po`
- `addons/website_event_booth_exhibitor/i18n/tr.po`
- `addons/website_event_booth_exhibitor/i18n/uk.po`
- `addons/website_event_booth_exhibitor/i18n/uz.po`
- `addons/website_event_booth_exhibitor/i18n/vi.po`
- `addons/website_event_booth_exhibitor/i18n/website_event_booth_exhibitor.pot`
- `addons/website_event_booth_exhibitor/i18n/zh_CN.po`
- `addons/website_event_booth_exhibitor/i18n/zh_TW.po`
- `addons/website_event_booth_exhibitor/models/__init__.py`
- `addons/website_event_booth_exhibitor/models/event_booth.py`
- `addons/website_event_booth_exhibitor/models/event_booth_category.py`
- `addons/website_event_booth_exhibitor/static/src/interactions/booth_sponsor_details.js`
- `addons/website_event_booth_exhibitor/static/tests/tours/website_event_booth_exhibitor.js`
- `addons/website_event_booth_exhibitor/static/tests/tours/website_event_booth_exhibitor_steps.js`
- `addons/website_event_booth_exhibitor/tests/__init__.py`
- `addons/website_event_booth_exhibitor/tests/test_wevent_booth_exhibitor.py`
- `addons/website_event_booth_exhibitor/views/event_booth_category_views.xml`
- `addons/website_event_booth_exhibitor/views/event_booth_registration_templates.xml`
- `addons/website_event_booth_exhibitor/views/event_booth_templates.xml`
- `addons/website_event_booth_exhibitor/views/event_booth_views.xml`
- `addons/website_event_booth_exhibitor/views/mail_templates.xml`
