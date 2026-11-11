# Module: sale_mrp

- **Module ID:** MOD-520
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_mrp`
- **Manifest:** `addons/sale_mrp/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module provides facility to the user to install mrp and sales modulesat a time.
====================================================================================

It is basically used when we want to keep track of production orders generated
from sales order. It adds sales name and sales Reference on production order.

**Scope evidence:** The module contains 83 files, including 20 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `mrp`, `sale_stock`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 2
- XML/data/view/template files: 3
- Browser asset files: 0
- Security files: 1
- Test files: 8
- Scheduled/automation evidence files: 0
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/sale_mrp/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 120 methods, 0 constraint handlers, 2 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/sale_mrp/models/sale_order.py:7`, `addons/sale_mrp/models/stock_move.py:6`, `addons/sale_mrp/models/stock_orderpoint.py:4`, `addons/sale_mrp/models/mrp_production.py:7`, `addons/sale_mrp/models/stock_rule.py:4`, `addons/sale_mrp/models/mrp_bom.py:10`, `addons/sale_mrp/models/sale_order_line.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/sale_mrp/controllers/portal.py`, `addons/sale_mrp/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/sale_mrp/views/sale_portal_templates.xml:4`, `addons/sale_mrp/views/sale_order_views.xml:4`, `addons/sale_mrp/views/mrp_production_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/sale_mrp/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/sale_mrp/tests/test_sale_mrp_report.py`, `addons/sale_mrp/tests/test_sale_mrp_kit_bom.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 8 test files are present.
- **Evidence:** `addons/sale_mrp/tests/test_sale_mrp_lead_time.py`, `addons/sale_mrp/tests/test_multistep_manufacturing.py`, `addons/sale_mrp/tests/test_sale_mrp_flow.py`, `addons/sale_mrp/tests/test_sale_mrp_anglo_saxon_valuation.py`, `addons/sale_mrp/tests/test_sale_mrp_procurement.py`, `addons/sale_mrp/tests/test_sale_mrp_report.py`, `addons/sale_mrp/tests/__init__.py`, `addons/sale_mrp/tests/test_sale_mrp_kit_bom.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `Orders MOs`, `sale_order_form_mrp`, `mrp_production_form_view_sale`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/sale_mrp/views/sale_portal_templates.xml:4`
- View/action field declarations: 4; representative evidence: `addons/sale_mrp/views/sale_order_views.xml:6`, `addons/sale_mrp/views/sale_order_views.xml:8`, `addons/sale_mrp/views/mrp_production_views.xml:5`, `addons/sale_mrp/views/mrp_production_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale_mrp/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/sale_mrp/tests/test_sale_mrp_report.py`, `addons/sale_mrp/tests/test_sale_mrp_kit_bom.py`

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: inherits `sale.order` (addons/sale_mrp/models/sale_order.py:7); inherits `stock.move` (addons/sale_mrp/models/stock_move.py:6); inherits `stock.warehouse.orderpoint` (addons/sale_mrp/models/stock_orderpoint.py:4); inherits `mrp.production` (addons/sale_mrp/models/mrp_production.py:7); inherits `stock.rule` (addons/sale_mrp/models/stock_rule.py:4); inherits `mrp.bom` (addons/sale_mrp/models/mrp_bom.py:10); inherits `sale.order.line` (addons/sale_mrp/models/sale_order_line.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mrp`, `sale_stock`
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

- `addons/sale_mrp/__init__.py`
- `addons/sale_mrp/__manifest__.py`
- `addons/sale_mrp/controllers/__init__.py`
- `addons/sale_mrp/controllers/portal.py`
- `addons/sale_mrp/i18n/am.po`
- `addons/sale_mrp/i18n/ar.po`
- `addons/sale_mrp/i18n/az.po`
- `addons/sale_mrp/i18n/bg.po`
- `addons/sale_mrp/i18n/bs.po`
- `addons/sale_mrp/i18n/ca.po`
- `addons/sale_mrp/i18n/cs.po`
- `addons/sale_mrp/i18n/da.po`
- `addons/sale_mrp/i18n/de.po`
- `addons/sale_mrp/i18n/el.po`
- `addons/sale_mrp/i18n/es.po`
- `addons/sale_mrp/i18n/es_419.po`
- `addons/sale_mrp/i18n/es_CL.po`
- `addons/sale_mrp/i18n/et.po`
- `addons/sale_mrp/i18n/eu.po`
- `addons/sale_mrp/i18n/fa.po`
- `addons/sale_mrp/i18n/fi.po`
- `addons/sale_mrp/i18n/fo.po`
- `addons/sale_mrp/i18n/fr.po`
- `addons/sale_mrp/i18n/fr_BE.po`
- `addons/sale_mrp/i18n/gl.po`
- `addons/sale_mrp/i18n/gu.po`
- `addons/sale_mrp/i18n/he.po`
- `addons/sale_mrp/i18n/hi.po`
- `addons/sale_mrp/i18n/hr.po`
- `addons/sale_mrp/i18n/hu.po`
- `addons/sale_mrp/i18n/id.po`
- `addons/sale_mrp/i18n/is.po`
- `addons/sale_mrp/i18n/it.po`
- `addons/sale_mrp/i18n/ja.po`
- `addons/sale_mrp/i18n/ka.po`
- `addons/sale_mrp/i18n/kab.po`
- `addons/sale_mrp/i18n/ko.po`
- `addons/sale_mrp/i18n/ku.po`
- `addons/sale_mrp/i18n/lo.po`
- `addons/sale_mrp/i18n/lt.po`
- `addons/sale_mrp/i18n/lv.po`
- `addons/sale_mrp/i18n/mk.po`
- `addons/sale_mrp/i18n/mn.po`
- `addons/sale_mrp/i18n/my.po`
- `addons/sale_mrp/i18n/nb.po`
- `addons/sale_mrp/i18n/nl.po`
- `addons/sale_mrp/i18n/pl.po`
- `addons/sale_mrp/i18n/pt.po`
- `addons/sale_mrp/i18n/pt_BR.po`
- `addons/sale_mrp/i18n/ro.po`
- `addons/sale_mrp/i18n/ru.po`
- `addons/sale_mrp/i18n/sale_mrp.pot`
- `addons/sale_mrp/i18n/sk.po`
- `addons/sale_mrp/i18n/sl.po`
- `addons/sale_mrp/i18n/sr@latin.po`
- `addons/sale_mrp/i18n/sv.po`
- `addons/sale_mrp/i18n/th.po`
- `addons/sale_mrp/i18n/tr.po`
- `addons/sale_mrp/i18n/uk.po`
- `addons/sale_mrp/i18n/uz.po`
- `addons/sale_mrp/i18n/vi.po`
- `addons/sale_mrp/i18n/zh_CN.po`
- `addons/sale_mrp/i18n/zh_TW.po`
- `addons/sale_mrp/models/__init__.py`
- `addons/sale_mrp/models/mrp_bom.py`
- `addons/sale_mrp/models/mrp_production.py`
- `addons/sale_mrp/models/sale_order.py`
- `addons/sale_mrp/models/sale_order_line.py`
- `addons/sale_mrp/models/stock_move.py`
- `addons/sale_mrp/models/stock_orderpoint.py`
- `addons/sale_mrp/models/stock_rule.py`
- `addons/sale_mrp/security/ir.access.csv`
- `addons/sale_mrp/tests/__init__.py`
- `addons/sale_mrp/tests/test_multistep_manufacturing.py`
- `addons/sale_mrp/tests/test_sale_mrp_anglo_saxon_valuation.py`
- `addons/sale_mrp/tests/test_sale_mrp_flow.py`
- `addons/sale_mrp/tests/test_sale_mrp_kit_bom.py`
- `addons/sale_mrp/tests/test_sale_mrp_lead_time.py`
- `addons/sale_mrp/tests/test_sale_mrp_procurement.py`
- `addons/sale_mrp/tests/test_sale_mrp_report.py`
- `addons/sale_mrp/views/mrp_production_views.xml`
- `addons/sale_mrp/views/sale_order_views.xml`
- `addons/sale_mrp/views/sale_portal_templates.xml`
