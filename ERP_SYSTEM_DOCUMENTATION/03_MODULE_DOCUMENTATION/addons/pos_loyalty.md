# Module: pos_loyalty

- **Module ID:** MOD-436
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_loyalty`
- **Manifest:** `addons/pos_loyalty/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point Of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Use Coupons, Gift Cards and Loyalty programs in Point of Sale

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 151 files, including 29 Python, 16 XML, and 54 JavaScript/TypeScript files. The manifest declares dependencies: `loyalty`, `point_of_sale`.

## 2. Module structure

- Model/business logic files: 14
- Controller/API files: 0
- XML/data/view/template files: 16
- Browser asset files: 54
- Security files: 1
- Test files: 11
- Scheduled/automation evidence files: 0
- Reporting evidence files: 5

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/pos_loyalty/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 14 model declarations, 196 methods, 0 constraint handlers, 0 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/pos_loyalty/models/product_product.py:4`, `addons/pos_loyalty/models/loyalty_reward.py:10`, `addons/pos_loyalty/models/barcode_rule.py:7`, `addons/pos_loyalty/models/product_template.py:4`, `addons/pos_loyalty/models/pos_config.py:6`, `addons/pos_loyalty/models/loyalty_program.py:7`, `addons/pos_loyalty/models/loyalty_rule.py:8`, `addons/pos_loyalty/models/pos_session.py:6`, `addons/pos_loyalty/models/loyalty_card.py:7`, `addons/pos_loyalty/models/pos_order.py:11`, `addons/pos_loyalty/models/loyalty_mail.py:7`, `addons/pos_loyalty/models/account_move_line.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 16 XML files and 54 JavaScript/TypeScript files; static XML analysis found 24 record/template/menu identifiers.
- **Evidence:** `addons/pos_loyalty/data/gift_card_data.xml:3`, `addons/pos_loyalty/data/gift_card_data.xml:7`, `addons/pos_loyalty/data/gift_card_data.xml:12`, `addons/pos_loyalty/data/default_barcode_patterns.xml:3`, `addons/pos_loyalty/data/pos_loyalty_demo.xml:5`, `addons/pos_loyalty/data/pos_loyalty_demo.xml:15`, `addons/pos_loyalty/data/pos_loyalty_demo.xml:20`, `addons/pos_loyalty/data/pos_loyalty_demo.xml:27`, `addons/pos_loyalty/data/pos_loyalty_demo.xml:31`, `addons/pos_loyalty/data/pos_loyalty_demo.xml:35`, `addons/pos_loyalty/data/pos_loyalty_demo.xml:59`, `addons/pos_loyalty/data/pos_loyalty_demo.xml:71`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/pos_loyalty/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 5 files contain report-action/template indicators.
- **Evidence:** `addons/pos_loyalty/models/loyalty_program.py`, `addons/pos_loyalty/models/pos_order.py`, `addons/pos_loyalty/models/loyalty_mail.py`, `addons/pos_loyalty/receipt/pos_order_receipt.py`, `addons/pos_loyalty/tests/test_gift_card_communication.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 11 test files are present.
- **Evidence:** `addons/pos_loyalty/tests/test_frontend.py`, `addons/pos_loyalty/tests/test_loyalty_mirror.py`, `addons/pos_loyalty/tests/test_unlink_reward.py`, `addons/pos_loyalty/tests/test_pos_loyalty_points.py`, `addons/pos_loyalty/tests/common.py`, `addons/pos_loyalty/tests/test_loyalty_history.py`, `addons/pos_loyalty/tests/test_product_loading.py`, `addons/pos_loyalty/tests/test_service_fee.py`, `addons/pos_loyalty/tests/test_gift_card_communication.py`, `addons/pos_loyalty/tests/__init__.py`, `addons/pos_loyalty/tests/test_order_receipt.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 16; representative identifiers: `loyalty.gift_card_product_50`, `loyalty.ewallet_product_50`, `loyalty.gift_card_program`, `barcode_rule_coupon`, `15_pc_on_next_order`, `15_pc_on_next_order_rule`, `15_pc_on_next_order_reward`, `loyalty.3_cabinets_plus_1_free`, `loyalty.10_percent_with_code`, `loyalty.10_percent_coupon`, `simple_pen`, `loyalty_program`, `loyalty_program_rule`, `loyalty_program_reward`, `product.product_product_6`, `pos_loyalty.pos_order_receipt`, `loyalty_mail_view_tree_inherit_pos_loyalty`, `Discount &amp; Loyalty`, `Gift cards &amp; eWallet`, `loyalty_program_view_form_inherit_pos_loyalty`
- Menus: 2; representative evidence: `addons/pos_loyalty/views/pos_loyalty_menu_views.xml:3`, `addons/pos_loyalty/views/pos_loyalty_menu_views.xml:12`
- Templates: 1; representative evidence: `addons/pos_loyalty/receipt/pos_order_receipt.xml:4`
- View/action field declarations: 12; representative evidence: `addons/pos_loyalty/views/loyalty_mail_views.xml:5`, `addons/pos_loyalty/views/loyalty_mail_views.xml:7`, `addons/pos_loyalty/views/loyalty_program_views.xml:6`, `addons/pos_loyalty/views/loyalty_program_views.xml:8`, `addons/pos_loyalty/views/loyalty_program_views.xml:32`, `addons/pos_loyalty/views/loyalty_program_views.xml:34`, `addons/pos_loyalty/views/res_config_settings_view.xml:5`, `addons/pos_loyalty/views/res_config_settings_view.xml:7`, `addons/pos_loyalty/views/res_partner_views.xml:6`, `addons/pos_loyalty/views/res_partner_views.xml:8`, `addons/pos_loyalty/views/loyalty_card_views.xml:5`, `addons/pos_loyalty/views/loyalty_card_views.xml:7`
- Browser assets: 54; representative files: `addons/pos_loyalty/static/src/app/services/customer_display_plugin.js`, `addons/pos_loyalty/static/src/app/services/pos_store.js`, `addons/pos_loyalty/static/src/app/models/data_service_options.js`, `addons/pos_loyalty/static/src/app/models/loyalty_program.js`, `addons/pos_loyalty/static/src/app/models/loyalty_card.js`, `addons/pos_loyalty/static/src/app/models/pos_order_line.js`, `addons/pos_loyalty/static/src/app/models/loyalty_reward.js`, `addons/pos_loyalty/static/src/app/models/loyalty_rule.js`, `addons/pos_loyalty/static/src/app/models/pos_order.js`, `addons/pos_loyalty/static/src/app/plugins/pos_data_plugin.js`, `addons/pos_loyalty/static/src/app/utils/order_payment_validation.js`, `addons/pos_loyalty/static/src/app/screens/product_screen/product_screen.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_loyalty/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/pos_loyalty/models/loyalty_program.py`, `addons/pos_loyalty/models/pos_order.py`, `addons/pos_loyalty/models/loyalty_mail.py`, `addons/pos_loyalty/receipt/pos_order_receipt.py`, `addons/pos_loyalty/tests/test_gift_card_communication.py`

