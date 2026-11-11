# Module: payment_flutterwave

- **Module ID:** MOD-402
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/payment_flutterwave`
- **Manifest:** `addons/payment_flutterwave/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Payment Providers`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** A Nigerian payment provider covering several African countries.

**Manifest description:**



**Scope evidence:** The module contains 72 files, including 14 Python, 3 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `payment`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 2
- XML/data/view/template files: 3
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

- **Description:** 3 model declarations, 34 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/payment_flutterwave/models/payment_token.py:6`, `addons/payment_flutterwave/models/payment_transaction.py:17`, `addons/payment_flutterwave/models/payment_provider.py:14`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 3 route declarations.
- **Evidence:** `addons/payment_flutterwave/controllers/main.py:21`, `addons/payment_flutterwave/controllers/main.py:37`, `addons/payment_flutterwave/controllers/main.py:46`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 1 JavaScript/TypeScript files; static XML analysis found 14 record/template/menu identifiers.
- **Evidence:** `addons/payment_flutterwave/data/payment_provider_data.xml:4`, `addons/payment_flutterwave/data/payment_method_data.xml:8`, `addons/payment_flutterwave/data/payment_method_data.xml:20`, `addons/payment_flutterwave/data/payment_method_data.xml:30`, `addons/payment_flutterwave/data/payment_method_data.xml:39`, `addons/payment_flutterwave/data/payment_method_data.xml:71`, `addons/payment_flutterwave/data/payment_method_data.xml:81`, `addons/payment_flutterwave/data/payment_method_data.xml:90`, `addons/payment_flutterwave/data/payment_method_data.xml:102`, `addons/payment_flutterwave/data/payment_method_data.xml:112`, `addons/payment_flutterwave/data/payment_method_data.xml:122`, `addons/payment_flutterwave/data/payment_method_data.xml:132`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/payment_flutterwave/tests/test_processing_flows.py`, `addons/payment_flutterwave/tests/common.py`, `addons/payment_flutterwave/tests/test_payment_provider.py`, `addons/payment_flutterwave/tests/test_payment_transaction.py`, `addons/payment_flutterwave/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `payment.payment_provider_flutterwave`, `payment_method_bank_account`, `payment_method_bank_transfer`, `payment_method_card`, `payment_method_mobile_money`, `payment_method_mpesa`, `payment_method_paypal`, `payment_method_ussd`, `payment_method_amex`, `payment_method_credit`, `payment_method_discover`, `payment_method_mastercard`, `payment_method_visa`, `payment_provider_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/payment_flutterwave/views/payment_provider_views.xml:6`, `addons/payment_flutterwave/views/payment_provider_views.xml:8`
- Browser assets: 1; representative files: `addons/payment_flutterwave/static/src/interactions/payment_form.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/payment_flutterwave/__manifest__.py`
- **HTTP entry points:** `addons/payment_flutterwave/controllers/main.py:21`, `addons/payment_flutterwave/controllers/main.py:37`, `addons/payment_flutterwave/controllers/main.py:46`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `payment.token` (addons/payment_flutterwave/models/payment_token.py:6); inherits `payment.transaction` (addons/payment_flutterwave/models/payment_transaction.py:17); inherits `payment.provider` (addons/payment_flutterwave/models/payment_provider.py:14)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 3
- Route evidence: `addons/payment_flutterwave/controllers/main.py:21`, `addons/payment_flutterwave/controllers/main.py:37`, `addons/payment_flutterwave/controllers/main.py:46`
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

