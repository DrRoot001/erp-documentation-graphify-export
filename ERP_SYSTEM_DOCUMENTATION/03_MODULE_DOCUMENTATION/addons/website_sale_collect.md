# Module: website_sale_collect

- **Module ID:** MOD-635
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_sale_collect`
- **Manifest:** `addons/website_sale_collect/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Allows customers to check in-store stock, pay on site, and pick up their orders at the shop.

**Scope evidence:** The module contains 110 files, including 31 Python, 18 XML, and 8 JavaScript/TypeScript files. The manifest declares dependencies: `base_geolocalize`, `payment_custom`, `website_sale_stock`.

## 2. Module structure

- Model/business logic files: 10
- Controller/API files: 4
- XML/data/view/template files: 18
- Browser asset files: 8
- Security files: 0
- Test files: 12
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 10 model declarations, 97 methods, 2 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/website_sale_collect/models/sale_order.py:6`, `addons/website_sale_collect/models/product_template.py:9`, `addons/website_sale_collect/models/delivery_carrier.py:11`, `addons/website_sale_collect/models/res_config_settings.py:6`, `addons/website_sale_collect/models/payment_transaction.py:9`, `addons/website_sale_collect/models/website.py:9`, `addons/website_sale_collect/models/sale_order_line.py:6`, `addons/website_sale_collect/models/stock_warehouse.py:12`, `addons/website_sale_collect/models/payment_method.py:6`, `addons/website_sale_collect/models/payment_provider.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 4 controller files and 3 route declarations.
- **Evidence:** `addons/website_sale_collect/controllers/delivery.py:10`, `addons/website_sale_collect/controllers/delivery.py:27`, `addons/website_sale_collect/controllers/delivery.py:50`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 18 XML files and 8 JavaScript/TypeScript files; static XML analysis found 16 record/template/menu identifiers.
- **Evidence:** `addons/website_sale_collect/demo/stock_warehouse_demo.xml:4`, `addons/website_sale_collect/demo/stock_warehouse_demo.xml:17`, `addons/website_sale_collect/data/product_product_data.xml:4`, `addons/website_sale_collect/data/delivery_carrier_data.xml:4`, `addons/website_sale_collect/data/payment_provider_data.xml:4`, `addons/website_sale_collect/data/payment_method_data.xml:4`, `addons/website_sale_collect/views/stock_picking_views.xml:3`, `addons/website_sale_collect/views/res_config_settings_views.xml:4`, `addons/website_sale_collect/views/sale_order_views.xml:3`, `addons/website_sale_collect/views/delivery_carrier_views.xml:4`, `addons/website_sale_collect/views/delivery_form_templates.xml:4`, `addons/website_sale_collect/views/delivery_form_templates.xml:92`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 12 test files are present.
- **Evidence:** `addons/website_sale_collect/tests/test_click_and_collect_express_checkout.py`, `addons/website_sale_collect/tests/test_website.py`, `addons/website_sale_collect/tests/test_in_store_delivery.py`, `addons/website_sale_collect/tests/test_sale_order.py`, `addons/website_sale_collect/tests/common.py`, `addons/website_sale_collect/tests/test_product_template.py`, `addons/website_sale_collect/tests/test_stock_warehouse.py`, `addons/website_sale_collect/tests/test_payment_provider.py`, `addons/website_sale_collect/tests/test_payment_transaction.py`, `addons/website_sale_collect/tests/__init__.py`, `addons/website_sale_collect/tests/test_click_and_collect_flow.py`, `addons/website_sale_collect/tests/test_delivery_carrier.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 18; representative identifiers: `resource_calendar_pick_up_in_store`, `stock.warehouse0`, `product_pick_up_in_store`, `carrier_pick_up_in_store`, `payment_provider_on_site`, `payment_method_pay_on_site`, `stock_picking_form`, `res_config_settings_form`, `sale_order_view_form`, `delivery_carrier_form`, `website_sale_collect.unavailable_products_warning`, `in_store_delivery_method`, `payment_provider_form`, `payment_confirmation_status`, `product_page_click_and_collect`, `stock_warehouse_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 4; representative evidence: `addons/website_sale_collect/views/delivery_form_templates.xml:4`, `addons/website_sale_collect/views/delivery_form_templates.xml:92`, `addons/website_sale_collect/views/templates.xml:4`, `addons/website_sale_collect/views/templates.xml:29`
- View/action field declarations: 12; representative evidence: `addons/website_sale_collect/views/stock_picking_views.xml:5`, `addons/website_sale_collect/views/stock_picking_views.xml:7`, `addons/website_sale_collect/views/res_config_settings_views.xml:6`, `addons/website_sale_collect/views/res_config_settings_views.xml:8`, `addons/website_sale_collect/views/sale_order_views.xml:5`, `addons/website_sale_collect/views/sale_order_views.xml:7`, `addons/website_sale_collect/views/delivery_carrier_views.xml:7`, `addons/website_sale_collect/views/delivery_carrier_views.xml:8`, `addons/website_sale_collect/views/payment_provider_views.xml:6`, `addons/website_sale_collect/views/payment_provider_views.xml:8`, `addons/website_sale_collect/views/stock_warehouse_views.xml:6`, `addons/website_sale_collect/views/stock_warehouse_views.xml:8`
- Browser assets: 8; representative files: `addons/website_sale_collect/static/src/interactions/product_page.js`, `addons/website_sale_collect/static/src/interactions/payment_form.js`, `addons/website_sale_collect/static/src/interactions/checkout.js`, `addons/website_sale_collect/static/src/js/click_and_collect_availability/click_and_collect_availability.js`, `addons/website_sale_collect/static/src/js/pickup_location_many2one/pickup_location_many2one.js`, `addons/website_sale_collect/static/src/js/location_selector/map_container/map_container.js`, `addons/website_sale_collect/static/src/js/location_selector/location_selector_dialog/location_selector_dialog.js`, `addons/website_sale_collect/static/src/tests/tours/buy_with_click_and_collect.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_sale_collect/__manifest__.py`
- **HTTP entry points:** `addons/website_sale_collect/controllers/delivery.py:10`, `addons/website_sale_collect/controllers/delivery.py:27`, `addons/website_sale_collect/controllers/delivery.py:50`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 10
- Representative model evidence: inherits `sale.order` (addons/website_sale_collect/models/sale_order.py:6); inherits `product.template` (addons/website_sale_collect/models/product_template.py:9); inherits `delivery.carrier` (addons/website_sale_collect/models/delivery_carrier.py:11); inherits `res.config.settings` (addons/website_sale_collect/models/res_config_settings.py:6); inherits `payment.transaction` (addons/website_sale_collect/models/payment_transaction.py:9); inherits `website` (addons/website_sale_collect/models/website.py:9); inherits `sale.order.line` (addons/website_sale_collect/models/sale_order_line.py:6); inherits `stock.warehouse` (addons/website_sale_collect/models/stock_warehouse.py:12); inherits `payment.method` (addons/website_sale_collect/models/payment_method.py:6); inherits `payment.provider` (addons/website_sale_collect/models/payment_provider.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 4
- Route declarations: 3
- Route evidence: `addons/website_sale_collect/controllers/delivery.py:10`, `addons/website_sale_collect/controllers/delivery.py:27`, `addons/website_sale_collect/controllers/delivery.py:50`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base_geolocalize`, `payment_custom`, `website_sale_stock`
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

- `addons/website_sale_collect/__init__.py`
- `addons/website_sale_collect/__manifest__.py`
- `addons/website_sale_collect/const.py`
- `addons/website_sale_collect/controllers/__init__.py`
- `addons/website_sale_collect/controllers/delivery.py`
- `addons/website_sale_collect/controllers/main.py`
- `addons/website_sale_collect/controllers/payment.py`
- `addons/website_sale_collect/data/delivery_carrier_data.xml`
- `addons/website_sale_collect/data/payment_method_data.xml`
- `addons/website_sale_collect/data/payment_provider_data.xml`
- `addons/website_sale_collect/data/product_product_data.xml`
- `addons/website_sale_collect/demo/stock_warehouse_demo.xml`
- `addons/website_sale_collect/i18n/ar.po`
- `addons/website_sale_collect/i18n/az.po`
- `addons/website_sale_collect/i18n/bg.po`
- `addons/website_sale_collect/i18n/bs.po`
- `addons/website_sale_collect/i18n/ca.po`
- `addons/website_sale_collect/i18n/cs.po`
- `addons/website_sale_collect/i18n/da.po`
- `addons/website_sale_collect/i18n/de.po`
- `addons/website_sale_collect/i18n/el.po`
- `addons/website_sale_collect/i18n/es.po`
- `addons/website_sale_collect/i18n/es_419.po`
- `addons/website_sale_collect/i18n/et.po`
- `addons/website_sale_collect/i18n/fa.po`
- `addons/website_sale_collect/i18n/fi.po`
- `addons/website_sale_collect/i18n/fr.po`
- `addons/website_sale_collect/i18n/he.po`
- `addons/website_sale_collect/i18n/hi.po`
- `addons/website_sale_collect/i18n/hr.po`
- `addons/website_sale_collect/i18n/hu.po`
- `addons/website_sale_collect/i18n/id.po`
- `addons/website_sale_collect/i18n/it.po`
- `addons/website_sale_collect/i18n/ja.po`
- `addons/website_sale_collect/i18n/kab.po`
- `addons/website_sale_collect/i18n/ko.po`
- `addons/website_sale_collect/i18n/ku.po`
- `addons/website_sale_collect/i18n/lo.po`
- `addons/website_sale_collect/i18n/lt.po`
- `addons/website_sale_collect/i18n/lv.po`
- `addons/website_sale_collect/i18n/mn.po`
- `addons/website_sale_collect/i18n/my.po`
- `addons/website_sale_collect/i18n/nb.po`
- `addons/website_sale_collect/i18n/nl.po`
- `addons/website_sale_collect/i18n/pl.po`
- `addons/website_sale_collect/i18n/pt.po`
- `addons/website_sale_collect/i18n/pt_BR.po`
- `addons/website_sale_collect/i18n/ro.po`
- `addons/website_sale_collect/i18n/ru.po`
- `addons/website_sale_collect/i18n/sk.po`
- `addons/website_sale_collect/i18n/sl.po`
- `addons/website_sale_collect/i18n/sr@latin.po`
- `addons/website_sale_collect/i18n/sv.po`
- `addons/website_sale_collect/i18n/th.po`
- `addons/website_sale_collect/i18n/tr.po`
- `addons/website_sale_collect/i18n/uk.po`
- `addons/website_sale_collect/i18n/uz.po`
- `addons/website_sale_collect/i18n/vi.po`
- `addons/website_sale_collect/i18n/website_sale_collect.pot`
- `addons/website_sale_collect/i18n/zh_CN.po`
- `addons/website_sale_collect/i18n/zh_TW.po`
- `addons/website_sale_collect/models/__init__.py`
- `addons/website_sale_collect/models/delivery_carrier.py`
- `addons/website_sale_collect/models/payment_method.py`
- `addons/website_sale_collect/models/payment_provider.py`
- `addons/website_sale_collect/models/payment_transaction.py`
- `addons/website_sale_collect/models/product_template.py`
- `addons/website_sale_collect/models/res_config_settings.py`
- `addons/website_sale_collect/models/sale_order.py`
- `addons/website_sale_collect/models/sale_order_line.py`
- `addons/website_sale_collect/models/stock_warehouse.py`
- `addons/website_sale_collect/models/website.py`
- `addons/website_sale_collect/static/description/icon.png`
- `addons/website_sale_collect/static/description/icon.svg`
- `addons/website_sale_collect/static/img/pay_on_site.png`
- `addons/website_sale_collect/static/src/interactions/checkout.js`
- `addons/website_sale_collect/static/src/interactions/payment_form.js`
- `addons/website_sale_collect/static/src/interactions/product_page.js`
- `addons/website_sale_collect/static/src/js/click_and_collect_availability/click_and_collect_availability.js`
- `addons/website_sale_collect/static/src/js/click_and_collect_availability/click_and_collect_availability.xml`
- `addons/website_sale_collect/static/src/js/location_selector/location/location.xml`
- `addons/website_sale_collect/static/src/js/location_selector/location_selector_dialog/location_selector_dialog.js`
- `addons/website_sale_collect/static/src/js/location_selector/location_selector_dialog/location_selector_dialog.xml`
- `addons/website_sale_collect/static/src/js/location_selector/map_container/map_container.js`
- `addons/website_sale_collect/static/src/js/location_selector/map_container/map_container.xml`
- `addons/website_sale_collect/static/src/js/pickup_location_many2one/pickup_location_many2one.js`
- `addons/website_sale_collect/static/src/scss/click_and_collect_availability.scss`
- `addons/website_sale_collect/static/src/tests/tours/buy_with_click_and_collect.js`
- `addons/website_sale_collect/static/src/xml/product_availability.xml`
- `addons/website_sale_collect/tests/__init__.py`
- `addons/website_sale_collect/tests/common.py`
- `addons/website_sale_collect/tests/test_click_and_collect_express_checkout.py`
- `addons/website_sale_collect/tests/test_click_and_collect_flow.py`
- `addons/website_sale_collect/tests/test_delivery_carrier.py`
- `addons/website_sale_collect/tests/test_in_store_delivery.py`
- `addons/website_sale_collect/tests/test_payment_provider.py`
- `addons/website_sale_collect/tests/test_payment_transaction.py`
- `addons/website_sale_collect/tests/test_product_template.py`
- `addons/website_sale_collect/tests/test_sale_order.py`
- `addons/website_sale_collect/tests/test_stock_warehouse.py`
- `addons/website_sale_collect/tests/test_website.py`
- `addons/website_sale_collect/utils.py`
- `addons/website_sale_collect/views/delivery_carrier_views.xml`
- `addons/website_sale_collect/views/delivery_form_templates.xml`
- `addons/website_sale_collect/views/payment_provider_views.xml`
- `addons/website_sale_collect/views/res_config_settings_views.xml`
- `addons/website_sale_collect/views/sale_order_views.xml`
- `addons/website_sale_collect/views/stock_picking_views.xml`
- `addons/website_sale_collect/views/stock_warehouse_views.xml`
- `addons/website_sale_collect/views/templates.xml`
