# Module: partner_autocomplete

- **Module ID:** MOD-390
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/partner_autocomplete`
- **Manifest:** `addons/partner_autocomplete/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Auto-complete partner companies' data

**Manifest description:**

Auto-complete partner companies' data

**Scope evidence:** The module contains 82 files, including 12 Python, 5 XML, and 8 JavaScript/TypeScript files. The manifest declares dependencies: `iap_mail`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 8
- Security files: 0
- Test files: 4
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 44 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/partner_autocomplete/models/res_partner.py:14`, `addons/partner_autocomplete/models/iap_autocomplete_api.py:13`, `addons/partner_autocomplete/models/res_config_settings.py:7`, `addons/partner_autocomplete/models/ir_http.py:7`, `addons/partner_autocomplete/models/res_company.py:12`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 8 JavaScript/TypeScript files; static XML analysis found 5 record/template/menu identifiers.
- **Evidence:** `addons/partner_autocomplete/data/iap_service_data.xml:4`, `addons/partner_autocomplete/views/res_config_settings_views.xml:3`, `addons/partner_autocomplete/views/res_company_views.xml:3`, `addons/partner_autocomplete/views/res_partner_views.xml:3`, `addons/partner_autocomplete/views/res_partner_views.xml:14`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/partner_autocomplete/views/res_partner_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/partner_autocomplete/tests/common.py`, `addons/partner_autocomplete/tests/test_autocomplete_address_extended.py`, `addons/partner_autocomplete/tests/test_res_company.py`, `addons/partner_autocomplete/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `iap_service_partner_autocomplete`, `res_config_settings_view_form`, `view_company_form_inherit_partner_autocomplete`, `view_partner_form_inherit_partner_autocomplete`, `model_res_partner_enrich`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/partner_autocomplete/views/res_config_settings_views.xml:5`, `addons/partner_autocomplete/views/res_config_settings_views.xml:7`, `addons/partner_autocomplete/views/res_company_views.xml:5`, `addons/partner_autocomplete/views/res_company_views.xml:7`, `addons/partner_autocomplete/views/res_partner_views.xml:5`, `addons/partner_autocomplete/views/res_partner_views.xml:7`
- Browser assets: 8; representative files: `addons/partner_autocomplete/static/lib/jsvat.js`, `addons/partner_autocomplete/static/tests/partner_autocomplete.test.js`, `addons/partner_autocomplete/static/src/js/partner_autocomplete_additional_identifiers_list.js`, `addons/partner_autocomplete/static/src/js/partner_autocomplete_core.js`, `addons/partner_autocomplete/static/src/js/partner_autocomplete_many2one.js`, `addons/partner_autocomplete/static/src/js/partner_autocomplete_fieldchar.js`, `addons/partner_autocomplete/static/src/js/web_company_autocomplete.js`, `addons/partner_autocomplete/static/src/js/partner_autocomplete_component.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/partner_autocomplete/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/partner_autocomplete/views/res_partner_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `res.partner` (addons/partner_autocomplete/models/res_partner.py:14); `iap.autocomplete.api` (addons/partner_autocomplete/models/iap_autocomplete_api.py:13); inherits `res.config.settings` (addons/partner_autocomplete/models/res_config_settings.py:7); inherits `ir.http` (addons/partner_autocomplete/models/ir_http.py:7); inherits `res.company` (addons/partner_autocomplete/models/res_company.py:12)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `iap_mail`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/partner_autocomplete/__init__.py`
- `addons/partner_autocomplete/__manifest__.py`
- `addons/partner_autocomplete/data/iap_service_data.xml`
- `addons/partner_autocomplete/i18n/af.po`
- `addons/partner_autocomplete/i18n/ar.po`
- `addons/partner_autocomplete/i18n/az.po`
- `addons/partner_autocomplete/i18n/bg.po`
- `addons/partner_autocomplete/i18n/bs.po`
- `addons/partner_autocomplete/i18n/ca.po`
- `addons/partner_autocomplete/i18n/cs.po`
- `addons/partner_autocomplete/i18n/da.po`
- `addons/partner_autocomplete/i18n/de.po`
- `addons/partner_autocomplete/i18n/el.po`
- `addons/partner_autocomplete/i18n/es.po`
- `addons/partner_autocomplete/i18n/es_419.po`
- `addons/partner_autocomplete/i18n/et.po`
- `addons/partner_autocomplete/i18n/fa.po`
- `addons/partner_autocomplete/i18n/fi.po`
- `addons/partner_autocomplete/i18n/fr.po`
- `addons/partner_autocomplete/i18n/gu.po`
- `addons/partner_autocomplete/i18n/he.po`
- `addons/partner_autocomplete/i18n/hi.po`
- `addons/partner_autocomplete/i18n/hr.po`
- `addons/partner_autocomplete/i18n/hu.po`
- `addons/partner_autocomplete/i18n/id.po`
- `addons/partner_autocomplete/i18n/is.po`
- `addons/partner_autocomplete/i18n/it.po`
- `addons/partner_autocomplete/i18n/ja.po`
- `addons/partner_autocomplete/i18n/kab.po`
- `addons/partner_autocomplete/i18n/km.po`
- `addons/partner_autocomplete/i18n/ko.po`
- `addons/partner_autocomplete/i18n/ku.po`
- `addons/partner_autocomplete/i18n/lo.po`
- `addons/partner_autocomplete/i18n/lt.po`
- `addons/partner_autocomplete/i18n/lv.po`
- `addons/partner_autocomplete/i18n/mn.po`
- `addons/partner_autocomplete/i18n/my.po`
- `addons/partner_autocomplete/i18n/nb.po`
- `addons/partner_autocomplete/i18n/nl.po`
- `addons/partner_autocomplete/i18n/partner_autocomplete.pot`
- `addons/partner_autocomplete/i18n/pl.po`
- `addons/partner_autocomplete/i18n/pt.po`
- `addons/partner_autocomplete/i18n/pt_BR.po`
- `addons/partner_autocomplete/i18n/ro.po`
- `addons/partner_autocomplete/i18n/ru.po`
- `addons/partner_autocomplete/i18n/sk.po`
- `addons/partner_autocomplete/i18n/sl.po`
- `addons/partner_autocomplete/i18n/sr@latin.po`
- `addons/partner_autocomplete/i18n/sv.po`
- `addons/partner_autocomplete/i18n/th.po`
- `addons/partner_autocomplete/i18n/tr.po`
- `addons/partner_autocomplete/i18n/uk.po`
- `addons/partner_autocomplete/i18n/uz.po`
- `addons/partner_autocomplete/i18n/vi.po`
- `addons/partner_autocomplete/i18n/zh_CN.po`
- `addons/partner_autocomplete/i18n/zh_TW.po`
- `addons/partner_autocomplete/models/__init__.py`
- `addons/partner_autocomplete/models/iap_autocomplete_api.py`
- `addons/partner_autocomplete/models/ir_http.py`
- `addons/partner_autocomplete/models/res_company.py`
- `addons/partner_autocomplete/models/res_config_settings.py`
- `addons/partner_autocomplete/models/res_partner.py`
- `addons/partner_autocomplete/static/description/icon.png`
- `addons/partner_autocomplete/static/description/icon.svg`
- `addons/partner_autocomplete/static/description/icon_hi.png`
- `addons/partner_autocomplete/static/lib/jsvat.js`
- `addons/partner_autocomplete/static/src/js/partner_autocomplete_additional_identifiers_list.js`
- `addons/partner_autocomplete/static/src/js/partner_autocomplete_component.js`
- `addons/partner_autocomplete/static/src/js/partner_autocomplete_core.js`
- `addons/partner_autocomplete/static/src/js/partner_autocomplete_fieldchar.js`
- `addons/partner_autocomplete/static/src/js/partner_autocomplete_many2one.js`
- `addons/partner_autocomplete/static/src/js/web_company_autocomplete.js`
- `addons/partner_autocomplete/static/src/scss/partner_autocomplete.scss`
- `addons/partner_autocomplete/static/src/xml/partner_autocomplete.xml`
- `addons/partner_autocomplete/static/tests/partner_autocomplete.test.js`
- `addons/partner_autocomplete/tests/__init__.py`
- `addons/partner_autocomplete/tests/common.py`
- `addons/partner_autocomplete/tests/test_autocomplete_address_extended.py`
- `addons/partner_autocomplete/tests/test_res_company.py`
- `addons/partner_autocomplete/views/res_company_views.xml`
- `addons/partner_autocomplete/views/res_config_settings_views.xml`
- `addons/partner_autocomplete/views/res_partner_views.xml`
