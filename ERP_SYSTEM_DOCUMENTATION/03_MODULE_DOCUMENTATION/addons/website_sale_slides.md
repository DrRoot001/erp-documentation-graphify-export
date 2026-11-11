# Module: website_sale_slides

- **Module ID:** MOD-641
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_sale_slides`
- **Manifest:** `addons/website_sale_slides/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/eLearning`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Sell your courses online

**Manifest description:**

Sell your courses using the e-commerce features of the website.

**Scope evidence:** The module contains 88 files, including 14 Python, 14 XML, and 5 JavaScript/TypeScript files. The manifest declares dependencies: `website_slides`, `website_sale`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 3
- XML/data/view/template files: 14
- Browser asset files: 5
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 25 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/website_sale_slides/models/sale_order.py:6`, `addons/website_sale_slides/models/product_product.py:7`, `addons/website_sale_slides/models/slide_channel.py:7`, `addons/website_sale_slides/models/product_template.py:7`, `addons/website_sale_slides/models/sale_order_line.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 1 route declarations.
- **Evidence:** `addons/website_sale_slides/controllers/slides.py:11`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 14 XML files and 5 JavaScript/TypeScript files; static XML analysis found 38 record/template/menu identifiers.
- **Evidence:** `addons/website_sale_slides/report/sale_report_views.xml:3`, `addons/website_sale_slides/report/sale_report_views.xml:14`, `addons/website_sale_slides/data/slide_demo.xml:5`, `addons/website_sale_slides/data/slide_demo.xml:12`, `addons/website_sale_slides/data/slide_demo.xml:19`, `addons/website_sale_slides/data/product_data.xml:2`, `addons/website_sale_slides/data/sale_order_demo.xml:7`, `addons/website_sale_slides/data/sale_order_demo.xml:18`, `addons/website_sale_slides/data/sale_order_demo.xml:24`, `addons/website_sale_slides/data/sale_order_demo.xml:34`, `addons/website_sale_slides/data/sale_order_demo.xml:39`, `addons/website_sale_slides/data/sale_order_demo.xml:48`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/website_sale_slides/tests/test_course_purchase_flow.py`, `addons/website_sale_slides/tests/__init__.py`, `addons/website_sale_slides/tests/test_ui_website_sale_slides.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 14; representative identifiers: `sale_report_view_graph_slides`, `sale_report_action_slides`, `website_slides.slide_channel_demo_1_gard1`, `website_slides.slide_channel_demo_5_furn2`, `website_slides.slide_channel_demo_6_furn3`, `default_product_course`, `sale_order_course_1`, `sale_order_course_1_line_1`, `sale_order_course_2`, `sale_order_course_2_line_1`, `sale_order_course_2_line_2`, `sale_order_course_3`, `sale_order_course_3_line_1`, `website_sale_slides_activity_1`, `website_sale_slides_activity_2`, `product_course_channel_1`, `product_course_channel_5`, `product_course_channel_6`, `lesson_content_quiz`, `slide_aside_training_category_buy_course`
- Menus: 1; representative evidence: `addons/website_sale_slides/views/website_slides_menu_views.xml:3`
- Templates: 14; representative evidence: `addons/website_sale_slides/views/website_slides_templates.xml:5`, `addons/website_sale_slides/views/website_slides_templates.xml:16`, `addons/website_sale_slides/views/website_slides_templates.xml:25`, `addons/website_sale_slides/views/website_slides_templates.xml:39`, `addons/website_sale_slides/views/website_slides_templates.xml:53`, `addons/website_sale_slides/views/website_slides_templates.xml:64`, `addons/website_sale_slides/views/website_slides_templates.xml:74`, `addons/website_sale_slides/views/website_slides_templates.xml:86`, `addons/website_sale_slides/views/website_slides_templates.xml:96`, `addons/website_sale_slides/views/website_slides_templates.xml:113`, `addons/website_sale_slides/views/website_slides_templates.xml:179`, `addons/website_sale_slides/views/website_sale_templates.xml:4`
- View/action field declarations: 14; representative evidence: `addons/website_sale_slides/report/sale_report_views.xml:5`, `addons/website_sale_slides/report/sale_report_views.xml:6`, `addons/website_sale_slides/report/sale_report_views.xml:16`, `addons/website_sale_slides/report/sale_report_views.xml:17`, `addons/website_sale_slides/views/product_template_views.xml:5`, `addons/website_sale_slides/views/product_template_views.xml:7`, `addons/website_sale_slides/views/slide_channel_views.xml:5`, `addons/website_sale_slides/views/slide_channel_views.xml:7`, `addons/website_sale_slides/views/slide_channel_views.xml:37`, `addons/website_sale_slides/views/slide_channel_views.xml:39`, `addons/website_sale_slides/views/slide_channel_views.xml:48`, `addons/website_sale_slides/views/slide_channel_views.xml:50`
- Browser assets: 5; representative files: `addons/website_sale_slides/static/src/interactions/slides_course_fullscreen.js`, `addons/website_sale_slides/static/src/interactions/slides_course_join.js`, `addons/website_sale_slides/static/src/interactions/slides_course_quiz_edit.js`, `addons/website_sale_slides/static/tests/tours/slides_course_member_invited_logged.js`, `addons/website_sale_slides/static/tests/tours/slides_course_member_invited_public.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_sale_slides/__manifest__.py`
- **HTTP entry points:** `addons/website_sale_slides/controllers/slides.py:11`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `sale.order` (addons/website_sale_slides/models/sale_order.py:6); inherits `product.product` (addons/website_sale_slides/models/product_product.py:7); inherits `slide.channel` (addons/website_sale_slides/models/slide_channel.py:7); inherits `product.template` (addons/website_sale_slides/models/product_template.py:7); inherits `sale.order.line` (addons/website_sale_slides/models/sale_order_line.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 1
- Route evidence: `addons/website_sale_slides/controllers/slides.py:11`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_slides`, `website_sale`
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

