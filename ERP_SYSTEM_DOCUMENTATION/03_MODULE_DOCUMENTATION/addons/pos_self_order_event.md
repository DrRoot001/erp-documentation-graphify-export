# Module: pos_self_order_event

- **Module ID:** MOD-457
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_self_order_event`
- **Manifest:** `addons/pos_self_order_event/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point Of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Link module between PoS Self Order and PoS Event

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 81 files, including 10 Python, 5 XML, and 14 JavaScript/TypeScript files. The manifest declares dependencies: `pos_self_order`, `pos_event`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 2
- XML/data/view/template files: 5
- Browser asset files: 14
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 12 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/pos_self_order_event/models/pos_config.py:6`, `addons/pos_self_order_event/models/pos_order.py:4`, `addons/pos_self_order_event/models/event_event.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 2 route declarations.
- **Evidence:** `addons/pos_self_order_event/controllers/main.py:10`, `addons/pos_self_order_event/controllers/main.py:18`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 14 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/pos_self_order_event/tests/test_self_order_event.py`, `addons/pos_self_order_event/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 14; representative files: `addons/pos_self_order_event/static/src/app/self_order_index.js`, `addons/pos_self_order_event/static/src/app/services/card_utils.js`, `addons/pos_self_order_event/static/src/app/services/self_order_service.js`, `addons/pos_self_order_event/static/src/app/models/pos_category.js`, `addons/pos_self_order_event/static/src/app/components/product_card/product_card.js`, `addons/pos_self_order_event/static/src/app/pages/order_history_page/order_history_page.js`, `addons/pos_self_order_event/static/src/app/pages/event_page/event_page.js`, `addons/pos_self_order_event/static/src/app/pages/confirmation_page/confirmation_page.js`, `addons/pos_self_order_event/static/src/app/pages/cart_page/cart_page.js`, `addons/pos_self_order_event/static/tests/unit/services/self_order_service.test.js`, `addons/pos_self_order_event/static/tests/unit/data/pos_config.data.js`, `addons/pos_self_order_event/static/tests/unit/components/product_card.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_self_order_event/__manifest__.py`
- **HTTP entry points:** `addons/pos_self_order_event/controllers/main.py:10`, `addons/pos_self_order_event/controllers/main.py:18`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `pos.config` (addons/pos_self_order_event/models/pos_config.py:6); inherits `pos.order` (addons/pos_self_order_event/models/pos_order.py:4); inherits `event.event` (addons/pos_self_order_event/models/event_event.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 2
- Route evidence: `addons/pos_self_order_event/controllers/main.py:10`, `addons/pos_self_order_event/controllers/main.py:18`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `pos_self_order`, `pos_event`
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

- `addons/pos_self_order_event/__init__.py`
- `addons/pos_self_order_event/__manifest__.py`
- `addons/pos_self_order_event/controllers/__init__.py`
- `addons/pos_self_order_event/controllers/main.py`
- `addons/pos_self_order_event/i18n/ar.po`
- `addons/pos_self_order_event/i18n/az.po`
- `addons/pos_self_order_event/i18n/bg.po`
- `addons/pos_self_order_event/i18n/bs.po`
- `addons/pos_self_order_event/i18n/ca.po`
- `addons/pos_self_order_event/i18n/cs.po`
- `addons/pos_self_order_event/i18n/da.po`
- `addons/pos_self_order_event/i18n/de.po`
- `addons/pos_self_order_event/i18n/el.po`
- `addons/pos_self_order_event/i18n/es.po`
- `addons/pos_self_order_event/i18n/es_419.po`
- `addons/pos_self_order_event/i18n/et.po`
- `addons/pos_self_order_event/i18n/fa.po`
- `addons/pos_self_order_event/i18n/fi.po`
- `addons/pos_self_order_event/i18n/fr.po`
- `addons/pos_self_order_event/i18n/he.po`
- `addons/pos_self_order_event/i18n/hi.po`
- `addons/pos_self_order_event/i18n/hr.po`
- `addons/pos_self_order_event/i18n/hu.po`
- `addons/pos_self_order_event/i18n/id.po`
- `addons/pos_self_order_event/i18n/it.po`
- `addons/pos_self_order_event/i18n/ja.po`
- `addons/pos_self_order_event/i18n/kab.po`
- `addons/pos_self_order_event/i18n/ko.po`
- `addons/pos_self_order_event/i18n/ku.po`
- `addons/pos_self_order_event/i18n/lo.po`
- `addons/pos_self_order_event/i18n/lt.po`
- `addons/pos_self_order_event/i18n/lv.po`
- `addons/pos_self_order_event/i18n/mn.po`
- `addons/pos_self_order_event/i18n/my.po`
- `addons/pos_self_order_event/i18n/nb.po`
- `addons/pos_self_order_event/i18n/nl.po`
- `addons/pos_self_order_event/i18n/pl.po`
- `addons/pos_self_order_event/i18n/pos_self_order_event.pot`
- `addons/pos_self_order_event/i18n/pt.po`
- `addons/pos_self_order_event/i18n/pt_BR.po`
- `addons/pos_self_order_event/i18n/ro.po`
- `addons/pos_self_order_event/i18n/ru.po`
- `addons/pos_self_order_event/i18n/sk.po`
- `addons/pos_self_order_event/i18n/sl.po`
- `addons/pos_self_order_event/i18n/sr@latin.po`
- `addons/pos_self_order_event/i18n/sv.po`
- `addons/pos_self_order_event/i18n/th.po`
- `addons/pos_self_order_event/i18n/tr.po`
- `addons/pos_self_order_event/i18n/uk.po`
- `addons/pos_self_order_event/i18n/uz.po`
- `addons/pos_self_order_event/i18n/vi.po`
- `addons/pos_self_order_event/i18n/zh_CN.po`
- `addons/pos_self_order_event/i18n/zh_TW.po`
- `addons/pos_self_order_event/models/__init__.py`
- `addons/pos_self_order_event/models/event_event.py`
- `addons/pos_self_order_event/models/pos_config.py`
- `addons/pos_self_order_event/models/pos_order.py`
- `addons/pos_self_order_event/static/src/app/components/product_card/product_card.js`
- `addons/pos_self_order_event/static/src/app/components/product_card/product_card.xml`
- `addons/pos_self_order_event/static/src/app/models/pos_category.js`
- `addons/pos_self_order_event/static/src/app/pages/cart_page/cart_page.js`
- `addons/pos_self_order_event/static/src/app/pages/confirmation_page/confirmation_page.js`
- `addons/pos_self_order_event/static/src/app/pages/confirmation_page/confirmation_page.xml`
- `addons/pos_self_order_event/static/src/app/pages/event_page/event_page.js`
- `addons/pos_self_order_event/static/src/app/pages/event_page/event_page.scss`
- `addons/pos_self_order_event/static/src/app/pages/event_page/event_page.xml`
- `addons/pos_self_order_event/static/src/app/pages/order_history_page/order_history_page.js`
- `addons/pos_self_order_event/static/src/app/pages/order_history_page/order_history_page.xml`
- `addons/pos_self_order_event/static/src/app/self_order_index.js`
- `addons/pos_self_order_event/static/src/app/self_order_index.xml`
- `addons/pos_self_order_event/static/src/app/services/card_utils.js`
- `addons/pos_self_order_event/static/src/app/services/self_order_service.js`
- `addons/pos_self_order_event/static/src/img/event_ticket_placeholder_thumbnail.png`
- `addons/pos_self_order_event/static/src/img/placeholder_thumbnail.png`
- `addons/pos_self_order_event/static/tests/unit/components/product_card.test.js`
- `addons/pos_self_order_event/static/tests/unit/data/pos_config.data.js`
- `addons/pos_self_order_event/static/tests/unit/pages/cart_page.test.js`
- `addons/pos_self_order_event/static/tests/unit/pages/event_page.test.js`
- `addons/pos_self_order_event/static/tests/unit/services/self_order_service.test.js`
- `addons/pos_self_order_event/tests/__init__.py`
- `addons/pos_self_order_event/tests/test_self_order_event.py`
