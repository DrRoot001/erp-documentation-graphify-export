# Module: website_sale_stock

- **Module ID:** MOD-642
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_sale_stock`
- **Manifest:** `addons/website_sale_stock/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Manage product inventory & availability

**Manifest description:**

Manage the inventory of your products and display their availability status in your eCommerce store.
In case of stockout, you can decide to block further sales or to keep selling.
A default behavior can be selected in the Website settings.
Then it can be made specific at the product level.

**Scope evidence:** The module contains 123 files, including 31 Python, 17 XML, and 17 JavaScript/TypeScript files. The manifest declares dependencies: `website_sale`, `sale_stock`, `stock_delivery`.

## 2. Module structure

- Model/business logic files: 9
- Controller/API files: 2
- XML/data/view/template files: 17
- Browser asset files: 17
- Security files: 0
- Test files: 16
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 9 model declarations, 72 methods, 0 constraint handlers, 1 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/website_sale_stock/models/res_partner.py:7`, `addons/website_sale_stock/models/sale_order.py:8`, `addons/website_sale_stock/models/product_product.py:6`, `addons/website_sale_stock/models/product_template.py:6`, `addons/website_sale_stock/models/delivery_carrier.py:7`, `addons/website_sale_stock/models/res_config_settings.py:6`, `addons/website_sale_stock/models/stock_picking.py:9`, `addons/website_sale_stock/models/website.py:6`, `addons/website_sale_stock/wizard/choose_delivery_carrier.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 2 route declarations.
- **Evidence:** `addons/website_sale_stock/controllers/location_selector.py:9`, `addons/website_sale_stock/controllers/location_selector.py:33`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 17 XML files and 17 JavaScript/TypeScript files; static XML analysis found 11 record/template/menu identifiers.
- **Evidence:** `addons/website_sale_stock/wizard/choose_delivery_carrier_views.xml:3`, `addons/website_sale_stock/data/website_sale_stock_demo.xml:3`, `addons/website_sale_stock/data/website_sale_stock_demo.xml:6`, `addons/website_sale_stock/data/website_sale_stock_demo.xml:9`, `addons/website_sale_stock/data/website_sale_stock_demo.xml:12`, `addons/website_sale_stock/views/stock_picking_views.xml:4`, `addons/website_sale_stock/views/res_config_settings_views.xml:4`, `addons/website_sale_stock/views/sale_order_views.xml:4`, `addons/website_sale_stock/views/sale_order_views.xml:26`, `addons/website_sale_stock/views/delivery_form.xml:4`, `addons/website_sale_stock/views/checkout_templates.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/website_sale_stock/tests/test_website_sale_stock_stock_notification.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 16 test files are present.
- **Evidence:** `addons/website_sale_stock/tests/test_website_sale_stock_stock_notification.py`, `addons/website_sale_stock/tests/test_website_sale_stock_gmc.py`, `addons/website_sale_stock/tests/test_website_sale_stock_configurators.py`, `addons/website_sale_stock/tests/test_website_sale_stock_stock_message.py`, `addons/website_sale_stock/tests/test_website_sale_stock_checkout.py`, `addons/website_sale_stock/tests/test_website_sale_stock_reorder_from_portal.py`, `addons/website_sale_stock/tests/test_website_sale_stock_product_template.py`, `addons/website_sale_stock/tests/test_website_sale_stock_product_product.py`, `addons/website_sale_stock/tests/test_website_sale_stock_product_warehouse.py`, `addons/website_sale_stock/tests/test_website_sale_stock_location_selector.py`, `addons/website_sale_stock/tests/common.py`, `addons/website_sale_stock/tests/test_website_sale_stock_multilang.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 17; representative identifiers: `choose_delivery_carrier_view_form_inherit_website_sale`, `stock.product_cable_management_box`, `stock.product_cable_management_box_product_template`, `website_sale.out_of_stock_ribbon`, `website_sale_order_19_box`, `view_picking_form_inherit_website_sale`, `res_config_settings_view_form`, `sale_order_view_form`, `sale_order_list_view_ecommerce`, `pickup_delivery_method`, `pickup_address_on_checkout`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/website_sale_stock/views/delivery_form.xml:4`, `addons/website_sale_stock/views/checkout_templates.xml:4`
- View/action field declarations: 10; representative evidence: `addons/website_sale_stock/wizard/choose_delivery_carrier_views.xml:5`, `addons/website_sale_stock/wizard/choose_delivery_carrier_views.xml:7`, `addons/website_sale_stock/views/stock_picking_views.xml:6`, `addons/website_sale_stock/views/stock_picking_views.xml:8`, `addons/website_sale_stock/views/res_config_settings_views.xml:6`, `addons/website_sale_stock/views/res_config_settings_views.xml:8`, `addons/website_sale_stock/views/sale_order_views.xml:6`, `addons/website_sale_stock/views/sale_order_views.xml:8`, `addons/website_sale_stock/views/sale_order_views.xml:28`, `addons/website_sale_stock/views/sale_order_views.xml:30`
- Browser assets: 17; representative files: `addons/website_sale_stock/static/src/interactions/checkout.js`, `addons/website_sale_stock/static/src/js/models/product_product.js`, `addons/website_sale_stock/static/src/js/product_card/product_card.js`, `addons/website_sale_stock/static/src/js/combo_configurator_dialog/combo_configurator_dialog.js`, `addons/website_sale_stock/static/src/js/tours/website_sale_stock_reorder_from_portal.js`, `addons/website_sale_stock/static/src/js/tours/combo_configurator_tour_utils.js`, `addons/website_sale_stock/static/src/js/pickup_location_many2one/pickup_location_many2one.js`, `addons/website_sale_stock/static/src/js/location_selector/map/map.js`, `addons/website_sale_stock/static/src/js/location_selector/map_container/map_container.js`, `addons/website_sale_stock/static/src/js/location_selector/location_selector_dialog/location_selector_dialog.js`, `addons/website_sale_stock/static/src/js/location_selector/location/location.js`, `addons/website_sale_stock/static/src/js/location_selector/location_schedule/location_schedule.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_sale_stock/__manifest__.py`
- **HTTP entry points:** `addons/website_sale_stock/controllers/location_selector.py:9`, `addons/website_sale_stock/controllers/location_selector.py:33`
- **Scheduled entry points:** `addons/website_sale_stock/tests/test_website_sale_stock_stock_notification.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 9
- Representative model evidence: inherits `res.partner` (addons/website_sale_stock/models/res_partner.py:7); inherits `sale.order` (addons/website_sale_stock/models/sale_order.py:8); inherits `product.product` (addons/website_sale_stock/models/product_product.py:6); inherits `product.template` (addons/website_sale_stock/models/product_template.py:6); `delivery.carrier` (addons/website_sale_stock/models/delivery_carrier.py:7); inherits `res.config.settings` (addons/website_sale_stock/models/res_config_settings.py:6); inherits `stock.picking` (addons/website_sale_stock/models/stock_picking.py:9); inherits `website` (addons/website_sale_stock/models/website.py:6); inherits `choose.delivery.carrier` (addons/website_sale_stock/wizard/choose_delivery_carrier.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 2
- Route evidence: `addons/website_sale_stock/controllers/location_selector.py:9`, `addons/website_sale_stock/controllers/location_selector.py:33`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_sale`, `sale_stock`, `stock_delivery`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/website_sale_stock/__init__.py`
- `addons/website_sale_stock/__manifest__.py`
- `addons/website_sale_stock/controllers/__init__.py`
- `addons/website_sale_stock/controllers/location_selector.py`
- `addons/website_sale_stock/data/website_sale_stock_demo.xml`
- `addons/website_sale_stock/i18n/af.po`
- `addons/website_sale_stock/i18n/ar.po`
- `addons/website_sale_stock/i18n/az.po`
- `addons/website_sale_stock/i18n/bg.po`
- `addons/website_sale_stock/i18n/bs.po`
- `addons/website_sale_stock/i18n/ca.po`
- `addons/website_sale_stock/i18n/cs.po`
- `addons/website_sale_stock/i18n/da.po`
- `addons/website_sale_stock/i18n/de.po`
- `addons/website_sale_stock/i18n/el.po`
- `addons/website_sale_stock/i18n/es.po`
- `addons/website_sale_stock/i18n/es_419.po`
- `addons/website_sale_stock/i18n/et.po`
- `addons/website_sale_stock/i18n/fa.po`
- `addons/website_sale_stock/i18n/fi.po`
- `addons/website_sale_stock/i18n/fr.po`
- `addons/website_sale_stock/i18n/gu.po`
- `addons/website_sale_stock/i18n/he.po`
- `addons/website_sale_stock/i18n/hi.po`
- `addons/website_sale_stock/i18n/hr.po`
- `addons/website_sale_stock/i18n/hu.po`
- `addons/website_sale_stock/i18n/id.po`
- `addons/website_sale_stock/i18n/is.po`
- `addons/website_sale_stock/i18n/it.po`
- `addons/website_sale_stock/i18n/ja.po`
- `addons/website_sale_stock/i18n/kab.po`
- `addons/website_sale_stock/i18n/km.po`
- `addons/website_sale_stock/i18n/ko.po`
- `addons/website_sale_stock/i18n/ku.po`
- `addons/website_sale_stock/i18n/lo.po`
- `addons/website_sale_stock/i18n/lt.po`
- `addons/website_sale_stock/i18n/lv.po`
- `addons/website_sale_stock/i18n/mn.po`
- `addons/website_sale_stock/i18n/my.po`
- `addons/website_sale_stock/i18n/nb.po`
- `addons/website_sale_stock/i18n/nl.po`
- `addons/website_sale_stock/i18n/pl.po`
- `addons/website_sale_stock/i18n/pt.po`
- `addons/website_sale_stock/i18n/pt_BR.po`
- `addons/website_sale_stock/i18n/ro.po`
- `addons/website_sale_stock/i18n/ru.po`
- `addons/website_sale_stock/i18n/sk.po`
- `addons/website_sale_stock/i18n/sl.po`
- `addons/website_sale_stock/i18n/sr@latin.po`
- `addons/website_sale_stock/i18n/sv.po`
- `addons/website_sale_stock/i18n/th.po`
- `addons/website_sale_stock/i18n/tr.po`
- `addons/website_sale_stock/i18n/uk.po`
- `addons/website_sale_stock/i18n/uz.po`
- `addons/website_sale_stock/i18n/vi.po`
- `addons/website_sale_stock/i18n/website_sale_stock.pot`
- `addons/website_sale_stock/i18n/zh_CN.po`
- `addons/website_sale_stock/i18n/zh_TW.po`
- `addons/website_sale_stock/models/__init__.py`
- `addons/website_sale_stock/models/delivery_carrier.py`
- `addons/website_sale_stock/models/product_product.py`
- `addons/website_sale_stock/models/product_template.py`
- `addons/website_sale_stock/models/res_config_settings.py`
- `addons/website_sale_stock/models/res_partner.py`
- `addons/website_sale_stock/models/sale_order.py`
- `addons/website_sale_stock/models/stock_picking.py`
- `addons/website_sale_stock/models/website.py`
- `addons/website_sale_stock/static/description/icon.png`
- `addons/website_sale_stock/static/description/icon.svg`
- `addons/website_sale_stock/static/description/icon_hi.png`
- `addons/website_sale_stock/static/src/interactions/checkout.js`
- `addons/website_sale_stock/static/src/js/combo_configurator_dialog/combo_configurator_dialog.js`
- `addons/website_sale_stock/static/src/js/combo_configurator_dialog/combo_configurator_dialog.xml`
- `addons/website_sale_stock/static/src/js/location_selector/location/location.js`
- `addons/website_sale_stock/static/src/js/location_selector/location/location.xml`
- `addons/website_sale_stock/static/src/js/location_selector/location_list/location_list.js`
- `addons/website_sale_stock/static/src/js/location_selector/location_list/location_list.xml`
- `addons/website_sale_stock/static/src/js/location_selector/location_schedule/location_schedule.js`
- `addons/website_sale_stock/static/src/js/location_selector/location_schedule/location_schedule.xml`
- `addons/website_sale_stock/static/src/js/location_selector/location_selector_dialog/location_selector_dialog.js`
- `addons/website_sale_stock/static/src/js/location_selector/location_selector_dialog/location_selector_dialog.scss`
- `addons/website_sale_stock/static/src/js/location_selector/location_selector_dialog/location_selector_dialog.xml`
- `addons/website_sale_stock/static/src/js/location_selector/map/map-pin-indicator.xml`
- `addons/website_sale_stock/static/src/js/location_selector/map/map.js`
- `addons/website_sale_stock/static/src/js/location_selector/map/map.scss`
- `addons/website_sale_stock/static/src/js/location_selector/map/map.xml`
- `addons/website_sale_stock/static/src/js/location_selector/map_container/map_container.js`
- `addons/website_sale_stock/static/src/js/location_selector/map_container/map_container.xml`
- `addons/website_sale_stock/static/src/js/models/product_product.js`
- `addons/website_sale_stock/static/src/js/pickup_location_many2one/pickup_location_many2one.js`
- `addons/website_sale_stock/static/src/js/pickup_location_many2one/pickup_location_many2one.xml`
- `addons/website_sale_stock/static/src/js/product_card/product_card.js`
- `addons/website_sale_stock/static/src/js/product_card/product_card.xml`
- `addons/website_sale_stock/static/src/js/tours/combo_configurator_tour_utils.js`
- `addons/website_sale_stock/static/src/js/tours/website_sale_stock_reorder_from_portal.js`
- `addons/website_sale_stock/static/tests/tours/website_sale_stock_combo_configurator.js`
- `addons/website_sale_stock/static/tests/tours/website_sale_stock_message_after_close_configurator_modal.js`
- `addons/website_sale_stock/static/tests/tours/website_sale_stock_multilang.js`
- `addons/website_sale_stock/static/tests/tours/website_sale_stock_stock_notification.js`
- `addons/website_sale_stock/tests/__init__.py`
- `addons/website_sale_stock/tests/common.py`
- `addons/website_sale_stock/tests/test_website_sale_stock_abandoned_cart_email.py`
- `addons/website_sale_stock/tests/test_website_sale_stock_checkout.py`
- `addons/website_sale_stock/tests/test_website_sale_stock_configurators.py`
- `addons/website_sale_stock/tests/test_website_sale_stock_gmc.py`
- `addons/website_sale_stock/tests/test_website_sale_stock_location_selector.py`
- `addons/website_sale_stock/tests/test_website_sale_stock_multilang.py`
- `addons/website_sale_stock/tests/test_website_sale_stock_product_combo.py`
- `addons/website_sale_stock/tests/test_website_sale_stock_product_product.py`
- `addons/website_sale_stock/tests/test_website_sale_stock_product_template.py`
- `addons/website_sale_stock/tests/test_website_sale_stock_product_warehouse.py`
- `addons/website_sale_stock/tests/test_website_sale_stock_reorder_from_portal.py`
- `addons/website_sale_stock/tests/test_website_sale_stock_sale_order_line.py`
- `addons/website_sale_stock/tests/test_website_sale_stock_stock_message.py`
- `addons/website_sale_stock/tests/test_website_sale_stock_stock_notification.py`
- `addons/website_sale_stock/views/checkout_templates.xml`
- `addons/website_sale_stock/views/delivery_form.xml`
- `addons/website_sale_stock/views/res_config_settings_views.xml`
- `addons/website_sale_stock/views/sale_order_views.xml`
- `addons/website_sale_stock/views/stock_picking_views.xml`
- `addons/website_sale_stock/wizard/__init__.py`
- `addons/website_sale_stock/wizard/choose_delivery_carrier.py`
- `addons/website_sale_stock/wizard/choose_delivery_carrier_views.xml`