- `addons/payment_flutterwave/README.md`
- `addons/payment_flutterwave/__init__.py`
- `addons/payment_flutterwave/__manifest__.py`
- `addons/payment_flutterwave/const.py`
- `addons/payment_flutterwave/controllers/__init__.py`
- `addons/payment_flutterwave/controllers/main.py`
- `addons/payment_flutterwave/data/neutralize.sql`
- `addons/payment_flutterwave/data/payment_method_data.xml`
- `addons/payment_flutterwave/data/payment_provider_data.xml`
- `addons/payment_flutterwave/i18n/ar.po`
- `addons/payment_flutterwave/i18n/az.po`
- `addons/payment_flutterwave/i18n/bg.po`
- `addons/payment_flutterwave/i18n/bs.po`
- `addons/payment_flutterwave/i18n/ca.po`
- `addons/payment_flutterwave/i18n/cs.po`
- `addons/payment_flutterwave/i18n/da.po`
- `addons/payment_flutterwave/i18n/de.po`
- `addons/payment_flutterwave/i18n/el.po`
- `addons/payment_flutterwave/i18n/es.po`
- `addons/payment_flutterwave/i18n/es_419.po`
- `addons/payment_flutterwave/i18n/et.po`
- `addons/payment_flutterwave/i18n/fa.po`
- `addons/payment_flutterwave/i18n/fi.po`
- `addons/payment_flutterwave/i18n/fr.po`
- `addons/payment_flutterwave/i18n/he.po`
- `addons/payment_flutterwave/i18n/hi.po`
- `addons/payment_flutterwave/i18n/hr.po`
- `addons/payment_flutterwave/i18n/hu.po`
- `addons/payment_flutterwave/i18n/id.po`
- `addons/payment_flutterwave/i18n/it.po`
- `addons/payment_flutterwave/i18n/ja.po`
- `addons/payment_flutterwave/i18n/kab.po`
- `addons/payment_flutterwave/i18n/ko.po`
- `addons/payment_flutterwave/i18n/ku.po`
- `addons/payment_flutterwave/i18n/lo.po`
- `addons/payment_flutterwave/i18n/lt.po`
- `addons/payment_flutterwave/i18n/lv.po`
- `addons/payment_flutterwave/i18n/mn.po`
- `addons/payment_flutterwave/i18n/my.po`
- `addons/payment_flutterwave/i18n/nb.po`
- `addons/payment_flutterwave/i18n/nl.po`
- `addons/payment_flutterwave/i18n/payment_flutterwave.pot`
- `addons/payment_flutterwave/i18n/pl.po`
- `addons/payment_flutterwave/i18n/pt.po`
- `addons/payment_flutterwave/i18n/pt_BR.po`
- `addons/payment_flutterwave/i18n/ro.po`
- `addons/payment_flutterwave/i18n/ru.po`
- `addons/payment_flutterwave/i18n/sk.po`
- `addons/payment_flutterwave/i18n/sl.po`
- `addons/payment_flutterwave/i18n/sr@latin.po`
- `addons/payment_flutterwave/i18n/sv.po`
- `addons/payment_flutterwave/i18n/th.po`
- `addons/payment_flutterwave/i18n/tr.po`
- `addons/payment_flutterwave/i18n/uk.po`
- `addons/payment_flutterwave/i18n/uz.po`
- `addons/payment_flutterwave/i18n/vi.po`
- `addons/payment_flutterwave/i18n/zh_CN.po`
- `addons/payment_flutterwave/i18n/zh_TW.po`
- `addons/payment_flutterwave/models/__init__.py`
- `addons/payment_flutterwave/models/payment_provider.py`
- `addons/payment_flutterwave/models/payment_token.py`
- `addons/payment_flutterwave/models/payment_transaction.py`
- `addons/payment_flutterwave/static/description/icon.png`
- `addons/payment_flutterwave/static/description/icon.svg`
- `addons/payment_flutterwave/static/description/icon_hi.png`
- `addons/payment_flutterwave/static/src/interactions/payment_form.js`
- `addons/payment_flutterwave/tests/__init__.py`
- `addons/payment_flutterwave/tests/common.py`
- `addons/payment_flutterwave/tests/test_payment_provider.py`
- `addons/payment_flutterwave/tests/test_payment_transaction.py`
- `addons/payment_flutterwave/tests/test_processing_flows.py`
- `addons/payment_flutterwave/views/payment_provider_views.xml`
