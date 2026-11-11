# Module: mrp_repair

- **Module ID:** MOD-382
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/mrp_repair`
- **Manifest:** `addons/mrp_repair/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Inventory`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 60 files, including 9 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `repair`, `mrp`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 2
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

- **Description:** 4 model declarations, 21 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/mrp_repair/models/production.py:6`, `addons/mrp_repair/models/stock_move.py:4`, `addons/mrp_repair/models/repair.py:6`, `addons/mrp_repair/models/repair.py:78`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/mrp_repair/views/production_views.xml:4`, `addons/mrp_repair/views/repair_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/mrp_repair/tests/test_tracability.py`, `addons/mrp_repair/tests/test_mrp_repair_flow.py`, `addons/mrp_repair/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `mrp_production_form_view_inherit`, `view_repair_order_form_inherit`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/mrp_repair/views/production_views.xml:6`, `addons/mrp_repair/views/production_views.xml:8`, `addons/mrp_repair/views/repair_views.xml:6`, `addons/mrp_repair/views/repair_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/mrp_repair/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `mrp.production` (addons/mrp_repair/models/production.py:6); inherits `stock.move` (addons/mrp_repair/models/stock_move.py:4); inherits `repair.order` (addons/mrp_repair/models/repair.py:6); inherits `stock.move` (addons/mrp_repair/models/repair.py:78)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `repair`, `mrp`
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

- `addons/mrp_repair/__init__.py`
- `addons/mrp_repair/__manifest__.py`
- `addons/mrp_repair/i18n/ar.po`
- `addons/mrp_repair/i18n/az.po`
- `addons/mrp_repair/i18n/bg.po`
- `addons/mrp_repair/i18n/bs.po`
- `addons/mrp_repair/i18n/ca.po`
- `addons/mrp_repair/i18n/cs.po`
- `addons/mrp_repair/i18n/da.po`
- `addons/mrp_repair/i18n/de.po`
- `addons/mrp_repair/i18n/el.po`
- `addons/mrp_repair/i18n/es.po`
- `addons/mrp_repair/i18n/es_419.po`
- `addons/mrp_repair/i18n/et.po`
- `addons/mrp_repair/i18n/fa.po`
- `addons/mrp_repair/i18n/fi.po`
- `addons/mrp_repair/i18n/fr.po`
- `addons/mrp_repair/i18n/he.po`
- `addons/mrp_repair/i18n/hi.po`
- `addons/mrp_repair/i18n/hr.po`
- `addons/mrp_repair/i18n/hu.po`
- `addons/mrp_repair/i18n/id.po`
- `addons/mrp_repair/i18n/it.po`
- `addons/mrp_repair/i18n/ja.po`
- `addons/mrp_repair/i18n/kab.po`
- `addons/mrp_repair/i18n/ko.po`
- `addons/mrp_repair/i18n/ku.po`
- `addons/mrp_repair/i18n/lo.po`
- `addons/mrp_repair/i18n/lt.po`
- `addons/mrp_repair/i18n/lv.po`
- `addons/mrp_repair/i18n/mn.po`
- `addons/mrp_repair/i18n/mrp_repair.pot`
- `addons/mrp_repair/i18n/my.po`
- `addons/mrp_repair/i18n/nb.po`
- `addons/mrp_repair/i18n/nl.po`
- `addons/mrp_repair/i18n/pl.po`
- `addons/mrp_repair/i18n/pt.po`
- `addons/mrp_repair/i18n/pt_BR.po`
- `addons/mrp_repair/i18n/ro.po`
- `addons/mrp_repair/i18n/ru.po`
- `addons/mrp_repair/i18n/sk.po`
- `addons/mrp_repair/i18n/sl.po`
- `addons/mrp_repair/i18n/sr@latin.po`
- `addons/mrp_repair/i18n/sv.po`
- `addons/mrp_repair/i18n/th.po`
- `addons/mrp_repair/i18n/tr.po`
- `addons/mrp_repair/i18n/uk.po`
- `addons/mrp_repair/i18n/uz.po`
- `addons/mrp_repair/i18n/vi.po`
- `addons/mrp_repair/i18n/zh_CN.po`
- `addons/mrp_repair/i18n/zh_TW.po`
- `addons/mrp_repair/models/__init__.py`
- `addons/mrp_repair/models/production.py`
- `addons/mrp_repair/models/repair.py`
- `addons/mrp_repair/models/stock_move.py`
- `addons/mrp_repair/tests/__init__.py`
- `addons/mrp_repair/tests/test_mrp_repair_flow.py`
- `addons/mrp_repair/tests/test_tracability.py`
- `addons/mrp_repair/views/production_views.xml`
- `addons/mrp_repair/views/repair_views.xml`
