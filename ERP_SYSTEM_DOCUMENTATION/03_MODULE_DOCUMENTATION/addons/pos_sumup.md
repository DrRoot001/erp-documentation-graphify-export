# Module: pos_sumup

- **Module ID:** MOD-466
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_sumup`
- **Manifest:** `addons/pos_sumup/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Integrate your POS with a SumUp payment terminal

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 65 files, including 8 Python, 1 XML, and 7 JavaScript/TypeScript files. The manifest declares dependencies: `point_of_sale`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 2
- XML/data/view/template files: 1
- Browser asset files: 7
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 1 model declarations, 25 methods, 1 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/pos_sumup/models/pos_payment_method.py:46`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/pos_sumup/controllers/webhook.py:12`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 7 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/pos_sumup/views/pos_payment_method_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/pos_sumup/tests/test_sumup_payment_method.py`, `addons/pos_sumup/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `pos_payment_method_view_form_inherit_pos_sumup`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/pos_sumup/views/pos_payment_method_views.xml:5`, `addons/pos_sumup/views/pos_payment_method_views.xml:7`
- Browser assets: 7; representative files: `addons/pos_sumup/static/src/app/models/pos_payment.js`, `addons/pos_sumup/static/src/app/screens/payment_screen/payment_screen.js`, `addons/pos_sumup/static/src/app/utils/payment/payment_sumup.js`, `addons/pos_sumup/static/tests/unit/payment_sumup.test.js`, `addons/pos_sumup/static/tests/unit/payment_screen.test.js`, `addons/pos_sumup/static/tests/unit/data/pos_config.data.js`, `addons/pos_sumup/static/tests/unit/data/pos_payment_method.data.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_sumup/__manifest__.py`
- **HTTP entry points:** `addons/pos_sumup/controllers/webhook.py:12`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `pos.payment.method` (addons/pos_sumup/models/pos_payment_method.py:46)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/pos_sumup/controllers/webhook.py:12`
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

- `addons/pos_sumup/__init__.py`
- `addons/pos_sumup/__manifest__.py`
- `addons/pos_sumup/controllers/__init__.py`
- `addons/pos_sumup/controllers/webhook.py`
- `addons/pos_sumup/i18n/ar.po`
- `addons/pos_sumup/i18n/az.po`
- `addons/pos_sumup/i18n/bg.po`
- `addons/pos_sumup/i18n/bs.po`
- `addons/pos_sumup/i18n/ca.po`
- `addons/pos_sumup/i18n/cs.po`
- `addons/pos_sumup/i18n/da.po`
- `addons/pos_sumup/i18n/de.po`
- `addons/pos_sumup/i18n/el.po`
- `addons/pos_sumup/i18n/es.po`
- `addons/pos_sumup/i18n/es_419.po`
- `addons/pos_sumup/i18n/et.po`
- `addons/pos_sumup/i18n/fa.po`
- `addons/pos_sumup/i18n/fi.po`
- `addons/pos_sumup/i18n/fr.po`
- `addons/pos_sumup/i18n/he.po`
- `addons/pos_sumup/i18n/hi.po`
- `addons/pos_sumup/i18n/hr.po`
- `addons/pos_sumup/i18n/hu.po`
- `addons/pos_sumup/i18n/id.po`
- `addons/pos_sumup/i18n/it.po`
- `addons/pos_sumup/i18n/ja.po`
- `addons/pos_sumup/i18n/kab.po`
- `addons/pos_sumup/i18n/ko.po`
- `addons/pos_sumup/i18n/ku.po`
- `addons/pos_sumup/i18n/lo.po`
- `addons/pos_sumup/i18n/lt.po`
- `addons/pos_sumup/i18n/lv.po`
- `addons/pos_sumup/i18n/mn.po`
- `addons/pos_sumup/i18n/my.po`
- `addons/pos_sumup/i18n/nb.po`
- `addons/pos_sumup/i18n/nl.po`
- `addons/pos_sumup/i18n/pl.po`
- `addons/pos_sumup/i18n/pos_sumup.pot`
- `addons/pos_sumup/i18n/pt.po`
- `addons/pos_sumup/i18n/pt_BR.po`
- `addons/pos_sumup/i18n/ro.po`
- `addons/pos_sumup/i18n/ru.po`
- `addons/pos_sumup/i18n/sk.po`
- `addons/pos_sumup/i18n/sl.po`
- `addons/pos_sumup/i18n/sr@latin.po`
- `addons/pos_sumup/i18n/sv.po`
- `addons/pos_sumup/i18n/th.po`
- `addons/pos_sumup/i18n/tr.po`
- `addons/pos_sumup/i18n/uk.po`
- `addons/pos_sumup/i18n/uz.po`
- `addons/pos_sumup/i18n/vi.po`
- `addons/pos_sumup/i18n/zh_CN.po`
- `addons/pos_sumup/i18n/zh_TW.po`
- `addons/pos_sumup/models/__init__.py`
- `addons/pos_sumup/models/pos_payment_method.py`
- `addons/pos_sumup/static/src/app/models/pos_payment.js`
- `addons/pos_sumup/static/src/app/screens/payment_screen/payment_screen.js`
- `addons/pos_sumup/static/src/app/utils/payment/payment_sumup.js`
- `addons/pos_sumup/static/tests/unit/data/pos_config.data.js`
- `addons/pos_sumup/static/tests/unit/data/pos_payment_method.data.js`
- `addons/pos_sumup/static/tests/unit/payment_screen.test.js`
- `addons/pos_sumup/static/tests/unit/payment_sumup.test.js`
- `addons/pos_sumup/tests/__init__.py`
- `addons/pos_sumup/tests/test_sumup_payment_method.py`
- `addons/pos_sumup/views/pos_payment_method_views.xml`
