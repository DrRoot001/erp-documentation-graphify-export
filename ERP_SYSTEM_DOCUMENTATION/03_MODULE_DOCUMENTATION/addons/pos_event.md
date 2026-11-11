# Module: pos_event

- **Module ID:** MOD-430
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_event`
- **Manifest:** `addons/pos_event/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Technical`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Link module between Point of Sale and Event

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 113 files, including 16 Python, 12 XML, and 34 JavaScript/TypeScript files. The manifest declares dependencies: `point_of_sale`, `event_product`.

## 2. Module structure

- Model/business logic files: 11
- Controller/API files: 0
- XML/data/view/template files: 12
- Browser asset files: 34
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/pos_event/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 11 model declarations, 49 methods, 0 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/pos_event/models/event_question_answer.py:6`, `addons/pos_event/models/event_ticket.py:5`, `addons/pos_event/models/event_registration_answer.py:6`, `addons/pos_event/models/pos_config.py:5`, `addons/pos_event/models/event_slot.py:5`, `addons/pos_event/models/pos_session.py:5`, `addons/pos_event/models/pos_order.py:5`, `addons/pos_event/models/event_question.py:6`, `addons/pos_event/models/event_event.py:4`, `addons/pos_event/models/event_registration.py:7`, `addons/pos_event/models/pos_order_line.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 12 XML files and 34 JavaScript/TypeScript files; static XML analysis found 8 record/template/menu identifiers.
- **Evidence:** `addons/pos_event/data/event_product_data.xml:4`, `addons/pos_event/data/point_of_sale_demo.xml:4`, `addons/pos_event/data/event_product_demo.xml:4`, `addons/pos_event/data/event_product_demo.xml:8`, `addons/pos_event/data/point_of_sale_data.xml:4`, `addons/pos_event/views/pos_order_views.xml:3`, `addons/pos_event/views/event_registration_views.xml:3`, `addons/pos_event/views/event_event_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/pos_event/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/pos_event/tests/test_frontend.py`, `addons/pos_event/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 12; representative identifiers: `event_product.product_product_event`, `point_of_sale.pos_config_main`, `event_product.product_product_event_standard`, `event_product.product_product_event_vip`, `pos_category_event`, `pos_order_form_view_inherit`, `event_registration_ticket_view_form`, `event_event_view_form_inherit_pos_event`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/pos_event/views/pos_order_views.xml:5`, `addons/pos_event/views/pos_order_views.xml:7`, `addons/pos_event/views/event_registration_views.xml:5`, `addons/pos_event/views/event_registration_views.xml:7`, `addons/pos_event/views/event_event_views.xml:5`, `addons/pos_event/views/event_event_views.xml:7`
- Browser assets: 34; representative files: `addons/pos_event/static/src/app/services/pos_store.js`, `addons/pos_event/static/src/app/models/data_service_options.js`, `addons/pos_event/static/src/app/models/pos_order_line.js`, `addons/pos_event/static/src/app/models/product_template.js`, `addons/pos_event/static/src/app/models/pos_order.js`, `addons/pos_event/static/src/app/utils/event_util.js`, `addons/pos_event/static/src/app/screens/product_screen/product_screen.js`, `addons/pos_event/static/src/app/screens/product_screen/order_summary/order_summary.js`, `addons/pos_event/static/src/app/components/product_card/product_card.js`, `addons/pos_event/static/src/app/components/popup/event_registration_popup/event_registration_popup.js`, `addons/pos_event/static/src/app/components/popup/event_slot_selection_popup/event_slot_selection_popup.js`, `addons/pos_event/static/src/app/components/popup/event_configurator_popup/event_configurator_popup.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_event/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 11
- Representative model evidence: `event.question.answer` (addons/pos_event/models/event_question_answer.py:6); `event.event.ticket` (addons/pos_event/models/event_ticket.py:5); `event.registration.answer` (addons/pos_event/models/event_registration_answer.py:6); inherits `pos.config` (addons/pos_event/models/pos_config.py:5); `event.slot` (addons/pos_event/models/event_slot.py:5); inherits `pos.session` (addons/pos_event/models/pos_session.py:5); inherits `pos.order` (addons/pos_event/models/pos_order.py:5); `event.question` (addons/pos_event/models/event_question.py:6); `event.event` (addons/pos_event/models/event_event.py:4); `event.registration` (addons/pos_event/models/event_registration.py:7); inherits `pos.order.line` (addons/pos_event/models/pos_order_line.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `point_of_sale`, `event_product`
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

- `addons/pos_event/__init__.py`
- `addons/pos_event/__manifest__.py`
- `addons/pos_event/data/event_product_data.xml`
- `addons/pos_event/data/event_product_demo.xml`
- `addons/pos_event/data/point_of_sale_data.xml`
- `addons/pos_event/data/point_of_sale_demo.xml`
- `addons/pos_event/i18n/ar.po`
- `addons/pos_event/i18n/az.po`
- `addons/pos_event/i18n/bg.po`
- `addons/pos_event/i18n/bs.po`
- `addons/pos_event/i18n/ca.po`
- `addons/pos_event/i18n/cs.po`
- `addons/pos_event/i18n/da.po`
- `addons/pos_event/i18n/de.po`
- `addons/pos_event/i18n/el.po`
- `addons/pos_event/i18n/es.po`
- `addons/pos_event/i18n/es_419.po`
- `addons/pos_event/i18n/et.po`
- `addons/pos_event/i18n/fa.po`
- `addons/pos_event/i18n/fi.po`
- `addons/pos_event/i18n/fr.po`
- `addons/pos_event/i18n/he.po`
- `addons/pos_event/i18n/hi.po`
- `addons/pos_event/i18n/hr.po`
- `addons/pos_event/i18n/hu.po`
- `addons/pos_event/i18n/id.po`
- `addons/pos_event/i18n/it.po`
- `addons/pos_event/i18n/ja.po`
- `addons/pos_event/i18n/kab.po`
- `addons/pos_event/i18n/ko.po`
- `addons/pos_event/i18n/ku.po`
- `addons/pos_event/i18n/lo.po`
- `addons/pos_event/i18n/lt.po`
- `addons/pos_event/i18n/lv.po`
- `addons/pos_event/i18n/mn.po`
- `addons/pos_event/i18n/my.po`
- `addons/pos_event/i18n/nb.po`
- `addons/pos_event/i18n/nl.po`
- `addons/pos_event/i18n/pl.po`
- `addons/pos_event/i18n/pos_event.pot`
- `addons/pos_event/i18n/pt.po`
- `addons/pos_event/i18n/pt_BR.po`
- `addons/pos_event/i18n/ro.po`
- `addons/pos_event/i18n/ru.po`
- `addons/pos_event/i18n/sk.po`
- `addons/pos_event/i18n/sl.po`
- `addons/pos_event/i18n/sr@latin.po`
- `addons/pos_event/i18n/sv.po`
- `addons/pos_event/i18n/th.po`
- `addons/pos_event/i18n/tr.po`
- `addons/pos_event/i18n/uk.po`
- `addons/pos_event/i18n/uz.po`
- `addons/pos_event/i18n/vi.po`
- `addons/pos_event/i18n/zh_CN.po`
- `addons/pos_event/i18n/zh_TW.po`
- `addons/pos_event/models/__init__.py`
- `addons/pos_event/models/event_event.py`
- `addons/pos_event/models/event_question.py`
- `addons/pos_event/models/event_question_answer.py`
- `addons/pos_event/models/event_registration.py`
- `addons/pos_event/models/event_registration_answer.py`
- `addons/pos_event/models/event_slot.py`
- `addons/pos_event/models/event_ticket.py`
- `addons/pos_event/models/pos_config.py`
- `addons/pos_event/models/pos_order.py`
- `addons/pos_event/models/pos_order_line.py`
- `addons/pos_event/models/pos_session.py`
- `addons/pos_event/security/ir.access.csv`
- `addons/pos_event/static/img/event_category.png`
- `addons/pos_event/static/src/app/components/popup/event_configurator_popup/event_configurator_popup.js`
- `addons/pos_event/static/src/app/components/popup/event_configurator_popup/event_configurator_popup.xml`
- `addons/pos_event/static/src/app/components/popup/event_registration_popup/event_registration_popup.js`
- `addons/pos_event/static/src/app/components/popup/event_registration_popup/event_registration_popup.xml`
- `addons/pos_event/static/src/app/components/popup/event_slot_selection_popup/event_slot_selection_popup.js`
- `addons/pos_event/static/src/app/components/popup/event_slot_selection_popup/event_slot_selection_popup.xml`
- `addons/pos_event/static/src/app/components/popup/print_popup/print_popup.js`
- `addons/pos_event/static/src/app/components/product_card/product_card.js`
- `addons/pos_event/static/src/app/components/product_card/product_card.xml`
- `addons/pos_event/static/src/app/models/data_service_options.js`
- `addons/pos_event/static/src/app/models/pos_order.js`
- `addons/pos_event/static/src/app/models/pos_order_line.js`
- `addons/pos_event/static/src/app/models/product_template.js`
- `addons/pos_event/static/src/app/screens/product_screen/order_summary/order_summary.js`
- `addons/pos_event/static/src/app/screens/product_screen/order_summary/order_summary.xml`
- `addons/pos_event/static/src/app/screens/product_screen/product_screen.js`
- `addons/pos_event/static/src/app/services/pos_store.js`
- `addons/pos_event/static/src/app/utils/event_util.js`
- `addons/pos_event/static/tests/tours/pos_event_tour.js`
- `addons/pos_event/static/tests/tours/pos_multi_slot_event_tour.js`
- `addons/pos_event/static/tests/tours/utils/event_tour_utils.js`
- `addons/pos_event/static/tests/tours/utils/slot_selection_screen_utils.js`
- `addons/pos_event/static/tests/unit/components/event_configurator_popup.test.js`
- `addons/pos_event/static/tests/unit/components/event_registration_popup.test.js`
- `addons/pos_event/static/tests/unit/components/event_slot_selection_popup.test.js`
- `addons/pos_event/static/tests/unit/components/product_card.test.js`
- `addons/pos_event/static/tests/unit/data/event_event.data.js`
- `addons/pos_event/static/tests/unit/data/event_event_ticket.data.js`
- `addons/pos_event/static/tests/unit/data/event_question.data.js`
- `addons/pos_event/static/tests/unit/data/event_question_answer.data.js`
- `addons/pos_event/static/tests/unit/data/event_registration.data.js`
- `addons/pos_event/static/tests/unit/data/event_registration_answer.data.js`
- `addons/pos_event/static/tests/unit/data/event_slot.data.js`
- `addons/pos_event/static/tests/unit/data/pos_order_line.data.js`
- `addons/pos_event/static/tests/unit/data/pos_session.data.js`
- `addons/pos_event/static/tests/unit/data/product_product.data.js`
- `addons/pos_event/static/tests/unit/data/product_template.data.js`
- `addons/pos_event/static/tests/unit/data_service_options.test.js`
- `addons/pos_event/static/tests/unit/services/pos_store.test.js`
- `addons/pos_event/tests/__init__.py`
- `addons/pos_event/tests/test_frontend.py`
- `addons/pos_event/views/event_event_views.xml`
- `addons/pos_event/views/event_registration_views.xml`
- `addons/pos_event/views/pos_order_views.xml`
