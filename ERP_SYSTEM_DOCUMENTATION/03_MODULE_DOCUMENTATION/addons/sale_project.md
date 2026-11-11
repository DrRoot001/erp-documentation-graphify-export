# Module: sale_project

- **Module ID:** MOD-524
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_project`
- **Manifest:** `addons/sale_project/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Task Generation from Sales Orders

**Manifest description:**

Allows to create task from your sales order
=============================================
This module allows to generate a project/task from sales orders.

**Scope evidence:** The module contains 108 files, including 32 Python, 16 XML, and 9 JavaScript/TypeScript files. The manifest declares dependencies: `sale_management`, `sale_service`, `project_account`.

## 2. Module structure

- Model/business logic files: 15
- Controller/API files: 2
- XML/data/view/template files: 16
- Browser asset files: 9
- Security files: 1
- Test files: 10
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/sale_project/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 15 model declarations, 292 methods, 2 constraint handlers, 8 onchange handlers, and 30 dependency declarations.
- **Evidence:** `addons/sale_project/models/sale_order.py:12`, `addons/sale_project/models/product_product.py:6`, `addons/sale_project/models/sale_order_template_line.py:7`, `addons/sale_project/models/product_template.py:7`, `addons/sale_project/models/project_task_recurrence.py:6`, `addons/sale_project/models/account_analytic_line.py:15`, `addons/sale_project/models/project_task.py:11`, `addons/sale_project/models/project_project.py:13`, `addons/sale_project/models/project_task_type.py:4`, `addons/sale_project/models/project_milestone.py:7`, `addons/sale_project/models/account_move_line.py:9`, `addons/sale_project/models/sale_order_line.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/sale_project/controllers/portal.py`, `addons/sale_project/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 16 XML files and 9 JavaScript/TypeScript files; static XML analysis found 93 record/template/menu identifiers.
- **Evidence:** `addons/sale_project/report/account_analytic_line_views.xml:3`, `addons/sale_project/report/account_analytic_line_views.xml:19`, `addons/sale_project/report/account_analytic_line_views.xml:33`, `addons/sale_project/report/account_analytic_line_views.xml:47`, `addons/sale_project/report/account_analytic_line_views.xml:60`, `addons/sale_project/report/account_analytic_line_views.xml:73`, `addons/sale_project/report/account_analytic_line_views.xml:85`, `addons/sale_project/report/account_analytic_line_views.xml:98`, `addons/sale_project/report/account_analytic_line_views.xml:110`, `addons/sale_project/report/account_analytic_line_views.xml:117`, `addons/sale_project/report/account_analytic_line_views.xml:124`, `addons/sale_project/report/account_analytic_line_views.xml:131`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/sale_project/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/sale_project/views/sale_order_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 10 test files are present.
- **Evidence:** `addons/sale_project/tests/test_analytic_distribution.py`, `addons/sale_project/tests/test_child_tasks.py`, `addons/sale_project/tests/test_reinvoice.py`, `addons/sale_project/tests/test_so_line_milestones.py`, `addons/sale_project/tests/test_sale_project.py`, `addons/sale_project/tests/test_sale_project_multicompany_access.py`, `addons/sale_project/tests/common.py`, `addons/sale_project/tests/test_project_project.py`, `addons/sale_project/tests/test_sale_warning.py`, `addons/sale_project/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 16; representative identifiers: `view_account_analytic_line_inherit_sale_project_pivot`, `view_account_analytic_line_inherit_sale_project_pivot_single`, `view_account_analytic_line_inherit_sale_project_tree`, `account_analytic_line_view_list_margins_no_group`, `account_analytic_line_view_graph_project_margin`, `account_analytic_line_view_graph_for_single_project`, `sale_project_line_search`, `action_analytic_reporting_inherit_sale_project`, `action_view_analytic_reporting_inherit_sale_project_pivot`, `action_view_analytic_reporting_inherit_sale_project_graph`, `action_view_analytic_reporting_inherit_sale_project_tree`, `action_view_analytic_reporting_inherit_sale_project_kanban`, `sale_report_view_search`, `project_project_view_form_simplified_template`, `sale_project_view_form_simplified_template`, `project_task_export_template_line_sale_line_id`, `services_template_export_template`, `services_template_export_template_line_id`, `services_template_export_template_line_name`, `services_template_export_template_line_product_tag_ids`
- Menus: 1; representative evidence: `addons/sale_project/views/project_menus.xml:3`
- Templates: 2; representative evidence: `addons/sale_project/views/project_update_template.xml:4`, `addons/sale_project/views/sale_project_portal_templates.xml:4`
- View/action field declarations: 78; representative evidence: `addons/sale_project/report/account_analytic_line_views.xml:5`, `addons/sale_project/report/account_analytic_line_views.xml:8`, `addons/sale_project/report/account_analytic_line_views.xml:21`, `addons/sale_project/report/account_analytic_line_views.xml:24`, `addons/sale_project/report/account_analytic_line_views.xml:35`, `addons/sale_project/report/account_analytic_line_views.xml:38`, `addons/sale_project/report/account_analytic_line_views.xml:49`, `addons/sale_project/report/account_analytic_line_views.xml:53`, `addons/sale_project/report/account_analytic_line_views.xml:62`, `addons/sale_project/report/account_analytic_line_views.xml:66`, `addons/sale_project/report/account_analytic_line_views.xml:75`, `addons/sale_project/report/account_analytic_line_views.xml:78`
- Browser assets: 9; representative files: `addons/sale_project/static/tests/project_task_list_sale_line.test.js`, `addons/sale_project/static/tests/so_line_create_button.test.js`, `addons/sale_project/static/tests/project_milestone_form_view.test.js`, `addons/sale_project/static/tests/project_task_model.js`, `addons/sale_project/static/src/fields/costs_percent_pie/costs_percent_pie.js`, `addons/sale_project/static/src/views/project_form/project_project_form_controller.js`, `addons/sale_project/static/src/views/project_task_list/project_task_list_sale_line.js`, `addons/sale_project/static/tests/tours/project_create_sol_tour.js`, `addons/sale_project/static/tests/tours/project_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale_project/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/sale_project/views/sale_order_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 15
- Representative model evidence: inherits `sale.order` (addons/sale_project/models/sale_order.py:12); inherits `product.product` (addons/sale_project/models/product_product.py:6); inherits `sale.order.template.line` (addons/sale_project/models/sale_order_template_line.py:7); inherits `product.template` (addons/sale_project/models/product_template.py:7); inherits `project.task.recurrence` (addons/sale_project/models/project_task_recurrence.py:6); inherits `account.analytic.line` (addons/sale_project/models/account_analytic_line.py:15); inherits `project.task` (addons/sale_project/models/project_task.py:11); inherits `project.project` (addons/sale_project/models/project_project.py:13); inherits `project.task.type` (addons/sale_project/models/project_task_type.py:4); inherits `project.milestone` (addons/sale_project/models/project_milestone.py:7); inherits `account.move.line` (addons/sale_project/models/account_move_line.py:9); inherits `sale.order.line` (addons/sale_project/models/sale_order_line.py:8); inherits `report.project.task.user` (addons/sale_project/report/project_report.py:7); inherits `sale.report` (addons/sale_project/report/sale_report.py:6); inherits `project.template.create.wizard` (addons/sale_project/wizard/project_template_create_wizard.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale_management`, `sale_service`, `project_account`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/sale_project/__init__.py`
- `addons/sale_project/__manifest__.py`
- `addons/sale_project/controllers/__init__.py`
- `addons/sale_project/controllers/portal.py`
- `addons/sale_project/data/sale_project_data.xml`
- `addons/sale_project/data/sale_project_demo.xml`
- `addons/sale_project/i18n/ar.po`
- `addons/sale_project/i18n/az.po`
- `addons/sale_project/i18n/bg.po`
- `addons/sale_project/i18n/bs.po`
- `addons/sale_project/i18n/ca.po`
- `addons/sale_project/i18n/cs.po`
- `addons/sale_project/i18n/da.po`
- `addons/sale_project/i18n/de.po`
- `addons/sale_project/i18n/el.po`
- `addons/sale_project/i18n/es.po`
- `addons/sale_project/i18n/es_419.po`
- `addons/sale_project/i18n/et.po`
- `addons/sale_project/i18n/fa.po`
- `addons/sale_project/i18n/fi.po`
- `addons/sale_project/i18n/fr.po`
- `addons/sale_project/i18n/he.po`
- `addons/sale_project/i18n/hi.po`
- `addons/sale_project/i18n/hr.po`
- `addons/sale_project/i18n/hu.po`
- `addons/sale_project/i18n/id.po`
- `addons/sale_project/i18n/it.po`
- `addons/sale_project/i18n/ja.po`
- `addons/sale_project/i18n/kab.po`
- `addons/sale_project/i18n/ko.po`
- `addons/sale_project/i18n/ku.po`
- `addons/sale_project/i18n/lo.po`
- `addons/sale_project/i18n/lt.po`
- `addons/sale_project/i18n/lv.po`
- `addons/sale_project/i18n/mn.po`
- `addons/sale_project/i18n/my.po`
- `addons/sale_project/i18n/nb.po`
- `addons/sale_project/i18n/nl.po`
- `addons/sale_project/i18n/pl.po`
- `addons/sale_project/i18n/pt.po`
- `addons/sale_project/i18n/pt_BR.po`
- `addons/sale_project/i18n/ro.po`
- `addons/sale_project/i18n/ru.po`
- `addons/sale_project/i18n/sale_project.pot`
- `addons/sale_project/i18n/sk.po`
- `addons/sale_project/i18n/sl.po`
- `addons/sale_project/i18n/sr@latin.po`
- `addons/sale_project/i18n/sv.po`
- `addons/sale_project/i18n/th.po`
- `addons/sale_project/i18n/tr.po`
- `addons/sale_project/i18n/uk.po`
- `addons/sale_project/i18n/uz.po`
- `addons/sale_project/i18n/vi.po`
- `addons/sale_project/i18n/zh_CN.po`
- `addons/sale_project/i18n/zh_TW.po`
- `addons/sale_project/models/__init__.py`
- `addons/sale_project/models/account_analytic_line.py`
- `addons/sale_project/models/account_move_line.py`
- `addons/sale_project/models/product_product.py`
- `addons/sale_project/models/product_template.py`
- `addons/sale_project/models/project_milestone.py`
- `addons/sale_project/models/project_project.py`
- `addons/sale_project/models/project_task.py`
- `addons/sale_project/models/project_task_recurrence.py`
- `addons/sale_project/models/project_task_type.py`
- `addons/sale_project/models/sale_order.py`
- `addons/sale_project/models/sale_order_line.py`
- `addons/sale_project/models/sale_order_template_line.py`
- `addons/sale_project/report/__init__.py`
- `addons/sale_project/report/account_analytic_line_views.xml`
- `addons/sale_project/report/project_report.py`
- `addons/sale_project/report/sale_report.py`
- `addons/sale_project/report/sale_report_views.xml`
- `addons/sale_project/security/ir.access.csv`
- `addons/sale_project/static/src/core/bottom_sheet/bottom_sheet.scss`
- `addons/sale_project/static/src/fields/costs_percent_pie/costs_percent_pie.js`
- `addons/sale_project/static/src/fields/costs_percent_pie/costs_percent_pie.xml`
- `addons/sale_project/static/src/views/project_form/project_project_form_controller.js`
- `addons/sale_project/static/src/views/project_task_list/project_task_list_sale_line.js`
- `addons/sale_project/static/tests/project_milestone_form_view.test.js`
- `addons/sale_project/static/tests/project_task_list_sale_line.test.js`
- `addons/sale_project/static/tests/project_task_model.js`
- `addons/sale_project/static/tests/so_line_create_button.test.js`
- `addons/sale_project/static/tests/tours/project_create_sol_tour.js`
- `addons/sale_project/static/tests/tours/project_tour.js`
- `addons/sale_project/tests/__init__.py`
- `addons/sale_project/tests/common.py`
- `addons/sale_project/tests/test_analytic_distribution.py`
- `addons/sale_project/tests/test_child_tasks.py`
- `addons/sale_project/tests/test_project_project.py`
- `addons/sale_project/tests/test_reinvoice.py`
- `addons/sale_project/tests/test_sale_project.py`
- `addons/sale_project/tests/test_sale_project_multicompany_access.py`
- `addons/sale_project/tests/test_sale_warning.py`
- `addons/sale_project/tests/test_so_line_milestones.py`
- `addons/sale_project/views/product_views.xml`
- `addons/sale_project/views/project_menus.xml`
- `addons/sale_project/views/project_sharing_views.xml`
- `addons/sale_project/views/project_task_type_views.xml`
- `addons/sale_project/views/project_task_views.xml`
- `addons/sale_project/views/project_update_template.xml`
- `addons/sale_project/views/project_views.xml`
- `addons/sale_project/views/sale_order_line_views.xml`
- `addons/sale_project/views/sale_order_views.xml`
- `addons/sale_project/views/sale_project_portal_templates.xml`
- `addons/sale_project/wizard/__init__.py`
- `addons/sale_project/wizard/project_template_create_wizard.py`
- `addons/sale_project/wizard/project_template_create_wizard.xml`
