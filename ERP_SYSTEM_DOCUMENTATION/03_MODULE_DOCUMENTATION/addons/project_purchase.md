# Module: project_purchase

- **Module ID:** MOD-484
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/project_purchase`
- **Manifest:** `addons/project_purchase/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Services/Project`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Monitor purchase in project

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 65 files, including 12 Python, 3 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `purchase`, `project_account`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 2
- XML/data/view/template files: 3
- Browser asset files: 1
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 10 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/project_purchase/models/purchase_order.py:6`, `addons/project_purchase/models/purchase_order_line.py:6`, `addons/project_purchase/models/project_project.py:4`, `addons/project_purchase/report/purchase_report.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/project_purchase/controllers/catalog.py:10`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 1 JavaScript/TypeScript files; static XML analysis found 11 record/template/menu identifiers.
- **Evidence:** `addons/project_purchase/data/project_purchase_demo.xml:9`, `addons/project_purchase/data/project_purchase_demo.xml:19`, `addons/project_purchase/data/project_purchase_demo.xml:29`, `addons/project_purchase/data/project_purchase_demo.xml:40`, `addons/project_purchase/data/project_purchase_demo.xml:48`, `addons/project_purchase/data/project_purchase_demo.xml:58`, `addons/project_purchase/data/project_purchase_demo.xml:68`, `addons/project_purchase/views/project_project.xml:3`, `addons/project_purchase/views/project_project.xml:17`, `addons/project_purchase/views/project_project.xml:27`, `addons/project_purchase/views/purchase_order.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/project_purchase/tests/__init__.py`, `addons/project_purchase/tests/test_project_purchase.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `product_product_cement`, `product_product_sand`, `product_product_bricks`, `purchase_order_for_home_construction`, `purchase_order_line_for_home_construction_1`, `purchase_order_line_for_home_construction_2`, `purchase_order_line_for_home_construction_3`, `project_view_form_inherit_project_purchase`, `project_embedded_action_purchase_orders`, `project_embedded_action_purchase_orders_dashboard`, `view_order_form_inherit_project_purchase`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/project_purchase/views/project_project.xml:5`, `addons/project_purchase/views/project_project.xml:7`, `addons/project_purchase/views/purchase_order.xml:5`, `addons/project_purchase/views/purchase_order.xml:8`
- Browser assets: 1; representative files: `addons/project_purchase/static/src/product_catalog/kanban_record.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/project_purchase/__manifest__.py`
- **HTTP entry points:** `addons/project_purchase/controllers/catalog.py:10`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `purchase.order` (addons/project_purchase/models/purchase_order.py:6); inherits `purchase.order.line` (addons/project_purchase/models/purchase_order_line.py:6); inherits `project.project` (addons/project_purchase/models/project_project.py:4); inherits `purchase.report` (addons/project_purchase/report/purchase_report.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/project_purchase/controllers/catalog.py:10`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `purchase`, `project_account`
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

- `addons/project_purchase/__init__.py`
- `addons/project_purchase/__manifest__.py`
- `addons/project_purchase/controllers/__init__.py`
- `addons/project_purchase/controllers/catalog.py`
- `addons/project_purchase/data/project_purchase_demo.xml`
- `addons/project_purchase/i18n/ar.po`
- `addons/project_purchase/i18n/az.po`
- `addons/project_purchase/i18n/bg.po`
- `addons/project_purchase/i18n/bs.po`
- `addons/project_purchase/i18n/ca.po`
- `addons/project_purchase/i18n/cs.po`
- `addons/project_purchase/i18n/da.po`
- `addons/project_purchase/i18n/de.po`
- `addons/project_purchase/i18n/el.po`
- `addons/project_purchase/i18n/es.po`
- `addons/project_purchase/i18n/es_419.po`
- `addons/project_purchase/i18n/et.po`
- `addons/project_purchase/i18n/fa.po`
- `addons/project_purchase/i18n/fi.po`
- `addons/project_purchase/i18n/fr.po`
- `addons/project_purchase/i18n/he.po`
- `addons/project_purchase/i18n/hi.po`
- `addons/project_purchase/i18n/hr.po`
- `addons/project_purchase/i18n/hu.po`
- `addons/project_purchase/i18n/id.po`
- `addons/project_purchase/i18n/it.po`
- `addons/project_purchase/i18n/ja.po`
- `addons/project_purchase/i18n/kab.po`
- `addons/project_purchase/i18n/ko.po`
- `addons/project_purchase/i18n/ku.po`
- `addons/project_purchase/i18n/lo.po`
- `addons/project_purchase/i18n/lt.po`
- `addons/project_purchase/i18n/lv.po`
- `addons/project_purchase/i18n/mn.po`
- `addons/project_purchase/i18n/my.po`
- `addons/project_purchase/i18n/nb.po`
- `addons/project_purchase/i18n/nl.po`
- `addons/project_purchase/i18n/pl.po`
- `addons/project_purchase/i18n/project_purchase.pot`
- `addons/project_purchase/i18n/pt.po`
- `addons/project_purchase/i18n/pt_BR.po`
- `addons/project_purchase/i18n/ro.po`
- `addons/project_purchase/i18n/ru.po`
- `addons/project_purchase/i18n/sk.po`
- `addons/project_purchase/i18n/sl.po`
- `addons/project_purchase/i18n/sr@latin.po`
- `addons/project_purchase/i18n/sv.po`
- `addons/project_purchase/i18n/th.po`
- `addons/project_purchase/i18n/tr.po`
- `addons/project_purchase/i18n/uk.po`
- `addons/project_purchase/i18n/uz.po`
- `addons/project_purchase/i18n/vi.po`
- `addons/project_purchase/i18n/zh_CN.po`
- `addons/project_purchase/i18n/zh_TW.po`
- `addons/project_purchase/models/__init__.py`
- `addons/project_purchase/models/project_project.py`
- `addons/project_purchase/models/purchase_order.py`
- `addons/project_purchase/models/purchase_order_line.py`
- `addons/project_purchase/report/__init__.py`
- `addons/project_purchase/report/purchase_report.py`
- `addons/project_purchase/static/src/product_catalog/kanban_record.js`
- `addons/project_purchase/tests/__init__.py`
- `addons/project_purchase/tests/test_project_purchase.py`
- `addons/project_purchase/views/project_project.xml`
- `addons/project_purchase/views/purchase_order.xml`
