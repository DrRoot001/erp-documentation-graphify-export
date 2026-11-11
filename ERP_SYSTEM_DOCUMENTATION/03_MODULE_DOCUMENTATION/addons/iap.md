# Module: iap

- **Module ID:** MOD-108
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/iap`
- **Manifest:** `addons/iap/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Basic models and helpers to support In-App Purchase.

**Manifest description:**

This module provides standard tools (account model, context manager and helpers)
to support In-App Purchase inside Odoo.

**Scope evidence:** The module contains 86 files, including 13 Python, 5 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `web`, `base_setup`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 1
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/iap/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 30 methods, 1 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/iap/models/iap_account.py:25`, `addons/iap/models/iap_service_pack.py:4`, `addons/iap/models/res_config_settings.py:4`, `addons/iap/models/iap_service.py:6`, `addons/iap/models/iap_enrich_api.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 1 JavaScript/TypeScript files; static XML analysis found 10 record/template/menu identifiers.
- **Evidence:** `addons/iap/data/services.xml:5`, `addons/iap/views/res_config_settings.xml:3`, `addons/iap/views/iap_views.xml:5`, `addons/iap/views/iap_views.xml:52`, `addons/iap/views/iap_views.xml:70`, `addons/iap/views/iap_views.xml:83`, `addons/iap/views/iap_views.xml:91`, `addons/iap/views/iap_views.xml:97`, `addons/iap/views/res_users_views.xml:4`, `addons/iap/static/src/action_buttons_widget/action_buttons_widget.xml:2`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/iap/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/iap/tests/test_iap.py`, `addons/iap/tests/common.py`, `addons/iap/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `iap_service_reveal`, `res_config_settings_view_form`, `iap_account_view_form`, `iap_account_view_tree`, `iap_service_pack_view_tree`, `iap_account_action`, `IAP`, `In-App Purchase Accounts`, `view_iap_users_tree`, `template`
- Menus: 2; representative evidence: `addons/iap/views/iap_views.xml:91`, `addons/iap/views/iap_views.xml:97`
- Templates: 1; representative evidence: `addons/iap/static/src/action_buttons_widget/action_buttons_widget.xml:2`
- View/action field declarations: 12; representative evidence: `addons/iap/views/res_config_settings.xml:5`, `addons/iap/views/res_config_settings.xml:7`, `addons/iap/views/iap_views.xml:7`, `addons/iap/views/iap_views.xml:8`, `addons/iap/views/iap_views.xml:54`, `addons/iap/views/iap_views.xml:55`, `addons/iap/views/iap_views.xml:72`, `addons/iap/views/iap_views.xml:73`, `addons/iap/views/iap_views.xml:85`, `addons/iap/views/iap_views.xml:87`, `addons/iap/views/res_users_views.xml:6`, `addons/iap/views/res_users_views.xml:7`
- Browser assets: 1; representative files: `addons/iap/static/src/action_buttons_widget/action_buttons_widget.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/iap/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: `iap.account` (addons/iap/models/iap_account.py:25); `iap.service.pack` (addons/iap/models/iap_service_pack.py:4); inherits `res.config.settings` (addons/iap/models/res_config_settings.py:4); `iap.service` (addons/iap/models/iap_service.py:6); `iap.enrich.api` (addons/iap/models/iap_enrich_api.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `web`, `base_setup`
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

- `addons/iap/__init__.py`
- `addons/iap/__manifest__.py`
- `addons/iap/data/neutralize.sql`
- `addons/iap/data/services.xml`
- `addons/iap/i18n/af.po`
- `addons/iap/i18n/am.po`
- `addons/iap/i18n/ar.po`
- `addons/iap/i18n/az.po`
- `addons/iap/i18n/bg.po`
- `addons/iap/i18n/bs.po`
- `addons/iap/i18n/ca.po`
- `addons/iap/i18n/cs.po`
- `addons/iap/i18n/da.po`
- `addons/iap/i18n/de.po`
- `addons/iap/i18n/el.po`
- `addons/iap/i18n/es.po`
- `addons/iap/i18n/es_419.po`
- `addons/iap/i18n/es_CL.po`
- `addons/iap/i18n/et.po`
- `addons/iap/i18n/eu.po`
- `addons/iap/i18n/fa.po`
- `addons/iap/i18n/fi.po`
- `addons/iap/i18n/fo.po`
- `addons/iap/i18n/fr.po`
- `addons/iap/i18n/fr_CA.po`
- `addons/iap/i18n/gl.po`
- `addons/iap/i18n/gu.po`
- `addons/iap/i18n/he.po`
- `addons/iap/i18n/hi.po`
- `addons/iap/i18n/hr.po`
- `addons/iap/i18n/hu.po`
- `addons/iap/i18n/iap.pot`
- `addons/iap/i18n/id.po`
- `addons/iap/i18n/is.po`
- `addons/iap/i18n/it.po`
- `addons/iap/i18n/ja.po`
- `addons/iap/i18n/ka.po`
- `addons/iap/i18n/kab.po`
- `addons/iap/i18n/km.po`
- `addons/iap/i18n/ko.po`
- `addons/iap/i18n/ku.po`
- `addons/iap/i18n/lo.po`
- `addons/iap/i18n/lt.po`
- `addons/iap/i18n/lv.po`
- `addons/iap/i18n/mk.po`
- `addons/iap/i18n/mn.po`
- `addons/iap/i18n/my.po`
- `addons/iap/i18n/nb.po`
- `addons/iap/i18n/nl.po`
- `addons/iap/i18n/pl.po`
- `addons/iap/i18n/pt.po`
- `addons/iap/i18n/pt_BR.po`
- `addons/iap/i18n/ro.po`
- `addons/iap/i18n/ru.po`
- `addons/iap/i18n/sk.po`
- `addons/iap/i18n/sl.po`
- `addons/iap/i18n/sq.po`
- `addons/iap/i18n/sr@latin.po`
- `addons/iap/i18n/sv.po`
- `addons/iap/i18n/th.po`
- `addons/iap/i18n/tr.po`
- `addons/iap/i18n/uk.po`
- `addons/iap/i18n/uz.po`
- `addons/iap/i18n/vi.po`
- `addons/iap/i18n/zh_CN.po`
- `addons/iap/i18n/zh_TW.po`
- `addons/iap/models/__init__.py`
- `addons/iap/models/iap_account.py`
- `addons/iap/models/iap_enrich_api.py`
- `addons/iap/models/iap_service.py`
- `addons/iap/models/iap_service_pack.py`
- `addons/iap/models/res_config_settings.py`
- `addons/iap/security/ir.access.csv`
- `addons/iap/static/description/icon.png`
- `addons/iap/static/description/icon.svg`
- `addons/iap/static/description/icon_hi.png`
- `addons/iap/static/src/action_buttons_widget/action_buttons_widget.js`
- `addons/iap/static/src/action_buttons_widget/action_buttons_widget.xml`
- `addons/iap/tests/__init__.py`
- `addons/iap/tests/common.py`
- `addons/iap/tests/test_iap.py`
- `addons/iap/tools/__init__.py`
- `addons/iap/tools/iap_tools.py`
- `addons/iap/views/iap_views.xml`
- `addons/iap/views/res_config_settings.xml`
- `addons/iap/views/res_users_views.xml`
