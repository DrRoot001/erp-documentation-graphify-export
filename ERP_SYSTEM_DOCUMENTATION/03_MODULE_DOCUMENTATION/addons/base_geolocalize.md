# Module: base_geolocalize

- **Module ID:** MOD-036
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/base_geolocalize`
- **Manifest:** `addons/base_geolocalize/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Partners Geolocation
========================

**Scope evidence:** The module contains 68 files, including 8 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `base_setup`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 4
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/base_geolocalize/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 23 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/base_geolocalize/models/res_partner.py:5`, `addons/base_geolocalize/models/res_config_settings.py:7`, `addons/base_geolocalize/models/base_geocoder.py:17`, `addons/base_geolocalize/models/base_geocoder.py:25`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/base_geolocalize/data/ir_cron.xml:4`, `addons/base_geolocalize/data/data.xml:3`, `addons/base_geolocalize/data/data.xml:8`, `addons/base_geolocalize/views/res_config_settings_views.xml:3`, `addons/base_geolocalize/views/geo_provider_view.xml:5`, `addons/base_geolocalize/views/res_partner_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/base_geolocalize/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 4 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/base_geolocalize/__manifest__.py`, `addons/base_geolocalize/models/res_partner.py`, `addons/base_geolocalize/data/ir_cron.xml`, `addons/base_geolocalize/tests/test_geolocalize.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/base_geolocalize/tests/test_geolocalize.py`, `addons/base_geolocalize/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `ir_cron_geolocalize_required_partners`, `geoprovider_open_street`, `geoprovider_google_map`, `res_config_settings_view_form`, `view_geo_provider_form`, `view_crm_partner_geo_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/base_geolocalize/views/res_config_settings_views.xml:5`, `addons/base_geolocalize/views/res_config_settings_views.xml:7`, `addons/base_geolocalize/views/geo_provider_view.xml:7`, `addons/base_geolocalize/views/geo_provider_view.xml:8`, `addons/base_geolocalize/views/res_partner_views.xml:5`, `addons/base_geolocalize/views/res_partner_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/base_geolocalize/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/base_geolocalize/__manifest__.py`, `addons/base_geolocalize/models/res_partner.py`, `addons/base_geolocalize/data/ir_cron.xml`, `addons/base_geolocalize/tests/test_geolocalize.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `res.partner` (addons/base_geolocalize/models/res_partner.py:5); inherits `res.config.settings` (addons/base_geolocalize/models/res_config_settings.py:7); `base.geo_provider` (addons/base_geolocalize/models/base_geocoder.py:17); `base.geocoder` (addons/base_geolocalize/models/base_geocoder.py:25)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base_setup`
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

- `addons/base_geolocalize/README.md`
- `addons/base_geolocalize/__init__.py`
- `addons/base_geolocalize/__manifest__.py`
- `addons/base_geolocalize/data/data.xml`
- `addons/base_geolocalize/data/ir_cron.xml`
- `addons/base_geolocalize/i18n/af.po`
- `addons/base_geolocalize/i18n/ar.po`
- `addons/base_geolocalize/i18n/az.po`
- `addons/base_geolocalize/i18n/base_geolocalize.pot`
- `addons/base_geolocalize/i18n/bg.po`
- `addons/base_geolocalize/i18n/bs.po`
- `addons/base_geolocalize/i18n/ca.po`
- `addons/base_geolocalize/i18n/cs.po`
- `addons/base_geolocalize/i18n/da.po`
- `addons/base_geolocalize/i18n/de.po`
- `addons/base_geolocalize/i18n/el.po`
- `addons/base_geolocalize/i18n/es.po`
- `addons/base_geolocalize/i18n/es_419.po`
- `addons/base_geolocalize/i18n/et.po`
- `addons/base_geolocalize/i18n/fa.po`
- `addons/base_geolocalize/i18n/fi.po`
- `addons/base_geolocalize/i18n/fr.po`
- `addons/base_geolocalize/i18n/gu.po`
- `addons/base_geolocalize/i18n/he.po`
- `addons/base_geolocalize/i18n/hi.po`
- `addons/base_geolocalize/i18n/hr.po`
- `addons/base_geolocalize/i18n/hu.po`
- `addons/base_geolocalize/i18n/id.po`
- `addons/base_geolocalize/i18n/is.po`
- `addons/base_geolocalize/i18n/it.po`
- `addons/base_geolocalize/i18n/ja.po`
- `addons/base_geolocalize/i18n/kab.po`
- `addons/base_geolocalize/i18n/km.po`
- `addons/base_geolocalize/i18n/ko.po`
- `addons/base_geolocalize/i18n/ku.po`
- `addons/base_geolocalize/i18n/lo.po`
- `addons/base_geolocalize/i18n/lt.po`
- `addons/base_geolocalize/i18n/lv.po`
- `addons/base_geolocalize/i18n/mn.po`
- `addons/base_geolocalize/i18n/my.po`
- `addons/base_geolocalize/i18n/nb.po`
- `addons/base_geolocalize/i18n/nl.po`
- `addons/base_geolocalize/i18n/pl.po`
- `addons/base_geolocalize/i18n/pt.po`
- `addons/base_geolocalize/i18n/pt_BR.po`
- `addons/base_geolocalize/i18n/ro.po`
- `addons/base_geolocalize/i18n/ru.po`
- `addons/base_geolocalize/i18n/sk.po`
- `addons/base_geolocalize/i18n/sl.po`
- `addons/base_geolocalize/i18n/sr@latin.po`
- `addons/base_geolocalize/i18n/sv.po`
- `addons/base_geolocalize/i18n/th.po`
- `addons/base_geolocalize/i18n/tr.po`
- `addons/base_geolocalize/i18n/uk.po`
- `addons/base_geolocalize/i18n/uz.po`
- `addons/base_geolocalize/i18n/vi.po`
- `addons/base_geolocalize/i18n/zh_CN.po`
- `addons/base_geolocalize/i18n/zh_TW.po`
- `addons/base_geolocalize/models/__init__.py`
- `addons/base_geolocalize/models/base_geocoder.py`
- `addons/base_geolocalize/models/res_config_settings.py`
- `addons/base_geolocalize/models/res_partner.py`
- `addons/base_geolocalize/security/ir.access.csv`
- `addons/base_geolocalize/tests/__init__.py`
- `addons/base_geolocalize/tests/test_geolocalize.py`
- `addons/base_geolocalize/views/geo_provider_view.xml`
- `addons/base_geolocalize/views/res_config_settings_views.xml`
- `addons/base_geolocalize/views/res_partner_views.xml`
