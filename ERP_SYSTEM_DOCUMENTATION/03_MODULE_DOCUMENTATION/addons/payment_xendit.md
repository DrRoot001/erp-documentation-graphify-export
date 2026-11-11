# Module: payment_xendit

- **Module ID:** MOD-415
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/payment_xendit`
- **Manifest:** `addons/payment_xendit/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Payment Providers`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** A payment provider for Indonesian and the Philippines.

**Manifest description:**



**Scope evidence:** The module contains 72 files, including 13 Python, 4 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `payment`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 2
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

- **Description:** 2 model declarations, 76 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/payment_xendit/models/payment_transaction.py:22`, `addons/payment_xendit/models/payment_provider.py:12`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 3 route declarations.
- **Evidence:** `addons/payment_xendit/controllers/main.py:19`, `addons/payment_xendit/controllers/main.py:31`, `addons/payment_xendit/controllers/main.py:59`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 1 JavaScript/TypeScript files; static XML analysis found 50 record/template/menu identifiers.
- **Evidence:** `addons/payment_xendit/data/payment_provider_data.xml:4`, `addons/payment_xendit/data/payment_method_data.xml:8`, `addons/payment_xendit/data/payment_method_data.xml:18`, `addons/payment_xendit/data/payment_method_data.xml:28`, `addons/payment_xendit/data/payment_method_data.xml:38`, `addons/payment_xendit/data/payment_method_data.xml:48`, `addons/payment_xendit/data/payment_method_data.xml:58`, `addons/payment_xendit/data/payment_method_data.xml:68`, `addons/payment_xendit/data/payment_method_data.xml:78`, `addons/payment_xendit/data/payment_method_data.xml:88`, `addons/payment_xendit/data/payment_method_data.xml:98`, `addons/payment_xendit/data/payment_method_data.xml:108`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/payment_xendit/tests/test_processing_flows.py`, `addons/payment_xendit/tests/common.py`, `addons/payment_xendit/tests/test_payment_provider.py`, `addons/payment_xendit/tests/test_payment_transaction.py`, `addons/payment_xendit/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `payment.payment_provider_xendit`, `payment_method_7eleven`, `payment_method_akulaku`, `payment_method_appota`, `payment_method_bangkok_bank`, `payment_method_bank_bca`, `payment_method_bank_permata`, `payment_method_billease`, `payment_method_bni`, `payment_method_bri`, `payment_method_bsi`, `payment_method_card`, `payment_method_cashalo`, `payment_method_cebuana`, `payment_method_cimb_niaga`, `payment_method_dana`, `payment_method_fpx`, `payment_method_gcash`, `payment_method_grabpay`, `payment_method_jeniuspay`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/payment_xendit/views/payment_xendit_templates.xml:7`
- View/action field declarations: 2; representative evidence: `addons/payment_xendit/views/payment_provider_views.xml:6`, `addons/payment_xendit/views/payment_provider_views.xml:8`
- Browser assets: 1; representative files: `addons/payment_xendit/static/src/interactions/payment_form.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/payment_xendit/__manifest__.py`
- **HTTP entry points:** `addons/payment_xendit/controllers/main.py:19`, `addons/payment_xendit/controllers/main.py:31`, `addons/payment_xendit/controllers/main.py:59`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `payment.transaction` (addons/payment_xendit/models/payment_transaction.py:22); inherits `payment.provider` (addons/payment_xendit/models/payment_provider.py:12)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 3
- Route evidence: `addons/payment_xendit/controllers/main.py:19`, `addons/payment_xendit/controllers/main.py:31`, `addons/payment_xendit/controllers/main.py:59`
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

- `addons/payment_xendit/README.md`
- `addons/payment_xendit/__init__.py`
- `addons/payment_xendit/__manifest__.py`
- `addons/payment_xendit/const.py`
- `addons/payment_xendit/controllers/__init__.py`
- `addons/payment_xendit/controllers/main.py`
- `addons/payment_xendit/data/neutralize.sql`
- `addons/payment_xendit/data/payment_method_data.xml`
- `addons/payment_xendit/data/payment_provider_data.xml`
- `addons/payment_xendit/i18n/ar.po`
- `addons/payment_xendit/i18n/az.po`
- `addons/payment_xendit/i18n/bg.po`
- `addons/payment_xendit/i18n/bs.po`
- `addons/payment_xendit/i18n/ca.po`
- `addons/payment_xendit/i18n/cs.po`
- `addons/payment_xendit/i18n/da.po`
- `addons/payment_xendit/i18n/de.po`
- `addons/payment_xendit/i18n/el.po`
- `addons/payment_xendit/i18n/es.po`
- `addons/payment_xendit/i18n/es_419.po`
- `addons/payment_xendit/i18n/et.po`
- `addons/payment_xendit/i18n/fa.po`
- `addons/payment_xendit/i18n/fi.po`
- `addons/payment_xendit/i18n/fr.po`
- `addons/payment_xendit/i18n/he.po`
- `addons/payment_xendit/i18n/hi.po`
- `addons/payment_xendit/i18n/hr.po`
- `addons/payment_xendit/i18n/hu.po`
- `addons/payment_xendit/i18n/id.po`
- `addons/payment_xendit/i18n/it.po`
- `addons/payment_xendit/i18n/ja.po`
- `addons/payment_xendit/i18n/kab.po`
- `addons/payment_xendit/i18n/ko.po`
- `addons/payment_xendit/i18n/ku.po`
- `addons/payment_xendit/i18n/lo.po`
- `addons/payment_xendit/i18n/lt.po`
- `addons/payment_xendit/i18n/lv.po`
- `addons/payment_xendit/i18n/mn.po`
- `addons/payment_xendit/i18n/my.po`
- `addons/payment_xendit/i18n/nb.po`
- `addons/payment_xendit/i18n/nl.po`
- `addons/payment_xendit/i18n/payment_xendit.pot`
- `addons/payment_xendit/i18n/pl.po`
- `addons/payment_xendit/i18n/pt.po`
- `addons/payment_xendit/i18n/pt_BR.po`
- `addons/payment_xendit/i18n/ro.po`
- `addons/payment_xendit/i18n/ru.po`
- `addons/payment_xendit/i18n/sk.po`
- `addons/payment_xendit/i18n/sl.po`
- `addons/payment_xendit/i18n/sr@latin.po`
- `addons/payment_xendit/i18n/sv.po`
- `addons/payment_xendit/i18n/th.po`
- `addons/payment_xendit/i18n/tr.po`
- `addons/payment_xendit/i18n/uk.po`
- `addons/payment_xendit/i18n/uz.po`
- `addons/payment_xendit/i18n/vi.po`
- `addons/payment_xendit/i18n/zh_CN.po`
- `addons/payment_xendit/i18n/zh_TW.po`
- `addons/payment_xendit/models/__init__.py`
- `addons/payment_xendit/models/payment_provider.py`
- `addons/payment_xendit/models/payment_transaction.py`
- `addons/payment_xendit/static/description/icon.png`
- `addons/payment_xendit/static/description/icon.svg`
- `addons/payment_xendit/static/description/icon_hi.png`
- `addons/payment_xendit/static/src/interactions/payment_form.js`
- `addons/payment_xendit/tests/__init__.py`
- `addons/payment_xendit/tests/common.py`
- `addons/payment_xendit/tests/test_payment_provider.py`
- `addons/payment_xendit/tests/test_payment_transaction.py`
- `addons/payment_xendit/tests/test_processing_flows.py`
- `addons/payment_xendit/views/payment_provider_views.xml`
- `addons/payment_xendit/views/payment_xendit_templates.xml`
