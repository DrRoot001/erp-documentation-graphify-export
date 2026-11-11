# Module: website_event_sale

- **Module ID:** MOD-613
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_event_sale`
- **Manifest:** `addons/website_event_sale/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Sell event tickets online

**Manifest description:**

Sell event tickets through eCommerce app.

**Scope evidence:** The module contains 95 files, including 21 Python, 5 XML, and 4 JavaScript/TypeScript files. The manifest declares dependencies: `website_event`, `event_sale`, `website_sale`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 3
- XML/data/view/template files: 5
- Browser asset files: 4
- Security files: 0
- Test files: 7
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 41 methods, 0 constraint handlers, 1 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/website_event_sale/models/sale_order.py:7`, `addons/website_event_sale/models/event_ticket.py:4`, `addons/website_event_sale/models/product_pricelist.py:6`, `addons/website_event_sale/models/product.py:7`, `addons/website_event_sale/models/product.py:35`, `addons/website_event_sale/models/event_event.py:6`, `addons/website_event_sale/models/sale_order_line.py:6`, `addons/website_event_sale/report/event_sale_report.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 1 route declarations.
- **Evidence:** `addons/website_event_sale/controllers/main.py:71`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 4 JavaScript/TypeScript files; static XML analysis found 7 record/template/menu identifiers.
- **Evidence:** `addons/website_event_sale/report/event_sale_report_views.xml:4`, `addons/website_event_sale/views/website_sale_templates.xml:5`, `addons/website_event_sale/views/website_sale_templates.xml:15`, `addons/website_event_sale/views/website_sale_templates.xml:21`, `addons/website_event_sale/views/website_event_templates.xml:4`, `addons/website_event_sale/views/website_event_templates.xml:85`, `addons/website_event_sale/views/event_event_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 7 test files are present.
- **Evidence:** `addons/website_event_sale/tests/test_website_event_sale_pricelist.py`, `addons/website_event_sale/tests/test_website_event_sale_cart.py`, `addons/website_event_sale/tests/common.py`, `addons/website_event_sale/tests/test_frontend_buy_tickets.py`, `addons/website_event_sale/tests/test_event_checkout.py`, `addons/website_event_sale/tests/__init__.py`, `addons/website_event_sale/tests/test_website_event_sale.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `event_sale_report_view_search`, `Event Shopping Cart Line Product Link`, `cart_summary_inherit_website_event_sale`, `event_confirmation`, `modal_ticket_registration`, `registration_attendee_details`, `event_form_mandatory_company`
- Menus: 0; representative evidence: Not found in module
- Templates: 5; representative evidence: `addons/website_event_sale/views/website_sale_templates.xml:5`, `addons/website_event_sale/views/website_sale_templates.xml:15`, `addons/website_event_sale/views/website_sale_templates.xml:21`, `addons/website_event_sale/views/website_event_templates.xml:4`, `addons/website_event_sale/views/website_event_templates.xml:85`
- View/action field declarations: 4; representative evidence: `addons/website_event_sale/report/event_sale_report_views.xml:6`, `addons/website_event_sale/report/event_sale_report_views.xml:8`, `addons/website_event_sale/views/event_event_views.xml:5`, `addons/website_event_sale/views/event_event_views.xml:7`
- Browser assets: 4; representative files: `addons/website_event_sale/static/tests/tours/website_event_sale_last_ticket.js`, `addons/website_event_sale/static/tests/tours/website_event_sale_pricelists.js`, `addons/website_event_sale/static/tests/tours/website_event_sale.js`, `addons/website_event_sale/static/tests/tours/helpers/WebsiteEventSaleTourMethods.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_event_sale/__manifest__.py`
- **HTTP entry points:** `addons/website_event_sale/controllers/main.py:71`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: inherits `sale.order` (addons/website_event_sale/models/sale_order.py:7); inherits `event.event.ticket` (addons/website_event_sale/models/event_ticket.py:4); inherits `product.pricelist.item` (addons/website_event_sale/models/product_pricelist.py:6); inherits `product.product` (addons/website_event_sale/models/product.py:7); inherits `product.template` (addons/website_event_sale/models/product.py:35); inherits `event.event` (addons/website_event_sale/models/event_event.py:6); inherits `sale.order.line` (addons/website_event_sale/models/sale_order_line.py:6); inherits `event.sale.report` (addons/website_event_sale/report/event_sale_report.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 1
- Route evidence: `addons/website_event_sale/controllers/main.py:71`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_event`, `event_sale`, `website_sale`
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

- `addons/website_event_sale/__init__.py`
- `addons/website_event_sale/__manifest__.py`
- `addons/website_event_sale/controllers/__init__.py`
- `addons/website_event_sale/controllers/main.py`
- `addons/website_event_sale/controllers/sale.py`
- `addons/website_event_sale/data/event_data.xml`
- `addons/website_event_sale/i18n/af.po`
- `addons/website_event_sale/i18n/ar.po`
- `addons/website_event_sale/i18n/az.po`
- `addons/website_event_sale/i18n/bg.po`
- `addons/website_event_sale/i18n/bs.po`
- `addons/website_event_sale/i18n/ca.po`
- `addons/website_event_sale/i18n/cs.po`
- `addons/website_event_sale/i18n/da.po`
- `addons/website_event_sale/i18n/de.po`
- `addons/website_event_sale/i18n/el.po`
- `addons/website_event_sale/i18n/es.po`
- `addons/website_event_sale/i18n/es_419.po`
- `addons/website_event_sale/i18n/es_CL.po`
- `addons/website_event_sale/i18n/et.po`
- `addons/website_event_sale/i18n/eu.po`
- `addons/website_event_sale/i18n/fa.po`
- `addons/website_event_sale/i18n/fi.po`
- `addons/website_event_sale/i18n/fo.po`
- `addons/website_event_sale/i18n/fr.po`
- `addons/website_event_sale/i18n/fr_CA.po`
- `addons/website_event_sale/i18n/gl.po`
- `addons/website_event_sale/i18n/gu.po`
- `addons/website_event_sale/i18n/he.po`
- `addons/website_event_sale/i18n/hi.po`
- `addons/website_event_sale/i18n/hr.po`
- `addons/website_event_sale/i18n/hu.po`
- `addons/website_event_sale/i18n/id.po`
- `addons/website_event_sale/i18n/is.po`
- `addons/website_event_sale/i18n/it.po`
- `addons/website_event_sale/i18n/ja.po`
- `addons/website_event_sale/i18n/ka.po`
- `addons/website_event_sale/i18n/kab.po`
- `addons/website_event_sale/i18n/km.po`
- `addons/website_event_sale/i18n/ko.po`
- `addons/website_event_sale/i18n/ku.po`
- `addons/website_event_sale/i18n/lo.po`
- `addons/website_event_sale/i18n/lt.po`
- `addons/website_event_sale/i18n/lv.po`
- `addons/website_event_sale/i18n/mk.po`
- `addons/website_event_sale/i18n/mn.po`
- `addons/website_event_sale/i18n/my.po`
- `addons/website_event_sale/i18n/nb.po`
- `addons/website_event_sale/i18n/nl.po`
- `addons/website_event_sale/i18n/pl.po`
- `addons/website_event_sale/i18n/pt.po`
- `addons/website_event_sale/i18n/pt_BR.po`
- `addons/website_event_sale/i18n/ro.po`
- `addons/website_event_sale/i18n/ru.po`
- `addons/website_event_sale/i18n/sk.po`
- `addons/website_event_sale/i18n/sl.po`
- `addons/website_event_sale/i18n/sr@latin.po`
- `addons/website_event_sale/i18n/sv.po`
- `addons/website_event_sale/i18n/th.po`
- `addons/website_event_sale/i18n/tr.po`
- `addons/website_event_sale/i18n/uk.po`
- `addons/website_event_sale/i18n/uz.po`
- `addons/website_event_sale/i18n/vi.po`
- `addons/website_event_sale/i18n/website_event_sale.pot`
- `addons/website_event_sale/i18n/zh_CN.po`
- `addons/website_event_sale/i18n/zh_TW.po`
- `addons/website_event_sale/models/__init__.py`
- `addons/website_event_sale/models/event_event.py`
- `addons/website_event_sale/models/event_ticket.py`
- `addons/website_event_sale/models/product.py`
- `addons/website_event_sale/models/product_pricelist.py`
- `addons/website_event_sale/models/sale_order.py`
- `addons/website_event_sale/models/sale_order_line.py`
- `addons/website_event_sale/report/__init__.py`
- `addons/website_event_sale/report/event_sale_report.py`
- `addons/website_event_sale/report/event_sale_report_views.xml`
- `addons/website_event_sale/static/description/icon.png`
- `addons/website_event_sale/static/description/icon.svg`
- `addons/website_event_sale/static/description/icon_hi.png`
- `addons/website_event_sale/static/img/event_ticket_placeholder_thumbnail.png`
- `addons/website_event_sale/static/src/scss/website_event_sale_templates.scss`
- `addons/website_event_sale/static/tests/tours/helpers/WebsiteEventSaleTourMethods.js`
- `addons/website_event_sale/static/tests/tours/website_event_sale.js`
- `addons/website_event_sale/static/tests/tours/website_event_sale_last_ticket.js`
- `addons/website_event_sale/static/tests/tours/website_event_sale_pricelists.js`
- `addons/website_event_sale/tests/__init__.py`
- `addons/website_event_sale/tests/common.py`
- `addons/website_event_sale/tests/test_event_checkout.py`
- `addons/website_event_sale/tests/test_frontend_buy_tickets.py`
- `addons/website_event_sale/tests/test_website_event_sale.py`
- `addons/website_event_sale/tests/test_website_event_sale_cart.py`
- `addons/website_event_sale/tests/test_website_event_sale_pricelist.py`
- `addons/website_event_sale/views/event_event_views.xml`
- `addons/website_event_sale/views/website_event_templates.xml`
- `addons/website_event_sale/views/website_sale_templates.xml`
