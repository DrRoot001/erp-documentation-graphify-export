# Module: base_setup

- **Module ID:** MOD-042
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/base_setup`
- **Manifest:** `addons/base_setup/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module helps to configure the system at the installation of a new database.
================================================================================

Shows you a list of applications features to install from.

**Scope evidence:** The module contains 85 files, including 15 Python, 4 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `web`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 3
- XML/data/view/template files: 4
- Browser asset files: 1
- Security files: 0
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 37 methods, 0 constraint handlers, 0 onchange handlers, and 5 dependency declarations.
- **Evidence:** `addons/base_setup/models/kpi_provider.py:4`, `addons/base_setup/models/res_config_settings.py:8`, `addons/base_setup/models/ir_http.py:6`, `addons/base_setup/models/res_users.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 3 route declarations.
- **Evidence:** `addons/base_setup/controllers/kpi.py:149`, `addons/base_setup/controllers/main.py:10`, `addons/base_setup/controllers/main.py:53`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 1 JavaScript/TypeScript files; static XML analysis found 5 record/template/menu identifiers.
- **Evidence:** `addons/base_setup/data/base_setup_data.xml:4`, `addons/base_setup/views/res_config_settings_views.xml:3`, `addons/base_setup/views/res_config_settings_views.xml:206`, `addons/base_setup/views/res_config_settings_views.xml:214`, `addons/base_setup/views/res_partner_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/base_setup/tests/test_default_group.py`, `addons/base_setup/tests/test_res_config_doc_links.py`, `addons/base_setup/tests/test_kpi_controller.py`, `addons/base_setup/tests/__init__.py`, `addons/base_setup/tests/test_res_config.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `show_effect`, `res_config_settings_view_form`, `action_general_configuration`, `General Settings`, `res_partner_kanban_view`
- Menus: 1; representative evidence: `addons/base_setup/views/res_config_settings_views.xml:214`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/base_setup/views/res_config_settings_views.xml:5`, `addons/base_setup/views/res_config_settings_views.xml:8`, `addons/base_setup/views/res_config_settings_views.xml:209`, `addons/base_setup/views/res_config_settings_views.xml:210`, `addons/base_setup/views/res_partner_views.xml:6`, `addons/base_setup/views/res_partner_views.xml:8`
- Browser assets: 1; representative files: `addons/base_setup/static/src/views/module_views.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/base_setup/__manifest__.py`
- **HTTP entry points:** `addons/base_setup/controllers/kpi.py:149`, `addons/base_setup/controllers/main.py:10`, `addons/base_setup/controllers/main.py:53`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: `kpi.provider` (addons/base_setup/models/kpi_provider.py:4); inherits `res.config.settings` (addons/base_setup/models/res_config_settings.py:8); inherits `ir.http` (addons/base_setup/models/ir_http.py:6); inherits `res.users` (addons/base_setup/models/res_users.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 3
- Route evidence: `addons/base_setup/controllers/kpi.py:149`, `addons/base_setup/controllers/main.py:10`, `addons/base_setup/controllers/main.py:53`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `web`
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

- `addons/base_setup/__init__.py`
- `addons/base_setup/__manifest__.py`
- `addons/base_setup/controllers/__init__.py`
- `addons/base_setup/controllers/kpi.py`
- `addons/base_setup/controllers/main.py`
- `addons/base_setup/data/base_setup_data.xml`
- `addons/base_setup/i18n/af.po`
- `addons/base_setup/i18n/am.po`
- `addons/base_setup/i18n/ar.po`
- `addons/base_setup/i18n/az.po`
- `addons/base_setup/i18n/base_setup.pot`
- `addons/base_setup/i18n/bg.po`
- `addons/base_setup/i18n/bs.po`
- `addons/base_setup/i18n/ca.po`
- `addons/base_setup/i18n/cs.po`
- `addons/base_setup/i18n/da.po`
- `addons/base_setup/i18n/de.po`
- `addons/base_setup/i18n/el.po`
- `addons/base_setup/i18n/es.po`
- `addons/base_setup/i18n/es_419.po`
- `addons/base_setup/i18n/es_CL.po`
- `addons/base_setup/i18n/et.po`
- `addons/base_setup/i18n/eu.po`
- `addons/base_setup/i18n/fa.po`
- `addons/base_setup/i18n/fi.po`
- `addons/base_setup/i18n/fo.po`
- `addons/base_setup/i18n/fr.po`
- `addons/base_setup/i18n/fr_CA.po`
- `addons/base_setup/i18n/gl.po`
- `addons/base_setup/i18n/gu.po`
- `addons/base_setup/i18n/he.po`
- `addons/base_setup/i18n/hi.po`
- `addons/base_setup/i18n/hr.po`
- `addons/base_setup/i18n/hu.po`
- `addons/base_setup/i18n/hy.po`
- `addons/base_setup/i18n/id.po`
- `addons/base_setup/i18n/is.po`
- `addons/base_setup/i18n/it.po`
- `addons/base_setup/i18n/ja.po`
- `addons/base_setup/i18n/ka.po`
- `addons/base_setup/i18n/kab.po`
- `addons/base_setup/i18n/km.po`
- `addons/base_setup/i18n/ko.po`
- `addons/base_setup/i18n/ku.po`
- `addons/base_setup/i18n/lo.po`
- `addons/base_setup/i18n/lt.po`
- `addons/base_setup/i18n/lv.po`
- `addons/base_setup/i18n/mk.po`
- `addons/base_setup/i18n/mn.po`
- `addons/base_setup/i18n/my.po`
- `addons/base_setup/i18n/nb.po`
- `addons/base_setup/i18n/nl.po`
- `addons/base_setup/i18n/pl.po`
- `addons/base_setup/i18n/pt.po`
- `addons/base_setup/i18n/pt_BR.po`
- `addons/base_setup/i18n/ro.po`
- `addons/base_setup/i18n/ru.po`
- `addons/base_setup/i18n/sk.po`
- `addons/base_setup/i18n/sl.po`
- `addons/base_setup/i18n/sq.po`
- `addons/base_setup/i18n/sr@latin.po`
- `addons/base_setup/i18n/sv.po`
- `addons/base_setup/i18n/th.po`
- `addons/base_setup/i18n/tr.po`
- `addons/base_setup/i18n/uk.po`
- `addons/base_setup/i18n/uz.po`
- `addons/base_setup/i18n/vi.po`
- `addons/base_setup/i18n/zh_CN.po`
- `addons/base_setup/i18n/zh_TW.po`
- `addons/base_setup/models/__init__.py`
- `addons/base_setup/models/ir_http.py`
- `addons/base_setup/models/kpi_provider.py`
- `addons/base_setup/models/res_config_settings.py`
- `addons/base_setup/models/res_users.py`
- `addons/base_setup/static/src/img/logo_apple_store.png`
- `addons/base_setup/static/src/img/logo_google_play.png`
- `addons/base_setup/static/src/views/module_views.js`
- `addons/base_setup/static/src/views/module_views.xml`
- `addons/base_setup/tests/__init__.py`
- `addons/base_setup/tests/test_default_group.py`
- `addons/base_setup/tests/test_kpi_controller.py`
- `addons/base_setup/tests/test_res_config.py`
- `addons/base_setup/tests/test_res_config_doc_links.py`
- `addons/base_setup/views/res_config_settings_views.xml`
- `addons/base_setup/views/res_partner_views.xml`
