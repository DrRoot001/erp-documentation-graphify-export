# Module: pos_self_order

- **Module ID:** MOD-455
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_self_order`
- **Manifest:** `addons/pos_self_order/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point Of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Addon for the POS App that allows customers to view the menu on their smartphone.

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 337 files, including 51 Python, 59 XML, and 146 JavaScript/TypeScript files. The manifest declares dependencies: `pos_restaurant`, `http_routing`, `link_tracker`, `google_address_autocomplete`, `base_geolocalize`.

## 2. Module structure

- Model/business logic files: 24
- Controller/API files: 4
- XML/data/view/template files: 59
- Browser asset files: 146
- Security files: 1
- Test files: 20
- Scheduled/automation evidence files: 0
- Reporting evidence files: 3

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/pos_self_order/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 24 model declarations, 335 methods, 1 constraint handlers, 6 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/pos_self_order/models/pos_prep_line.py:4`, `addons/pos_self_order/models/res_partner.py:5`, `addons/pos_self_order/models/product_product.py:7`, `addons/pos_self_order/models/pos_self_order_custom_link.py:9`, `addons/pos_self_order/models/pos_restaurant.py:9`, `addons/pos_self_order/models/pos_restaurant.py:38`, `addons/pos_self_order/models/product_template.py:5`, `addons/pos_self_order/models/ir_ui_view.py:6`, `addons/pos_self_order/models/mail_template.py:3`, `addons/pos_self_order/models/pos_config.py:16`, `addons/pos_self_order/models/res_config_settings.py:11`, `addons/pos_self_order/models/pos_category.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 4 controller files and 18 route declarations.
- **Evidence:** `addons/pos_self_order/controllers/self_entry.py:9`, `addons/pos_self_order/controllers/self_entry.py:36`, `addons/pos_self_order/controllers/webmanifest.py:34`, `addons/pos_self_order/controllers/orders.py:29`, `addons/pos_self_order/controllers/orders.py:156`, `addons/pos_self_order/controllers/orders.py:166`, `addons/pos_self_order/controllers/orders.py:228`, `addons/pos_self_order/controllers/orders.py:241`, `addons/pos_self_order/controllers/orders.py:272`, `addons/pos_self_order/controllers/orders.py:294`, `addons/pos_self_order/controllers/orders.py:315`, `addons/pos_self_order/controllers/orders.py:336`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 59 XML files and 146 JavaScript/TypeScript files; static XML analysis found 27 record/template/menu identifiers.
- **Evidence:** `addons/pos_self_order/data/mail_template_data.xml:4`, `addons/pos_self_order/data/mail_template_data.xml:38`, `addons/pos_self_order/data/preset_data.xml:3`, `addons/pos_self_order/data/preset_data.xml:10`, `addons/pos_self_order/data/preset_data.xml:15`, `addons/pos_self_order/data/preset_data.xml:20`, `addons/pos_self_order/receipt/pos_order_change_receipt.xml:4`, `addons/pos_self_order/receipt/dynamic_qr_receipt.xml:4`, `addons/pos_self_order/receipt/pos_order_receipt.xml:4`, `addons/pos_self_order/views/pos_config_view.xml:3`, `addons/pos_self_order/views/pos_config_view.xml:14`, `addons/pos_self_order/views/res_config_settings_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/pos_self_order/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 3 files contain report-action/template indicators.
- **Evidence:** `addons/pos_self_order/controllers/orders.py`, `addons/pos_self_order/views/qr_code.xml`, `addons/pos_self_order/tests/test_self_order_receipt_lang.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 20 test files are present.
- **Evidence:** `addons/pos_self_order/tests/test_self_order_controller.py`, `addons/pos_self_order/tests/test_self_order_sibling_ptav.py`, `addons/pos_self_order/tests/test_frontend.py`, `addons/pos_self_order/tests/test_self_order_attribute.py`, `addons/pos_self_order/tests/test_self_order_payment_method.py`, `addons/pos_self_order/tests/test_self_order_prices.py`, `addons/pos_self_order/tests/test_self_order_common.py`, `addons/pos_self_order/tests/test_self_order_combo.py`, `addons/pos_self_order/tests/test_self_order_preset.py`, `addons/pos_self_order/tests/test_webmanifest.py`, `addons/pos_self_order/tests/test_takeaway_preset_mail.py`, `addons/pos_self_order/tests/test_self_order_sequence.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 59; representative identifiers: `takeout_email_template`, `delivery_email_template`, `product_delivery_template`, `pos_restaurant.pos_takein_preset`, `pos_restaurant.pos_takeout_preset`, `pos_restaurant.pos_delivery_preset`, `pos_self_order.pos_order_change_receipt`, `pos_self_order.DynamicQrReceipt`, `pos_self_order.pos_order_receipt_header`, `pos_self_view_pos_config_tree`, `pos_config_view_form_inherit_pos_self_order`, `res_config_settings_view_form_menu`, `POS Self Order`, `report_self_order_qr_codes_page`, `paperformat_qrcodes`, `qr_codes_page`, `pos_self_order_product_pos_category_form_view`, `product_template_search_view_pos`, `product_template_form_view`, `product_template_tree_view`
- Menus: 0; representative evidence: Not found in module
- Templates: 5; representative evidence: `addons/pos_self_order/receipt/pos_order_change_receipt.xml:4`, `addons/pos_self_order/receipt/dynamic_qr_receipt.xml:4`, `addons/pos_self_order/receipt/pos_order_receipt.xml:4`, `addons/pos_self_order/views/pos_self_order.index.xml:3`, `addons/pos_self_order/views/qr_code.xml:18`
- View/action field declarations: 29; representative evidence: `addons/pos_self_order/views/pos_config_view.xml:5`, `addons/pos_self_order/views/pos_config_view.xml:7`, `addons/pos_self_order/views/pos_config_view.xml:16`, `addons/pos_self_order/views/pos_config_view.xml:18`, `addons/pos_self_order/views/res_config_settings_views.xml:5`, `addons/pos_self_order/views/res_config_settings_views.xml:7`, `addons/pos_self_order/views/qr_code.xml:6`, `addons/pos_self_order/views/pos_category_views.xml:5`, `addons/pos_self_order/views/pos_category_views.xml:7`, `addons/pos_self_order/views/product_views.xml:5`, `addons/pos_self_order/views/product_views.xml:7`, `addons/pos_self_order/views/product_views.xml:21`
- Browser assets: 146; representative files: `addons/pos_self_order/static/src/upgrade_selection_field.js`, `addons/pos_self_order/static/src/app/self_order_index.js`, `addons/pos_self_order/static/src/app/kiosk_style.js`, `addons/pos_self_order/static/src/app/utils.js`, `addons/pos_self_order/static/src/app/data_service_options.js`, `addons/pos_self_order/static/src/app/router.js`, `addons/pos_self_order/static/src/app/root.js`, `addons/pos_self_order/static/src/overrides/services/pos_ticket_printer_plugin.js`, `addons/pos_self_order/static/src/overrides/models/pos_store.js`, `addons/pos_self_order/static/src/overrides/models/restaurant_table.js`, `addons/pos_self_order/static/src/overrides/models/pos_config.js`, `addons/pos_self_order/static/src/overrides/order_tracker_dropdown/order_tracker_dropdown.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_self_order/__manifest__.py`
- **HTTP entry points:** `addons/pos_self_order/controllers/self_entry.py:9`, `addons/pos_self_order/controllers/self_entry.py:36`, `addons/pos_self_order/controllers/webmanifest.py:34`, `addons/pos_self_order/controllers/orders.py:29`, `addons/pos_self_order/controllers/orders.py:156`, `addons/pos_self_order/controllers/orders.py:166`, `addons/pos_self_order/controllers/orders.py:228`, `addons/pos_self_order/controllers/orders.py:241`, `addons/pos_self_order/controllers/orders.py:272`, `addons/pos_self_order/controllers/orders.py:294`, `addons/pos_self_order/controllers/orders.py:315`, `addons/pos_self_order/controllers/orders.py:336`
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/pos_self_order/controllers/orders.py`, `addons/pos_self_order/views/qr_code.xml`, `addons/pos_self_order/tests/test_self_order_receipt_lang.py`

