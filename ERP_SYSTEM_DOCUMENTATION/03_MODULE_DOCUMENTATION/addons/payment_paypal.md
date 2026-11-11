# Module: payment_paypal

- **Module ID:** MOD-408
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/payment_paypal`
- **Manifest:** `addons/payment_paypal/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Payment Providers`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** An American payment provider for online payments all over the world.

**Manifest description:**



**Scope evidence:** The module contains 79 files, including 14 Python, 6 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `payment`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 3
- XML/data/view/template files: 6
- Browser asset files: 3
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 64 methods, 1 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/payment_paypal/models/payment_token.py:6`, `addons/payment_paypal/models/payment_transaction.py:17`, `addons/payment_paypal/models/payment_provider.py:16`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 6 route declarations.
- **Evidence:** `addons/payment_paypal/controllers/onboarding.py:16`, `addons/payment_paypal/controllers/onboarding.py:59`, `addons/payment_paypal/controllers/main.py:22`, `addons/payment_paypal/controllers/main.py:43`, `addons/payment_paypal/controllers/main.py:56`, `addons/payment_paypal/controllers/main.py:163`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 3 JavaScript/TypeScript files; static XML analysis found 24 record/template/menu identifiers.
- **Evidence:** `addons/payment_paypal/data/payment_provider_data.xml:4`, `addons/payment_paypal/data/payment_method_data.xml:6`, `addons/payment_paypal/data/payment_method_data.xml:15`, `addons/payment_paypal/data/payment_method_data.xml:24`, `addons/payment_paypal/data/payment_method_data.xml:33`, `addons/payment_paypal/data/payment_method_data.xml:111`, `addons/payment_paypal/data/payment_method_data.xml:120`, `addons/payment_paypal/data/payment_method_data.xml:129`, `addons/payment_paypal/data/payment_method_data.xml:138`, `addons/payment_paypal/data/payment_method_data.xml:147`, `addons/payment_paypal/data/payment_method_data.xml:177`, `addons/payment_paypal/data/payment_method_data.xml:189`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/payment_paypal/tests/test_paypal.py`, `addons/payment_paypal/tests/common.py`, `addons/payment_paypal/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `payment.payment_provider_paypal`, `payment_method_paypal`, `payment_method_bancontact`, `payment_method_blik`, `payment_method_card`, `payment_method_eps`, `payment_method_ideal`, `payment_method_multibanco`, `payment_method_mybank`, `payment_method_paypal_paylater`, `payment_method_p24`, `payment_method_trustly`, `payment_method_venmo`, `payment_method_amex`, `payment_method_diners`, `payment_method_jcb`, `payment_method_maestro`, `payment_method_mastercard`, `payment_method_visa`, `inline_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 3; representative evidence: `addons/payment_paypal/views/payment_paypal_templates.xml:4`, `addons/payment_paypal/views/payment_form_templates.xml:4`, `addons/payment_paypal/views/payment_form_templates.xml:12`
- View/action field declarations: 4; representative evidence: `addons/payment_paypal/views/payment_transaction_views.xml:6`, `addons/payment_paypal/views/payment_transaction_views.xml:8`, `addons/payment_paypal/views/payment_provider_views.xml:6`, `addons/payment_paypal/views/payment_provider_views.xml:8`
- Browser assets: 3; representative files: `addons/payment_paypal/static/src/onboarding/paypal_onboarding.js`, `addons/payment_paypal/static/src/interactions/payment_form.js`, `addons/payment_paypal/static/src/interactions/payment_button.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/payment_paypal/__manifest__.py`
- **HTTP entry points:** `addons/payment_paypal/controllers/onboarding.py:16`, `addons/payment_paypal/controllers/onboarding.py:59`, `addons/payment_paypal/controllers/main.py:22`, `addons/payment_paypal/controllers/main.py:43`, `addons/payment_paypal/controllers/main.py:56`, `addons/payment_paypal/controllers/main.py:163`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `payment.token` (addons/payment_paypal/models/payment_token.py:6); inherits `payment.transaction` (addons/payment_paypal/models/payment_transaction.py:17); inherits `payment.provider` (addons/payment_paypal/models/payment_provider.py:16)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 6
- Route evidence: `addons/payment_paypal/controllers/onboarding.py:16`, `addons/payment_paypal/controllers/onboarding.py:59`, `addons/payment_paypal/controllers/main.py:22`, `addons/payment_paypal/controllers/main.py:43`, `addons/payment_paypal/controllers/main.py:56`, `addons/payment_paypal/controllers/main.py:163`
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

- `addons/payment_paypal/README.md`
- `addons/payment_paypal/__init__.py`
- `addons/payment_paypal/__manifest__.py`
- `addons/payment_paypal/const.py`
- `addons/payment_paypal/controllers/__init__.py`
- `addons/payment_paypal/controllers/main.py`
- `addons/payment_paypal/controllers/onboarding.py`
- `addons/payment_paypal/data/neutralize.sql`
- `addons/payment_paypal/data/payment_method_data.xml`
- `addons/payment_paypal/data/payment_provider_data.xml`
- `addons/payment_paypal/i18n/ar.po`
- `addons/payment_paypal/i18n/az.po`
- `addons/payment_paypal/i18n/bg.po`
- `addons/payment_paypal/i18n/bs.po`
- `addons/payment_paypal/i18n/ca.po`
- `addons/payment_paypal/i18n/cs.po`
- `addons/payment_paypal/i18n/da.po`
- `addons/payment_paypal/i18n/de.po`
- `addons/payment_paypal/i18n/el.po`
- `addons/payment_paypal/i18n/es.po`
- `addons/payment_paypal/i18n/es_419.po`
- `addons/payment_paypal/i18n/et.po`
- `addons/payment_paypal/i18n/fa.po`
- `addons/payment_paypal/i18n/fi.po`
- `addons/payment_paypal/i18n/fr.po`
- `addons/payment_paypal/i18n/he.po`
- `addons/payment_paypal/i18n/hi.po`
- `addons/payment_paypal/i18n/hr.po`
- `addons/payment_paypal/i18n/hu.po`
- `addons/payment_paypal/i18n/id.po`
- `addons/payment_paypal/i18n/it.po`
- `addons/payment_paypal/i18n/ja.po`
- `addons/payment_paypal/i18n/kab.po`
- `addons/payment_paypal/i18n/ko.po`
- `addons/payment_paypal/i18n/ku.po`
- `addons/payment_paypal/i18n/lo.po`
- `addons/payment_paypal/i18n/lt.po`
- `addons/payment_paypal/i18n/lv.po`
- `addons/payment_paypal/i18n/mn.po`
- `addons/payment_paypal/i18n/my.po`
- `addons/payment_paypal/i18n/nb.po`
- `addons/payment_paypal/i18n/nl.po`
- `addons/payment_paypal/i18n/payment_paypal.pot`
- `addons/payment_paypal/i18n/pl.po`
- `addons/payment_paypal/i18n/pt.po`
- `addons/payment_paypal/i18n/pt_BR.po`
- `addons/payment_paypal/i18n/ro.po`
- `addons/payment_paypal/i18n/ru.po`
- `addons/payment_paypal/i18n/sk.po`
- `addons/payment_paypal/i18n/sl.po`
- `addons/payment_paypal/i18n/sr@latin.po`
- `addons/payment_paypal/i18n/sv.po`
- `addons/payment_paypal/i18n/th.po`
- `addons/payment_paypal/i18n/tr.po`
- `addons/payment_paypal/i18n/uk.po`
- `addons/payment_paypal/i18n/uz.po`
- `addons/payment_paypal/i18n/vi.po`
- `addons/payment_paypal/i18n/zh_CN.po`
- `addons/payment_paypal/i18n/zh_TW.po`
- `addons/payment_paypal/models/__init__.py`
- `addons/payment_paypal/models/payment_provider.py`
- `addons/payment_paypal/models/payment_token.py`
- `addons/payment_paypal/models/payment_transaction.py`
- `addons/payment_paypal/static/description/icon.png`
- `addons/payment_paypal/static/description/icon.svg`
- `addons/payment_paypal/static/description/icon_hi.png`
- `addons/payment_paypal/static/src/interactions/payment_button.js`
- `addons/payment_paypal/static/src/interactions/payment_form.js`
- `addons/payment_paypal/static/src/onboarding/paypal_onboarding.js`
- `addons/payment_paypal/static/src/onboarding/paypal_onboarding.scss`
- `addons/payment_paypal/static/src/scss/payment_paypal.scss`
- `addons/payment_paypal/tests/__init__.py`
- `addons/payment_paypal/tests/common.py`
- `addons/payment_paypal/tests/test_paypal.py`
- `addons/payment_paypal/utils.py`
- `addons/payment_paypal/views/payment_form_templates.xml`
- `addons/payment_paypal/views/payment_paypal_templates.xml`
- `addons/payment_paypal/views/payment_provider_views.xml`
- `addons/payment_paypal/views/payment_transaction_views.xml`
