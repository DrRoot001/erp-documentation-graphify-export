# Module: payment_stripe

- **Module ID:** MOD-412
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/payment_stripe`
- **Manifest:** `addons/payment_stripe/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Payment Providers`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** An Irish-American payment provider covering the US and many others.

**Manifest description:**



**Scope evidence:** The module contains 81 files, including 16 Python, 5 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `payment`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 3
- XML/data/view/template files: 5
- Browser asset files: 3
- Security files: 0
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 80 methods, 2 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/payment_stripe/models/payment_token.py:11`, `addons/payment_stripe/models/payment_transaction.py:18`, `addons/payment_stripe/models/payment_provider.py:21`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 6 route declarations.
- **Evidence:** `addons/payment_stripe/controllers/onboarding.py:11`, `addons/payment_stripe/controllers/onboarding.py:29`, `addons/payment_stripe/controllers/main.py:29`, `addons/payment_stripe/controllers/main.py:69`, `addons/payment_stripe/controllers/main.py:94`, `addons/payment_stripe/controllers/main.py:262`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 3 JavaScript/TypeScript files; static XML analysis found 55 record/template/menu identifiers.
- **Evidence:** `addons/payment_stripe/data/payment_provider_data.xml:4`, `addons/payment_stripe/data/payment_method_data.xml:8`, `addons/payment_stripe/data/payment_method_data.xml:20`, `addons/payment_stripe/data/payment_method_data.xml:43`, `addons/payment_stripe/data/payment_method_data.xml:57`, `addons/payment_stripe/data/payment_method_data.xml:75`, `addons/payment_stripe/data/payment_method_data.xml:101`, `addons/payment_stripe/data/payment_method_data.xml:122`, `addons/payment_stripe/data/payment_method_data.xml:149`, `addons/payment_stripe/data/payment_method_data.xml:161`, `addons/payment_stripe/data/payment_method_data.xml:173`, `addons/payment_stripe/data/payment_method_data.xml:185`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/payment_stripe/tests/test_processing_flows.py`, `addons/payment_stripe/tests/common.py`, `addons/payment_stripe/tests/test_refund_flows.py`, `addons/payment_stripe/tests/__init__.py`, `addons/payment_stripe/tests/test_stripe.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `payment.payment_provider_stripe`, `payment_method_ach_direct_debit`, `payment_method_acss_direct_debit`, `payment_method_affirm`, `payment_method_afterpay`, `payment_method_alipay`, `payment_method_alma`, `payment_method_amazon_pay`, `payment_method_bacs_direct_debit`, `payment_method_bancontact`, `payment_method_becs_direct_debit`, `payment_method_boleto`, `payment_method_card`, `payment_method_cash_app_pay`, `payment_method_clearpay`, `payment_method_eps`, `payment_method_fpx`, `payment_method_grabpay`, `payment_method_ideal`, `payment_method_klarna`
- Menus: 0; representative evidence: Not found in module
- Templates: 5; representative evidence: `addons/payment_stripe/views/payment_stripe_templates.xml:4`, `addons/payment_stripe/views/payment_stripe_templates.xml:20`, `addons/payment_stripe/views/payment_templates.xml:4`, `addons/payment_stripe/views/payment_templates.xml:10`, `addons/payment_stripe/views/payment_templates.xml:16`
- View/action field declarations: 4; representative evidence: `addons/payment_stripe/views/payment_provider_views.xml:6`, `addons/payment_stripe/views/payment_provider_views.xml:8`, `addons/payment_stripe/views/payment_provider_views.xml:83`, `addons/payment_stripe/views/payment_provider_views.xml:84`
- Browser assets: 3; representative files: `addons/payment_stripe/static/src/interactions/stripe_options.js`, `addons/payment_stripe/static/src/interactions/express_checkout.js`, `addons/payment_stripe/static/src/interactions/payment_form.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/payment_stripe/__manifest__.py`
- **HTTP entry points:** `addons/payment_stripe/controllers/onboarding.py:11`, `addons/payment_stripe/controllers/onboarding.py:29`, `addons/payment_stripe/controllers/main.py:29`, `addons/payment_stripe/controllers/main.py:69`, `addons/payment_stripe/controllers/main.py:94`, `addons/payment_stripe/controllers/main.py:262`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `payment.token` (addons/payment_stripe/models/payment_token.py:11); inherits `payment.transaction` (addons/payment_stripe/models/payment_transaction.py:18); inherits `payment.provider` (addons/payment_stripe/models/payment_provider.py:21)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 6
- Route evidence: `addons/payment_stripe/controllers/onboarding.py:11`, `addons/payment_stripe/controllers/onboarding.py:29`, `addons/payment_stripe/controllers/main.py:29`, `addons/payment_stripe/controllers/main.py:69`, `addons/payment_stripe/controllers/main.py:94`, `addons/payment_stripe/controllers/main.py:262`
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

