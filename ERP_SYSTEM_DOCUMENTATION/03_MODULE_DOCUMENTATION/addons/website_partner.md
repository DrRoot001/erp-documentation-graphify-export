# Module: website_partner

- **Module ID:** MOD-629
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_partner`
- **Manifest:** `addons/website_partner/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Partner module for website

**Manifest description:**

This is a base module. It holds website-related stuff for Contact model (res.partner).

**Scope evidence:** The module contains 67 files, including 6 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `website`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 2
- XML/data/view/template files: 4
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

- **Description:** 1 model declarations, 8 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/website_partner/models/res_partner.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/website_partner/controllers/main.py:19`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 16 record/template/menu identifiers.
- **Evidence:** `addons/website_partner/data/website_partner_data.xml:3`, `addons/website_partner/data/website_partner_data.xml:9`, `addons/website_partner/data/website_partner_data.xml:15`, `addons/website_partner/data/website_partner_demo.xml:4`, `addons/website_partner/data/website_partner_demo.xml:7`, `addons/website_partner/data/website_partner_demo.xml:10`, `addons/website_partner/data/website_partner_demo.xml:14`, `addons/website_partner/data/website_partner_demo.xml:21`, `addons/website_partner/data/website_partner_demo.xml:32`, `addons/website_partner/data/website_partner_demo.xml:40`, `addons/website_partner/data/website_partner_demo.xml:51`, `addons/website_partner/data/website_partner_demo.xml:79`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `base.main_partner`, `mt_partner_published`, `mt_partner_unpublished`, `base.partner_admin`, `base.partner_demo`, `base.partner_demo_portal`, `base.res_partner_2`, `base.res_partner_1`, `base.res_partner_4`, `base.res_partner_3`, `base.res_partner_10`, `base.res_partner_18`, `base.res_partner_12`, `Partner Page`, `Partner Details`, `view_partners_form_website`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/website_partner/views/website_partner_templates.xml:3`, `addons/website_partner/views/website_partner_templates.xml:17`
- View/action field declarations: 4; representative evidence: `addons/website_partner/data/website_partner_data.xml:11`, `addons/website_partner/data/website_partner_data.xml:17`, `addons/website_partner/views/res_partner_views.xml:5`, `addons/website_partner/views/res_partner_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_partner/__manifest__.py`
- **HTTP entry points:** `addons/website_partner/controllers/main.py:19`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: `res.partner` (addons/website_partner/models/res_partner.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/website_partner/controllers/main.py:19`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website`
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

- `addons/website_partner/__init__.py`
- `addons/website_partner/__manifest__.py`
- `addons/website_partner/controllers/__init__.py`
- `addons/website_partner/controllers/main.py`
- `addons/website_partner/data/website_partner_data.xml`
- `addons/website_partner/data/website_partner_demo.xml`
- `addons/website_partner/i18n/af.po`
- `addons/website_partner/i18n/ar.po`
- `addons/website_partner/i18n/az.po`
- `addons/website_partner/i18n/bg.po`
- `addons/website_partner/i18n/bs.po`
- `addons/website_partner/i18n/ca.po`
- `addons/website_partner/i18n/cs.po`
- `addons/website_partner/i18n/da.po`
- `addons/website_partner/i18n/de.po`
- `addons/website_partner/i18n/el.po`
- `addons/website_partner/i18n/es.po`
- `addons/website_partner/i18n/es_419.po`
- `addons/website_partner/i18n/et.po`
- `addons/website_partner/i18n/fa.po`
- `addons/website_partner/i18n/fi.po`
- `addons/website_partner/i18n/fr.po`
- `addons/website_partner/i18n/gu.po`
- `addons/website_partner/i18n/he.po`
- `addons/website_partner/i18n/hi.po`
- `addons/website_partner/i18n/hr.po`
- `addons/website_partner/i18n/hu.po`
- `addons/website_partner/i18n/id.po`
- `addons/website_partner/i18n/is.po`
- `addons/website_partner/i18n/it.po`
- `addons/website_partner/i18n/ja.po`
- `addons/website_partner/i18n/kab.po`
- `addons/website_partner/i18n/km.po`
- `addons/website_partner/i18n/ko.po`
- `addons/website_partner/i18n/ku.po`
- `addons/website_partner/i18n/lo.po`
- `addons/website_partner/i18n/lt.po`
- `addons/website_partner/i18n/lv.po`
- `addons/website_partner/i18n/mk.po`
- `addons/website_partner/i18n/mn.po`
- `addons/website_partner/i18n/my.po`
- `addons/website_partner/i18n/nb.po`
- `addons/website_partner/i18n/nl.po`
- `addons/website_partner/i18n/pl.po`
- `addons/website_partner/i18n/pt.po`
- `addons/website_partner/i18n/pt_BR.po`
- `addons/website_partner/i18n/ro.po`
- `addons/website_partner/i18n/ru.po`
- `addons/website_partner/i18n/sk.po`
- `addons/website_partner/i18n/sl.po`
- `addons/website_partner/i18n/sr@latin.po`
- `addons/website_partner/i18n/sv.po`
- `addons/website_partner/i18n/th.po`
- `addons/website_partner/i18n/tr.po`
- `addons/website_partner/i18n/uk.po`
- `addons/website_partner/i18n/uz.po`
- `addons/website_partner/i18n/vi.po`
- `addons/website_partner/i18n/website_partner.pot`
- `addons/website_partner/i18n/zh_CN.po`
- `addons/website_partner/i18n/zh_TW.po`
- `addons/website_partner/models/__init__.py`
- `addons/website_partner/models/res_partner.py`
- `addons/website_partner/static/description/icon.png`
- `addons/website_partner/static/description/icon.svg`
- `addons/website_partner/static/description/icon_hi.png`
- `addons/website_partner/views/res_partner_views.xml`
- `addons/website_partner/views/website_partner_templates.xml`
