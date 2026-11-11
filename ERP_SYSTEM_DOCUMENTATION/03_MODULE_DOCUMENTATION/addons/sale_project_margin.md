# Module: sale_project_margin

- **Module ID:** MOD-525
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_project_margin`
- **Manifest:** `addons/sale_project_margin/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Bridge module between Sales Margin and Project

**Manifest description:**

Allows to compute accurate margin for Service sales.
======================================================

**Scope evidence:** The module contains 56 files, including 4 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `sale_margin`, `sale_project`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 3
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

- **Description:** 1 model declarations, 2 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/sale_project_margin/models/project_project.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 10 record/template/menu identifiers.
- **Evidence:** `addons/sale_project_margin/report/sale_report_views.xml:4`, `addons/sale_project_margin/report/sale_report_views.xml:15`, `addons/sale_project_margin/report/sale_report_views.xml:28`, `addons/sale_project_margin/report/sale_report_views.xml:40`, `addons/sale_project_margin/report/sale_report_views.xml:47`, `addons/sale_project_margin/report/sale_report_views.xml:54`, `addons/sale_project_margin/report/sale_report_views.xml:61`, `addons/sale_project_margin/views/project_menus.xml:3`, `addons/sale_project_margin/views/project_task_views.xml:4`, `addons/sale_project_margin/views/project_task_views.xml:24`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `sale_report_view_graph_project_forecast_margin`, `sale_report_view_pivot_project_forecast_margin`, `action_project_forecast_margin`, `action_project_forecast_margin_view_list`, `action_project_forecast_margin_view_pivot`, `action_project_forecast_margin_view_graph`, `action_project_forecast_margin_view_kanban`, `analytic_projected_margins_menu_project`, `view_edit_project_inherit_form_sale_project_margin`, `project_embedded_action_project_projected_margin`
- Menus: 1; representative evidence: `addons/sale_project_margin/views/project_menus.xml:3`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 12; representative evidence: `addons/sale_project_margin/report/sale_report_views.xml:6`, `addons/sale_project_margin/report/sale_report_views.xml:7`, `addons/sale_project_margin/report/sale_report_views.xml:17`, `addons/sale_project_margin/report/sale_report_views.xml:18`, `addons/sale_project_margin/report/sale_report_views.xml:30`, `addons/sale_project_margin/report/sale_report_views.xml:31`, `addons/sale_project_margin/report/sale_report_views.xml:42`, `addons/sale_project_margin/report/sale_report_views.xml:49`, `addons/sale_project_margin/report/sale_report_views.xml:56`, `addons/sale_project_margin/report/sale_report_views.xml:63`, `addons/sale_project_margin/views/project_task_views.xml:6`, `addons/sale_project_margin/views/project_task_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale_project_margin/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `project.project` (addons/sale_project_margin/models/project_project.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale_margin`, `sale_project`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/sale_project_margin/__init__.py`
- `addons/sale_project_margin/__manifest__.py`
- `addons/sale_project_margin/i18n/ar.po`
- `addons/sale_project_margin/i18n/az.po`
- `addons/sale_project_margin/i18n/bg.po`
- `addons/sale_project_margin/i18n/bs.po`
- `addons/sale_project_margin/i18n/ca.po`
- `addons/sale_project_margin/i18n/cs.po`
- `addons/sale_project_margin/i18n/da.po`
- `addons/sale_project_margin/i18n/de.po`
- `addons/sale_project_margin/i18n/el.po`
- `addons/sale_project_margin/i18n/es.po`
- `addons/sale_project_margin/i18n/es_419.po`
- `addons/sale_project_margin/i18n/et.po`
- `addons/sale_project_margin/i18n/fa.po`
- `addons/sale_project_margin/i18n/fi.po`
- `addons/sale_project_margin/i18n/fr.po`
- `addons/sale_project_margin/i18n/he.po`
- `addons/sale_project_margin/i18n/hi.po`
- `addons/sale_project_margin/i18n/hr.po`
- `addons/sale_project_margin/i18n/hu.po`
- `addons/sale_project_margin/i18n/id.po`
- `addons/sale_project_margin/i18n/it.po`
- `addons/sale_project_margin/i18n/ja.po`
- `addons/sale_project_margin/i18n/kab.po`
- `addons/sale_project_margin/i18n/ko.po`
- `addons/sale_project_margin/i18n/ku.po`
- `addons/sale_project_margin/i18n/lo.po`
- `addons/sale_project_margin/i18n/lt.po`
- `addons/sale_project_margin/i18n/lv.po`
- `addons/sale_project_margin/i18n/mn.po`
- `addons/sale_project_margin/i18n/my.po`
- `addons/sale_project_margin/i18n/nb.po`
- `addons/sale_project_margin/i18n/nl.po`
- `addons/sale_project_margin/i18n/pl.po`
- `addons/sale_project_margin/i18n/pt.po`
- `addons/sale_project_margin/i18n/pt_BR.po`
- `addons/sale_project_margin/i18n/ro.po`
- `addons/sale_project_margin/i18n/ru.po`
- `addons/sale_project_margin/i18n/sale_project_margin.pot`
- `addons/sale_project_margin/i18n/sk.po`
- `addons/sale_project_margin/i18n/sl.po`
- `addons/sale_project_margin/i18n/sr@latin.po`
- `addons/sale_project_margin/i18n/sv.po`
- `addons/sale_project_margin/i18n/th.po`
- `addons/sale_project_margin/i18n/tr.po`
- `addons/sale_project_margin/i18n/uk.po`
- `addons/sale_project_margin/i18n/uz.po`
- `addons/sale_project_margin/i18n/vi.po`
- `addons/sale_project_margin/i18n/zh_CN.po`
- `addons/sale_project_margin/i18n/zh_TW.po`
- `addons/sale_project_margin/models/__init__.py`
- `addons/sale_project_margin/models/project_project.py`
- `addons/sale_project_margin/report/sale_report_views.xml`
- `addons/sale_project_margin/views/project_menus.xml`
- `addons/sale_project_margin/views/project_task_views.xml`
