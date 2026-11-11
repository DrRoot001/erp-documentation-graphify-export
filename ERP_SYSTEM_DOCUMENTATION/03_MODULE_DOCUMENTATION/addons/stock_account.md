# Module: stock_account

- **Module ID:** MOD-560
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/stock_account`
- **Manifest:** `addons/stock_account/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Inventory`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Inventory, Logistic, Valuation, Accounting

**Manifest description:**

WMS Accounting module
======================
This module makes the link between the 'stock' and 'account' modules and allows you to create accounting entries to value your stock movements

Key Features
------------
* Stock Valuation (periodical or automatic)
* Invoice from Picking

Dashboard / Reports for Warehouse Management includes:
------------------------------------------------------
* Stock Inventory Value at given date (support dates in the past)

**Scope evidence:** The module contains 117 files, including 32 Python, 16 XML, and 4 JavaScript/TypeScript files. The manifest declares dependencies: `stock`, `account`.

## 2. Module structure

- Model/business logic files: 22
- Controller/API files: 0
- XML/data/view/template files: 16
- Browser asset files: 4
- Security files: 2
- Test files: 8
- Scheduled/automation evidence files: 2
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/stock_account/security/ir.access.csv`, `addons/stock_account/security/stock_account_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 22 model declarations, 431 methods, 1 constraint handlers, 0 onchange handlers, and 17 dependency declarations.
- **Evidence:** `addons/stock_account/models/stock_location.py:8`, `addons/stock_account/models/stock_move_line.py:4`, `addons/stock_account/models/res_groups.py:6`, `addons/stock_account/models/res_config_settings.py:4`, `addons/stock_account/models/stock_move.py:19`, `addons/stock_account/models/stock_quant.py:7`, `addons/stock_account/models/product.py:18`, `addons/stock_account/models/product.py:83`, `addons/stock_account/models/product.py:748`, `addons/stock_account/models/stock_picking_type.py:6`, `addons/stock_account/models/analytic_account.py:5`, `addons/stock_account/models/analytic_account.py:30`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 16 XML files and 4 JavaScript/TypeScript files; static XML analysis found 30 record/template/menu identifiers.
- **Evidence:** `addons/stock_account/security/stock_account_security.xml:3`, `addons/stock_account/report/stock_avco_audit_report_views.xml:2`, `addons/stock_account/report/stock_avco_audit_report_views.xml:23`, `addons/stock_account/report/account_invoice_report_view.xml:3`, `addons/stock_account/wizard/stock_inventory_adjustment_name_views.xml:3`, `addons/stock_account/views/stock_move_views.xml:3`, `addons/stock_account/views/stock_move_views.xml:11`, `addons/stock_account/views/stock_move_views.xml:19`, `addons/stock_account/views/stock_move_views.xml:36`, `addons/stock_account/views/stock_move_views.xml:48`, `addons/stock_account/views/stock_move_views.xml:60`, `addons/stock_account/views/stock_move_views.xml:81`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/stock_account/security/ir.access.csv`, `addons/stock_account/security/stock_account_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/stock_account/views/stock_move_views.xml`, `addons/stock_account/tests/test_stockvaluation.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 8 test files are present.
- **Evidence:** `addons/stock_account/tests/test_anglo_saxon_valuation_reconciliation_common.py`, `addons/stock_account/tests/test_multicompany_lot_valuation.py`, `addons/stock_account/tests/test_stockvaluationlayer.py`, `addons/stock_account/tests/common.py`, `addons/stock_account/tests/test_stockvaluation.py`, `addons/stock_account/tests/test_lot_valuation.py`, `addons/stock_account/tests/__init__.py`, `addons/stock_account/tests/test_account_move.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 16; representative identifiers: `group_lot_on_invoice`, `stock_avco_report_view_list`, `stock_avco_report_action`, `filter_invoice_inventory_valuation`, `stock_inventory_adjustment_name_form_view_inherit_stock_account`, `filter_stock_move_aging_report`, `filter_stock_move_intercompany_deliveries`, `stock_move_view_list`, `stock_move_view_pivot`, `view_move_search`, `stock_move_view_list_valuation`, `stock_move_valuation_action`, `stock_move_action_adjust_valuation`, `res_config_settings_view_form`, `stock_account_report_invoice_document`, `view_location_form_inherit`, `view_stock_quant_tree_inherit`, `view_stock_quant_tree_editable_inherit`, `view_stock_quant_tree_inventory_editable_inherit_stock_account`, `view_move_form`
- Menus: 1; representative evidence: `addons/stock_account/views/product_value_views.xml:80`
- Templates: 1; representative evidence: `addons/stock_account/views/report_invoice.xml:3`
- View/action field declarations: 46; representative evidence: `addons/stock_account/report/stock_avco_audit_report_views.xml:4`, `addons/stock_account/report/stock_avco_audit_report_views.xml:5`, `addons/stock_account/report/stock_avco_audit_report_views.xml:25`, `addons/stock_account/report/stock_avco_audit_report_views.xml:26`, `addons/stock_account/wizard/stock_inventory_adjustment_name_views.xml:5`, `addons/stock_account/wizard/stock_inventory_adjustment_name_views.xml:7`, `addons/stock_account/views/stock_move_views.xml:22`, `addons/stock_account/views/stock_move_views.xml:23`, `addons/stock_account/views/stock_move_views.xml:39`, `addons/stock_account/views/stock_move_views.xml:40`, `addons/stock_account/views/stock_move_views.xml:50`, `addons/stock_account/views/stock_move_views.xml:52`
- Browser assets: 4; representative files: `addons/stock_account/static/src/stock_valuation/stock_valuation_report.js`, `addons/stock_account/static/src/stock_account_forecasted/forecasted_header.js`, `addons/stock_account/static/src/fields/boolean_confirm.js`, `addons/stock_account/static/src/views/stock_account_move_list_view.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/stock_account/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/stock_account/views/stock_move_views.xml`, `addons/stock_account/tests/test_stockvaluation.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 22
- Representative model evidence: inherits `stock.location` (addons/stock_account/models/stock_location.py:8); inherits `stock.move.line` (addons/stock_account/models/stock_move_line.py:4); inherits `res.groups` (addons/stock_account/models/res_groups.py:6); inherits `res.config.settings` (addons/stock_account/models/res_config_settings.py:4); inherits `stock.move` (addons/stock_account/models/stock_move.py:19); inherits `stock.quant` (addons/stock_account/models/stock_quant.py:7); inherits `product.template` (addons/stock_account/models/product.py:18); inherits `product.product` (addons/stock_account/models/product.py:83); inherits `product.category` (addons/stock_account/models/product.py:748); inherits `stock.picking.type` (addons/stock_account/models/stock_picking_type.py:6); inherits `account.analytic.plan` (addons/stock_account/models/analytic_account.py:5); inherits `account.analytic.account` (addons/stock_account/models/analytic_account.py:30); inherits `stock.picking` (addons/stock_account/models/stock_picking.py:8); `product.value` (addons/stock_account/models/product_value.py:4); inherits `account.move` (addons/stock_account/models/account_move.py:4); inherits `account.move.line` (addons/stock_account/models/account_move_line.py:4); inherits `stock.lot` (addons/stock_account/models/stock_lot.py:7); inherits `res.company` (addons/stock_account/models/res_company.py:8); inherits `account.stock.valuation.report` (addons/stock_account/report/account_stock_valuation_report.py:6); `stock.avco.report` (addons/stock_account/report/stock_avco_audit_report.py:5); inherits `stock.forecasted_product_product` (addons/stock_account/report/stock_forecasted.py:8); inherits `stock.inventory.adjustment.name` (addons/stock_account/wizard/stock_inventory_adjustment_name.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `stock`, `account`
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

- `addons/stock_account/__init__.py`
- `addons/stock_account/__manifest__.py`
- `addons/stock_account/data/stock_account_data.xml`
- `addons/stock_account/i18n/af.po`
- `addons/stock_account/i18n/am.po`
- `addons/stock_account/i18n/ar.po`
- `addons/stock_account/i18n/az.po`
- `addons/stock_account/i18n/bg.po`
- `addons/stock_account/i18n/bs.po`
- `addons/stock_account/i18n/ca.po`
- `addons/stock_account/i18n/cs.po`
- `addons/stock_account/i18n/da.po`
- `addons/stock_account/i18n/de.po`
- `addons/stock_account/i18n/el.po`
- `addons/stock_account/i18n/es.po`
- `addons/stock_account/i18n/es_419.po`
- `addons/stock_account/i18n/es_CL.po`
- `addons/stock_account/i18n/et.po`
- `addons/stock_account/i18n/eu.po`
- `addons/stock_account/i18n/fa.po`
- `addons/stock_account/i18n/fi.po`
- `addons/stock_account/i18n/fo.po`
- `addons/stock_account/i18n/fr.po`
- `addons/stock_account/i18n/fr_BE.po`
- `addons/stock_account/i18n/fr_CA.po`
- `addons/stock_account/i18n/gl.po`
- `addons/stock_account/i18n/gu.po`
- `addons/stock_account/i18n/he.po`
- `addons/stock_account/i18n/hi.po`
- `addons/stock_account/i18n/hr.po`
- `addons/stock_account/i18n/hu.po`
- `addons/stock_account/i18n/id.po`
- `addons/stock_account/i18n/is.po`
- `addons/stock_account/i18n/it.po`
- `addons/stock_account/i18n/ja.po`
- `addons/stock_account/i18n/ka.po`
- `addons/stock_account/i18n/kab.po`
- `addons/stock_account/i18n/km.po`
- `addons/stock_account/i18n/ko.po`
- `addons/stock_account/i18n/ku.po`
- `addons/stock_account/i18n/lo.po`
- `addons/stock_account/i18n/lt.po`
- `addons/stock_account/i18n/lv.po`
- `addons/stock_account/i18n/mk.po`
- `addons/stock_account/i18n/mn.po`
- `addons/stock_account/i18n/my.po`
- `addons/stock_account/i18n/nb.po`
- `addons/stock_account/i18n/nl.po`
- `addons/stock_account/i18n/pl.po`
- `addons/stock_account/i18n/pt.po`
- `addons/stock_account/i18n/pt_BR.po`
- `addons/stock_account/i18n/ro.po`
- `addons/stock_account/i18n/ru.po`
- `addons/stock_account/i18n/sk.po`
- `addons/stock_account/i18n/sl.po`
- `addons/stock_account/i18n/sq.po`
- `addons/stock_account/i18n/sr@latin.po`
- `addons/stock_account/i18n/stock_account.pot`
- `addons/stock_account/i18n/sv.po`
- `addons/stock_account/i18n/ta.po`
- `addons/stock_account/i18n/th.po`
- `addons/stock_account/i18n/tr.po`
- `addons/stock_account/i18n/uk.po`
- `addons/stock_account/i18n/uz.po`
- `addons/stock_account/i18n/vi.po`
- `addons/stock_account/i18n/zh_CN.po`
- `addons/stock_account/i18n/zh_TW.po`
- `addons/stock_account/models/__init__.py`
- `addons/stock_account/models/account_move.py`
- `addons/stock_account/models/account_move_line.py`
- `addons/stock_account/models/analytic_account.py`
- `addons/stock_account/models/product.py`
- `addons/stock_account/models/product_value.py`
- `addons/stock_account/models/res_company.py`
- `addons/stock_account/models/res_config_settings.py`
- `addons/stock_account/models/res_groups.py`
- `addons/stock_account/models/stock_location.py`
- `addons/stock_account/models/stock_lot.py`
- `addons/stock_account/models/stock_move.py`
- `addons/stock_account/models/stock_move_line.py`
- `addons/stock_account/models/stock_picking.py`
- `addons/stock_account/models/stock_picking_type.py`
- `addons/stock_account/models/stock_quant.py`
- `addons/stock_account/report/__init__.py`
- `addons/stock_account/report/account_invoice_report_view.xml`
- `addons/stock_account/report/account_stock_valuation_report.py`
- `addons/stock_account/report/stock_avco_audit_report.py`
- `addons/stock_account/report/stock_avco_audit_report_views.xml`
- `addons/stock_account/report/stock_forecasted.py`
- `addons/stock_account/security/ir.access.csv`
- `addons/stock_account/security/stock_account_security.xml`
- `addons/stock_account/static/src/fields/boolean_confirm.js`
- `addons/stock_account/static/src/fields/boolean_confirm.xml`
- `addons/stock_account/static/src/stock_account_forecasted/forecasted_header.js`
- `addons/stock_account/static/src/stock_account_forecasted/forecasted_header.xml`
- `addons/stock_account/static/src/stock_valuation/stock_valuation_report.js`
- `addons/stock_account/static/src/views/stock_account_move_list_view.js`
- `addons/stock_account/tests/__init__.py`
- `addons/stock_account/tests/common.py`
- `addons/stock_account/tests/test_account_move.py`
- `addons/stock_account/tests/test_anglo_saxon_valuation_reconciliation_common.py`
- `addons/stock_account/tests/test_lot_valuation.py`
- `addons/stock_account/tests/test_multicompany_lot_valuation.py`
- `addons/stock_account/tests/test_stockvaluation.py`
- `addons/stock_account/tests/test_stockvaluationlayer.py`
- `addons/stock_account/views/account_move_views.xml`
- `addons/stock_account/views/product_value_views.xml`
- `addons/stock_account/views/product_views.xml`
- `addons/stock_account/views/report_invoice.xml`
- `addons/stock_account/views/res_config_settings_views.xml`
- `addons/stock_account/views/stock_location_views.xml`
- `addons/stock_account/views/stock_lot_views.xml`
- `addons/stock_account/views/stock_move_views.xml`
- `addons/stock_account/views/stock_quant_views.xml`
- `addons/stock_account/wizard/__init__.py`
- `addons/stock_account/wizard/stock_inventory_adjustment_name.py`
- `addons/stock_account/wizard/stock_inventory_adjustment_name_views.xml`