- `addons/website_sale_slides/__init__.py`
- `addons/website_sale_slides/__manifest__.py`
- `addons/website_sale_slides/controllers/__init__.py`
- `addons/website_sale_slides/controllers/sale.py`
- `addons/website_sale_slides/controllers/slides.py`
- `addons/website_sale_slides/data/product_data.xml`
- `addons/website_sale_slides/data/product_demo.xml`
- `addons/website_sale_slides/data/sale_order_demo.xml`
- `addons/website_sale_slides/data/slide_demo.xml`
- `addons/website_sale_slides/i18n/ar.po`
- `addons/website_sale_slides/i18n/az.po`
- `addons/website_sale_slides/i18n/bg.po`
- `addons/website_sale_slides/i18n/bs.po`
- `addons/website_sale_slides/i18n/ca.po`
- `addons/website_sale_slides/i18n/cs.po`
- `addons/website_sale_slides/i18n/da.po`
- `addons/website_sale_slides/i18n/de.po`
- `addons/website_sale_slides/i18n/el.po`
- `addons/website_sale_slides/i18n/es.po`
- `addons/website_sale_slides/i18n/es_419.po`
- `addons/website_sale_slides/i18n/et.po`
- `addons/website_sale_slides/i18n/fa.po`
- `addons/website_sale_slides/i18n/fi.po`
- `addons/website_sale_slides/i18n/fr.po`
- `addons/website_sale_slides/i18n/he.po`
- `addons/website_sale_slides/i18n/hi.po`
- `addons/website_sale_slides/i18n/hr.po`
- `addons/website_sale_slides/i18n/hu.po`
- `addons/website_sale_slides/i18n/id.po`
- `addons/website_sale_slides/i18n/it.po`
- `addons/website_sale_slides/i18n/ja.po`
- `addons/website_sale_slides/i18n/kab.po`
- `addons/website_sale_slides/i18n/ko.po`
- `addons/website_sale_slides/i18n/ku.po`
- `addons/website_sale_slides/i18n/lo.po`
- `addons/website_sale_slides/i18n/lt.po`
- `addons/website_sale_slides/i18n/lv.po`
- `addons/website_sale_slides/i18n/mn.po`
- `addons/website_sale_slides/i18n/my.po`
- `addons/website_sale_slides/i18n/nb.po`
- `addons/website_sale_slides/i18n/nl.po`
- `addons/website_sale_slides/i18n/pl.po`
- `addons/website_sale_slides/i18n/pt.po`
- `addons/website_sale_slides/i18n/pt_BR.po`
- `addons/website_sale_slides/i18n/ro.po`
- `addons/website_sale_slides/i18n/ru.po`
- `addons/website_sale_slides/i18n/sk.po`
- `addons/website_sale_slides/i18n/sl.po`
- `addons/website_sale_slides/i18n/sr@latin.po`
- `addons/website_sale_slides/i18n/sv.po`
- `addons/website_sale_slides/i18n/th.po`
- `addons/website_sale_slides/i18n/tr.po`
- `addons/website_sale_slides/i18n/uk.po`
- `addons/website_sale_slides/i18n/uz.po`
- `addons/website_sale_slides/i18n/vi.po`
- `addons/website_sale_slides/i18n/website_sale_slides.pot`
- `addons/website_sale_slides/i18n/zh_CN.po`
- `addons/website_sale_slides/i18n/zh_TW.po`
- `addons/website_sale_slides/models/__init__.py`
- `addons/website_sale_slides/models/product_product.py`
- `addons/website_sale_slides/models/product_template.py`
- `addons/website_sale_slides/models/sale_order.py`
- `addons/website_sale_slides/models/sale_order_line.py`
- `addons/website_sale_slides/models/slide_channel.py`
- `addons/website_sale_slides/report/sale_report_views.xml`
- `addons/website_sale_slides/static/img/channel_demo_furniture_2.jpg`
- `addons/website_sale_slides/static/img/channel_demo_tree_1.jpg`
- `addons/website_sale_slides/static/img/default_course_product.jpg`
- `addons/website_sale_slides/static/img/flower_pot.jpg`
- `addons/website_sale_slides/static/img/product_course.jpg`
- `addons/website_sale_slides/static/img/water_can.jpg`
- `addons/website_sale_slides/static/src/interactions/slides_course_fullscreen.js`
- `addons/website_sale_slides/static/src/interactions/slides_course_join.js`
- `addons/website_sale_slides/static/src/interactions/slides_course_quiz_edit.js`
- `addons/website_sale_slides/static/src/website_builder/course_page_option.xml`
- `addons/website_sale_slides/static/src/xml/slide_course_join.xml`
- `addons/website_sale_slides/static/src/xml/website_sale_slides_quiz.xml`
- `addons/website_sale_slides/static/src/xml/website_slides_unsubscribe.xml`
- `addons/website_sale_slides/static/tests/tours/slides_course_member_invited_logged.js`
- `addons/website_sale_slides/static/tests/tours/slides_course_member_invited_public.js`
- `addons/website_sale_slides/tests/__init__.py`
- `addons/website_sale_slides/tests/test_course_purchase_flow.py`
- `addons/website_sale_slides/tests/test_ui_website_sale_slides.py`
- `addons/website_sale_slides/views/product_template_views.xml`
- `addons/website_sale_slides/views/slide_channel_views.xml`
- `addons/website_sale_slides/views/website_sale_templates.xml`
- `addons/website_sale_slides/views/website_slides_menu_views.xml`
- `addons/website_sale_slides/views/website_slides_templates.xml`
