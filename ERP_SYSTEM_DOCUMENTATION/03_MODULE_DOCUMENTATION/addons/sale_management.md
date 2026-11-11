# Module: sale_management

- **Module ID:** MOD-518
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_management`
- **Manifest:** `addons/sale_management/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** From quotations to invoices

**Manifest description:**

Manage sales quotations and orders
==================================

This application allows you to manage your sales goals in an effective and efficient manner by
keeping track of all sales orders and history.

It handles the full sales workflow:

* **Quotation** -> **Sales order** -> **Invoice**

Preferences (only with Warehouse Management installed)
------------------------------------------------------

If you also installed the Warehouse Management, you can deal with the following preferences:

* Shipping: Choice of delivery at once or partial delivery
* Invoicing: choose how invoices will be paid
* Incoterms: International Commercial terms


With this module you can personnalize the sales order and invoice report with
categories, subtotals or page-breaks.

The Dashboard for the Sales Manager will include
------------------------------------------------
* My Quotations
* Monthly Turnover (Graph)

**Scope evidence:** The module contains 125 files, including 19 Python, 14 XML, and 24 JavaScript/TypeScript files. The manifest declares dependencies: `sale`, `digest`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 2
- XML/data/view/template files: 14
- Browser asset files: 24
- Security files: 1
- Test files: 6
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/sale_management/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 94 methods, 2 constraint handlers, 2 onchange handlers, and 18 dependency declarations.
- **Evidence:** `addons/sale_management/models/sale_order.py:11`, `addons/sale_management/models/sale_order_template_line.py:8`, `addons/sale_management/models/digest.py:6`, `addons/sale_management/models/sale_order_template.py:8`, `addons/sale_management/models/product_attribute_custom_value.py:6`, `addons/sale_management/models/sale_order_line.py:7`, `addons/sale_management/wizard/res_config_settings.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/sale_management/controllers/portal.py:10`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 14 XML files and 24 JavaScript/TypeScript files; static XML analysis found 17 record/template/menu identifiers.
- **Evidence:** `addons/sale_management/data/sale_order_template_demo.xml:4`, `addons/sale_management/data/digest_data.xml:4`, `addons/sale_management/data/digest_data.xml:9`, `addons/sale_management/data/digest_data.xml:21`, `addons/sale_management/views/digest_views.xml:4`, `addons/sale_management/views/sale_management_menus.xml:4`, `addons/sale_management/views/sale_management_menus.xml:8`, `addons/sale_management/views/sale_portal_templates.xml:4`, `addons/sale_management/views/sale_portal_templates.xml:39`, `addons/sale_management/views/res_config_settings_views.xml:4`, `addons/sale_management/views/sale_order_views.xml:4`, `addons/sale_management/views/sale_order_views.xml:38`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/sale_management/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/sale_management/views/sale_order_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 6 test files are present.
- **Evidence:** `addons/sale_management/tests/test_sale_ui.py`, `addons/sale_management/tests/test_sale_section_templates.py`, `addons/sale_management/tests/test_sale_order.py`, `addons/sale_management/tests/common.py`, `addons/sale_management/tests/__init__.py`, `addons/sale_management/tests/test_sale_order_template.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 14; representative identifiers: `sale_order_template_1`, `digest.digest_digest_default`, `digest_tip_sale1_management_0`, `digest_tip_sale_management_1`, `digest_digest_view_form`, `sale.sale_menu_root`, `Templates`, `Order Quantity`, `Order Options`, `res_config_settings_view_form`, `sale_order_form_quote`, `model_sale_order_action_create_quotation_template`, `sale_order_template_view_search`, `sale_order_template_view_form`, `sale_order_template_view_form_mandatory_product`, `sale_order_template_view_tree`, `sale_order_template_action`
- Menus: 1; representative evidence: `addons/sale_management/views/sale_management_menus.xml:8`
- Templates: 2; representative evidence: `addons/sale_management/views/sale_portal_templates.xml:4`, `addons/sale_management/views/sale_portal_templates.xml:39`
- View/action field declarations: 16; representative evidence: `addons/sale_management/views/digest_views.xml:6`, `addons/sale_management/views/digest_views.xml:9`, `addons/sale_management/views/res_config_settings_views.xml:6`, `addons/sale_management/views/res_config_settings_views.xml:8`, `addons/sale_management/views/sale_order_views.xml:6`, `addons/sale_management/views/sale_order_views.xml:8`, `addons/sale_management/views/sale_order_template_views.xml:5`, `addons/sale_management/views/sale_order_template_views.xml:6`, `addons/sale_management/views/sale_order_template_views.xml:31`, `addons/sale_management/views/sale_order_template_views.xml:32`, `addons/sale_management/views/sale_order_template_views.xml:267`, `addons/sale_management/views/sale_order_template_views.xml:271`
- Browser assets: 24; representative files: `addons/sale_management/static/tests/sale_management_test_helpers.js`, `addons/sale_management/static/tests/sale_order_template_line_field.test.js`, `addons/sale_management/static/tests/sale_order_line_field.test.js`, `addons/sale_management/static/src/interactions/sale_update_line_button.js`, `addons/sale_management/static/src/fields/sale_product_mixin.js`, `addons/sale_management/static/src/components/product_catalog/kanban_controller.js`, `addons/sale_management/static/src/fields/sale_order_template_line_field/sale_order_template_line_field.js`, `addons/sale_management/static/src/fields/sale_order_line_field/sale_order_line_field.js`, `addons/sale_management/static/src/fields/sale_order_template_product_field/sale_order_template_product_field.js`, `addons/sale_management/static/src/fields/sale_order_template_label_text/sale_order_template_label_text.js`, `addons/sale_management/static/src/views/file_upload_list/file_upload_list_view.js`, `addons/sale_management/static/src/views/file_upload_list/file_upload_list_controller.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale_management/__manifest__.py`
- **HTTP entry points:** `addons/sale_management/controllers/portal.py:10`
- **Scheduled entry points:** `addons/sale_management/views/sale_order_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: inherits `sale.order` (addons/sale_management/models/sale_order.py:11); `sale.order.template.line` (addons/sale_management/models/sale_order_template_line.py:8); inherits `digest.digest` (addons/sale_management/models/digest.py:6); `sale.order.template` (addons/sale_management/models/sale_order_template.py:8); inherits `product.attribute.custom.value` (addons/sale_management/models/product_attribute_custom_value.py:6); inherits `sale.order.line` (addons/sale_management/models/sale_order_line.py:7); inherits `res.config.settings` (addons/sale_management/wizard/res_config_settings.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/sale_management/controllers/portal.py:10`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale`, `digest`
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

- `addons/sale_management/__init__.py`
- `addons/sale_management/__manifest__.py`
- `addons/sale_management/controllers/__init__.py`
- `addons/sale_management/controllers/portal.py`
- `addons/sale_management/data/digest_data.xml`
- `addons/sale_management/data/sale_order_template_demo.xml`
- `addons/sale_management/i18n/ar.po`
- `addons/sale_management/i18n/az.po`
- `addons/sale_management/i18n/bg.po`
- `addons/sale_management/i18n/bs.po`
- `addons/sale_management/i18n/ca.po`
- `addons/sale_management/i18n/cs.po`
- `addons/sale_management/i18n/da.po`
- `addons/sale_management/i18n/de.po`
- `addons/sale_management/i18n/el.po`
- `addons/sale_management/i18n/es.po`
- `addons/sale_management/i18n/es_419.po`
- `addons/sale_management/i18n/et.po`
- `addons/sale_management/i18n/fa.po`
- `addons/sale_management/i18n/fi.po`
- `addons/sale_management/i18n/fr.po`
- `addons/sale_management/i18n/gu.po`
- `addons/sale_management/i18n/he.po`
- `addons/sale_management/i18n/hi.po`
- `addons/sale_management/i18n/hr.po`
- `addons/sale_management/i18n/hu.po`
- `addons/sale_management/i18n/id.po`
- `addons/sale_management/i18n/is.po`
- `addons/sale_management/i18n/it.po`
- `addons/sale_management/i18n/ja.po`
- `addons/sale_management/i18n/kab.po`
- `addons/sale_management/i18n/km.po`
- `addons/sale_management/i18n/ko.po`
- `addons/sale_management/i18n/ku.po`
- `addons/sale_management/i18n/lo.po`
- `addons/sale_management/i18n/lt.po`
- `addons/sale_management/i18n/lv.po`
- `addons/sale_management/i18n/mn.po`
- `addons/sale_management/i18n/my.po`
- `addons/sale_management/i18n/nb.po`
- `addons/sale_management/i18n/nl.po`
- `addons/sale_management/i18n/pl.po`
- `addons/sale_management/i18n/pt.po`
- `addons/sale_management/i18n/pt_BR.po`
- `addons/sale_management/i18n/ro.po`
- `addons/sale_management/i18n/ru.po`
- `addons/sale_management/i18n/sale_management.pot`
- `addons/sale_management/i18n/sk.po`
- `addons/sale_management/i18n/sl.po`
- `addons/sale_management/i18n/sr@latin.po`
- `addons/sale_management/i18n/sv.po`
- `addons/sale_management/i18n/th.po`
- `addons/sale_management/i18n/tr.po`
- `addons/sale_management/i18n/uk.po`
- `addons/sale_management/i18n/uz.po`
- `addons/sale_management/i18n/vi.po`
- `addons/sale_management/i18n/zh_CN.po`
- `addons/sale_management/i18n/zh_TW.po`
- `addons/sale_management/models/__init__.py`
- `addons/sale_management/models/digest.py`
- `addons/sale_management/models/product_attribute_custom_value.py`
- `addons/sale_management/models/sale_order.py`
- `addons/sale_management/models/sale_order_line.py`
- `addons/sale_management/models/sale_order_template.py`
- `addons/sale_management/models/sale_order_template_line.py`
- `addons/sale_management/security/ir.access.csv`
- `addons/sale_management/static/description/icon.png`
- `addons/sale_management/static/description/icon.svg`
- `addons/sale_management/static/description/icon_hi.png`
- `addons/sale_management/static/src/components/product_catalog/kanban_controller.js`
- `addons/sale_management/static/src/fields/sale_order_line_field/sale_order_line_field.js`
- `addons/sale_management/static/src/fields/sale_order_line_field/sale_order_line_field.scss`
- `addons/sale_management/static/src/fields/sale_order_line_field/sale_order_line_field.xml`
- `addons/sale_management/static/src/fields/sale_order_template_label_text/sale_order_template_label_text.js`
- `addons/sale_management/static/src/fields/sale_order_template_label_text/sale_order_template_label_text.scss`
- `addons/sale_management/static/src/fields/sale_order_template_line_field/sale_order_template_line_field.js`
- `addons/sale_management/static/src/fields/sale_order_template_line_field/sale_order_template_line_field.scss`
- `addons/sale_management/static/src/fields/sale_order_template_line_field/sale_order_template_line_field.xml`
- `addons/sale_management/static/src/fields/sale_order_template_product_field/sale_order_template_product_field.js`
- `addons/sale_management/static/src/fields/sale_product_mixin.js`
- `addons/sale_management/static/src/img/milk-Sales-configure-products.gif`
- `addons/sale_management/static/src/img/milk-t-shirts.png`
- `addons/sale_management/static/src/img/online_training.png`
- `addons/sale_management/static/src/img/openerp_gold_partner.png`
- `addons/sale_management/static/src/img/partner_icon_01.png`
- `addons/sale_management/static/src/img/partner_icon_02.png`
- `addons/sale_management/static/src/img/partner_icon_04.png`
- `addons/sale_management/static/src/img/partner_sc_01.png`
- `addons/sale_management/static/src/interactions/sale_update_line_button.js`
- `addons/sale_management/static/src/views/components/template_dropdown.js`
- `addons/sale_management/static/src/views/components/template_dropdown.scss`
- `addons/sale_management/static/src/views/components/template_dropdown.xml`
- `addons/sale_management/static/src/views/file_upload_kanban/file_upload_kanban_controller.js`
- `addons/sale_management/static/src/views/file_upload_kanban/file_upload_kanban_view.js`
- `addons/sale_management/static/src/views/file_upload_list/file_upload_list_controller.js`
- `addons/sale_management/static/src/views/file_upload_list/file_upload_list_view.js`
- `addons/sale_management/static/src/views/onboarding_kanban/onboarding_kanban_view.js`
- `addons/sale_management/static/src/views/onboarding_list/onboarding_list_view.js`
- `addons/sale_management/static/src/views/order_form/order_form_controller.js`
- `addons/sale_management/static/src/views/order_form/order_form_controller.xml`
- `addons/sale_management/static/src/views/order_form/order_form_view.js`
- `addons/sale_management/static/src/views/sale_order_template_form/sale_order_template_form_view.js`
- `addons/sale_management/static/src/views/sale_order_template_form/sale_order_template_static_list.js`
- `addons/sale_management/static/src/views/template_kanban_buttons/template_kanban_buttons.xml`
- `addons/sale_management/static/src/views/template_list_buttons/template_list_buttons.xml`
- `addons/sale_management/static/tests/mock_server/mock_models/sale_order_template.js`
- `addons/sale_management/static/tests/mock_server/mock_models/sale_order_template_line.js`
- `addons/sale_management/static/tests/sale_management_test_helpers.js`
- `addons/sale_management/static/tests/sale_order_line_field.test.js`
- `addons/sale_management/static/tests/sale_order_template_line_field.test.js`
- `addons/sale_management/static/tests/tours/sale_flow_tour.js`
- `addons/sale_management/tests/__init__.py`
- `addons/sale_management/tests/common.py`
- `addons/sale_management/tests/test_sale_order.py`
- `addons/sale_management/tests/test_sale_order_template.py`
- `addons/sale_management/tests/test_sale_section_templates.py`
- `addons/sale_management/tests/test_sale_ui.py`
- `addons/sale_management/views/digest_views.xml`
- `addons/sale_management/views/res_config_settings_views.xml`
- `addons/sale_management/views/sale_management_menus.xml`
- `addons/sale_management/views/sale_order_template_views.xml`
- `addons/sale_management/views/sale_order_views.xml`
- `addons/sale_management/views/sale_portal_templates.xml`
- `addons/sale_management/wizard/__init__.py`
- `addons/sale_management/wizard/res_config_settings.py`
