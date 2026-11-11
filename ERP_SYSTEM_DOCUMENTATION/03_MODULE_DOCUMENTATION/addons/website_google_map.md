# Module: website_google_map

- **Module ID:** MOD-619
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_google_map`
- **Manifest:** `addons/website_google_map/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Show your company address on Google Maps

**Manifest description:**

Show your company address/partner address on Google Maps. Configure an API key in the Website settings.

**Scope evidence:** The module contains 76 files, including 4 Python, 1 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `base_geolocalize`, `website_partner`.

## 2. Module structure

- Model/business logic files: 0
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

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/website_google_map/controllers/main.py:30`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 2 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/website_google_map/views/google_map_templates.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `google_map`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/website_google_map/views/google_map_templates.xml:3`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 2; representative files: `addons/website_google_map/static/src/lib/markerclusterer.js`, `addons/website_google_map/static/src/js/website_google_map.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_google_map/__manifest__.py`
- **HTTP entry points:** `addons/website_google_map/controllers/main.py:30`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/website_google_map/controllers/main.py:30`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base_geolocalize`, `website_partner`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Not found
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/website_google_map/__init__.py`
- `addons/website_google_map/__manifest__.py`
- `addons/website_google_map/controllers/__init__.py`
- `addons/website_google_map/controllers/main.py`
- `addons/website_google_map/i18n/ar.po`
- `addons/website_google_map/i18n/az.po`
- `addons/website_google_map/i18n/bg.po`
- `addons/website_google_map/i18n/bs.po`
- `addons/website_google_map/i18n/ca.po`
- `addons/website_google_map/i18n/cs.po`
- `addons/website_google_map/i18n/da.po`
- `addons/website_google_map/i18n/de.po`
- `addons/website_google_map/i18n/el.po`
- `addons/website_google_map/i18n/es.po`
- `addons/website_google_map/i18n/es_419.po`
- `addons/website_google_map/i18n/et.po`
- `addons/website_google_map/i18n/fa.po`
- `addons/website_google_map/i18n/fi.po`
- `addons/website_google_map/i18n/fr.po`
- `addons/website_google_map/i18n/he.po`
- `addons/website_google_map/i18n/hi.po`
- `addons/website_google_map/i18n/hr.po`
- `addons/website_google_map/i18n/hu.po`
- `addons/website_google_map/i18n/id.po`
- `addons/website_google_map/i18n/it.po`
- `addons/website_google_map/i18n/ja.po`
- `addons/website_google_map/i18n/kab.po`
- `addons/website_google_map/i18n/ko.po`
- `addons/website_google_map/i18n/ku.po`
- `addons/website_google_map/i18n/lo.po`
- `addons/website_google_map/i18n/lt.po`
- `addons/website_google_map/i18n/lv.po`
- `addons/website_google_map/i18n/mn.po`
- `addons/website_google_map/i18n/my.po`
- `addons/website_google_map/i18n/nb.po`
- `addons/website_google_map/i18n/nl.po`
- `addons/website_google_map/i18n/pl.po`
- `addons/website_google_map/i18n/pt.po`
- `addons/website_google_map/i18n/pt_BR.po`
- `addons/website_google_map/i18n/ro.po`
- `addons/website_google_map/i18n/ru.po`
- `addons/website_google_map/i18n/sk.po`
- `addons/website_google_map/i18n/sl.po`
- `addons/website_google_map/i18n/sr@latin.po`
- `addons/website_google_map/i18n/sv.po`
- `addons/website_google_map/i18n/th.po`
- `addons/website_google_map/i18n/tr.po`
- `addons/website_google_map/i18n/uk.po`
- `addons/website_google_map/i18n/uz.po`
- `addons/website_google_map/i18n/vi.po`
- `addons/website_google_map/i18n/website_google_map.pot`
- `addons/website_google_map/i18n/zh_CN.po`
- `addons/website_google_map/i18n/zh_TW.po`
- `addons/website_google_map/static/description/icon.png`
- `addons/website_google_map/static/description/icon.svg`
- `addons/website_google_map/static/description/icon_hi.png`
- `addons/website_google_map/static/src/css/website_google_map.css`
- `addons/website_google_map/static/src/img/partners.png`
- `addons/website_google_map/static/src/js/website_google_map.js`
- `addons/website_google_map/static/src/lib/images/conv30.png`
- `addons/website_google_map/static/src/lib/images/conv40.png`
- `addons/website_google_map/static/src/lib/images/conv50.png`
- `addons/website_google_map/static/src/lib/images/heart30.png`
- `addons/website_google_map/static/src/lib/images/heart40.png`
- `addons/website_google_map/static/src/lib/images/heart50.png`
- `addons/website_google_map/static/src/lib/images/m1.png`
- `addons/website_google_map/static/src/lib/images/m2.png`
- `addons/website_google_map/static/src/lib/images/m3.png`
- `addons/website_google_map/static/src/lib/images/m4.png`
- `addons/website_google_map/static/src/lib/images/m5.png`
- `addons/website_google_map/static/src/lib/images/people35.png`
- `addons/website_google_map/static/src/lib/images/people45.png`
- `addons/website_google_map/static/src/lib/images/people55.png`
- `addons/website_google_map/static/src/lib/images/pin.png`
- `addons/website_google_map/static/src/lib/markerclusterer.js`
- `addons/website_google_map/views/google_map_templates.xml`
