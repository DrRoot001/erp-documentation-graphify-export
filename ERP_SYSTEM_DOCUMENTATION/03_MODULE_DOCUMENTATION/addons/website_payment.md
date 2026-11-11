# Module: website_payment

- **Module ID:** MOD-631
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_payment`
- **Manifest:** `addons/website_payment/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Payment integration with website

**Manifest description:**

This is a bridge module that adds multi-website support for payment providers.

**Scope evidence:** The module contains 85 files, including 10 Python, 7 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `website`, `account_payment`, `portal`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 3
- XML/data/view/template files: 7
- Browser asset files: 3
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 11 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/website_payment/models/res_config_settings.py:7`, `addons/website_payment/models/payment_provider.py:12`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 3 route declarations.
- **Evidence:** `addons/website_payment/controllers/portal.py:11`, `addons/website_payment/controllers/payment.py:10`, `addons/website_payment/controllers/payment.py:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 3 JavaScript/TypeScript files; static XML analysis found 4 record/template/menu identifiers.
- **Evidence:** `addons/website_payment/views/res_config_settings_views.xml:3`, `addons/website_payment/views/payment_provider.xml:5`, `addons/website_payment/views/snippets/snippets.xml:4`, `addons/website_payment/views/snippets/s_supported_payment_methods.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/website_payment/tests/test_website_payment_technical_page.py`, `addons/website_payment/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `res_config_settings_view_form`, `payment_provider_form`, `Snippet Supported Payment Methods`, `Supported Payment Methods`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/website_payment/views/snippets/snippets.xml:4`, `addons/website_payment/views/snippets/s_supported_payment_methods.xml:4`
- View/action field declarations: 4; representative evidence: `addons/website_payment/views/res_config_settings_views.xml:5`, `addons/website_payment/views/res_config_settings_views.xml:8`, `addons/website_payment/views/payment_provider.xml:7`, `addons/website_payment/views/payment_provider.xml:9`
- Browser assets: 3; representative files: `addons/website_payment/static/src/website_builder/supported_payment_methods_option_plugin.js`, `addons/website_payment/static/src/snippets/s_supported_payment_methods/supported_payment_methods.js`, `addons/website_payment/static/src/snippets/s_supported_payment_methods/supported_payment_methods.edit.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_payment/__manifest__.py`
- **HTTP entry points:** `addons/website_payment/controllers/portal.py:11`, `addons/website_payment/controllers/payment.py:10`, `addons/website_payment/controllers/payment.py:15`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `res.config.settings` (addons/website_payment/models/res_config_settings.py:7); inherits `payment.provider` (addons/website_payment/models/payment_provider.py:12)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 3
- Route evidence: `addons/website_payment/controllers/portal.py:11`, `addons/website_payment/controllers/payment.py:10`, `addons/website_payment/controllers/payment.py:15`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website`, `account_payment`, `portal`
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

- `addons/website_payment/__init__.py`
- `addons/website_payment/__manifest__.py`
- `addons/website_payment/controllers/__init__.py`
- `addons/website_payment/controllers/payment.py`
- `addons/website_payment/controllers/portal.py`
- `addons/website_payment/i18n/af.po`
- `addons/website_payment/i18n/ar.po`
- `addons/website_payment/i18n/az.po`
- `addons/website_payment/i18n/bg.po`
- `addons/website_payment/i18n/bs.po`
- `addons/website_payment/i18n/ca.po`
- `addons/website_payment/i18n/cs.po`
- `addons/website_payment/i18n/da.po`
- `addons/website_payment/i18n/de.po`
- `addons/website_payment/i18n/el.po`
- `addons/website_payment/i18n/es.po`
- `addons/website_payment/i18n/es_419.po`
- `addons/website_payment/i18n/es_CL.po`
- `addons/website_payment/i18n/et.po`
- `addons/website_payment/i18n/eu.po`
- `addons/website_payment/i18n/fa.po`
- `addons/website_payment/i18n/fi.po`
- `addons/website_payment/i18n/fr.po`
- `addons/website_payment/i18n/fr_CA.po`
- `addons/website_payment/i18n/gl.po`
- `addons/website_payment/i18n/gu.po`
- `addons/website_payment/i18n/he.po`
- `addons/website_payment/i18n/hi.po`
- `addons/website_payment/i18n/hr.po`
- `addons/website_payment/i18n/hu.po`
- `addons/website_payment/i18n/id.po`
- `addons/website_payment/i18n/is.po`
- `addons/website_payment/i18n/it.po`
- `addons/website_payment/i18n/ja.po`
- `addons/website_payment/i18n/ka.po`
- `addons/website_payment/i18n/kab.po`
- `addons/website_payment/i18n/kk.po`
- `addons/website_payment/i18n/km.po`
- `addons/website_payment/i18n/ko.po`
- `addons/website_payment/i18n/ku.po`
- `addons/website_payment/i18n/lo.po`
- `addons/website_payment/i18n/lt.po`
- `addons/website_payment/i18n/lv.po`
- `addons/website_payment/i18n/mk.po`
- `addons/website_payment/i18n/mn.po`
- `addons/website_payment/i18n/my.po`
- `addons/website_payment/i18n/nb.po`
- `addons/website_payment/i18n/nl.po`
- `addons/website_payment/i18n/pl.po`
- `addons/website_payment/i18n/pt.po`
- `addons/website_payment/i18n/pt_BR.po`
- `addons/website_payment/i18n/ro.po`
- `addons/website_payment/i18n/ru.po`
- `addons/website_payment/i18n/sk.po`
- `addons/website_payment/i18n/sl.po`
- `addons/website_payment/i18n/sq.po`
- `addons/website_payment/i18n/sr@latin.po`
- `addons/website_payment/i18n/sv.po`
- `addons/website_payment/i18n/th.po`
- `addons/website_payment/i18n/tr.po`
- `addons/website_payment/i18n/uk.po`
- `addons/website_payment/i18n/uz.po`
- `addons/website_payment/i18n/vi.po`
- `addons/website_payment/i18n/website_payment.pot`
- `addons/website_payment/i18n/zh_CN.po`
- `addons/website_payment/i18n/zh_TW.po`
- `addons/website_payment/models/__init__.py`
- `addons/website_payment/models/payment_provider.py`
- `addons/website_payment/models/res_config_settings.py`
- `addons/website_payment/static/description/icon.png`
- `addons/website_payment/static/description/icon.svg`
- `addons/website_payment/static/description/icon_hi.png`
- `addons/website_payment/static/img/s_supported_payment_methods.svg`
- `addons/website_payment/static/src/snippets/s_supported_payment_methods/000.edit.xml`
- `addons/website_payment/static/src/snippets/s_supported_payment_methods/000.xml`
- `addons/website_payment/static/src/snippets/s_supported_payment_methods/supported_payment_methods.edit.js`
- `addons/website_payment/static/src/snippets/s_supported_payment_methods/supported_payment_methods.js`
- `addons/website_payment/static/src/website_builder/supported_payment_methods_option.xml`
- `addons/website_payment/static/src/website_builder/supported_payment_methods_option_plugin.js`
- `addons/website_payment/tests/__init__.py`
- `addons/website_payment/tests/test_website_payment_technical_page.py`
- `addons/website_payment/views/payment_provider.xml`
- `addons/website_payment/views/res_config_settings_views.xml`
- `addons/website_payment/views/snippets/s_supported_payment_methods.xml`
- `addons/website_payment/views/snippets/snippets.xml`
