# Module: payment_mercado_pago

- **Module ID:** MOD-404
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/payment_mercado_pago`
- **Manifest:** `addons/payment_mercado_pago/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Payment Providers`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** A payment provider covering several countries in Latin America.

**Manifest description:**



**Scope evidence:** The module contains 75 files, including 15 Python, 5 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `payment`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 3
- XML/data/view/template files: 5
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

- **Description:** 3 model declarations, 46 methods, 3 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/payment_mercado_pago/models/payment_token.py:6`, `addons/payment_mercado_pago/models/payment_transaction.py:18`, `addons/payment_mercado_pago/models/payment_provider.py:21`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 4 route declarations.
- **Evidence:** `addons/payment_mercado_pago/controllers/onboarding.py:19`, `addons/payment_mercado_pago/controllers/payment.py:19`, `addons/payment_mercado_pago/controllers/payment.py:55`, `addons/payment_mercado_pago/controllers/payment.py:70`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 1 JavaScript/TypeScript files; static XML analysis found 29 record/template/menu identifiers.
- **Evidence:** `addons/payment_mercado_pago/data/payment_provider_data.xml:4`, `addons/payment_mercado_pago/data/payment_method_data.xml:8`, `addons/payment_mercado_pago/data/payment_method_data.xml:16`, `addons/payment_mercado_pago/data/payment_method_data.xml:25`, `addons/payment_mercado_pago/data/payment_method_data.xml:35`, `addons/payment_mercado_pago/data/payment_method_data.xml:43`, `addons/payment_mercado_pago/data/payment_method_data.xml:51`, `addons/payment_mercado_pago/data/payment_method_data.xml:59`, `addons/payment_mercado_pago/data/payment_method_data.xml:67`, `addons/payment_mercado_pago/data/payment_method_data.xml:77`, `addons/payment_mercado_pago/data/payment_method_data.xml:85`, `addons/payment_mercado_pago/data/payment_method_data.xml:93`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/payment_mercado_pago/tests/test_processing_flows.py`, `addons/payment_mercado_pago/tests/common.py`, `addons/payment_mercado_pago/tests/test_payment_provider.py`, `addons/payment_mercado_pago/tests/test_payment_transaction.py`, `addons/payment_mercado_pago/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `payment.payment_provider_mercado_pago`, `payment_method_bank_transfer`, `payment_method_card`, `payment_method_mercado_pago_wallet`, `payment_method_amex`, `payment_method_argencard`, `payment_method_cabal`, `payment_method_caixa`, `payment_method_cencosud`, `payment_method_codensa`, `payment_method_cordial`, `payment_method_cordobesa`, `payment_method_elo`, `payment_method_hipercard`, `payment_method_lider`, `payment_method_magna`, `payment_method_mastercard`, `payment_method_mercado_livre`, `payment_method_naranja`, `payment_method_nativa`
- Menus: 0; representative evidence: Not found in module
- Templates: 3; representative evidence: `addons/payment_mercado_pago/views/payment_form_templates.xml:4`, `addons/payment_mercado_pago/views/payment_mercado_pago_templates.xml:5`, `addons/payment_mercado_pago/views/payment_mercado_pago_templates.xml:13`
- View/action field declarations: 2; representative evidence: `addons/payment_mercado_pago/views/payment_provider_views.xml:6`, `addons/payment_mercado_pago/views/payment_provider_views.xml:8`
- Browser assets: 1; representative files: `addons/payment_mercado_pago/static/src/interactions/payment_form.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/payment_mercado_pago/__manifest__.py`
- **HTTP entry points:** `addons/payment_mercado_pago/controllers/onboarding.py:19`, `addons/payment_mercado_pago/controllers/payment.py:19`, `addons/payment_mercado_pago/controllers/payment.py:55`, `addons/payment_mercado_pago/controllers/payment.py:70`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `payment.token` (addons/payment_mercado_pago/models/payment_token.py:6); inherits `payment.transaction` (addons/payment_mercado_pago/models/payment_transaction.py:18); inherits `payment.provider` (addons/payment_mercado_pago/models/payment_provider.py:21)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 4
- Route evidence: `addons/payment_mercado_pago/controllers/onboarding.py:19`, `addons/payment_mercado_pago/controllers/payment.py:19`, `addons/payment_mercado_pago/controllers/payment.py:55`, `addons/payment_mercado_pago/controllers/payment.py:70`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `payment`
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

