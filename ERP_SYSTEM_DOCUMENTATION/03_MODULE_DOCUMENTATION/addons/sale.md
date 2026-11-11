# Module: sale

- **Module ID:** MOD-509
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale`
- **Manifest:** `addons/sale/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Sales internal machinery

**Manifest description:**

This module contains all the common features of Sales Management and eCommerce.

**Scope evidence:** The module contains 306 files, including 76 Python, 64 XML, and 69 JavaScript/TypeScript files. The manifest declares dependencies: `sales_team`, `account_payment`, `utm`.

## 2. Module structure

- Model/business logic files: 30
- Controller/API files: 4
- XML/data/view/template files: 64
- Browser asset files: 69
- Security files: 2
- Test files: 37
- Scheduled/automation evidence files: 13
- Reporting evidence files: 4

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/sale/security/ir.access.csv`, `addons/sale/security/res_groups.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 30 model declarations, 859 methods, 7 constraint handlers, 19 onchange handlers, and 109 dependency declarations.
- **Evidence:** `addons/sale/models/product_category.py:6`, `addons/sale/models/res_partner.py:7`, `addons/sale/models/sale_order.py:34`, `addons/sale/models/product_product.py:10`, `addons/sale/models/product_product.py:171`, `addons/sale/models/ir_config_parameter.py:9`, `addons/sale/models/product_template.py:11`, `addons/sale/models/res_groups.py:6`, `addons/sale/models/account_analytic_applicability.py:6`, `addons/sale/models/account_analytic_line.py:8`, `addons/sale/models/ir_actions_report.py:7`, `addons/sale/models/crm_team.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 4 controller files and 14 route declarations.
- **Evidence:** `addons/sale/controllers/portal.py:106`, `addons/sale/controllers/portal.py:114`, `addons/sale/controllers/portal.py:132`, `addons/sale/controllers/portal.py:347`, `addons/sale/controllers/portal.py:407`, `addons/sale/controllers/portal.py:447`, `addons/sale/controllers/portal.py:475`, `addons/sale/controllers/portal.py:508`, `addons/sale/controllers/product_configurator.py:9`, `addons/sale/controllers/product_configurator.py:123`, `addons/sale/controllers/product_configurator.py:144`, `addons/sale/controllers/product_configurator.py:211`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 64 XML files and 69 JavaScript/TypeScript files; static XML analysis found 307 record/template/menu identifiers.
- **Evidence:** `addons/sale/security/res_groups.xml:4`, `addons/sale/security/res_groups.xml:8`, `addons/sale/security/res_groups.xml:12`, `addons/sale/security/res_groups.xml:16`, `addons/sale/security/res_groups.xml:20`, `addons/sale/report/ir_actions_report_templates.xml:3`, `addons/sale/report/ir_actions_report_templates.xml:477`, `addons/sale/report/ir_actions_report_templates.xml:485`, `addons/sale/report/ir_actions_report_templates.xml:489`, `addons/sale/report/ir_actions_report_templates.xml:500`, `addons/sale/report/ir_actions_report_templates.xml:502`, `addons/sale/report/ir_actions_report.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/sale/security/ir.access.csv`, `addons/sale/security/res_groups.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 13 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/sale/__manifest__.py`, `addons/sale/const.py`, `addons/sale/__init__.py`, `addons/sale/models/sale_order.py`, `addons/sale/models/ir_config_parameter.py`, `addons/sale/models/account_move.py`, `addons/sale/models/payment_transaction.py`, `addons/sale/models/res_company.py`, `addons/sale/wizard/account_accrued_orders_wizard_views.xml`, `addons/sale/data/ir_cron.xml`, `addons/sale/views/sale_order_views.xml`, `addons/sale/tests/test_sale_order.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 4 files contain report-action/template indicators.
- **Evidence:** `addons/sale/models/sale_order.py`, `addons/sale/models/ir_actions_report.py`, `addons/sale/controllers/portal.py`, `addons/sale/report/ir_actions_report.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 37 test files are present.
- **Evidence:** `addons/sale/tests/test_product_configurator_data.py`, `addons/sale/tests/test_access_rights.py`, `addons/sale/tests/test_sale_sections.py`, `addons/sale/tests/test_sale_order_line.py`, `addons/sale/tests/test_sale_combo_configurator.py`, `addons/sale/tests/test_controllers.py`, `addons/sale/tests/test_sale_prices.py`, `addons/sale/tests/test_product_attribute_value.py`, `addons/sale/tests/test_taxes_global_discount.py`, `addons/sale/tests/test_taxes_tax_totals_summary.py`, `addons/sale/tests/test_import_files.py`, `addons/sale/tests/test_sale_report.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 64; representative identifiers: `group_auto_done_setting`, `group_discount_per_so_line`, `group_warning_sale`, `group_proforma_sales`, `group_services_and_material`, `report_saleorder_document`, `report_saleorder_raw`, `report_saleorder`, `report_saleorder_pro_forma`, `document_tax_totals`, `quote_document_layout_preview`, `action_report_saleorder`, `action_report_pro_forma_invoice`, `view_account_invoice_report_search_inherit`, `account_invoice_report_view_tree`, `action_account_invoice_report_salesteam`, `view_order_product_pivot`, `view_order_product_graph`, `sale_report_graph_pie`, `sale_report_graph_bar`
- Menus: 21; representative evidence: `addons/sale/views/sale_menus.xml:4`, `addons/sale/views/sale_menus.xml:10`, `addons/sale/views/sale_menus.xml:14`, `addons/sale/views/sale_menus.xml:21`, `addons/sale/views/sale_menus.xml:27`, `addons/sale/views/sale_menus.xml:34`, `addons/sale/views/sale_menus.xml:42`, `addons/sale/views/sale_menus.xml:47`, `addons/sale/views/sale_menus.xml:51`, `addons/sale/views/sale_menus.xml:57`, `addons/sale/views/sale_menus.xml:66`, `addons/sale/views/sale_menus.xml:68`
- Templates: 17; representative evidence: `addons/sale/report/ir_actions_report_templates.xml:3`, `addons/sale/report/ir_actions_report_templates.xml:477`, `addons/sale/report/ir_actions_report_templates.xml:485`, `addons/sale/report/ir_actions_report_templates.xml:489`, `addons/sale/report/ir_actions_report_templates.xml:500`, `addons/sale/report/ir_actions_report_templates.xml:502`, `addons/sale/views/sale_portal_templates.xml:4`, `addons/sale/views/sale_portal_templates.xml:21`, `addons/sale/views/sale_portal_templates.xml:57`, `addons/sale/views/sale_portal_templates.xml:125`, `addons/sale/views/sale_portal_templates.xml:501`, `addons/sale/views/sale_portal_templates.xml:528`
- View/action field declarations: 208; representative evidence: `addons/sale/report/ir_actions_report.xml:6`, `addons/sale/report/ir_actions_report.xml:16`, `addons/sale/report/account_invoice_report_views.xml:6`, `addons/sale/report/account_invoice_report_views.xml:8`, `addons/sale/report/account_invoice_report_views.xml:23`, `addons/sale/report/account_invoice_report_views.xml:25`, `addons/sale/report/account_invoice_report_views.xml:34`, `addons/sale/report/account_invoice_report_views.xml:35`, `addons/sale/report/sale_report_views.xml:6`, `addons/sale/report/sale_report_views.xml:7`, `addons/sale/report/sale_report_views.xml:18`, `addons/sale/report/sale_report_views.xml:19`
- Browser assets: 69; representative files: `addons/sale/static/tests/sale_order_section_quantity.test.js`, `addons/sale/static/tests/sale_product_field.test.js`, `addons/sale/static/tests/sale_test_helpers.js`, `addons/sale/static/tests/sale_order_line_field.test.js`, `addons/sale/static/src/js/sale_product_mixin.js`, `addons/sale/static/src/js/combo_configurator_utils.js`, `addons/sale/static/src/js/discount_menu_widget.js`, `addons/sale/static/src/js/combo_menu_widget.js`, `addons/sale/static/src/js/labeled_field_short_labels.js`, `addons/sale/static/src/js/sale_utils.js`, `addons/sale/static/src/interactions/sale_sidebar.js`, `addons/sale/static/src/interactions/portal_prepayment.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale/__manifest__.py`
- **HTTP entry points:** `addons/sale/controllers/portal.py:106`, `addons/sale/controllers/portal.py:114`, `addons/sale/controllers/portal.py:132`, `addons/sale/controllers/portal.py:347`, `addons/sale/controllers/portal.py:407`, `addons/sale/controllers/portal.py:447`, `addons/sale/controllers/portal.py:475`, `addons/sale/controllers/portal.py:508`, `addons/sale/controllers/product_configurator.py:9`, `addons/sale/controllers/product_configurator.py:123`, `addons/sale/controllers/product_configurator.py:144`, `addons/sale/controllers/product_configurator.py:211`
- **Scheduled entry points:** `addons/sale/__manifest__.py`, `addons/sale/const.py`, `addons/sale/__init__.py`, `addons/sale/models/sale_order.py`, `addons/sale/models/ir_config_parameter.py`, `addons/sale/models/account_move.py`, `addons/sale/models/payment_transaction.py`, `addons/sale/models/res_company.py`, `addons/sale/wizard/account_accrued_orders_wizard_views.xml`, `addons/sale/data/ir_cron.xml`, `addons/sale/views/sale_order_views.xml`, `addons/sale/tests/test_sale_order.py`
- **Report entry points:** `addons/sale/models/sale_order.py`, `addons/sale/models/ir_actions_report.py`, `addons/sale/controllers/portal.py`, `addons/sale/report/ir_actions_report.xml`

