# Module: event_booth_sale

- **Module ID:** MOD-066
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/event_booth_sale`
- **Manifest:** `addons/event_booth_sale/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Events`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Manage event booths sale

**Manifest description:**

Sell your event booths and track payments on sale orders.

**Scope evidence:** The module contains 78 files, including 18 Python, 8 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `event_booth`, `event_sale`.

## 2. Module structure

- Model/business logic files: 10
- Controller/API files: 0
- XML/data/view/template files: 8
- Browser asset files: 2
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/event_booth_sale/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 10 model declarations, 50 methods, 5 constraint handlers, 4 onchange handlers, and 13 dependency declarations.
- **Evidence:** `addons/event_booth_sale/models/event_booth_category.py:13`, `addons/event_booth_sale/models/sale_order.py:8`, `addons/event_booth_sale/models/product_product.py:5`, `addons/event_booth_sale/models/product_template.py:5`, `addons/event_booth_sale/models/event_type_booth.py:7`, `addons/event_booth_sale/models/event_booth_registration.py:8`, `addons/event_booth_sale/models/account_move.py:7`, `addons/event_booth_sale/models/event_booth.py:8`, `addons/event_booth_sale/models/sale_order_line.py:9`, `addons/event_booth_sale/wizard/event_booth_configurator.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 8 XML files and 2 JavaScript/TypeScript files; static XML analysis found 18 record/template/menu identifiers.
- **Evidence:** `addons/event_booth_sale/wizard/event_booth_configurator_views.xml:4`, `addons/event_booth_sale/wizard/event_booth_configurator_views.xml:37`, `addons/event_booth_sale/data/product_data.xml:4`, `addons/event_booth_sale/data/event_booth_category_data.xml:4`, `addons/event_booth_sale/data/event_booth_category_data.xml:9`, `addons/event_booth_sale/data/event_booth_category_data.xml:14`, `addons/event_booth_sale/views/event_booth_views.xml:4`, `addons/event_booth_sale/views/event_booth_views.xml:47`, `addons/event_booth_sale/views/event_booth_views.xml:59`, `addons/event_booth_sale/views/event_booth_views.xml:73`, `addons/event_booth_sale/views/event_booth_views.xml:84`, `addons/event_booth_sale/views/sale_order_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/event_booth_sale/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/event_booth_sale/tests/test_event_booth_sale.py`, `addons/event_booth_sale/tests/common.py`, `addons/event_booth_sale/tests/test_event_internals.py`, `addons/event_booth_sale/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 8; representative identifiers: `event_booth_configurator_view_form`, `event_booth_configurator_action`, `product_product_event_booth`, `event_booth.event_booth_category_standard`, `event_booth.event_booth_category_premium`, `event_booth.event_booth_category_vip`, `event_booth_view_form_from_event`, `event_booth_view_tree_from_event`, `event_booth_view_search`, `event_booth_view_graph`, `event_booth_view_pivot`, `sale_order_view_form`, `event_booth_category_view_form`, `event_booth_category_view_tree`, `event_type_booth_view_form_from_type`, `event_type_booth_view_tree_from_type`, `event_booth_registration_view_form`, `event_booth_registration_view_tree`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 28; representative evidence: `addons/event_booth_sale/wizard/event_booth_configurator_views.xml:6`, `addons/event_booth_sale/wizard/event_booth_configurator_views.xml:7`, `addons/event_booth_sale/wizard/event_booth_configurator_views.xml:39`, `addons/event_booth_sale/wizard/event_booth_configurator_views.xml:40`, `addons/event_booth_sale/views/event_booth_views.xml:6`, `addons/event_booth_sale/views/event_booth_views.xml:9`, `addons/event_booth_sale/views/event_booth_views.xml:49`, `addons/event_booth_sale/views/event_booth_views.xml:51`, `addons/event_booth_sale/views/event_booth_views.xml:61`, `addons/event_booth_sale/views/event_booth_views.xml:63`, `addons/event_booth_sale/views/event_booth_views.xml:75`, `addons/event_booth_sale/views/event_booth_views.xml:77`
- Browser assets: 2; representative files: `addons/event_booth_sale/static/src/js/event_booth_configurator_controller.js`, `addons/event_booth_sale/static/src/js/sale_product_mixin.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/event_booth_sale/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 10
- Representative model evidence: inherits `event.booth.category` (addons/event_booth_sale/models/event_booth_category.py:13); inherits `sale.order` (addons/event_booth_sale/models/sale_order.py:8); inherits `product.product` (addons/event_booth_sale/models/product_product.py:5); inherits `product.template` (addons/event_booth_sale/models/product_template.py:5); inherits `event.type.booth` (addons/event_booth_sale/models/event_type_booth.py:7); `event.booth.registration` (addons/event_booth_sale/models/event_booth_registration.py:8); inherits `account.move` (addons/event_booth_sale/models/account_move.py:7); inherits `event.booth` (addons/event_booth_sale/models/event_booth.py:8); inherits `sale.order.line` (addons/event_booth_sale/models/sale_order_line.py:9); `event.booth.configurator` (addons/event_booth_sale/wizard/event_booth_configurator.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `event_booth`, `event_sale`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/event_booth_sale/__init__.py`
- `addons/event_booth_sale/__manifest__.py`
- `addons/event_booth_sale/data/event_booth_category_data.xml`
- `addons/event_booth_sale/data/product_data.xml`
- `addons/event_booth_sale/i18n/ar.po`
- `addons/event_booth_sale/i18n/az.po`
- `addons/event_booth_sale/i18n/bg.po`
- `addons/event_booth_sale/i18n/bs.po`
- `addons/event_booth_sale/i18n/ca.po`
- `addons/event_booth_sale/i18n/cs.po`
- `addons/event_booth_sale/i18n/da.po`
- `addons/event_booth_sale/i18n/de.po`
- `addons/event_booth_sale/i18n/el.po`
- `addons/event_booth_sale/i18n/es.po`
- `addons/event_booth_sale/i18n/es_419.po`
- `addons/event_booth_sale/i18n/et.po`
- `addons/event_booth_sale/i18n/event_booth_sale.pot`
- `addons/event_booth_sale/i18n/fa.po`
- `addons/event_booth_sale/i18n/fi.po`
- `addons/event_booth_sale/i18n/fr.po`
- `addons/event_booth_sale/i18n/he.po`
- `addons/event_booth_sale/i18n/hi.po`
- `addons/event_booth_sale/i18n/hr.po`
- `addons/event_booth_sale/i18n/hu.po`
- `addons/event_booth_sale/i18n/id.po`
- `addons/event_booth_sale/i18n/it.po`
- `addons/event_booth_sale/i18n/ja.po`
- `addons/event_booth_sale/i18n/kab.po`
- `addons/event_booth_sale/i18n/ko.po`
- `addons/event_booth_sale/i18n/ku.po`
- `addons/event_booth_sale/i18n/lo.po`
- `addons/event_booth_sale/i18n/lt.po`
- `addons/event_booth_sale/i18n/lv.po`
- `addons/event_booth_sale/i18n/mn.po`
- `addons/event_booth_sale/i18n/my.po`
- `addons/event_booth_sale/i18n/nb.po`
- `addons/event_booth_sale/i18n/nl.po`
- `addons/event_booth_sale/i18n/pl.po`
- `addons/event_booth_sale/i18n/pt.po`
- `addons/event_booth_sale/i18n/pt_BR.po`
- `addons/event_booth_sale/i18n/ro.po`
- `addons/event_booth_sale/i18n/ru.po`
- `addons/event_booth_sale/i18n/sk.po`
- `addons/event_booth_sale/i18n/sl.po`
- `addons/event_booth_sale/i18n/sr@latin.po`
- `addons/event_booth_sale/i18n/sv.po`
- `addons/event_booth_sale/i18n/th.po`
- `addons/event_booth_sale/i18n/tr.po`
- `addons/event_booth_sale/i18n/uk.po`
- `addons/event_booth_sale/i18n/uz.po`
- `addons/event_booth_sale/i18n/vi.po`
- `addons/event_booth_sale/i18n/zh_CN.po`
- `addons/event_booth_sale/i18n/zh_TW.po`
- `addons/event_booth_sale/models/__init__.py`
- `addons/event_booth_sale/models/account_move.py`
- `addons/event_booth_sale/models/event_booth.py`
- `addons/event_booth_sale/models/event_booth_category.py`
- `addons/event_booth_sale/models/event_booth_registration.py`
- `addons/event_booth_sale/models/event_type_booth.py`
- `addons/event_booth_sale/models/product_product.py`
- `addons/event_booth_sale/models/product_template.py`
- `addons/event_booth_sale/models/sale_order.py`
- `addons/event_booth_sale/models/sale_order_line.py`
- `addons/event_booth_sale/security/ir.access.csv`
- `addons/event_booth_sale/static/src/js/event_booth_configurator_controller.js`
- `addons/event_booth_sale/static/src/js/sale_product_mixin.js`
- `addons/event_booth_sale/tests/__init__.py`
- `addons/event_booth_sale/tests/common.py`
- `addons/event_booth_sale/tests/test_event_booth_sale.py`
- `addons/event_booth_sale/tests/test_event_internals.py`
- `addons/event_booth_sale/views/event_booth_category_views.xml`
- `addons/event_booth_sale/views/event_booth_registration_views.xml`
- `addons/event_booth_sale/views/event_booth_views.xml`
- `addons/event_booth_sale/views/event_type_booth_views.xml`
- `addons/event_booth_sale/views/sale_order_views.xml`
- `addons/event_booth_sale/wizard/__init__.py`
- `addons/event_booth_sale/wizard/event_booth_configurator.py`
- `addons/event_booth_sale/wizard/event_booth_configurator_views.xml`
