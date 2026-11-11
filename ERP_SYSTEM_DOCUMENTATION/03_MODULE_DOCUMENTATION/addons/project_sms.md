# Module: project_sms

- **Module ID:** MOD-487
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/project_sms`
- **Manifest:** `addons/project_sms/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Services/Project`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Send text messages when project/task stage move

**Manifest description:**

Send text messages when project/task stage move

**Scope evidence:** The module contains 64 files, including 10 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `project`, `sms`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/project_sms/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 9 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/project_sms/models/project_stage.py:7`, `addons/project_sms/models/project_task.py:7`, `addons/project_sms/models/project_project.py:7`, `addons/project_sms/models/project_task_type.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 8 record/template/menu identifiers.
- **Evidence:** `addons/project_sms/views/project_task_type_views.xml:3`, `addons/project_sms/views/project_task_type_views.xml:15`, `addons/project_sms/views/project_task_type_views.xml:26`, `addons/project_sms/views/project_stage_views.xml:3`, `addons/project_sms/views/project_stage_views.xml:14`, `addons/project_sms/views/project_stage_views.xml:26`, `addons/project_sms/views/project_task_views.xml:3`, `addons/project_sms/views/project_project_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/project_sms/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/project_sms/tests/test_project_sharing.py`, `addons/project_sms/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `task_type_edit_view_form_inherit_project_sms`, `task_type_edit_view_tree_inherit_project_sms`, `task_type_search_view_search_inherit_project_sms`, `project_project_stage_view_tree_inherit_project_sms`, `project_project_stage_view_form_inherit_project_sms`, `project_project_stage_view_search_inherit_project_sms`, `project_task_act_window_sms_composer`, `project_project_act_window_sms_composer`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 16; representative evidence: `addons/project_sms/views/project_task_type_views.xml:5`, `addons/project_sms/views/project_task_type_views.xml:7`, `addons/project_sms/views/project_task_type_views.xml:17`, `addons/project_sms/views/project_task_type_views.xml:19`, `addons/project_sms/views/project_task_type_views.xml:28`, `addons/project_sms/views/project_task_type_views.xml:30`, `addons/project_sms/views/project_stage_views.xml:5`, `addons/project_sms/views/project_stage_views.xml:7`, `addons/project_sms/views/project_stage_views.xml:16`, `addons/project_sms/views/project_stage_views.xml:18`, `addons/project_sms/views/project_stage_views.xml:28`, `addons/project_sms/views/project_stage_views.xml:30`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/project_sms/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `project.project.stage` (addons/project_sms/models/project_stage.py:7); inherits `project.task` (addons/project_sms/models/project_task.py:7); inherits `project.project` (addons/project_sms/models/project_project.py:7); inherits `project.task.type` (addons/project_sms/models/project_task_type.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `project`, `sms`
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

- `addons/project_sms/__init__.py`
- `addons/project_sms/__manifest__.py`
- `addons/project_sms/i18n/ar.po`
- `addons/project_sms/i18n/az.po`
- `addons/project_sms/i18n/bg.po`
- `addons/project_sms/i18n/bs.po`
- `addons/project_sms/i18n/ca.po`
- `addons/project_sms/i18n/cs.po`
- `addons/project_sms/i18n/da.po`
- `addons/project_sms/i18n/de.po`
- `addons/project_sms/i18n/el.po`
- `addons/project_sms/i18n/es.po`
- `addons/project_sms/i18n/es_419.po`
- `addons/project_sms/i18n/et.po`
- `addons/project_sms/i18n/fa.po`
- `addons/project_sms/i18n/fi.po`
- `addons/project_sms/i18n/fr.po`
- `addons/project_sms/i18n/he.po`
- `addons/project_sms/i18n/hi.po`
- `addons/project_sms/i18n/hr.po`
- `addons/project_sms/i18n/hu.po`
- `addons/project_sms/i18n/id.po`
- `addons/project_sms/i18n/it.po`
- `addons/project_sms/i18n/ja.po`
- `addons/project_sms/i18n/kab.po`
- `addons/project_sms/i18n/ko.po`
- `addons/project_sms/i18n/ku.po`
- `addons/project_sms/i18n/lo.po`
- `addons/project_sms/i18n/lt.po`
- `addons/project_sms/i18n/lv.po`
- `addons/project_sms/i18n/mn.po`
- `addons/project_sms/i18n/my.po`
- `addons/project_sms/i18n/nb.po`
- `addons/project_sms/i18n/nl.po`
- `addons/project_sms/i18n/pl.po`
- `addons/project_sms/i18n/project_sms.pot`
- `addons/project_sms/i18n/pt.po`
- `addons/project_sms/i18n/pt_BR.po`
- `addons/project_sms/i18n/ro.po`
- `addons/project_sms/i18n/ru.po`
- `addons/project_sms/i18n/sk.po`
- `addons/project_sms/i18n/sl.po`
- `addons/project_sms/i18n/sr@latin.po`
- `addons/project_sms/i18n/sv.po`
- `addons/project_sms/i18n/th.po`
- `addons/project_sms/i18n/tr.po`
- `addons/project_sms/i18n/uk.po`
- `addons/project_sms/i18n/uz.po`
- `addons/project_sms/i18n/vi.po`
- `addons/project_sms/i18n/zh_CN.po`
- `addons/project_sms/i18n/zh_TW.po`
- `addons/project_sms/models/__init__.py`
- `addons/project_sms/models/project_project.py`
- `addons/project_sms/models/project_stage.py`
- `addons/project_sms/models/project_task.py`
- `addons/project_sms/models/project_task_type.py`
- `addons/project_sms/security/ir.access.csv`
- `addons/project_sms/tests/__init__.py`
- `addons/project_sms/tests/test_project_sharing.py`
- `addons/project_sms/upgrades/1.1/pre-migrate.py`
- `addons/project_sms/views/project_project_views.xml`
- `addons/project_sms/views/project_stage_views.xml`
- `addons/project_sms/views/project_task_type_views.xml`
- `addons/project_sms/views/project_task_views.xml`
