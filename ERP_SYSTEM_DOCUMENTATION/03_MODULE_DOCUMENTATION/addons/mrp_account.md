# Module: mrp_account

- **Module ID:** MOD-378
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/mrp_account`
- **Manifest:** `addons/mrp_account/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Manufacturing`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Analytic accounting in Manufacturing

**Manifest description:**

Analytic Accounting in MRP
==========================

* Cost structure report

Also, allows to compute the cost of the product based on its BoM, using the costs of its components and work center operations.
It adds a button on the product itself but also an action in the list view of the products.
If the automated inventory valuation is active, the necessary accounting entries will be created.

**Scope evidence:** The module contains 98 files, including 24 Python, 13 XML, and 4 JavaScript/TypeScript files. The manifest declares dependencies: `mrp`, `stock_account`.

## 2. Module structure

- Model/business logic files: 20
- Controller/API files: 0
- XML/data/view/template files: 13
- Browser asset files: 4
- Security files: 1
- Test files: 6
- Scheduled/automation evidence files: 1
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/mrp_account/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 20 model declarations, 127 methods, 0 constraint handlers, 0 onchange handlers, and 10 dependency declarations.
- **Evidence:** `addons/mrp_account/models/stock_move.py:9`, `addons/mrp_account/models/product.py:7`, `addons/mrp_account/models/product.py:39`, `addons/mrp_account/models/product.py:121`, `addons/mrp_account/models/mrp_workcenter.py:7`, `addons/mrp_account/models/mrp_workcenter.py:23`, `addons/mrp_account/models/analytic_account.py:7`, `addons/mrp_account/models/analytic_account.py:76`, `addons/mrp_account/models/analytic_account.py:82`, `addons/mrp_account/models/mrp_workorder.py:7`, `addons/mrp_account/models/mrp_production.py:11`, `addons/mrp_account/models/account_move.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 13 XML files and 4 JavaScript/TypeScript files; static XML analysis found 18 record/template/menu identifiers.
- **Evidence:** `addons/mrp_account/report/report_mrp_templates.xml:71`, `addons/mrp_account/report/report_mrp_templates.xml:4`, `addons/mrp_account/report/mrp_report_mo_overview.xml:3`, `addons/mrp_account/wizard/mrp_wip_accounting.xml:4`, `addons/mrp_account/wizard/mrp_wip_accounting.xml:37`, `addons/mrp_account/data/mrp_account_demo.xml:4`, `addons/mrp_account/data/mrp_account_demo.xml:15`, `addons/mrp_account/views/mrp_workcenter_views.xml:3`, `addons/mrp_account/views/mrp_bom_views.xml:3`, `addons/mrp_account/views/account_move_views.xml:2`, `addons/mrp_account/views/mrp_production_views.xml:2`, `addons/mrp_account/views/mrp_production_views.xml:22`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/mrp_account/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/mrp_account/views/product_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/mrp_account/report/report_mrp_templates.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 6 test files are present.
- **Evidence:** `addons/mrp_account/tests/test_valuation_operation.py`, `addons/mrp_account/tests/common.py`, `addons/mrp_account/tests/__init__.py`, `addons/mrp_account/tests/test_analytic_account.py`, `addons/mrp_account/tests/test_valuation_layers.py`, `addons/mrp_account/tests/test_mrp_account.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 13; representative identifiers: `wip_report`, `mrp_account.report_wip`, `mrp_account.mo_overview_components`, `view_wip_accounting_form`, `action_wip_accounting`, `mrp_production_drawer_2`, `mrp_production_drawer_3`, `mrp_workcenter_view_inherit`, `mrp_account_inherits_mrp_bom_form_view`, `view_move_form_inherit_mrp_account`, `mrp_production_form_view_inherited`, `view_production_graph_inherit_mrp_account`, `view_production_pivot_inherit_mrp_account`, `product_product_ext_form_view2`, `product_product_view_form_normal_inherit_extended`, `action_compute_price_bom_template`, `action_compute_price_bom_product`, `account_analytic_account_view_form_mrp`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/mrp_account/report/report_mrp_templates.xml:4`, `addons/mrp_account/report/mrp_report_mo_overview.xml:3`
- View/action field declarations: 23; representative evidence: `addons/mrp_account/report/report_mrp_templates.xml:73`, `addons/mrp_account/wizard/mrp_wip_accounting.xml:6`, `addons/mrp_account/wizard/mrp_wip_accounting.xml:7`, `addons/mrp_account/wizard/mrp_wip_accounting.xml:39`, `addons/mrp_account/wizard/mrp_wip_accounting.xml:40`, `addons/mrp_account/views/mrp_workcenter_views.xml:5`, `addons/mrp_account/views/mrp_workcenter_views.xml:7`, `addons/mrp_account/views/mrp_bom_views.xml:5`, `addons/mrp_account/views/mrp_bom_views.xml:7`, `addons/mrp_account/views/account_move_views.xml:4`, `addons/mrp_account/views/account_move_views.xml:6`, `addons/mrp_account/views/mrp_production_views.xml:4`
- Browser assets: 4; representative files: `addons/mrp_account/static/src/stock_valuation/controller.js`, `addons/mrp_account/static/src/stock_valuation/stock_valuation_report.js`, `addons/mrp_account/static/src/components/mo_overview_extra_bom_cost_line/mo_overview_extra_bom_cost_line.js`, `addons/mrp_account/static/src/components/bom_overview_extra_bom_cost_line/bom_overview_extra_bom_cost_line.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/mrp_account/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/mrp_account/views/product_views.xml`
- **Report entry points:** `addons/mrp_account/report/report_mrp_templates.xml`

