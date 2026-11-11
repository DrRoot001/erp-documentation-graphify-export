# Module: pos_adyen

- **Module ID:** MOD-423
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_adyen`
- **Manifest:** `addons/pos_adyen/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Integrate your POS with an Adyen payment terminal

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 70 files, including 13 Python, 2 XML, and 5 JavaScript/TypeScript files. The manifest declares dependencies: `point_of_sale`, `payment_adyen`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 3
- XML/data/view/template files: 2
- Browser asset files: 5
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 29 methods, 2 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/pos_adyen/models/pos_payment.py:6`, `addons/pos_adyen/models/pos_config.py:11`, `addons/pos_adyen/models/res_config_settings.py:7`, `addons/pos_adyen/models/pos_order.py:6`, `addons/pos_adyen/models/pos_payment_method.py:18`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 2 route declarations.
- **Evidence:** `addons/pos_adyen/controllers/payment_adyen.py:12`, `addons/pos_adyen/controllers/main.py:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 5 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/pos_adyen/views/pos_payment_method_views.xml:3`, `addons/pos_adyen/views/res_config_settings_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/pos_adyen/tests/__init__.py`, `addons/pos_adyen/tests/test_basic.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `pos_payment_method_view_form_inherit_pos_adyen`, `res_config_settings_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/pos_adyen/views/pos_payment_method_views.xml:5`, `addons/pos_adyen/views/pos_payment_method_views.xml:7`, `addons/pos_adyen/views/res_config_settings_views.xml:5`, `addons/pos_adyen/views/res_config_settings_views.xml:7`
- Browser assets: 5; representative files: `addons/pos_adyen/static/src/app/models/pos_payment.js`, `addons/pos_adyen/static/src/app/screens/payment_screen/payment_screen.js`, `addons/pos_adyen/static/src/app/utils/payment/payment_adyen.js`, `addons/pos_adyen/static/tests/tours/adyen_tour.js`, `addons/pos_adyen/static/tests/unit/data/pos_payment_method.data.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_adyen/__manifest__.py`
- **HTTP entry points:** `addons/pos_adyen/controllers/payment_adyen.py:12`, `addons/pos_adyen/controllers/main.py:15`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `pos.payment` (addons/pos_adyen/models/pos_payment.py:6); inherits `pos.config` (addons/pos_adyen/models/pos_config.py:11); inherits `res.config.settings` (addons/pos_adyen/models/res_config_settings.py:7); inherits `pos.order` (addons/pos_adyen/models/pos_order.py:6); inherits `pos.payment.method` (addons/pos_adyen/models/pos_payment_method.py:18)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 2
- Route evidence: `addons/pos_adyen/controllers/payment_adyen.py:12`, `addons/pos_adyen/controllers/main.py:15`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `point_of_sale`, `payment_adyen`
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

- `addons/pos_adyen/__init__.py`
- `addons/pos_adyen/__manifest__.py`
- `addons/pos_adyen/controllers/__init__.py`
- `addons/pos_adyen/controllers/main.py`
- `addons/pos_adyen/controllers/payment_adyen.py`
- `addons/pos_adyen/data/neutralize.sql`
- `addons/pos_adyen/i18n/ar.po`
- `addons/pos_adyen/i18n/az.po`
- `addons/pos_adyen/i18n/bg.po`
- `addons/pos_adyen/i18n/bs.po`
- `addons/pos_adyen/i18n/ca.po`
- `addons/pos_adyen/i18n/cs.po`
- `addons/pos_adyen/i18n/da.po`
- `addons/pos_adyen/i18n/de.po`
- `addons/pos_adyen/i18n/el.po`
- `addons/pos_adyen/i18n/es.po`
- `addons/pos_adyen/i18n/es_419.po`
- `addons/pos_adyen/i18n/et.po`
- `addons/pos_adyen/i18n/fa.po`
- `addons/pos_adyen/i18n/fi.po`
- `addons/pos_adyen/i18n/fr.po`
- `addons/pos_adyen/i18n/he.po`
- `addons/pos_adyen/i18n/hi.po`
- `addons/pos_adyen/i18n/hr.po`
- `addons/pos_adyen/i18n/hu.po`
- `addons/pos_adyen/i18n/id.po`
- `addons/pos_adyen/i18n/it.po`
- `addons/pos_adyen/i18n/ja.po`
- `addons/pos_adyen/i18n/kab.po`
- `addons/pos_adyen/i18n/ko.po`
- `addons/pos_adyen/i18n/ku.po`
- `addons/pos_adyen/i18n/lo.po`
- `addons/pos_adyen/i18n/lt.po`
- `addons/pos_adyen/i18n/lv.po`
- `addons/pos_adyen/i18n/mn.po`
- `addons/pos_adyen/i18n/my.po`
- `addons/pos_adyen/i18n/nb.po`
- `addons/pos_adyen/i18n/nl.po`
- `addons/pos_adyen/i18n/pl.po`
- `addons/pos_adyen/i18n/pos_adyen.pot`
- `addons/pos_adyen/i18n/pt.po`
- `addons/pos_adyen/i18n/pt_BR.po`
- `addons/pos_adyen/i18n/ro.po`
- `addons/pos_adyen/i18n/ru.po`
- `addons/pos_adyen/i18n/sk.po`
- `addons/pos_adyen/i18n/sl.po`
- `addons/pos_adyen/i18n/sr@latin.po`
- `addons/pos_adyen/i18n/sv.po`
- `addons/pos_adyen/i18n/th.po`
- `addons/pos_adyen/i18n/tr.po`
- `addons/pos_adyen/i18n/uk.po`
- `addons/pos_adyen/i18n/uz.po`
- `addons/pos_adyen/i18n/vi.po`
- `addons/pos_adyen/i18n/zh_CN.po`
- `addons/pos_adyen/i18n/zh_TW.po`
- `addons/pos_adyen/models/__init__.py`
- `addons/pos_adyen/models/pos_config.py`
- `addons/pos_adyen/models/pos_order.py`
- `addons/pos_adyen/models/pos_payment.py`
- `addons/pos_adyen/models/pos_payment_method.py`
- `addons/pos_adyen/models/res_config_settings.py`
- `addons/pos_adyen/static/src/app/models/pos_payment.js`
- `addons/pos_adyen/static/src/app/screens/payment_screen/payment_screen.js`
- `addons/pos_adyen/static/src/app/utils/payment/payment_adyen.js`
- `addons/pos_adyen/static/tests/tours/adyen_tour.js`
- `addons/pos_adyen/static/tests/unit/data/pos_payment_method.data.js`
- `addons/pos_adyen/tests/__init__.py`
- `addons/pos_adyen/tests/test_basic.py`
- `addons/pos_adyen/views/pos_payment_method_views.xml`
- `addons/pos_adyen/views/res_config_settings_views.xml`
