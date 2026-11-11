# Module: mrp_subcontracting_dropshipping

- **Module ID:** MOD-385
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/mrp_subcontracting_dropshipping`
- **Manifest:** `addons/mrp_subcontracting_dropshipping/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Purchase`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This bridge module allows to manage subcontracting with the dropshipping module.

**Scope evidence:** The module contains 69 files, including 18 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `mrp_subcontracting`, `stock_dropshipping`.

## 2. Module structure

- Model/business logic files: 10
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 0
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 10 model declarations, 64 methods, 0 constraint handlers, 1 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/mrp_subcontracting_dropshipping/models/stock_move.py:7`, `addons/mrp_subcontracting_dropshipping/models/purchase.py:8`, `addons/mrp_subcontracting_dropshipping/models/stock_orderpoint.py:7`, `addons/mrp_subcontracting_dropshipping/models/stock_replenish_mixin.py:7`, `addons/mrp_subcontracting_dropshipping/models/stock_picking.py:8`, `addons/mrp_subcontracting_dropshipping/models/stock_rule.py:7`, `addons/mrp_subcontracting_dropshipping/models/account_move_line.py:4`, `addons/mrp_subcontracting_dropshipping/models/stock_warehouse.py:7`, `addons/mrp_subcontracting_dropshipping/models/res_company.py:7`, `addons/mrp_subcontracting_dropshipping/report/stock_traceability.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/mrp_subcontracting_dropshipping/views/purchase_order_views.xml:2`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/mrp_subcontracting_dropshipping/tests/test_purchase_subcontracting.py`, `addons/mrp_subcontracting_dropshipping/tests/test_anglo_saxon_valuation.py`, `addons/mrp_subcontracting_dropshipping/tests/test_sale_dropshipping.py`, `addons/mrp_subcontracting_dropshipping/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `view_purchase_order_inherit`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/mrp_subcontracting_dropshipping/views/purchase_order_views.xml:4`, `addons/mrp_subcontracting_dropshipping/views/purchase_order_views.xml:6`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/mrp_subcontracting_dropshipping/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 10
- Representative model evidence: inherits `stock.move` (addons/mrp_subcontracting_dropshipping/models/stock_move.py:7); inherits `purchase.order` (addons/mrp_subcontracting_dropshipping/models/purchase.py:8); inherits `stock.warehouse.orderpoint` (addons/mrp_subcontracting_dropshipping/models/stock_orderpoint.py:7); inherits `stock.replenish.mixin` (addons/mrp_subcontracting_dropshipping/models/stock_replenish_mixin.py:7); inherits `stock.picking` (addons/mrp_subcontracting_dropshipping/models/stock_picking.py:8); inherits `stock.rule` (addons/mrp_subcontracting_dropshipping/models/stock_rule.py:7); inherits `account.move.line` (addons/mrp_subcontracting_dropshipping/models/account_move_line.py:4); inherits `stock.warehouse` (addons/mrp_subcontracting_dropshipping/models/stock_warehouse.py:7); inherits `res.company` (addons/mrp_subcontracting_dropshipping/models/res_company.py:7); inherits `stock.traceability.report` (addons/mrp_subcontracting_dropshipping/report/stock_traceability.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mrp_subcontracting`, `stock_dropshipping`
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