## 7. Database interactions

- Model declarations: 20
- Representative model evidence: inherits `stock.move` (addons/mrp_account/models/stock_move.py:9); inherits `product.template` (addons/mrp_account/models/product.py:7); inherits `product.product` (addons/mrp_account/models/product.py:39); inherits `product.category` (addons/mrp_account/models/product.py:121); `mrp.workcenter` (addons/mrp_account/models/mrp_workcenter.py:7); inherits `mrp.workcenter.productivity` (addons/mrp_account/models/mrp_workcenter.py:23); inherits `account.analytic.account` (addons/mrp_account/models/analytic_account.py:7); inherits `account.analytic.line` (addons/mrp_account/models/analytic_account.py:76); inherits `account.analytic.applicability` (addons/mrp_account/models/analytic_account.py:82); inherits `mrp.workorder` (addons/mrp_account/models/mrp_workorder.py:7); `mrp.production` (addons/mrp_account/models/mrp_production.py:11); inherits `account.move` (addons/mrp_account/models/account_move.py:8); inherits `account.move.line` (addons/mrp_account/models/account_move.py:48); inherits `mrp.bom` (addons/mrp_account/models/mrp_bom.py:4); inherits `res.company` (addons/mrp_account/models/res_company.py:5); inherits `account.stock.valuation.report` (addons/mrp_account/report/stock_valuation_report.py:6); inherits `report.mrp.report_mo_overview` (addons/mrp_account/report/mrp_report_mo_overview.py:7); inherits `report.mrp.report_bom_structure` (addons/mrp_account/report/mrp_report_bom_structure.py:4); `mrp.account.wip.accounting.line` (addons/mrp_account/wizard/mrp_wip_accounting.py:9); `mrp.account.wip.accounting` (addons/mrp_account/wizard/mrp_wip_accounting.py:38)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mrp`, `stock_account`
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

- `addons/mrp_account/__init__.py`
- `addons/mrp_account/__manifest__.py`
- `addons/mrp_account/data/mrp_account_demo.xml`
- `addons/mrp_account/i18n/ar.po`
- `addons/mrp_account/i18n/az.po`
- `addons/mrp_account/i18n/bg.po`
- `addons/mrp_account/i18n/bs.po`
- `addons/mrp_account/i18n/ca.po`
- `addons/mrp_account/i18n/cs.po`
- `addons/mrp_account/i18n/da.po`
- `addons/mrp_account/i18n/de.po`
- `addons/mrp_account/i18n/el.po`
- `addons/mrp_account/i18n/es.po`
- `addons/mrp_account/i18n/es_419.po`
- `addons/mrp_account/i18n/es_CL.po`
- `addons/mrp_account/i18n/et.po`
- `addons/mrp_account/i18n/eu.po`
- `addons/mrp_account/i18n/fa.po`
- `addons/mrp_account/i18n/fi.po`
- `addons/mrp_account/i18n/fr.po`
- `addons/mrp_account/i18n/gl.po`
- `addons/mrp_account/i18n/gu.po`
- `addons/mrp_account/i18n/he.po`
- `addons/mrp_account/i18n/hi.po`
- `addons/mrp_account/i18n/hr.po`
- `addons/mrp_account/i18n/hu.po`
- `addons/mrp_account/i18n/id.po`
- `addons/mrp_account/i18n/is.po`
- `addons/mrp_account/i18n/it.po`
- `addons/mrp_account/i18n/ja.po`
- `addons/mrp_account/i18n/kab.po`
- `addons/mrp_account/i18n/km.po`
- `addons/mrp_account/i18n/ko.po`
- `addons/mrp_account/i18n/ku.po`
- `addons/mrp_account/i18n/lo.po`
- `addons/mrp_account/i18n/lt.po`
- `addons/mrp_account/i18n/lv.po`
- `addons/mrp_account/i18n/mk.po`
- `addons/mrp_account/i18n/mn.po`
- `addons/mrp_account/i18n/mrp_account.pot`
- `addons/mrp_account/i18n/my.po`
- `addons/mrp_account/i18n/nb.po`
- `addons/mrp_account/i18n/nl.po`
- `addons/mrp_account/i18n/pl.po`
- `addons/mrp_account/i18n/pt.po`
- `addons/mrp_account/i18n/pt_BR.po`
- `addons/mrp_account/i18n/ro.po`
- `addons/mrp_account/i18n/ru.po`
- `addons/mrp_account/i18n/sk.po`
- `addons/mrp_account/i18n/sl.po`
- `addons/mrp_account/i18n/sr@latin.po`
- `addons/mrp_account/i18n/sv.po`
- `addons/mrp_account/i18n/th.po`
- `addons/mrp_account/i18n/tr.po`
- `addons/mrp_account/i18n/uk.po`
- `addons/mrp_account/i18n/uz.po`
- `addons/mrp_account/i18n/vi.po`
- `addons/mrp_account/i18n/zh_CN.po`
- `addons/mrp_account/i18n/zh_TW.po`
- `addons/mrp_account/models/__init__.py`
- `addons/mrp_account/models/account_move.py`
- `addons/mrp_account/models/analytic_account.py`
- `addons/mrp_account/models/mrp_bom.py`
- `addons/mrp_account/models/mrp_production.py`
- `addons/mrp_account/models/mrp_workcenter.py`
- `addons/mrp_account/models/mrp_workorder.py`
- `addons/mrp_account/models/product.py`
- `addons/mrp_account/models/res_company.py`
- `addons/mrp_account/models/stock_move.py`
- `addons/mrp_account/report/__init__.py`
- `addons/mrp_account/report/mrp_report_bom_structure.py`
- `addons/mrp_account/report/mrp_report_mo_overview.py`
- `addons/mrp_account/report/mrp_report_mo_overview.xml`
- `addons/mrp_account/report/report_mrp_templates.xml`
- `addons/mrp_account/report/stock_valuation_report.py`
- `addons/mrp_account/security/ir.access.csv`
- `addons/mrp_account/static/src/components/bom_overview_extra_bom_cost_line/bom_overview_extra_bom_cost_line.js`
- `addons/mrp_account/static/src/components/bom_overview_extra_bom_cost_line/bom_overview_extra_bom_cost_line.xml`
- `addons/mrp_account/static/src/components/mo_overview_extra_bom_cost_line/mo_overview_extra_bom_cost_line.js`
- `addons/mrp_account/static/src/components/mo_overview_extra_bom_cost_line/mo_overview_extra_bom_cost_line.xml`
- `addons/mrp_account/static/src/stock_valuation/controller.js`
- `addons/mrp_account/static/src/stock_valuation/stock_valuation_report.js`
- `addons/mrp_account/static/src/stock_valuation/stock_valuation_report.xml`
- `addons/mrp_account/tests/__init__.py`
- `addons/mrp_account/tests/common.py`
- `addons/mrp_account/tests/test_analytic_account.py`
- `addons/mrp_account/tests/test_mrp_account.py`
- `addons/mrp_account/tests/test_valuation_layers.py`
- `addons/mrp_account/tests/test_valuation_operation.py`
- `addons/mrp_account/views/account_move_views.xml`
- `addons/mrp_account/views/analytic_account_views.xml`
- `addons/mrp_account/views/mrp_bom_views.xml`
- `addons/mrp_account/views/mrp_production_views.xml`
- `addons/mrp_account/views/mrp_workcenter_views.xml`
- `addons/mrp_account/views/product_views.xml`
- `addons/mrp_account/wizard/__init__.py`
- `addons/mrp_account/wizard/mrp_wip_accounting.py`
- `addons/mrp_account/wizard/mrp_wip_accounting.xml`
