# Module: pos_online_payment

- **Module ID:** MOD-440
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_online_payment`
- **Manifest:** `addons/pos_online_payment/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `not declared`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 84 files, including 15 Python, 7 XML, and 11 JavaScript/TypeScript files. The manifest declares dependencies: `point_of_sale`, `account_payment`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 3
- XML/data/view/template files: 7
- Browser asset files: 11
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/pos_online_payment/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 74 methods, 3 constraint handlers, 1 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/pos_online_payment/models/pos_payment.py:11`, `addons/pos_online_payment/models/pos_config.py:8`, `addons/pos_online_payment/models/account_payment.py:7`, `addons/pos_online_payment/models/pos_order.py:6`, `addons/pos_online_payment/models/pos_payment_method.py:7`, `addons/pos_online_payment/models/payment_transaction.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 3 route declarations.
- **Evidence:** `addons/pos_online_payment/controllers/payment_portal.py:89`, `addons/pos_online_payment/controllers/payment_portal.py:169`, `addons/pos_online_payment/controllers/payment_portal.py:284`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 11 JavaScript/TypeScript files; static XML analysis found 11 record/template/menu identifiers.
- **Evidence:** `addons/pos_online_payment/views/pos_payment_method_views.xml:3`, `addons/pos_online_payment/views/pos_payment_method_views.xml:35`, `addons/pos_online_payment/views/payment_portal_templates.xml:5`, `addons/pos_online_payment/views/payment_portal_templates.xml:48`, `addons/pos_online_payment/views/payment_portal_templates.xml:57`, `addons/pos_online_payment/views/payment_portal_templates.xml:122`, `addons/pos_online_payment/views/payment_portal_templates.xml:175`, `addons/pos_online_payment/views/res_config_settings_views.xml:3`, `addons/pos_online_payment/views/account_payment_views.xml:4`, `addons/pos_online_payment/views/pos_payment_views.xml:3`, `addons/pos_online_payment/views/payment_transaction_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/pos_online_payment/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/pos_online_payment/tests/test_frontend.py`, `addons/pos_online_payment/tests/online_payment_common.py`, `addons/pos_online_payment/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `pos_payment_method_view_form_inherit_pos_online_payment`, `pos_payment_method_view_tree_inherit_pos_online_payment`, `pay`, `pay_summary`, `POS Payment Status`, `POS State Header`, `pay_confirmation`, `res_config_settings_view_form`, `view_account_payment_form_inherit_pos_online_payment`, `view_pos_payment_form`, `payment_transaction_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 5; representative evidence: `addons/pos_online_payment/views/payment_portal_templates.xml:5`, `addons/pos_online_payment/views/payment_portal_templates.xml:48`, `addons/pos_online_payment/views/payment_portal_templates.xml:57`, `addons/pos_online_payment/views/payment_portal_templates.xml:122`, `addons/pos_online_payment/views/payment_portal_templates.xml:175`
- View/action field declarations: 12; representative evidence: `addons/pos_online_payment/views/pos_payment_method_views.xml:5`, `addons/pos_online_payment/views/pos_payment_method_views.xml:7`, `addons/pos_online_payment/views/pos_payment_method_views.xml:37`, `addons/pos_online_payment/views/pos_payment_method_views.xml:39`, `addons/pos_online_payment/views/res_config_settings_views.xml:5`, `addons/pos_online_payment/views/res_config_settings_views.xml:8`, `addons/pos_online_payment/views/account_payment_views.xml:6`, `addons/pos_online_payment/views/account_payment_views.xml:8`, `addons/pos_online_payment/views/pos_payment_views.xml:5`, `addons/pos_online_payment/views/pos_payment_views.xml:7`, `addons/pos_online_payment/views/payment_transaction_views.xml:5`, `addons/pos_online_payment/views/payment_transaction_views.xml:7`
- Browser assets: 11; representative files: `addons/pos_online_payment/static/src/overrides/pos_overrides/services/customer_display_plugin.js`, `addons/pos_online_payment/static/src/overrides/pos_overrides/services/pos_store.js`, `addons/pos_online_payment/static/src/app/services/pos_store.js`, `addons/pos_online_payment/static/src/app/models/pos_order.js`, `addons/pos_online_payment/static/src/app/models/pos_payment.js`, `addons/pos_online_payment/static/src/app/utils/order_payment_validation.js`, `addons/pos_online_payment/static/src/app/screens/payment_screen/payment_screen.js`, `addons/pos_online_payment/static/src/portal/js/payment_status_dwell.js`, `addons/pos_online_payment/static/tests/tours/online_payment_tour.js`, `addons/pos_online_payment/static/tests/unit/customer_display/customer_display.test.js`, `addons/pos_online_payment/static/tests/unit/components/payment_lines.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_online_payment/__manifest__.py`
- **HTTP entry points:** `addons/pos_online_payment/controllers/payment_portal.py:89`, `addons/pos_online_payment/controllers/payment_portal.py:169`, `addons/pos_online_payment/controllers/payment_portal.py:284`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `pos.payment` (addons/pos_online_payment/models/pos_payment.py:11); inherits `pos.config` (addons/pos_online_payment/models/pos_config.py:8); inherits `account.payment` (addons/pos_online_payment/models/account_payment.py:7); inherits `pos.order` (addons/pos_online_payment/models/pos_order.py:6); inherits `pos.payment.method` (addons/pos_online_payment/models/pos_payment_method.py:7); inherits `payment.transaction` (addons/pos_online_payment/models/payment_transaction.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 3
- Route evidence: `addons/pos_online_payment/controllers/payment_portal.py:89`, `addons/pos_online_payment/controllers/payment_portal.py:169`, `addons/pos_online_payment/controllers/payment_portal.py:284`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `point_of_sale`, `account_payment`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/pos_online_payment/__init__.py`
- `addons/pos_online_payment/__manifest__.py`
- `addons/pos_online_payment/controllers/__init__.py`
- `addons/pos_online_payment/controllers/payment_portal.py`
- `addons/pos_online_payment/controllers/payment_status.py`
- `addons/pos_online_payment/i18n/ar.po`
- `addons/pos_online_payment/i18n/az.po`
- `addons/pos_online_payment/i18n/bg.po`
- `addons/pos_online_payment/i18n/bs.po`
- `addons/pos_online_payment/i18n/ca.po`
- `addons/pos_online_payment/i18n/cs.po`
- `addons/pos_online_payment/i18n/da.po`
- `addons/pos_online_payment/i18n/de.po`
- `addons/pos_online_payment/i18n/el.po`
- `addons/pos_online_payment/i18n/es.po`
- `addons/pos_online_payment/i18n/es_419.po`
- `addons/pos_online_payment/i18n/et.po`
- `addons/pos_online_payment/i18n/fa.po`
- `addons/pos_online_payment/i18n/fi.po`
- `addons/pos_online_payment/i18n/fr.po`
- `addons/pos_online_payment/i18n/he.po`
- `addons/pos_online_payment/i18n/hi.po`
- `addons/pos_online_payment/i18n/hr.po`
- `addons/pos_online_payment/i18n/hu.po`
- `addons/pos_online_payment/i18n/id.po`
- `addons/pos_online_payment/i18n/it.po`
- `addons/pos_online_payment/i18n/ja.po`
- `addons/pos_online_payment/i18n/kab.po`
- `addons/pos_online_payment/i18n/ko.po`
- `addons/pos_online_payment/i18n/ku.po`
- `addons/pos_online_payment/i18n/lo.po`
- `addons/pos_online_payment/i18n/lt.po`
- `addons/pos_online_payment/i18n/lv.po`
- `addons/pos_online_payment/i18n/mn.po`
- `addons/pos_online_payment/i18n/my.po`
- `addons/pos_online_payment/i18n/nb.po`
- `addons/pos_online_payment/i18n/nl.po`
- `addons/pos_online_payment/i18n/pl.po`
- `addons/pos_online_payment/i18n/pos_online_payment.pot`
- `addons/pos_online_payment/i18n/pt.po`
- `addons/pos_online_payment/i18n/pt_BR.po`
- `addons/pos_online_payment/i18n/ro.po`
- `addons/pos_online_payment/i18n/ru.po`
- `addons/pos_online_payment/i18n/sk.po`
- `addons/pos_online_payment/i18n/sl.po`
- `addons/pos_online_payment/i18n/sr@latin.po`
- `addons/pos_online_payment/i18n/sv.po`
- `addons/pos_online_payment/i18n/th.po`
- `addons/pos_online_payment/i18n/tr.po`
- `addons/pos_online_payment/i18n/uk.po`
- `addons/pos_online_payment/i18n/uz.po`
- `addons/pos_online_payment/i18n/vi.po`
- `addons/pos_online_payment/i18n/zh_CN.po`
- `addons/pos_online_payment/i18n/zh_TW.po`
- `addons/pos_online_payment/models/__init__.py`
- `addons/pos_online_payment/models/account_payment.py`
- `addons/pos_online_payment/models/payment_transaction.py`
- `addons/pos_online_payment/models/pos_config.py`
- `addons/pos_online_payment/models/pos_order.py`
- `addons/pos_online_payment/models/pos_payment.py`
- `addons/pos_online_payment/models/pos_payment_method.py`
- `addons/pos_online_payment/security/ir.access.csv`
- `addons/pos_online_payment/static/src/app/models/pos_order.js`
- `addons/pos_online_payment/static/src/app/models/pos_payment.js`
- `addons/pos_online_payment/static/src/app/screens/payment_screen/payment_lines/payment_lines.xml`
- `addons/pos_online_payment/static/src/app/screens/payment_screen/payment_screen.js`
- `addons/pos_online_payment/static/src/app/services/pos_store.js`
- `addons/pos_online_payment/static/src/app/utils/order_payment_validation.js`
- `addons/pos_online_payment/static/src/overrides/pos_overrides/services/customer_display_plugin.js`
- `addons/pos_online_payment/static/src/overrides/pos_overrides/services/pos_store.js`
- `addons/pos_online_payment/static/src/portal/js/payment_status_dwell.js`
- `addons/pos_online_payment/static/src/portal/scss/payment_portal_template.scss`
- `addons/pos_online_payment/static/tests/tours/online_payment_tour.js`
- `addons/pos_online_payment/static/tests/unit/components/payment_lines.test.js`
- `addons/pos_online_payment/static/tests/unit/customer_display/customer_display.test.js`
- `addons/pos_online_payment/tests/__init__.py`
- `addons/pos_online_payment/tests/online_payment_common.py`
- `addons/pos_online_payment/tests/test_frontend.py`
- `addons/pos_online_payment/views/account_payment_views.xml`
- `addons/pos_online_payment/views/payment_portal_templates.xml`
- `addons/pos_online_payment/views/payment_transaction_views.xml`
- `addons/pos_online_payment/views/pos_payment_method_views.xml`
- `addons/pos_online_payment/views/pos_payment_views.xml`
- `addons/pos_online_payment/views/res_config_settings_views.xml`
