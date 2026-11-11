# Module: pos_pine_labs

- **Module ID:** MOD-443
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_pine_labs`
- **Manifest:** `addons/pos_pine_labs/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Integrate your POS with Pine Labs payment terminals

**Manifest description:**

Allow Pine Labs POS payments
==============================

This module is available only for companies that use INR currency.
It enables customers to pay for their orders using debit/credit cards and UPI through Pine Labs POS terminals.
A Pine Labs merchant account is required to process transactions.
Features include:

* Quick payments by swiping, scanning, or tapping your credit/debit card or UPI QR code at the payment terminal.
* Supported cards: Visa, MasterCard, RuPay.

**Scope evidence:** The module contains 60 files, including 6 Python, 2 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `point_of_sale`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 2
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 5 methods, 1 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/pos_pine_labs/models/pos_payment.py:3`, `addons/pos_pine_labs/models/pos_payment_method.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 2 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/pos_pine_labs/views/pos_payment_method_views.xml:3`, `addons/pos_pine_labs/views/pos_payment_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `pos_payment_method_view_form_inherit_pos_pine_labs`, `view_pos_payment_form_inherit_pine_labs`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/pos_pine_labs/views/pos_payment_method_views.xml:5`, `addons/pos_pine_labs/views/pos_payment_method_views.xml:7`, `addons/pos_pine_labs/views/pos_payment_views.xml:5`, `addons/pos_pine_labs/views/pos_payment_views.xml:7`
- Browser assets: 2; representative files: `addons/pos_pine_labs/static/src/app/screens/payment_screen/payment_screen.js`, `addons/pos_pine_labs/static/src/app/utils/payment/payment_pine_labs.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_pine_labs/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `pos.payment` (addons/pos_pine_labs/models/pos_payment.py:3); inherits `pos.payment.method` (addons/pos_pine_labs/models/pos_payment_method.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `point_of_sale`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/pos_pine_labs/__init__.py`
- `addons/pos_pine_labs/__manifest__.py`
- `addons/pos_pine_labs/data/neutralize.sql`
- `addons/pos_pine_labs/i18n/ar.po`
- `addons/pos_pine_labs/i18n/az.po`
- `addons/pos_pine_labs/i18n/bg.po`
- `addons/pos_pine_labs/i18n/bs.po`
- `addons/pos_pine_labs/i18n/ca.po`
- `addons/pos_pine_labs/i18n/cs.po`
- `addons/pos_pine_labs/i18n/da.po`
- `addons/pos_pine_labs/i18n/de.po`
- `addons/pos_pine_labs/i18n/el.po`
- `addons/pos_pine_labs/i18n/es.po`
- `addons/pos_pine_labs/i18n/es_419.po`
- `addons/pos_pine_labs/i18n/et.po`
- `addons/pos_pine_labs/i18n/fa.po`
- `addons/pos_pine_labs/i18n/fi.po`
- `addons/pos_pine_labs/i18n/fr.po`
- `addons/pos_pine_labs/i18n/he.po`
- `addons/pos_pine_labs/i18n/hi.po`
- `addons/pos_pine_labs/i18n/hr.po`
- `addons/pos_pine_labs/i18n/hu.po`
- `addons/pos_pine_labs/i18n/id.po`
- `addons/pos_pine_labs/i18n/it.po`
- `addons/pos_pine_labs/i18n/ja.po`
- `addons/pos_pine_labs/i18n/kab.po`
- `addons/pos_pine_labs/i18n/ko.po`
- `addons/pos_pine_labs/i18n/ku.po`
- `addons/pos_pine_labs/i18n/lo.po`
- `addons/pos_pine_labs/i18n/lt.po`
- `addons/pos_pine_labs/i18n/lv.po`
- `addons/pos_pine_labs/i18n/mn.po`
- `addons/pos_pine_labs/i18n/my.po`
- `addons/pos_pine_labs/i18n/nb.po`
- `addons/pos_pine_labs/i18n/nl.po`
- `addons/pos_pine_labs/i18n/pl.po`
- `addons/pos_pine_labs/i18n/pos_pine_labs.pot`
- `addons/pos_pine_labs/i18n/pt.po`
- `addons/pos_pine_labs/i18n/pt_BR.po`
- `addons/pos_pine_labs/i18n/ro.po`
- `addons/pos_pine_labs/i18n/ru.po`
- `addons/pos_pine_labs/i18n/sk.po`
- `addons/pos_pine_labs/i18n/sl.po`
- `addons/pos_pine_labs/i18n/sr@latin.po`
- `addons/pos_pine_labs/i18n/sv.po`
- `addons/pos_pine_labs/i18n/th.po`
- `addons/pos_pine_labs/i18n/tr.po`
- `addons/pos_pine_labs/i18n/uk.po`
- `addons/pos_pine_labs/i18n/uz.po`
- `addons/pos_pine_labs/i18n/vi.po`
- `addons/pos_pine_labs/i18n/zh_CN.po`
- `addons/pos_pine_labs/i18n/zh_TW.po`
- `addons/pos_pine_labs/models/__init__.py`
- `addons/pos_pine_labs/models/pine_labs_pos_request.py`
- `addons/pos_pine_labs/models/pos_payment.py`
- `addons/pos_pine_labs/models/pos_payment_method.py`
- `addons/pos_pine_labs/static/src/app/screens/payment_screen/payment_screen.js`
- `addons/pos_pine_labs/static/src/app/utils/payment/payment_pine_labs.js`
- `addons/pos_pine_labs/views/pos_payment_method_views.xml`
- `addons/pos_pine_labs/views/pos_payment_views.xml`
