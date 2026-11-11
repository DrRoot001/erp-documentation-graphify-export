# Module: mrp_landed_costs

- **Module ID:** MOD-380
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/mrp_landed_costs`
- **Manifest:** `addons/mrp_landed_costs/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Manufacturing`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Landed Costs on Manufacturing Order

**Manifest description:**

This module allows you to easily add extra costs on manufacturing order
and decide the split of these costs among their stock moves in order to
take them into account in your stock valuation.

**Scope evidence:** The module contains 56 files, including 6 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `stock_landed_costs`, `mrp`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 1
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 1 model declarations, 9 methods, 0 constraint handlers, 1 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/mrp_landed_costs/models/stock_landed_cost.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/mrp_landed_costs/views/stock_landed_cost_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/mrp_landed_costs/tests/test_stock_landed_costs_mrp.py`, `addons/mrp_landed_costs/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `view_mrp_landed_costs_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/mrp_landed_costs/views/stock_landed_cost_views.xml:5`, `addons/mrp_landed_costs/views/stock_landed_cost_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/mrp_landed_costs/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `stock.landed.cost` (addons/mrp_landed_costs/models/stock_landed_cost.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `stock_landed_costs`, `mrp`
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

- `addons/mrp_landed_costs/__init__.py`
- `addons/mrp_landed_costs/__manifest__.py`
- `addons/mrp_landed_costs/i18n/ar.po`
- `addons/mrp_landed_costs/i18n/az.po`
- `addons/mrp_landed_costs/i18n/bg.po`
- `addons/mrp_landed_costs/i18n/bs.po`
- `addons/mrp_landed_costs/i18n/ca.po`
- `addons/mrp_landed_costs/i18n/cs.po`
- `addons/mrp_landed_costs/i18n/da.po`
- `addons/mrp_landed_costs/i18n/de.po`
- `addons/mrp_landed_costs/i18n/el.po`
- `addons/mrp_landed_costs/i18n/es.po`
- `addons/mrp_landed_costs/i18n/es_419.po`
- `addons/mrp_landed_costs/i18n/et.po`
- `addons/mrp_landed_costs/i18n/fa.po`
- `addons/mrp_landed_costs/i18n/fi.po`
- `addons/mrp_landed_costs/i18n/fr.po`
- `addons/mrp_landed_costs/i18n/he.po`
- `addons/mrp_landed_costs/i18n/hi.po`
- `addons/mrp_landed_costs/i18n/hr.po`
- `addons/mrp_landed_costs/i18n/hu.po`
- `addons/mrp_landed_costs/i18n/id.po`
- `addons/mrp_landed_costs/i18n/it.po`
- `addons/mrp_landed_costs/i18n/ja.po`
- `addons/mrp_landed_costs/i18n/kab.po`
- `addons/mrp_landed_costs/i18n/ko.po`
- `addons/mrp_landed_costs/i18n/ku.po`
- `addons/mrp_landed_costs/i18n/lo.po`
- `addons/mrp_landed_costs/i18n/lt.po`
- `addons/mrp_landed_costs/i18n/lv.po`
- `addons/mrp_landed_costs/i18n/mn.po`
- `addons/mrp_landed_costs/i18n/mrp_landed_costs.pot`
- `addons/mrp_landed_costs/i18n/my.po`
- `addons/mrp_landed_costs/i18n/nb.po`
- `addons/mrp_landed_costs/i18n/nl.po`
- `addons/mrp_landed_costs/i18n/pl.po`
- `addons/mrp_landed_costs/i18n/pt.po`
- `addons/mrp_landed_costs/i18n/pt_BR.po`
- `addons/mrp_landed_costs/i18n/ro.po`
- `addons/mrp_landed_costs/i18n/ru.po`
- `addons/mrp_landed_costs/i18n/sk.po`
- `addons/mrp_landed_costs/i18n/sl.po`
- `addons/mrp_landed_costs/i18n/sr@latin.po`
- `addons/mrp_landed_costs/i18n/sv.po`
- `addons/mrp_landed_costs/i18n/th.po`
- `addons/mrp_landed_costs/i18n/tr.po`
- `addons/mrp_landed_costs/i18n/uk.po`
- `addons/mrp_landed_costs/i18n/uz.po`
- `addons/mrp_landed_costs/i18n/vi.po`
- `addons/mrp_landed_costs/i18n/zh_CN.po`
- `addons/mrp_landed_costs/i18n/zh_TW.po`
- `addons/mrp_landed_costs/models/__init__.py`
- `addons/mrp_landed_costs/models/stock_landed_cost.py`
- `addons/mrp_landed_costs/tests/__init__.py`
- `addons/mrp_landed_costs/tests/test_stock_landed_costs_mrp.py`
- `addons/mrp_landed_costs/views/stock_landed_cost_views.xml`
