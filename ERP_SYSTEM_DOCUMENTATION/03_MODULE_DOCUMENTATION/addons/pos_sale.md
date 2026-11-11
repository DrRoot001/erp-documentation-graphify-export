# Module: pos_sale

- **Module ID:** MOD-450
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_sale`
- **Manifest:** `addons/pos_sale/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Link module between Point of Sale and Sales

**Manifest description:**

This module adds a custom Sales Team for the Point of Sale. This enables you to view and manage your point of sale sales with more ease.

**Scope evidence:** The module contains 116 files, including 22 Python, 9 XML, and 30 JavaScript/TypeScript files. The manifest declares dependencies: `point_of_sale`, `sale_management`.

## 2. Module structure

- Model/business logic files: 14
- Controller/API files: 0
- XML/data/view/template files: 9
- Browser asset files: 30
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/pos_sale/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 14 model declarations, 110 methods, 0 constraint handlers, 0 onchange handlers, and 9 dependency declarations.
- **Evidence:** `addons/pos_sale/models/res_partner.py:4`, `addons/pos_sale/models/sale_order.py:8`, `addons/pos_sale/models/sale_order.py:121`, `addons/pos_sale/models/product_template.py:4`, `addons/pos_sale/models/pos_config.py:7`, `addons/pos_sale/models/res_config_settings.py:6`, `addons/pos_sale/models/pos_session.py:7`, `addons/pos_sale/models/crm_team.py:4`, `addons/pos_sale/models/pos_order.py:8`, `addons/pos_sale/models/account_move.py:4`, `addons/pos_sale/models/account_move_line.py:5`, `addons/pos_sale/models/pos_order_line.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 9 XML files and 30 JavaScript/TypeScript files; static XML analysis found 11 record/template/menu identifiers.
- **Evidence:** `addons/pos_sale/data/pos_sale_data.xml:4`, `addons/pos_sale/data/pos_sale_data.xml:8`, `addons/pos_sale/data/pos_sale_data.xml:21`, `addons/pos_sale/receipt/pos_order_receipt.xml:4`, `addons/pos_sale/views/point_of_sale_report.xml:3`, `addons/pos_sale/views/res_config_settings_views.xml:4`, `addons/pos_sale/views/sale_order_views.xml:4`, `addons/pos_sale/views/pos_order_views.xml:4`, `addons/pos_sale/views/sales_team_views.xml:3`, `addons/pos_sale/views/sales_team_views.xml:14`, `addons/pos_sale/views/sales_team_views.xml:22`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/pos_sale/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/pos_sale/tests/test_pos_sale_report.py`, `addons/pos_sale/tests/test_pos_sale_flow.py`, `addons/pos_sale/tests/__init__.py`, `addons/pos_sale/tests/test_taxes_downpayment.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 9; representative identifiers: `sales_team.pos_sales_team`, `pos_sale.default_downpayment_product`, `pos_sale.default_sol_product`, `pos_sale.pos_orderline_receipt_information`, `report_invoice_document`, `res_config_settings_view_form`, `view_order_form_inherit_pos_sale`, `view_pos_order_form_inherit_pos_sale`, `view_pos_session_search_inherit_pos_sale`, `pos_session_action_from_crm_team`, `view_pos_config_search_inherit_pos_sale`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/pos_sale/receipt/pos_order_receipt.xml:4`, `addons/pos_sale/views/point_of_sale_report.xml:3`
- View/action field declarations: 12; representative evidence: `addons/pos_sale/views/res_config_settings_views.xml:6`, `addons/pos_sale/views/res_config_settings_views.xml:8`, `addons/pos_sale/views/sale_order_views.xml:6`, `addons/pos_sale/views/sale_order_views.xml:8`, `addons/pos_sale/views/pos_order_views.xml:6`, `addons/pos_sale/views/pos_order_views.xml:8`, `addons/pos_sale/views/sales_team_views.xml:5`, `addons/pos_sale/views/sales_team_views.xml:7`, `addons/pos_sale/views/sales_team_views.xml:17`, `addons/pos_sale/views/sales_team_views.xml:18`, `addons/pos_sale/views/sales_team_views.xml:24`, `addons/pos_sale/views/sales_team_views.xml:26`
- Browser assets: 30; representative files: `addons/pos_sale/static/src/app/services/pos_store.js`, `addons/pos_sale/static/src/app/models/data_service_options.js`, `addons/pos_sale/static/src/app/models/pos_order_line.js`, `addons/pos_sale/static/src/app/models/pos_order.js`, `addons/pos_sale/static/src/app/utils/order_payment_validation.js`, `addons/pos_sale/static/src/app/components/screens/product_screen/control_buttons/control_buttons.js`, `addons/pos_sale/static/src/app/utils/printer/generate_printer_data.js`, `addons/pos_sale/static/tests/unit/ui_utils.js`, `addons/pos_sale/static/tests/tours/pos_sale_tour.js`, `addons/pos_sale/static/tests/tours/test_taxes_downpayment.js`, `addons/pos_sale/static/tests/unit/services/pos_store.test.js`, `addons/pos_sale/static/tests/unit/scenarios/pos_sale_flow.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_sale/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 14
- Representative model evidence: inherits `res.partner` (addons/pos_sale/models/res_partner.py:4); `sale.order` (addons/pos_sale/models/sale_order.py:8); `sale.order.line` (addons/pos_sale/models/sale_order.py:121); inherits `product.template` (addons/pos_sale/models/product_template.py:4); inherits `pos.config` (addons/pos_sale/models/pos_config.py:7); inherits `res.config.settings` (addons/pos_sale/models/res_config_settings.py:6); inherits `pos.session` (addons/pos_sale/models/pos_session.py:7); inherits `crm.team` (addons/pos_sale/models/crm_team.py:4); inherits `pos.order` (addons/pos_sale/models/pos_order.py:8); inherits `account.move` (addons/pos_sale/models/account_move.py:4); inherits `account.move.line` (addons/pos_sale/models/account_move_line.py:5); inherits `pos.order.line` (addons/pos_sale/models/pos_order_line.py:6); inherits `sale.report` (addons/pos_sale/report/sale_report.py:9); inherits `pos.order.receipt` (addons/pos_sale/receipt/pos_order_receipt.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `point_of_sale`, `sale_management`
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

- `addons/pos_sale/__init__.py`
- `addons/pos_sale/__manifest__.py`
- `addons/pos_sale/data/pos_sale_data.xml`
- `addons/pos_sale/i18n/ar.po`
- `addons/pos_sale/i18n/az.po`
- `addons/pos_sale/i18n/bg.po`
- `addons/pos_sale/i18n/bs.po`
- `addons/pos_sale/i18n/ca.po`
- `addons/pos_sale/i18n/cs.po`
- `addons/pos_sale/i18n/da.po`
- `addons/pos_sale/i18n/de.po`
- `addons/pos_sale/i18n/el.po`
- `addons/pos_sale/i18n/es.po`
- `addons/pos_sale/i18n/es_419.po`
- `addons/pos_sale/i18n/et.po`
- `addons/pos_sale/i18n/fa.po`
- `addons/pos_sale/i18n/fi.po`
- `addons/pos_sale/i18n/fr.po`
- `addons/pos_sale/i18n/gu.po`
- `addons/pos_sale/i18n/he.po`
- `addons/pos_sale/i18n/hi.po`
- `addons/pos_sale/i18n/hr.po`
- `addons/pos_sale/i18n/hu.po`
- `addons/pos_sale/i18n/id.po`
- `addons/pos_sale/i18n/is.po`
- `addons/pos_sale/i18n/it.po`
- `addons/pos_sale/i18n/ja.po`
- `addons/pos_sale/i18n/kab.po`
- `addons/pos_sale/i18n/km.po`
- `addons/pos_sale/i18n/ko.po`
- `addons/pos_sale/i18n/ku.po`
- `addons/pos_sale/i18n/lo.po`
- `addons/pos_sale/i18n/lt.po`
- `addons/pos_sale/i18n/lv.po`
- `addons/pos_sale/i18n/mn.po`
- `addons/pos_sale/i18n/my.po`
- `addons/pos_sale/i18n/nb.po`
- `addons/pos_sale/i18n/nl.po`
- `addons/pos_sale/i18n/pl.po`
- `addons/pos_sale/i18n/pos_sale.pot`
- `addons/pos_sale/i18n/pt.po`
- `addons/pos_sale/i18n/pt_BR.po`
- `addons/pos_sale/i18n/ro.po`
- `addons/pos_sale/i18n/ru.po`
- `addons/pos_sale/i18n/sk.po`
- `addons/pos_sale/i18n/sl.po`
- `addons/pos_sale/i18n/sr@latin.po`
- `addons/pos_sale/i18n/sv.po`
- `addons/pos_sale/i18n/th.po`
- `addons/pos_sale/i18n/tr.po`
- `addons/pos_sale/i18n/uk.po`
- `addons/pos_sale/i18n/uz.po`
- `addons/pos_sale/i18n/vi.po`
- `addons/pos_sale/i18n/zh_CN.po`
- `addons/pos_sale/i18n/zh_TW.po`
- `addons/pos_sale/models/__init__.py`
- `addons/pos_sale/models/account_move.py`
- `addons/pos_sale/models/account_move_line.py`
- `addons/pos_sale/models/crm_team.py`
- `addons/pos_sale/models/pos_config.py`
- `addons/pos_sale/models/pos_order.py`
- `addons/pos_sale/models/pos_order_line.py`
- `addons/pos_sale/models/pos_session.py`
- `addons/pos_sale/models/product_template.py`
- `addons/pos_sale/models/res_config_settings.py`
- `addons/pos_sale/models/res_partner.py`
- `addons/pos_sale/models/sale_order.py`
- `addons/pos_sale/receipt/__init__.py`
- `addons/pos_sale/receipt/pos_order_receipt.py`
- `addons/pos_sale/receipt/pos_order_receipt.xml`
- `addons/pos_sale/report/__init__.py`
- `addons/pos_sale/report/sale_report.py`
- `addons/pos_sale/security/ir.access.csv`
- `addons/pos_sale/static/src/app/components/orderline/orderline.scss`
- `addons/pos_sale/static/src/app/components/orderline/orderline.xml`
- `addons/pos_sale/static/src/app/components/screens/product_screen/control_buttons/control_buttons.js`
- `addons/pos_sale/static/src/app/components/screens/product_screen/control_buttons/control_buttons.xml`
- `addons/pos_sale/static/src/app/models/data_service_options.js`
- `addons/pos_sale/static/src/app/models/pos_order.js`
- `addons/pos_sale/static/src/app/models/pos_order_line.js`
- `addons/pos_sale/static/src/app/services/pos_store.js`
- `addons/pos_sale/static/src/app/utils/order_payment_validation.js`
- `addons/pos_sale/static/src/app/utils/printer/generate_printer_data.js`
- `addons/pos_sale/static/src/css/popups/product_info_popup.css`
- `addons/pos_sale/static/tests/tours/pos_sale_tour.js`
- `addons/pos_sale/static/tests/tours/test_taxes_downpayment.js`
- `addons/pos_sale/static/tests/tours/utils/pos_sale_utils.js`
- `addons/pos_sale/static/tests/unit/components/orderline.test.js`
- `addons/pos_sale/static/tests/unit/data/account_tax.data.js`
- `addons/pos_sale/static/tests/unit/data/pos_config.data.js`
- `addons/pos_sale/static/tests/unit/data/pos_order_line.data.js`
- `addons/pos_sale/static/tests/unit/data/pos_session.data.js`
- `addons/pos_sale/static/tests/unit/data/product_attribute.data.js`
- `addons/pos_sale/static/tests/unit/data/product_attribute_custom_value.data.js`
- `addons/pos_sale/static/tests/unit/data/product_product.data.js`
- `addons/pos_sale/static/tests/unit/data/product_template.data.js`
- `addons/pos_sale/static/tests/unit/data/product_template_attribute_line.data.js`
- `addons/pos_sale/static/tests/unit/data/product_template_attribute_value.data.js`
- `addons/pos_sale/static/tests/unit/data/res_partner.data.js`
- `addons/pos_sale/static/tests/unit/data/sale_order.data.js`
- `addons/pos_sale/static/tests/unit/data/sale_order_line.data.js`
- `addons/pos_sale/static/tests/unit/models/pos_order_line.test.js`
- `addons/pos_sale/static/tests/unit/scenarios/pos_sale_flow.test.js`
- `addons/pos_sale/static/tests/unit/scenarios/quotation_list_flow.test.js`
- `addons/pos_sale/static/tests/unit/scenarios/sale_warning_flow.test.js`
- `addons/pos_sale/static/tests/unit/services/pos_store.test.js`
- `addons/pos_sale/static/tests/unit/ui_utils.js`
- `addons/pos_sale/tests/__init__.py`
- `addons/pos_sale/tests/test_pos_sale_flow.py`
- `addons/pos_sale/tests/test_pos_sale_report.py`
- `addons/pos_sale/tests/test_taxes_downpayment.py`
- `addons/pos_sale/views/point_of_sale_report.xml`
- `addons/pos_sale/views/pos_order_views.xml`
- `addons/pos_sale/views/res_config_settings_views.xml`
- `addons/pos_sale/views/sale_order_views.xml`
- `addons/pos_sale/views/sales_team_views.xml`