- `addons/mrp_subcontracting_dropshipping/__init__.py`
- `addons/mrp_subcontracting_dropshipping/__manifest__.py`
- `addons/mrp_subcontracting_dropshipping/data/mrp_subcontracting_dropshipping_data.xml`
- `addons/mrp_subcontracting_dropshipping/i18n/ar.po`
- `addons/mrp_subcontracting_dropshipping/i18n/az.po`
- `addons/mrp_subcontracting_dropshipping/i18n/bg.po`
- `addons/mrp_subcontracting_dropshipping/i18n/bs.po`
- `addons/mrp_subcontracting_dropshipping/i18n/ca.po`
- `addons/mrp_subcontracting_dropshipping/i18n/cs.po`
- `addons/mrp_subcontracting_dropshipping/i18n/da.po`
- `addons/mrp_subcontracting_dropshipping/i18n/de.po`
- `addons/mrp_subcontracting_dropshipping/i18n/el.po`
- `addons/mrp_subcontracting_dropshipping/i18n/es.po`
- `addons/mrp_subcontracting_dropshipping/i18n/es_419.po`
- `addons/mrp_subcontracting_dropshipping/i18n/et.po`
- `addons/mrp_subcontracting_dropshipping/i18n/fa.po`
- `addons/mrp_subcontracting_dropshipping/i18n/fi.po`
- `addons/mrp_subcontracting_dropshipping/i18n/fr.po`
- `addons/mrp_subcontracting_dropshipping/i18n/he.po`
- `addons/mrp_subcontracting_dropshipping/i18n/hi.po`
- `addons/mrp_subcontracting_dropshipping/i18n/hr.po`
- `addons/mrp_subcontracting_dropshipping/i18n/hu.po`
- `addons/mrp_subcontracting_dropshipping/i18n/id.po`
- `addons/mrp_subcontracting_dropshipping/i18n/it.po`
- `addons/mrp_subcontracting_dropshipping/i18n/ja.po`
- `addons/mrp_subcontracting_dropshipping/i18n/kab.po`
- `addons/mrp_subcontracting_dropshipping/i18n/ko.po`
- `addons/mrp_subcontracting_dropshipping/i18n/ku.po`
- `addons/mrp_subcontracting_dropshipping/i18n/lo.po`
- `addons/mrp_subcontracting_dropshipping/i18n/lt.po`
- `addons/mrp_subcontracting_dropshipping/i18n/lv.po`
- `addons/mrp_subcontracting_dropshipping/i18n/mn.po`
- `addons/mrp_subcontracting_dropshipping/i18n/mrp_subcontracting_dropshipping.pot`
- `addons/mrp_subcontracting_dropshipping/i18n/my.po`
- `addons/mrp_subcontracting_dropshipping/i18n/nb.po`
- `addons/mrp_subcontracting_dropshipping/i18n/nl.po`
- `addons/mrp_subcontracting_dropshipping/i18n/pl.po`
- `addons/mrp_subcontracting_dropshipping/i18n/pt.po`
- `addons/mrp_subcontracting_dropshipping/i18n/pt_BR.po`
- `addons/mrp_subcontracting_dropshipping/i18n/ro.po`
- `addons/mrp_subcontracting_dropshipping/i18n/ru.po`
- `addons/mrp_subcontracting_dropshipping/i18n/sk.po`
- `addons/mrp_subcontracting_dropshipping/i18n/sl.po`
- `addons/mrp_subcontracting_dropshipping/i18n/sr@latin.po`
- `addons/mrp_subcontracting_dropshipping/i18n/sv.po`
- `addons/mrp_subcontracting_dropshipping/i18n/th.po`
- `addons/mrp_subcontracting_dropshipping/i18n/tr.po`
- `addons/mrp_subcontracting_dropshipping/i18n/uk.po`
- `addons/mrp_subcontracting_dropshipping/i18n/uz.po`
- `addons/mrp_subcontracting_dropshipping/i18n/vi.po`
- `addons/mrp_subcontracting_dropshipping/i18n/zh_CN.po`
- `addons/mrp_subcontracting_dropshipping/i18n/zh_TW.po`
- `addons/mrp_subcontracting_dropshipping/models/__init__.py`
- `addons/mrp_subcontracting_dropshipping/models/account_move_line.py`
- `addons/mrp_subcontracting_dropshipping/models/purchase.py`
- `addons/mrp_subcontracting_dropshipping/models/res_company.py`
- `addons/mrp_subcontracting_dropshipping/models/stock_move.py`
- `addons/mrp_subcontracting_dropshipping/models/stock_orderpoint.py`
- `addons/mrp_subcontracting_dropshipping/models/stock_picking.py`
- `addons/mrp_subcontracting_dropshipping/models/stock_replenish_mixin.py`
- `addons/mrp_subcontracting_dropshipping/models/stock_rule.py`
- `addons/mrp_subcontracting_dropshipping/models/stock_warehouse.py`
- `addons/mrp_subcontracting_dropshipping/report/__init__.py`
- `addons/mrp_subcontracting_dropshipping/report/stock_traceability.py`
- `addons/mrp_subcontracting_dropshipping/tests/__init__.py`
- `addons/mrp_subcontracting_dropshipping/tests/test_anglo_saxon_valuation.py`
- `addons/mrp_subcontracting_dropshipping/tests/test_purchase_subcontracting.py`
- `addons/mrp_subcontracting_dropshipping/tests/test_sale_dropshipping.py`
- `addons/mrp_subcontracting_dropshipping/views/purchase_order_views.xml`