- `addons/payment_mercado_pago/README.md`
- `addons/payment_mercado_pago/__init__.py`
- `addons/payment_mercado_pago/__manifest__.py`
- `addons/payment_mercado_pago/const.py`
- `addons/payment_mercado_pago/controllers/__init__.py`
- `addons/payment_mercado_pago/controllers/onboarding.py`
- `addons/payment_mercado_pago/controllers/payment.py`
- `addons/payment_mercado_pago/data/neutralize.sql`
- `addons/payment_mercado_pago/data/payment_method_data.xml`
- `addons/payment_mercado_pago/data/payment_provider_data.xml`
- `addons/payment_mercado_pago/i18n/ar.po`
- `addons/payment_mercado_pago/i18n/az.po`
- `addons/payment_mercado_pago/i18n/bg.po`
- `addons/payment_mercado_pago/i18n/bs.po`
- `addons/payment_mercado_pago/i18n/ca.po`
- `addons/payment_mercado_pago/i18n/cs.po`
- `addons/payment_mercado_pago/i18n/da.po`
- `addons/payment_mercado_pago/i18n/de.po`
- `addons/payment_mercado_pago/i18n/el.po`
- `addons/payment_mercado_pago/i18n/es.po`
- `addons/payment_mercado_pago/i18n/es_419.po`
- `addons/payment_mercado_pago/i18n/et.po`
- `addons/payment_mercado_pago/i18n/fa.po`
- `addons/payment_mercado_pago/i18n/fi.po`
- `addons/payment_mercado_pago/i18n/fr.po`
- `addons/payment_mercado_pago/i18n/he.po`
- `addons/payment_mercado_pago/i18n/hi.po`
- `addons/payment_mercado_pago/i18n/hr.po`
- `addons/payment_mercado_pago/i18n/hu.po`
- `addons/payment_mercado_pago/i18n/id.po`
- `addons/payment_mercado_pago/i18n/it.po`
- `addons/payment_mercado_pago/i18n/ja.po`
- `addons/payment_mercado_pago/i18n/kab.po`
- `addons/payment_mercado_pago/i18n/ko.po`
- `addons/payment_mercado_pago/i18n/ku.po`
- `addons/payment_mercado_pago/i18n/lo.po`
- `addons/payment_mercado_pago/i18n/lt.po`
- `addons/payment_mercado_pago/i18n/lv.po`
- `addons/payment_mercado_pago/i18n/mn.po`
- `addons/payment_mercado_pago/i18n/my.po`
- `addons/payment_mercado_pago/i18n/nb.po`
- `addons/payment_mercado_pago/i18n/nl.po`
- `addons/payment_mercado_pago/i18n/payment_mercado_pago.pot`
- `addons/payment_mercado_pago/i18n/pl.po`
- `addons/payment_mercado_pago/i18n/pt.po`
- `addons/payment_mercado_pago/i18n/pt_BR.po`
- `addons/payment_mercado_pago/i18n/ro.po`
- `addons/payment_mercado_pago/i18n/ru.po`
- `addons/payment_mercado_pago/i18n/sk.po`
- `addons/payment_mercado_pago/i18n/sl.po`
- `addons/payment_mercado_pago/i18n/sr@latin.po`
- `addons/payment_mercado_pago/i18n/sv.po`
- `addons/payment_mercado_pago/i18n/th.po`
- `addons/payment_mercado_pago/i18n/tr.po`
- `addons/payment_mercado_pago/i18n/uk.po`
- `addons/payment_mercado_pago/i18n/uz.po`
- `addons/payment_mercado_pago/i18n/vi.po`
- `addons/payment_mercado_pago/i18n/zh_CN.po`
- `addons/payment_mercado_pago/i18n/zh_TW.po`
- `addons/payment_mercado_pago/models/__init__.py`
- `addons/payment_mercado_pago/models/payment_provider.py`
- `addons/payment_mercado_pago/models/payment_token.py`
- `addons/payment_mercado_pago/models/payment_transaction.py`
- `addons/payment_mercado_pago/static/description/icon.png`
- `addons/payment_mercado_pago/static/description/icon.svg`
- `addons/payment_mercado_pago/static/description/icon_hi.png`
- `addons/payment_mercado_pago/static/src/interactions/payment_form.js`
- `addons/payment_mercado_pago/tests/__init__.py`
- `addons/payment_mercado_pago/tests/common.py`
- `addons/payment_mercado_pago/tests/test_payment_provider.py`
- `addons/payment_mercado_pago/tests/test_payment_transaction.py`
- `addons/payment_mercado_pago/tests/test_processing_flows.py`
- `addons/payment_mercado_pago/views/payment_form_templates.xml`
- `addons/payment_mercado_pago/views/payment_mercado_pago_templates.xml`
- `addons/payment_mercado_pago/views/payment_provider_views.xml`
