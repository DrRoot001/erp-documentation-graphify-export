# Module: website_sale

- **Module ID:** MOD-634
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_sale`
- **Manifest:** `addons/website_sale/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Sell your products online

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 567 files, including 123 Python, 108 XML, and 165 JavaScript/TypeScript files. The manifest declares dependencies: `website`, `sale`, `website_payment`, `website_mail`, `portal_rating`, `digest`, `delivery`, `html_builder`.

## 2. Module structure

- Model/business logic files: 42
- Controller/API files: 17
- XML/data/view/template files: 108
- Browser asset files: 165
- Security files: 3
- Test files: 58
- Scheduled/automation evidence files: 15
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_sale/security/ir.access.csv`, `addons/website_sale/security/res_groups.xml`, `addons/website_sale/security/ir_access.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 42 model declarations, 996 methods, 4 constraint handlers, 5 onchange handlers, and 32 dependency declarations.
- **Evidence:** `addons/website_sale/models/res_partner.py:7`, `addons/website_sale/models/sale_order.py:20`, `addons/website_sale/models/product_product.py:12`, `addons/website_sale/models/product_combo.py:6`, `addons/website_sale/models/website_track.py:6`, `addons/website_sale/models/product_attribute.py:6`, `addons/website_sale/models/product_feed.py:19`, `addons/website_sale/models/digest.py:6`, `addons/website_sale/models/product_template.py:38`, `addons/website_sale/models/website_menu.py:6`, `addons/website_sale/models/res_groups.py:6`, `addons/website_sale/models/website_snippet_filter.py:11`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 17 controller files and 62 route declarations.
- **Evidence:** `addons/website_sale/controllers/product_feed.py:10`, `addons/website_sale/controllers/donation.py:5`, `addons/website_sale/controllers/cart.py:19`, `addons/website_sale/controllers/cart.py:82`, `addons/website_sale/controllers/cart.py:315`, `addons/website_sale/controllers/cart.py:373`, `addons/website_sale/controllers/wishlist.py:10`, `addons/website_sale/controllers/wishlist.py:37`, `addons/website_sale/controllers/wishlist.py:52`, `addons/website_sale/controllers/wishlist.py:65`, `addons/website_sale/controllers/wishlist.py:71`, `addons/website_sale/controllers/comparison.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 108 XML files and 165 JavaScript/TypeScript files; static XML analysis found 565 record/template/menu identifiers.
- **Evidence:** `addons/website_sale/security/res_groups.xml:5`, `addons/website_sale/security/res_groups.xml:9`, `addons/website_sale/security/res_groups.xml:13`, `addons/website_sale/security/res_groups.xml:17`, `addons/website_sale/security/res_groups.xml:22`, `addons/website_sale/security/res_groups.xml:28`, `addons/website_sale/security/ir_access.xml:11`, `addons/website_sale/security/ir_access.xml:14`, `addons/website_sale/report/sale_report_views.xml:3`, `addons/website_sale/report/sale_report_views.xml:40`, `addons/website_sale/report/sale_report_views.xml:52`, `addons/website_sale/report/sale_report_views.xml:63`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 3 security-directory files are present.
- **Evidence:** `addons/website_sale/security/ir.access.csv`, `addons/website_sale/security/res_groups.xml`, `addons/website_sale/security/ir_access.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 15 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/website_sale/__manifest__.py`, `addons/website_sale/models/sale_order.py`, `addons/website_sale/models/product_product.py`, `addons/website_sale/models/product_template.py`, `addons/website_sale/models/withdrawal_request.py`, `addons/website_sale/models/res_config_settings.py`, `addons/website_sale/models/product_wishlist.py`, `addons/website_sale/models/website.py`, `addons/website_sale/data/ir_actions_server_data.xml`, `addons/website_sale/data/website_snippet_filter_data.xml`, `addons/website_sale/data/ir_cron_data.xml`, `addons/website_sale/views/product_feed_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/website_sale/controllers/main.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 58 test files are present.
- **Evidence:** `addons/website_sale/tests/test_product_public_category.py`, `addons/website_sale/tests/test_product_configurator.py`, `addons/website_sale/tests/test_google_analytics.py`, `addons/website_sale/tests/test_fuzzy.py`, `addons/website_sale/tests/test_ecommerce_access.py`, `addons/website_sale/tests/test_donation_snippets.py`, `addons/website_sale/tests/test_dashboard.py`, `addons/website_sale/tests/test_performance.py`, `addons/website_sale/tests/test_shop_redirects.py`, `addons/website_sale/tests/test_sale_process.py`, `addons/website_sale/tests/test_main_controller.py`, `addons/website_sale/tests/test_abandoned_cart.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 108; representative identifiers: `group_product_price_comparison`, `group_automate_suggested_products`, `group_product_feed`, `group_unpublish_out_of_stock`, `base.group_user`, `sales_team.group_sale_manager`, `product.product_pricelist_comp_rule`, `product.product_pricelist_item_comp_rule`, `sale_report_view_search_website`, `sale_report_view_pivot_website`, `sale_report_view_graph_website`, `sale_report_view_tree`, `sale_report_action_dashboard`, `sale_report_action_view_pivot_website`, `sale_report_action_view_graph_website`, `sale_report_action_carts`, `sale_report_action_view_pivot_carts`, `sale_report_action_view_graph_carts`, `Product Base unit price`, `Product`
- Menus: 19; representative evidence: `addons/website_sale/views/website_sale_menus.xml:9`, `addons/website_sale/views/website_sale_menus.xml:15`, `addons/website_sale/views/website_sale_menus.xml:21`, `addons/website_sale/views/website_sale_menus.xml:26`, `addons/website_sale/views/website_sale_menus.xml:32`, `addons/website_sale/views/website_sale_menus.xml:39`, `addons/website_sale/views/website_sale_menus.xml:47`, `addons/website_sale/views/website_sale_menus.xml:52`, `addons/website_sale/views/website_sale_menus.xml:58`, `addons/website_sale/views/website_sale_menus.xml:65`, `addons/website_sale/views/website_sale_menus.xml:71`, `addons/website_sale/views/website_sale_menus.xml:77`
- Templates: 191; representative evidence: `addons/website_sale/templates/product_page_templates.xml:4`, `addons/website_sale/templates/product_page_templates.xml:15`, `addons/website_sale/templates/product_page_templates.xml:180`, `addons/website_sale/templates/product_page_templates.xml:406`, `addons/website_sale/templates/product_page_templates.xml:433`, `addons/website_sale/templates/product_page_templates.xml:448`, `addons/website_sale/templates/product_page_templates.xml:486`, `addons/website_sale/templates/product_page_templates.xml:534`, `addons/website_sale/templates/product_page_templates.xml:629`, `addons/website_sale/templates/product_page_templates.xml:679`, `addons/website_sale/templates/product_page_templates.xml:740`, `addons/website_sale/templates/product_page_templates.xml:753`
- View/action field declarations: 138; representative evidence: `addons/website_sale/report/sale_report_views.xml:5`, `addons/website_sale/report/sale_report_views.xml:6`, `addons/website_sale/report/sale_report_views.xml:42`, `addons/website_sale/report/sale_report_views.xml:43`, `addons/website_sale/report/sale_report_views.xml:54`, `addons/website_sale/report/sale_report_views.xml:55`, `addons/website_sale/report/sale_report_views.xml:65`, `addons/website_sale/report/sale_report_views.xml:67`, `addons/website_sale/report/sale_report_views.xml:77`, `addons/website_sale/report/sale_report_views.xml:79`, `addons/website_sale/report/sale_report_views.xml:92`, `addons/website_sale/report/sale_report_views.xml:99`
- Browser assets: 165; representative files: `addons/website_sale/static/src/website_builder/wishlist_page_option_plugin.js`, `addons/website_sale/static/src/website_builder/dynamic_snippet_products_option.js`, `addons/website_sale/static/src/website_builder/product_tag_image_option_plugin.js`, `addons/website_sale/static/src/website_builder/product_variant_option_plugin.js`, `addons/website_sale/static/src/website_builder/product_page_option.js`, `addons/website_sale/static/src/website_builder/product_template_option_plugin.js`, `addons/website_sale/static/src/website_builder/products_searchbar_option_plugin.js`, `addons/website_sale/static/src/website_builder/website_sale_form_editor.edit.js`, `addons/website_sale/static/src/website_builder/snippet_model.js`, `addons/website_sale/static/src/website_builder/footer_option_plugin.js`, `addons/website_sale/static/src/website_builder/product_ribbon_options.js`, `addons/website_sale/static/src/website_builder/product_template_option.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_sale/__manifest__.py`
- **HTTP entry points:** `addons/website_sale/controllers/product_feed.py:10`, `addons/website_sale/controllers/donation.py:5`, `addons/website_sale/controllers/cart.py:19`, `addons/website_sale/controllers/cart.py:82`, `addons/website_sale/controllers/cart.py:315`, `addons/website_sale/controllers/cart.py:373`, `addons/website_sale/controllers/wishlist.py:10`, `addons/website_sale/controllers/wishlist.py:37`, `addons/website_sale/controllers/wishlist.py:52`, `addons/website_sale/controllers/wishlist.py:65`, `addons/website_sale/controllers/wishlist.py:71`, `addons/website_sale/controllers/comparison.py:7`
- **Scheduled entry points:** `addons/website_sale/__manifest__.py`, `addons/website_sale/models/sale_order.py`, `addons/website_sale/models/product_product.py`, `addons/website_sale/models/product_template.py`, `addons/website_sale/models/withdrawal_request.py`, `addons/website_sale/models/res_config_settings.py`, `addons/website_sale/models/product_wishlist.py`, `addons/website_sale/models/website.py`, `addons/website_sale/data/ir_actions_server_data.xml`, `addons/website_sale/data/website_snippet_filter_data.xml`, `addons/website_sale/data/ir_cron_data.xml`, `addons/website_sale/views/product_feed_views.xml`
- **Report entry points:** `addons/website_sale/controllers/main.py`

## 7. Database interactions

- Model declarations: 42
- Representative model evidence: inherits `res.partner` (addons/website_sale/models/res_partner.py:7); `sale.order` (addons/website_sale/models/sale_order.py:20); `product.product` (addons/website_sale/models/product_product.py:12); inherits `product.combo` (addons/website_sale/models/product_combo.py:6); inherits `website.track` (addons/website_sale/models/website_track.py:6); inherits `product.attribute` (addons/website_sale/models/product_attribute.py:6); `product.feed` (addons/website_sale/models/product_feed.py:19); inherits `digest.digest` (addons/website_sale/models/digest.py:6); `product.template` (addons/website_sale/models/product_template.py:38); inherits `website.menu` (addons/website_sale/models/website_menu.py:6); inherits `res.groups` (addons/website_sale/models/res_groups.py:6); inherits `website.snippet.filter` (addons/website_sale/models/website_snippet_filter.py:11); `product.attribute.category` (addons/website_sale/models/product_attribute_category.py:6); `delivery.carrier` (addons/website_sale/models/delivery_carrier.py:11); `withdrawal.request` (addons/website_sale/models/withdrawal_request.py:12); inherits `res.config.settings` (addons/website_sale/models/res_config_settings.py:6); inherits `product.pricelist` (addons/website_sale/models/product_pricelist.py:7); inherits `product.template.attribute.value` (addons/website_sale/models/product_template_attribute_value.py:8); `website.checkout.step` (addons/website_sale/models/website_checkout_step.py:9); inherits `product.template.attribute.line` (addons/website_sale/models/product_template_attribute_line.py:8); inherits `crm.team` (addons/website_sale/models/crm_team.py:6); inherits `website.visitor` (addons/website_sale/models/website_visitor.py:6); inherits `ir.http` (addons/website_sale/models/ir_http.py:8); inherits `product.pricelist.item` (addons/website_sale/models/product_pricelist_item.py:6); inherits `ir.module.module` (addons/website_sale/models/ir_module_module.py:7); inherits `product.document` (addons/website_sale/models/product_document.py:6); `product.wishlist` (addons/website_sale/models/product_wishlist.py:9); `product.ribbon` (addons/website_sale/models/product_ribbon.py:7); inherits `theme.utils` (addons/website_sale/models/theme_utils.py:6); inherits `res.users` (addons/website_sale/models/res_users.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 17
- Route declarations: 62
- Route evidence: `addons/website_sale/controllers/product_feed.py:10`, `addons/website_sale/controllers/donation.py:5`, `addons/website_sale/controllers/cart.py:19`, `addons/website_sale/controllers/cart.py:82`, `addons/website_sale/controllers/cart.py:315`, `addons/website_sale/controllers/cart.py:373`, `addons/website_sale/controllers/wishlist.py:10`, `addons/website_sale/controllers/wishlist.py:37`, `addons/website_sale/controllers/wishlist.py:52`, `addons/website_sale/controllers/wishlist.py:65`, `addons/website_sale/controllers/wishlist.py:71`, `addons/website_sale/controllers/comparison.py:7`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website`, `sale`, `website_payment`, `website_mail`, `portal_rating`, `digest`, `delivery`, `html_builder`
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

