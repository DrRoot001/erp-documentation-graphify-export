# Module: pos_discount

- **Module ID:** MOD-427
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_discount`
- **Manifest:** `addons/pos_discount/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Simple Discounts in the Point of Sale

**Manifest description:**

This module allows the cashier to quickly give percentage-based
discount to a customer.

**Scope evidence:** The module contains 91 files, including 10 Python, 6 XML, and 17 JavaScript/TypeScript files. The manifest declares dependencies: `point_of_sale`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 17
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 13 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/pos_discount/models/product_template.py:4`, `addons/pos_discount/models/pos_config.py:8`, `addons/pos_discount/models/res_config_settings.py:7`, `addons/pos_discount/models/report_sale_details.py:6`, `addons/pos_discount/models/account_move_line.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 17 JavaScript/TypeScript files; static XML analysis found 4 record/template/menu identifiers.
- **Evidence:** `addons/pos_discount/data/pos_discount_data.xml:4`, `addons/pos_discount/receipt/pos_order_receipt.xml:4`, `addons/pos_discount/views/res_config_settings_views.xml:3`, `addons/pos_discount/views/pos_session_sales_details.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/pos_discount/tests/test_taxes_global_discount.py`, `addons/pos_discount/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `product_product_consumable`, `pos_discount.pos_order_receipt`, `res_config_settings_view_form`, `pos_discount.pos_session_sales_details`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/pos_discount/receipt/pos_order_receipt.xml:4`, `addons/pos_discount/views/pos_session_sales_details.xml:3`
- View/action field declarations: 2; representative evidence: `addons/pos_discount/views/res_config_settings_views.xml:5`, `addons/pos_discount/views/res_config_settings_views.xml:7`
- Browser assets: 17; representative files: `addons/pos_discount/static/src/app/services/pos_store.js`, `addons/pos_discount/static/src/app/models/pos_order_line.js`, `addons/pos_discount/static/src/app/screens/product_screen/product_screen.js`, `addons/pos_discount/static/src/app/screens/ticket_screen/ticket_screen.js`, `addons/pos_discount/static/src/app/screens/product_screen/control_buttons/control_buttons.js`, `addons/pos_discount/static/tests/unit/ui_utils.js`, `addons/pos_discount/static/tests/tours/test_pos_global_discount_flow.js`, `addons/pos_discount/static/tests/tours/test_taxes_global_discount.js`, `addons/pos_discount/static/tests/unit/services/pos_service.test.js`, `addons/pos_discount/static/tests/unit/models/pos_order_line.test.js`, `addons/pos_discount/static/tests/unit/data/pos_config.data.js`, `addons/pos_discount/static/tests/unit/data/product_product.data.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_discount/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `product.template` (addons/pos_discount/models/product_template.py:4); inherits `pos.config` (addons/pos_discount/models/pos_config.py:8); inherits `res.config.settings` (addons/pos_discount/models/res_config_settings.py:7); inherits `report.point_of_sale.report_saledetails` (addons/pos_discount/models/report_sale_details.py:6); inherits `account.move.line` (addons/pos_discount/models/account_move_line.py:6)
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
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/pos_discount/__init__.py`
- `addons/pos_discount/__manifest__.py`
- `addons/pos_discount/data/pos_discount_data.xml`
- `addons/pos_discount/i18n/af.po`
- `addons/pos_discount/i18n/ar.po`
- `addons/pos_discount/i18n/az.po`
- `addons/pos_discount/i18n/bg.po`
- `addons/pos_discount/i18n/bs.po`
- `addons/pos_discount/i18n/ca.po`
- `addons/pos_discount/i18n/cs.po`
- `addons/pos_discount/i18n/da.po`
- `addons/pos_discount/i18n/de.po`
- `addons/pos_discount/i18n/el.po`
- `addons/pos_discount/i18n/es.po`
- `addons/pos_discount/i18n/es_419.po`
- `addons/pos_discount/i18n/es_CL.po`
- `addons/pos_discount/i18n/et.po`
- `addons/pos_discount/i18n/eu.po`
- `addons/pos_discount/i18n/fa.po`
- `addons/pos_discount/i18n/fi.po`
- `addons/pos_discount/i18n/fo.po`
- `addons/pos_discount/i18n/fr.po`
- `addons/pos_discount/i18n/gu.po`
- `addons/pos_discount/i18n/he.po`
- `addons/pos_discount/i18n/hi.po`
- `addons/pos_discount/i18n/hr.po`
- `addons/pos_discount/i18n/hu.po`
- `addons/pos_discount/i18n/id.po`
- `addons/pos_discount/i18n/is.po`
- `addons/pos_discount/i18n/it.po`
- `addons/pos_discount/i18n/ja.po`
- `addons/pos_discount/i18n/ka.po`
- `addons/pos_discount/i18n/kab.po`
- `addons/pos_discount/i18n/km.po`
- `addons/pos_discount/i18n/ko.po`
- `addons/pos_discount/i18n/ku.po`
- `addons/pos_discount/i18n/lo.po`
- `addons/pos_discount/i18n/lt.po`
- `addons/pos_discount/i18n/lv.po`
- `addons/pos_discount/i18n/mk.po`
- `addons/pos_discount/i18n/mn.po`
- `addons/pos_discount/i18n/my.po`
- `addons/pos_discount/i18n/nb.po`
- `addons/pos_discount/i18n/nl.po`
- `addons/pos_discount/i18n/pl.po`
- `addons/pos_discount/i18n/pos_discount.pot`
- `addons/pos_discount/i18n/pt.po`
- `addons/pos_discount/i18n/pt_BR.po`
- `addons/pos_discount/i18n/ro.po`
- `addons/pos_discount/i18n/ru.po`
- `addons/pos_discount/i18n/sk.po`
- `addons/pos_discount/i18n/sl.po`
- `addons/pos_discount/i18n/sr@latin.po`
- `addons/pos_discount/i18n/sv.po`
- `addons/pos_discount/i18n/th.po`
- `addons/pos_discount/i18n/tr.po`
- `addons/pos_discount/i18n/uk.po`
- `addons/pos_discount/i18n/uz.po`
- `addons/pos_discount/i18n/vi.po`
- `addons/pos_discount/i18n/zh_CN.po`
- `addons/pos_discount/i18n/zh_TW.po`
- `addons/pos_discount/models/__init__.py`
- `addons/pos_discount/models/account_move_line.py`
- `addons/pos_discount/models/pos_config.py`
- `addons/pos_discount/models/product_template.py`
- `addons/pos_discount/models/report_sale_details.py`
- `addons/pos_discount/models/res_config_settings.py`
- `addons/pos_discount/receipt/pos_order_receipt.xml`
- `addons/pos_discount/static/src/app/models/pos_order_line.js`
- `addons/pos_discount/static/src/app/screens/product_screen/control_buttons/control_buttons.js`
- `addons/pos_discount/static/src/app/screens/product_screen/control_buttons/control_buttons.xml`
- `addons/pos_discount/static/src/app/screens/product_screen/product_screen.js`
- `addons/pos_discount/static/src/app/screens/ticket_screen/ticket_screen.js`
- `addons/pos_discount/static/src/app/services/pos_store.js`
- `addons/pos_discount/static/tests/tours/test_pos_global_discount_flow.js`
- `addons/pos_discount/static/tests/tours/test_taxes_global_discount.js`
- `addons/pos_discount/static/tests/unit/components/control_buttons.test.js`
- `addons/pos_discount/static/tests/unit/components/product_screen.test.js`
- `addons/pos_discount/static/tests/unit/components/ticket_screen.test.js`
- `addons/pos_discount/static/tests/unit/data/pos_config.data.js`
- `addons/pos_discount/static/tests/unit/data/product_product.data.js`
- `addons/pos_discount/static/tests/unit/data/product_template.data.js`
- `addons/pos_discount/static/tests/unit/models/pos_order_line.test.js`
- `addons/pos_discount/static/tests/unit/scenario/pos_discount_flow.test.js`
- `addons/pos_discount/static/tests/unit/services/pos_service.test.js`
- `addons/pos_discount/static/tests/unit/ui_utils.js`
- `addons/pos_discount/tests/__init__.py`
- `addons/pos_discount/tests/test_taxes_global_discount.py`
- `addons/pos_discount/views/pos_config_views.xml`
- `addons/pos_discount/views/pos_session_sales_details.xml`
- `addons/pos_discount/views/res_config_settings_views.xml`
