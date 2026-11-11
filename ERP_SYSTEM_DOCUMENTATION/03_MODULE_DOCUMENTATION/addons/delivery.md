# Module: delivery

- **Module ID:** MOD-062
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/delivery`
- **Manifest:** `addons/delivery/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Delivery`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Allows you to add delivery methods in sale orders.
==================================================
You can define your own carrier for prices.
The system is able to add and compute the shipping line.

**Scope evidence:** The module contains 120 files, including 29 Python, 22 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `sale`, `payment_custom`.

## 2. Module structure

- Model/business logic files: 16
- Controller/API files: 0
- XML/data/view/template files: 22
- Browser asset files: 3
- Security files: 1
- Test files: 8
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/delivery/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 16 model declarations, 137 methods, 1 constraint handlers, 8 onchange handlers, and 20 dependency declarations.
- **Evidence:** `addons/delivery/models/product_category.py:7`, `addons/delivery/models/res_partner.py:6`, `addons/delivery/models/sale_order.py:8`, `addons/delivery/models/delivery_carrier.py:14`, `addons/delivery/models/delivery_price_rule.py:15`, `addons/delivery/models/ir_http.py:6`, `addons/delivery/models/ir_module_module.py:6`, `addons/delivery/models/delivery_zip_prefix.py:6`, `addons/delivery/models/payment_transaction.py:7`, `addons/delivery/models/sale_order_line.py:7`, `addons/delivery/models/payment_method.py:6`, `addons/delivery/models/payment_provider.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 22 XML files and 3 JavaScript/TypeScript files; static XML analysis found 37 record/template/menu identifiers.
- **Evidence:** `addons/delivery/report/ir_actions_report_templates.xml:4`, `addons/delivery/report/ir_actions_report_templates.xml:13`, `addons/delivery/report/ir_actions_report.xml:4`, `addons/delivery/wizard/res_config_settings_views.xml:4`, `addons/delivery/wizard/delivery_note_views.xml:4`, `addons/delivery/wizard/delivery_note_line_views.xml:4`, `addons/delivery/wizard/choose_delivery_carrier_views.xml:3`, `addons/delivery/data/delivery_data.xml:4`, `addons/delivery/data/delivery_data.xml:7`, `addons/delivery/data/delivery_data.xml:17`, `addons/delivery/data/mail_template_data.xml:4`, `addons/delivery/data/delivery_demo.xml:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/delivery/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/delivery/report/ir_actions_report.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 8 test files are present.
- **Evidence:** `addons/delivery/tests/test_delivery_availability.py`, `addons/delivery/tests/test_choose_delivery_carrier.py`, `addons/delivery/tests/common.py`, `addons/delivery/tests/cash_on_delivery_common.py`, `addons/delivery/tests/test_payment_provider.py`, `addons/delivery/tests/test_payment_transaction.py`, `addons/delivery/tests/__init__.py`, `addons/delivery/tests/test_delivery_cost.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 22; representative identifiers: `delivery_report_saleorder_document`, `report_delivery_note`, `action_report_delivery_note`, `res_config_settings_view_form`, `delivery_note_form_view`, `delivery_note_list_view`, `choose_delivery_carrier_view_form`, `product_category_deliveries`, `product_product_delivery`, `free_delivery_carrier`, `mail_template_data_delivery_note`, `product_product_delivery_poste`, `delivery_carrier`, `product.product_product_local_delivery`, `delivery_local_delivery`, `delivery_price_rule1`, `delivery_price_rule2`, `delivery_price_rule3`, `seq_delivery_note`, `payment_provider_cod`
- Menus: 1; representative evidence: `addons/delivery/views/delivery_carrier_views.xml:243`
- Templates: 4; representative evidence: `addons/delivery/report/ir_actions_report_templates.xml:4`, `addons/delivery/report/ir_actions_report_templates.xml:13`, `addons/delivery/views/portal_templates.xml:4`, `addons/delivery/views/payment_form_templates.xml:4`
- View/action field declarations: 35; representative evidence: `addons/delivery/report/ir_actions_report.xml:6`, `addons/delivery/wizard/res_config_settings_views.xml:6`, `addons/delivery/wizard/res_config_settings_views.xml:8`, `addons/delivery/wizard/delivery_note_views.xml:6`, `addons/delivery/wizard/delivery_note_views.xml:7`, `addons/delivery/wizard/delivery_note_line_views.xml:6`, `addons/delivery/wizard/delivery_note_line_views.xml:7`, `addons/delivery/wizard/choose_delivery_carrier_views.xml:5`, `addons/delivery/wizard/choose_delivery_carrier_views.xml:6`, `addons/delivery/views/delivery_price_rule_views.xml:6`, `addons/delivery/views/delivery_price_rule_views.xml:7`, `addons/delivery/views/delivery_price_rule_views.xml:35`
- Browser assets: 3; representative files: `addons/delivery/static/src/interactions/payment_form.js`, `addons/delivery/static/src/backend/widgets/carrier_rates_loader.js`, `addons/delivery/static/tests/tours/tour_test_get_all_rates.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/delivery/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/delivery/report/ir_actions_report.xml`

