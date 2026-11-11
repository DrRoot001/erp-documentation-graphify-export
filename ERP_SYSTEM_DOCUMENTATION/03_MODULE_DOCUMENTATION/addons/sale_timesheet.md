# Module: sale_timesheet

- **Module ID:** MOD-536
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_timesheet`
- **Manifest:** `addons/sale_timesheet/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Sell based on timesheets

**Manifest description:**

Allows to sell timesheets in your sales order
=============================================

This module set the right product on all timesheet lines
according to the order/contract you work on. This allows to
have real delivered quantities in sales orders.

**Scope evidence:** The module contains 141 files, including 47 Python, 18 XML, and 5 JavaScript/TypeScript files. The manifest declares dependencies: `sale_project`, `hr_timesheet`.

## 2. Module structure

- Model/business logic files: 18
- Controller/API files: 2
- XML/data/view/template files: 18
- Browser asset files: 5
- Security files: 2
- Test files: 22
- Scheduled/automation evidence files: 0
- Reporting evidence files: 4

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/sale_timesheet/security/ir.access.csv`, `addons/sale_timesheet/security/sale_timesheet_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 18 model declarations, 279 methods, 1 constraint handlers, 4 onchange handlers, and 34 dependency declarations.
- **Evidence:** `addons/sale_timesheet/models/hr_employee_departure.py:4`, `addons/sale_timesheet/models/sale_order.py:11`, `addons/sale_timesheet/models/product_product.py:9`, `addons/sale_timesheet/models/product_template.py:9`, `addons/sale_timesheet/models/res_config_settings.py:7`, `addons/sale_timesheet/models/account_analytic_line.py:10`, `addons/sale_timesheet/models/account_move_reversal.py:4`, `addons/sale_timesheet/models/project_sale_line_employee_map.py:8`, `addons/sale_timesheet/models/project_task.py:7`, `addons/sale_timesheet/models/project_project.py:12`, `addons/sale_timesheet/models/account_move.py:9`, `addons/sale_timesheet/models/account_move_line.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 2 route declarations.
- **Evidence:** `addons/sale_timesheet/controllers/portal.py:33`, `addons/sale_timesheet/controllers/portal.py:121`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 18 XML files and 5 JavaScript/TypeScript files; static XML analysis found 363 record/template/menu identifiers.
- **Evidence:** `addons/sale_timesheet/security/sale_timesheet_security.xml:10`, `addons/sale_timesheet/security/sale_timesheet_security.xml:14`, `addons/sale_timesheet/report/project_report_view.xml:4`, `addons/sale_timesheet/report/project_report_view.xml:15`, `addons/sale_timesheet/report/project_report_view.xml:26`, `addons/sale_timesheet/report/timesheets_analysis_views.xml:3`, `addons/sale_timesheet/report/timesheets_analysis_views.xml:22`, `addons/sale_timesheet/report/timesheets_analysis_views.xml:33`, `addons/sale_timesheet/report/timesheets_analysis_views.xml:45`, `addons/sale_timesheet/report/timesheets_analysis_views.xml:58`, `addons/sale_timesheet/report/timesheets_analysis_views.xml:71`, `addons/sale_timesheet/report/timesheets_analysis_views.xml:83`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/sale_timesheet/security/ir.access.csv`, `addons/sale_timesheet/security/sale_timesheet_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 4 files contain report-action/template indicators.
- **Evidence:** `addons/sale_timesheet/models/account_move_send.py`, `addons/sale_timesheet/report/report_timesheet_templates.xml`, `addons/sale_timesheet/tests/test_sale_timesheet_report.py`, `addons/sale_timesheet/tests/test_report_timesheet.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 22 test files are present.
- **Evidence:** `addons/sale_timesheet/tests/test_analytic_to_sale_timesheet.py`, `addons/sale_timesheet/tests/test_edit_so_line_timesheet.py`, `addons/sale_timesheet/tests/test_sale_timesheet_accrued_entries.py`, `addons/sale_timesheet/tests/test_performance.py`, `addons/sale_timesheet/tests/test_sale_timesheet_product_template.py`, `addons/sale_timesheet/tests/test_reinvoice.py`, `addons/sale_timesheet/tests/test_sale_timesheet.py`, `addons/sale_timesheet/tests/test_sale_service.py`, `addons/sale_timesheet/tests/test_task_analysis.py`, `addons/sale_timesheet/tests/test_sale_timesheet_product_product.py`, `addons/sale_timesheet/tests/test_so_line_determined_in_timesheet.py`, `addons/sale_timesheet/tests/test_upsell_warning.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 18; representative identifiers: `account.account_analytic_line_rule_billing_user`, `account.account_analytic_line_rule_readonly_user`, `view_task_project_user_pivot_inherited`, `view_task_project_user_fsm_pivot_base_inherited`, `view_task_project_user_fsm_graph_base_inherited`, `timesheets_analysis_report_list_inherited`, `timesheete_analysis_report_form`, `timesheets_analysis_report_pivot_inherit`, `timesheets_analysis_report_graph_inherit`, `timesheets_analysis_report_graph_timesheet_grid`, `timesheets_analysis_report_pivot_project_inherit`, `timesheets_analysis_report_graph_project_inherit`, `timesheets_analysis_report_pivot_task_inherit`, `timesheets_analysis_report_graph_task_inherit`, `timesheets_analysis_report_pivot_invoice_type`, `timesheets_analysis_report_graph_invoice_type`, `hr_timesheet_report_search_sale_timesheet`, `timesheet_action_billing_report`, `timesheet_action_view_report_by_billing_rate_pivot`, `timesheet_action_view_report_by_billing_rate_graph`
- Menus: 1; representative evidence: `addons/sale_timesheet/report/timesheets_analysis_views.xml:203`
- Templates: 11; representative evidence: `addons/sale_timesheet/report/report_timesheet_templates.xml:3`, `addons/sale_timesheet/report/report_timesheet_templates.xml:26`, `addons/sale_timesheet/report/report_timesheet_templates.xml:61`, `addons/sale_timesheet/report/report_timesheet_templates.xml:78`, `addons/sale_timesheet/views/project_portal_templates.xml:4`, `addons/sale_timesheet/views/project_portal_templates.xml:23`, `addons/sale_timesheet/views/sale_timesheet_portal_templates.xml:4`, `addons/sale_timesheet/views/sale_timesheet_portal_templates.xml:12`, `addons/sale_timesheet/views/sale_timesheet_portal_templates.xml:74`, `addons/sale_timesheet/views/sale_timesheet_portal_templates.xml:85`, `addons/sale_timesheet/views/sale_timesheet_portal_templates.xml:113`
- View/action field declarations: 117; representative evidence: `addons/sale_timesheet/report/project_report_view.xml:6`, `addons/sale_timesheet/report/project_report_view.xml:8`, `addons/sale_timesheet/report/project_report_view.xml:17`, `addons/sale_timesheet/report/project_report_view.xml:19`, `addons/sale_timesheet/report/project_report_view.xml:28`, `addons/sale_timesheet/report/project_report_view.xml:30`, `addons/sale_timesheet/report/timesheets_analysis_views.xml:5`, `addons/sale_timesheet/report/timesheets_analysis_views.xml:7`, `addons/sale_timesheet/report/timesheets_analysis_views.xml:24`, `addons/sale_timesheet/report/timesheets_analysis_views.xml:26`, `addons/sale_timesheet/report/timesheets_analysis_views.xml:35`, `addons/sale_timesheet/report/timesheets_analysis_views.xml:37`
- Browser assets: 5; representative files: `addons/sale_timesheet/static/tests/sale_timesheet_test_helpers.js`, `addons/sale_timesheet/static/tests/so_line_create_button.test.js`, `addons/sale_timesheet/static/tests/so_line_field.test.js`, `addons/sale_timesheet/static/src/components/so_line_field/so_line_field.js`, `addons/sale_timesheet/static/tests/tours/sale_timesheet_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale_timesheet/__manifest__.py`
- **HTTP entry points:** `addons/sale_timesheet/controllers/portal.py:33`, `addons/sale_timesheet/controllers/portal.py:121`
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/sale_timesheet/models/account_move_send.py`, `addons/sale_timesheet/report/report_timesheet_templates.xml`, `addons/sale_timesheet/tests/test_sale_timesheet_report.py`, `addons/sale_timesheet/tests/test_report_timesheet.py`

