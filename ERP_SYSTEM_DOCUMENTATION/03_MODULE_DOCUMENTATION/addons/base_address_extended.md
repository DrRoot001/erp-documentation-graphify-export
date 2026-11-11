# Module: base_address_extended

- **Module ID:** MOD-034
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/base_address_extended`
- **Manifest:** `addons/base_address_extended/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Add extra fields on addresses

**Manifest description:**

Extended Addresses Management
=============================

This module provides the ability to choose a city from a list (in specific countries).

It is primarily used for EDIs that might need a special city code.

**Scope evidence:** The module contains 65 files, including 8 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `web`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 3
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/base_address_extended/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 11 methods, 0 constraint handlers, 2 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/base_address_extended/models/res_partner.py:7`, `addons/base_address_extended/models/res_city.py:6`, `addons/base_address_extended/models/res_country.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/base_address_extended/views/res_city_view.xml:4`, `addons/base_address_extended/views/res_city_view.xml:16`, `addons/base_address_extended/views/res_city_view.xml:28`, `addons/base_address_extended/views/res_city_view.xml:52`, `addons/base_address_extended/views/res_country_view.xml:4`, `addons/base_address_extended/views/res_partner_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/base_address_extended/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/base_address_extended/tests/__init__.py`, `addons/base_address_extended/tests/test_street_fields.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `view_city_tree`, `view_city_filter`, `res_city_view_form`, `action_res_city_tree`, `view_res_country_city_extended_form`, `address_street_extended_city_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 12; representative evidence: `addons/base_address_extended/views/res_city_view.xml:6`, `addons/base_address_extended/views/res_city_view.xml:7`, `addons/base_address_extended/views/res_city_view.xml:17`, `addons/base_address_extended/views/res_city_view.xml:18`, `addons/base_address_extended/views/res_city_view.xml:30`, `addons/base_address_extended/views/res_city_view.xml:31`, `addons/base_address_extended/views/res_city_view.xml:54`, `addons/base_address_extended/views/res_city_view.xml:55`, `addons/base_address_extended/views/res_country_view.xml:5`, `addons/base_address_extended/views/res_country_view.xml:7`, `addons/base_address_extended/views/res_partner_views.xml:6`, `addons/base_address_extended/views/res_partner_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/base_address_extended/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `res.partner` (addons/base_address_extended/models/res_partner.py:7); `res.city` (addons/base_address_extended/models/res_city.py:6); inherits `res.country` (addons/base_address_extended/models/res_country.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `web`
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

- `addons/base_address_extended/__init__.py`
- `addons/base_address_extended/__manifest__.py`
- `addons/base_address_extended/i18n/af.po`
- `addons/base_address_extended/i18n/ar.po`
- `addons/base_address_extended/i18n/az.po`
- `addons/base_address_extended/i18n/base_address_extended.pot`
- `addons/base_address_extended/i18n/bg.po`
- `addons/base_address_extended/i18n/bs.po`
- `addons/base_address_extended/i18n/ca.po`
- `addons/base_address_extended/i18n/cs.po`
- `addons/base_address_extended/i18n/da.po`
- `addons/base_address_extended/i18n/de.po`
- `addons/base_address_extended/i18n/el.po`
- `addons/base_address_extended/i18n/es.po`
- `addons/base_address_extended/i18n/es_419.po`
- `addons/base_address_extended/i18n/et.po`
- `addons/base_address_extended/i18n/fa.po`
- `addons/base_address_extended/i18n/fi.po`
- `addons/base_address_extended/i18n/fr.po`
- `addons/base_address_extended/i18n/gu.po`
- `addons/base_address_extended/i18n/he.po`
- `addons/base_address_extended/i18n/hi.po`
- `addons/base_address_extended/i18n/hr.po`
- `addons/base_address_extended/i18n/hu.po`
- `addons/base_address_extended/i18n/id.po`
- `addons/base_address_extended/i18n/is.po`
- `addons/base_address_extended/i18n/it.po`
- `addons/base_address_extended/i18n/ja.po`
- `addons/base_address_extended/i18n/kab.po`
- `addons/base_address_extended/i18n/km.po`
- `addons/base_address_extended/i18n/ko.po`
- `addons/base_address_extended/i18n/ku.po`
- `addons/base_address_extended/i18n/lo.po`
- `addons/base_address_extended/i18n/lt.po`
- `addons/base_address_extended/i18n/lv.po`
- `addons/base_address_extended/i18n/mn.po`
- `addons/base_address_extended/i18n/my.po`
- `addons/base_address_extended/i18n/nb.po`
- `addons/base_address_extended/i18n/nl.po`
- `addons/base_address_extended/i18n/pl.po`
- `addons/base_address_extended/i18n/pt.po`
- `addons/base_address_extended/i18n/pt_BR.po`
- `addons/base_address_extended/i18n/ro.po`
- `addons/base_address_extended/i18n/ru.po`
- `addons/base_address_extended/i18n/sk.po`
- `addons/base_address_extended/i18n/sl.po`
- `addons/base_address_extended/i18n/sr@latin.po`
- `addons/base_address_extended/i18n/sv.po`
- `addons/base_address_extended/i18n/th.po`
- `addons/base_address_extended/i18n/tr.po`
- `addons/base_address_extended/i18n/uk.po`
- `addons/base_address_extended/i18n/uz.po`
- `addons/base_address_extended/i18n/vi.po`
- `addons/base_address_extended/i18n/zh_CN.po`
- `addons/base_address_extended/i18n/zh_TW.po`
- `addons/base_address_extended/models/__init__.py`
- `addons/base_address_extended/models/res_city.py`
- `addons/base_address_extended/models/res_country.py`
- `addons/base_address_extended/models/res_partner.py`
- `addons/base_address_extended/security/ir.access.csv`
- `addons/base_address_extended/tests/__init__.py`
- `addons/base_address_extended/tests/test_street_fields.py`
- `addons/base_address_extended/views/res_city_view.xml`
- `addons/base_address_extended/views/res_country_view.xml`
- `addons/base_address_extended/views/res_partner_views.xml`
