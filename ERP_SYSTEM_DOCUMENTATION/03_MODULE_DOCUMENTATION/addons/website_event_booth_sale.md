# Module: website_event_booth_sale

- **Module ID:** MOD-609
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_event_booth_sale`
- **Manifest:** `addons/website_event_booth_sale/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Events`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Events, sell your booths online

**Manifest description:**

Use the e-commerce to sell your event booths.

**Scope evidence:** The module contains 66 files, including 11 Python, 2 XML, and 4 JavaScript/TypeScript files. The manifest declares dependencies: `event_booth_sale`, `website_event_booth`, `website_sale`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 2
- XML/data/view/template files: 2
- Browser asset files: 4
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 14 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/website_event_booth_sale/models/sale_order.py:7`, `addons/website_event_booth_sale/models/product_template.py:7`, `addons/website_event_booth_sale/models/sale_order_line.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/website_event_booth_sale/controllers/event_booth.py:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 4 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/website_event_booth_sale/views/event_booth_templates.xml:4`, `addons/website_event_booth_sale/views/event_booth_templates.xml:47`, `addons/website_event_booth_sale/views/event_booth_registration_templates.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/website_event_booth_sale/tests/test_website_event_booth_sale_pricelist.py`, `addons/website_event_booth_sale/tests/test_event_booth_sale.py`, `addons/website_event_booth_sale/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `event_booth_registration`, `event_booth_order_progress`, `event_booth_registration_details`
- Menus: 0; representative evidence: Not found in module
- Templates: 3; representative evidence: `addons/website_event_booth_sale/views/event_booth_templates.xml:4`, `addons/website_event_booth_sale/views/event_booth_templates.xml:47`, `addons/website_event_booth_sale/views/event_booth_registration_templates.xml:4`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 4; representative files: `addons/website_event_booth_sale/static/src/interactions/booth_registration.js`, `addons/website_event_booth_sale/static/tests/tours/website_event_booth.js`, `addons/website_event_booth_sale/static/tests/tours/website_event_booth_sale_pricelists.js`, `addons/website_event_booth_sale/static/tests/tours/helpers/WebsiteEventBoothSaleTourMethods.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_event_booth_sale/__manifest__.py`
- **HTTP entry points:** `addons/website_event_booth_sale/controllers/event_booth.py:15`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `sale.order` (addons/website_event_booth_sale/models/sale_order.py:7); inherits `product.template` (addons/website_event_booth_sale/models/product_template.py:7); inherits `sale.order.line` (addons/website_event_booth_sale/models/sale_order_line.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/website_event_booth_sale/controllers/event_booth.py:15`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `event_booth_sale`, `website_event_booth`, `website_sale`
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

- `addons/website_event_booth_sale/__init__.py`
- `addons/website_event_booth_sale/__manifest__.py`
- `addons/website_event_booth_sale/controllers/__init__.py`
- `addons/website_event_booth_sale/controllers/event_booth.py`
- `addons/website_event_booth_sale/i18n/ar.po`
- `addons/website_event_booth_sale/i18n/az.po`
- `addons/website_event_booth_sale/i18n/bg.po`
- `addons/website_event_booth_sale/i18n/bs.po`
- `addons/website_event_booth_sale/i18n/ca.po`
- `addons/website_event_booth_sale/i18n/cs.po`
- `addons/website_event_booth_sale/i18n/da.po`
- `addons/website_event_booth_sale/i18n/de.po`
- `addons/website_event_booth_sale/i18n/el.po`
- `addons/website_event_booth_sale/i18n/es.po`
- `addons/website_event_booth_sale/i18n/es_419.po`
- `addons/website_event_booth_sale/i18n/et.po`
- `addons/website_event_booth_sale/i18n/fa.po`
- `addons/website_event_booth_sale/i18n/fi.po`
- `addons/website_event_booth_sale/i18n/fr.po`
- `addons/website_event_booth_sale/i18n/he.po`
- `addons/website_event_booth_sale/i18n/hi.po`
- `addons/website_event_booth_sale/i18n/hr.po`
- `addons/website_event_booth_sale/i18n/hu.po`
- `addons/website_event_booth_sale/i18n/id.po`
- `addons/website_event_booth_sale/i18n/it.po`
- `addons/website_event_booth_sale/i18n/ja.po`
- `addons/website_event_booth_sale/i18n/kab.po`
- `addons/website_event_booth_sale/i18n/ko.po`
- `addons/website_event_booth_sale/i18n/ku.po`
- `addons/website_event_booth_sale/i18n/lo.po`
- `addons/website_event_booth_sale/i18n/lt.po`
- `addons/website_event_booth_sale/i18n/lv.po`
- `addons/website_event_booth_sale/i18n/mn.po`
- `addons/website_event_booth_sale/i18n/my.po`
- `addons/website_event_booth_sale/i18n/nb.po`
- `addons/website_event_booth_sale/i18n/nl.po`
- `addons/website_event_booth_sale/i18n/pl.po`
- `addons/website_event_booth_sale/i18n/pt.po`
- `addons/website_event_booth_sale/i18n/pt_BR.po`
- `addons/website_event_booth_sale/i18n/ro.po`
- `addons/website_event_booth_sale/i18n/ru.po`
- `addons/website_event_booth_sale/i18n/sk.po`
- `addons/website_event_booth_sale/i18n/sl.po`
- `addons/website_event_booth_sale/i18n/sr@latin.po`
- `addons/website_event_booth_sale/i18n/sv.po`
- `addons/website_event_booth_sale/i18n/th.po`
- `addons/website_event_booth_sale/i18n/tr.po`
- `addons/website_event_booth_sale/i18n/uk.po`
- `addons/website_event_booth_sale/i18n/uz.po`
- `addons/website_event_booth_sale/i18n/vi.po`
- `addons/website_event_booth_sale/i18n/website_event_booth_sale.pot`
- `addons/website_event_booth_sale/i18n/zh_CN.po`
- `addons/website_event_booth_sale/i18n/zh_TW.po`
- `addons/website_event_booth_sale/models/__init__.py`
- `addons/website_event_booth_sale/models/product_template.py`
- `addons/website_event_booth_sale/models/sale_order.py`
- `addons/website_event_booth_sale/models/sale_order_line.py`
- `addons/website_event_booth_sale/static/src/interactions/booth_registration.js`
- `addons/website_event_booth_sale/static/tests/tours/helpers/WebsiteEventBoothSaleTourMethods.js`
- `addons/website_event_booth_sale/static/tests/tours/website_event_booth.js`
- `addons/website_event_booth_sale/static/tests/tours/website_event_booth_sale_pricelists.js`
- `addons/website_event_booth_sale/tests/__init__.py`
- `addons/website_event_booth_sale/tests/test_event_booth_sale.py`
- `addons/website_event_booth_sale/tests/test_website_event_booth_sale_pricelist.py`
- `addons/website_event_booth_sale/views/event_booth_registration_templates.xml`
- `addons/website_event_booth_sale/views/event_booth_templates.xml`
