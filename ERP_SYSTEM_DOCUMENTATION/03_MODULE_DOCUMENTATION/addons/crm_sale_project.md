# Module: crm_sale_project

- **Module ID:** MOD-059
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/crm_sale_project`
- **Manifest:** `addons/crm_sale_project/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/CRM`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Project Generation from Opportunities

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 63 files, including 10 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `sale_project`, `crm`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 15 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/crm_sale_project/models/sale_order.py:4`, `addons/crm_sale_project/models/project_project.py:4`, `addons/crm_sale_project/models/crm_lead.py:4`, `addons/crm_sale_project/wizard/project_template_create_wizard.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 4 record/template/menu identifiers.
- **Evidence:** `addons/crm_sale_project/wizard/project_template_create_wizard.xml:4`, `addons/crm_sale_project/data/ir_actions_server_data.xml:5`, `addons/crm_sale_project/views/crm_lead_views.xml:5`, `addons/crm_sale_project/views/project_project_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/crm_sale_project/data/ir_actions_server_data.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/crm_sale_project/tests/test_crm_sale_project.py`, `addons/crm_sale_project/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `crm_project_view_form_simplified_template`, `action_create_project_crm_lead`, `crm_lead_view_form`, `view_edit_project_inherit_form_crm_project`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/crm_sale_project/wizard/project_template_create_wizard.xml:6`, `addons/crm_sale_project/wizard/project_template_create_wizard.xml:9`, `addons/crm_sale_project/views/crm_lead_views.xml:7`, `addons/crm_sale_project/views/crm_lead_views.xml:9`, `addons/crm_sale_project/views/project_project_views.xml:6`, `addons/crm_sale_project/views/project_project_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/crm_sale_project/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/crm_sale_project/data/ir_actions_server_data.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `sale.order` (addons/crm_sale_project/models/sale_order.py:4); inherits `project.project` (addons/crm_sale_project/models/project_project.py:4); inherits `crm.lead` (addons/crm_sale_project/models/crm_lead.py:4); inherits `project.template.create.wizard` (addons/crm_sale_project/wizard/project_template_create_wizard.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale_project`, `crm`
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

- `addons/crm_sale_project/__init__.py`
- `addons/crm_sale_project/__manifest__.py`
- `addons/crm_sale_project/data/ir_actions_server_data.xml`
- `addons/crm_sale_project/i18n/ar.po`
- `addons/crm_sale_project/i18n/az.po`
- `addons/crm_sale_project/i18n/bg.po`
- `addons/crm_sale_project/i18n/bs.po`
- `addons/crm_sale_project/i18n/ca.po`
- `addons/crm_sale_project/i18n/crm_sale_project.pot`
- `addons/crm_sale_project/i18n/cs.po`
- `addons/crm_sale_project/i18n/da.po`
- `addons/crm_sale_project/i18n/de.po`
- `addons/crm_sale_project/i18n/el.po`
- `addons/crm_sale_project/i18n/es.po`
- `addons/crm_sale_project/i18n/es_419.po`
- `addons/crm_sale_project/i18n/et.po`
- `addons/crm_sale_project/i18n/fa.po`
- `addons/crm_sale_project/i18n/fi.po`
- `addons/crm_sale_project/i18n/fr.po`
- `addons/crm_sale_project/i18n/he.po`
- `addons/crm_sale_project/i18n/hi.po`
- `addons/crm_sale_project/i18n/hr.po`
- `addons/crm_sale_project/i18n/hu.po`
- `addons/crm_sale_project/i18n/id.po`
- `addons/crm_sale_project/i18n/it.po`
- `addons/crm_sale_project/i18n/ja.po`
- `addons/crm_sale_project/i18n/kab.po`
- `addons/crm_sale_project/i18n/ko.po`
- `addons/crm_sale_project/i18n/ku.po`
- `addons/crm_sale_project/i18n/lo.po`
- `addons/crm_sale_project/i18n/lt.po`
- `addons/crm_sale_project/i18n/lv.po`
- `addons/crm_sale_project/i18n/mn.po`
- `addons/crm_sale_project/i18n/my.po`
- `addons/crm_sale_project/i18n/nb.po`
- `addons/crm_sale_project/i18n/nl.po`
- `addons/crm_sale_project/i18n/pl.po`
- `addons/crm_sale_project/i18n/pt.po`
- `addons/crm_sale_project/i18n/pt_BR.po`
- `addons/crm_sale_project/i18n/ro.po`
- `addons/crm_sale_project/i18n/ru.po`
- `addons/crm_sale_project/i18n/sk.po`
- `addons/crm_sale_project/i18n/sl.po`
- `addons/crm_sale_project/i18n/sr@latin.po`
- `addons/crm_sale_project/i18n/sv.po`
- `addons/crm_sale_project/i18n/th.po`
- `addons/crm_sale_project/i18n/tr.po`
- `addons/crm_sale_project/i18n/uk.po`
- `addons/crm_sale_project/i18n/uz.po`
- `addons/crm_sale_project/i18n/vi.po`
- `addons/crm_sale_project/i18n/zh_CN.po`
- `addons/crm_sale_project/i18n/zh_TW.po`
- `addons/crm_sale_project/models/__init__.py`
- `addons/crm_sale_project/models/crm_lead.py`
- `addons/crm_sale_project/models/project_project.py`
- `addons/crm_sale_project/models/sale_order.py`
- `addons/crm_sale_project/tests/__init__.py`
- `addons/crm_sale_project/tests/test_crm_sale_project.py`
- `addons/crm_sale_project/views/crm_lead_views.xml`
- `addons/crm_sale_project/views/project_project_views.xml`
- `addons/crm_sale_project/wizard/__init__.py`
- `addons/crm_sale_project/wizard/project_template_create_wizard.py`
- `addons/crm_sale_project/wizard/project_template_create_wizard.xml`
