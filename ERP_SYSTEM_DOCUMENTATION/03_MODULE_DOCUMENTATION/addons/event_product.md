# Module: event_product

- **Module ID:** MOD-069
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/event_product`
- **Manifest:** `addons/event_product/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Events`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 66 files, including 12 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `event`, `product`, `account`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 0
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 17 methods, 1 constraint handlers, 0 onchange handlers, and 6 dependency declarations.
- **Evidence:** `addons/event_product/models/product_product.py:5`, `addons/event_product/models/product_template.py:4`, `addons/event_product/models/event_type_ticket.py:12`, `addons/event_product/models/event_event_ticket.py:5`, `addons/event_product/models/event_event.py:4`, `addons/event_product/models/event_registration.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 21 record/template/menu identifiers.
- **Evidence:** `addons/event_product/data/event_product_data.xml:4`, `addons/event_product/data/event_product_data.xml:9`, `addons/event_product/data/event_product_demo.xml:4`, `addons/event_product/data/event_product_demo.xml:14`, `addons/event_product/data/event_demo.xml:3`, `addons/event_product/data/event_demo.xml:7`, `addons/event_product/data/event_demo.xml:11`, `addons/event_product/data/event_demo.xml:16`, `addons/event_product/data/event_demo.xml:20`, `addons/event_product/data/event_demo.xml:25`, `addons/event_product/data/event_demo.xml:30`, `addons/event_product/data/event_demo.xml:34`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/event_product/tests/common.py`, `addons/event_product/tests/__init__.py`, `addons/event_product/tests/test_event_product.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `product_category_events`, `product_product_event`, `product_product_event_standard`, `product_product_event_vip`, `event.event_0_ticket_0`, `event.event_0_ticket_1`, `event.event_0_ticket_2`, `event.event_2_ticket_1`, `event.event_2_ticket_2`, `event.event_4_ticket_0`, `event.event_7_ticket_1`, `event.event_7_ticket_2`, `event_type_ticket_view_tree_from_type`, `event_type_ticket_view_form_from_type`, `event_event_ticket_view_tree_from_event`, `event_event_ticket_view_form_from_event`, `event_event_ticket_view_kanban_from_event`, `event_event_ticket_form_view`, `view_event_registration_ticket_tree`, `event_registration_view_graph`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 18; representative evidence: `addons/event_product/views/event_ticket_views.xml:7`, `addons/event_product/views/event_ticket_views.xml:9`, `addons/event_product/views/event_ticket_views.xml:26`, `addons/event_product/views/event_ticket_views.xml:28`, `addons/event_product/views/event_ticket_views.xml:46`, `addons/event_product/views/event_ticket_views.xml:48`, `addons/event_product/views/event_ticket_views.xml:74`, `addons/event_product/views/event_ticket_views.xml:76`, `addons/event_product/views/event_ticket_views.xml:93`, `addons/event_product/views/event_ticket_views.xml:95`, `addons/event_product/views/event_ticket_views.xml:107`, `addons/event_product/views/event_ticket_views.xml:109`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/event_product/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `product.product` (addons/event_product/models/product_product.py:5); inherits `product.template` (addons/event_product/models/product_template.py:4); inherits `event.type.ticket` (addons/event_product/models/event_type_ticket.py:12); inherits `event.event.ticket` (addons/event_product/models/event_event_ticket.py:5); inherits `event.event` (addons/event_product/models/event_event.py:4); inherits `event.registration` (addons/event_product/models/event_registration.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `event`, `product`, `account`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/event_product/__init__.py`
- `addons/event_product/__manifest__.py`
- `addons/event_product/data/event_demo.xml`
- `addons/event_product/data/event_product_data.xml`
- `addons/event_product/data/event_product_demo.xml`
- `addons/event_product/i18n/ar.po`
- `addons/event_product/i18n/az.po`
- `addons/event_product/i18n/bg.po`
- `addons/event_product/i18n/bs.po`
- `addons/event_product/i18n/ca.po`
- `addons/event_product/i18n/cs.po`
- `addons/event_product/i18n/da.po`
- `addons/event_product/i18n/de.po`
- `addons/event_product/i18n/el.po`
- `addons/event_product/i18n/es.po`
- `addons/event_product/i18n/es_419.po`
- `addons/event_product/i18n/et.po`
- `addons/event_product/i18n/event_product.pot`
- `addons/event_product/i18n/fa.po`
- `addons/event_product/i18n/fi.po`
- `addons/event_product/i18n/fr.po`
- `addons/event_product/i18n/he.po`
- `addons/event_product/i18n/hi.po`
- `addons/event_product/i18n/hr.po`
- `addons/event_product/i18n/hu.po`
- `addons/event_product/i18n/id.po`
- `addons/event_product/i18n/it.po`
- `addons/event_product/i18n/ja.po`
- `addons/event_product/i18n/kab.po`
- `addons/event_product/i18n/ko.po`
- `addons/event_product/i18n/ku.po`
- `addons/event_product/i18n/lo.po`
- `addons/event_product/i18n/lt.po`
- `addons/event_product/i18n/lv.po`
- `addons/event_product/i18n/mn.po`
- `addons/event_product/i18n/my.po`
- `addons/event_product/i18n/nb.po`
- `addons/event_product/i18n/nl.po`
- `addons/event_product/i18n/pl.po`
- `addons/event_product/i18n/pt.po`
- `addons/event_product/i18n/pt_BR.po`
- `addons/event_product/i18n/ro.po`
- `addons/event_product/i18n/ru.po`
- `addons/event_product/i18n/sk.po`
- `addons/event_product/i18n/sl.po`
- `addons/event_product/i18n/sr@latin.po`
- `addons/event_product/i18n/sv.po`
- `addons/event_product/i18n/th.po`
- `addons/event_product/i18n/tr.po`
- `addons/event_product/i18n/uk.po`
- `addons/event_product/i18n/uz.po`
- `addons/event_product/i18n/vi.po`
- `addons/event_product/i18n/zh_CN.po`
- `addons/event_product/i18n/zh_TW.po`
- `addons/event_product/models/__init__.py`
- `addons/event_product/models/event_event.py`
- `addons/event_product/models/event_event_ticket.py`
- `addons/event_product/models/event_registration.py`
- `addons/event_product/models/event_type_ticket.py`
- `addons/event_product/models/product_product.py`
- `addons/event_product/models/product_template.py`
- `addons/event_product/tests/__init__.py`
- `addons/event_product/tests/common.py`
- `addons/event_product/tests/test_event_product.py`
- `addons/event_product/views/event_registration_views.xml`
- `addons/event_product/views/event_ticket_views.xml`
