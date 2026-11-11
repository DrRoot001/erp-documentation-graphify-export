# Module: project_hr_expense

- **Module ID:** MOD-477
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/project_hr_expense`
- **Manifest:** `addons/project_hr_expense/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Services/expenses`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Project expenses

**Manifest description:**

Bridge created to add the number of expenses linked to an AA to a project form

**Scope evidence:** The module contains 58 files, including 7 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `project_account`, `hr_expense`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 2
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

- **Description:** 2 model declarations, 7 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/project_hr_expense/models/hr_expense.py:4`, `addons/project_hr_expense/models/project_project.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/project_hr_expense/data/project_hr_expense_demo.xml:4`, `addons/project_hr_expense/data/project_hr_expense_demo.xml:7`, `addons/project_hr_expense/data/project_hr_expense_demo.xml:10`, `addons/project_hr_expense/data/project_hr_expense_demo.xml:19`, `addons/project_hr_expense/views/project_project_views.xml:3`, `addons/project_hr_expense/views/project_project_views.xml:13`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/project_hr_expense/tests/test_analytics.py`, `addons/project_hr_expense/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `hr_expense.travel_admin_by_car_expense`, `hr_expense.travel_demo_by_car_expense`, `transportation_expense`, `restaurant_expense`, `project_embedded_action_hr_expenses`, `project_embedded_action_hr_expenses_dashbord`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/project_hr_expense/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `hr.expense` (addons/project_hr_expense/models/hr_expense.py:4); inherits `project.project` (addons/project_hr_expense/models/project_project.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `project_account`, `hr_expense`
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

- `addons/project_hr_expense/__init__.py`
- `addons/project_hr_expense/__manifest__.py`
- `addons/project_hr_expense/data/project_hr_expense_demo.xml`
- `addons/project_hr_expense/i18n/ar.po`
- `addons/project_hr_expense/i18n/az.po`
- `addons/project_hr_expense/i18n/bg.po`
- `addons/project_hr_expense/i18n/bs.po`
- `addons/project_hr_expense/i18n/ca.po`
- `addons/project_hr_expense/i18n/cs.po`
- `addons/project_hr_expense/i18n/da.po`
- `addons/project_hr_expense/i18n/de.po`
- `addons/project_hr_expense/i18n/el.po`
- `addons/project_hr_expense/i18n/es.po`
- `addons/project_hr_expense/i18n/es_419.po`
- `addons/project_hr_expense/i18n/et.po`
- `addons/project_hr_expense/i18n/fa.po`
- `addons/project_hr_expense/i18n/fi.po`
- `addons/project_hr_expense/i18n/fr.po`
- `addons/project_hr_expense/i18n/he.po`
- `addons/project_hr_expense/i18n/hi.po`
- `addons/project_hr_expense/i18n/hr.po`
- `addons/project_hr_expense/i18n/hu.po`
- `addons/project_hr_expense/i18n/id.po`
- `addons/project_hr_expense/i18n/it.po`
- `addons/project_hr_expense/i18n/ja.po`
- `addons/project_hr_expense/i18n/kab.po`
- `addons/project_hr_expense/i18n/ko.po`
- `addons/project_hr_expense/i18n/ku.po`
- `addons/project_hr_expense/i18n/lo.po`
- `addons/project_hr_expense/i18n/lt.po`
- `addons/project_hr_expense/i18n/lv.po`
- `addons/project_hr_expense/i18n/mn.po`
- `addons/project_hr_expense/i18n/my.po`
- `addons/project_hr_expense/i18n/nb.po`
- `addons/project_hr_expense/i18n/nl.po`
- `addons/project_hr_expense/i18n/pl.po`
- `addons/project_hr_expense/i18n/project_hr_expense.pot`
- `addons/project_hr_expense/i18n/pt.po`
- `addons/project_hr_expense/i18n/pt_BR.po`
- `addons/project_hr_expense/i18n/ro.po`
- `addons/project_hr_expense/i18n/ru.po`
- `addons/project_hr_expense/i18n/sk.po`
- `addons/project_hr_expense/i18n/sl.po`
- `addons/project_hr_expense/i18n/sr@latin.po`
- `addons/project_hr_expense/i18n/sv.po`
- `addons/project_hr_expense/i18n/th.po`
- `addons/project_hr_expense/i18n/tr.po`
- `addons/project_hr_expense/i18n/uk.po`
- `addons/project_hr_expense/i18n/uz.po`
- `addons/project_hr_expense/i18n/vi.po`
- `addons/project_hr_expense/i18n/zh_CN.po`
- `addons/project_hr_expense/i18n/zh_TW.po`
- `addons/project_hr_expense/models/__init__.py`
- `addons/project_hr_expense/models/hr_expense.py`
- `addons/project_hr_expense/models/project_project.py`
- `addons/project_hr_expense/tests/__init__.py`
- `addons/project_hr_expense/tests/test_analytics.py`
- `addons/project_hr_expense/views/project_project_views.xml`
