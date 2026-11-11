# Module: pos_restaurant

- **Module ID:** MOD-447
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_restaurant`
- **Manifest:** `addons/pos_restaurant/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Sales/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Restaurant extensions for the Point of Sale

**Manifest description:**

This module adds several features to the Point of Sale that are specific to restaurant management:
- Bill Printing: Allows you to print a receipt before the order is paid
- Bill Splitting: Allows you to split an order into different orders
- Kitchen Order Printing: allows you to print orders updates to kitchen or bar printers

**Scope evidence:** The module contains 297 files, including 21 Python, 42 XML, and 108 JavaScript/TypeScript files. The manifest declares dependencies: `point_of_sale`.

## 2. Module structure

- Model/business logic files: 13
- Controller/API files: 0
- XML/data/view/template files: 42
- Browser asset files: 108
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/pos_restaurant/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 13 model declarations, 97 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/pos_restaurant/models/pos_restaurant.py:24`, `addons/pos_restaurant/models/pos_restaurant.py:118`, `addons/pos_restaurant/models/product_template.py:6`, `addons/pos_restaurant/models/pos_config.py:7`, `addons/pos_restaurant/models/res_config_settings.py:6`, `addons/pos_restaurant/models/pos_category.py:4`, `addons/pos_restaurant/models/restaurant_order_course.py:7`, `addons/pos_restaurant/models/pos_session.py:7`, `addons/pos_restaurant/models/pos_order.py:6`, `addons/pos_restaurant/models/pos_preset.py:5`, `addons/pos_restaurant/models/pos_course.py:4`, `addons/pos_restaurant/models/pos_order_line.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 42 XML files and 108 JavaScript/TypeScript files; static XML analysis found 163 record/template/menu identifiers.
- **Evidence:** `addons/pos_restaurant/receipt/pos_order_change_receipt.xml:4`, `addons/pos_restaurant/receipt/pos_order_receipt.xml:4`, `addons/pos_restaurant/views/pos_category_view.xml:3`, `addons/pos_restaurant/views/pos_category_view.xml:16`, `addons/pos_restaurant/views/pos_category_view.xml:27`, `addons/pos_restaurant/views/res_config_settings_views.xml:3`, `addons/pos_restaurant/views/pos_preset_views.xml:3`, `addons/pos_restaurant/views/pos_order_views.xml:4`, `addons/pos_restaurant/views/pos_course_views.xml:2`, `addons/pos_restaurant/views/pos_course_views.xml:14`, `addons/pos_restaurant/views/pos_course_views.xml:29`, `addons/pos_restaurant/views/pos_course_views.xml:42`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/pos_restaurant/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/pos_restaurant/models/pos_restaurant.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/pos_restaurant/tests/test_pos_restaurant_flow.py`, `addons/pos_restaurant/tests/test_frontend.py`, `addons/pos_restaurant/tests/test_devices_synchronization.py`, `addons/pos_restaurant/tests/__init__.py`, `addons/pos_restaurant/tests/test_order_receipt.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 42; representative identifiers: `pos_restaurant.pos_order_change_receipt`, `pos_restaurant.pos_order_receipt_header`, `view_pos_category_form_inherit_course`, `pos_restaurant_product_pos_category_tree_view`, `pos_restaurant_pos_category_kanban_view`, `res_config_settings_view_form`, `view_pos_preset_form_inherit_pos_restaurant`, `view_pos_pos_form`, `view_pos_course_list`, `view_pos_course_form`, `action_pos_course`, `Courses`, `view_restaurant_floor_form`, `view_restaurant_floor_tree`, `view_restaurant_floor_search`, `view_restaurant_floor_kanban`, `action_restaurant_floor_form`, `view_restaurant_table_form`, `menu_restaurant_floor_all`, `food`
- Menus: 2; representative evidence: `addons/pos_restaurant/views/pos_course_views.xml:42`, `addons/pos_restaurant/views/pos_restaurant_views.xml:98`
- Templates: 2; representative evidence: `addons/pos_restaurant/receipt/pos_order_change_receipt.xml:4`, `addons/pos_restaurant/receipt/pos_order_receipt.xml:4`
- View/action field declarations: 30; representative evidence: `addons/pos_restaurant/views/pos_category_view.xml:5`, `addons/pos_restaurant/views/pos_category_view.xml:7`, `addons/pos_restaurant/views/pos_category_view.xml:18`, `addons/pos_restaurant/views/pos_category_view.xml:20`, `addons/pos_restaurant/views/pos_category_view.xml:29`, `addons/pos_restaurant/views/pos_category_view.xml:31`, `addons/pos_restaurant/views/res_config_settings_views.xml:5`, `addons/pos_restaurant/views/res_config_settings_views.xml:7`, `addons/pos_restaurant/views/pos_preset_views.xml:5`, `addons/pos_restaurant/views/pos_preset_views.xml:7`, `addons/pos_restaurant/views/pos_order_views.xml:6`, `addons/pos_restaurant/views/pos_order_views.xml:8`
- Browser assets: 108; representative files: `addons/pos_restaurant/static/src/app/services/pos_store.js`, `addons/pos_restaurant/static/src/app/models/restaurant_order_course.js`, `addons/pos_restaurant/static/src/app/models/data_service_options.js`, `addons/pos_restaurant/static/src/app/models/pos_order_line.js`, `addons/pos_restaurant/static/src/app/models/pos_order.js`, `addons/pos_restaurant/static/src/app/models/restaurant_table.js`, `addons/pos_restaurant/static/src/app/models/pos_config.js`, `addons/pos_restaurant/static/src/app/hooks/floor_plan_hook.js`, `addons/pos_restaurant/static/src/app/utils/order_payment_validation.js`, `addons/pos_restaurant/static/src/app/utils/devices_synchronisation.js`, `addons/pos_restaurant/static/src/app/services/floor_plan/floor_plan_service.js`, `addons/pos_restaurant/static/src/app/services/floor_plan/elements/floor.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_restaurant/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/pos_restaurant/models/pos_restaurant.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 13
- Representative model evidence: `restaurant.floor` (addons/pos_restaurant/models/pos_restaurant.py:24); `restaurant.table` (addons/pos_restaurant/models/pos_restaurant.py:118); inherits `product.template` (addons/pos_restaurant/models/product_template.py:6); inherits `pos.config` (addons/pos_restaurant/models/pos_config.py:7); inherits `res.config.settings` (addons/pos_restaurant/models/res_config_settings.py:6); inherits `pos.category` (addons/pos_restaurant/models/pos_category.py:4); `restaurant.order.course` (addons/pos_restaurant/models/restaurant_order_course.py:7); inherits `pos.session` (addons/pos_restaurant/models/pos_session.py:7); inherits `pos.order` (addons/pos_restaurant/models/pos_order.py:6); inherits `pos.preset` (addons/pos_restaurant/models/pos_preset.py:5); `pos.course` (addons/pos_restaurant/models/pos_course.py:4); inherits `pos.order.line` (addons/pos_restaurant/models/pos_order_line.py:6); inherits `pos.order.receipt` (addons/pos_restaurant/receipt/pos_order_receipt.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `point_of_sale`
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

- `addons/pos_restaurant/__init__.py`
- `addons/pos_restaurant/__manifest__.py`
- `addons/pos_restaurant/data/demo_data.xml`
- `addons/pos_restaurant/data/scenarios/bar_category_data.xml`
- `addons/pos_restaurant/data/scenarios/bar_demo_data.xml`
- `addons/pos_restaurant/data/scenarios/restaurant_category_data.xml`
- `addons/pos_restaurant/data/scenarios/restaurant_demo_data.xml`
- `addons/pos_restaurant/data/scenarios/restaurant_demo_session.xml`
- `addons/pos_restaurant/data/scenarios/restaurant_floor.xml`
- `addons/pos_restaurant/data/scenarios/restaurant_preset.xml`
- `addons/pos_restaurant/i18n/af.po`
- `addons/pos_restaurant/i18n/ar.po`
- `addons/pos_restaurant/i18n/az.po`
- `addons/pos_restaurant/i18n/bg.po`
- `addons/pos_restaurant/i18n/bs.po`
- `addons/pos_restaurant/i18n/ca.po`
- `addons/pos_restaurant/i18n/cs.po`
- `addons/pos_restaurant/i18n/da.po`
- `addons/pos_restaurant/i18n/de.po`
- `addons/pos_restaurant/i18n/el.po`
- `addons/pos_restaurant/i18n/es.po`
- `addons/pos_restaurant/i18n/es_419.po`
- `addons/pos_restaurant/i18n/es_CL.po`
- `addons/pos_restaurant/i18n/et.po`
- `addons/pos_restaurant/i18n/eu.po`
- `addons/pos_restaurant/i18n/fa.po`
- `addons/pos_restaurant/i18n/fi.po`
- `addons/pos_restaurant/i18n/fr.po`
- `addons/pos_restaurant/i18n/fr_CA.po`
- `addons/pos_restaurant/i18n/gl.po`
- `addons/pos_restaurant/i18n/gu.po`
- `addons/pos_restaurant/i18n/he.po`
- `addons/pos_restaurant/i18n/hi.po`
- `addons/pos_restaurant/i18n/hr.po`
- `addons/pos_restaurant/i18n/hu.po`
- `addons/pos_restaurant/i18n/id.po`
- `addons/pos_restaurant/i18n/is.po`
- `addons/pos_restaurant/i18n/it.po`
- `addons/pos_restaurant/i18n/ja.po`
- `addons/pos_restaurant/i18n/ka.po`
- `addons/pos_restaurant/i18n/kab.po`
- `addons/pos_restaurant/i18n/km.po`
- `addons/pos_restaurant/i18n/ko.po`
- `addons/pos_restaurant/i18n/ku.po`
- `addons/pos_restaurant/i18n/lo.po`
- `addons/pos_restaurant/i18n/lt.po`
- `addons/pos_restaurant/i18n/lv.po`
- `addons/pos_restaurant/i18n/mk.po`
- `addons/pos_restaurant/i18n/mn.po`
- `addons/pos_restaurant/i18n/my.po`
- `addons/pos_restaurant/i18n/nb.po`
- `addons/pos_restaurant/i18n/nl.po`
- `addons/pos_restaurant/i18n/pl.po`
- `addons/pos_restaurant/i18n/pos_restaurant.pot`
- `addons/pos_restaurant/i18n/pt.po`
- `addons/pos_restaurant/i18n/pt_BR.po`
- `addons/pos_restaurant/i18n/ro.po`
- `addons/pos_restaurant/i18n/ru.po`
- `addons/pos_restaurant/i18n/sk.po`
- `addons/pos_restaurant/i18n/sl.po`
- `addons/pos_restaurant/i18n/sq.po`
- `addons/pos_restaurant/i18n/sr@latin.po`
- `addons/pos_restaurant/i18n/sv.po`
- `addons/pos_restaurant/i18n/th.po`
- `addons/pos_restaurant/i18n/tr.po`
- `addons/pos_restaurant/i18n/uk.po`
- `addons/pos_restaurant/i18n/uz.po`
- `addons/pos_restaurant/i18n/vi.po`
- `addons/pos_restaurant/i18n/zh_CN.po`
- `addons/pos_restaurant/i18n/zh_TW.po`
- `addons/pos_restaurant/models/__init__.py`
- `addons/pos_restaurant/models/pos_category.py`
- `addons/pos_restaurant/models/pos_config.py`
- `addons/pos_restaurant/models/pos_course.py`
- `addons/pos_restaurant/models/pos_order.py`
- `addons/pos_restaurant/models/pos_order_line.py`
- `addons/pos_restaurant/models/pos_preset.py`
- `addons/pos_restaurant/models/pos_restaurant.py`
- `addons/pos_restaurant/models/pos_session.py`
- `addons/pos_restaurant/models/product_template.py`
- `addons/pos_restaurant/models/res_config_settings.py`
- `addons/pos_restaurant/models/restaurant_order_course.py`
- `addons/pos_restaurant/receipt/__init__.py`
- `addons/pos_restaurant/receipt/pos_order_change_receipt.xml`
- `addons/pos_restaurant/receipt/pos_order_receipt.py`
- `addons/pos_restaurant/receipt/pos_order_receipt.xml`
- `addons/pos_restaurant/security/ir.access.csv`
- `addons/pos_restaurant/static/description/icon.png`
- `addons/pos_restaurant/static/description/icon.svg`
- `addons/pos_restaurant/static/description/icon_hi.png`
- `addons/pos_restaurant/static/floor_plan/door.svg`
- `addons/pos_restaurant/static/floor_plan/plant.svg`
- `addons/pos_restaurant/static/floor_plan/tile-1.jpg`
- `addons/pos_restaurant/static/floor_plan/tile-1p.png`
- `addons/pos_restaurant/static/floor_plan/tile-2.jpg`
- `addons/pos_restaurant/static/floor_plan/tile-2p.jpg`
- `addons/pos_restaurant/static/floor_plan/tile-3.jpg`
- `addons/pos_restaurant/static/floor_plan/tile-3p.jpg`
- `addons/pos_restaurant/static/floor_plan/toilet.svg`
- `addons/pos_restaurant/static/floor_plan/wood-h.jpg`
- `addons/pos_restaurant/static/floor_plan/wood-hp.png`
- `addons/pos_restaurant/static/floor_plan/wood-v.jpg`
- `addons/pos_restaurant/static/floor_plan/wood-vp.png`
- `addons/pos_restaurant/static/img/combo-hamb.png`
- `addons/pos_restaurant/static/img/drink_category.jpg`
- `addons/pos_restaurant/static/img/floor_main.jpeg`
- `addons/pos_restaurant/static/img/food_category.jpg`
- `addons/pos_restaurant/static/img/plan.svg`
- `addons/pos_restaurant/static/img/product_aperol_spritz.png`
- `addons/pos_restaurant/static/img/product_cosmopolitan.png`
- `addons/pos_restaurant/static/img/product_mai_tai.png`
- `addons/pos_restaurant/static/img/product_margarita.png`
- `addons/pos_restaurant/static/img/product_mojito.png`
- `addons/pos_restaurant/static/img/product_moscow_mule.png`
- `addons/pos_restaurant/static/img/product_negroni.png`
- `addons/pos_restaurant/static/img/product_old_fashioned.png`
- `addons/pos_restaurant/static/img/product_pina_colada.png`
- `addons/pos_restaurant/static/img/product_whiskey_sour.png`
- `addons/pos_restaurant/static/img/soft-drink-icon.png`
- `addons/pos_restaurant/static/img/sushi-combo.png`
- `addons/pos_restaurant/static/img/table.svg`
- `addons/pos_restaurant/static/img/th-burger.png`
- `addons/pos_restaurant/static/img/th-cheeseburger.png`
- `addons/pos_restaurant/static/img/th-club.png`
- `addons/pos_restaurant/static/img/th-coke.png`
- `addons/pos_restaurant/static/img/th-espresso.png`
- `addons/pos_restaurant/static/img/th-fanta.png`
- `addons/pos_restaurant/static/img/th-green_tea.png`
- `addons/pos_restaurant/static/img/th-ice_tea.png`
- `addons/pos_restaurant/static/img/th-maki.png`
- `addons/pos_restaurant/static/img/th-milkshake_banana.png`
- `addons/pos_restaurant/static/img/th-minute_maid.png`
- `addons/pos_restaurant/static/img/th-mozza.png`
- `addons/pos_restaurant/static/img/th-pasta-4f.png`
- `addons/pos_restaurant/static/img/th-pasta.png`
- `addons/pos_restaurant/static/img/th-pizza-fu.png`
- `addons/pos_restaurant/static/img/th-pizza-ma.png`
- `addons/pos_restaurant/static/img/th-pizza-ve.png`
- `addons/pos_restaurant/static/img/th-pizza.png`
- `addons/pos_restaurant/static/img/th-salmon-avocado.png`
- `addons/pos_restaurant/static/img/th-salmon.png`
- `addons/pos_restaurant/static/img/th-sandwich.png`
- `addons/pos_restaurant/static/img/th-schweppes.png`
- `addons/pos_restaurant/static/img/th-temaki.png`
- `addons/pos_restaurant/static/img/th-tuna.png`
- `addons/pos_restaurant/static/img/th-water.png`
- `addons/pos_restaurant/static/src/app/components/navbar/navbar.js`
- `addons/pos_restaurant/static/src/app/components/navbar/navbar.xml`
- `addons/pos_restaurant/static/src/app/components/numpad_dropdown/numpad_dropdown.js`
- `addons/pos_restaurant/static/src/app/components/numpad_dropdown/numpad_dropdown.scss`
- `addons/pos_restaurant/static/src/app/components/numpad_dropdown/numpad_dropdown.xml`
- `addons/pos_restaurant/static/src/app/components/order_course/order_course.js`
- `addons/pos_restaurant/static/src/app/components/order_course/order_course.xml`
- `addons/pos_restaurant/static/src/app/components/order_display/order_display.js`
- `addons/pos_restaurant/static/src/app/components/order_display/order_display.xml`
- `addons/pos_restaurant/static/src/app/components/order_tabs/order_tabs.xml`
- `addons/pos_restaurant/static/src/app/components/orderline/orderline.xml`
- `addons/pos_restaurant/static/src/app/components/popup/edit_order_name_popup/edit_order_name_popup.js`
- `addons/pos_restaurant/static/src/app/components/popup/edit_order_name_popup/edit_order_name_popup.xml`
- `addons/pos_restaurant/static/src/app/hooks/floor_plan_hook.js`
- `addons/pos_restaurant/static/src/app/models/data_service_options.js`
- `addons/pos_restaurant/static/src/app/models/pos_config.js`
- `addons/pos_restaurant/static/src/app/models/pos_order.js`
- `addons/pos_restaurant/static/src/app/models/pos_order_line.js`
- `addons/pos_restaurant/static/src/app/models/restaurant_order_course.js`
- `addons/pos_restaurant/static/src/app/models/restaurant_table.js`
- `addons/pos_restaurant/static/src/app/screens/feedback_screen/feedback_screen.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan/floor_plan.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan/floor_plan.xml`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_base.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/action_menu_hook.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/add_decor_popup/add_decor_popup.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/add_decor_popup/add_decor_popup.xml`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/add_table_popup/add_table_popup.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/add_table_popup/add_table_popup.xml`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/edit_decor/edit_decor.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/edit_decor/edit_decor.xml`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/edit_floor/edit_floor.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/edit_floor/edit_floor.xml`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/edit_table/edit_table.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/edit_table/edit_table.xml`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/floor_plan_editor.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/floor_plan_editor.xml`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/handles/handles.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/handles/handles.xml`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/handles/utils.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/navbar/navbar.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/navbar/navbar.xml`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/operations/index.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/operations/keydown-move.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/operations/line-resize.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/operations/move.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/operations/resize.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/operations/rotation.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/operations/text_edit.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/toolbar/toolbar.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/toolbar/toolbar.xml`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/utils/border_detection.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/utils/image.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/utils/snapping.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_plan_editor/utils/text.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_screen.js`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_screen.scss`
- `addons/pos_restaurant/static/src/app/screens/floor_screen/floor_screen.xml`
- `addons/pos_restaurant/static/src/app/screens/payment_screen/payment_screen.js`
- `addons/pos_restaurant/static/src/app/screens/payment_screen/payment_screen.xml`
- `addons/pos_restaurant/static/src/app/screens/payment_screen/payment_screen_payment_lines/payment_screen_payment_lines.js`
- `addons/pos_restaurant/static/src/app/screens/product_screen/actionpad_widget/actionpad_widget.js`
- `addons/pos_restaurant/static/src/app/screens/product_screen/actionpad_widget/actionpad_widget.scss`
- `addons/pos_restaurant/static/src/app/screens/product_screen/actionpad_widget/actionpad_widget.xml`
- `addons/pos_restaurant/static/src/app/screens/product_screen/control_buttons/control_buttons.js`
- `addons/pos_restaurant/static/src/app/screens/product_screen/control_buttons/control_buttons.xml`
- `addons/pos_restaurant/static/src/app/screens/product_screen/order_summary/order_summary.js`
- `addons/pos_restaurant/static/src/app/screens/product_screen/order_summary/order_summary.scss`
- `addons/pos_restaurant/static/src/app/screens/product_screen/order_summary/order_summary.xml`
- `addons/pos_restaurant/static/src/app/screens/product_screen/product_screen.js`
- `addons/pos_restaurant/static/src/app/screens/product_screen/product_screen.xml`
- `addons/pos_restaurant/static/src/app/screens/split_bill_screen/split_bill_screen.js`
- `addons/pos_restaurant/static/src/app/screens/split_bill_screen/split_bill_screen.xml`
- `addons/pos_restaurant/static/src/app/screens/ticket_screen/order_details_dialog/order_details_dialog.js`
- `addons/pos_restaurant/static/src/app/screens/ticket_screen/order_details_dialog/order_details_dialog.xml`
- `addons/pos_restaurant/static/src/app/screens/ticket_screen/ticket_screen.js`
- `addons/pos_restaurant/static/src/app/screens/ticket_screen/ticket_screen.xml`
- `addons/pos_restaurant/static/src/app/services/floor_plan/elements/border_decor.js`
- `addons/pos_restaurant/static/src/app/services/floor_plan/elements/decor.js`
- `addons/pos_restaurant/static/src/app/services/floor_plan/elements/floor.js`
- `addons/pos_restaurant/static/src/app/services/floor_plan/elements/floor_element.js`
- `addons/pos_restaurant/static/src/app/services/floor_plan/elements/image.js`
- `addons/pos_restaurant/static/src/app/services/floor_plan/elements/index.js`
- `addons/pos_restaurant/static/src/app/services/floor_plan/elements/line.js`
- `addons/pos_restaurant/static/src/app/services/floor_plan/elements/table.js`
- `addons/pos_restaurant/static/src/app/services/floor_plan/elements/text.js`
- `addons/pos_restaurant/static/src/app/services/floor_plan/floor_plan_service.js`
- `addons/pos_restaurant/static/src/app/services/floor_plan/utils/bounds_calculator.js`
- `addons/pos_restaurant/static/src/app/services/floor_plan/utils/colors.js`
- `addons/pos_restaurant/static/src/app/services/floor_plan/utils/floor_texture.js`
- `addons/pos_restaurant/static/src/app/services/floor_plan/utils/history.js`
- `addons/pos_restaurant/static/src/app/services/floor_plan/utils/utils.js`
- `addons/pos_restaurant/static/src/app/services/pos_store.js`
- `addons/pos_restaurant/static/src/app/utils/devices_synchronisation.js`
- `addons/pos_restaurant/static/src/app/utils/order_payment_validation.js`
- `addons/pos_restaurant/static/src/app/utils/printer/generate_printer_data.js`
- `addons/pos_restaurant/static/src/scss/restaurant.scss`
- `addons/pos_restaurant/static/src/xml/Screens/SplitBillScreen/SplitBillScreen.scss`
- `addons/pos_restaurant/static/tests/tours/devices_synchronization_tour.js`
- `addons/pos_restaurant/static/tests/tours/fake_tours.js`
- `addons/pos_restaurant/static/tests/tours/floor_screen_tour.js`
- `addons/pos_restaurant/static/tests/tours/pos_restaurant_tour.js`
- `addons/pos_restaurant/static/tests/tours/service_fee_tour.js`
- `addons/pos_restaurant/static/tests/tours/split_bill_screen_tour.js`
- Additional source files not expanded in this page: 47; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
