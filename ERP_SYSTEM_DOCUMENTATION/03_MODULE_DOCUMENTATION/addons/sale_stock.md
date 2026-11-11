# Module: sale_stock

- **Module ID:** MOD-533
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_stock`
- **Manifest:** `addons/sale_stock/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Quotation, Sales Orders, Delivery & Invoicing Control

**Manifest description:**

Manage sales quotations and orders
==================================

This module makes the link between the sales and warehouses management applications.

Preferences
-----------
* Shipping: Choice of delivery at once or partial delivery
* Invoicing: choose how invoices will be paid
* Incoterms: International Commercial terms

**Scope evidence:** The module contains 132 files, including 40 Python, 24 XML, and 6 JavaScript/TypeScript files. The manifest declares dependencies: `sale`, `stock_account`.

## 2. Module structure

- Model/business logic files: 21
- Controller/API files: 3
- XML/data/view/template files: 24
- Browser asset files: 6
- Security files: 1
- Test files: 17
- Scheduled/automation evidence files: 1
- Reporting evidence files: 4

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/sale_stock/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 21 model declarations, 322 methods, 1 constraint handlers, 2 onchange handlers, and 26 dependency declarations.
- **Evidence:** `addons/sale_stock/models/sale_order.py:16`, `addons/sale_stock/models/product_template.py:7`, `addons/sale_stock/models/res_config_settings.py:7`, `addons/sale_stock/models/stock.py:10`, `addons/sale_stock/models/stock.py:15`, `addons/sale_stock/models/stock.py:242`, `addons/sale_stock/models/stock.py:249`, `addons/sale_stock/models/stock.py:258`, `addons/sale_stock/models/stock.py:411`, `addons/sale_stock/models/res_users.py:6`, `addons/sale_stock/models/account_move.py:9`, `addons/sale_stock/models/account_move.py:121`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 3 route declarations.
- **Evidence:** `addons/sale_stock/controllers/portal.py:36`, `addons/sale_stock/controllers/return_order.py:16`, `addons/sale_stock/controllers/return_order.py:66`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 24 XML files and 6 JavaScript/TypeScript files; static XML analysis found 59 record/template/menu identifiers.
- **Evidence:** `addons/sale_stock/report/stock_report_deliveryslip.xml:3`, `addons/sale_stock/report/return_label.xml:94`, `addons/sale_stock/report/return_label.xml:2`, `addons/sale_stock/wizard/stock_rules_report_views.xml:3`, `addons/sale_stock/wizard/stock_replenishment_info.xml:3`, `addons/sale_stock/data/sale_stock_data.xml:4`, `addons/sale_stock/data/return_reason_data.xml:4`, `addons/sale_stock/data/return_reason_data.xml:8`, `addons/sale_stock/data/return_reason_data.xml:12`, `addons/sale_stock/data/return_reason_data.xml:16`, `addons/sale_stock/data/return_reason_data.xml:20`, `addons/sale_stock/data/sale_order_demo.xml:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/sale_stock/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/sale_stock/views/sale_order_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 4 files contain report-action/template indicators.
- **Evidence:** `addons/sale_stock/controllers/portal.py`, `addons/sale_stock/controllers/return_order.py`, `addons/sale_stock/report/return_label.xml`, `addons/sale_stock/tests/test_sale_stock_report.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 17 test files are present.
- **Evidence:** `addons/sale_stock/tests/test_sale_stock_report.py`, `addons/sale_stock/tests/test_sale_stock_lead_time.py`, `addons/sale_stock/tests/test_sale_stock_accrued_entries.py`, `addons/sale_stock/tests/test_anglo_saxon_valuation_reconciliation.py`, `addons/sale_stock/tests/test_anglosaxon_account.py`, `addons/sale_stock/tests/test_create_perf.py`, `addons/sale_stock/tests/test_sale_stock_access_rights.py`, `addons/sale_stock/tests/test_return_order.py`, `addons/sale_stock/tests/test_analytic_to_sale_stock.py`, `addons/sale_stock/tests/test_sale_stock_multicompany.py`, `addons/sale_stock/tests/test_packaging_tours.py`, `addons/sale_stock/tests/common.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 24; representative identifiers: `report_delivery_document_inherit_sale_stock`, `action_report_return_label`, `return_label`, `view_stock_rules_report_sale`, `view_stock_replenishment_info_sale_stock_inherit`, `stock.route_warehouse0_mto`, `return_reason_wrong_item`, `return_reason_damaged_product`, `return_reason_not_meeting_expectations`, `return_reason_incorrect_specs`, `return_reason_order_by_mistake`, `sale.sale_order_1`, `sale.sale_order_2`, `sale.sale_order_3`, `sale.sale_order_5`, `sale.sale_order_6`, `sale.sale_order_8`, `sale_order_19`, `sale_order_line_42`, `sale_order_line_43`
- Menus: 1; representative evidence: `addons/sale_stock/views/stock_picking_views.xml:94`
- Templates: 8; representative evidence: `addons/sale_stock/report/stock_report_deliveryslip.xml:3`, `addons/sale_stock/report/return_label.xml:2`, `addons/sale_stock/data/mail_templates.xml:4`, `addons/sale_stock/data/mail_templates.xml:38`, `addons/sale_stock/views/sale_stock_portal_template.xml:4`, `addons/sale_stock/views/sale_stock_portal_template.xml:33`, `addons/sale_stock/views/stock_picking_views.xml:4`, `addons/sale_stock/static/src/widgets/qty_at_date_widget.xml:2`
- View/action field declarations: 45; representative evidence: `addons/sale_stock/report/return_label.xml:96`, `addons/sale_stock/wizard/stock_rules_report_views.xml:5`, `addons/sale_stock/wizard/stock_rules_report_views.xml:7`, `addons/sale_stock/wizard/stock_replenishment_info.xml:5`, `addons/sale_stock/wizard/stock_replenishment_info.xml:7`, `addons/sale_stock/views/stock_route_views.xml:6`, `addons/sale_stock/views/stock_route_views.xml:8`, `addons/sale_stock/views/sale_order_line_views.xml:7`, `addons/sale_stock/views/sale_order_line_views.xml:8`, `addons/sale_stock/views/stock_picking_views.xml:22`, `addons/sale_stock/views/stock_picking_views.xml:24`, `addons/sale_stock/views/stock_picking_views.xml:48`
- Browser assets: 6; representative files: `addons/sale_stock/static/src/widgets/qty_at_date_widget.js`, `addons/sale_stock/static/src/product_catalog/kanban_record.js`, `addons/sale_stock/static/src/return_order_dialog/return_order_dialog.js`, `addons/sale_stock/static/src/interactions/return_order.js`, `addons/sale_stock/static/src/product_catalog/sale_order_line/sale_order_line.js`, `addons/sale_stock/static/tests/tours/barcode_duplication_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale_stock/__manifest__.py`
- **HTTP entry points:** `addons/sale_stock/controllers/portal.py:36`, `addons/sale_stock/controllers/return_order.py:16`, `addons/sale_stock/controllers/return_order.py:66`
- **Scheduled entry points:** `addons/sale_stock/views/sale_order_views.xml`
- **Report entry points:** `addons/sale_stock/controllers/portal.py`, `addons/sale_stock/controllers/return_order.py`, `addons/sale_stock/report/return_label.xml`, `addons/sale_stock/tests/test_sale_stock_report.py`

## 7. Database interactions

- Model declarations: 21
- Representative model evidence: inherits `sale.order` (addons/sale_stock/models/sale_order.py:16); inherits `product.template` (addons/sale_stock/models/product_template.py:7); inherits `res.config.settings` (addons/sale_stock/models/res_config_settings.py:7); inherits `stock.route` (addons/sale_stock/models/stock.py:10); inherits `stock.move` (addons/sale_stock/models/stock.py:15); inherits `stock.move.line` (addons/sale_stock/models/stock.py:242); inherits `stock.rule` (addons/sale_stock/models/stock.py:249); inherits `stock.picking` (addons/sale_stock/models/stock.py:258); inherits `stock.lot` (addons/sale_stock/models/stock.py:411); inherits `res.users` (addons/sale_stock/models/res_users.py:6); inherits `account.move` (addons/sale_stock/models/account_move.py:9); inherits `account.move.line` (addons/sale_stock/models/account_move.py:121); `return.reason` (addons/sale_stock/models/return_reason.py:6); inherits `sale.order.line` (addons/sale_stock/models/sale_order_line.py:12); inherits `stock.reference` (addons/sale_stock/models/stock_reference.py:4); inherits `res.company` (addons/sale_stock/models/res_company.py:7); inherits `report.stock.report_stock_rule` (addons/sale_stock/report/report_stock_rule.py:7); inherits `stock.forecasted_product_product` (addons/sale_stock/report/stock_forecasted.py:7); inherits `sale.report` (addons/sale_stock/report/sale_report.py:6); inherits `stock.replenishment.info` (addons/sale_stock/wizard/stock_replenishment_info.py:4); inherits `stock.rules.report` (addons/sale_stock/wizard/stock_rules_report.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 3
- Route evidence: `addons/sale_stock/controllers/portal.py:36`, `addons/sale_stock/controllers/return_order.py:16`, `addons/sale_stock/controllers/return_order.py:66`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale`, `stock_account`
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