- `addons/payment_stripe/README.md`
- `addons/payment_stripe/__init__.py`
- `addons/payment_stripe/__manifest__.py`
- `addons/payment_stripe/const.py`
- `addons/payment_stripe/controllers/__init__.py`
- `addons/payment_stripe/controllers/main.py`
- `addons/payment_stripe/controllers/onboarding.py`
- `addons/payment_stripe/data/neutralize.sql`
- `addons/payment_stripe/data/payment_method_data.xml`
- `addons/payment_stripe/data/payment_provider_data.xml`
- `addons/payment_stripe/i18n/ar.po`
- `addons/payment_stripe/i18n/az.po`
- `addons/payment_stripe/i18n/bg.po`
- `addons/payment_stripe/i18n/bs.po`
- `addons/payment_stripe/i18n/ca.po`
- `addons/payment_stripe/i18n/cs.po`
- `addons/payment_stripe/i18n/da.po`
- `addons/payment_stripe/i18n/de.po`
- `addons/payment_stripe/i18n/el.po`
- `addons/payment_stripe/i18n/es.po`
- `addons/payment_stripe/i18n/es_419.po`
- `addons/payment_stripe/i18n/et.po`
- `addons/payment_stripe/i18n/fa.po`
- `addons/payment_stripe/i18n/fi.po`
- `addons/payment_stripe/i18n/fr.po`
- `addons/payment_stripe/i18n/he.po`
- `addons/payment_stripe/i18n/hi.po`
- `addons/payment_stripe/i18n/hr.po`
- `addons/payment_stripe/i18n/hu.po`
- `addons/payment_stripe/i18n/id.po`
- `addons/payment_stripe/i18n/is.po`
- `addons/payment_stripe/i18n/it.po`
- `addons/payment_stripe/i18n/ja.po`
- `addons/payment_stripe/i18n/kab.po`
- `addons/payment_stripe/i18n/ko.po`
- `addons/payment_stripe/i18n/ku.po`
- `addons/payment_stripe/i18n/lo.po`
- `addons/payment_stripe/i18n/lt.po`
- `addons/payment_stripe/i18n/lv.po`
- `addons/payment_stripe/i18n/mn.po`
- `addons/payment_stripe/i18n/my.po`
- `addons/payment_stripe/i18n/nb.po`
- `addons/payment_stripe/i18n/nl.po`
- `addons/payment_stripe/i18n/payment_stripe.pot`
- `addons/payment_stripe/i18n/pl.po`
- `addons/payment_stripe/i18n/pt.po`
- `addons/payment_stripe/i18n/pt_BR.po`
- `addons/payment_stripe/i18n/ro.po`
- `addons/payment_stripe/i18n/ru.po`
- `addons/payment_stripe/i18n/sk.po`
- `addons/payment_stripe/i18n/sl.po`
- `addons/payment_stripe/i18n/sr@latin.po`
- `addons/payment_stripe/i18n/sv.po`
- `addons/payment_stripe/i18n/th.po`
- `addons/payment_stripe/i18n/tr.po`
- `addons/payment_stripe/i18n/uk.po`
- `addons/payment_stripe/i18n/uz.po`
- `addons/payment_stripe/i18n/vi.po`
- `addons/payment_stripe/i18n/zh_CN.po`
- `addons/payment_stripe/i18n/zh_TW.po`
- `addons/payment_stripe/models/__init__.py`
- `addons/payment_stripe/models/payment_provider.py`
- `addons/payment_stripe/models/payment_token.py`
- `addons/payment_stripe/models/payment_transaction.py`
- `addons/payment_stripe/static/description/icon.png`
- `addons/payment_stripe/static/description/icon.svg`
- `addons/payment_stripe/static/description/icon_hi.png`
- `addons/payment_stripe/static/files/apple-developer-merchantid-domain-association`
- `addons/payment_stripe/static/src/interactions/express_checkout.js`
- `addons/payment_stripe/static/src/interactions/payment_form.js`
- `addons/payment_stripe/static/src/interactions/stripe_options.js`
- `addons/payment_stripe/static/src/scss/payment_stripe_templates.scss`
- `addons/payment_stripe/tests/__init__.py`
- `addons/payment_stripe/tests/common.py`
- `addons/payment_stripe/tests/test_processing_flows.py`
- `addons/payment_stripe/tests/test_refund_flows.py`
- `addons/payment_stripe/tests/test_stripe.py`
- `addons/payment_stripe/utils.py`
- `addons/payment_stripe/views/payment_provider_views.xml`
- `addons/payment_stripe/views/payment_stripe_templates.xml`
- `addons/payment_stripe/views/payment_templates.xml`