- `addons/website_sale/README.md`
- `addons/website_sale/__init__.py`
- `addons/website_sale/__manifest__.py`
- `addons/website_sale/const.py`
- `addons/website_sale/controllers/__init__.py`
- `addons/website_sale/controllers/cart.py`
- `addons/website_sale/controllers/combo_configurator.py`
- `addons/website_sale/controllers/comparison.py`
- `addons/website_sale/controllers/delivery.py`
- `addons/website_sale/controllers/donation.py`
- `addons/website_sale/controllers/main.py`
- `addons/website_sale/controllers/payment.py`
- `addons/website_sale/controllers/portal.py`
- `addons/website_sale/controllers/product_configurator.py`
- `addons/website_sale/controllers/product_feed.py`
- `addons/website_sale/controllers/reorder.py`
- `addons/website_sale/controllers/sale.py`
- `addons/website_sale/controllers/thread.py`
- `addons/website_sale/controllers/variant.py`
- `addons/website_sale/controllers/website.py`
- `addons/website_sale/controllers/wishlist.py`
- `addons/website_sale/data/data.xml`
- `addons/website_sale/data/demo.xml`
- `addons/website_sale/data/digest_data.xml`
- `addons/website_sale/data/donation_data.xml`
- `addons/website_sale/data/ir_actions_server_data.xml`
- `addons/website_sale/data/ir_cron_data.xml`
- `addons/website_sale/data/mail_template_data.xml`
- `addons/website_sale/data/product_attribute_category_data.xml`
- `addons/website_sale/data/product_attribute_category_demo.xml`
- `addons/website_sale/data/product_attribute_data.xml`
- `addons/website_sale/data/product_ribbon_data.xml`
- `addons/website_sale/data/tour.xml`
- `addons/website_sale/data/website_checkout_step_data.xml`
- `addons/website_sale/data/website_snippet_filter_data.xml`
- `addons/website_sale/i18n/af.po`
- `addons/website_sale/i18n/ar.po`
- `addons/website_sale/i18n/az.po`
- `addons/website_sale/i18n/bg.po`
- `addons/website_sale/i18n/bs.po`
- `addons/website_sale/i18n/ca.po`
- `addons/website_sale/i18n/cs.po`
- `addons/website_sale/i18n/da.po`
- `addons/website_sale/i18n/de.po`
- `addons/website_sale/i18n/el.po`
- `addons/website_sale/i18n/es.po`
- `addons/website_sale/i18n/es_419.po`
- `addons/website_sale/i18n/es_CL.po`
- `addons/website_sale/i18n/et.po`
- `addons/website_sale/i18n/eu.po`
- `addons/website_sale/i18n/fa.po`
- `addons/website_sale/i18n/fi.po`
- `addons/website_sale/i18n/fr.po`
- `addons/website_sale/i18n/gl.po`
- `addons/website_sale/i18n/gu.po`
- `addons/website_sale/i18n/he.po`
- `addons/website_sale/i18n/hi.po`
- `addons/website_sale/i18n/hr.po`
- `addons/website_sale/i18n/hu.po`
- `addons/website_sale/i18n/id.po`
- `addons/website_sale/i18n/is.po`
- `addons/website_sale/i18n/it.po`
- `addons/website_sale/i18n/ja.po`
- `addons/website_sale/i18n/ka.po`
- `addons/website_sale/i18n/kab.po`
- `addons/website_sale/i18n/km.po`
- `addons/website_sale/i18n/ko.po`
- `addons/website_sale/i18n/ku.po`
- `addons/website_sale/i18n/lo.po`
- `addons/website_sale/i18n/lt.po`
- `addons/website_sale/i18n/lv.po`
- `addons/website_sale/i18n/mk.po`
- `addons/website_sale/i18n/mn.po`
- `addons/website_sale/i18n/my.po`
- `addons/website_sale/i18n/nb.po`
- `addons/website_sale/i18n/nl.po`
- `addons/website_sale/i18n/pl.po`
- `addons/website_sale/i18n/pt.po`
- `addons/website_sale/i18n/pt_BR.po`
- `addons/website_sale/i18n/ro.po`
- `addons/website_sale/i18n/ru.po`
- `addons/website_sale/i18n/sk.po`
- `addons/website_sale/i18n/sl.po`
- `addons/website_sale/i18n/sr@latin.po`
- `addons/website_sale/i18n/sv.po`
- `addons/website_sale/i18n/th.po`
- `addons/website_sale/i18n/tr.po`
- `addons/website_sale/i18n/uk.po`
- `addons/website_sale/i18n/uz.po`
- `addons/website_sale/i18n/vi.po`
- `addons/website_sale/i18n/website_sale.pot`
- `addons/website_sale/i18n/zh_CN.po`
- `addons/website_sale/i18n/zh_TW.po`
- `addons/website_sale/models/__init__.py`
- `addons/website_sale/models/account_move.py`
- `addons/website_sale/models/crm_team.py`
- `addons/website_sale/models/delivery_carrier.py`
- `addons/website_sale/models/digest.py`
- `addons/website_sale/models/ir_http.py`
- `addons/website_sale/models/ir_module_module.py`
- `addons/website_sale/models/payment_transaction.py`
- `addons/website_sale/models/product_attribute.py`
- `addons/website_sale/models/product_attribute_category.py`
- `addons/website_sale/models/product_combo.py`
- `addons/website_sale/models/product_document.py`
- `addons/website_sale/models/product_feed.py`
- `addons/website_sale/models/product_image.py`
- `addons/website_sale/models/product_pricelist.py`
- `addons/website_sale/models/product_pricelist_item.py`
- `addons/website_sale/models/product_product.py`
- `addons/website_sale/models/product_public_category.py`
- `addons/website_sale/models/product_ribbon.py`
- `addons/website_sale/models/product_stock_notification.py`
- `addons/website_sale/models/product_tag.py`
- `addons/website_sale/models/product_template.py`
- `addons/website_sale/models/product_template_attribute_line.py`
- `addons/website_sale/models/product_template_attribute_value.py`
- `addons/website_sale/models/product_wishlist.py`
- `addons/website_sale/models/res_company.py`
- `addons/website_sale/models/res_config_settings.py`
- `addons/website_sale/models/res_groups.py`
- `addons/website_sale/models/res_partner.py`
- `addons/website_sale/models/res_users.py`
- `addons/website_sale/models/sale_order.py`
- `addons/website_sale/models/sale_order_line.py`
- `addons/website_sale/models/theme_utils.py`
- `addons/website_sale/models/website.py`
- `addons/website_sale/models/website_checkout_alert_mixin.py`
- `addons/website_sale/models/website_checkout_step.py`
- `addons/website_sale/models/website_menu.py`
- `addons/website_sale/models/website_sale_extra_field.py`
- `addons/website_sale/models/website_snippet_filter.py`
- `addons/website_sale/models/website_track.py`
- `addons/website_sale/models/website_visitor.py`
- `addons/website_sale/models/withdrawal_request.py`
- `addons/website_sale/report/__init__.py`
- `addons/website_sale/report/sale_report.py`
- `addons/website_sale/report/sale_report_views.xml`
- `addons/website_sale/security/ir.access.csv`
- `addons/website_sale/security/ir_access.xml`
- `addons/website_sale/security/res_groups.xml`
- `addons/website_sale/static/description/icon.png`
- `addons/website_sale/static/description/icon.svg`
- `addons/website_sale/static/description/icon_hi.png`
- `addons/website_sale/static/shapes/s_donation_gift.svg`
- `addons/website_sale/static/src/img/categories/bins.jpg`
- `addons/website_sale/static/src/img/categories/boxes.jpg`
- `addons/website_sale/static/src/img/categories/cabinets.jpg`
- `addons/website_sale/static/src/img/categories/desk_components.jpg`
- `addons/website_sale/static/src/img/categories/desks.jpg`
- `addons/website_sale/static/src/img/categories/drawers.jpg`
- `addons/website_sale/static/src/img/categories/furnitures.jpg`
- `addons/website_sale/static/src/img/categories/lamps.jpg`
- `addons/website_sale/static/src/img/categories/placeholder_thumbnail.png`
- `addons/website_sale/static/src/img/categories/shape_mixed_1.png`
- `addons/website_sale/static/src/img/categories/shape_mixed_2.png`
- `addons/website_sale/static/src/img/categories/shape_mixed_3.png`
- `addons/website_sale/static/src/img/categories/shape_mixed_4.png`
- `addons/website_sale/static/src/img/categories/shape_mixed_5.png`
- `addons/website_sale/static/src/img/categories/shape_mixed_6.png`
- `addons/website_sale/static/src/img/categories/shape_mixed_7.png`
- `addons/website_sale/static/src/img/categories/shape_mixed_8.png`
- `addons/website_sale/static/src/img/configurator/product/classic.webp`
- `addons/website_sale/static/src/img/configurator/product/focused.webp`
- `addons/website_sale/static/src/img/configurator/product/functional.webp`
- `addons/website_sale/static/src/img/configurator/product/image_grid.webp`
- `addons/website_sale/static/src/img/configurator/product/large_grid.webp`
- `addons/website_sale/static/src/img/configurator/product/large_image.webp`
- `addons/website_sale/static/src/img/configurator/shop/cards.webp`
- `addons/website_sale/static/src/img/configurator/shop/chips_contained.webp`
- `addons/website_sale/static/src/img/configurator/shop/classic_grid.webp`
- `addons/website_sale/static/src/img/configurator/shop/condensed_list.webp`
- `addons/website_sale/static/src/img/configurator/shop/modern_grid.webp`
- `addons/website_sale/static/src/img/configurator/shop/showcase.webp`
- `addons/website_sale/static/src/img/filmstrips/bordered.svg`
- `addons/website_sale/static/src/img/filmstrips/default.svg`
- `addons/website_sale/static/src/img/filmstrips/grid.svg`
- `addons/website_sale/static/src/img/filmstrips/images.svg`
- `addons/website_sale/static/src/img/filmstrips/large_images.svg`
- `addons/website_sale/static/src/img/filmstrips/pills.svg`
- `addons/website_sale/static/src/img/filmstrips/tabs.svg`
- `addons/website_sale/static/src/img/product_previews/product_1.jpg`
- `addons/website_sale/static/src/img/product_previews/product_2.jpg`
- `addons/website_sale/static/src/img/product_previews/product_3.jpg`
- `addons/website_sale/static/src/img/product_previews/product_4.jpg`
- `addons/website_sale/static/src/img/products_demo/carpentry.jpg`
- `addons/website_sale/static/src/img/products_demo/desk_organizer_02.jpg`
- `addons/website_sale/static/src/img/products_demo/donation.png`
- `addons/website_sale/static/src/img/products_demo/floor_protection-image_02.jpg`
- `addons/website_sale/static/src/img/products_demo/product_lamp_02.jpg`
- `addons/website_sale/static/src/img/products_demo/product_product_10-image_02.jpg`
- `addons/website_sale/static/src/img/products_demo/product_product_12-image_02.jpg`
- `addons/website_sale/static/src/img/products_demo/product_product_16-image_02.jpg`
- `addons/website_sale/static/src/img/products_demo/product_product_24-image_02.jpg`
- `addons/website_sale/static/src/img/products_demo/product_product_27-image_02.jpg`
- `addons/website_sale/static/src/img/products_demo/product_product_3-image_02.jpg`
- `addons/website_sale/static/src/img/products_demo/product_product_46-image_02.jpg`
- `addons/website_sale/static/src/img/products_demo/product_product_5-image_02.jpg`
- `addons/website_sale/static/src/img/products_demo/product_product_6-image_02.jpg`
- `addons/website_sale/static/src/img/products_demo/product_product_7-image_02.jpg`
- `addons/website_sale/static/src/img/products_demo/product_product_9-image_02.jpg`
- `addons/website_sale/static/src/img/products_demo/product_product_d01_image_02.jpg`
- `addons/website_sale/static/src/img/products_demo/product_product_d03_image_02.jpg`
- `addons/website_sale/static/src/img/products_demo/table02_02.jpg`
- `addons/website_sale/static/src/img/products_demo/table02_03.webp`
- `addons/website_sale/static/src/img/products_demo/warranty.jpg`
- `addons/website_sale/static/src/img/products_entries_design/style_catalog_bento.svg`
- `addons/website_sale/static/src/img/products_entries_design/style_catalog_cards.svg`
- `addons/website_sale/static/src/img/products_entries_design/style_catalog_chips.svg`
- `addons/website_sale/static/src/img/products_entries_design/style_catalog_grid.svg`
- `addons/website_sale/static/src/img/products_entries_design/style_catalog_overlay.svg`
- `addons/website_sale/static/src/img/products_entries_design/style_catalog_panel.svg`
- `addons/website_sale/static/src/img/products_entries_design/style_catalog_thumb.svg`
- `addons/website_sale/static/src/img/products_entries_design/style_list_cards.svg`
- `addons/website_sale/static/src/img/products_entries_design/style_list_condensed.svg`
- `addons/website_sale/static/src/img/products_entries_design/style_list_grid.svg`
- `addons/website_sale/static/src/img/products_entries_design/style_list_large.svg`
- `addons/website_sale/static/src/img/products_entries_design/style_list_list.svg`
- `addons/website_sale/static/src/img/products_entries_design/style_list_narrow.svg`
- `addons/website_sale/static/src/img/products_entries_design/style_list_showcase.svg`
- `addons/website_sale/static/src/img/products_entries_design/style_list_thumbs.svg`
- `addons/website_sale/static/src/img/snippet_options/image-width-100.svg`
- `addons/website_sale/static/src/img/snippet_options/image-width-33.svg`
- `addons/website_sale/static/src/img/snippet_options/image-width-50.svg`
- `addons/website_sale/static/src/img/snippet_options/image-width-66.svg`
- `addons/website_sale/static/src/img/snippet_options/image-width-none.svg`
- `addons/website_sale/static/src/img/snippets_options/footer_template_website_sale.svg`
- `addons/website_sale/static/src/interactions/add_to_cart.js`
- `addons/website_sale/static/src/interactions/add_to_comparison.js`
- `addons/website_sale/static/src/interactions/add_to_wishlist.js`
- `addons/website_sale/static/src/interactions/address.js`
- `addons/website_sale/static/src/interactions/carousel_product.js`
- `addons/website_sale/static/src/interactions/cart_line.js`
- `addons/website_sale/static/src/interactions/checkout.js`
- `addons/website_sale/static/src/interactions/comparison_bottom_bar.js`
- `addons/website_sale/static/src/interactions/comparison_page.js`
- `addons/website_sale/static/src/interactions/confirm_order.js`
- `addons/website_sale/static/src/interactions/delivery_date_picker.js`
- `addons/website_sale/static/src/interactions/dropdown_typeahead.js`
- `addons/website_sale/static/src/interactions/express_checkout.js`
- `addons/website_sale/static/src/interactions/extra_info_form.js`
- `addons/website_sale/static/src/interactions/mobile_summary_keyboard.js`
- `addons/website_sale/static/src/interactions/payment_button.js`
- `addons/website_sale/static/src/interactions/payment_form.js`
- `addons/website_sale/static/src/interactions/popup.js`
- `addons/website_sale/static/src/interactions/price_range.js`
- `addons/website_sale/static/src/interactions/product/product_images_grid.js`
- `addons/website_sale/static/src/interactions/product/product_variant_preview.js`
- `addons/website_sale/static/src/interactions/product/product_variant_preview_hover.js`
- `addons/website_sale/static/src/interactions/product_accordion.js`
- Additional source files not expanded in this page: 317; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
