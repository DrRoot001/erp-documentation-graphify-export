# Module: lunch

- **Module ID:** MOD-350
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/lunch`
- **Manifest:** `addons/lunch/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Human Resources/Lunch`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Handle lunch orders of your employees

**Manifest description:**

The base module to manage lunch.
================================

Many companies order sandwiches, pizzas and other, from usual vendors, for their employees to offer them more facilities.

However lunches management within the company requires proper administration especially when the number of employees or vendors is important.

The “Lunch Order” module has been developed to make this management easier but also to offer employees more tools and usability.

In addition to a full meal and vendor management, this module offers the possibility to display warning and provides quick order selection based on employee’s preferences.

If you want to save your employees' time and avoid them to always have coins in their pockets, this module is essential.

**Scope evidence:** The module contains 154 files, including 25 Python, 18 XML, and 10 JavaScript/TypeScript files. The manifest declares dependencies: `mail`.

## 2. Module structure

- Model/business logic files: 13
- Controller/API files: 2
- XML/data/view/template files: 18
- Browser asset files: 10
- Security files: 2
- Test files: 6
- Scheduled/automation evidence files: 5
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/lunch/security/ir.access.csv`, `addons/lunch/security/lunch_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 13 model declarations, 99 methods, 3 constraint handlers, 0 onchange handlers, and 17 dependency declarations.
- **Evidence:** `addons/lunch/models/res_groups.py:6`, `addons/lunch/models/lunch_product_category.py:7`, `addons/lunch/models/lunch_location.py:7`, `addons/lunch/models/res_config_settings.py:7`, `addons/lunch/models/lunch_cashmove.py:8`, `addons/lunch/models/lunch_order.py:9`, `addons/lunch/models/lunch_supplier.py:21`, `addons/lunch/models/lunch_topping.py:9`, `addons/lunch/models/res_users.py:6`, `addons/lunch/models/lunch_alert.py:19`, `addons/lunch/models/res_company.py:7`, `addons/lunch/models/lunch_product.py:10`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 6 route declarations.
- **Evidence:** `addons/lunch/controllers/main.py:11`, `addons/lunch/controllers/main.py:51`, `addons/lunch/controllers/main.py:63`, `addons/lunch/controllers/main.py:78`, `addons/lunch/controllers/main.py:82`, `addons/lunch/controllers/main.py:92`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 18 XML files and 10 JavaScript/TypeScript files; static XML analysis found 143 record/template/menu identifiers.
- **Evidence:** `addons/lunch/security/lunch_security.xml:3`, `addons/lunch/security/lunch_security.xml:8`, `addons/lunch/security/lunch_security.xml:13`, `addons/lunch/security/lunch_security.xml:22`, `addons/lunch/report/lunch_cashmove_report_views.xml:3`, `addons/lunch/report/lunch_cashmove_report_views.xml:18`, `addons/lunch/report/lunch_cashmove_report_views.xml:32`, `addons/lunch/report/lunch_cashmove_report_views.xml:46`, `addons/lunch/report/lunch_cashmove_report_views.xml:59`, `addons/lunch/report/lunch_cashmove_report_views.xml:78`, `addons/lunch/report/lunch_cashmove_report_views.xml:108`, `addons/lunch/report/lunch_cashmove_report_views.xml:125`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/lunch/security/ir.access.csv`, `addons/lunch/security/lunch_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 5 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/lunch/models/lunch_supplier.py`, `addons/lunch/models/lunch_alert.py`, `addons/lunch/data/lunch_data.xml`, `addons/lunch/tests/test_alert.py`, `addons/lunch/tests/test_supplier.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 6 test files are present.
- **Evidence:** `addons/lunch/tests/test_alert.py`, `addons/lunch/tests/test_supplier.py`, `addons/lunch/tests/test_order.py`, `addons/lunch/tests/common.py`, `addons/lunch/tests/test_ui.py`, `addons/lunch/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 18; representative identifiers: `res_groups_privilege_lunch`, `group_lunch_user`, `group_lunch_manager`, `base.default_user_group`, `lunch_cashmove_report_view_search`, `lunch_cashmove_report_view_search_2`, `lunch_cashmove_report_view_tree`, `lunch_cashmove_report_view_tree_2`, `lunch_cashmove_report_view_form`, `view_lunch_cashmove_report_kanban`, `lunch_cashmove_report_action_account`, `lunch_cashmove_report_action_control_accounts`, `lunch_order_mail_supplier`, `lunch_location_main`, `categ_sandwich`, `categ_pizza`, `categ_burger`, `categ_drinks`, `partner_hungry_dog`, `supplier_hungry_dog`
- Menus: 17; representative evidence: `addons/lunch/views/lunch_views.xml:4`, `addons/lunch/views/lunch_views.xml:5`, `addons/lunch/views/lunch_views.xml:6`, `addons/lunch/views/lunch_views.xml:7`, `addons/lunch/views/lunch_views.xml:8`, `addons/lunch/views/lunch_views.xml:10`, `addons/lunch/views/lunch_views.xml:11`, `addons/lunch/views/lunch_views.xml:12`, `addons/lunch/views/lunch_views.xml:13`, `addons/lunch/views/lunch_views.xml:14`, `addons/lunch/views/lunch_views.xml:16`, `addons/lunch/views/lunch_views.xml:17`
- Templates: 1; representative evidence: `addons/lunch/views/lunch_templates.xml:3`
- View/action field declarations: 106; representative evidence: `addons/lunch/report/lunch_cashmove_report_views.xml:5`, `addons/lunch/report/lunch_cashmove_report_views.xml:6`, `addons/lunch/report/lunch_cashmove_report_views.xml:20`, `addons/lunch/report/lunch_cashmove_report_views.xml:21`, `addons/lunch/report/lunch_cashmove_report_views.xml:34`, `addons/lunch/report/lunch_cashmove_report_views.xml:35`, `addons/lunch/report/lunch_cashmove_report_views.xml:48`, `addons/lunch/report/lunch_cashmove_report_views.xml:49`, `addons/lunch/report/lunch_cashmove_report_views.xml:61`, `addons/lunch/report/lunch_cashmove_report_views.xml:62`, `addons/lunch/report/lunch_cashmove_report_views.xml:80`, `addons/lunch/report/lunch_cashmove_report_views.xml:81`
- Browser assets: 10; representative files: `addons/lunch/static/tests/lunch_is_favorite_field.test.js`, `addons/lunch/static/tests/lunch_kanban.test.js`, `addons/lunch/static/src/mixins/lunch_renderer_mixin.js`, `addons/lunch/static/src/components/lunch_dashboard.js`, `addons/lunch/static/src/components/lunch_is_favorite_field.js`, `addons/lunch/static/src/views/kanban.js`, `addons/lunch/static/src/views/list.js`, `addons/lunch/static/src/views/search_model.js`, `addons/lunch/static/src/views/search_panel.js`, `addons/lunch/static/tests/tours/order_lunch.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/lunch/__manifest__.py`
- **HTTP entry points:** `addons/lunch/controllers/main.py:11`, `addons/lunch/controllers/main.py:51`, `addons/lunch/controllers/main.py:63`, `addons/lunch/controllers/main.py:78`, `addons/lunch/controllers/main.py:82`, `addons/lunch/controllers/main.py:92`
- **Scheduled entry points:** `addons/lunch/models/lunch_supplier.py`, `addons/lunch/models/lunch_alert.py`, `addons/lunch/data/lunch_data.xml`, `addons/lunch/tests/test_alert.py`, `addons/lunch/tests/test_supplier.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 13
- Representative model evidence: inherits `res.groups` (addons/lunch/models/res_groups.py:6); `lunch.product.category` (addons/lunch/models/lunch_product_category.py:7); `lunch.location` (addons/lunch/models/lunch_location.py:7); inherits `res.config.settings` (addons/lunch/models/res_config_settings.py:7); `lunch.cashmove` (addons/lunch/models/lunch_cashmove.py:8); `lunch.order` (addons/lunch/models/lunch_order.py:9); `lunch.supplier` (addons/lunch/models/lunch_supplier.py:21); `lunch.topping` (addons/lunch/models/lunch_topping.py:9); inherits `res.users` (addons/lunch/models/res_users.py:6); `lunch.alert` (addons/lunch/models/lunch_alert.py:19); inherits `res.company` (addons/lunch/models/res_company.py:7); `lunch.product` (addons/lunch/models/lunch_product.py:10); `lunch.cashmove.report` (addons/lunch/report/lunch_cashmove_report.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 6
- Route evidence: `addons/lunch/controllers/main.py:11`, `addons/lunch/controllers/main.py:51`, `addons/lunch/controllers/main.py:63`, `addons/lunch/controllers/main.py:78`, `addons/lunch/controllers/main.py:82`, `addons/lunch/controllers/main.py:92`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mail`
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

