# Module: google_address_autocomplete

- **Module ID:** MOD-077
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/google_address_autocomplete`
- **Manifest:** `addons/google_address_autocomplete/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Assist with automatic completion & suggestions when filling address

**Manifest description:**

This module Auto complete the address data.

**Scope evidence:** The module contains 72 files, including 10 Python, 4 XML, and 4 JavaScript/TypeScript files. The manifest declares dependencies: `web`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 2
- XML/data/view/template files: 4
- Browser asset files: 4
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 13 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/google_address_autocomplete/models/res_partner.py:4`, `addons/google_address_autocomplete/models/res_config_settings.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 2 route declarations.
- **Evidence:** `addons/google_address_autocomplete/controllers/google_address_autocomplete.py:200`, `addons/google_address_autocomplete/controllers/google_address_autocomplete.py:213`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 4 JavaScript/TypeScript files; static XML analysis found 4 record/template/menu identifiers.
- **Evidence:** `addons/google_address_autocomplete/views/res_config_settings_views.xml:3`, `addons/google_address_autocomplete/views/res_company_views.xml:4`, `addons/google_address_autocomplete/views/res_partner_views.xml:3`, `addons/google_address_autocomplete/views/res_partner_views.xml:14`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/google_address_autocomplete/tests/test_ui.py`, `addons/google_address_autocomplete/tests/mock_google_places.py`, `addons/google_address_autocomplete/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `res_config_settings_view_form`, `view_company_form_inherit_address_autocomplete`, `view_partner_form_inherit_address_autocomplete`, `view_partner_address_form_inherit_address_autocomplete`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 8; representative evidence: `addons/google_address_autocomplete/views/res_config_settings_views.xml:5`, `addons/google_address_autocomplete/views/res_config_settings_views.xml:8`, `addons/google_address_autocomplete/views/res_company_views.xml:6`, `addons/google_address_autocomplete/views/res_company_views.xml:8`, `addons/google_address_autocomplete/views/res_partner_views.xml:5`, `addons/google_address_autocomplete/views/res_partner_views.xml:7`, `addons/google_address_autocomplete/views/res_partner_views.xml:16`, `addons/google_address_autocomplete/views/res_partner_views.xml:18`
- Browser assets: 4; representative files: `addons/google_address_autocomplete/static/src/google_places_session.js`, `addons/google_address_autocomplete/static/tests/google_address_autocomplete.test.js`, `addons/google_address_autocomplete/static/src/address_autocomplete/google_address_autocomplete.js`, `addons/google_address_autocomplete/static/tests/tours/autocomplete_address_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/google_address_autocomplete/__manifest__.py`
- **HTTP entry points:** `addons/google_address_autocomplete/controllers/google_address_autocomplete.py:200`, `addons/google_address_autocomplete/controllers/google_address_autocomplete.py:213`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `res.partner` (addons/google_address_autocomplete/models/res_partner.py:4); inherits `res.config.settings` (addons/google_address_autocomplete/models/res_config_settings.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 2
- Route evidence: `addons/google_address_autocomplete/controllers/google_address_autocomplete.py:200`, `addons/google_address_autocomplete/controllers/google_address_autocomplete.py:213`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `web`
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

- `addons/google_address_autocomplete/__init__.py`
- `addons/google_address_autocomplete/__manifest__.py`
- `addons/google_address_autocomplete/controllers/__init__.py`
- `addons/google_address_autocomplete/controllers/google_address_autocomplete.py`
- `addons/google_address_autocomplete/data/neutralize.sql`
- `addons/google_address_autocomplete/i18n/ar.po`
- `addons/google_address_autocomplete/i18n/az.po`
- `addons/google_address_autocomplete/i18n/bg.po`
- `addons/google_address_autocomplete/i18n/bs.po`
- `addons/google_address_autocomplete/i18n/ca.po`
- `addons/google_address_autocomplete/i18n/cs.po`
- `addons/google_address_autocomplete/i18n/da.po`
- `addons/google_address_autocomplete/i18n/de.po`
- `addons/google_address_autocomplete/i18n/el.po`
- `addons/google_address_autocomplete/i18n/es.po`
- `addons/google_address_autocomplete/i18n/es_419.po`
- `addons/google_address_autocomplete/i18n/et.po`
- `addons/google_address_autocomplete/i18n/fa.po`
- `addons/google_address_autocomplete/i18n/fi.po`
- `addons/google_address_autocomplete/i18n/fr.po`
- `addons/google_address_autocomplete/i18n/google_address_autocomplete.pot`
- `addons/google_address_autocomplete/i18n/he.po`
- `addons/google_address_autocomplete/i18n/hi.po`
- `addons/google_address_autocomplete/i18n/hr.po`
- `addons/google_address_autocomplete/i18n/hu.po`
- `addons/google_address_autocomplete/i18n/id.po`
- `addons/google_address_autocomplete/i18n/it.po`
- `addons/google_address_autocomplete/i18n/ja.po`
- `addons/google_address_autocomplete/i18n/kab.po`
- `addons/google_address_autocomplete/i18n/ko.po`
- `addons/google_address_autocomplete/i18n/ku.po`
- `addons/google_address_autocomplete/i18n/lo.po`
- `addons/google_address_autocomplete/i18n/lt.po`
- `addons/google_address_autocomplete/i18n/lv.po`
- `addons/google_address_autocomplete/i18n/mn.po`
- `addons/google_address_autocomplete/i18n/my.po`
- `addons/google_address_autocomplete/i18n/nb.po`
- `addons/google_address_autocomplete/i18n/nl.po`
- `addons/google_address_autocomplete/i18n/pl.po`
- `addons/google_address_autocomplete/i18n/pt.po`
- `addons/google_address_autocomplete/i18n/pt_BR.po`
- `addons/google_address_autocomplete/i18n/ro.po`
- `addons/google_address_autocomplete/i18n/ru.po`
- `addons/google_address_autocomplete/i18n/sk.po`
- `addons/google_address_autocomplete/i18n/sl.po`
- `addons/google_address_autocomplete/i18n/sr@latin.po`
- `addons/google_address_autocomplete/i18n/sv.po`
- `addons/google_address_autocomplete/i18n/th.po`
- `addons/google_address_autocomplete/i18n/tr.po`
- `addons/google_address_autocomplete/i18n/uk.po`
- `addons/google_address_autocomplete/i18n/uz.po`
- `addons/google_address_autocomplete/i18n/vi.po`
- `addons/google_address_autocomplete/i18n/zh_CN.po`
- `addons/google_address_autocomplete/i18n/zh_TW.po`
- `addons/google_address_autocomplete/models/__init__.py`
- `addons/google_address_autocomplete/models/res_config_settings.py`
- `addons/google_address_autocomplete/models/res_partner.py`
- `addons/google_address_autocomplete/static/src/address_autocomplete/google_address_autocomplete.js`
- `addons/google_address_autocomplete/static/src/address_autocomplete/google_address_autocomplete.scss`
- `addons/google_address_autocomplete/static/src/address_autocomplete/google_address_autocomplete.xml`
- `addons/google_address_autocomplete/static/src/address_autocomplete/google_address_autocomplete_dark.scss`
- `addons/google_address_autocomplete/static/src/google_places_session.js`
- `addons/google_address_autocomplete/static/src/img/powered_by_google_on_non_white.png`
- `addons/google_address_autocomplete/static/src/img/powered_by_google_on_white.png`
- `addons/google_address_autocomplete/static/tests/google_address_autocomplete.test.js`
- `addons/google_address_autocomplete/static/tests/tours/autocomplete_address_tour.js`
- `addons/google_address_autocomplete/tests/__init__.py`
- `addons/google_address_autocomplete/tests/mock_google_places.py`
- `addons/google_address_autocomplete/tests/test_ui.py`
- `addons/google_address_autocomplete/views/res_company_views.xml`
- `addons/google_address_autocomplete/views/res_config_settings_views.xml`
- `addons/google_address_autocomplete/views/res_partner_views.xml`
