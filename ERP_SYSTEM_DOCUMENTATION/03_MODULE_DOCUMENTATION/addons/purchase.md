# Module: purchase

- **Module ID:** MOD-493
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/purchase`
- **Manifest:** `addons/purchase/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Supply Chain/Purchase`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Purchase orders, tenders and agreements

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 168 files, including 38 Python, 33 XML, and 21 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 21
- Controller/API files: 2
- XML/data/view/template files: 33
- Browser asset files: 21
- Security files: 2
- Test files: 13
- Scheduled/automation evidence files: 5
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/purchase/security/ir.access.csv`, `addons/purchase/security/purchase_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 21 model declarations, 401 methods, 1 constraint handlers, 12 onchange handlers, and 59 dependency declarations.
- **Evidence:** `addons/purchase/models/product_category.py:6`, `addons/purchase/models/res_partner.py:7`, `addons/purchase/models/purchase_order.py:21`, `addons/purchase/models/res_groups.py:6`, `addons/purchase/models/purchase_order_line.py:13`, `addons/purchase/models/res_config_settings.py:7`, `addons/purchase/models/ir_actions_report.py:7`, `addons/purchase/models/product.py:10`, `addons/purchase/models/product.py:73`, `addons/purchase/models/product.py:276`, `addons/purchase/models/account_tax.py:4`, `addons/purchase/models/purchase_bill_line_match.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 5 route declarations.
- **Evidence:** `addons/purchase/controllers/portal.py:105`, `addons/purchase/controllers/portal.py:119`, `addons/purchase/controllers/portal.py:137`, `addons/purchase/controllers/portal.py:160`, `addons/purchase/controllers/portal.py:190`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 33 XML files and 21 JavaScript/TypeScript files; static XML analysis found 140 record/template/menu identifiers.
- **Evidence:** `addons/purchase/security/purchase_security.xml:4`, `addons/purchase/security/purchase_security.xml:10`, `addons/purchase/security/purchase_security.xml:17`, `addons/purchase/security/purchase_security.xml:25`, `addons/purchase/security/purchase_security.xml:29`, `addons/purchase/security/purchase_security.xml:35`, `addons/purchase/report/purchase_reports.xml:4`, `addons/purchase/report/purchase_reports.xml:16`, `addons/purchase/report/purchase_quotation_templates.xml:3`, `addons/purchase/report/purchase_quotation_templates.xml:89`, `addons/purchase/report/purchase_report_views.xml:3`, `addons/purchase/report/purchase_report_views.xml:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/purchase/security/ir.access.csv`, `addons/purchase/security/purchase_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 5 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/purchase/__manifest__.py`, `addons/purchase/data/purchase_data.xml`, `addons/purchase/data/ir_cron_data.xml`, `addons/purchase/views/purchase_bill_line_match_views.xml`, `addons/purchase/views/purchase_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/purchase/models/ir_actions_report.py`, `addons/purchase/report/purchase_reports.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 13 test files are present.
- **Evidence:** `addons/purchase/tests/test_purchase.py`, `addons/purchase/tests/test_access_rights.py`, `addons/purchase/tests/test_purchase_flow.py`, `addons/purchase/tests/test_purchase_downpayment.py`, `addons/purchase/tests/test_import_files.py`, `addons/purchase/tests/test_purchase_dashboard.py`, `addons/purchase/tests/test_purchase_invoice.py`, `addons/purchase/tests/test_purchase_order_product_catalog.py`, `addons/purchase/tests/test_purchase_product_catalog.py`, `addons/purchase/tests/test_accrued_purchase_orders.py`, `addons/purchase/tests/__init__.py`, `addons/purchase/tests/test_purchase_order_tax_mode.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 33; representative identifiers: `res_groups_privilege_purchase`, `group_purchase_user`, `group_purchase_manager`, `group_warning_purchase`, `group_send_reminder`, `base.group_user`, `action_report_purchase_order`, `report_purchase_quotation`, `report_purchasequotation_document`, `report_purchasequotation`, `view_purchase_order_pivot`, `view_purchase_order_graph`, `purchase_report_view_tree`, `view_purchase_order_search`, `action_purchase_order_report_all`, `Reporting`, `Purchase`, `report_purchaseorder_document`, `report_purchaseorder`, `document_tax_totals`
- Menus: 16; representative evidence: `addons/purchase/report/purchase_report_views.xml:108`, `addons/purchase/report/purchase_report_views.xml:109`, `addons/purchase/views/res_config_settings_views.xml:81`, `addons/purchase/views/purchase_views.xml:5`, `addons/purchase/views/purchase_views.xml:11`, `addons/purchase/views/purchase_views.xml:15`, `addons/purchase/views/purchase_views.xml:19`, `addons/purchase/views/purchase_views.xml:21`, `addons/purchase/views/purchase_views.xml:25`, `addons/purchase/views/purchase_views.xml:33`, `addons/purchase/views/purchase_views.xml:37`, `addons/purchase/views/purchase_views.xml:41`
- Templates: 14; representative evidence: `addons/purchase/report/purchase_quotation_templates.xml:3`, `addons/purchase/report/purchase_quotation_templates.xml:89`, `addons/purchase/report/purchase_order_templates.xml:3`, `addons/purchase/report/purchase_order_templates.xml:146`, `addons/purchase/report/purchase_order_templates.xml:155`, `addons/purchase/data/mail_templates.xml:4`, `addons/purchase/data/mail_templates.xml:37`, `addons/purchase/views/portal_templates.xml:4`, `addons/purchase/views/portal_templates.xml:20`, `addons/purchase/views/portal_templates.xml:50`, `addons/purchase/views/portal_templates.xml:94`, `addons/purchase/views/portal_templates.xml:185`
- View/action field declarations: 122; representative evidence: `addons/purchase/report/purchase_reports.xml:6`, `addons/purchase/report/purchase_reports.xml:18`, `addons/purchase/report/purchase_report_views.xml:5`, `addons/purchase/report/purchase_report_views.xml:6`, `addons/purchase/report/purchase_report_views.xml:17`, `addons/purchase/report/purchase_report_views.xml:18`, `addons/purchase/report/purchase_report_views.xml:28`, `addons/purchase/report/purchase_report_views.xml:29`, `addons/purchase/report/purchase_report_views.xml:51`, `addons/purchase/report/purchase_report_views.xml:52`, `addons/purchase/report/purchase_report_views.xml:90`, `addons/purchase/report/purchase_report_views.xml:92`
- Browser assets: 21; representative files: `addons/purchase/static/src/toaster_button/toaster_button_widget.js`, `addons/purchase/static/src/product_catalog/kanban_renderer.js`, `addons/purchase/static/src/product_catalog/kanban_record.js`, `addons/purchase/static/src/product_catalog/kanban_view.js`, `addons/purchase/static/src/interactions/purchase_datetimepicker.js`, `addons/purchase/static/src/interactions/purchase_sidebar.js`, `addons/purchase/static/src/views/purchase_kanbanview.js`, `addons/purchase/static/src/views/purchase_dashboard.js`, `addons/purchase/static/src/views/purchase_listview.js`, `addons/purchase/static/src/js/tours/purchase_steps.js`, `addons/purchase/static/src/js/tours/purchase.js`, `addons/purchase/static/src/product_catalog/purchase_order_line/purchase_order_line.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/purchase/__manifest__.py`
- **HTTP entry points:** `addons/purchase/controllers/portal.py:105`, `addons/purchase/controllers/portal.py:119`, `addons/purchase/controllers/portal.py:137`, `addons/purchase/controllers/portal.py:160`, `addons/purchase/controllers/portal.py:190`
- **Scheduled entry points:** `addons/purchase/__manifest__.py`, `addons/purchase/data/purchase_data.xml`, `addons/purchase/data/ir_cron_data.xml`, `addons/purchase/views/purchase_bill_line_match_views.xml`, `addons/purchase/views/purchase_views.xml`
- **Report entry points:** `addons/purchase/models/ir_actions_report.py`, `addons/purchase/report/purchase_reports.xml`

