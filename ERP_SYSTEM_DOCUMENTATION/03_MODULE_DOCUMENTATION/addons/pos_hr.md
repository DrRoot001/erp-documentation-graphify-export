# Module: pos_hr

- **Module ID:** MOD-433
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_hr`
- **Manifest:** `addons/pos_hr/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Link module between Point of Sale and HR

**Manifest description:**

This module allows Employees (and not users) to log in to the Point of Sale application using a barcode, a PIN number or both.
The actual till still requires one user but an unlimited number of employees can log on to that till and process sales.

**Scope evidence:** The module contains 117 files, including 23 Python, 14 XML, and 31 JavaScript/TypeScript files. The manifest declares dependencies: `point_of_sale`, `hr`.

## 2. Module structure

- Model/business logic files: 13
- Controller/API files: 0
- XML/data/view/template files: 14
- Browser asset files: 31
- Security files: 0
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 13 model declarations, 67 methods, 0 constraint handlers, 9 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/pos_hr/models/res_partner.py:7`, `addons/pos_hr/models/product_product.py:4`, `addons/pos_hr/models/account_bank_statement.py:5`, `addons/pos_hr/models/pos_payment.py:4`, `addons/pos_hr/models/single_employee_sales_report.py:6`, `addons/pos_hr/models/pos_config.py:14`, `addons/pos_hr/models/pos_order_receipt.py:5`, `addons/pos_hr/models/res_config_settings.py:13`, `addons/pos_hr/models/pos_session.py:7`, `addons/pos_hr/models/pos_order.py:6`, `addons/pos_hr/models/hr_employee.py:10`, `addons/pos_hr/report/pos_order_report.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 14 XML files and 31 JavaScript/TypeScript files; static XML analysis found 13 record/template/menu identifiers.
- **Evidence:** `addons/pos_hr/wizard/pos_daily_sales_reports.xml:3`, `addons/pos_hr/views/single_employee_sales_report.xml:3`, `addons/pos_hr/views/single_employee_sales_report.xml:17`, `addons/pos_hr/views/pos_payment_view.xml:3`, `addons/pos_hr/views/res_config_settings_views.xml:3`, `addons/pos_hr/views/pos_config.xml:3`, `addons/pos_hr/views/pos_session_view.xml:3`, `addons/pos_hr/views/pos_order_report_view.xml:3`, `addons/pos_hr/views/pos_order_report_view.xml:14`, `addons/pos_hr/views/pos_order_view.xml:3`, `addons/pos_hr/views/pos_order_view.xml:17`, `addons/pos_hr/views/pos_order_view.xml:31`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/pos_hr/tests/test_frontend.py`, `addons/pos_hr/tests/test_synchronisation.py`, `addons/pos_hr/tests/test_point_of_sale_flow.py`, `addons/pos_hr/tests/__init__.py`, `addons/pos_hr/tests/test_res_config_settings.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 14; representative identifiers: `view_pos_daily_sales_reports_wizard`, `pos_hr.single_employee_sales_report`, `pos_hr.report_salesdetails_with_employee_reports`, `view_pos_payment_tree_inherit`, `res_config_settings_view_form`, `pos_config_form_view_inherit`, `view_pos_session_form_inherit_pos_hr`, `view_report_pos_order_search_inherit`, `report_pos_order_view_tree`, `pos_order_form_inherit`, `pos_order_list_select_inherit`, `view_pos_order_tree_inherit`, `view_pos_config_kanban_inherit_pos_hr`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/pos_hr/views/single_employee_sales_report.xml:3`, `addons/pos_hr/views/single_employee_sales_report.xml:17`
- View/action field declarations: 22; representative evidence: `addons/pos_hr/wizard/pos_daily_sales_reports.xml:5`, `addons/pos_hr/wizard/pos_daily_sales_reports.xml:7`, `addons/pos_hr/views/pos_payment_view.xml:5`, `addons/pos_hr/views/pos_payment_view.xml:7`, `addons/pos_hr/views/res_config_settings_views.xml:5`, `addons/pos_hr/views/res_config_settings_views.xml:7`, `addons/pos_hr/views/pos_config.xml:5`, `addons/pos_hr/views/pos_config.xml:7`, `addons/pos_hr/views/pos_session_view.xml:5`, `addons/pos_hr/views/pos_session_view.xml:7`, `addons/pos_hr/views/pos_order_report_view.xml:5`, `addons/pos_hr/views/pos_order_report_view.xml:7`
- Browser assets: 31; representative files: `addons/pos_hr/static/src/app/services/pos_store.js`, `addons/pos_hr/static/src/app/models/data_service_options.js`, `addons/pos_hr/static/src/app/models/pos_order.js`, `addons/pos_hr/static/src/app/screens/order_details_dialog.js`, `addons/pos_hr/static/src/app/plugins/access_right_plugin.js`, `addons/pos_hr/static/src/app/utils/order_payment_validation.js`, `addons/pos_hr/static/src/app/screens/login_screen/login_screen.js`, `addons/pos_hr/static/src/app/components/navbar/navbar.js`, `addons/pos_hr/static/src/app/components/popups/cashier_selection_popup/cashier_selection_popup.js`, `addons/pos_hr/static/src/app/components/popups/cash_move_popup/cash_move_popup.js`, `addons/pos_hr/static/src/app/components/popups/closing_popup/closing_popup.js`, `addons/pos_hr/static/src/app/components/navbar/cashier_name/cashier_name.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_hr/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 13
- Representative model evidence: inherits `res.partner` (addons/pos_hr/models/res_partner.py:7); inherits `product.product` (addons/pos_hr/models/product_product.py:4); inherits `account.bank.statement.line` (addons/pos_hr/models/account_bank_statement.py:5); inherits `pos.payment` (addons/pos_hr/models/pos_payment.py:4); `report.pos_hr.single_employee_sales_report` (addons/pos_hr/models/single_employee_sales_report.py:6); `pos.config` (addons/pos_hr/models/pos_config.py:14); inherits `pos.order.receipt` (addons/pos_hr/models/pos_order_receipt.py:5); inherits `res.config.settings` (addons/pos_hr/models/res_config_settings.py:13); inherits `pos.session` (addons/pos_hr/models/pos_session.py:7); inherits `pos.order` (addons/pos_hr/models/pos_order.py:6); `hr.employee` (addons/pos_hr/models/hr_employee.py:10); inherits `report.pos.order` (addons/pos_hr/report/pos_order_report.py:5); inherits `pos.daily.sales.reports.wizard` (addons/pos_hr/wizard/pos_daily_sales_reports.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `point_of_sale`, `hr`
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

- `addons/pos_hr/__init__.py`
- `addons/pos_hr/__manifest__.py`
- `addons/pos_hr/i18n/ar.po`
- `addons/pos_hr/i18n/az.po`
- `addons/pos_hr/i18n/bg.po`
- `addons/pos_hr/i18n/bs.po`
- `addons/pos_hr/i18n/ca.po`
- `addons/pos_hr/i18n/cs.po`
- `addons/pos_hr/i18n/da.po`
- `addons/pos_hr/i18n/de.po`
- `addons/pos_hr/i18n/el.po`
- `addons/pos_hr/i18n/es.po`
- `addons/pos_hr/i18n/es_419.po`
- `addons/pos_hr/i18n/et.po`
- `addons/pos_hr/i18n/fa.po`
- `addons/pos_hr/i18n/fi.po`
- `addons/pos_hr/i18n/fr.po`
- `addons/pos_hr/i18n/he.po`
- `addons/pos_hr/i18n/hi.po`
- `addons/pos_hr/i18n/hr.po`
- `addons/pos_hr/i18n/hu.po`
- `addons/pos_hr/i18n/id.po`
- `addons/pos_hr/i18n/it.po`
- `addons/pos_hr/i18n/ja.po`
- `addons/pos_hr/i18n/kab.po`
- `addons/pos_hr/i18n/ko.po`
- `addons/pos_hr/i18n/ku.po`
- `addons/pos_hr/i18n/lo.po`
- `addons/pos_hr/i18n/lt.po`
- `addons/pos_hr/i18n/lv.po`
- `addons/pos_hr/i18n/mn.po`
- `addons/pos_hr/i18n/my.po`
- `addons/pos_hr/i18n/nb.po`
- `addons/pos_hr/i18n/nl.po`
- `addons/pos_hr/i18n/pl.po`
- `addons/pos_hr/i18n/pos_hr.pot`
- `addons/pos_hr/i18n/pt.po`
- `addons/pos_hr/i18n/pt_BR.po`
- `addons/pos_hr/i18n/ro.po`
- `addons/pos_hr/i18n/ru.po`
- `addons/pos_hr/i18n/sk.po`
- `addons/pos_hr/i18n/sl.po`
- `addons/pos_hr/i18n/sr@latin.po`
- `addons/pos_hr/i18n/sv.po`
- `addons/pos_hr/i18n/th.po`
- `addons/pos_hr/i18n/tr.po`
- `addons/pos_hr/i18n/uk.po`
- `addons/pos_hr/i18n/uz.po`
- `addons/pos_hr/i18n/vi.po`
- `addons/pos_hr/i18n/zh_CN.po`
- `addons/pos_hr/i18n/zh_TW.po`
- `addons/pos_hr/models/__init__.py`
- `addons/pos_hr/models/account_bank_statement.py`
- `addons/pos_hr/models/hr_employee.py`
- `addons/pos_hr/models/pos_config.py`
- `addons/pos_hr/models/pos_order.py`
- `addons/pos_hr/models/pos_order_receipt.py`
- `addons/pos_hr/models/pos_payment.py`
- `addons/pos_hr/models/pos_session.py`
- `addons/pos_hr/models/product_product.py`
- `addons/pos_hr/models/res_config_settings.py`
- `addons/pos_hr/models/res_partner.py`
- `addons/pos_hr/models/single_employee_sales_report.py`
- `addons/pos_hr/report/__init__.py`
- `addons/pos_hr/report/pos_order_report.py`
- `addons/pos_hr/static/src/app/components/navbar/cashier_name/cashier_name.js`
- `addons/pos_hr/static/src/app/components/navbar/cashier_name/cashier_name.xml`
- `addons/pos_hr/static/src/app/components/navbar/navbar.js`
- `addons/pos_hr/static/src/app/components/navbar/navbar.xml`
- `addons/pos_hr/static/src/app/components/popups/cash_move_popup/cash_move_popup.js`
- `addons/pos_hr/static/src/app/components/popups/cashier_selection_popup/cashier_selection_popup.js`
- `addons/pos_hr/static/src/app/components/popups/cashier_selection_popup/cashier_selection_popup.xml`
- `addons/pos_hr/static/src/app/components/popups/closing_popup/closing_popup.js`
- `addons/pos_hr/static/src/app/components/popups/closing_popup/closing_popup.xml`
- `addons/pos_hr/static/src/app/models/data_service_options.js`
- `addons/pos_hr/static/src/app/models/pos_order.js`
- `addons/pos_hr/static/src/app/plugins/access_right_plugin.js`
- `addons/pos_hr/static/src/app/screens/login_screen/login_screen.js`
- `addons/pos_hr/static/src/app/screens/login_screen/login_screen.xml`
- `addons/pos_hr/static/src/app/screens/order_details_dialog.js`
- `addons/pos_hr/static/src/app/services/pos_store.js`
- `addons/pos_hr/static/src/app/utils/order_payment_validation.js`
- `addons/pos_hr/static/tests/tours/pos_hr_tour.js`
- `addons/pos_hr/static/tests/tours/utils/cashier_selection_popup_util.js`
- `addons/pos_hr/static/tests/tours/utils/pos_hr_helpers.js`
- `addons/pos_hr/static/tests/unit/components/navbar/cashier_name.test.js`
- `addons/pos_hr/static/tests/unit/components/popups/cash_move_popup.test.js`
- `addons/pos_hr/static/tests/unit/components/popups/cashier_selection_popup.test.js`
- `addons/pos_hr/static/tests/unit/components/popups/product_info_popup.test.js`
- `addons/pos_hr/static/tests/unit/components/screens/feedback_screen.test.js`
- `addons/pos_hr/static/tests/unit/components/screens/login_screen.test.js`
- `addons/pos_hr/static/tests/unit/components/screens/payment_screen.test.js`
- `addons/pos_hr/static/tests/unit/components/screens/ticket_screen.test.js`
- `addons/pos_hr/static/tests/unit/data/hr_employee.data.js`
- `addons/pos_hr/static/tests/unit/data/pos_config.data.js`
- `addons/pos_hr/static/tests/unit/data/pos_order.data.js`
- `addons/pos_hr/static/tests/unit/data/pos_session.data.js`
- `addons/pos_hr/static/tests/unit/models/pos_order.test.js`
- `addons/pos_hr/static/tests/unit/services/access_right_plugin.test.js`
- `addons/pos_hr/static/tests/unit/services/pos_store.test.js`
- `addons/pos_hr/static/tests/unit/utils.js`
- `addons/pos_hr/tests/__init__.py`
- `addons/pos_hr/tests/test_frontend.py`
- `addons/pos_hr/tests/test_point_of_sale_flow.py`
- `addons/pos_hr/tests/test_res_config_settings.py`
- `addons/pos_hr/tests/test_synchronisation.py`
- `addons/pos_hr/views/point_of_sale_dashboard.xml`
- `addons/pos_hr/views/pos_config.xml`
- `addons/pos_hr/views/pos_order_report_view.xml`
- `addons/pos_hr/views/pos_order_view.xml`
- `addons/pos_hr/views/pos_payment_view.xml`
- `addons/pos_hr/views/pos_session_view.xml`
- `addons/pos_hr/views/res_config_settings_views.xml`
- `addons/pos_hr/views/single_employee_sales_report.xml`
- `addons/pos_hr/wizard/__init__.py`
- `addons/pos_hr/wizard/pos_daily_sales_reports.py`
- `addons/pos_hr/wizard/pos_daily_sales_reports.xml`
