# Module: pos_bancontact_pay

- **Module ID:** MOD-424
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_bancontact_pay`
- **Manifest:** `addons/pos_bancontact_pay/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Accept Bancontact Pay and Wero QR code payments in POS (Payconiq).

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 94 files, including 20 Python, 3 XML, and 12 JavaScript/TypeScript files. The manifest declares dependencies: `point_of_sale`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 3
- XML/data/view/template files: 3
- Browser asset files: 12
- Security files: 0
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 104 methods, 5 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/pos_bancontact_pay/models/pos_payment.py:4`, `addons/pos_bancontact_pay/models/pos_config.py:5`, `addons/pos_bancontact_pay/models/account_journal.py:7`, `addons/pos_bancontact_pay/models/pos_payment_method.py:15`, `addons/pos_bancontact_pay/models/res_company.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 2 route declarations.
- **Evidence:** `addons/pos_bancontact_pay/controllers/webhook.py:24`, `addons/pos_bancontact_pay/controllers/webhook.py:64`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 12 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/pos_bancontact_pay/views/pos_payment_method_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/pos_bancontact_pay/tests/test_webhook.py`, `addons/pos_bancontact_pay/tests/test_models.py`, `addons/pos_bancontact_pay/tests/common.py`, `addons/pos_bancontact_pay/tests/__init__.py`, `addons/pos_bancontact_pay/tests/test_signature.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `pos_payment_method_view_form_inherit_bancontact_pay`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/pos_bancontact_pay/views/pos_payment_method_views.xml:5`, `addons/pos_bancontact_pay/views/pos_payment_method_views.xml:7`
- Browser assets: 12; representative files: `addons/pos_bancontact_pay/static/src/app/payment_bancontact.js`, `addons/pos_bancontact_pay/static/src/app/pos_payment_method.js`, `addons/pos_bancontact_pay/static/src/app/pos_store.js`, `addons/pos_bancontact_pay/static/src/app/pos_payment.js`, `addons/pos_bancontact_pay/static/src/app/qr_code_popup/qr_code_popup.js`, `addons/pos_bancontact_pay/static/tests/unit/ui_utils.js`, `addons/pos_bancontact_pay/static/tests/unit/app/pos_payment_method.test.js`, `addons/pos_bancontact_pay/static/tests/unit/app/pos_payment.test.js`, `addons/pos_bancontact_pay/static/tests/unit/app/pos_store.test.js`, `addons/pos_bancontact_pay/static/tests/unit/app/payment_bancontact.test.js`, `addons/pos_bancontact_pay/static/tests/unit/data/pos_payment_method.data.js`, `addons/pos_bancontact_pay/static/tests/unit/scenario/bancontact_pay_flow.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_bancontact_pay/__manifest__.py`
- **HTTP entry points:** `addons/pos_bancontact_pay/controllers/webhook.py:24`, `addons/pos_bancontact_pay/controllers/webhook.py:64`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `pos.payment` (addons/pos_bancontact_pay/models/pos_payment.py:4); inherits `pos.config` (addons/pos_bancontact_pay/models/pos_config.py:5); inherits `account.journal` (addons/pos_bancontact_pay/models/account_journal.py:7); inherits `pos.payment.method` (addons/pos_bancontact_pay/models/pos_payment_method.py:15); inherits `res.company` (addons/pos_bancontact_pay/models/res_company.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 2
- Route evidence: `addons/pos_bancontact_pay/controllers/webhook.py:24`, `addons/pos_bancontact_pay/controllers/webhook.py:64`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `point_of_sale`
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

- `addons/pos_bancontact_pay/__init__.py`
- `addons/pos_bancontact_pay/__manifest__.py`
- `addons/pos_bancontact_pay/const.py`
- `addons/pos_bancontact_pay/controllers/__init__.py`
- `addons/pos_bancontact_pay/controllers/signature.py`
- `addons/pos_bancontact_pay/controllers/webhook.py`
- `addons/pos_bancontact_pay/data/neutralize.sql`
- `addons/pos_bancontact_pay/errors/__init__.py`
- `addons/pos_bancontact_pay/errors/exceptions.py`
- `addons/pos_bancontact_pay/errors/http.py`
- `addons/pos_bancontact_pay/i18n/ar.po`
- `addons/pos_bancontact_pay/i18n/az.po`
- `addons/pos_bancontact_pay/i18n/bg.po`
- `addons/pos_bancontact_pay/i18n/bs.po`
- `addons/pos_bancontact_pay/i18n/ca.po`
- `addons/pos_bancontact_pay/i18n/cs.po`
- `addons/pos_bancontact_pay/i18n/da.po`
- `addons/pos_bancontact_pay/i18n/de.po`
- `addons/pos_bancontact_pay/i18n/el.po`
- `addons/pos_bancontact_pay/i18n/es.po`
- `addons/pos_bancontact_pay/i18n/es_419.po`
- `addons/pos_bancontact_pay/i18n/et.po`
- `addons/pos_bancontact_pay/i18n/fa.po`
- `addons/pos_bancontact_pay/i18n/fi.po`
- `addons/pos_bancontact_pay/i18n/fr.po`
- `addons/pos_bancontact_pay/i18n/he.po`
- `addons/pos_bancontact_pay/i18n/hi.po`
- `addons/pos_bancontact_pay/i18n/hr.po`
- `addons/pos_bancontact_pay/i18n/hu.po`
- `addons/pos_bancontact_pay/i18n/id.po`
- `addons/pos_bancontact_pay/i18n/it.po`
- `addons/pos_bancontact_pay/i18n/ja.po`
- `addons/pos_bancontact_pay/i18n/kab.po`
- `addons/pos_bancontact_pay/i18n/ko.po`
- `addons/pos_bancontact_pay/i18n/ku.po`
- `addons/pos_bancontact_pay/i18n/lo.po`
- `addons/pos_bancontact_pay/i18n/lt.po`
- `addons/pos_bancontact_pay/i18n/lv.po`
- `addons/pos_bancontact_pay/i18n/mn.po`
- `addons/pos_bancontact_pay/i18n/my.po`
- `addons/pos_bancontact_pay/i18n/nb.po`
- `addons/pos_bancontact_pay/i18n/nl.po`
- `addons/pos_bancontact_pay/i18n/pl.po`
- `addons/pos_bancontact_pay/i18n/pos_bancontact_pay.pot`
- `addons/pos_bancontact_pay/i18n/pt.po`
- `addons/pos_bancontact_pay/i18n/pt_BR.po`
- `addons/pos_bancontact_pay/i18n/ro.po`
- `addons/pos_bancontact_pay/i18n/ru.po`
- `addons/pos_bancontact_pay/i18n/sk.po`
- `addons/pos_bancontact_pay/i18n/sl.po`
- `addons/pos_bancontact_pay/i18n/sr@latin.po`
- `addons/pos_bancontact_pay/i18n/sv.po`
- `addons/pos_bancontact_pay/i18n/th.po`
- `addons/pos_bancontact_pay/i18n/tr.po`
- `addons/pos_bancontact_pay/i18n/uk.po`
- `addons/pos_bancontact_pay/i18n/uz.po`
- `addons/pos_bancontact_pay/i18n/vi.po`
- `addons/pos_bancontact_pay/i18n/zh_CN.po`
- `addons/pos_bancontact_pay/i18n/zh_TW.po`
- `addons/pos_bancontact_pay/models/__init__.py`
- `addons/pos_bancontact_pay/models/account_journal.py`
- `addons/pos_bancontact_pay/models/pos_config.py`
- `addons/pos_bancontact_pay/models/pos_payment.py`
- `addons/pos_bancontact_pay/models/pos_payment_method.py`
- `addons/pos_bancontact_pay/models/res_company.py`
- `addons/pos_bancontact_pay/static/description/icon.png`
- `addons/pos_bancontact_pay/static/description/icon.svg`
- `addons/pos_bancontact_pay/static/img/frames/frame_fr.png`
- `addons/pos_bancontact_pay/static/img/frames/frame_fr.svg`
- `addons/pos_bancontact_pay/static/img/frames/frame_nl.png`
- `addons/pos_bancontact_pay/static/img/frames/frame_nl.svg`
- `addons/pos_bancontact_pay/static/img/logo/logo_colored_bg.svg`
- `addons/pos_bancontact_pay/static/img/logo/logo_neutral_bg.svg`
- `addons/pos_bancontact_pay/static/img/logo/logo_white_bg.svg`
- `addons/pos_bancontact_pay/static/src/app/payment_bancontact.js`
- `addons/pos_bancontact_pay/static/src/app/pos_payment.js`
- `addons/pos_bancontact_pay/static/src/app/pos_payment_method.js`
- `addons/pos_bancontact_pay/static/src/app/pos_store.js`
- `addons/pos_bancontact_pay/static/src/app/qr_code_popup/qr_code_popup.js`
- `addons/pos_bancontact_pay/static/src/app/qr_code_popup/qr_code_popup.xml`
- `addons/pos_bancontact_pay/static/src/customer_display/customer_display.xml`
- `addons/pos_bancontact_pay/static/tests/unit/app/payment_bancontact.test.js`
- `addons/pos_bancontact_pay/static/tests/unit/app/pos_payment.test.js`
- `addons/pos_bancontact_pay/static/tests/unit/app/pos_payment_method.test.js`
- `addons/pos_bancontact_pay/static/tests/unit/app/pos_store.test.js`
- `addons/pos_bancontact_pay/static/tests/unit/data/pos_payment_method.data.js`
- `addons/pos_bancontact_pay/static/tests/unit/scenario/bancontact_pay_flow.test.js`
- `addons/pos_bancontact_pay/static/tests/unit/ui_utils.js`
- `addons/pos_bancontact_pay/tests/__init__.py`
- `addons/pos_bancontact_pay/tests/common.py`
- `addons/pos_bancontact_pay/tests/test_models.py`
- `addons/pos_bancontact_pay/tests/test_signature.py`
- `addons/pos_bancontact_pay/tests/test_webhook.py`
- `addons/pos_bancontact_pay/views/pos_payment_method_views.xml`
