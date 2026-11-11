# Module: stock_dropshipping

- **Module ID:** MOD-562
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/stock_dropshipping`
- **Manifest:** `addons/stock_dropshipping/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Inventory`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Drop Shipping

**Manifest description:**

Manage drop shipping orders
===========================

This module adds a pre-configured Drop Shipping operation type
as well as a procurement route that allow configuring Drop
Shipping products and orders.

When drop shipping is used the goods are directly transferred
from vendors to customers (direct delivery) without
going through the retailer's warehouse. In this case no
internal transfer document is needed.

**Scope evidence:** The module contains 76 files, including 18 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `sale_purchase_stock`.

## 2. Module structure

- Model/business logic files: 13
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 0
- Security files: 0
- Test files: 7
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 13 model declarations, 83 methods, 0 constraint handlers, 0 onchange handlers, and 6 dependency declarations.
- **Evidence:** `addons/stock_dropshipping/models/stock_move_line.py:4`, `addons/stock_dropshipping/models/purchase.py:10`, `addons/stock_dropshipping/models/purchase.py:89`, `addons/stock_dropshipping/models/product.py:6`, `addons/stock_dropshipping/models/stock.py:7`, `addons/stock_dropshipping/models/stock.py:31`, `addons/stock_dropshipping/models/stock.py:48`, `addons/stock_dropshipping/models/stock.py:85`, `addons/stock_dropshipping/models/stock_replenish_mixin.py:7`, `addons/stock_dropshipping/models/sale.py:7`, `addons/stock_dropshipping/models/sale.py:27`, `addons/stock_dropshipping/models/account_move_line.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 10 record/template/menu identifiers.
- **Evidence:** `addons/stock_dropshipping/data/stock_dropshipping_demo.xml:4`, `addons/stock_dropshipping/data/stock_dropshipping_demo.xml:8`, `addons/stock_dropshipping/data/stock_dropshipping_demo.xml:12`, `addons/stock_dropshipping/data/stock_data.xml:7`, `addons/stock_dropshipping/views/stock_picking_views.xml:3`, `addons/stock_dropshipping/views/stock_picking_views.xml:14`, `addons/stock_dropshipping/views/stock_picking_views.xml:29`, `addons/stock_dropshipping/views/stock_picking_views.xml:24`, `addons/stock_dropshipping/views/sale_order_views.xml:4`, `addons/stock_dropshipping/views/purchase_order_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 7 test files are present.
- **Evidence:** `addons/stock_dropshipping/tests/test_dropship.py`, `addons/stock_dropshipping/tests/test_procurement_exception.py`, `addons/stock_dropshipping/tests/test_dropship_variant_description.py`, `addons/stock_dropshipping/tests/test_stockvaluation.py`, `addons/stock_dropshipping/tests/__init__.py`, `addons/stock_dropshipping/tests/test_lifo_price.py`, `addons/stock_dropshipping/tests/test_purchase_order.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `product.product_product_6`, `sale_order_purchase`, `sale_order_line_purchase`, `route_drop_shipping`, `view_picking_internal_search_inherit_stock_dropshipping`, `action_picking_tree_dropship`, `stock_picking_type_kanban`, `Dropships`, `view_order_form_inherit_sale_stock`, `purchase_order_form_inherit_stock_dropshipping`
- Menus: 1; representative evidence: `addons/stock_dropshipping/views/stock_picking_views.xml:24`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 10; representative evidence: `addons/stock_dropshipping/views/stock_picking_views.xml:5`, `addons/stock_dropshipping/views/stock_picking_views.xml:7`, `addons/stock_dropshipping/views/stock_picking_views.xml:16`, `addons/stock_dropshipping/views/stock_picking_views.xml:18`, `addons/stock_dropshipping/views/stock_picking_views.xml:31`, `addons/stock_dropshipping/views/stock_picking_views.xml:33`, `addons/stock_dropshipping/views/sale_order_views.xml:6`, `addons/stock_dropshipping/views/sale_order_views.xml:8`, `addons/stock_dropshipping/views/purchase_order_views.xml:5`, `addons/stock_dropshipping/views/purchase_order_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/stock_dropshipping/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 13
- Representative model evidence: inherits `stock.move.line` (addons/stock_dropshipping/models/stock_move_line.py:4); inherits `purchase.order` (addons/stock_dropshipping/models/purchase.py:10); inherits `purchase.order.line` (addons/stock_dropshipping/models/purchase.py:89); inherits `product.product` (addons/stock_dropshipping/models/product.py:6); inherits `stock.rule` (addons/stock_dropshipping/models/stock.py:7); inherits `stock.picking` (addons/stock_dropshipping/models/stock.py:31); inherits `stock.picking.type` (addons/stock_dropshipping/models/stock.py:48); inherits `stock.lot` (addons/stock_dropshipping/models/stock.py:85); inherits `stock.replenish.mixin` (addons/stock_dropshipping/models/stock_replenish_mixin.py:7); inherits `sale.order` (addons/stock_dropshipping/models/sale.py:7); inherits `sale.order.line` (addons/stock_dropshipping/models/sale.py:27); inherits `account.move.line` (addons/stock_dropshipping/models/account_move_line.py:4); inherits `res.company` (addons/stock_dropshipping/models/res_company.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale_purchase_stock`
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

