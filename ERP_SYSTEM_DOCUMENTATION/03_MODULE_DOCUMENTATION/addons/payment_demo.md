# Module: payment_demo

- **Module ID:** MOD-399
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/payment_demo`
- **Manifest:** `addons/payment_demo/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** A payment provider for running fake payment flows for demo purposes.

**Manifest description:**



**Scope evidence:** The module contains 77 files, including 14 Python, 6 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `payment`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 3
- XML/data/view/template files: 6
- Browser asset files: 3
- Security files: 0
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 26 methods, 1 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/payment_demo/models/payment_token.py:6`, `addons/payment_demo/models/payment_transaction.py:10`, `addons/payment_demo/models/payment_provider.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 1 route declarations.
- **Evidence:** `addons/payment_demo/controllers/main.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 3 JavaScript/TypeScript files; static XML analysis found 11 record/template/menu identifiers.
- **Evidence:** `addons/payment_demo/data/payment_provider_data.xml:4`, `addons/payment_demo/data/payment_method_data.xml:4`, `addons/payment_demo/data/payment_method_data.xml:17`, `addons/payment_demo/views/payment_demo_templates.xml:4`, `addons/payment_demo/views/payment_demo_templates.xml:10`, `addons/payment_demo/views/payment_demo_templates.xml:29`, `addons/payment_demo/views/payment_demo_templates.xml:80`, `addons/payment_demo/views/payment_demo_templates.xml:181`, `addons/payment_demo/views/payment_token_views.xml:4`, `addons/payment_demo/views/payment_transaction_views.xml:4`, `addons/payment_demo/views/payment_provider_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/payment_demo/tests/test_processing_flows.py`, `addons/payment_demo/tests/common.py`, `addons/payment_demo/tests/test_payment_transaction.py`, `addons/payment_demo/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `payment.payment_provider_demo`, `payment_method_demo`, `payment_method_unknown`, `inline_form`, `token_inline_form`, `express_checkout_form`, `express_inline_form`, `payment_details`, `payment_token_form`, `payment_transaction_form`, `payment_provider_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 5; representative evidence: `addons/payment_demo/views/payment_demo_templates.xml:4`, `addons/payment_demo/views/payment_demo_templates.xml:10`, `addons/payment_demo/views/payment_demo_templates.xml:29`, `addons/payment_demo/views/payment_demo_templates.xml:80`, `addons/payment_demo/views/payment_demo_templates.xml:181`
- View/action field declarations: 6; representative evidence: `addons/payment_demo/views/payment_token_views.xml:6`, `addons/payment_demo/views/payment_token_views.xml:8`, `addons/payment_demo/views/payment_transaction_views.xml:6`, `addons/payment_demo/views/payment_transaction_views.xml:8`, `addons/payment_demo/views/payment_provider_views.xml:6`, `addons/payment_demo/views/payment_provider_views.xml:8`
- Browser assets: 3; representative files: `addons/payment_demo/static/src/interactions/express_checkout.js`, `addons/payment_demo/static/src/interactions/payment_form.js`, `addons/payment_demo/static/src/interactions/payment_demo_mixin.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/payment_demo/__manifest__.py`
- **HTTP entry points:** `addons/payment_demo/controllers/main.py:9`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `payment.token` (addons/payment_demo/models/payment_token.py:6); inherits `payment.transaction` (addons/payment_demo/models/payment_transaction.py:10); inherits `payment.provider` (addons/payment_demo/models/payment_provider.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 1
- Route evidence: `addons/payment_demo/controllers/main.py:9`
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

- `addons/payment_demo/README.md`
- `addons/payment_demo/__init__.py`
- `addons/payment_demo/__manifest__.py`
- `addons/payment_demo/const.py`
- `addons/payment_demo/controllers/__init__.py`
- `addons/payment_demo/controllers/main.py`
- `addons/payment_demo/controllers/portal.py`
- `addons/payment_demo/data/payment_method_data.xml`
- `addons/payment_demo/data/payment_provider_data.xml`
- `addons/payment_demo/i18n/ar.po`
- `addons/payment_demo/i18n/az.po`
- `addons/payment_demo/i18n/bg.po`
- `addons/payment_demo/i18n/bs.po`
- `addons/payment_demo/i18n/ca.po`
- `addons/payment_demo/i18n/cs.po`
- `addons/payment_demo/i18n/da.po`
- `addons/payment_demo/i18n/de.po`
- `addons/payment_demo/i18n/el.po`
- `addons/payment_demo/i18n/es.po`
- `addons/payment_demo/i18n/es_419.po`
- `addons/payment_demo/i18n/et.po`
- `addons/payment_demo/i18n/fa.po`
- `addons/payment_demo/i18n/fi.po`
- `addons/payment_demo/i18n/fr.po`
- `addons/payment_demo/i18n/he.po`
- `addons/payment_demo/i18n/hi.po`
- `addons/payment_demo/i18n/hr.po`
- `addons/payment_demo/i18n/hu.po`
- `addons/payment_demo/i18n/id.po`
- `addons/payment_demo/i18n/it.po`
- `addons/payment_demo/i18n/ja.po`
- `addons/payment_demo/i18n/kab.po`
- `addons/payment_demo/i18n/ko.po`
- `addons/payment_demo/i18n/ku.po`
- `addons/payment_demo/i18n/lo.po`
- `addons/payment_demo/i18n/lt.po`
- `addons/payment_demo/i18n/lv.po`
- `addons/payment_demo/i18n/mn.po`
- `addons/payment_demo/i18n/my.po`
- `addons/payment_demo/i18n/nb.po`
- `addons/payment_demo/i18n/nl.po`
- `addons/payment_demo/i18n/payment_demo.pot`
- `addons/payment_demo/i18n/pl.po`
- `addons/payment_demo/i18n/pt.po`
- `addons/payment_demo/i18n/pt_BR.po`
- `addons/payment_demo/i18n/ro.po`
- `addons/payment_demo/i18n/ru.po`
- `addons/payment_demo/i18n/sk.po`
- `addons/payment_demo/i18n/sl.po`
- `addons/payment_demo/i18n/sr@latin.po`
- `addons/payment_demo/i18n/sv.po`
- `addons/payment_demo/i18n/th.po`
- `addons/payment_demo/i18n/tr.po`
- `addons/payment_demo/i18n/uk.po`
- `addons/payment_demo/i18n/uz.po`
- `addons/payment_demo/i18n/vi.po`
- `addons/payment_demo/i18n/zh_CN.po`
- `addons/payment_demo/i18n/zh_TW.po`
- `addons/payment_demo/models/__init__.py`
- `addons/payment_demo/models/payment_provider.py`
- `addons/payment_demo/models/payment_token.py`
- `addons/payment_demo/models/payment_transaction.py`
- `addons/payment_demo/static/description/icon.png`
- `addons/payment_demo/static/description/icon.svg`
- `addons/payment_demo/static/description/icon_hi.png`
- `addons/payment_demo/static/img/demo.png`
- `addons/payment_demo/static/src/interactions/express_checkout.js`
- `addons/payment_demo/static/src/interactions/payment_demo_mixin.js`
- `addons/payment_demo/static/src/interactions/payment_form.js`
- `addons/payment_demo/tests/__init__.py`
- `addons/payment_demo/tests/common.py`
- `addons/payment_demo/tests/test_payment_transaction.py`
- `addons/payment_demo/tests/test_processing_flows.py`
- `addons/payment_demo/views/payment_demo_templates.xml`
- `addons/payment_demo/views/payment_provider_views.xml`
- `addons/payment_demo/views/payment_token_views.xml`
- `addons/payment_demo/views/payment_transaction_views.xml`