## 7. Database interactions

- Model declarations: 18
- Representative model evidence: inherits `hr.employee.departure` (addons/sale_timesheet/models/hr_employee_departure.py:4); inherits `sale.order` (addons/sale_timesheet/models/sale_order.py:11); inherits `product.product` (addons/sale_timesheet/models/product_product.py:9); inherits `product.template` (addons/sale_timesheet/models/product_template.py:9); inherits `res.config.settings` (addons/sale_timesheet/models/res_config_settings.py:7); inherits `account.analytic.line` (addons/sale_timesheet/models/account_analytic_line.py:10); inherits `account.move.reversal` (addons/sale_timesheet/models/account_move_reversal.py:4); `project.sale.line.employee.map` (addons/sale_timesheet/models/project_sale_line_employee_map.py:8); inherits `project.task` (addons/sale_timesheet/models/project_task.py:7); inherits `project.project` (addons/sale_timesheet/models/project_project.py:12); inherits `account.move` (addons/sale_timesheet/models/account_move.py:9); inherits `account.move.line` (addons/sale_timesheet/models/account_move_line.py:8); inherits `hr.employee` (addons/sale_timesheet/models/hr_employee.py:6); inherits `sale.order.line` (addons/sale_timesheet/models/sale_order_line.py:7); inherits `account.move.send` (addons/sale_timesheet/models/account_move_send.py:4); inherits `report.project.task.user` (addons/sale_timesheet/report/project_report.py:7); inherits `timesheets.analysis.report` (addons/sale_timesheet/report/timesheets_analysis_report.py:8); inherits `sale.advance.payment.inv` (addons/sale_timesheet/wizard/sale_make_invoice_advance.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 2
- Route evidence: `addons/sale_timesheet/controllers/portal.py:33`, `addons/sale_timesheet/controllers/portal.py:121`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale_project`, `hr_timesheet`
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

- `addons/sale_timesheet/__init__.py`
- `addons/sale_timesheet/__manifest__.py`
- `addons/sale_timesheet/controllers/__init__.py`
- `addons/sale_timesheet/controllers/portal.py`
- `addons/sale_timesheet/data/mail_template_data.xml`
- `addons/sale_timesheet/data/sale_service_data.xml`
- `addons/sale_timesheet/data/sale_service_demo.xml`
- `addons/sale_timesheet/i18n/af.po`
- `addons/sale_timesheet/i18n/am.po`
- `addons/sale_timesheet/i18n/ar.po`
- `addons/sale_timesheet/i18n/az.po`
- `addons/sale_timesheet/i18n/bg.po`
- `addons/sale_timesheet/i18n/bs.po`
- `addons/sale_timesheet/i18n/ca.po`
- `addons/sale_timesheet/i18n/cs.po`
- `addons/sale_timesheet/i18n/da.po`
- `addons/sale_timesheet/i18n/de.po`
- `addons/sale_timesheet/i18n/el.po`
- `addons/sale_timesheet/i18n/es.po`
- `addons/sale_timesheet/i18n/es_419.po`
- `addons/sale_timesheet/i18n/es_CL.po`
- `addons/sale_timesheet/i18n/et.po`
- `addons/sale_timesheet/i18n/eu.po`
- `addons/sale_timesheet/i18n/fa.po`
- `addons/sale_timesheet/i18n/fi.po`
- `addons/sale_timesheet/i18n/fo.po`
- `addons/sale_timesheet/i18n/fr.po`
- `addons/sale_timesheet/i18n/fr_BE.po`
- `addons/sale_timesheet/i18n/fr_CA.po`
- `addons/sale_timesheet/i18n/gl.po`
- `addons/sale_timesheet/i18n/gu.po`
- `addons/sale_timesheet/i18n/he.po`
- `addons/sale_timesheet/i18n/hi.po`
- `addons/sale_timesheet/i18n/hr.po`
- `addons/sale_timesheet/i18n/hu.po`
- `addons/sale_timesheet/i18n/hy.po`
- `addons/sale_timesheet/i18n/id.po`
- `addons/sale_timesheet/i18n/is.po`
- `addons/sale_timesheet/i18n/it.po`
- `addons/sale_timesheet/i18n/ja.po`
- `addons/sale_timesheet/i18n/ka.po`
- `addons/sale_timesheet/i18n/kab.po`
- `addons/sale_timesheet/i18n/km.po`
- `addons/sale_timesheet/i18n/ko.po`
- `addons/sale_timesheet/i18n/ku.po`
- `addons/sale_timesheet/i18n/lo.po`
- `addons/sale_timesheet/i18n/lt.po`
- `addons/sale_timesheet/i18n/lv.po`
- `addons/sale_timesheet/i18n/mk.po`
- `addons/sale_timesheet/i18n/mn.po`
- `addons/sale_timesheet/i18n/my.po`
- `addons/sale_timesheet/i18n/nb.po`
- `addons/sale_timesheet/i18n/nl.po`
- `addons/sale_timesheet/i18n/pl.po`
- `addons/sale_timesheet/i18n/pt.po`
- `addons/sale_timesheet/i18n/pt_BR.po`
- `addons/sale_timesheet/i18n/ro.po`
- `addons/sale_timesheet/i18n/ru.po`
- `addons/sale_timesheet/i18n/sale_timesheet.pot`
- `addons/sale_timesheet/i18n/sk.po`
- `addons/sale_timesheet/i18n/sl.po`
- `addons/sale_timesheet/i18n/sr@latin.po`
- `addons/sale_timesheet/i18n/sv.po`
- `addons/sale_timesheet/i18n/th.po`
- `addons/sale_timesheet/i18n/tr.po`
- `addons/sale_timesheet/i18n/uk.po`
- `addons/sale_timesheet/i18n/uz.po`
- `addons/sale_timesheet/i18n/vi.po`
- `addons/sale_timesheet/i18n/zh_CN.po`
- `addons/sale_timesheet/i18n/zh_TW.po`
- `addons/sale_timesheet/models/__init__.py`
- `addons/sale_timesheet/models/account_analytic_line.py`
- `addons/sale_timesheet/models/account_move.py`
- `addons/sale_timesheet/models/account_move_line.py`
- `addons/sale_timesheet/models/account_move_reversal.py`
- `addons/sale_timesheet/models/account_move_send.py`
- `addons/sale_timesheet/models/hr_employee.py`
- `addons/sale_timesheet/models/hr_employee_departure.py`
- `addons/sale_timesheet/models/product_product.py`
- `addons/sale_timesheet/models/product_template.py`
- `addons/sale_timesheet/models/project_project.py`
- `addons/sale_timesheet/models/project_sale_line_employee_map.py`
- `addons/sale_timesheet/models/project_task.py`
- `addons/sale_timesheet/models/res_config_settings.py`
- `addons/sale_timesheet/models/sale_order.py`
- `addons/sale_timesheet/models/sale_order_line.py`
- `addons/sale_timesheet/report/__init__.py`
- `addons/sale_timesheet/report/project_report.py`
- `addons/sale_timesheet/report/project_report_view.xml`
- `addons/sale_timesheet/report/report_timesheet_templates.xml`
- `addons/sale_timesheet/report/timesheets_analysis_report.py`
- `addons/sale_timesheet/report/timesheets_analysis_views.xml`
- `addons/sale_timesheet/security/ir.access.csv`
- `addons/sale_timesheet/security/sale_timesheet_security.xml`
- `addons/sale_timesheet/static/description/icon.png`
- `addons/sale_timesheet/static/description/icon.svg`
- `addons/sale_timesheet/static/description/icon_hi.png`
- `addons/sale_timesheet/static/img/employee_jjo-image.webp`
- `addons/sale_timesheet/static/img/employee_jsm-image.webp`
- `addons/sale_timesheet/static/img/product_product_time_product.png`
- `addons/sale_timesheet/static/src/components/so_line_field/so_line_field.js`
- `addons/sale_timesheet/static/src/components/so_line_field/so_line_field.xml`
- `addons/sale_timesheet/static/src/scss/sale_timesheet_portal.scss`
- `addons/sale_timesheet/static/tests/sale_timesheet_test_helpers.js`
- `addons/sale_timesheet/static/tests/so_line_create_button.test.js`
- `addons/sale_timesheet/static/tests/so_line_field.test.js`
- `addons/sale_timesheet/static/tests/tours/sale_timesheet_tour.js`
- `addons/sale_timesheet/tests/__init__.py`
- `addons/sale_timesheet/tests/common.py`
- `addons/sale_timesheet/tests/test_account_analytic_line.py`
- `addons/sale_timesheet/tests/test_analytic_to_sale_timesheet.py`
- `addons/sale_timesheet/tests/test_edit_so_line_timesheet.py`
- `addons/sale_timesheet/tests/test_performance.py`
- `addons/sale_timesheet/tests/test_project.py`
- `addons/sale_timesheet/tests/test_project_billing.py`
- `addons/sale_timesheet/tests/test_project_pricing_type.py`
- `addons/sale_timesheet/tests/test_reinvoice.py`
- `addons/sale_timesheet/tests/test_report_timesheet.py`
- `addons/sale_timesheet/tests/test_sale_service.py`
- `addons/sale_timesheet/tests/test_sale_timesheet.py`
- `addons/sale_timesheet/tests/test_sale_timesheet_accrued_entries.py`
- `addons/sale_timesheet/tests/test_sale_timesheet_portal.py`
- `addons/sale_timesheet/tests/test_sale_timesheet_product_product.py`
- `addons/sale_timesheet/tests/test_sale_timesheet_product_template.py`
- `addons/sale_timesheet/tests/test_sale_timesheet_report.py`
- `addons/sale_timesheet/tests/test_sale_timesheet_ui.py`
- `addons/sale_timesheet/tests/test_so_line_determined_in_timesheet.py`
- `addons/sale_timesheet/tests/test_task_analysis.py`
- `addons/sale_timesheet/tests/test_upsell_warning.py`
- `addons/sale_timesheet/views/account_analytic_line_views.xml`
- `addons/sale_timesheet/views/account_invoice_views.xml`
- `addons/sale_timesheet/views/product_views.xml`
- `addons/sale_timesheet/views/project_portal_templates.xml`
- `addons/sale_timesheet/views/project_sharing_views.xml`
- `addons/sale_timesheet/views/project_task_views.xml`
- `addons/sale_timesheet/views/res_config_settings_views.xml`
- `addons/sale_timesheet/views/sale_order_views.xml`
- `addons/sale_timesheet/views/sale_timesheet_portal_templates.xml`
- `addons/sale_timesheet/wizard/__init__.py`
- `addons/sale_timesheet/wizard/sale_make_invoice_advance.py`
- `addons/sale_timesheet/wizard/sale_make_invoice_advance_views.xml`