## 7. Database interactions

- Model declarations: 21
- Representative model evidence: inherits `product.category` (addons/purchase/models/product_category.py:6); inherits `res.partner` (addons/purchase/models/res_partner.py:7); `purchase.order` (addons/purchase/models/purchase_order.py:21); inherits `res.groups` (addons/purchase/models/res_groups.py:6); `purchase.order.line` (addons/purchase/models/purchase_order_line.py:13); inherits `res.config.settings` (addons/purchase/models/res_config_settings.py:7); inherits `ir.actions.report` (addons/purchase/models/ir_actions_report.py:7); inherits `product.template` (addons/purchase/models/product.py:10); inherits `product.product` (addons/purchase/models/product.py:73); inherits `product.supplierinfo` (addons/purchase/models/product.py:276); inherits `account.tax` (addons/purchase/models/account_tax.py:4); `purchase.bill.line.match` (addons/purchase/models/purchase_bill_line_match.py:9); inherits `account.analytic.account` (addons/purchase/models/analytic_account.py:7); inherits `account.move` (addons/purchase/models/account_invoice.py:17); inherits `account.move.line` (addons/purchase/models/account_invoice.py:658); inherits `account.analytic.applicability` (addons/purchase/models/analytic_applicability.py:6); inherits `res.company` (addons/purchase/models/res_company.py:10); `purchase.report` (addons/purchase/report/purchase_report.py:12); `purchase.bill.union` (addons/purchase/report/purchase_bill.py:7); inherits `account.accrued.orders.wizard` (addons/purchase/wizard/accrued_orders.py:9); `bill.to.po.wizard` (addons/purchase/wizard/bill_to_po_wizard.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 5
- Route evidence: `addons/purchase/controllers/portal.py:105`, `addons/purchase/controllers/portal.py:119`, `addons/purchase/controllers/portal.py:137`, `addons/purchase/controllers/portal.py:160`, `addons/purchase/controllers/portal.py:190`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`
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

- `addons/purchase/README.md`
- `addons/purchase/__init__.py`
- `addons/purchase/__manifest__.py`
- `addons/purchase/controllers/__init__.py`
- `addons/purchase/controllers/portal.py`
- `addons/purchase/data/digest_data.xml`
- `addons/purchase/data/ir_cron_data.xml`
- `addons/purchase/data/mail_template_data.xml`
- `addons/purchase/data/mail_templates.xml`
- `addons/purchase/data/portal_entry_data.xml`
- `addons/purchase/data/purchase_data.xml`
- `addons/purchase/data/purchase_demo.xml`
- `addons/purchase/data/purchase_tour.xml`
- `addons/purchase/i18n/af.po`
- `addons/purchase/i18n/am.po`
- `addons/purchase/i18n/ar.po`
- `addons/purchase/i18n/az.po`
- `addons/purchase/i18n/bg.po`
- `addons/purchase/i18n/bs.po`
- `addons/purchase/i18n/ca.po`
- `addons/purchase/i18n/cs.po`
- `addons/purchase/i18n/da.po`
- `addons/purchase/i18n/de.po`
- `addons/purchase/i18n/el.po`
- `addons/purchase/i18n/en_AU.po`
- `addons/purchase/i18n/es.po`
- `addons/purchase/i18n/es_419.po`
- `addons/purchase/i18n/es_CL.po`
- `addons/purchase/i18n/et.po`
- `addons/purchase/i18n/eu.po`
- `addons/purchase/i18n/fa.po`
- `addons/purchase/i18n/fi.po`
- `addons/purchase/i18n/fo.po`
- `addons/purchase/i18n/fr.po`
- `addons/purchase/i18n/fr_CA.po`
- `addons/purchase/i18n/gl.po`
- `addons/purchase/i18n/gu.po`
- `addons/purchase/i18n/he.po`
- `addons/purchase/i18n/hi.po`
- `addons/purchase/i18n/hr.po`
- `addons/purchase/i18n/hu.po`
- `addons/purchase/i18n/id.po`
- `addons/purchase/i18n/is.po`
- `addons/purchase/i18n/it.po`
- `addons/purchase/i18n/ja.po`
- `addons/purchase/i18n/ka.po`
- `addons/purchase/i18n/kab.po`
- `addons/purchase/i18n/km.po`
- `addons/purchase/i18n/ko.po`
- `addons/purchase/i18n/ku.po`
- `addons/purchase/i18n/lb.po`
- `addons/purchase/i18n/lo.po`
- `addons/purchase/i18n/lt.po`
- `addons/purchase/i18n/lv.po`
- `addons/purchase/i18n/mk.po`
- `addons/purchase/i18n/mn.po`
- `addons/purchase/i18n/my.po`
- `addons/purchase/i18n/nb.po`
- `addons/purchase/i18n/nl.po`
- `addons/purchase/i18n/pl.po`
- `addons/purchase/i18n/pt.po`
- `addons/purchase/i18n/pt_BR.po`
- `addons/purchase/i18n/purchase.pot`
- `addons/purchase/i18n/ro.po`
- `addons/purchase/i18n/ru.po`
- `addons/purchase/i18n/sk.po`
- `addons/purchase/i18n/sl.po`
- `addons/purchase/i18n/sq.po`
- `addons/purchase/i18n/sr@latin.po`
- `addons/purchase/i18n/sv.po`
- `addons/purchase/i18n/th.po`
- `addons/purchase/i18n/tr.po`
- `addons/purchase/i18n/uk.po`
- `addons/purchase/i18n/uz.po`
- `addons/purchase/i18n/vi.po`
- `addons/purchase/i18n/zh_CN.po`
- `addons/purchase/i18n/zh_TW.po`
- `addons/purchase/models/__init__.py`
- `addons/purchase/models/account_invoice.py`
- `addons/purchase/models/account_tax.py`
- `addons/purchase/models/analytic_account.py`
- `addons/purchase/models/analytic_applicability.py`
- `addons/purchase/models/ir_actions_report.py`
- `addons/purchase/models/product.py`
- `addons/purchase/models/product_category.py`
- `addons/purchase/models/purchase_bill_line_match.py`
- `addons/purchase/models/purchase_order.py`
- `addons/purchase/models/purchase_order_line.py`
- `addons/purchase/models/res_company.py`
- `addons/purchase/models/res_config_settings.py`
- `addons/purchase/models/res_groups.py`
- `addons/purchase/models/res_partner.py`
- `addons/purchase/report/__init__.py`
- `addons/purchase/report/purchase_bill.py`
- `addons/purchase/report/purchase_bill_views.xml`
- `addons/purchase/report/purchase_order_templates.xml`
- `addons/purchase/report/purchase_quotation_templates.xml`
- `addons/purchase/report/purchase_report.py`
- `addons/purchase/report/purchase_report_views.xml`
- `addons/purchase/report/purchase_reports.xml`
- `addons/purchase/security/ir.access.csv`
- `addons/purchase/security/purchase_security.xml`
- `addons/purchase/static/description/icon.png`
- `addons/purchase/static/description/icon.svg`
- `addons/purchase/static/description/icon_hi.png`
- `addons/purchase/static/src/components/matching_tag/matching_tag.js`
- `addons/purchase/static/src/components/matching_tag/matching_tag.xml`
- `addons/purchase/static/src/components/monetary_field_no_zero/monetary_field_no_zero.js`
- `addons/purchase/static/src/components/open_match_line_widget/open_match_line_widget.js`
- `addons/purchase/static/src/components/open_match_line_widget/open_match_line_widget.xml`
- `addons/purchase/static/src/components/purchase_file_uploader/purchase_file_uploader.js`
- `addons/purchase/static/src/components/purchase_file_uploader/purchase_file_uploader.xml`
- `addons/purchase/static/src/components/purchase_line_match_field/purchase_line_match_field.js`
- `addons/purchase/static/src/components/purchase_line_match_field/purchase_line_match_field.xml`
- `addons/purchase/static/src/components/tax_totals/tax_totals.xml`
- `addons/purchase/static/src/img/calculator.svg`
- `addons/purchase/static/src/img/milk-OTDPurchase.gif`
- `addons/purchase/static/src/interactions/purchase_datetimepicker.js`
- `addons/purchase/static/src/interactions/purchase_sidebar.js`
- `addons/purchase/static/src/js/tours/purchase.js`
- `addons/purchase/static/src/js/tours/purchase_steps.js`
- `addons/purchase/static/src/product_catalog/kanban_record.js`
- `addons/purchase/static/src/product_catalog/kanban_renderer.js`
- `addons/purchase/static/src/product_catalog/kanban_renderer.xml`
- `addons/purchase/static/src/product_catalog/kanban_view.js`
- `addons/purchase/static/src/product_catalog/purchase_order_line/purchase_order_line.js`
- `addons/purchase/static/src/scss/purchase_portal.scss`
- `addons/purchase/static/src/toaster_button/toaster_button_widget.js`
- `addons/purchase/static/src/toaster_button/toaster_button_widget.xml`
- `addons/purchase/static/src/views/purchase_dashboard.js`
- `addons/purchase/static/src/views/purchase_dashboard.scss`
- `addons/purchase/static/src/views/purchase_dashboard.xml`
- `addons/purchase/static/src/views/purchase_kanbanview.js`
- `addons/purchase/static/src/views/purchase_kanbanview.xml`
- `addons/purchase/static/src/views/purchase_listview.js`
- `addons/purchase/static/src/views/purchase_listview.xml`
- `addons/purchase/static/tests/tours/purchase_catalog.js`
- `addons/purchase/static/tests/tours/purchase_flow_tour.js`
- `addons/purchase/static/tests/tours/purchase_order_duplicate_section_test_tour.js`
- `addons/purchase/static/tests/tours/tour_helper.js`
- `addons/purchase/static/xls/product_purchase.xls`
- `addons/purchase/static/xls/products_import_template.xlsx`
- `addons/purchase/static/xls/requests_for_quotation_import_template.xlsx`
- `addons/purchase/tests/__init__.py`
- `addons/purchase/tests/test_access_rights.py`
- `addons/purchase/tests/test_accrued_purchase_orders.py`
- `addons/purchase/tests/test_import_files.py`
- `addons/purchase/tests/test_purchase.py`
- `addons/purchase/tests/test_purchase_dashboard.py`
- `addons/purchase/tests/test_purchase_downpayment.py`
- `addons/purchase/tests/test_purchase_flow.py`
- `addons/purchase/tests/test_purchase_invoice.py`
- `addons/purchase/tests/test_purchase_order_product_catalog.py`
- `addons/purchase/tests/test_purchase_order_report.py`
- `addons/purchase/tests/test_purchase_order_tax_mode.py`
- `addons/purchase/tests/test_purchase_product_catalog.py`
- `addons/purchase/views/account_move_views.xml`
- `addons/purchase/views/analytic_account_views.xml`
- `addons/purchase/views/portal_templates.xml`
- `addons/purchase/views/product_views.xml`
- `addons/purchase/views/purchase_bill_line_match_views.xml`
- `addons/purchase/views/purchase_views.xml`
- `addons/purchase/views/res_config_settings_views.xml`
- `addons/purchase/views/res_partner_views.xml`
- `addons/purchase/wizard/__init__.py`
- `addons/purchase/wizard/accrued_orders.py`
- `addons/purchase/wizard/bill_to_po_wizard.py`
- `addons/purchase/wizard/bill_to_po_wizard_views.xml`