- `addons/lunch/__init__.py`
- `addons/lunch/__manifest__.py`
- `addons/lunch/controllers/__init__.py`
- `addons/lunch/controllers/main.py`
- `addons/lunch/data/lunch_data.xml`
- `addons/lunch/data/lunch_demo.xml`
- `addons/lunch/data/mail_template_data.xml`
- `addons/lunch/i18n/af.po`
- `addons/lunch/i18n/am.po`
- `addons/lunch/i18n/ar.po`
- `addons/lunch/i18n/az.po`
- `addons/lunch/i18n/bg.po`
- `addons/lunch/i18n/bs.po`
- `addons/lunch/i18n/ca.po`
- `addons/lunch/i18n/cs.po`
- `addons/lunch/i18n/da.po`
- `addons/lunch/i18n/de.po`
- `addons/lunch/i18n/el.po`
- `addons/lunch/i18n/es.po`
- `addons/lunch/i18n/es_419.po`
- `addons/lunch/i18n/es_CL.po`
- `addons/lunch/i18n/et.po`
- `addons/lunch/i18n/eu.po`
- `addons/lunch/i18n/fa.po`
- `addons/lunch/i18n/fi.po`
- `addons/lunch/i18n/fo.po`
- `addons/lunch/i18n/fr.po`
- `addons/lunch/i18n/fr_BE.po`
- `addons/lunch/i18n/fr_CA.po`
- `addons/lunch/i18n/gl.po`
- `addons/lunch/i18n/gu.po`
- `addons/lunch/i18n/he.po`
- `addons/lunch/i18n/hi.po`
- `addons/lunch/i18n/hr.po`
- `addons/lunch/i18n/hu.po`
- `addons/lunch/i18n/id.po`
- `addons/lunch/i18n/is.po`
- `addons/lunch/i18n/it.po`
- `addons/lunch/i18n/ja.po`
- `addons/lunch/i18n/ka.po`
- `addons/lunch/i18n/kab.po`
- `addons/lunch/i18n/km.po`
- `addons/lunch/i18n/ko.po`
- `addons/lunch/i18n/ku.po`
- `addons/lunch/i18n/lb.po`
- `addons/lunch/i18n/lo.po`
- `addons/lunch/i18n/lt.po`
- `addons/lunch/i18n/lunch.pot`
- `addons/lunch/i18n/lv.po`
- `addons/lunch/i18n/mk.po`
- `addons/lunch/i18n/mn.po`
- `addons/lunch/i18n/my.po`
- `addons/lunch/i18n/nb.po`
- `addons/lunch/i18n/nl.po`
- `addons/lunch/i18n/pl.po`
- `addons/lunch/i18n/pt.po`
- `addons/lunch/i18n/pt_BR.po`
- `addons/lunch/i18n/ro.po`
- `addons/lunch/i18n/ru.po`
- `addons/lunch/i18n/sk.po`
- `addons/lunch/i18n/sl.po`
- `addons/lunch/i18n/sq.po`
- `addons/lunch/i18n/sr@latin.po`
- `addons/lunch/i18n/sv.po`
- `addons/lunch/i18n/ta.po`
- `addons/lunch/i18n/th.po`
- `addons/lunch/i18n/tr.po`
- `addons/lunch/i18n/uk.po`
- `addons/lunch/i18n/uz.po`
- `addons/lunch/i18n/vi.po`
- `addons/lunch/i18n/zh_CN.po`
- `addons/lunch/i18n/zh_TW.po`
- `addons/lunch/models/__init__.py`
- `addons/lunch/models/lunch_alert.py`
- `addons/lunch/models/lunch_cashmove.py`
- `addons/lunch/models/lunch_location.py`
- `addons/lunch/models/lunch_order.py`
- `addons/lunch/models/lunch_product.py`
- `addons/lunch/models/lunch_product_category.py`
- `addons/lunch/models/lunch_supplier.py`
- `addons/lunch/models/lunch_topping.py`
- `addons/lunch/models/res_company.py`
- `addons/lunch/models/res_config_settings.py`
- `addons/lunch/models/res_groups.py`
- `addons/lunch/models/res_users.py`
- `addons/lunch/report/__init__.py`
- `addons/lunch/report/lunch_cashmove_report.py`
- `addons/lunch/report/lunch_cashmove_report_views.xml`
- `addons/lunch/security/ir.access.csv`
- `addons/lunch/security/lunch_security.xml`
- `addons/lunch/static/description/icon.png`
- `addons/lunch/static/description/icon.svg`
- `addons/lunch/static/description/icon_hi.png`
- `addons/lunch/static/img/4formaggio.png`
- `addons/lunch/static/img/Coke.png`
- `addons/lunch/static/img/bacon_burger.png`
- `addons/lunch/static/img/brie.png`
- `addons/lunch/static/img/burger.png`
- `addons/lunch/static/img/cheeseburger.png`
- `addons/lunch/static/img/chicken_curry.png`
- `addons/lunch/static/img/chirashi.png`
- `addons/lunch/static/img/club.png`
- `addons/lunch/static/img/coke_zero.png`
- `addons/lunch/static/img/drink.png`
- `addons/lunch/static/img/fanta.png`
- `addons/lunch/static/img/fuze_black.png`
- `addons/lunch/static/img/fuze_green.png`
- `addons/lunch/static/img/gouda.png`
- `addons/lunch/static/img/italiana.png`
- `addons/lunch/static/img/lipton.png`
- `addons/lunch/static/img/lunch.png`
- `addons/lunch/static/img/maki.png`
- `addons/lunch/static/img/mozza.png`
- `addons/lunch/static/img/napoli.png`
- `addons/lunch/static/img/pasta_bolognese.png`
- `addons/lunch/static/img/pizza.jpeg`
- `addons/lunch/static/img/pizza.png`
- `addons/lunch/static/img/pizza_funghi.png`
- `addons/lunch/static/img/pizza_margherita.png`
- `addons/lunch/static/img/pizza_veggie.png`
- `addons/lunch/static/img/salmon_sushi.png`
- `addons/lunch/static/img/temaki.png`
- `addons/lunch/static/img/tuna_sandwich.png`
- `addons/lunch/static/src/components/lunch_dashboard.js`
- `addons/lunch/static/src/components/lunch_dashboard.scss`
- `addons/lunch/static/src/components/lunch_dashboard.xml`
- `addons/lunch/static/src/components/lunch_is_favorite_field.js`
- `addons/lunch/static/src/mixins/lunch_renderer_mixin.js`
- `addons/lunch/static/src/scss/lunch_kanban.scss`
- `addons/lunch/static/src/views/kanban.js`
- `addons/lunch/static/src/views/kanban.xml`
- `addons/lunch/static/src/views/list.js`
- `addons/lunch/static/src/views/list.xml`
- `addons/lunch/static/src/views/no_content_helper.xml`
- `addons/lunch/static/src/views/search_model.js`
- `addons/lunch/static/src/views/search_panel.js`
- `addons/lunch/static/tests/lunch_is_favorite_field.test.js`
- `addons/lunch/static/tests/lunch_kanban.test.js`
- `addons/lunch/static/tests/tours/order_lunch.js`
- `addons/lunch/tests/__init__.py`
- `addons/lunch/tests/common.py`
- `addons/lunch/tests/test_alert.py`
- `addons/lunch/tests/test_order.py`
- `addons/lunch/tests/test_supplier.py`
- `addons/lunch/tests/test_ui.py`
- `addons/lunch/views/lunch_alert_views.xml`
- `addons/lunch/views/lunch_cashmove_views.xml`
- `addons/lunch/views/lunch_location_views.xml`
- `addons/lunch/views/lunch_orders_views.xml`
- `addons/lunch/views/lunch_product_views.xml`
- `addons/lunch/views/lunch_supplier_views.xml`
- `addons/lunch/views/lunch_templates.xml`
- `addons/lunch/views/lunch_views.xml`
- `addons/lunch/views/res_config_settings.xml`
