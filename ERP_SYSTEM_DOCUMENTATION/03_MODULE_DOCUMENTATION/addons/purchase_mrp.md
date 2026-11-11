# Module: purchase_mrp

- **Module ID:** MOD-498
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/purchase_mrp`
- **Manifest:** `addons/purchase_mrp/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Purchase`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module provides facility to the user to install mrp and purchase modules at a time.
========================================================================================

It is basically used when we want to keep track of production orders generated
from purchase order.

**Scope evidence:** The module contains 72 files, including 15 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `mrp`, `purchase_stock`.

## 2. Module structure

- Model/business logic files: 9
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 0
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/purchase_mrp/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 9 model declarations, 89 methods, 1 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/purchase_mrp/models/stock_move.py:9`, `addons/purchase_mrp/models/purchase.py:10`, `addons/purchase_mrp/models/purchase.py:47`, `addons/purchase_mrp/models/mrp_production.py:7`, `addons/purchase_mrp/models/stock_rule.py:6`, `addons/purchase_mrp/models/mrp_bom.py:8`, `addons/purchase_mrp/models/mrp_bom.py:33`, `addons/purchase_mrp/report/mrp_report_mo_overview.py:7`, `addons/purchase_mrp/report/mrp_report_bom_structure.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 5 record/template/menu identifiers.
- **Evidence:** `addons/purchase_mrp/views/mrp_bom_views.xml:3`, `addons/purchase_mrp/views/mrp_bom_views.xml:14`, `addons/purchase_mrp/views/mrp_production_views.xml:3`, `addons/purchase_mrp/views/stock_orderpoint_views.xml:3`, `addons/purchase_mrp/views/purchase_order_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/purchase_mrp/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/purchase_mrp/tests/test_replenishment.py`, `addons/purchase_mrp/tests/test_purchase_mrp_flow.py`, `addons/purchase_mrp/tests/test_anglo_saxon_valuation.py`, `addons/purchase_mrp/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `mrp_bom_form_view`, `mrp_bom_line_view_pivot`, `mrp_production_form_view_purchase`, `view_warehouse_orderpoint_tree_editable`, `purchase_order_form_mrp`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 10; representative evidence: `addons/purchase_mrp/views/mrp_bom_views.xml:5`, `addons/purchase_mrp/views/mrp_bom_views.xml:7`, `addons/purchase_mrp/views/mrp_bom_views.xml:16`, `addons/purchase_mrp/views/mrp_bom_views.xml:18`, `addons/purchase_mrp/views/mrp_production_views.xml:5`, `addons/purchase_mrp/views/mrp_production_views.xml:8`, `addons/purchase_mrp/views/stock_orderpoint_views.xml:5`, `addons/purchase_mrp/views/stock_orderpoint_views.xml:7`, `addons/purchase_mrp/views/purchase_order_views.xml:5`, `addons/purchase_mrp/views/purchase_order_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/purchase_mrp/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 9
- Representative model evidence: inherits `stock.move` (addons/purchase_mrp/models/stock_move.py:9); inherits `purchase.order` (addons/purchase_mrp/models/purchase.py:10); inherits `purchase.order.line` (addons/purchase_mrp/models/purchase.py:47); inherits `mrp.production` (addons/purchase_mrp/models/mrp_production.py:7); inherits `stock.rule` (addons/purchase_mrp/models/stock_rule.py:6); inherits `mrp.bom` (addons/purchase_mrp/models/mrp_bom.py:8); inherits `mrp.bom.line` (addons/purchase_mrp/models/mrp_bom.py:33); inherits `report.mrp.report_mo_overview` (addons/purchase_mrp/report/mrp_report_mo_overview.py:7); inherits `report.mrp.report_bom_structure` (addons/purchase_mrp/report/mrp_report_bom_structure.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mrp`, `purchase_stock`
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

