# Module: social_media

- **Module ID:** MOD-543
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/social_media`
- **Manifest:** `addons/social_media/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Social Marketing`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Social media connectors for company settings.

**Manifest description:**

The purpose of this technical module is to provide a front for
social media configuration for any other module that might need it.

**Scope evidence:** The module contains 58 files, including 4 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `base`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 2
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

- **Description:** 1 model declarations, 0 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/social_media/models/res_company.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/social_media/demo/res_company_demo.xml:3`, `addons/social_media/views/res_company_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `base.main_company`, `view_company_form_inherit_social_media`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/social_media/views/res_company_views.xml:6`, `addons/social_media/views/res_company_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/social_media/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `res.company` (addons/social_media/models/res_company.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`
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

- `addons/social_media/__init__.py`
- `addons/social_media/__manifest__.py`
- `addons/social_media/demo/res_company_demo.xml`
- `addons/social_media/i18n/ar.po`
- `addons/social_media/i18n/az.po`
- `addons/social_media/i18n/bg.po`
- `addons/social_media/i18n/bs.po`
- `addons/social_media/i18n/ca.po`
- `addons/social_media/i18n/cs.po`
- `addons/social_media/i18n/da.po`
- `addons/social_media/i18n/de.po`
- `addons/social_media/i18n/el.po`
- `addons/social_media/i18n/es.po`
- `addons/social_media/i18n/es_419.po`
- `addons/social_media/i18n/et.po`
- `addons/social_media/i18n/fa.po`
- `addons/social_media/i18n/fi.po`
- `addons/social_media/i18n/fr.po`
- `addons/social_media/i18n/gu.po`
- `addons/social_media/i18n/he.po`
- `addons/social_media/i18n/hi.po`
- `addons/social_media/i18n/hr.po`
- `addons/social_media/i18n/hu.po`
- `addons/social_media/i18n/id.po`
- `addons/social_media/i18n/is.po`
- `addons/social_media/i18n/it.po`
- `addons/social_media/i18n/ja.po`
- `addons/social_media/i18n/kab.po`
- `addons/social_media/i18n/km.po`
- `addons/social_media/i18n/ko.po`
- `addons/social_media/i18n/ku.po`
- `addons/social_media/i18n/lo.po`
- `addons/social_media/i18n/lt.po`
- `addons/social_media/i18n/lv.po`
- `addons/social_media/i18n/mn.po`
- `addons/social_media/i18n/my.po`
- `addons/social_media/i18n/nb.po`
- `addons/social_media/i18n/nl.po`
- `addons/social_media/i18n/pl.po`
- `addons/social_media/i18n/pt.po`
- `addons/social_media/i18n/pt_BR.po`
- `addons/social_media/i18n/ro.po`
- `addons/social_media/i18n/ru.po`
- `addons/social_media/i18n/sk.po`
- `addons/social_media/i18n/sl.po`
- `addons/social_media/i18n/social_media.pot`
- `addons/social_media/i18n/sr@latin.po`
- `addons/social_media/i18n/sv.po`
- `addons/social_media/i18n/th.po`
- `addons/social_media/i18n/tr.po`
- `addons/social_media/i18n/uk.po`
- `addons/social_media/i18n/uz.po`
- `addons/social_media/i18n/vi.po`
- `addons/social_media/i18n/zh_CN.po`
- `addons/social_media/i18n/zh_TW.po`
- `addons/social_media/models/__init__.py`
- `addons/social_media/models/res_company.py`
- `addons/social_media/views/res_company_views.xml`