- `addons/stock_dropshipping/__init__.py`
- `addons/stock_dropshipping/__manifest__.py`
- `addons/stock_dropshipping/data/stock_data.xml`
- `addons/stock_dropshipping/data/stock_dropshipping_demo.xml`
- `addons/stock_dropshipping/i18n/af.po`
- `addons/stock_dropshipping/i18n/ar.po`
- `addons/stock_dropshipping/i18n/az.po`
- `addons/stock_dropshipping/i18n/bg.po`
- `addons/stock_dropshipping/i18n/bs.po`
- `addons/stock_dropshipping/i18n/ca.po`
- `addons/stock_dropshipping/i18n/cs.po`
- `addons/stock_dropshipping/i18n/da.po`
- `addons/stock_dropshipping/i18n/de.po`
- `addons/stock_dropshipping/i18n/el.po`
- `addons/stock_dropshipping/i18n/es.po`
- `addons/stock_dropshipping/i18n/es_419.po`
- `addons/stock_dropshipping/i18n/et.po`
- `addons/stock_dropshipping/i18n/fa.po`
- `addons/stock_dropshipping/i18n/fi.po`
- `addons/stock_dropshipping/i18n/fr.po`
- `addons/stock_dropshipping/i18n/gu.po`
- `addons/stock_dropshipping/i18n/he.po`
- `addons/stock_dropshipping/i18n/hi.po`
- `addons/stock_dropshipping/i18n/hr.po`
- `addons/stock_dropshipping/i18n/hu.po`
- `addons/stock_dropshipping/i18n/id.po`
- `addons/stock_dropshipping/i18n/is.po`
- `addons/stock_dropshipping/i18n/it.po`
- `addons/stock_dropshipping/i18n/ja.po`
- `addons/stock_dropshipping/i18n/kab.po`
- `addons/stock_dropshipping/i18n/ko.po`
- `addons/stock_dropshipping/i18n/ku.po`
- `addons/stock_dropshipping/i18n/lo.po`
- `addons/stock_dropshipping/i18n/lt.po`
- `addons/stock_dropshipping/i18n/lv.po`
- `addons/stock_dropshipping/i18n/mk.po`
- `addons/stock_dropshipping/i18n/mn.po`
- `addons/stock_dropshipping/i18n/my.po`
- `addons/stock_dropshipping/i18n/nb.po`
- `addons/stock_dropshipping/i18n/nl.po`
- `addons/stock_dropshipping/i18n/pl.po`
- `addons/stock_dropshipping/i18n/pt.po`
- `addons/stock_dropshipping/i18n/pt_BR.po`
- `addons/stock_dropshipping/i18n/ro.po`
- `addons/stock_dropshipping/i18n/ru.po`
- `addons/stock_dropshipping/i18n/sk.po`
- `addons/stock_dropshipping/i18n/sl.po`
- `addons/stock_dropshipping/i18n/sr@latin.po`
- `addons/stock_dropshipping/i18n/stock_dropshipping.pot`
- `addons/stock_dropshipping/i18n/sv.po`
- `addons/stock_dropshipping/i18n/th.po`
- `addons/stock_dropshipping/i18n/tr.po`
- `addons/stock_dropshipping/i18n/uk.po`
- `addons/stock_dropshipping/i18n/uz.po`
- `addons/stock_dropshipping/i18n/vi.po`
- `addons/stock_dropshipping/i18n/zh_CN.po`
- `addons/stock_dropshipping/i18n/zh_TW.po`
- `addons/stock_dropshipping/models/__init__.py`
- `addons/stock_dropshipping/models/account_move_line.py`
- `addons/stock_dropshipping/models/product.py`
- `addons/stock_dropshipping/models/purchase.py`
- `addons/stock_dropshipping/models/res_company.py`
- `addons/stock_dropshipping/models/sale.py`
- `addons/stock_dropshipping/models/stock.py`
- `addons/stock_dropshipping/models/stock_move_line.py`
- `addons/stock_dropshipping/models/stock_replenish_mixin.py`
- `addons/stock_dropshipping/tests/__init__.py`
- `addons/stock_dropshipping/tests/test_dropship.py`
- `addons/stock_dropshipping/tests/test_dropship_variant_description.py`
- `addons/stock_dropshipping/tests/test_lifo_price.py`
- `addons/stock_dropshipping/tests/test_procurement_exception.py`
- `addons/stock_dropshipping/tests/test_purchase_order.py`
- `addons/stock_dropshipping/tests/test_stockvaluation.py`
- `addons/stock_dropshipping/views/purchase_order_views.xml`
- `addons/stock_dropshipping/views/sale_order_views.xml`
- `addons/stock_dropshipping/views/stock_picking_views.xml`
