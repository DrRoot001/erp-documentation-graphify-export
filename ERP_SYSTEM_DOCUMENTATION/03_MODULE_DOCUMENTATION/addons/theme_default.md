# Module: theme_default

- **Module ID:** MOD-589
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/theme_default`
- **Manifest:** `addons/theme_default/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Theme`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Default website theme

**Scope evidence:** The module contains 55 files, including 2 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `website`.

## 2. Module structure

- Model/business logic files: 0
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

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/theme_default/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Not found
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/theme_default/__init__.py`
- `addons/theme_default/__manifest__.py`
- `addons/theme_default/data/generate_primary_template.xml`
- `addons/theme_default/i18n/ar.po`
- `addons/theme_default/i18n/az.po`
- `addons/theme_default/i18n/bg.po`
- `addons/theme_default/i18n/bs.po`
- `addons/theme_default/i18n/ca.po`
- `addons/theme_default/i18n/cs.po`
- `addons/theme_default/i18n/da.po`
- `addons/theme_default/i18n/de.po`
- `addons/theme_default/i18n/el.po`
- `addons/theme_default/i18n/es.po`
- `addons/theme_default/i18n/es_419.po`
- `addons/theme_default/i18n/et.po`
- `addons/theme_default/i18n/fa.po`
- `addons/theme_default/i18n/fi.po`
- `addons/theme_default/i18n/fr.po`
- `addons/theme_default/i18n/he.po`
- `addons/theme_default/i18n/hi.po`
- `addons/theme_default/i18n/hr.po`
- `addons/theme_default/i18n/hu.po`
- `addons/theme_default/i18n/id.po`
- `addons/theme_default/i18n/it.po`
- `addons/theme_default/i18n/ja.po`
- `addons/theme_default/i18n/kab.po`
- `addons/theme_default/i18n/ko.po`
- `addons/theme_default/i18n/ku.po`
- `addons/theme_default/i18n/lo.po`
- `addons/theme_default/i18n/lt.po`
- `addons/theme_default/i18n/lv.po`
- `addons/theme_default/i18n/mn.po`
- `addons/theme_default/i18n/my.po`
- `addons/theme_default/i18n/nb.po`
- `addons/theme_default/i18n/nl.po`
- `addons/theme_default/i18n/pl.po`
- `addons/theme_default/i18n/pt.po`
- `addons/theme_default/i18n/pt_BR.po`
- `addons/theme_default/i18n/ro.po`
- `addons/theme_default/i18n/ru.po`
- `addons/theme_default/i18n/sk.po`
- `addons/theme_default/i18n/sl.po`
- `addons/theme_default/i18n/sr@latin.po`
- `addons/theme_default/i18n/sv.po`
- `addons/theme_default/i18n/th.po`
- `addons/theme_default/i18n/theme_default.pot`
- `addons/theme_default/i18n/tr.po`
- `addons/theme_default/i18n/uk.po`
- `addons/theme_default/i18n/uz.po`
- `addons/theme_default/i18n/vi.po`
- `addons/theme_default/i18n/zh_CN.po`
- `addons/theme_default/i18n/zh_TW.po`
- `addons/theme_default/static/description/cover.png`
- `addons/theme_default/static/description/icon.png`
- `addons/theme_default/static/description/theme_default_screenshot.jpg`
