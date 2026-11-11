# Module: payment_iyzico

- **Module ID:** MOD-403
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/payment_iyzico`
- **Manifest:** `addons/payment_iyzico/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Payment Providers`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** A payment provider covering Turkey.

**Manifest description:**



**Scope evidence:** The module contains 69 files, including 13 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `payment`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 2
- XML/data/view/template files: 3
- Browser asset files: 0
- Security files: 0
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 27 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/payment_iyzico/models/payment_transaction.py:16`, `addons/payment_iyzico/models/payment_provider.py:17`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 2 route declarations.
- **Evidence:** `addons/payment_iyzico/controllers/main.py:18`, `addons/payment_iyzico/controllers/main.py:48`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 8 record/template/menu identifiers.
- **Evidence:** `addons/payment_iyzico/data/payment_provider_data.xml:4`, `addons/payment_iyzico/data/payment_method_data.xml:6`, `addons/payment_iyzico/data/payment_method_data.xml:13`, `addons/payment_iyzico/data/payment_method_data.xml:23`, `addons/payment_iyzico/data/payment_method_data.xml:31`, `addons/payment_iyzico/data/payment_method_data.xml:40`, `addons/payment_iyzico/data/payment_method_data.xml:48`, `addons/payment_iyzico/views/payment_provider_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/payment_iyzico/tests/test_processing_flows.py`, `addons/payment_iyzico/tests/common.py`, `addons/payment_iyzico/tests/test_payment_provider.py`, `addons/payment_iyzico/tests/test_payment_transaction.py`, `addons/payment_iyzico/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `payment.payment_provider_iyzico`, `payment_method_bank_transfer`, `payment_method_card`, `payment_method_amex`, `payment_method_mastercard`, `payment_method_troy`, `payment_method_visa`, `payment_provider_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/payment_iyzico/views/payment_provider_views.xml:6`, `addons/payment_iyzico/views/payment_provider_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/payment_iyzico/__manifest__.py`
- **HTTP entry points:** `addons/payment_iyzico/controllers/main.py:18`, `addons/payment_iyzico/controllers/main.py:48`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `payment.transaction` (addons/payment_iyzico/models/payment_transaction.py:16); inherits `payment.provider` (addons/payment_iyzico/models/payment_provider.py:17)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 2
- Route evidence: `addons/payment_iyzico/controllers/main.py:18`, `addons/payment_iyzico/controllers/main.py:48`
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

- `addons/payment_iyzico/README.md`
- `addons/payment_iyzico/__init__.py`
- `addons/payment_iyzico/__manifest__.py`
- `addons/payment_iyzico/const.py`
- `addons/payment_iyzico/controllers/__init__.py`
- `addons/payment_iyzico/controllers/main.py`
- `addons/payment_iyzico/data/neutralize.sql`
- `addons/payment_iyzico/data/payment_method_data.xml`
- `addons/payment_iyzico/data/payment_provider_data.xml`
- `addons/payment_iyzico/i18n/ar.po`
- `addons/payment_iyzico/i18n/az.po`
- `addons/payment_iyzico/i18n/bg.po`
- `addons/payment_iyzico/i18n/bs.po`
- `addons/payment_iyzico/i18n/ca.po`
- `addons/payment_iyzico/i18n/cs.po`
- `addons/payment_iyzico/i18n/da.po`
- `addons/payment_iyzico/i18n/de.po`
- `addons/payment_iyzico/i18n/el.po`
- `addons/payment_iyzico/i18n/es.po`
- `addons/payment_iyzico/i18n/es_419.po`
- `addons/payment_iyzico/i18n/et.po`
- `addons/payment_iyzico/i18n/fa.po`
- `addons/payment_iyzico/i18n/fi.po`
- `addons/payment_iyzico/i18n/fr.po`
- `addons/payment_iyzico/i18n/he.po`
- `addons/payment_iyzico/i18n/hi.po`
- `addons/payment_iyzico/i18n/hr.po`
- `addons/payment_iyzico/i18n/hu.po`
- `addons/payment_iyzico/i18n/id.po`
- `addons/payment_iyzico/i18n/it.po`
- `addons/payment_iyzico/i18n/ja.po`
- `addons/payment_iyzico/i18n/kab.po`
- `addons/payment_iyzico/i18n/ko.po`
- `addons/payment_iyzico/i18n/ku.po`
- `addons/payment_iyzico/i18n/lo.po`
- `addons/payment_iyzico/i18n/lt.po`
- `addons/payment_iyzico/i18n/lv.po`
- `addons/payment_iyzico/i18n/mn.po`
- `addons/payment_iyzico/i18n/my.po`
- `addons/payment_iyzico/i18n/nb.po`
- `addons/payment_iyzico/i18n/nl.po`
- `addons/payment_iyzico/i18n/payment_iyzico.pot`
- `addons/payment_iyzico/i18n/pl.po`
- `addons/payment_iyzico/i18n/pt.po`
- `addons/payment_iyzico/i18n/pt_BR.po`
- `addons/payment_iyzico/i18n/ro.po`
- `addons/payment_iyzico/i18n/ru.po`
- `addons/payment_iyzico/i18n/sk.po`
- `addons/payment_iyzico/i18n/sl.po`
- `addons/payment_iyzico/i18n/sr@latin.po`
- `addons/payment_iyzico/i18n/sv.po`
- `addons/payment_iyzico/i18n/th.po`
- `addons/payment_iyzico/i18n/tr.po`
- `addons/payment_iyzico/i18n/uk.po`
- `addons/payment_iyzico/i18n/uz.po`
- `addons/payment_iyzico/i18n/vi.po`
- `addons/payment_iyzico/i18n/zh_CN.po`
- `addons/payment_iyzico/i18n/zh_TW.po`
- `addons/payment_iyzico/models/__init__.py`
- `addons/payment_iyzico/models/payment_provider.py`
- `addons/payment_iyzico/models/payment_transaction.py`
- `addons/payment_iyzico/static/description/icon.png`
- `addons/payment_iyzico/static/description/icon.svg`
- `addons/payment_iyzico/tests/__init__.py`
- `addons/payment_iyzico/tests/common.py`
- `addons/payment_iyzico/tests/test_payment_provider.py`
- `addons/payment_iyzico/tests/test_payment_transaction.py`
- `addons/payment_iyzico/tests/test_processing_flows.py`
- `addons/payment_iyzico/views/payment_provider_views.xml`
