# Module: event_sale

- **Module ID:** MOD-070
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/event_sale`
- **Manifest:** `addons/event_sale/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Events`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Creating registration with sales orders.
========================================

This module allows you to automate and connect your registration creation with
your main sale flow and therefore, to enable the invoicing feature of registrations.

It defines a new kind of service products that offers you the possibility to
choose an event category associated with it. When you encode a sales order for
that product, you will be able to choose an existing event of that category and
when you confirm your sales order it will automatically create a registration for
this event.

**Scope evidence:** The module contains 104 files, including 22 Python, 13 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `event_product`, `sale_management`.

## 2. Module structure

- Model/business logic files: 10
- Controller/API files: 2
- XML/data/view/template files: 13
- Browser asset files: 3
- Security files: 2
- Test files: 6
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/event_sale/security/ir.access.csv`, `addons/event_sale/security/event_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 10 model declarations, 71 methods, 2 constraint handlers, 1 onchange handlers, and 14 dependency declarations.
- **Evidence:** `addons/event_sale/models/sale_order.py:8`, `addons/event_sale/models/event_ticket.py:4`, `addons/event_sale/models/product_template.py:4`, `addons/event_sale/models/event_event.py:7`, `addons/event_sale/models/event_registration.py:8`, `addons/event_sale/models/sale_order_line.py:7`, `addons/event_sale/report/event_sale_report.py:8`, `addons/event_sale/wizard/event_edit_registration.py:9`, `addons/event_sale/wizard/event_edit_registration.py:74`, `addons/event_sale/wizard/event_configurator.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/event_sale/controllers/portal.py`, `addons/event_sale/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 13 XML files and 3 JavaScript/TypeScript files; static XML analysis found 56 record/template/menu identifiers.
- **Evidence:** `addons/event_sale/security/event_security.xml:4`, `addons/event_sale/report/event_sale_report_views.xml:3`, `addons/event_sale/report/event_sale_report_views.xml:15`, `addons/event_sale/report/event_sale_report_views.xml:53`, `addons/event_sale/report/event_sale_report_views.xml:67`, `addons/event_sale/report/event_sale_report_views.xml:90`, `addons/event_sale/report/event_sale_report_views.xml:131`, `addons/event_sale/report/event_sale_report_views.xml:149`, `addons/event_sale/wizard/event_edit_registration.xml:4`, `addons/event_sale/wizard/event_edit_registration.xml:33`, `addons/event_sale/wizard/event_configurator_views.xml:3`, `addons/event_sale/wizard/event_configurator_views.xml:56`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/event_sale/security/ir.access.csv`, `addons/event_sale/security/event_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 6 test files are present.
- **Evidence:** `addons/event_sale/tests/common.py`, `addons/event_sale/tests/test_event_specific.py`, `addons/event_sale/tests/test_event_sale_ui.py`, `addons/event_sale/tests/test_event_internals.py`, `addons/event_sale/tests/test_event_sale.py`, `addons/event_sale/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 13; representative identifiers: `sales_team.group_sale_salesman`, `event_sale_report_view_graph`, `event_sale_report_view_form`, `event_sale_report_view_pivot`, `event_sale_report_view_tree`, `event_sale_report_view_search`, `event_sale_report_action`, `menu_action_show_revenues`, `view_event_registration_editor_form`, `action_sale_order_event_registration`, `event_configurator_view_form`, `event_configurator_action`, `event_product.product_product_event`, `event_product.product_product_event_standard`, `event_product.product_product_event_vip`, `event_0_sale_order_0`, `event_0_sale_order_0_line_0`, `event_0_sale_order_0_line_1`, `event_2_sale_order_0`, `event_2_sale_order_0_line_0`
- Menus: 1; representative evidence: `addons/event_sale/report/event_sale_report_views.xml:149`
- Templates: 1; representative evidence: `addons/event_sale/data/mail_templates.xml:4`
- View/action field declarations: 30; representative evidence: `addons/event_sale/report/event_sale_report_views.xml:5`, `addons/event_sale/report/event_sale_report_views.xml:6`, `addons/event_sale/report/event_sale_report_views.xml:17`, `addons/event_sale/report/event_sale_report_views.xml:18`, `addons/event_sale/report/event_sale_report_views.xml:55`, `addons/event_sale/report/event_sale_report_views.xml:56`, `addons/event_sale/report/event_sale_report_views.xml:69`, `addons/event_sale/report/event_sale_report_views.xml:70`, `addons/event_sale/report/event_sale_report_views.xml:92`, `addons/event_sale/report/event_sale_report_views.xml:93`, `addons/event_sale/report/event_sale_report_views.xml:133`, `addons/event_sale/report/event_sale_report_views.xml:134`
- Browser assets: 3; representative files: `addons/event_sale/static/src/js/sale_product_mixin.js`, `addons/event_sale/static/src/js/event_configurator_controller.js`, `addons/event_sale/static/tests/tours/event_configurator_ui.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/event_sale/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 10
- Representative model evidence: inherits `sale.order` (addons/event_sale/models/sale_order.py:8); inherits `event.event.ticket` (addons/event_sale/models/event_ticket.py:4); inherits `product.template` (addons/event_sale/models/product_template.py:4); inherits `event.event` (addons/event_sale/models/event_event.py:7); inherits `event.registration` (addons/event_sale/models/event_registration.py:8); inherits `sale.order.line` (addons/event_sale/models/sale_order_line.py:7); `event.sale.report` (addons/event_sale/report/event_sale_report.py:8); `registration.editor` (addons/event_sale/wizard/event_edit_registration.py:9); `registration.editor.line` (addons/event_sale/wizard/event_edit_registration.py:74); `event.event.configurator` (addons/event_sale/wizard/event_configurator.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `event_product`, `sale_management`
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

- `addons/event_sale/__init__.py`
- `addons/event_sale/__manifest__.py`
- `addons/event_sale/controllers/__init__.py`
- `addons/event_sale/controllers/portal.py`
- `addons/event_sale/data/event_registration_demo.xml`
- `addons/event_sale/data/event_sale_data.xml`
- `addons/event_sale/data/event_sale_demo.xml`
- `addons/event_sale/data/mail_templates.xml`
- `addons/event_sale/i18n/af.po`
- `addons/event_sale/i18n/am.po`
- `addons/event_sale/i18n/ar.po`
- `addons/event_sale/i18n/az.po`
- `addons/event_sale/i18n/bg.po`
- `addons/event_sale/i18n/bs.po`
- `addons/event_sale/i18n/ca.po`
- `addons/event_sale/i18n/cs.po`
- `addons/event_sale/i18n/da.po`
- `addons/event_sale/i18n/de.po`
- `addons/event_sale/i18n/el.po`
- `addons/event_sale/i18n/es.po`
- `addons/event_sale/i18n/es_419.po`
- `addons/event_sale/i18n/es_CL.po`
- `addons/event_sale/i18n/et.po`
- `addons/event_sale/i18n/eu.po`
- `addons/event_sale/i18n/event_sale.pot`
- `addons/event_sale/i18n/fa.po`
- `addons/event_sale/i18n/fi.po`
- `addons/event_sale/i18n/fo.po`
- `addons/event_sale/i18n/fr.po`
- `addons/event_sale/i18n/fr_BE.po`
- `addons/event_sale/i18n/fr_CA.po`
- `addons/event_sale/i18n/gl.po`
- `addons/event_sale/i18n/gu.po`
- `addons/event_sale/i18n/he.po`
- `addons/event_sale/i18n/hi.po`
- `addons/event_sale/i18n/hr.po`
- `addons/event_sale/i18n/hu.po`
- `addons/event_sale/i18n/id.po`
- `addons/event_sale/i18n/is.po`
- `addons/event_sale/i18n/it.po`
- `addons/event_sale/i18n/ja.po`
- `addons/event_sale/i18n/ka.po`
- `addons/event_sale/i18n/kab.po`
- `addons/event_sale/i18n/km.po`
- `addons/event_sale/i18n/ko.po`
- `addons/event_sale/i18n/ku.po`
- `addons/event_sale/i18n/lo.po`
- `addons/event_sale/i18n/lt.po`
- `addons/event_sale/i18n/lv.po`
- `addons/event_sale/i18n/mk.po`
- `addons/event_sale/i18n/mn.po`
- `addons/event_sale/i18n/my.po`
- `addons/event_sale/i18n/nb.po`
- `addons/event_sale/i18n/nl.po`
- `addons/event_sale/i18n/pl.po`
- `addons/event_sale/i18n/pt.po`
- `addons/event_sale/i18n/pt_BR.po`
- `addons/event_sale/i18n/ro.po`
- `addons/event_sale/i18n/ru.po`
- `addons/event_sale/i18n/sk.po`
- `addons/event_sale/i18n/sl.po`
- `addons/event_sale/i18n/sq.po`
- `addons/event_sale/i18n/sr@latin.po`
- `addons/event_sale/i18n/sv.po`
- `addons/event_sale/i18n/ta.po`
- `addons/event_sale/i18n/th.po`
- `addons/event_sale/i18n/tr.po`
- `addons/event_sale/i18n/uk.po`
- `addons/event_sale/i18n/uz.po`
- `addons/event_sale/i18n/vi.po`
- `addons/event_sale/i18n/zh_CN.po`
- `addons/event_sale/i18n/zh_TW.po`
- `addons/event_sale/models/__init__.py`
- `addons/event_sale/models/event_event.py`
- `addons/event_sale/models/event_registration.py`
- `addons/event_sale/models/event_ticket.py`
- `addons/event_sale/models/product_template.py`
- `addons/event_sale/models/sale_order.py`
- `addons/event_sale/models/sale_order_line.py`
- `addons/event_sale/report/__init__.py`
- `addons/event_sale/report/event_sale_report.py`
- `addons/event_sale/report/event_sale_report_views.xml`
- `addons/event_sale/security/event_security.xml`
- `addons/event_sale/security/ir.access.csv`
- `addons/event_sale/static/img/event_product-image.jpg`
- `addons/event_sale/static/src/client_action/event_registration_summary_dialog.xml`
- `addons/event_sale/static/src/js/event_configurator_controller.js`
- `addons/event_sale/static/src/js/sale_product_mixin.js`
- `addons/event_sale/static/tests/tours/event_configurator_ui.js`
- `addons/event_sale/tests/__init__.py`
- `addons/event_sale/tests/common.py`
- `addons/event_sale/tests/test_event_internals.py`
- `addons/event_sale/tests/test_event_sale.py`
- `addons/event_sale/tests/test_event_sale_ui.py`
- `addons/event_sale/tests/test_event_specific.py`
- `addons/event_sale/views/event_registration_views.xml`
- `addons/event_sale/views/event_views.xml`
- `addons/event_sale/views/product_template_views.xml`
- `addons/event_sale/views/sale_order_views.xml`
- `addons/event_sale/wizard/__init__.py`
- `addons/event_sale/wizard/event_configurator.py`
- `addons/event_sale/wizard/event_configurator_views.xml`
- `addons/event_sale/wizard/event_edit_registration.py`
- `addons/event_sale/wizard/event_edit_registration.xml`
