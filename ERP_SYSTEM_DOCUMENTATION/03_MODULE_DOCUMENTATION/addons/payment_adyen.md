# Module: payment_adyen

- **Module ID:** MOD-393
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/payment_adyen`
- **Manifest:** `addons/payment_adyen/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Payment Providers`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** A Dutch payment provider covering Europe and the US.

**Manifest description:**



**Scope evidence:** The module contains 77 files, including 16 Python, 6 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `payment`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 2
- XML/data/view/template files: 6
- Browser asset files: 1
- Security files: 0
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 58 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/payment_adyen/models/payment_token.py:6`, `addons/payment_adyen/models/payment_transaction.py:14`, `addons/payment_adyen/models/payment_provider.py:16`, `addons/payment_adyen/wizards/payment_capture_wizard.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 5 route declarations.
- **Evidence:** `addons/payment_adyen/controllers/main.py:24`, `addons/payment_adyen/controllers/main.py:58`, `addons/payment_adyen/controllers/main.py:163`, `addons/payment_adyen/controllers/main.py:199`, `addons/payment_adyen/controllers/main.py:243`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 1 JavaScript/TypeScript files; static XML analysis found 79 record/template/menu identifiers.
- **Evidence:** `addons/payment_adyen/wizards/payment_capture_wizard_views.xml:4`, `addons/payment_adyen/data/payment_provider_data.xml:4`, `addons/payment_adyen/data/payment_method_data.xml:6`, `addons/payment_adyen/data/payment_method_data.xml:18`, `addons/payment_adyen/data/payment_method_data.xml:36`, `addons/payment_adyen/data/payment_method_data.xml:54`, `addons/payment_adyen/data/payment_method_data.xml:134`, `addons/payment_adyen/data/payment_method_data.xml:146`, `addons/payment_adyen/data/payment_method_data.xml:158`, `addons/payment_adyen/data/payment_method_data.xml:170`, `addons/payment_adyen/data/payment_method_data.xml:182`, `addons/payment_adyen/data/payment_method_data.xml:194`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/payment_adyen/tests/test_adyen.py`, `addons/payment_adyen/tests/test_processing_flows.py`, `addons/payment_adyen/tests/common.py`, `addons/payment_adyen/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `payment_capture_wizard_view_form`, `payment.payment_provider_adyen`, `payment_method_ach_direct_debit`, `payment_method_affirm`, `payment_method_afterpay`, `payment_method_alipay`, `payment_method_alipay_hk`, `payment_method_alma`, `payment_method_bacs_direct_debit`, `payment_method_bancontact`, `payment_method_benefit`, `payment_method_bizum`, `payment_method_blik`, `payment_method_card`, `payment_method_cash_app_pay`, `payment_method_clearpay`, `payment_method_dana`, `payment_method_duitnow`, `payment_method_eps`, `payment_method_fpx`
- Menus: 0; representative evidence: Not found in module
- Templates: 3; representative evidence: `addons/payment_adyen/views/payment_adyen_templates.xml:4`, `addons/payment_adyen/views/payment_form_templates.xml:5`, `addons/payment_adyen/views/payment_form_templates.xml:19`
- View/action field declarations: 4; representative evidence: `addons/payment_adyen/wizards/payment_capture_wizard_views.xml:6`, `addons/payment_adyen/wizards/payment_capture_wizard_views.xml:8`, `addons/payment_adyen/views/payment_provider_views.xml:6`, `addons/payment_adyen/views/payment_provider_views.xml:8`
- Browser assets: 1; representative files: `addons/payment_adyen/static/src/interactions/payment_form.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/payment_adyen/__manifest__.py`
- **HTTP entry points:** `addons/payment_adyen/controllers/main.py:24`, `addons/payment_adyen/controllers/main.py:58`, `addons/payment_adyen/controllers/main.py:163`, `addons/payment_adyen/controllers/main.py:199`, `addons/payment_adyen/controllers/main.py:243`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `payment.token` (addons/payment_adyen/models/payment_token.py:6); inherits `payment.transaction` (addons/payment_adyen/models/payment_transaction.py:14); inherits `payment.provider` (addons/payment_adyen/models/payment_provider.py:16); inherits `payment.capture.wizard` (addons/payment_adyen/wizards/payment_capture_wizard.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 5
- Route evidence: `addons/payment_adyen/controllers/main.py:24`, `addons/payment_adyen/controllers/main.py:58`, `addons/payment_adyen/controllers/main.py:163`, `addons/payment_adyen/controllers/main.py:199`, `addons/payment_adyen/controllers/main.py:243`
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

- `addons/payment_adyen/README.md`
- `addons/payment_adyen/__init__.py`
- `addons/payment_adyen/__manifest__.py`
- `addons/payment_adyen/const.py`
- `addons/payment_adyen/controllers/__init__.py`
- `addons/payment_adyen/controllers/main.py`
- `addons/payment_adyen/data/neutralize.sql`
- `addons/payment_adyen/data/payment_method_data.xml`
- `addons/payment_adyen/data/payment_provider_data.xml`
- `addons/payment_adyen/i18n/ar.po`
- `addons/payment_adyen/i18n/az.po`
- `addons/payment_adyen/i18n/bg.po`
- `addons/payment_adyen/i18n/bs.po`
- `addons/payment_adyen/i18n/ca.po`
- `addons/payment_adyen/i18n/cs.po`
- `addons/payment_adyen/i18n/da.po`
- `addons/payment_adyen/i18n/de.po`
- `addons/payment_adyen/i18n/el.po`
- `addons/payment_adyen/i18n/es.po`
- `addons/payment_adyen/i18n/es_419.po`
- `addons/payment_adyen/i18n/et.po`
- `addons/payment_adyen/i18n/fa.po`
- `addons/payment_adyen/i18n/fi.po`
- `addons/payment_adyen/i18n/fr.po`
- `addons/payment_adyen/i18n/he.po`
- `addons/payment_adyen/i18n/hi.po`
- `addons/payment_adyen/i18n/hr.po`
- `addons/payment_adyen/i18n/hu.po`
- `addons/payment_adyen/i18n/id.po`
- `addons/payment_adyen/i18n/it.po`
- `addons/payment_adyen/i18n/ja.po`
- `addons/payment_adyen/i18n/kab.po`
- `addons/payment_adyen/i18n/ko.po`
- `addons/payment_adyen/i18n/ku.po`
- `addons/payment_adyen/i18n/lo.po`
- `addons/payment_adyen/i18n/lt.po`
- `addons/payment_adyen/i18n/lv.po`
- `addons/payment_adyen/i18n/mn.po`
- `addons/payment_adyen/i18n/my.po`
- `addons/payment_adyen/i18n/nb.po`
- `addons/payment_adyen/i18n/nl.po`
- `addons/payment_adyen/i18n/payment_adyen.pot`
- `addons/payment_adyen/i18n/pl.po`
- `addons/payment_adyen/i18n/pt.po`
- `addons/payment_adyen/i18n/pt_BR.po`
- `addons/payment_adyen/i18n/ro.po`
- `addons/payment_adyen/i18n/ru.po`
- `addons/payment_adyen/i18n/sk.po`
- `addons/payment_adyen/i18n/sl.po`
- `addons/payment_adyen/i18n/sr@latin.po`
- `addons/payment_adyen/i18n/sv.po`
- `addons/payment_adyen/i18n/th.po`
- `addons/payment_adyen/i18n/tr.po`
- `addons/payment_adyen/i18n/uk.po`
- `addons/payment_adyen/i18n/uz.po`
- `addons/payment_adyen/i18n/vi.po`
- `addons/payment_adyen/i18n/zh_CN.po`
- `addons/payment_adyen/i18n/zh_TW.po`
- `addons/payment_adyen/models/__init__.py`
- `addons/payment_adyen/models/payment_provider.py`
- `addons/payment_adyen/models/payment_token.py`
- `addons/payment_adyen/models/payment_transaction.py`
- `addons/payment_adyen/static/description/icon.png`
- `addons/payment_adyen/static/description/icon.svg`
- `addons/payment_adyen/static/description/icon_hi.png`
- `addons/payment_adyen/static/src/interactions/payment_form.js`
- `addons/payment_adyen/tests/__init__.py`
- `addons/payment_adyen/tests/common.py`
- `addons/payment_adyen/tests/test_adyen.py`
- `addons/payment_adyen/tests/test_processing_flows.py`
- `addons/payment_adyen/utils.py`
- `addons/payment_adyen/views/payment_adyen_templates.xml`
- `addons/payment_adyen/views/payment_form_templates.xml`
- `addons/payment_adyen/views/payment_provider_views.xml`
- `addons/payment_adyen/wizards/__init__.py`
- `addons/payment_adyen/wizards/payment_capture_wizard.py`
- `addons/payment_adyen/wizards/payment_capture_wizard_views.xml`