## 7. Database interactions

- Model declarations: 30
- Representative model evidence: inherits `product.category` (addons/sale/models/product_category.py:6); inherits `res.partner` (addons/sale/models/res_partner.py:7); `sale.order` (addons/sale/models/sale_order.py:34); inherits `product.product` (addons/sale/models/product_product.py:10); inherits `product.attribute.custom.value` (addons/sale/models/product_product.py:171); inherits `ir.config_parameter` (addons/sale/models/ir_config_parameter.py:9); inherits `product.template` (addons/sale/models/product_template.py:11); inherits `res.groups` (addons/sale/models/res_groups.py:6); inherits `account.analytic.applicability` (addons/sale/models/account_analytic_applicability.py:6); inherits `account.analytic.line` (addons/sale/models/account_analytic_line.py:8); inherits `ir.actions.report` (addons/sale/models/ir_actions_report.py:7); inherits `crm.team` (addons/sale/models/crm_team.py:7); inherits `product.pricelist.item` (addons/sale/models/product_pricelist_item.py:4); inherits `product.document` (addons/sale/models/product_document.py:6); inherits `utm.campaign` (addons/sale/models/utm_campaign.py:7); `account.move` (addons/sale/models/account_move.py:7); inherits `account.move.line` (addons/sale/models/account_move_line.py:8); inherits `payment.transaction` (addons/sale/models/payment_transaction.py:10); `sale.order.line` (addons/sale/models/sale_order_line.py:12); inherits `payment.provider` (addons/sale/models/payment_provider.py:6); inherits `res.company` (addons/sale/models/res_company.py:12); inherits `account.invoice.report` (addons/sale/report/account_invoice_report.py:6); `sale.report` (addons/sale/report/sale_report.py:11); `sale.advance.payment.inv` (addons/sale/wizard/sale_make_invoice_advance.py:10); inherits `base.document.layout` (addons/sale/wizard/base_document_layout.py:6); inherits `res.config.settings` (addons/sale/wizard/res_config_settings.py:6); inherits `account.accrued.orders.wizard` (addons/sale/wizard/accrued_orders.py:9); `sale.order.discount` (addons/sale/wizard/sale_order_discount.py:9); inherits `payment.link.wizard` (addons/sale/wizard/payment_link_wizard.py:8); `sale.mass.cancel.orders` (addons/sale/wizard/mass_cancel_orders.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 4
- Route declarations: 14
- Route evidence: `addons/sale/controllers/portal.py:106`, `addons/sale/controllers/portal.py:114`, `addons/sale/controllers/portal.py:132`, `addons/sale/controllers/portal.py:347`, `addons/sale/controllers/portal.py:407`, `addons/sale/controllers/portal.py:447`, `addons/sale/controllers/portal.py:475`, `addons/sale/controllers/portal.py:508`, `addons/sale/controllers/product_configurator.py:9`, `addons/sale/controllers/product_configurator.py:123`, `addons/sale/controllers/product_configurator.py:144`, `addons/sale/controllers/product_configurator.py:211`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sales_team`, `account_payment`, `utm`
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

- `addons/sale/README.md`
- `addons/sale/__init__.py`
- `addons/sale/__manifest__.py`
- `addons/sale/const.py`
- `addons/sale/controllers/__init__.py`
- `addons/sale/controllers/combo_configurator.py`
- `addons/sale/controllers/portal.py`
- `addons/sale/controllers/product_configurator.py`
- `addons/sale/data/ir_config_parameter.xml`
- `addons/sale/data/ir_cron.xml`
- `addons/sale/data/ir_sequence_data.xml`
- `addons/sale/data/mail_message_subtype_data.xml`
- `addons/sale/data/mail_template_data.xml`
- `addons/sale/data/portal_entry_data.xml`
- `addons/sale/data/product_demo.xml`
- `addons/sale/data/sale_demo.xml`
- `addons/sale/data/sale_tour.xml`
- `addons/sale/i18n/af.po`
- `addons/sale/i18n/am.po`
- `addons/sale/i18n/ar.po`
- `addons/sale/i18n/az.po`
- `addons/sale/i18n/bg.po`
- `addons/sale/i18n/bs.po`
- `addons/sale/i18n/ca.po`
- `addons/sale/i18n/cs.po`
- `addons/sale/i18n/da.po`
- `addons/sale/i18n/de.po`
- `addons/sale/i18n/el.po`
- `addons/sale/i18n/en_AU.po`
- `addons/sale/i18n/es.po`
- `addons/sale/i18n/es_419.po`
- `addons/sale/i18n/es_CL.po`
- `addons/sale/i18n/et.po`
- `addons/sale/i18n/eu.po`
- `addons/sale/i18n/fa.po`
- `addons/sale/i18n/fi.po`
- `addons/sale/i18n/fo.po`
- `addons/sale/i18n/fr.po`
- `addons/sale/i18n/fr_CA.po`
- `addons/sale/i18n/gl.po`
- `addons/sale/i18n/gu.po`
- `addons/sale/i18n/he.po`
- `addons/sale/i18n/hi.po`
- `addons/sale/i18n/hr.po`
- `addons/sale/i18n/hu.po`
- `addons/sale/i18n/id.po`
- `addons/sale/i18n/is.po`
- `addons/sale/i18n/it.po`
- `addons/sale/i18n/ja.po`
- `addons/sale/i18n/ka.po`
- `addons/sale/i18n/kab.po`
- `addons/sale/i18n/km.po`
- `addons/sale/i18n/ko.po`
- `addons/sale/i18n/ku.po`
- `addons/sale/i18n/lb.po`
- `addons/sale/i18n/lo.po`
- `addons/sale/i18n/lt.po`
- `addons/sale/i18n/lv.po`
- `addons/sale/i18n/mk.po`
- `addons/sale/i18n/mn.po`
- `addons/sale/i18n/my.po`
- `addons/sale/i18n/nb.po`
- `addons/sale/i18n/nl.po`
- `addons/sale/i18n/pl.po`
- `addons/sale/i18n/pt.po`
- `addons/sale/i18n/pt_BR.po`
- `addons/sale/i18n/ro.po`
- `addons/sale/i18n/ru.po`
- `addons/sale/i18n/sale.pot`
- `addons/sale/i18n/sk.po`
- `addons/sale/i18n/sl.po`
- `addons/sale/i18n/sq.po`
- `addons/sale/i18n/sr@latin.po`
- `addons/sale/i18n/sv.po`
- `addons/sale/i18n/th.po`
- `addons/sale/i18n/tr.po`
- `addons/sale/i18n/uk.po`
- `addons/sale/i18n/uz.po`
- `addons/sale/i18n/vi.po`
- `addons/sale/i18n/zh_CN.po`
- `addons/sale/i18n/zh_TW.po`
- `addons/sale/models/__init__.py`
- `addons/sale/models/account_analytic_applicability.py`
- `addons/sale/models/account_analytic_line.py`
- `addons/sale/models/account_move.py`
- `addons/sale/models/account_move_line.py`
- `addons/sale/models/crm_team.py`
- `addons/sale/models/ir_actions_report.py`
- `addons/sale/models/ir_config_parameter.py`
- `addons/sale/models/payment_provider.py`
- `addons/sale/models/payment_transaction.py`
- `addons/sale/models/product_category.py`
- `addons/sale/models/product_document.py`
- `addons/sale/models/product_pricelist_item.py`
- `addons/sale/models/product_product.py`
- `addons/sale/models/product_template.py`
- `addons/sale/models/res_company.py`
- `addons/sale/models/res_groups.py`
- `addons/sale/models/res_partner.py`
- `addons/sale/models/sale_order.py`
- `addons/sale/models/sale_order_line.py`
- `addons/sale/models/utm_campaign.py`
- `addons/sale/populate/benchmarks.xml`
- `addons/sale/populate/populate_demo.xml`
- `addons/sale/report/__init__.py`
- `addons/sale/report/account_invoice_report.py`
- `addons/sale/report/account_invoice_report_views.xml`
- `addons/sale/report/ir_actions_report.xml`
- `addons/sale/report/ir_actions_report_templates.xml`
- `addons/sale/report/sale_report.py`
- `addons/sale/report/sale_report_views.xml`
- `addons/sale/security/ir.access.csv`
- `addons/sale/security/res_groups.xml`
- `addons/sale/static/description/icon.png`
- `addons/sale/static/description/icon.svg`
- `addons/sale/static/description/icon_hi.png`
- `addons/sale/static/img/advance_product_0-image.jpg`
- `addons/sale/static/img/btn_paynowcc_lg.gif`
- `addons/sale/static/img/floor_protection-image.jpg`
- `addons/sale/static/src/img/bag.svg`
- `addons/sale/static/src/img/onboarding_quotation_order_tooltip.jpg`
- `addons/sale/static/src/img/sales_quotation_thumbnail.webp`
- `addons/sale/static/src/img/services_and_material_empty_dark.svg`
- `addons/sale/static/src/img/services_and_material_empty_light.svg`
- `addons/sale/static/src/interactions/portal_prepayment.js`
- `addons/sale/static/src/interactions/sale_portal.js`
- `addons/sale/static/src/interactions/sale_sidebar.js`
- `addons/sale/static/src/js/badge_extra_price/badge_extra_price.js`
- `addons/sale/static/src/js/badge_extra_price/badge_extra_price.xml`
- `addons/sale/static/src/js/combo_configurator_dialog/combo_configurator_dialog.js`
- `addons/sale/static/src/js/combo_configurator_dialog/combo_configurator_dialog.scss`
- `addons/sale/static/src/js/combo_configurator_dialog/combo_configurator_dialog.xml`
- `addons/sale/static/src/js/combo_configurator_utils.js`
- `addons/sale/static/src/js/combo_menu_widget.js`
- `addons/sale/static/src/js/dashboard/dashboard.dark.scss`
- `addons/sale/static/src/js/dashboard/dashboard.js`
- `addons/sale/static/src/js/dashboard/dashboard.scss`
- `addons/sale/static/src/js/dashboard/dashboard.xml`
- `addons/sale/static/src/js/date_filter_button/date_filter_button.js`
- `addons/sale/static/src/js/date_filter_button/date_filter_button.xml`
- `addons/sale/static/src/js/discount_menu_widget.js`
- `addons/sale/static/src/js/extra_total_field/extra_total_field.js`
- `addons/sale/static/src/js/extra_total_field/extra_total_field.xml`
- `addons/sale/static/src/js/labeled_field_short_labels.js`
- `addons/sale/static/src/js/labeled_float_field/labeled_float_field.js`
- `addons/sale/static/src/js/labeled_float_field/labeled_float_field.xml`
- `addons/sale/static/src/js/labeled_monetary_field/labeled_monetary_field.js`
- `addons/sale/static/src/js/labeled_monetary_field/labeled_monetary_field.xml`
- `addons/sale/static/src/js/labeled_percentage_field/labeled_percentage_field.js`
- `addons/sale/static/src/js/labeled_percentage_field/labeled_percentage_field.xml`
- `addons/sale/static/src/js/models/product_combo.js`
- `addons/sale/static/src/js/models/product_combo_item.js`
- `addons/sale/static/src/js/models/product_product.js`
- `addons/sale/static/src/js/models/product_template_attribute_line.js`
- `addons/sale/static/src/js/models/product_template_attribute_value.js`
- `addons/sale/static/src/js/product/product.js`
- `addons/sale/static/src/js/product/product.scss`
- `addons/sale/static/src/js/product/product.xml`
- `addons/sale/static/src/js/product_card/product_card.js`
- `addons/sale/static/src/js/product_card/product_card.scss`
- `addons/sale/static/src/js/product_card/product_card.xml`
- `addons/sale/static/src/js/product_configurator_dialog/product_configurator_dialog.js`
- `addons/sale/static/src/js/product_configurator_dialog/product_configurator_dialog.xml`
- `addons/sale/static/src/js/product_list/product_list.js`
- `addons/sale/static/src/js/product_list/product_list.scss`
- `addons/sale/static/src/js/product_list/product_list.xml`
- `addons/sale/static/src/js/product_template_attribute_line/product_template_attribute_line.js`
- `addons/sale/static/src/js/product_template_attribute_line/product_template_attribute_line.scss`
- `addons/sale/static/src/js/product_template_attribute_line/product_template_attribute_line.xml`
- `addons/sale/static/src/js/quantity_availability/qty_at_date_widget.js`
- `addons/sale/static/src/js/quantity_availability/qty_at_date_widget.xml`
- `addons/sale/static/src/js/quantity_buttons/quantity_buttons.js`
- `addons/sale/static/src/js/quantity_buttons/quantity_buttons.scss`
- `addons/sale/static/src/js/quantity_buttons/quantity_buttons.xml`
- `addons/sale/static/src/js/sale_action_helper/sale_action_helper.js`
- `addons/sale/static/src/js/sale_action_helper/sale_action_helper.scss`
- `addons/sale/static/src/js/sale_action_helper/sale_action_helper.xml`
- `addons/sale/static/src/js/sale_action_helper/sale_action_helper_dialog.js`
- `addons/sale/static/src/js/sale_action_helper/sale_action_helper_dialog.xml`
- `addons/sale/static/src/js/sale_label_text/sale_label_text.js`
- `addons/sale/static/src/js/sale_label_text/sale_label_text.xml`
- `addons/sale/static/src/js/sale_label_text/sale_lebel_text.scss`
- `addons/sale/static/src/js/sale_line_number/sale_line_number.scss`
- `addons/sale/static/src/js/sale_line_number/sale_line_number_widget.js`
- `addons/sale/static/src/js/sale_line_number/sale_line_number_widget.xml`
- `addons/sale/static/src/js/sale_order_line_field/sale_order_line_field.js`
- `addons/sale/static/src/js/sale_order_line_field/sale_order_line_field.scss`
- `addons/sale/static/src/js/sale_order_line_field/sale_order_line_field.xml`
- `addons/sale/static/src/js/sale_product_field/sale_product_field.js`
- `addons/sale/static/src/js/sale_product_field/sale_product_field.scss`
- `addons/sale/static/src/js/sale_product_field/sale_product_field.xml`
- `addons/sale/static/src/js/sale_product_mixin.js`
- `addons/sale/static/src/js/sale_utils.js`
- `addons/sale/static/src/js/section_line_record/section_line_record.js`
- `addons/sale/static/src/js/tours/combo_configurator_tour_utils.js`
- `addons/sale/static/src/js/tours/product_configurator_tour_utils.js`
- `addons/sale/static/src/js/tours/sale.js`
- `addons/sale/static/src/js/tours/tour_utils.js`
- `addons/sale/static/src/js/upload_rfq_cog_menu/upload_rfq_cog_menu.js`
- `addons/sale/static/src/js/upload_rfq_cog_menu/upload_rfq_cog_menu.xml`
- `addons/sale/static/src/scss/sale_onboarding.scss`
- `addons/sale/static/src/scss/sale_order_line_kanban.scss`
- `addons/sale/static/src/scss/sale_portal.scss`
- `addons/sale/static/src/scss/sale_report.scss`
- `addons/sale/static/src/scss/services_and_material.dark.scss`
- `addons/sale/static/src/scss/services_and_material.scss`
- `addons/sale/static/src/views/dashboard_kanban_view/dashboard_kanban_view.js`
- `addons/sale/static/src/views/dashboard_kanban_view/dashboard_kanban_view.xml`
- `addons/sale/static/src/views/dashboard_list_view/dashboard_list_view.js`
- `addons/sale/static/src/views/dashboard_list_view/dashboard_list_view.xml`
- `addons/sale/static/src/views/sale_file_upload_kanban/sale_file_upload_kanban_controller.js`
- `addons/sale/static/src/views/sale_file_upload_kanban/sale_file_upload_kanban_renderer.js`
- `addons/sale/static/src/views/sale_file_upload_kanban/sale_file_upload_kanban_view.js`
- `addons/sale/static/src/views/sale_file_upload_list/sale_file_upload_list_controller.js`
- `addons/sale/static/src/views/sale_file_upload_list/sale_file_upload_list_renderer.js`
- `addons/sale/static/src/views/sale_file_upload_list/sale_file_upload_list_view.js`
- `addons/sale/static/src/views/sale_onboarding_kanban/sale_onboarding_kanban_renderer.js`
- `addons/sale/static/src/views/sale_onboarding_kanban/sale_onboarding_kanban_renderer.xml`
- `addons/sale/static/src/views/sale_onboarding_kanban/sale_onboarding_kanban_view.js`
- `addons/sale/static/src/views/sale_onboarding_list/sale_onboarding_list_renderer.js`
- `addons/sale/static/src/views/sale_onboarding_list/sale_onboarding_list_renderer.xml`
- `addons/sale/static/src/views/sale_onboarding_list/sale_onboarding_list_view.js`
- `addons/sale/static/src/views/sale_order_form_view/sale_order_form_view.js`
- `addons/sale/static/src/views/sale_order_form_view/sale_order_static_list.js`
- `addons/sale/static/src/xml/combo_menu_widget.xml`
- `addons/sale/static/src/xml/discount_menu_widget.xml`
- `addons/sale/static/tests/mock_server/mock_models/sale_order.js`
- `addons/sale/static/tests/mock_server/mock_models/sale_order_line.js`
- `addons/sale/static/tests/sale_order_line_field.test.js`
- `addons/sale/static/tests/sale_order_section_quantity.test.js`
- `addons/sale/static/tests/sale_product_field.test.js`
- `addons/sale/static/tests/sale_test_helpers.js`
- `addons/sale/static/tests/tours/mail_attachment_removal_test_tour.js`
- `addons/sale/static/tests/tours/product_attribute_value_tour.js`
- `addons/sale/static/tests/tours/sale_catalog.js`
- `addons/sale/static/tests/tours/sale_combo_configurator.js`
- `addons/sale/static/tests/tours/sale_combo_configurator_preconfigure_unconfigurable_ptals.js`
- `addons/sale/static/tests/tours/sale_combo_configurator_preselect_single_unconfigurable_items.js`
- `addons/sale/static/tests/tours/sale_order_product_uom_integrity.js`
- `addons/sale/static/tests/tours/sale_signature.js`
- `addons/sale/static/xls/quotations_import_template.xlsx`
- `addons/sale/tests/__init__.py`
- `addons/sale/tests/common.py`
- `addons/sale/tests/product_configurator_common.py`
- `addons/sale/tests/test_access_rights.py`
- `addons/sale/tests/test_accrued_sale_orders.py`
- `addons/sale/tests/test_analytic_to_sale_to_invoice.py`
- `addons/sale/tests/test_common.py`
- `addons/sale/tests/test_controllers.py`
- `addons/sale/tests/test_credit_limit.py`
- Additional source files not expanded in this page: 56; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
