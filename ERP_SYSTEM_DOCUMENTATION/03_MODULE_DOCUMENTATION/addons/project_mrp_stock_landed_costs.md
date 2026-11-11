# Module: project_mrp_stock_landed_costs

- **Module ID:** MOD-483
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/project_mrp_stock_landed_costs`
- **Manifest:** `addons/project_mrp_stock_landed_costs/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Manufacturing`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Technical Bridge

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 53 files, including 4 Python, 0 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `project_mrp_account`, `mrp_landed_costs`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 0
- Browser asset files: 0
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 1 model declarations, 1 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/project_mrp_stock_landed_costs/models/stock_landed_costs.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 0; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/project_mrp_stock_landed_costs/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `stock.valuation.adjustment.lines` (addons/project_mrp_stock_landed_costs/models/stock_landed_costs.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `project_mrp_account`, `mrp_landed_costs`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Not found
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/project_mrp_stock_landed_costs/__init__.py`
- `addons/project_mrp_stock_landed_costs/__manifest__.py`
- `addons/project_mrp_stock_landed_costs/i18n/ar.po`
- `addons/project_mrp_stock_landed_costs/i18n/az.po`
- `addons/project_mrp_stock_landed_costs/i18n/bg.po`
- `addons/project_mrp_stock_landed_costs/i18n/bs.po`
- `addons/project_mrp_stock_landed_costs/i18n/ca.po`
- `addons/project_mrp_stock_landed_costs/i18n/cs.po`
- `addons/project_mrp_stock_landed_costs/i18n/da.po`
- `addons/project_mrp_stock_landed_costs/i18n/de.po`
- `addons/project_mrp_stock_landed_costs/i18n/el.po`
- `addons/project_mrp_stock_landed_costs/i18n/es.po`
- `addons/project_mrp_stock_landed_costs/i18n/es_419.po`
- `addons/project_mrp_stock_landed_costs/i18n/et.po`
- `addons/project_mrp_stock_landed_costs/i18n/fa.po`
- `addons/project_mrp_stock_landed_costs/i18n/fi.po`
- `addons/project_mrp_stock_landed_costs/i18n/fr.po`
- `addons/project_mrp_stock_landed_costs/i18n/he.po`
- `addons/project_mrp_stock_landed_costs/i18n/hi.po`
- `addons/project_mrp_stock_landed_costs/i18n/hr.po`
- `addons/project_mrp_stock_landed_costs/i18n/hu.po`
- `addons/project_mrp_stock_landed_costs/i18n/id.po`
- `addons/project_mrp_stock_landed_costs/i18n/it.po`
- `addons/project_mrp_stock_landed_costs/i18n/ja.po`
- `addons/project_mrp_stock_landed_costs/i18n/kab.po`
- `addons/project_mrp_stock_landed_costs/i18n/ko.po`
- `addons/project_mrp_stock_landed_costs/i18n/ku.po`
- `addons/project_mrp_stock_landed_costs/i18n/lo.po`
- `addons/project_mrp_stock_landed_costs/i18n/lt.po`
- `addons/project_mrp_stock_landed_costs/i18n/lv.po`
- `addons/project_mrp_stock_landed_costs/i18n/mn.po`
- `addons/project_mrp_stock_landed_costs/i18n/my.po`
- `addons/project_mrp_stock_landed_costs/i18n/nb.po`
- `addons/project_mrp_stock_landed_costs/i18n/nl.po`
- `addons/project_mrp_stock_landed_costs/i18n/pl.po`
- `addons/project_mrp_stock_landed_costs/i18n/project_mrp_stock_landed_costs.pot`
- `addons/project_mrp_stock_landed_costs/i18n/pt.po`
- `addons/project_mrp_stock_landed_costs/i18n/pt_BR.po`
- `addons/project_mrp_stock_landed_costs/i18n/ro.po`
- `addons/project_mrp_stock_landed_costs/i18n/ru.po`
- `addons/project_mrp_stock_landed_costs/i18n/sk.po`
- `addons/project_mrp_stock_landed_costs/i18n/sl.po`
- `addons/project_mrp_stock_landed_costs/i18n/sr@latin.po`
- `addons/project_mrp_stock_landed_costs/i18n/sv.po`
- `addons/project_mrp_stock_landed_costs/i18n/th.po`
- `addons/project_mrp_stock_landed_costs/i18n/tr.po`
- `addons/project_mrp_stock_landed_costs/i18n/uk.po`
- `addons/project_mrp_stock_landed_costs/i18n/uz.po`
- `addons/project_mrp_stock_landed_costs/i18n/vi.po`
- `addons/project_mrp_stock_landed_costs/i18n/zh_CN.po`
- `addons/project_mrp_stock_landed_costs/i18n/zh_TW.po`
- `addons/project_mrp_stock_landed_costs/models/__init__.py`
- `addons/project_mrp_stock_landed_costs/models/stock_landed_costs.py`
