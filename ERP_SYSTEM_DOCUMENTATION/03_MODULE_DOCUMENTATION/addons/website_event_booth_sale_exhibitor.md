# Module: website_event_booth_sale_exhibitor

- **Module ID:** MOD-610
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_event_booth_sale_exhibitor`
- **Manifest:** `addons/website_event_booth_sale_exhibitor/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Events`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Bridge module between website_event_booth_exhibitor and website_event_booth_sale.

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 54 files, including 4 Python, 0 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `website_event_exhibitor`, `website_event_booth_sale`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 0
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

- **Description:** 1 model declarations, 1 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/website_event_booth_sale_exhibitor/models/event_booth_registration.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 0 XML files and 1 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 0; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 1; representative files: `addons/website_event_booth_sale_exhibitor/static/tests/tours/website_event_booth_sale_exhibitor.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_event_booth_sale_exhibitor/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `event.booth.registration` (addons/website_event_booth_sale_exhibitor/models/event_booth_registration.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_event_exhibitor`, `website_event_booth_sale`
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

- `addons/website_event_booth_sale_exhibitor/__init__.py`
- `addons/website_event_booth_sale_exhibitor/__manifest__.py`
- `addons/website_event_booth_sale_exhibitor/i18n/ar.po`
- `addons/website_event_booth_sale_exhibitor/i18n/az.po`
- `addons/website_event_booth_sale_exhibitor/i18n/bg.po`
- `addons/website_event_booth_sale_exhibitor/i18n/bs.po`
- `addons/website_event_booth_sale_exhibitor/i18n/ca.po`
- `addons/website_event_booth_sale_exhibitor/i18n/cs.po`
- `addons/website_event_booth_sale_exhibitor/i18n/da.po`
- `addons/website_event_booth_sale_exhibitor/i18n/de.po`
- `addons/website_event_booth_sale_exhibitor/i18n/el.po`
- `addons/website_event_booth_sale_exhibitor/i18n/es.po`
- `addons/website_event_booth_sale_exhibitor/i18n/es_419.po`
- `addons/website_event_booth_sale_exhibitor/i18n/et.po`
- `addons/website_event_booth_sale_exhibitor/i18n/fa.po`
- `addons/website_event_booth_sale_exhibitor/i18n/fi.po`
- `addons/website_event_booth_sale_exhibitor/i18n/fr.po`
- `addons/website_event_booth_sale_exhibitor/i18n/he.po`
- `addons/website_event_booth_sale_exhibitor/i18n/hi.po`
- `addons/website_event_booth_sale_exhibitor/i18n/hr.po`
- `addons/website_event_booth_sale_exhibitor/i18n/hu.po`
- `addons/website_event_booth_sale_exhibitor/i18n/id.po`
- `addons/website_event_booth_sale_exhibitor/i18n/it.po`
- `addons/website_event_booth_sale_exhibitor/i18n/ja.po`
- `addons/website_event_booth_sale_exhibitor/i18n/kab.po`
- `addons/website_event_booth_sale_exhibitor/i18n/ko.po`
- `addons/website_event_booth_sale_exhibitor/i18n/ku.po`
- `addons/website_event_booth_sale_exhibitor/i18n/lo.po`
- `addons/website_event_booth_sale_exhibitor/i18n/lt.po`
- `addons/website_event_booth_sale_exhibitor/i18n/lv.po`
- `addons/website_event_booth_sale_exhibitor/i18n/mn.po`
- `addons/website_event_booth_sale_exhibitor/i18n/my.po`
- `addons/website_event_booth_sale_exhibitor/i18n/nb.po`
- `addons/website_event_booth_sale_exhibitor/i18n/nl.po`
- `addons/website_event_booth_sale_exhibitor/i18n/pl.po`
- `addons/website_event_booth_sale_exhibitor/i18n/pt.po`
- `addons/website_event_booth_sale_exhibitor/i18n/pt_BR.po`
- `addons/website_event_booth_sale_exhibitor/i18n/ro.po`
- `addons/website_event_booth_sale_exhibitor/i18n/ru.po`
- `addons/website_event_booth_sale_exhibitor/i18n/sk.po`
- `addons/website_event_booth_sale_exhibitor/i18n/sl.po`
- `addons/website_event_booth_sale_exhibitor/i18n/sr@latin.po`
- `addons/website_event_booth_sale_exhibitor/i18n/sv.po`
- `addons/website_event_booth_sale_exhibitor/i18n/th.po`
- `addons/website_event_booth_sale_exhibitor/i18n/tr.po`
- `addons/website_event_booth_sale_exhibitor/i18n/uk.po`
- `addons/website_event_booth_sale_exhibitor/i18n/uz.po`
- `addons/website_event_booth_sale_exhibitor/i18n/vi.po`
- `addons/website_event_booth_sale_exhibitor/i18n/website_event_booth_sale_exhibitor.pot`
- `addons/website_event_booth_sale_exhibitor/i18n/zh_CN.po`
- `addons/website_event_booth_sale_exhibitor/i18n/zh_TW.po`
- `addons/website_event_booth_sale_exhibitor/models/__init__.py`
- `addons/website_event_booth_sale_exhibitor/models/event_booth_registration.py`
- `addons/website_event_booth_sale_exhibitor/static/tests/tours/website_event_booth_sale_exhibitor.js`