- `addons/purchase_mrp/__init__.py`
- `addons/purchase_mrp/__manifest__.py`
- `addons/purchase_mrp/data/purchase_mrp_demo.xml`
- `addons/purchase_mrp/i18n/ar.po`
- `addons/purchase_mrp/i18n/az.po`
- `addons/purchase_mrp/i18n/bg.po`
- `addons/purchase_mrp/i18n/bs.po`
- `addons/purchase_mrp/i18n/ca.po`
- `addons/purchase_mrp/i18n/cs.po`
- `addons/purchase_mrp/i18n/da.po`
- `addons/purchase_mrp/i18n/de.po`
- `addons/purchase_mrp/i18n/el.po`
- `addons/purchase_mrp/i18n/es.po`
- `addons/purchase_mrp/i18n/es_419.po`
- `addons/purchase_mrp/i18n/et.po`
- `addons/purchase_mrp/i18n/fa.po`
- `addons/purchase_mrp/i18n/fi.po`
- `addons/purchase_mrp/i18n/fr.po`
- `addons/purchase_mrp/i18n/gu.po`
- `addons/purchase_mrp/i18n/he.po`
- `addons/purchase_mrp/i18n/hi.po`
- `addons/purchase_mrp/i18n/hr.po`
- `addons/purchase_mrp/i18n/hu.po`
- `addons/purchase_mrp/i18n/id.po`
- `addons/purchase_mrp/i18n/is.po`
- `addons/purchase_mrp/i18n/it.po`
- `addons/purchase_mrp/i18n/ja.po`
- `addons/purchase_mrp/i18n/kab.po`
- `addons/purchase_mrp/i18n/ko.po`
- `addons/purchase_mrp/i18n/ku.po`
- `addons/purchase_mrp/i18n/lo.po`
- `addons/purchase_mrp/i18n/lt.po`
- `addons/purchase_mrp/i18n/lv.po`
- `addons/purchase_mrp/i18n/mn.po`
- `addons/purchase_mrp/i18n/my.po`
- `addons/purchase_mrp/i18n/nb.po`
- `addons/purchase_mrp/i18n/nl.po`
- `addons/purchase_mrp/i18n/pl.po`
- `addons/purchase_mrp/i18n/pt.po`
- `addons/purchase_mrp/i18n/pt_BR.po`
- `addons/purchase_mrp/i18n/purchase_mrp.pot`
- `addons/purchase_mrp/i18n/ro.po`
- `addons/purchase_mrp/i18n/ru.po`
- `addons/purchase_mrp/i18n/sk.po`
- `addons/purchase_mrp/i18n/sl.po`
- `addons/purchase_mrp/i18n/sr@latin.po`
- `addons/purchase_mrp/i18n/sv.po`
- `addons/purchase_mrp/i18n/th.po`
- `addons/purchase_mrp/i18n/tr.po`
- `addons/purchase_mrp/i18n/uk.po`
- `addons/purchase_mrp/i18n/uz.po`
- `addons/purchase_mrp/i18n/vi.po`
- `addons/purchase_mrp/i18n/zh_CN.po`
- `addons/purchase_mrp/i18n/zh_TW.po`
- `addons/purchase_mrp/models/__init__.py`
- `addons/purchase_mrp/models/mrp_bom.py`
- `addons/purchase_mrp/models/mrp_production.py`
- `addons/purchase_mrp/models/purchase.py`
- `addons/purchase_mrp/models/stock_move.py`
- `addons/purchase_mrp/models/stock_rule.py`
- `addons/purchase_mrp/report/__init__.py`
- `addons/purchase_mrp/report/mrp_report_bom_structure.py`
- `addons/purchase_mrp/report/mrp_report_mo_overview.py`
- `addons/purchase_mrp/security/ir.access.csv`
- `addons/purchase_mrp/tests/__init__.py`
- `addons/purchase_mrp/tests/test_anglo_saxon_valuation.py`
- `addons/purchase_mrp/tests/test_purchase_mrp_flow.py`
- `addons/purchase_mrp/tests/test_replenishment.py`
- `addons/purchase_mrp/views/mrp_bom_views.xml`
- `addons/purchase_mrp/views/mrp_production_views.xml`
- `addons/purchase_mrp/views/purchase_order_views.xml`
- `addons/purchase_mrp/views/stock_orderpoint_views.xml`
