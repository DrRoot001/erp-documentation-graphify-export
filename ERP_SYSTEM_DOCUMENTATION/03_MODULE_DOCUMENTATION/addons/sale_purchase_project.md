# Module: sale_purchase_project

- **Module ID:** MOD-529
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_purchase_project`
- **Manifest:** `addons/sale_purchase_project/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Technical Bridge

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 56 files, including 7 Python, 0 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `sale_purchase`, `project_purchase`, `sale_project`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 0
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

- **Description:** 2 model declarations, 7 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/sale_purchase_project/models/account_analytic_line.py:4`, `addons/sale_purchase_project/models/sale_order_line.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/sale_purchase_project/tests/test_sale_purchase_project.py`, `addons/sale_purchase_project/tests/__init__.py`
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

- **Entry point evidence:** `addons/sale_purchase_project/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `account.analytic.line` (addons/sale_purchase_project/models/account_analytic_line.py:4); inherits `sale.order.line` (addons/sale_purchase_project/models/sale_order_line.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale_purchase`, `project_purchase`, `sale_project`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Not found
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/sale_purchase_project/__init__.py`
- `addons/sale_purchase_project/__manifest__.py`
- `addons/sale_purchase_project/i18n/ar.po`
- `addons/sale_purchase_project/i18n/az.po`
- `addons/sale_purchase_project/i18n/bg.po`
- `addons/sale_purchase_project/i18n/bs.po`
- `addons/sale_purchase_project/i18n/ca.po`
- `addons/sale_purchase_project/i18n/cs.po`
- `addons/sale_purchase_project/i18n/da.po`
- `addons/sale_purchase_project/i18n/de.po`
- `addons/sale_purchase_project/i18n/el.po`
- `addons/sale_purchase_project/i18n/es.po`
- `addons/sale_purchase_project/i18n/es_419.po`
- `addons/sale_purchase_project/i18n/et.po`
- `addons/sale_purchase_project/i18n/fa.po`
- `addons/sale_purchase_project/i18n/fi.po`
- `addons/sale_purchase_project/i18n/fr.po`
- `addons/sale_purchase_project/i18n/he.po`
- `addons/sale_purchase_project/i18n/hi.po`
- `addons/sale_purchase_project/i18n/hr.po`
- `addons/sale_purchase_project/i18n/hu.po`
- `addons/sale_purchase_project/i18n/id.po`
- `addons/sale_purchase_project/i18n/it.po`
- `addons/sale_purchase_project/i18n/ja.po`
- `addons/sale_purchase_project/i18n/kab.po`
- `addons/sale_purchase_project/i18n/ko.po`
- `addons/sale_purchase_project/i18n/ku.po`
- `addons/sale_purchase_project/i18n/lo.po`
- `addons/sale_purchase_project/i18n/lt.po`
- `addons/sale_purchase_project/i18n/lv.po`
- `addons/sale_purchase_project/i18n/mn.po`
- `addons/sale_purchase_project/i18n/my.po`
- `addons/sale_purchase_project/i18n/nb.po`
- `addons/sale_purchase_project/i18n/nl.po`
- `addons/sale_purchase_project/i18n/pl.po`
- `addons/sale_purchase_project/i18n/pt.po`
- `addons/sale_purchase_project/i18n/pt_BR.po`
- `addons/sale_purchase_project/i18n/ro.po`
- `addons/sale_purchase_project/i18n/ru.po`
- `addons/sale_purchase_project/i18n/sale_purchase_project.pot`
- `addons/sale_purchase_project/i18n/sk.po`
- `addons/sale_purchase_project/i18n/sl.po`
- `addons/sale_purchase_project/i18n/sr@latin.po`
- `addons/sale_purchase_project/i18n/sv.po`
- `addons/sale_purchase_project/i18n/th.po`
- `addons/sale_purchase_project/i18n/tr.po`
- `addons/sale_purchase_project/i18n/uk.po`
- `addons/sale_purchase_project/i18n/uz.po`
- `addons/sale_purchase_project/i18n/vi.po`
- `addons/sale_purchase_project/i18n/zh_CN.po`
- `addons/sale_purchase_project/i18n/zh_TW.po`
- `addons/sale_purchase_project/models/__init__.py`
- `addons/sale_purchase_project/models/account_analytic_line.py`
- `addons/sale_purchase_project/models/sale_order_line.py`
- `addons/sale_purchase_project/tests/__init__.py`
- `addons/sale_purchase_project/tests/test_sale_purchase_project.py`