- `addons/sale_stock/__init__.py`
- `addons/sale_stock/__manifest__.py`
- `addons/sale_stock/controllers/__init__.py`
- `addons/sale_stock/controllers/portal.py`
- `addons/sale_stock/controllers/return_order.py`
- `addons/sale_stock/data/mail_templates.xml`
- `addons/sale_stock/data/return_reason_data.xml`
- `addons/sale_stock/data/sale_order_demo.xml`
- `addons/sale_stock/data/sale_stock_data.xml`
- `addons/sale_stock/i18n/af.po`
- `addons/sale_stock/i18n/am.po`
- `addons/sale_stock/i18n/ar.po`
- `addons/sale_stock/i18n/az.po`
- `addons/sale_stock/i18n/bg.po`
- `addons/sale_stock/i18n/bs.po`
- `addons/sale_stock/i18n/ca.po`
- `addons/sale_stock/i18n/cs.po`
- `addons/sale_stock/i18n/da.po`
- `addons/sale_stock/i18n/de.po`
- `addons/sale_stock/i18n/el.po`
- `addons/sale_stock/i18n/es.po`
- `addons/sale_stock/i18n/es_419.po`
- `addons/sale_stock/i18n/es_CL.po`
- `addons/sale_stock/i18n/et.po`
- `addons/sale_stock/i18n/eu.po`
- `addons/sale_stock/i18n/fa.po`
- `addons/sale_stock/i18n/fi.po`
- `addons/sale_stock/i18n/fo.po`
- `addons/sale_stock/i18n/fr.po`
- `addons/sale_stock/i18n/fr_CA.po`
- `addons/sale_stock/i18n/gl.po`
- `addons/sale_stock/i18n/gu.po`
- `addons/sale_stock/i18n/he.po`
- `addons/sale_stock/i18n/hi.po`
- `addons/sale_stock/i18n/hr.po`
- `addons/sale_stock/i18n/hu.po`
- `addons/sale_stock/i18n/id.po`
- `addons/sale_stock/i18n/is.po`
- `addons/sale_stock/i18n/it.po`
- `addons/sale_stock/i18n/ja.po`
- `addons/sale_stock/i18n/kab.po`
- `addons/sale_stock/i18n/km.po`
- `addons/sale_stock/i18n/ko.po`
- `addons/sale_stock/i18n/ku.po`
- `addons/sale_stock/i18n/lo.po`
- `addons/sale_stock/i18n/lt.po`
- `addons/sale_stock/i18n/lv.po`
- `addons/sale_stock/i18n/mk.po`
- `addons/sale_stock/i18n/mn.po`
- `addons/sale_stock/i18n/my.po`
- `addons/sale_stock/i18n/nb.po`
- `addons/sale_stock/i18n/nl.po`
- `addons/sale_stock/i18n/pl.po`
- `addons/sale_stock/i18n/pt.po`
- `addons/sale_stock/i18n/pt_BR.po`
- `addons/sale_stock/i18n/ro.po`
- `addons/sale_stock/i18n/ru.po`
- `addons/sale_stock/i18n/sale_stock.pot`
- `addons/sale_stock/i18n/sk.po`
- `addons/sale_stock/i18n/sl.po`
- `addons/sale_stock/i18n/sr@latin.po`
- `addons/sale_stock/i18n/sv.po`
- `addons/sale_stock/i18n/th.po`
- `addons/sale_stock/i18n/tr.po`
- `addons/sale_stock/i18n/uk.po`
- `addons/sale_stock/i18n/uz.po`
- `addons/sale_stock/i18n/vi.po`
- `addons/sale_stock/i18n/zh_CN.po`
- `addons/sale_stock/i18n/zh_TW.po`
- `addons/sale_stock/models/__init__.py`
- `addons/sale_stock/models/account_move.py`
- `addons/sale_stock/models/product_template.py`
- `addons/sale_stock/models/res_company.py`
- `addons/sale_stock/models/res_config_settings.py`
- `addons/sale_stock/models/res_users.py`
- `addons/sale_stock/models/return_reason.py`
- `addons/sale_stock/models/sale_order.py`
- `addons/sale_stock/models/sale_order_line.py`
- `addons/sale_stock/models/stock.py`
- `addons/sale_stock/models/stock_reference.py`
- `addons/sale_stock/report/__init__.py`
- `addons/sale_stock/report/report_stock_rule.py`
- `addons/sale_stock/report/return_label.xml`
- `addons/sale_stock/report/sale_report.py`
- `addons/sale_stock/report/stock_forecasted.py`
- `addons/sale_stock/report/stock_report_deliveryslip.xml`
- `addons/sale_stock/security/ir.access.csv`
- `addons/sale_stock/static/src/interactions/return_order.js`
- `addons/sale_stock/static/src/product_catalog/kanban_record.js`
- `addons/sale_stock/static/src/product_catalog/sale_order_line/sale_order_line.js`
- `addons/sale_stock/static/src/return_order_dialog/return_label_info.xml`
- `addons/sale_stock/static/src/return_order_dialog/return_order_dialog.js`
- `addons/sale_stock/static/src/return_order_dialog/return_order_dialog.scss`
- `addons/sale_stock/static/src/return_order_dialog/return_order_dialog.xml`
- `addons/sale_stock/static/src/sale_stock_forecasted/forecasted_details.xml`
- `addons/sale_stock/static/src/widgets/qty_at_date_widget.js`
- `addons/sale_stock/static/src/widgets/qty_at_date_widget.xml`
- `addons/sale_stock/static/src/xml/delay_alert.xml`
- `addons/sale_stock/static/tests/tours/barcode_duplication_tour.js`
- `addons/sale_stock/tests/__init__.py`
- `addons/sale_stock/tests/common.py`
- `addons/sale_stock/tests/test_analytic_to_sale_stock.py`
- `addons/sale_stock/tests/test_anglo_saxon_valuation.py`
- `addons/sale_stock/tests/test_anglo_saxon_valuation_reconciliation.py`
- `addons/sale_stock/tests/test_anglosaxon_account.py`
- `addons/sale_stock/tests/test_create_perf.py`
- `addons/sale_stock/tests/test_packaging_tours.py`
- `addons/sale_stock/tests/test_return_order.py`
- `addons/sale_stock/tests/test_sale_order_dates.py`
- `addons/sale_stock/tests/test_sale_stock.py`
- `addons/sale_stock/tests/test_sale_stock_access_rights.py`
- `addons/sale_stock/tests/test_sale_stock_accrued_entries.py`
- `addons/sale_stock/tests/test_sale_stock_lead_time.py`
- `addons/sale_stock/tests/test_sale_stock_multi_warehouse.py`
- `addons/sale_stock/tests/test_sale_stock_multicompany.py`
- `addons/sale_stock/tests/test_sale_stock_report.py`
- `addons/sale_stock/views/product_views.xml`
- `addons/sale_stock/views/res_config_settings_views.xml`
- `addons/sale_stock/views/res_users_views.xml`
- `addons/sale_stock/views/return_reason_views.xml`
- `addons/sale_stock/views/sale_order_line_views.xml`
- `addons/sale_stock/views/sale_order_views.xml`
- `addons/sale_stock/views/sale_stock_portal_template.xml`
- `addons/sale_stock/views/stock_lot_views.xml`
- `addons/sale_stock/views/stock_picking_views.xml`
- `addons/sale_stock/views/stock_reference_views.xml`
- `addons/sale_stock/views/stock_route_views.xml`
- `addons/sale_stock/wizard/__init__.py`
- `addons/sale_stock/wizard/stock_replenishment_info.py`
- `addons/sale_stock/wizard/stock_replenishment_info.xml`
- `addons/sale_stock/wizard/stock_rules_report.py`
- `addons/sale_stock/wizard/stock_rules_report_views.xml`
