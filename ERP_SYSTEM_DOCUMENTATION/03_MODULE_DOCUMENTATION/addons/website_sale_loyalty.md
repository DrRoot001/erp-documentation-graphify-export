# Module: website_sale_loyalty

- **Module ID:** MOD-637
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_sale_loyalty`
- **Manifest:** `addons/website_sale_loyalty/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Use coupon, promotion, gift cards and loyalty programs in your eCommerce store

**Manifest description:**

Create coupons, promotion codes, gift cards and loyalty programs to boost your sales (free products,
discounts, etc.). Shoppers can use them in the eCommerce checkout.

Coupon & promotion programs can be edited in the Catalog menu of the Website app.

**Scope evidence:** The module contains 102 files, including 27 Python, 10 XML, and 12 JavaScript/TypeScript files. The manifest declares dependencies: `website_sale`, `website_links`, `sale_loyalty`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 5
- XML/data/view/template files: 10
- Browser asset files: 12
- Security files: 1
- Test files: 11
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_sale_loyalty/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 101 methods, 3 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/website_sale_loyalty/models/sale_order.py:13`, `addons/website_sale_loyalty/models/product_product.py:6`, `addons/website_sale_loyalty/models/loyalty_program.py:6`, `addons/website_sale_loyalty/models/loyalty_rule.py:7`, `addons/website_sale_loyalty/models/loyalty_card.py:6`, `addons/website_sale_loyalty/models/sale_order_line.py:8`, `addons/website_sale_loyalty/wizard/coupon_share.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 5 controller files and 8 route declarations.
- **Evidence:** `addons/website_sale_loyalty/controllers/portal.py:10`, `addons/website_sale_loyalty/controllers/cart.py:9`, `addons/website_sale_loyalty/controllers/cart.py:28`, `addons/website_sale_loyalty/controllers/cart.py:34`, `addons/website_sale_loyalty/controllers/delivery.py:12`, `addons/website_sale_loyalty/controllers/main.py:12`, `addons/website_sale_loyalty/controllers/main.py:36`, `addons/website_sale_loyalty/controllers/main.py:59`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 10 XML files and 12 JavaScript/TypeScript files; static XML analysis found 21 record/template/menu identifiers.
- **Evidence:** `addons/website_sale_loyalty/wizard/coupon_share_views.xml:3`, `addons/website_sale_loyalty/wizard/res_config_settings_views.xml:4`, `addons/website_sale_loyalty/data/product_demo.xml:3`, `addons/website_sale_loyalty/data/product_demo.xml:7`, `addons/website_sale_loyalty/data/product_demo.xml:13`, `addons/website_sale_loyalty/data/product_demo.xml:19`, `addons/website_sale_loyalty/views/website_sale_templates.xml:3`, `addons/website_sale_loyalty/views/website_sale_templates.xml:10`, `addons/website_sale_loyalty/views/website_sale_templates.xml:159`, `addons/website_sale_loyalty/views/website_sale_templates.xml:176`, `addons/website_sale_loyalty/views/website_sale_templates.xml:186`, `addons/website_sale_loyalty/views/website_sale_templates.xml:200`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_sale_loyalty/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/website_sale_loyalty/models/sale_order.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 11 test files are present.
- **Evidence:** `addons/website_sale_loyalty/tests/test_website_sale_loyalty_delivery.py`, `addons/website_sale_loyalty/tests/test_sale_coupon_multiwebsite.py`, `addons/website_sale_loyalty/tests/test_shop_sale_coupon.py`, `addons/website_sale_loyalty/tests/test_website_sale_auto_invoice.py`, `addons/website_sale_loyalty/tests/test_shop_multi_reward.py`, `addons/website_sale_loyalty/tests/test_concurrent_promo_code.py`, `addons/website_sale_loyalty/tests/test_free_product_reward.py`, `addons/website_sale_loyalty/tests/test_apply_pending_coupon.py`, `addons/website_sale_loyalty/tests/test_ewallet.py`, `addons/website_sale_loyalty/tests/__init__.py`, `addons/website_sale_loyalty/tests/test_shop_loyalty_payment.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 10; representative identifiers: `coupon_share_view_form`, `res_config_settings_view_form_inherit_website_sale_loyalty`, `loyalty.gift_card_product_50`, `free_shipping_promotion`, `free_shipping_promotion_rule`, `free_shipping_promotion_reward`, `website_sale_loyalty.sale_coupon_result`, `Loyalty, coupon, gift card`, `website_sale_loyalty.layout`, `Payment`, `Shopping Cart Lines`, `website_sale_loyalty.cart_line_product_no_link`, `website_sale_loyalty.cart_summary_inherit_website_gift_card_sale`, `website_sale_loyalty.website_sale_purchased_gift_card`, `Promotion Progress Bar`, `Loyalty`, `menu_discount_loyalty_type_config`, `menu_gift_ewallet_type_config`, `loyalty_program_view_form_inherit_website_sale_loyalty`, `loyalty_program_view_tree_inherit_website_sale_loyalty`
- Menus: 3; representative evidence: `addons/website_sale_loyalty/views/website_sale_loyalty_menus.xml:4`, `addons/website_sale_loyalty/views/website_sale_loyalty_menus.xml:11`, `addons/website_sale_loyalty/views/website_sale_loyalty_menus.xml:13`
- Templates: 9; representative evidence: `addons/website_sale_loyalty/views/website_sale_templates.xml:3`, `addons/website_sale_loyalty/views/website_sale_templates.xml:10`, `addons/website_sale_loyalty/views/website_sale_templates.xml:159`, `addons/website_sale_loyalty/views/website_sale_templates.xml:176`, `addons/website_sale_loyalty/views/website_sale_templates.xml:186`, `addons/website_sale_loyalty/views/website_sale_templates.xml:200`, `addons/website_sale_loyalty/views/website_sale_templates.xml:206`, `addons/website_sale_loyalty/views/website_sale_templates.xml:215`, `addons/website_sale_loyalty/views/website_sale_templates.xml:224`
- View/action field declarations: 10; representative evidence: `addons/website_sale_loyalty/wizard/coupon_share_views.xml:5`, `addons/website_sale_loyalty/wizard/coupon_share_views.xml:6`, `addons/website_sale_loyalty/wizard/res_config_settings_views.xml:6`, `addons/website_sale_loyalty/wizard/res_config_settings_views.xml:8`, `addons/website_sale_loyalty/views/loyalty_program_views.xml:6`, `addons/website_sale_loyalty/views/loyalty_program_views.xml:8`, `addons/website_sale_loyalty/views/loyalty_program_views.xml:39`, `addons/website_sale_loyalty/views/loyalty_program_views.xml:41`, `addons/website_sale_loyalty/views/loyalty_card_views.xml:5`, `addons/website_sale_loyalty/views/loyalty_card_views.xml:7`
- Browser assets: 12; representative files: `addons/website_sale_loyalty/static/src/interactions/coupon_toaster.js`, `addons/website_sale_loyalty/static/src/interactions/checkout.js`, `addons/website_sale_loyalty/static/src/js/promotion_progress_bar/promotion_progress_bar.js`, `addons/website_sale_loyalty/static/src/js/cart_notification/item_added_notification/item_added_notification.js`, `addons/website_sale_loyalty/static/tests/tours/gift_card.js`, `addons/website_sale_loyalty/static/tests/tours/ewallet.js`, `addons/website_sale_loyalty/static/tests/tours/tour_utils.js`, `addons/website_sale_loyalty/static/tests/tours/delivery_with_gift_card.js`, `addons/website_sale_loyalty/static/tests/tours/shipping_discount.js`, `addons/website_sale_loyalty/static/tests/tours/promotions.js`, `addons/website_sale_loyalty/static/tests/tours/test_apply_discount_code.js`, `addons/website_sale_loyalty/static/tests/tours/test_website_sale_free_shipping_discount_line.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_sale_loyalty/__manifest__.py`
- **HTTP entry points:** `addons/website_sale_loyalty/controllers/portal.py:10`, `addons/website_sale_loyalty/controllers/cart.py:9`, `addons/website_sale_loyalty/controllers/cart.py:28`, `addons/website_sale_loyalty/controllers/cart.py:34`, `addons/website_sale_loyalty/controllers/delivery.py:12`, `addons/website_sale_loyalty/controllers/main.py:12`, `addons/website_sale_loyalty/controllers/main.py:36`, `addons/website_sale_loyalty/controllers/main.py:59`
- **Scheduled entry points:** `addons/website_sale_loyalty/models/sale_order.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: inherits `sale.order` (addons/website_sale_loyalty/models/sale_order.py:13); inherits `product.product` (addons/website_sale_loyalty/models/product_product.py:6); `loyalty.program` (addons/website_sale_loyalty/models/loyalty_program.py:6); inherits `loyalty.rule` (addons/website_sale_loyalty/models/loyalty_rule.py:7); inherits `loyalty.card` (addons/website_sale_loyalty/models/loyalty_card.py:6); inherits `sale.order.line` (addons/website_sale_loyalty/models/sale_order_line.py:8); `coupon.share` (addons/website_sale_loyalty/wizard/coupon_share.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 5
- Route declarations: 8
- Route evidence: `addons/website_sale_loyalty/controllers/portal.py:10`, `addons/website_sale_loyalty/controllers/cart.py:9`, `addons/website_sale_loyalty/controllers/cart.py:28`, `addons/website_sale_loyalty/controllers/cart.py:34`, `addons/website_sale_loyalty/controllers/delivery.py:12`, `addons/website_sale_loyalty/controllers/main.py:12`, `addons/website_sale_loyalty/controllers/main.py:36`, `addons/website_sale_loyalty/controllers/main.py:59`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_sale`, `website_links`, `sale_loyalty`
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

- `addons/website_sale_loyalty/__init__.py`
- `addons/website_sale_loyalty/__manifest__.py`
- `addons/website_sale_loyalty/controllers/__init__.py`
- `addons/website_sale_loyalty/controllers/cart.py`
- `addons/website_sale_loyalty/controllers/delivery.py`
- `addons/website_sale_loyalty/controllers/main.py`
- `addons/website_sale_loyalty/controllers/portal.py`
- `addons/website_sale_loyalty/data/product_demo.xml`
- `addons/website_sale_loyalty/i18n/ar.po`
- `addons/website_sale_loyalty/i18n/az.po`
- `addons/website_sale_loyalty/i18n/bg.po`
- `addons/website_sale_loyalty/i18n/bs.po`
- `addons/website_sale_loyalty/i18n/ca.po`
- `addons/website_sale_loyalty/i18n/cs.po`
- `addons/website_sale_loyalty/i18n/da.po`
- `addons/website_sale_loyalty/i18n/de.po`
- `addons/website_sale_loyalty/i18n/el.po`
- `addons/website_sale_loyalty/i18n/es.po`
- `addons/website_sale_loyalty/i18n/es_419.po`
- `addons/website_sale_loyalty/i18n/et.po`
- `addons/website_sale_loyalty/i18n/fa.po`
- `addons/website_sale_loyalty/i18n/fi.po`
- `addons/website_sale_loyalty/i18n/fr.po`
- `addons/website_sale_loyalty/i18n/he.po`
- `addons/website_sale_loyalty/i18n/hi.po`
- `addons/website_sale_loyalty/i18n/hr.po`
- `addons/website_sale_loyalty/i18n/hu.po`
- `addons/website_sale_loyalty/i18n/id.po`
- `addons/website_sale_loyalty/i18n/it.po`
- `addons/website_sale_loyalty/i18n/ja.po`
- `addons/website_sale_loyalty/i18n/kab.po`
- `addons/website_sale_loyalty/i18n/ko.po`
- `addons/website_sale_loyalty/i18n/ku.po`
- `addons/website_sale_loyalty/i18n/lo.po`
- `addons/website_sale_loyalty/i18n/lt.po`
- `addons/website_sale_loyalty/i18n/lv.po`
- `addons/website_sale_loyalty/i18n/mn.po`
- `addons/website_sale_loyalty/i18n/my.po`
- `addons/website_sale_loyalty/i18n/nb.po`
- `addons/website_sale_loyalty/i18n/nl.po`
- `addons/website_sale_loyalty/i18n/pl.po`
- `addons/website_sale_loyalty/i18n/pt.po`
- `addons/website_sale_loyalty/i18n/pt_BR.po`
- `addons/website_sale_loyalty/i18n/ro.po`
- `addons/website_sale_loyalty/i18n/ru.po`
- `addons/website_sale_loyalty/i18n/sk.po`
- `addons/website_sale_loyalty/i18n/sl.po`
- `addons/website_sale_loyalty/i18n/sr@latin.po`
- `addons/website_sale_loyalty/i18n/sv.po`
- `addons/website_sale_loyalty/i18n/th.po`
- `addons/website_sale_loyalty/i18n/tr.po`
- `addons/website_sale_loyalty/i18n/uk.po`
- `addons/website_sale_loyalty/i18n/uz.po`
- `addons/website_sale_loyalty/i18n/vi.po`
- `addons/website_sale_loyalty/i18n/website_sale_loyalty.pot`
- `addons/website_sale_loyalty/i18n/zh_CN.po`
- `addons/website_sale_loyalty/i18n/zh_TW.po`
- `addons/website_sale_loyalty/models/__init__.py`
- `addons/website_sale_loyalty/models/loyalty_card.py`
- `addons/website_sale_loyalty/models/loyalty_program.py`
- `addons/website_sale_loyalty/models/loyalty_rule.py`
- `addons/website_sale_loyalty/models/product_product.py`
- `addons/website_sale_loyalty/models/sale_order.py`
- `addons/website_sale_loyalty/models/sale_order_line.py`
- `addons/website_sale_loyalty/security/ir.access.csv`
- `addons/website_sale_loyalty/static/description/icon.png`
- `addons/website_sale_loyalty/static/description/icon.svg`
- `addons/website_sale_loyalty/static/description/icon_hi.png`
- `addons/website_sale_loyalty/static/src/interactions/checkout.js`
- `addons/website_sale_loyalty/static/src/interactions/coupon_toaster.js`
- `addons/website_sale_loyalty/static/src/js/cart_notification/item_added_notification/item_added_notification.js`
- `addons/website_sale_loyalty/static/src/js/cart_notification/item_added_notification/item_added_notification.xml`
- `addons/website_sale_loyalty/static/src/js/portal_loyalty_card.xml`
- `addons/website_sale_loyalty/static/src/js/promotion_progress_bar/promotion_progress_bar.js`
- `addons/website_sale_loyalty/static/src/js/promotion_progress_bar/promotion_progress_bar.xml`
- `addons/website_sale_loyalty/static/tests/tours/delivery_with_gift_card.js`
- `addons/website_sale_loyalty/static/tests/tours/ewallet.js`
- `addons/website_sale_loyalty/static/tests/tours/gift_card.js`
- `addons/website_sale_loyalty/static/tests/tours/promotions.js`
- `addons/website_sale_loyalty/static/tests/tours/shipping_discount.js`
- `addons/website_sale_loyalty/static/tests/tours/test_apply_discount_code.js`
- `addons/website_sale_loyalty/static/tests/tours/test_website_sale_free_shipping_discount_line.js`
- `addons/website_sale_loyalty/static/tests/tours/tour_utils.js`
- `addons/website_sale_loyalty/tests/__init__.py`
- `addons/website_sale_loyalty/tests/test_apply_pending_coupon.py`
- `addons/website_sale_loyalty/tests/test_concurrent_promo_code.py`
- `addons/website_sale_loyalty/tests/test_ewallet.py`
- `addons/website_sale_loyalty/tests/test_free_product_reward.py`
- `addons/website_sale_loyalty/tests/test_sale_coupon_multiwebsite.py`
- `addons/website_sale_loyalty/tests/test_shop_loyalty_payment.py`
- `addons/website_sale_loyalty/tests/test_shop_multi_reward.py`
- `addons/website_sale_loyalty/tests/test_shop_sale_coupon.py`
- `addons/website_sale_loyalty/tests/test_website_sale_auto_invoice.py`
- `addons/website_sale_loyalty/tests/test_website_sale_loyalty_delivery.py`
- `addons/website_sale_loyalty/views/loyalty_card_views.xml`
- `addons/website_sale_loyalty/views/loyalty_program_views.xml`
- `addons/website_sale_loyalty/views/website_sale_loyalty_menus.xml`
- `addons/website_sale_loyalty/views/website_sale_templates.xml`
- `addons/website_sale_loyalty/wizard/__init__.py`
- `addons/website_sale_loyalty/wizard/coupon_share.py`
- `addons/website_sale_loyalty/wizard/coupon_share_views.xml`
- `addons/website_sale_loyalty/wizard/res_config_settings_views.xml`