## 7. Database interactions

- Model declarations: 16
- Representative model evidence: inherits `product.category` (addons/delivery/models/product_category.py:7); inherits `res.partner` (addons/delivery/models/res_partner.py:6); inherits `sale.order` (addons/delivery/models/sale_order.py:8); `delivery.carrier` (addons/delivery/models/delivery_carrier.py:14); `delivery.price.rule` (addons/delivery/models/delivery_price_rule.py:15); inherits `ir.http` (addons/delivery/models/ir_http.py:6); `ir.module.module` (addons/delivery/models/ir_module_module.py:6); `delivery.zip.prefix` (addons/delivery/models/delivery_zip_prefix.py:6); inherits `payment.transaction` (addons/delivery/models/payment_transaction.py:7); inherits `sale.order.line` (addons/delivery/models/sale_order_line.py:7); inherits `payment.method` (addons/delivery/models/payment_method.py:6); inherits `payment.provider` (addons/delivery/models/payment_provider.py:9); inherits `res.config.settings` (addons/delivery/wizard/res_config_settings.py:6); `delivery.note.wizard.line` (addons/delivery/wizard/delivery_note_line.py:6); `delivery.note.wizard` (addons/delivery/wizard/delivery_note.py:6); `choose.delivery.carrier` (addons/delivery/wizard/choose_delivery_carrier.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale`, `payment_custom`
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

- `addons/delivery/__init__.py`
- `addons/delivery/__manifest__.py`
- `addons/delivery/const.py`
- `addons/delivery/data/delivery_data.xml`
- `addons/delivery/data/delivery_demo.xml`
- `addons/delivery/data/ir_sequence_data.xml`
- `addons/delivery/data/mail_template_data.xml`
- `addons/delivery/data/neutralize.sql`
- `addons/delivery/data/payment_method_data.xml`
- `addons/delivery/data/payment_provider_data.xml`
- `addons/delivery/i18n/af.po`
- `addons/delivery/i18n/am.po`
- `addons/delivery/i18n/ar.po`
- `addons/delivery/i18n/az.po`
- `addons/delivery/i18n/bg.po`
- `addons/delivery/i18n/bs.po`
- `addons/delivery/i18n/ca.po`
- `addons/delivery/i18n/cs.po`
- `addons/delivery/i18n/da.po`
- `addons/delivery/i18n/de.po`
- `addons/delivery/i18n/delivery.pot`
- `addons/delivery/i18n/el.po`
- `addons/delivery/i18n/es.po`
- `addons/delivery/i18n/es_419.po`
- `addons/delivery/i18n/es_CL.po`
- `addons/delivery/i18n/et.po`
- `addons/delivery/i18n/eu.po`
- `addons/delivery/i18n/fa.po`
- `addons/delivery/i18n/fi.po`
- `addons/delivery/i18n/fo.po`
- `addons/delivery/i18n/fr.po`
- `addons/delivery/i18n/fr_CA.po`
- `addons/delivery/i18n/gl.po`
- `addons/delivery/i18n/gu.po`
- `addons/delivery/i18n/he.po`
- `addons/delivery/i18n/hi.po`
- `addons/delivery/i18n/hr.po`
- `addons/delivery/i18n/hu.po`
- `addons/delivery/i18n/id.po`
- `addons/delivery/i18n/is.po`
- `addons/delivery/i18n/it.po`
- `addons/delivery/i18n/ja.po`
- `addons/delivery/i18n/ka.po`
- `addons/delivery/i18n/kab.po`
- `addons/delivery/i18n/km.po`
- `addons/delivery/i18n/ko.po`
- `addons/delivery/i18n/ku.po`
- `addons/delivery/i18n/lo.po`
- `addons/delivery/i18n/lt.po`
- `addons/delivery/i18n/lv.po`
- `addons/delivery/i18n/mk.po`
- `addons/delivery/i18n/mn.po`
- `addons/delivery/i18n/my.po`
- `addons/delivery/i18n/nb.po`
- `addons/delivery/i18n/nl.po`
- `addons/delivery/i18n/pl.po`
- `addons/delivery/i18n/pt.po`
- `addons/delivery/i18n/pt_BR.po`
- `addons/delivery/i18n/ro.po`
- `addons/delivery/i18n/ru.po`
- `addons/delivery/i18n/sk.po`
- `addons/delivery/i18n/sl.po`
- `addons/delivery/i18n/sq.po`
- `addons/delivery/i18n/sr@latin.po`
- `addons/delivery/i18n/sv.po`
- `addons/delivery/i18n/th.po`
- `addons/delivery/i18n/tr.po`
- `addons/delivery/i18n/uk.po`
- `addons/delivery/i18n/uz.po`
- `addons/delivery/i18n/vi.po`
- `addons/delivery/i18n/zh_CN.po`
- `addons/delivery/i18n/zh_TW.po`
- `addons/delivery/models/__init__.py`
- `addons/delivery/models/delivery_carrier.py`
- `addons/delivery/models/delivery_price_rule.py`
- `addons/delivery/models/delivery_zip_prefix.py`
- `addons/delivery/models/ir_http.py`
- `addons/delivery/models/ir_module_module.py`
- `addons/delivery/models/payment_method.py`
- `addons/delivery/models/payment_provider.py`
- `addons/delivery/models/payment_transaction.py`
- `addons/delivery/models/product_category.py`
- `addons/delivery/models/res_partner.py`
- `addons/delivery/models/sale_order.py`
- `addons/delivery/models/sale_order_line.py`
- `addons/delivery/report/ir_actions_report.xml`
- `addons/delivery/report/ir_actions_report_templates.xml`
- `addons/delivery/security/ir.access.csv`
- `addons/delivery/static/src/backend/widgets/carrier_rates_loader.js`
- `addons/delivery/static/src/backend/widgets/carrier_rates_loader.xml`
- `addons/delivery/static/src/img/payment_method_cash_on_delivery.png`
- `addons/delivery/static/src/img/payment_provider_cash_on_delivery.png`
- `addons/delivery/static/src/interactions/payment_form.js`
- `addons/delivery/static/tests/tours/tour_test_get_all_rates.js`
- `addons/delivery/tests/__init__.py`
- `addons/delivery/tests/cash_on_delivery_common.py`
- `addons/delivery/tests/common.py`
- `addons/delivery/tests/test_choose_delivery_carrier.py`
- `addons/delivery/tests/test_delivery_availability.py`
- `addons/delivery/tests/test_delivery_cost.py`
- `addons/delivery/tests/test_payment_provider.py`
- `addons/delivery/tests/test_payment_transaction.py`
- `addons/delivery/views/delivery_carrier_views.xml`
- `addons/delivery/views/delivery_price_rule_views.xml`
- `addons/delivery/views/delivery_zip_prefix_views.xml`
- `addons/delivery/views/ir_module_module_views.xml`
- `addons/delivery/views/payment_form_templates.xml`
- `addons/delivery/views/payment_provider_views.xml`
- `addons/delivery/views/portal_templates.xml`
- `addons/delivery/views/res_partner_views.xml`
- `addons/delivery/views/sale_order_views.xml`
- `addons/delivery/wizard/__init__.py`
- `addons/delivery/wizard/choose_delivery_carrier.py`
- `addons/delivery/wizard/choose_delivery_carrier_views.xml`
- `addons/delivery/wizard/delivery_note.py`
- `addons/delivery/wizard/delivery_note_line.py`
- `addons/delivery/wizard/delivery_note_line_views.xml`
- `addons/delivery/wizard/delivery_note_views.xml`
- `addons/delivery/wizard/res_config_settings.py`
- `addons/delivery/wizard/res_config_settings_views.xml`