## 7. Database interactions

- Model declarations: 24
- Representative model evidence: inherits `pos.prep.line` (addons/pos_self_order/models/pos_prep_line.py:4); inherits `res.partner` (addons/pos_self_order/models/res_partner.py:5); inherits `product.product` (addons/pos_self_order/models/product_product.py:7); `pos_self_order.custom_link` (addons/pos_self_order/models/pos_self_order_custom_link.py:9); inherits `restaurant.table` (addons/pos_self_order/models/pos_restaurant.py:9); inherits `restaurant.floor` (addons/pos_self_order/models/pos_restaurant.py:38); inherits `product.template` (addons/pos_self_order/models/product_template.py:5); inherits `ir.ui.view` (addons/pos_self_order/models/ir_ui_view.py:6); `mail.template` (addons/pos_self_order/models/mail_template.py:3); inherits `pos.config` (addons/pos_self_order/models/pos_config.py:16); inherits `res.config.settings` (addons/pos_self_order/models/res_config_settings.py:11); inherits `pos.category` (addons/pos_self_order/models/pos_category.py:7); inherits `pos.session` (addons/pos_self_order/models/pos_session.py:7); inherits `pos.prep.order` (addons/pos_self_order/models/pos_prep_order.py:4); inherits `pos.order` (addons/pos_self_order/models/pos_order.py:14); inherits `ir.http` (addons/pos_self_order/models/ir_http.py:9); inherits `pos.preset` (addons/pos_self_order/models/pos_preset.py:10); inherits `pos.load.mixin` (addons/pos_self_order/models/pos_load_mixin.py:9); inherits `pos.payment.method` (addons/pos_self_order/models/pos_payment_method.py:4); `res.country` (addons/pos_self_order/models/res_country.py:4); inherits `pos.order.line` (addons/pos_self_order/models/pos_order_line.py:6); inherits `product.tag` (addons/pos_self_order/models/product_tag.py:5); inherits `pos.snooze` (addons/pos_self_order/models/pos_snooze.py:6); inherits `pos.order.receipt` (addons/pos_self_order/receipt/pos_order_receipt.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 4
- Route declarations: 18
- Route evidence: `addons/pos_self_order/controllers/self_entry.py:9`, `addons/pos_self_order/controllers/self_entry.py:36`, `addons/pos_self_order/controllers/webmanifest.py:34`, `addons/pos_self_order/controllers/orders.py:29`, `addons/pos_self_order/controllers/orders.py:156`, `addons/pos_self_order/controllers/orders.py:166`, `addons/pos_self_order/controllers/orders.py:228`, `addons/pos_self_order/controllers/orders.py:241`, `addons/pos_self_order/controllers/orders.py:272`, `addons/pos_self_order/controllers/orders.py:294`, `addons/pos_self_order/controllers/orders.py:315`, `addons/pos_self_order/controllers/orders.py:336`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `pos_restaurant`, `http_routing`, `link_tracker`, `google_address_autocomplete`, `base_geolocalize`
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

- `addons/pos_self_order/__init__.py`
- `addons/pos_self_order/__manifest__.py`
- `addons/pos_self_order/controllers/__init__.py`
- `addons/pos_self_order/controllers/orders.py`
- `addons/pos_self_order/controllers/self_entry.py`
- `addons/pos_self_order/controllers/webmanifest.py`
- `addons/pos_self_order/data/init_access.xml`
- `addons/pos_self_order/data/kiosk_demo_data.xml`
- `addons/pos_self_order/data/mail_template_data.xml`
- `addons/pos_self_order/data/preset_data.xml`
- `addons/pos_self_order/i18n/ar.po`
- `addons/pos_self_order/i18n/az.po`
- `addons/pos_self_order/i18n/bg.po`
- `addons/pos_self_order/i18n/bs.po`
- `addons/pos_self_order/i18n/ca.po`
- `addons/pos_self_order/i18n/cs.po`
- `addons/pos_self_order/i18n/da.po`
- `addons/pos_self_order/i18n/de.po`
- `addons/pos_self_order/i18n/el.po`
- `addons/pos_self_order/i18n/es.po`
- `addons/pos_self_order/i18n/es_419.po`
- `addons/pos_self_order/i18n/et.po`
- `addons/pos_self_order/i18n/fa.po`
- `addons/pos_self_order/i18n/fi.po`
- `addons/pos_self_order/i18n/fr.po`
- `addons/pos_self_order/i18n/he.po`
- `addons/pos_self_order/i18n/hi.po`
- `addons/pos_self_order/i18n/hr.po`
- `addons/pos_self_order/i18n/hu.po`
- `addons/pos_self_order/i18n/id.po`
- `addons/pos_self_order/i18n/it.po`
- `addons/pos_self_order/i18n/ja.po`
- `addons/pos_self_order/i18n/kab.po`
- `addons/pos_self_order/i18n/ko.po`
- `addons/pos_self_order/i18n/ku.po`
- `addons/pos_self_order/i18n/lo.po`
- `addons/pos_self_order/i18n/lt.po`
- `addons/pos_self_order/i18n/lv.po`
- `addons/pos_self_order/i18n/mn.po`
- `addons/pos_self_order/i18n/my.po`
- `addons/pos_self_order/i18n/nb.po`
- `addons/pos_self_order/i18n/nl.po`
- `addons/pos_self_order/i18n/pl.po`
- `addons/pos_self_order/i18n/pos_self_order.pot`
- `addons/pos_self_order/i18n/pt.po`
- `addons/pos_self_order/i18n/pt_BR.po`
- `addons/pos_self_order/i18n/ro.po`
- `addons/pos_self_order/i18n/ru.po`
- `addons/pos_self_order/i18n/sk.po`
- `addons/pos_self_order/i18n/sl.po`
- `addons/pos_self_order/i18n/sr@latin.po`
- `addons/pos_self_order/i18n/sv.po`
- `addons/pos_self_order/i18n/th.po`
- `addons/pos_self_order/i18n/tr.po`
- `addons/pos_self_order/i18n/uk.po`
- `addons/pos_self_order/i18n/uz.po`
- `addons/pos_self_order/i18n/vi.po`
- `addons/pos_self_order/i18n/zh_CN.po`
- `addons/pos_self_order/i18n/zh_TW.po`
- `addons/pos_self_order/models/__init__.py`
- `addons/pos_self_order/models/ir_http.py`
- `addons/pos_self_order/models/ir_ui_view.py`
- `addons/pos_self_order/models/mail_template.py`
- `addons/pos_self_order/models/pos_category.py`
- `addons/pos_self_order/models/pos_config.py`
- `addons/pos_self_order/models/pos_load_mixin.py`
- `addons/pos_self_order/models/pos_order.py`
- `addons/pos_self_order/models/pos_order_line.py`
- `addons/pos_self_order/models/pos_payment_method.py`
- `addons/pos_self_order/models/pos_prep_line.py`
- `addons/pos_self_order/models/pos_prep_order.py`
- `addons/pos_self_order/models/pos_preset.py`
- `addons/pos_self_order/models/pos_restaurant.py`
- `addons/pos_self_order/models/pos_self_order_custom_link.py`
- `addons/pos_self_order/models/pos_session.py`
- `addons/pos_self_order/models/pos_snooze.py`
- `addons/pos_self_order/models/product_product.py`
- `addons/pos_self_order/models/product_tag.py`
- `addons/pos_self_order/models/product_template.py`
- `addons/pos_self_order/models/res_config_settings.py`
- `addons/pos_self_order/models/res_country.py`
- `addons/pos_self_order/models/res_partner.py`
- `addons/pos_self_order/receipt/__init__.py`
- `addons/pos_self_order/receipt/dynamic_qr_receipt.xml`
- `addons/pos_self_order/receipt/pos_order_change_receipt.xml`
- `addons/pos_self_order/receipt/pos_order_receipt.py`
- `addons/pos_self_order/receipt/pos_order_receipt.xml`
- `addons/pos_self_order/security/ir.access.csv`
- `addons/pos_self_order/static/img/delivery.jpg`
- `addons/pos_self_order/static/img/dine_in.jpg`
- `addons/pos_self_order/static/img/eatin.svg`
- `addons/pos_self_order/static/img/kiosk_background.jpg`
- `addons/pos_self_order/static/img/landing_01.jpg`
- `addons/pos_self_order/static/img/landing_02.jpg`
- `addons/pos_self_order/static/img/landing_03.jpg`
- `addons/pos_self_order/static/img/takeAway.svg`
- `addons/pos_self_order/static/img/take_out.jpg`
- `addons/pos_self_order/static/src/app/bootstrap_overridden.scss`
- `addons/pos_self_order/static/src/app/components/attribute_selection/attribute_selection.js`
- `addons/pos_self_order/static/src/app/components/attribute_selection/attribute_selection.scss`
- `addons/pos_self_order/static/src/app/components/attribute_selection/attribute_selection.xml`
- `addons/pos_self_order/static/src/app/components/attribute_selection/attribute_selection_helper.js`
- `addons/pos_self_order/static/src/app/components/cancel_popup/cancel_popup.js`
- `addons/pos_self_order/static/src/app/components/cancel_popup/cancel_popup.xml`
- `addons/pos_self_order/static/src/app/components/category_list_popup/category_list_popup.js`
- `addons/pos_self_order/static/src/app/components/category_list_popup/category_list_popup.xml`
- `addons/pos_self_order/static/src/app/components/choose_combo_popup/choose_combo_popup.js`
- `addons/pos_self_order/static/src/app/components/choose_combo_popup/choose_combo_popup.xml`
- `addons/pos_self_order/static/src/app/components/combo_stepper/combo_stepper.js`
- `addons/pos_self_order/static/src/app/components/combo_stepper/combo_stepper.scss`
- `addons/pos_self_order/static/src/app/components/combo_stepper/combo_stepper.xml`
- `addons/pos_self_order/static/src/app/components/info_popup/info_popup.js`
- `addons/pos_self_order/static/src/app/components/info_popup/info_popup.xml`
- `addons/pos_self_order/static/src/app/components/language_popup/language_popup.js`
- `addons/pos_self_order/static/src/app/components/language_popup/language_popup.scss`
- `addons/pos_self_order/static/src/app/components/language_popup/language_popup.xml`
- `addons/pos_self_order/static/src/app/components/language_selector/language_selector.js`
- `addons/pos_self_order/static/src/app/components/language_selector/language_selector.scss`
- `addons/pos_self_order/static/src/app/components/language_selector/language_selector.xml`
- `addons/pos_self_order/static/src/app/components/loading_overlay/loading_overlay.js`
- `addons/pos_self_order/static/src/app/components/loading_overlay/loading_overlay.xml`
- `addons/pos_self_order/static/src/app/components/missing_required_details/missing_required_details.scss`
- `addons/pos_self_order/static/src/app/components/missing_required_details/missing_required_details.xml`
- `addons/pos_self_order/static/src/app/components/network_connectionLost_popup/network_connectionLost_popup.js`
- `addons/pos_self_order/static/src/app/components/network_connectionLost_popup/network_connectionLost_popup.xml`
- `addons/pos_self_order/static/src/app/components/number_popup/number_popup.js`
- `addons/pos_self_order/static/src/app/components/number_popup/number_popup.scss`
- `addons/pos_self_order/static/src/app/components/number_popup/number_popup.xml`
- `addons/pos_self_order/static/src/app/components/order_widget/order_widget.js`
- `addons/pos_self_order/static/src/app/components/order_widget/order_widget.xml`
- `addons/pos_self_order/static/src/app/components/pills_selection_popup/pills_selection_popup.js`
- `addons/pos_self_order/static/src/app/components/pills_selection_popup/pills_selection_popup.scss`
- `addons/pos_self_order/static/src/app/components/pills_selection_popup/pills_selection_popup.xml`
- `addons/pos_self_order/static/src/app/components/preset_info_popup/preset_info_popup.js`
- `addons/pos_self_order/static/src/app/components/preset_info_popup/preset_info_popup.scss`
- `addons/pos_self_order/static/src/app/components/preset_info_popup/preset_info_popup.xml`
- `addons/pos_self_order/static/src/app/components/printing_failure_popup/printing_failure_popup.js`
- `addons/pos_self_order/static/src/app/components/printing_failure_popup/printing_failure_popup.xml`
- `addons/pos_self_order/static/src/app/components/product_card/product_card.js`
- `addons/pos_self_order/static/src/app/components/product_card/product_card.scss`
- `addons/pos_self_order/static/src/app/components/product_card/product_card.xml`
- `addons/pos_self_order/static/src/app/components/product_info_popup/product_info_popup.js`
- `addons/pos_self_order/static/src/app/components/product_info_popup/product_info_popup.xml`
- `addons/pos_self_order/static/src/app/components/product_interface/product_interface.js`
- `addons/pos_self_order/static/src/app/components/product_interface/product_interface.scss`
- `addons/pos_self_order/static/src/app/components/product_interface/product_interface.xml`
- `addons/pos_self_order/static/src/app/components/quantity_widget/quantity_widget.xml`
- `addons/pos_self_order/static/src/app/components/slots_popup/slots_popup.xml`
- `addons/pos_self_order/static/src/app/components/timeout_popup/timeout_popup.js`
- `addons/pos_self_order/static/src/app/components/timeout_popup/timeout_popup.xml`
- `addons/pos_self_order/static/src/app/components/unavailable_product_dialog/unavailable_product_dialog.js`
- `addons/pos_self_order/static/src/app/components/unavailable_product_dialog/unavailable_product_dialog.xml`
- `addons/pos_self_order/static/src/app/data_service_options.js`
- `addons/pos_self_order/static/src/app/kiosk_style.js`
- `addons/pos_self_order/static/src/app/models/pos_config.js`
- `addons/pos_self_order/static/src/app/models/pos_order.js`
- `addons/pos_self_order/static/src/app/models/pos_order_line.js`
- `addons/pos_self_order/static/src/app/models/pos_preset.js`
- `addons/pos_self_order/static/src/app/models/product_template.js`
- `addons/pos_self_order/static/src/app/models/restaurant_floor.js`
- `addons/pos_self_order/static/src/app/models/utils/snooze_tracker.js`
- `addons/pos_self_order/static/src/app/pages/cart_page/cart_page.js`
- `addons/pos_self_order/static/src/app/pages/cart_page/cart_page.scss`
- `addons/pos_self_order/static/src/app/pages/cart_page/cart_page.xml`
- `addons/pos_self_order/static/src/app/pages/combo_page/combo_page.js`
- `addons/pos_self_order/static/src/app/pages/combo_page/combo_page.scss`
- `addons/pos_self_order/static/src/app/pages/combo_page/combo_page.xml`
- `addons/pos_self_order/static/src/app/pages/confirmation_page/confirmation_page.js`
- `addons/pos_self_order/static/src/app/pages/confirmation_page/confirmation_page.scss`
- `addons/pos_self_order/static/src/app/pages/confirmation_page/confirmation_page.xml`
- `addons/pos_self_order/static/src/app/pages/eating_location_page/eating_location_page.js`
- `addons/pos_self_order/static/src/app/pages/eating_location_page/eating_location_page.xml`
- `addons/pos_self_order/static/src/app/pages/landing_page/landing_page.js`
- `addons/pos_self_order/static/src/app/pages/landing_page/landing_page.scss`
- `addons/pos_self_order/static/src/app/pages/landing_page/landing_page.xml`
- `addons/pos_self_order/static/src/app/pages/optional_product_page/optional_product_page.js`
- `addons/pos_self_order/static/src/app/pages/optional_product_page/optional_product_page.scss`
- `addons/pos_self_order/static/src/app/pages/optional_product_page/optional_product_page.xml`
- `addons/pos_self_order/static/src/app/pages/order_history_page/order_history_page.js`
- `addons/pos_self_order/static/src/app/pages/order_history_page/order_history_page.xml`
- `addons/pos_self_order/static/src/app/pages/payment_page/payment_page.js`
- `addons/pos_self_order/static/src/app/pages/payment_page/payment_page.scss`
- `addons/pos_self_order/static/src/app/pages/payment_page/payment_page.xml`
- `addons/pos_self_order/static/src/app/pages/product_list_page/product_list_page.js`
- `addons/pos_self_order/static/src/app/pages/product_list_page/product_list_page.scss`
- `addons/pos_self_order/static/src/app/pages/product_list_page/product_list_page.xml`
- `addons/pos_self_order/static/src/app/pages/product_page/product_page.js`
- `addons/pos_self_order/static/src/app/pages/product_page/product_page.scss`
- `addons/pos_self_order/static/src/app/pages/product_page/product_page.xml`
- `addons/pos_self_order/static/src/app/pages/stand_number_page/stand_number_page.js`
- `addons/pos_self_order/static/src/app/pages/stand_number_page/stand_number_page.scss`
- `addons/pos_self_order/static/src/app/pages/stand_number_page/stand_number_page.xml`
- `addons/pos_self_order/static/src/app/plugins/pos_data_plugin.js`
- `addons/pos_self_order/static/src/app/plugins/pos_ticket_printer_plugin.js`
- `addons/pos_self_order/static/src/app/primary_variables.scss`
- `addons/pos_self_order/static/src/app/root.js`
- `addons/pos_self_order/static/src/app/router.js`
- `addons/pos_self_order/static/src/app/self_order_index.js`
- `addons/pos_self_order/static/src/app/self_order_index.scss`
- `addons/pos_self_order/static/src/app/self_order_index.xml`
- `addons/pos_self_order/static/src/app/services/card_utils.js`
- `addons/pos_self_order/static/src/app/services/self_order_router_service.js`
- `addons/pos_self_order/static/src/app/services/self_order_service.js`
- `addons/pos_self_order/static/src/app/utils/carousel_hook.js`
- `addons/pos_self_order/static/src/app/utils/category_scrollspy_hook.js`
- `addons/pos_self_order/static/src/app/utils/payment_interface.js`
- `addons/pos_self_order/static/src/app/utils/scroll.js`
- `addons/pos_self_order/static/src/app/utils/scroll_dnd_hook.js`
- `addons/pos_self_order/static/src/app/utils/scroll_shadow_hook.js`
- `addons/pos_self_order/static/src/app/utils/scroll_to_selected.js`
- `addons/pos_self_order/static/src/app/utils/sticky_title_observer.js`
- `addons/pos_self_order/static/src/app/utils/ui_animations.js`
- `addons/pos_self_order/static/src/app/utils.js`
- `addons/pos_self_order/static/src/backend/pos_open_ui_button/pos_open_ui_button.js`
- `addons/pos_self_order/static/src/backend/qr_order_button/qr_order_button.js`
- `addons/pos_self_order/static/src/overrides/components/dynamic_qr_popup/dynamic_qr_popup.js`
- `addons/pos_self_order/static/src/overrides/components/dynamic_qr_popup/dynamic_qr_popup.xml`
- `addons/pos_self_order/static/src/overrides/components/navbar/navbar.js`
- `addons/pos_self_order/static/src/overrides/components/navbar/navbar.xml`
- `addons/pos_self_order/static/src/overrides/components/product_info_popup/product_info_popup.js`
- `addons/pos_self_order/static/src/overrides/components/product_info_popup/product_info_popup.xml`
- `addons/pos_self_order/static/src/overrides/components/product_screen.xml`
- `addons/pos_self_order/static/src/overrides/models/pos_config.js`
- `addons/pos_self_order/static/src/overrides/models/pos_store.js`
- `addons/pos_self_order/static/src/overrides/models/restaurant_table.js`
- `addons/pos_self_order/static/src/overrides/order_tracker_dropdown/order_tracker_dropdown.js`
- `addons/pos_self_order/static/src/overrides/order_tracker_dropdown/order_tracker_dropdown.xml`
- `addons/pos_self_order/static/src/overrides/screens/floor_screen/floor_screen.xml`
- `addons/pos_self_order/static/src/overrides/screens/product_screen/control_buttons/control_buttons.js`
- `addons/pos_self_order/static/src/overrides/screens/product_screen/control_buttons/control_buttons.xml`
- `addons/pos_self_order/static/src/overrides/screens/ticket_screen/order_details_dialog/order_details_dialog.js`
- `addons/pos_self_order/static/src/overrides/screens/ticket_screen/ticket_screen.js`
- `addons/pos_self_order/static/src/overrides/services/pos_ticket_printer_plugin.js`
- `addons/pos_self_order/static/src/overrides/utils/printer/generate_printer_data.js`
- `addons/pos_self_order/static/src/upgrade_selection_field.js`
- `addons/pos_self_order/static/tests/pos/pos_self_order_tour.js`
- `addons/pos_self_order/static/tests/tours/self_order_common_tour.js`
- `addons/pos_self_order/static/tests/tours/self_order_kiosk_tour.js`
- `addons/pos_self_order/static/tests/tours/self_order_mobile_tour.js`
- `addons/pos_self_order/static/tests/tours/self_order_preset_tour.js`
- `addons/pos_self_order/static/tests/tours/self_order_prices_tour.js`
- `addons/pos_self_order/static/tests/tours/utils/cart_page_util.js`
- `addons/pos_self_order/static/tests/tours/utils/combo_page_util.js`
- `addons/pos_self_order/static/tests/tours/utils/common.js`
- `addons/pos_self_order/static/tests/tours/utils/confirmation_page_util.js`
- `addons/pos_self_order/static/tests/tours/utils/landing_page_util.js`
- `addons/pos_self_order/static/tests/tours/utils/product_page_util.js`
- `addons/pos_self_order/static/tests/unit/components/order_widget.test.js`
- `addons/pos_self_order/static/tests/unit/components/pills_selection_popup.test.js`
- `addons/pos_self_order/static/tests/unit/components/preset_info_popup.test.js`
- Additional source files not expanded in this page: 87; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
