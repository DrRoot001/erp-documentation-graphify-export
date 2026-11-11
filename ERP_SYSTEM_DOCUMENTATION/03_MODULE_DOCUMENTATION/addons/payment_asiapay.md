# Module: payment_asiapay

- **Module ID:** MOD-395
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/payment_asiapay`
- **Manifest:** `addons/payment_asiapay/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Payment Providers`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** An payment provider based in Hong Kong covering most Asian countries.

**Manifest description:**



**Scope evidence:** The module contains 70 files, including 13 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `payment`.

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

- **Description:** 2 model declarations, 24 methods, 1 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/payment_asiapay/models/payment_transaction.py:15`, `addons/payment_asiapay/models/payment_provider.py:11`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 2 route declarations.
- **Evidence:** `addons/payment_asiapay/controllers/main.py:18`, `addons/payment_asiapay/controllers/main.py:28`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 43 record/template/menu identifiers.
- **Evidence:** `addons/payment_asiapay/data/payment_provider_data.xml:4`, `addons/payment_asiapay/data/payment_method_data.xml:8`, `addons/payment_asiapay/data/payment_method_data.xml:15`, `addons/payment_asiapay/data/payment_method_data.xml:24`, `addons/payment_asiapay/data/payment_method_data.xml:35`, `addons/payment_asiapay/data/payment_method_data.xml:44`, `addons/payment_asiapay/data/payment_method_data.xml:53`, `addons/payment_asiapay/data/payment_method_data.xml:61`, `addons/payment_asiapay/data/payment_method_data.xml:70`, `addons/payment_asiapay/data/payment_method_data.xml:79`, `addons/payment_asiapay/data/payment_method_data.xml:88`, `addons/payment_asiapay/data/payment_method_data.xml:97`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/payment_asiapay/tests/test_processing_flows.py`, `addons/payment_asiapay/tests/common.py`, `addons/payment_asiapay/tests/test_payment_provider.py`, `addons/payment_asiapay/tests/test_payment_transaction.py`, `addons/payment_asiapay/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `payment.payment_provider_asiapay`, `payment_method_alipay`, `payment_method_alipay_hk`, `payment_method_atome`, `payment_method_bank_of_ayudhya`, `payment_method_bangkok_bank`, `payment_method_card`, `payment_method_duitnow`, `payment_method_enets`, `payment_method_fps`, `payment_method_gcash`, `payment_method_hoolah`, `payment_method_humm`, `payment_method_jkopay`, `payment_method_krungthai_bank`, `payment_method_linepay`, `payment_method_maya`, `payment_method_maybank`, `payment_method_momo`, `payment_method_octopus`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/payment_asiapay/views/payment_provider_views.xml:6`, `addons/payment_asiapay/views/payment_provider_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/payment_asiapay/__manifest__.py`
- **HTTP entry points:** `addons/payment_asiapay/controllers/main.py:18`, `addons/payment_asiapay/controllers/main.py:28`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `payment.transaction` (addons/payment_asiapay/models/payment_transaction.py:15); inherits `payment.provider` (addons/payment_asiapay/models/payment_provider.py:11)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 2
- Route evidence: `addons/payment_asiapay/controllers/main.py:18`, `addons/payment_asiapay/controllers/main.py:28`
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

- `addons/payment_asiapay/README.md`
- `addons/payment_asiapay/__init__.py`
- `addons/payment_asiapay/__manifest__.py`
- `addons/payment_asiapay/const.py`
- `addons/payment_asiapay/controllers/__init__.py`
- `addons/payment_asiapay/controllers/main.py`
- `addons/payment_asiapay/data/neutralize.sql`
- `addons/payment_asiapay/data/payment_method_data.xml`
- `addons/payment_asiapay/data/payment_provider_data.xml`
- `addons/payment_asiapay/i18n/ar.po`
- `addons/payment_asiapay/i18n/az.po`
- `addons/payment_asiapay/i18n/bg.po`
- `addons/payment_asiapay/i18n/bs.po`
- `addons/payment_asiapay/i18n/ca.po`
- `addons/payment_asiapay/i18n/cs.po`
- `addons/payment_asiapay/i18n/da.po`
- `addons/payment_asiapay/i18n/de.po`
- `addons/payment_asiapay/i18n/el.po`
- `addons/payment_asiapay/i18n/es.po`
- `addons/payment_asiapay/i18n/es_419.po`
- `addons/payment_asiapay/i18n/et.po`
- `addons/payment_asiapay/i18n/fa.po`
- `addons/payment_asiapay/i18n/fi.po`
- `addons/payment_asiapay/i18n/fr.po`
- `addons/payment_asiapay/i18n/he.po`
- `addons/payment_asiapay/i18n/hi.po`
- `addons/payment_asiapay/i18n/hr.po`
- `addons/payment_asiapay/i18n/hu.po`
- `addons/payment_asiapay/i18n/id.po`
- `addons/payment_asiapay/i18n/it.po`
- `addons/payment_asiapay/i18n/ja.po`
- `addons/payment_asiapay/i18n/kab.po`
- `addons/payment_asiapay/i18n/ko.po`
- `addons/payment_asiapay/i18n/ku.po`
- `addons/payment_asiapay/i18n/lo.po`
- `addons/payment_asiapay/i18n/lt.po`
- `addons/payment_asiapay/i18n/lv.po`
- `addons/payment_asiapay/i18n/mn.po`
- `addons/payment_asiapay/i18n/my.po`
- `addons/payment_asiapay/i18n/nb.po`
- `addons/payment_asiapay/i18n/nl.po`
- `addons/payment_asiapay/i18n/payment_asiapay.pot`
- `addons/payment_asiapay/i18n/pl.po`
- `addons/payment_asiapay/i18n/pt.po`
- `addons/payment_asiapay/i18n/pt_BR.po`
- `addons/payment_asiapay/i18n/ro.po`
- `addons/payment_asiapay/i18n/ru.po`
- `addons/payment_asiapay/i18n/sk.po`
- `addons/payment_asiapay/i18n/sl.po`
- `addons/payment_asiapay/i18n/sr@latin.po`
- `addons/payment_asiapay/i18n/sv.po`
- `addons/payment_asiapay/i18n/th.po`
- `addons/payment_asiapay/i18n/tr.po`
- `addons/payment_asiapay/i18n/uk.po`
- `addons/payment_asiapay/i18n/uz.po`
- `addons/payment_asiapay/i18n/vi.po`
- `addons/payment_asiapay/i18n/zh_CN.po`
- `addons/payment_asiapay/i18n/zh_TW.po`
- `addons/payment_asiapay/models/__init__.py`
- `addons/payment_asiapay/models/payment_provider.py`
- `addons/payment_asiapay/models/payment_transaction.py`
- `addons/payment_asiapay/static/description/icon.png`
- `addons/payment_asiapay/static/description/icon.svg`
- `addons/payment_asiapay/static/description/icon_hi.png`
- `addons/payment_asiapay/tests/__init__.py`
- `addons/payment_asiapay/tests/common.py`
- `addons/payment_asiapay/tests/test_payment_provider.py`
- `addons/payment_asiapay/tests/test_payment_transaction.py`
- `addons/payment_asiapay/tests/test_processing_flows.py`
- `addons/payment_asiapay/views/payment_provider_views.xml`
