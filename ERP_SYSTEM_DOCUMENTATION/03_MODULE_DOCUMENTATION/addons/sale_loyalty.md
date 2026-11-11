# Module: sale_loyalty

- **Module ID:** MOD-516
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_loyalty`
- **Manifest:** `addons/sale_loyalty/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Use discounts and loyalty programs in sales orders

**Manifest description:**

Integrate discount and loyalty programs mechanisms in sales orders.

**Scope evidence:** The module contains 94 files, including 31 Python, 10 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `sale`, `loyalty`.

## 2. Module structure

- Model/business logic files: 10
- Controller/API files: 3
- XML/data/view/template files: 10
- Browser asset files: 2
- Security files: 1
- Test files: 14
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/sale_loyalty/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 10 model declarations, 218 methods, 0 constraint handlers, 0 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/sale_loyalty/models/sale_order.py:19`, `addons/sale_loyalty/models/loyalty_reward.py:6`, `addons/sale_loyalty/models/loyalty_program.py:6`, `addons/sale_loyalty/models/loyalty_history.py:6`, `addons/sale_loyalty/models/sale_order_coupon_points.py:6`, `addons/sale_loyalty/models/loyalty_card.py:6`, `addons/sale_loyalty/models/account_move_line.py:6`, `addons/sale_loyalty/models/sale_order_line.py:6`, `addons/sale_loyalty/wizard/sale_loyalty_reward_wizard.py:7`, `addons/sale_loyalty/wizard/sale_loyalty_coupon_wizard.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 1 route declarations.
- **Evidence:** `addons/sale_loyalty/controllers/gift_card.py:10`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 10 XML files and 2 JavaScript/TypeScript files; static XML analysis found 18 record/template/menu identifiers.
- **Evidence:** `addons/sale_loyalty/wizard/sale_loyalty_reward_wizard_views.xml:3`, `addons/sale_loyalty/wizard/sale_loyalty_reward_wizard_views.xml:60`, `addons/sale_loyalty/wizard/sale_loyalty_coupon_wizard_views.xml:3`, `addons/sale_loyalty/wizard/sale_loyalty_coupon_wizard_views.xml:23`, `addons/sale_loyalty/data/sale_loyalty_data.xml:4`, `addons/sale_loyalty/data/sale_loyalty_data.xml:7`, `addons/sale_loyalty/views/sale_portal_templates.xml:4`, `addons/sale_loyalty/views/sale_portal_templates.xml:21`, `addons/sale_loyalty/views/sale_portal_templates.xml:68`, `addons/sale_loyalty/views/sale_portal_templates.xml:107`, `addons/sale_loyalty/views/sale_portal_templates.xml:119`, `addons/sale_loyalty/views/sale_order_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/sale_loyalty/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 14 test files are present.
- **Evidence:** `addons/sale_loyalty/tests/test_program_rules.py`, `addons/sale_loyalty/tests/test_pay_with_gift_card.py`, `addons/sale_loyalty/tests/test_buy_gift_card.py`, `addons/sale_loyalty/tests/test_program_without_code_operations.py`, `addons/sale_loyalty/tests/test_sale_auto_invoice.py`, `addons/sale_loyalty/tests/test_program_multi_company.py`, `addons/sale_loyalty/tests/test_unlink_reward.py`, `addons/sale_loyalty/tests/test_sale_invoicing.py`, `addons/sale_loyalty/tests/test_program_numbers.py`, `addons/sale_loyalty/tests/common.py`, `addons/sale_loyalty/tests/test_loyalty_history.py`, `addons/sale_loyalty/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 10; representative identifiers: `sale_loyalty_reward_wizard_view_form`, `sale_loyalty_reward_wizard_action`, `sale_loyalty_coupon_wizard_view_form`, `sale_loyalty_coupon_wizard_action`, `loyalty.gift_card_product_50`, `loyalty.ewallet_product_50`, `used_gift_card`, `sale_purchased_gift_card`, `sale_order_portal_loyalty_content`, `Gift Card Products Portal`, `Loyalty Points`, `sale_order_view_form_inherit_sale_loyalty`, `loyalty_program_view_form_inherit_sale_loyalty`, `res_partner_form`, `Promotions`, `menu_discount_loyalty_type_config`, `menu_gift_ewallet_type_config`, `loyalty_card_view_form_inherit_sale_loyalty`
- Menus: 3; representative evidence: `addons/sale_loyalty/views/sale_loyalty_menus.xml:4`, `addons/sale_loyalty/views/sale_loyalty_menus.xml:11`, `addons/sale_loyalty/views/sale_loyalty_menus.xml:16`
- Templates: 5; representative evidence: `addons/sale_loyalty/views/sale_portal_templates.xml:4`, `addons/sale_loyalty/views/sale_portal_templates.xml:21`, `addons/sale_loyalty/views/sale_portal_templates.xml:68`, `addons/sale_loyalty/views/sale_portal_templates.xml:107`, `addons/sale_loyalty/views/sale_portal_templates.xml:119`
- View/action field declarations: 16; representative evidence: `addons/sale_loyalty/wizard/sale_loyalty_reward_wizard_views.xml:5`, `addons/sale_loyalty/wizard/sale_loyalty_reward_wizard_views.xml:6`, `addons/sale_loyalty/wizard/sale_loyalty_reward_wizard_views.xml:62`, `addons/sale_loyalty/wizard/sale_loyalty_reward_wizard_views.xml:63`, `addons/sale_loyalty/wizard/sale_loyalty_coupon_wizard_views.xml:5`, `addons/sale_loyalty/wizard/sale_loyalty_coupon_wizard_views.xml:6`, `addons/sale_loyalty/wizard/sale_loyalty_coupon_wizard_views.xml:25`, `addons/sale_loyalty/wizard/sale_loyalty_coupon_wizard_views.xml:26`, `addons/sale_loyalty/views/sale_order_views.xml:6`, `addons/sale_loyalty/views/sale_order_views.xml:9`, `addons/sale_loyalty/views/loyalty_program_views.xml:6`, `addons/sale_loyalty/views/loyalty_program_views.xml:8`
- Browser assets: 2; representative files: `addons/sale_loyalty/static/src/sale_order_form_view/sale_order_static_list.js`, `addons/sale_loyalty/static/src/interactions/gift_card.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale_loyalty/__manifest__.py`
- **HTTP entry points:** `addons/sale_loyalty/controllers/gift_card.py:10`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 10
- Representative model evidence: inherits `sale.order` (addons/sale_loyalty/models/sale_order.py:19); inherits `loyalty.reward` (addons/sale_loyalty/models/loyalty_reward.py:6); inherits `loyalty.program` (addons/sale_loyalty/models/loyalty_program.py:6); inherits `loyalty.history` (addons/sale_loyalty/models/loyalty_history.py:6); `sale.order.coupon.points` (addons/sale_loyalty/models/sale_order_coupon_points.py:6); inherits `loyalty.card` (addons/sale_loyalty/models/loyalty_card.py:6); inherits `account.move.line` (addons/sale_loyalty/models/account_move_line.py:6); inherits `sale.order.line` (addons/sale_loyalty/models/sale_order_line.py:6); `sale.loyalty.reward.wizard` (addons/sale_loyalty/wizard/sale_loyalty_reward_wizard.py:7); `sale.loyalty.coupon.wizard` (addons/sale_loyalty/wizard/sale_loyalty_coupon_wizard.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 1
- Route evidence: `addons/sale_loyalty/controllers/gift_card.py:10`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale`, `loyalty`
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

- `addons/sale_loyalty/__init__.py`
- `addons/sale_loyalty/__manifest__.py`
- `addons/sale_loyalty/controllers/__init__.py`
- `addons/sale_loyalty/controllers/gift_card.py`
- `addons/sale_loyalty/controllers/portal.py`
- `addons/sale_loyalty/data/sale_loyalty_data.xml`
- `addons/sale_loyalty/i18n/ar.po`
- `addons/sale_loyalty/i18n/az.po`
- `addons/sale_loyalty/i18n/bg.po`
- `addons/sale_loyalty/i18n/bs.po`
- `addons/sale_loyalty/i18n/ca.po`
- `addons/sale_loyalty/i18n/cs.po`
- `addons/sale_loyalty/i18n/da.po`
- `addons/sale_loyalty/i18n/de.po`
- `addons/sale_loyalty/i18n/el.po`
- `addons/sale_loyalty/i18n/es.po`
- `addons/sale_loyalty/i18n/es_419.po`
- `addons/sale_loyalty/i18n/et.po`
- `addons/sale_loyalty/i18n/fa.po`
- `addons/sale_loyalty/i18n/fi.po`
- `addons/sale_loyalty/i18n/fr.po`
- `addons/sale_loyalty/i18n/he.po`
- `addons/sale_loyalty/i18n/hi.po`
- `addons/sale_loyalty/i18n/hr.po`
- `addons/sale_loyalty/i18n/hu.po`
- `addons/sale_loyalty/i18n/id.po`
- `addons/sale_loyalty/i18n/it.po`
- `addons/sale_loyalty/i18n/ja.po`
- `addons/sale_loyalty/i18n/kab.po`
- `addons/sale_loyalty/i18n/ko.po`
- `addons/sale_loyalty/i18n/ku.po`
- `addons/sale_loyalty/i18n/lo.po`
- `addons/sale_loyalty/i18n/lt.po`
- `addons/sale_loyalty/i18n/lv.po`
- `addons/sale_loyalty/i18n/mn.po`
- `addons/sale_loyalty/i18n/my.po`
- `addons/sale_loyalty/i18n/nb.po`
- `addons/sale_loyalty/i18n/nl.po`
- `addons/sale_loyalty/i18n/pl.po`
- `addons/sale_loyalty/i18n/pt.po`
- `addons/sale_loyalty/i18n/pt_BR.po`
- `addons/sale_loyalty/i18n/ro.po`
- `addons/sale_loyalty/i18n/ru.po`
- `addons/sale_loyalty/i18n/sale_loyalty.pot`
- `addons/sale_loyalty/i18n/sk.po`
- `addons/sale_loyalty/i18n/sl.po`
- `addons/sale_loyalty/i18n/sr@latin.po`
- `addons/sale_loyalty/i18n/sv.po`
- `addons/sale_loyalty/i18n/th.po`
- `addons/sale_loyalty/i18n/tr.po`
- `addons/sale_loyalty/i18n/uk.po`
- `addons/sale_loyalty/i18n/uz.po`
- `addons/sale_loyalty/i18n/vi.po`
- `addons/sale_loyalty/i18n/zh_CN.po`
- `addons/sale_loyalty/i18n/zh_TW.po`
- `addons/sale_loyalty/models/__init__.py`
- `addons/sale_loyalty/models/account_move_line.py`
- `addons/sale_loyalty/models/loyalty_card.py`
- `addons/sale_loyalty/models/loyalty_history.py`
- `addons/sale_loyalty/models/loyalty_program.py`
- `addons/sale_loyalty/models/loyalty_reward.py`
- `addons/sale_loyalty/models/sale_order.py`
- `addons/sale_loyalty/models/sale_order_coupon_points.py`
- `addons/sale_loyalty/models/sale_order_line.py`
- `addons/sale_loyalty/security/ir.access.csv`
- `addons/sale_loyalty/static/src/interactions/gift_card.js`
- `addons/sale_loyalty/static/src/sale_order_form_view/sale_order_static_list.js`
- `addons/sale_loyalty/static/src/scss/gift_card.scss`
- `addons/sale_loyalty/static/src/xml/discount_menu_widget.xml`
- `addons/sale_loyalty/tests/__init__.py`
- `addons/sale_loyalty/tests/common.py`
- `addons/sale_loyalty/tests/test_buy_gift_card.py`
- `addons/sale_loyalty/tests/test_loyalty.py`
- `addons/sale_loyalty/tests/test_loyalty_history.py`
- `addons/sale_loyalty/tests/test_pay_with_gift_card.py`
- `addons/sale_loyalty/tests/test_program_multi_company.py`
- `addons/sale_loyalty/tests/test_program_numbers.py`
- `addons/sale_loyalty/tests/test_program_rules.py`
- `addons/sale_loyalty/tests/test_program_with_code_operations.py`
- `addons/sale_loyalty/tests/test_program_without_code_operations.py`
- `addons/sale_loyalty/tests/test_sale_auto_invoice.py`
- `addons/sale_loyalty/tests/test_sale_invoicing.py`
- `addons/sale_loyalty/tests/test_unlink_reward.py`
- `addons/sale_loyalty/views/loyalty_card_views.xml`
- `addons/sale_loyalty/views/loyalty_program_views.xml`
- `addons/sale_loyalty/views/res_partner_views.xml`
- `addons/sale_loyalty/views/sale_loyalty_menus.xml`
- `addons/sale_loyalty/views/sale_order_views.xml`
- `addons/sale_loyalty/views/sale_portal_templates.xml`
- `addons/sale_loyalty/wizard/__init__.py`
- `addons/sale_loyalty/wizard/sale_loyalty_coupon_wizard.py`
- `addons/sale_loyalty/wizard/sale_loyalty_coupon_wizard_views.xml`
- `addons/sale_loyalty/wizard/sale_loyalty_reward_wizard.py`
- `addons/sale_loyalty/wizard/sale_loyalty_reward_wizard_views.xml`
