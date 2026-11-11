# Module: pos_mrp

- **Module ID:** MOD-439
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_mrp`
- **Manifest:** `addons/pos_mrp/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Link module between Point of Sale and Mrp

**Manifest description:**

This is a link module between Point of Sale and Mrp.

**Scope evidence:** The module contains 61 files, including 10 Python, 0 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `pos_stock`, `mrp`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 0
- Browser asset files: 1
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/pos_mrp/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 20 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/pos_mrp/models/pos_order.py:7`, `addons/pos_mrp/models/stock_picking.py:4`, `addons/pos_mrp/models/pos_order_line.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 0 XML files and 1 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/pos_mrp/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/pos_mrp/tests/test_frontend.py`, `addons/pos_mrp/tests/common.py`, `addons/pos_mrp/tests/test_pos_mrp_flow.py`, `addons/pos_mrp/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 0; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 1; representative files: `addons/pos_mrp/static/tests/tours/pos_mrp_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_mrp/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `pos.order` (addons/pos_mrp/models/pos_order.py:7); inherits `stock.move` (addons/pos_mrp/models/stock_picking.py:4); inherits `pos.order.line` (addons/pos_mrp/models/pos_order_line.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `pos_stock`, `mrp`
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

- `addons/pos_mrp/__init__.py`
- `addons/pos_mrp/__manifest__.py`
- `addons/pos_mrp/i18n/ar.po`
- `addons/pos_mrp/i18n/az.po`
- `addons/pos_mrp/i18n/bg.po`
- `addons/pos_mrp/i18n/bs.po`
- `addons/pos_mrp/i18n/ca.po`
- `addons/pos_mrp/i18n/cs.po`
- `addons/pos_mrp/i18n/da.po`
- `addons/pos_mrp/i18n/de.po`
- `addons/pos_mrp/i18n/el.po`
- `addons/pos_mrp/i18n/es.po`
- `addons/pos_mrp/i18n/es_419.po`
- `addons/pos_mrp/i18n/et.po`
- `addons/pos_mrp/i18n/fa.po`
- `addons/pos_mrp/i18n/fi.po`
- `addons/pos_mrp/i18n/fr.po`
- `addons/pos_mrp/i18n/he.po`
- `addons/pos_mrp/i18n/hi.po`
- `addons/pos_mrp/i18n/hr.po`
- `addons/pos_mrp/i18n/hu.po`
- `addons/pos_mrp/i18n/id.po`
- `addons/pos_mrp/i18n/it.po`
- `addons/pos_mrp/i18n/ja.po`
- `addons/pos_mrp/i18n/kab.po`
- `addons/pos_mrp/i18n/ko.po`
- `addons/pos_mrp/i18n/ku.po`
- `addons/pos_mrp/i18n/lo.po`
- `addons/pos_mrp/i18n/lt.po`
- `addons/pos_mrp/i18n/lv.po`
- `addons/pos_mrp/i18n/mn.po`
- `addons/pos_mrp/i18n/my.po`
- `addons/pos_mrp/i18n/nb.po`
- `addons/pos_mrp/i18n/nl.po`
- `addons/pos_mrp/i18n/pl.po`
- `addons/pos_mrp/i18n/pos_mrp.pot`
- `addons/pos_mrp/i18n/pt.po`
- `addons/pos_mrp/i18n/pt_BR.po`
- `addons/pos_mrp/i18n/ro.po`
- `addons/pos_mrp/i18n/ru.po`
- `addons/pos_mrp/i18n/sk.po`
- `addons/pos_mrp/i18n/sl.po`
- `addons/pos_mrp/i18n/sr@latin.po`
- `addons/pos_mrp/i18n/sv.po`
- `addons/pos_mrp/i18n/th.po`
- `addons/pos_mrp/i18n/tr.po`
- `addons/pos_mrp/i18n/uk.po`
- `addons/pos_mrp/i18n/uz.po`
- `addons/pos_mrp/i18n/vi.po`
- `addons/pos_mrp/i18n/zh_CN.po`
- `addons/pos_mrp/i18n/zh_TW.po`
- `addons/pos_mrp/models/__init__.py`
- `addons/pos_mrp/models/pos_order.py`
- `addons/pos_mrp/models/pos_order_line.py`
- `addons/pos_mrp/models/stock_picking.py`
- `addons/pos_mrp/security/ir.access.csv`
- `addons/pos_mrp/static/tests/tours/pos_mrp_tour.js`
- `addons/pos_mrp/tests/__init__.py`
- `addons/pos_mrp/tests/common.py`
- `addons/pos_mrp/tests/test_frontend.py`
- `addons/pos_mrp/tests/test_pos_mrp_flow.py`
