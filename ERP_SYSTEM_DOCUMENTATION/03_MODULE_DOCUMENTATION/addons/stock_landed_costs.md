# Module: stock_landed_costs

- **Module ID:** MOD-564
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/stock_landed_costs`
- **Manifest:** `addons/stock_landed_costs/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Inventory`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Landed Costs

**Manifest description:**

Landed Costs Management
=======================
This module allows you to easily add extra costs on pickings and decide the split of these costs among their stock moves in order to take them into account in your stock valuation.

**Scope evidence:** The module contains 91 files, including 18 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `stock_account`, `purchase_stock`.

## 2. Module structure

- Model/business logic files: 10
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 0
- Security files: 1
- Test files: 8
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/stock_landed_costs/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 10 model declarations, 104 methods, 0 constraint handlers, 4 onchange handlers, and 7 dependency declarations.
- **Evidence:** `addons/stock_landed_costs/models/res_config_settings.py:7`, `addons/stock_landed_costs/models/stock_landed_cost.py:19`, `addons/stock_landed_costs/models/stock_landed_cost.py:300`, `addons/stock_landed_costs/models/stock_landed_cost.py:342`, `addons/stock_landed_costs/models/stock_move.py:4`, `addons/stock_landed_costs/models/purchase.py:4`, `addons/stock_landed_costs/models/product.py:9`, `addons/stock_landed_costs/models/account_move.py:7`, `addons/stock_landed_costs/models/account_move.py:63`, `addons/stock_landed_costs/models/res_company.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 12 record/template/menu identifiers.
- **Evidence:** `addons/stock_landed_costs/data/stock_landed_cost_data.xml:5`, `addons/stock_landed_costs/data/stock_landed_cost_data.xml:11`, `addons/stock_landed_costs/views/res_config_settings_views.xml:4`, `addons/stock_landed_costs/views/account_move_views.xml:3`, `addons/stock_landed_costs/views/stock_landed_cost_views.xml:5`, `addons/stock_landed_costs/views/stock_landed_cost_views.xml:123`, `addons/stock_landed_costs/views/stock_landed_cost_views.xml:137`, `addons/stock_landed_costs/views/stock_landed_cost_views.xml:153`, `addons/stock_landed_costs/views/stock_landed_cost_views.xml:178`, `addons/stock_landed_costs/views/stock_landed_cost_views.xml:209`, `addons/stock_landed_costs/views/stock_landed_cost_views.xml:224`, `addons/stock_landed_costs/views/product_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/stock_landed_costs/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 8 test files are present.
- **Evidence:** `addons/stock_landed_costs/tests/test_stock_landed_costs.py`, `addons/stock_landed_costs/tests/test_stock_landed_costs_branches.py`, `addons/stock_landed_costs/tests/test_stockvaluationlayer.py`, `addons/stock_landed_costs/tests/test_stock_landed_costs_rounding.py`, `addons/stock_landed_costs/tests/common.py`, `addons/stock_landed_costs/tests/test_stock_landed_costs_purchase.py`, `addons/stock_landed_costs/tests/__init__.py`, `addons/stock_landed_costs/tests/test_stock_landed_costs_lots.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `mt_stock_landed_cost_open`, `seq_stock_landed_costs`, `res_config_settings_view_form`, `account_view_move_form_inherited`, `view_stock_landed_cost_form`, `view_stock_landed_cost_tree`, `view_stock_landed_cost_tree2`, `stock_landed_cost_view_kanban`, `view_stock_landed_cost_search`, `action_stock_landed_cost`, `menu_stock_landed_cost`, `view_product_landed_cost_form`
- Menus: 1; representative evidence: `addons/stock_landed_costs/views/stock_landed_cost_views.xml:224`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 19; representative evidence: `addons/stock_landed_costs/data/stock_landed_cost_data.xml:7`, `addons/stock_landed_costs/views/res_config_settings_views.xml:6`, `addons/stock_landed_costs/views/res_config_settings_views.xml:8`, `addons/stock_landed_costs/views/account_move_views.xml:5`, `addons/stock_landed_costs/views/account_move_views.xml:7`, `addons/stock_landed_costs/views/stock_landed_cost_views.xml:7`, `addons/stock_landed_costs/views/stock_landed_cost_views.xml:8`, `addons/stock_landed_costs/views/stock_landed_cost_views.xml:125`, `addons/stock_landed_costs/views/stock_landed_cost_views.xml:126`, `addons/stock_landed_costs/views/stock_landed_cost_views.xml:139`, `addons/stock_landed_costs/views/stock_landed_cost_views.xml:141`, `addons/stock_landed_costs/views/stock_landed_cost_views.xml:155`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/stock_landed_costs/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 10
- Representative model evidence: inherits `res.config.settings` (addons/stock_landed_costs/models/res_config_settings.py:7); `stock.landed.cost` (addons/stock_landed_costs/models/stock_landed_cost.py:19); `stock.landed.cost.lines` (addons/stock_landed_costs/models/stock_landed_cost.py:300); `stock.valuation.adjustment.lines` (addons/stock_landed_costs/models/stock_landed_cost.py:342); inherits `stock.move` (addons/stock_landed_costs/models/stock_move.py:4); inherits `purchase.order.line` (addons/stock_landed_costs/models/purchase.py:4); inherits `product.template` (addons/stock_landed_costs/models/product.py:9); inherits `account.move` (addons/stock_landed_costs/models/account_move.py:7); inherits `account.move.line` (addons/stock_landed_costs/models/account_move.py:63); inherits `res.company` (addons/stock_landed_costs/models/res_company.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `stock_account`, `purchase_stock`
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

- `addons/stock_landed_costs/__init__.py`
- `addons/stock_landed_costs/__manifest__.py`
- `addons/stock_landed_costs/data/stock_landed_cost_data.xml`
- `addons/stock_landed_costs/i18n/af.po`
- `addons/stock_landed_costs/i18n/am.po`
- `addons/stock_landed_costs/i18n/ar.po`
- `addons/stock_landed_costs/i18n/az.po`
- `addons/stock_landed_costs/i18n/bg.po`
- `addons/stock_landed_costs/i18n/bs.po`
- `addons/stock_landed_costs/i18n/ca.po`
- `addons/stock_landed_costs/i18n/cs.po`
- `addons/stock_landed_costs/i18n/da.po`
- `addons/stock_landed_costs/i18n/de.po`
- `addons/stock_landed_costs/i18n/el.po`
- `addons/stock_landed_costs/i18n/es.po`
- `addons/stock_landed_costs/i18n/es_419.po`
- `addons/stock_landed_costs/i18n/es_CL.po`
- `addons/stock_landed_costs/i18n/et.po`
- `addons/stock_landed_costs/i18n/eu.po`
- `addons/stock_landed_costs/i18n/fa.po`
- `addons/stock_landed_costs/i18n/fi.po`
- `addons/stock_landed_costs/i18n/fo.po`
- `addons/stock_landed_costs/i18n/fr.po`
- `addons/stock_landed_costs/i18n/fr_BE.po`
- `addons/stock_landed_costs/i18n/fr_CA.po`
- `addons/stock_landed_costs/i18n/gl.po`
- `addons/stock_landed_costs/i18n/gu.po`
- `addons/stock_landed_costs/i18n/he.po`
- `addons/stock_landed_costs/i18n/hi.po`
- `addons/stock_landed_costs/i18n/hr.po`
- `addons/stock_landed_costs/i18n/hu.po`
- `addons/stock_landed_costs/i18n/hy.po`
- `addons/stock_landed_costs/i18n/id.po`
- `addons/stock_landed_costs/i18n/is.po`
- `addons/stock_landed_costs/i18n/it.po`
- `addons/stock_landed_costs/i18n/ja.po`
- `addons/stock_landed_costs/i18n/ka.po`
- `addons/stock_landed_costs/i18n/kab.po`
- `addons/stock_landed_costs/i18n/kk.po`
- `addons/stock_landed_costs/i18n/km.po`
- `addons/stock_landed_costs/i18n/ko.po`
- `addons/stock_landed_costs/i18n/ku.po`
- `addons/stock_landed_costs/i18n/lo.po`
- `addons/stock_landed_costs/i18n/lt.po`
- `addons/stock_landed_costs/i18n/lv.po`
- `addons/stock_landed_costs/i18n/mk.po`
- `addons/stock_landed_costs/i18n/mn.po`
- `addons/stock_landed_costs/i18n/my.po`
- `addons/stock_landed_costs/i18n/nb.po`
- `addons/stock_landed_costs/i18n/nl.po`
- `addons/stock_landed_costs/i18n/pl.po`
- `addons/stock_landed_costs/i18n/pt.po`
- `addons/stock_landed_costs/i18n/pt_BR.po`
- `addons/stock_landed_costs/i18n/ro.po`
- `addons/stock_landed_costs/i18n/ru.po`
- `addons/stock_landed_costs/i18n/sk.po`
- `addons/stock_landed_costs/i18n/sl.po`
- `addons/stock_landed_costs/i18n/sq.po`
- `addons/stock_landed_costs/i18n/sr@latin.po`
- `addons/stock_landed_costs/i18n/stock_landed_costs.pot`
- `addons/stock_landed_costs/i18n/sv.po`
- `addons/stock_landed_costs/i18n/ta.po`
- `addons/stock_landed_costs/i18n/te.po`
- `addons/stock_landed_costs/i18n/th.po`
- `addons/stock_landed_costs/i18n/tr.po`
- `addons/stock_landed_costs/i18n/uk.po`
- `addons/stock_landed_costs/i18n/uz.po`
- `addons/stock_landed_costs/i18n/vi.po`
- `addons/stock_landed_costs/i18n/zh_CN.po`
- `addons/stock_landed_costs/i18n/zh_TW.po`
- `addons/stock_landed_costs/models/__init__.py`
- `addons/stock_landed_costs/models/account_move.py`
- `addons/stock_landed_costs/models/product.py`
- `addons/stock_landed_costs/models/purchase.py`
- `addons/stock_landed_costs/models/res_company.py`
- `addons/stock_landed_costs/models/res_config_settings.py`
- `addons/stock_landed_costs/models/stock_landed_cost.py`
- `addons/stock_landed_costs/models/stock_move.py`
- `addons/stock_landed_costs/security/ir.access.csv`
- `addons/stock_landed_costs/tests/__init__.py`
- `addons/stock_landed_costs/tests/common.py`
- `addons/stock_landed_costs/tests/test_stock_landed_costs.py`
- `addons/stock_landed_costs/tests/test_stock_landed_costs_branches.py`
- `addons/stock_landed_costs/tests/test_stock_landed_costs_lots.py`
- `addons/stock_landed_costs/tests/test_stock_landed_costs_purchase.py`
- `addons/stock_landed_costs/tests/test_stock_landed_costs_rounding.py`
- `addons/stock_landed_costs/tests/test_stockvaluationlayer.py`
- `addons/stock_landed_costs/views/account_move_views.xml`
- `addons/stock_landed_costs/views/product_views.xml`
- `addons/stock_landed_costs/views/res_config_settings_views.xml`
- `addons/stock_landed_costs/views/stock_landed_cost_views.xml`