## 7. Database interactions

- Model declarations: 14
- Representative model evidence: inherits `product.product` (addons/pos_loyalty/models/product_product.py:4); `loyalty.reward` (addons/pos_loyalty/models/loyalty_reward.py:10); inherits `barcode.rule` (addons/pos_loyalty/models/barcode_rule.py:7); inherits `product.template` (addons/pos_loyalty/models/product_template.py:4); inherits `pos.config` (addons/pos_loyalty/models/pos_config.py:6); `loyalty.program` (addons/pos_loyalty/models/loyalty_program.py:7); `loyalty.rule` (addons/pos_loyalty/models/loyalty_rule.py:8); inherits `pos.session` (addons/pos_loyalty/models/pos_session.py:6); `loyalty.card` (addons/pos_loyalty/models/loyalty_card.py:7); inherits `pos.order` (addons/pos_loyalty/models/pos_order.py:11); inherits `loyalty.mail` (addons/pos_loyalty/models/loyalty_mail.py:7); inherits `account.move.line` (addons/pos_loyalty/models/account_move_line.py:6); inherits `pos.order.line` (addons/pos_loyalty/models/pos_order_line.py:7); inherits `pos.order.receipt` (addons/pos_loyalty/receipt/pos_order_receipt.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `loyalty`, `point_of_sale`
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

- `addons/pos_loyalty/__init__.py`
- `addons/pos_loyalty/__manifest__.py`
- `addons/pos_loyalty/data/default_barcode_patterns.xml`
- `addons/pos_loyalty/data/gift_card_data.xml`
- `addons/pos_loyalty/data/pos_loyalty_demo.xml`
- `addons/pos_loyalty/i18n/ar.po`
- `addons/pos_loyalty/i18n/az.po`
- `addons/pos_loyalty/i18n/bg.po`
- `addons/pos_loyalty/i18n/bs.po`
- `addons/pos_loyalty/i18n/ca.po`
- `addons/pos_loyalty/i18n/cs.po`
- `addons/pos_loyalty/i18n/da.po`
- `addons/pos_loyalty/i18n/de.po`
- `addons/pos_loyalty/i18n/el.po`
- `addons/pos_loyalty/i18n/es.po`
- `addons/pos_loyalty/i18n/es_419.po`
- `addons/pos_loyalty/i18n/et.po`
- `addons/pos_loyalty/i18n/fa.po`
- `addons/pos_loyalty/i18n/fi.po`
- `addons/pos_loyalty/i18n/fr.po`
- `addons/pos_loyalty/i18n/he.po`
- `addons/pos_loyalty/i18n/hi.po`
- `addons/pos_loyalty/i18n/hr.po`
- `addons/pos_loyalty/i18n/hu.po`
- `addons/pos_loyalty/i18n/id.po`
- `addons/pos_loyalty/i18n/it.po`
- `addons/pos_loyalty/i18n/ja.po`
- `addons/pos_loyalty/i18n/kab.po`
- `addons/pos_loyalty/i18n/ko.po`
- `addons/pos_loyalty/i18n/ku.po`
- `addons/pos_loyalty/i18n/lo.po`
- `addons/pos_loyalty/i18n/lt.po`
- `addons/pos_loyalty/i18n/lv.po`
- `addons/pos_loyalty/i18n/mn.po`
- `addons/pos_loyalty/i18n/my.po`
- `addons/pos_loyalty/i18n/nb.po`
- `addons/pos_loyalty/i18n/nl.po`
- `addons/pos_loyalty/i18n/pl.po`
- `addons/pos_loyalty/i18n/pos_loyalty.pot`
- `addons/pos_loyalty/i18n/pt.po`
- `addons/pos_loyalty/i18n/pt_BR.po`
- `addons/pos_loyalty/i18n/ro.po`
- `addons/pos_loyalty/i18n/ru.po`
- `addons/pos_loyalty/i18n/sk.po`
- `addons/pos_loyalty/i18n/sl.po`
- `addons/pos_loyalty/i18n/sr@latin.po`
- `addons/pos_loyalty/i18n/sv.po`
- `addons/pos_loyalty/i18n/th.po`
- `addons/pos_loyalty/i18n/tr.po`
- `addons/pos_loyalty/i18n/uk.po`
- `addons/pos_loyalty/i18n/uz.po`
- `addons/pos_loyalty/i18n/vi.po`
- `addons/pos_loyalty/i18n/zh_CN.po`
- `addons/pos_loyalty/i18n/zh_TW.po`
- `addons/pos_loyalty/models/__init__.py`
- `addons/pos_loyalty/models/account_move_line.py`
- `addons/pos_loyalty/models/barcode_rule.py`
- `addons/pos_loyalty/models/loyalty_card.py`
- `addons/pos_loyalty/models/loyalty_mail.py`
- `addons/pos_loyalty/models/loyalty_program.py`
- `addons/pos_loyalty/models/loyalty_reward.py`
- `addons/pos_loyalty/models/loyalty_rule.py`
- `addons/pos_loyalty/models/pos_config.py`
- `addons/pos_loyalty/models/pos_order.py`
- `addons/pos_loyalty/models/pos_order_line.py`
- `addons/pos_loyalty/models/pos_session.py`
- `addons/pos_loyalty/models/product_product.py`
- `addons/pos_loyalty/models/product_template.py`
- `addons/pos_loyalty/receipt/__init__.py`
- `addons/pos_loyalty/receipt/pos_order_receipt.py`
- `addons/pos_loyalty/receipt/pos_order_receipt.xml`
- `addons/pos_loyalty/security/ir.access.csv`
- `addons/pos_loyalty/static/img/simple_pen.png`
- `addons/pos_loyalty/static/src/app/components/popups/manage_giftcard_popup/manage_giftcard_popup.js`
- `addons/pos_loyalty/static/src/app/components/popups/manage_giftcard_popup/manage_giftcard_popup.xml`
- `addons/pos_loyalty/static/src/app/css/Loyalty.scss`
- `addons/pos_loyalty/static/src/app/models/data_service_options.js`
- `addons/pos_loyalty/static/src/app/models/loyalty_card.js`
- `addons/pos_loyalty/static/src/app/models/loyalty_program.js`
- `addons/pos_loyalty/static/src/app/models/loyalty_reward.js`
- `addons/pos_loyalty/static/src/app/models/loyalty_rule.js`
- `addons/pos_loyalty/static/src/app/models/pos_order.js`
- `addons/pos_loyalty/static/src/app/models/pos_order_line.js`
- `addons/pos_loyalty/static/src/app/plugins/pos_data_plugin.js`
- `addons/pos_loyalty/static/src/app/screens/partner_list_screen/partner_line/partner_line.js`
- `addons/pos_loyalty/static/src/app/screens/partner_list_screen/partner_line/partner_line.xml`
- `addons/pos_loyalty/static/src/app/screens/partner_list_screen/partner_list_screen.js`
- `addons/pos_loyalty/static/src/app/screens/product_screen/control_buttons/control_buttons.js`
- `addons/pos_loyalty/static/src/app/screens/product_screen/control_buttons/control_buttons.xml`
- `addons/pos_loyalty/static/src/app/screens/product_screen/order_summary/order_summary.js`
- `addons/pos_loyalty/static/src/app/screens/product_screen/order_summary/order_summary.xml`
- `addons/pos_loyalty/static/src/app/screens/product_screen/product_screen.js`
- `addons/pos_loyalty/static/src/app/screens/ticket_screen/ticket_screen.js`
- `addons/pos_loyalty/static/src/app/services/customer_display_plugin.js`
- `addons/pos_loyalty/static/src/app/services/pos_store.js`
- `addons/pos_loyalty/static/src/app/utils/order_payment_validation.js`
- `addons/pos_loyalty/static/src/app/utils/printer/generate_printer_data.js`
- `addons/pos_loyalty/static/src/customer_display/customer_display.xml`
- `addons/pos_loyalty/static/src/portal/loyalty_card_dialog.xml`
- `addons/pos_loyalty/static/tests/tours/e_wallet_program_tour.js`
- `addons/pos_loyalty/static/tests/tours/gift_card_program_tour.js`
- `addons/pos_loyalty/static/tests/tours/loyalty_history_tour.js`
- `addons/pos_loyalty/static/tests/tours/loyalty_mirror_tour.js`
- `addons/pos_loyalty/static/tests/tours/multiple_gift_wallet_programs_tour.js`
- `addons/pos_loyalty/static/tests/tours/order_receipt.js`
- `addons/pos_loyalty/static/tests/tours/pos_loyalty_loyalty_program_tour.js`
- `addons/pos_loyalty/static/tests/tours/pos_loyalty_reward_button_tour.js`
- `addons/pos_loyalty/static/tests/tours/pos_loyalty_tour.js`
- `addons/pos_loyalty/static/tests/tours/pos_loyalty_validity_tour.js`
- `addons/pos_loyalty/static/tests/tours/service_fee_payment_reward_tour.js`
- `addons/pos_loyalty/static/tests/tours/service_fee_promotion_tour.js`
- `addons/pos_loyalty/static/tests/tours/utils/pos_loyalty_util.js`
- `addons/pos_loyalty/static/tests/unit/components/manage_giftcard_popup.test.js`
- `addons/pos_loyalty/static/tests/unit/components/order_receipt.test.js`
- `addons/pos_loyalty/static/tests/unit/components/screens/control_buttons.test.js`
- `addons/pos_loyalty/static/tests/unit/components/screens/order_summary.test.js`
- `addons/pos_loyalty/static/tests/unit/components/screens/partner_line.test.js`
- `addons/pos_loyalty/static/tests/unit/customer_display/customer_display.test.js`
- `addons/pos_loyalty/static/tests/unit/data/barcode_nomenclature.data.js`
- `addons/pos_loyalty/static/tests/unit/data/barcode_rule.data.js`
- `addons/pos_loyalty/static/tests/unit/data/loyalty_card.data.js`
- `addons/pos_loyalty/static/tests/unit/data/loyalty_program.data.js`
- `addons/pos_loyalty/static/tests/unit/data/loyalty_reward.data.js`
- `addons/pos_loyalty/static/tests/unit/data/loyalty_rule.data.js`
- `addons/pos_loyalty/static/tests/unit/data/pos_order.data.js`
- `addons/pos_loyalty/static/tests/unit/data/pos_order_line.data.js`
- `addons/pos_loyalty/static/tests/unit/data/pos_session.data.js`
- `addons/pos_loyalty/static/tests/unit/data/product_product.data.js`
- `addons/pos_loyalty/static/tests/unit/data/product_template.data.js`
- `addons/pos_loyalty/static/tests/unit/models/pos_order.test.js`
- `addons/pos_loyalty/static/tests/unit/models/pos_order_line.test.js`
- `addons/pos_loyalty/static/tests/unit/receipt_utils.js`
- `addons/pos_loyalty/static/tests/unit/screens/ticket_screen.test.js`
- `addons/pos_loyalty/static/tests/unit/utils.js`
- `addons/pos_loyalty/tests/__init__.py`
- `addons/pos_loyalty/tests/common.py`
- `addons/pos_loyalty/tests/test_frontend.py`
- `addons/pos_loyalty/tests/test_gift_card_communication.py`
- `addons/pos_loyalty/tests/test_loyalty_history.py`
- `addons/pos_loyalty/tests/test_loyalty_mirror.py`
- `addons/pos_loyalty/tests/test_order_receipt.py`
- `addons/pos_loyalty/tests/test_pos_loyalty_points.py`
- `addons/pos_loyalty/tests/test_product_loading.py`
- `addons/pos_loyalty/tests/test_service_fee.py`
- `addons/pos_loyalty/tests/test_unlink_reward.py`
- `addons/pos_loyalty/views/loyalty_card_views.xml`
- `addons/pos_loyalty/views/loyalty_mail_views.xml`
- `addons/pos_loyalty/views/loyalty_program_views.xml`
- `addons/pos_loyalty/views/pos_loyalty_menu_views.xml`
- `addons/pos_loyalty/views/res_config_settings_view.xml`
- `addons/pos_loyalty/views/res_partner_views.xml`
