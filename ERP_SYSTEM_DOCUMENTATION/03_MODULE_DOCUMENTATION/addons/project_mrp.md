# Module: project_mrp

- **Module ID:** MOD-480
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/project_mrp`
- **Manifest:** `addons/project_mrp/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Services/Project`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Monitor MRP using project

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 62 files, including 9 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `mrp`, `project`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 3
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/project_mrp/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 10 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/project_mrp/models/stock.py:6`, `addons/project_mrp/models/stock.py:16`, `addons/project_mrp/models/project_project.py:6`, `addons/project_mrp/models/mrp_production.py:6`, `addons/project_mrp/models/mrp_bom.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 8 record/template/menu identifiers.
- **Evidence:** `addons/project_mrp/views/mrp_bom_views.xml:3`, `addons/project_mrp/views/mrp_production_views.xml:3`, `addons/project_mrp/views/mrp_production_views.xml:14`, `addons/project_mrp/views/project_project_views.xml:3`, `addons/project_mrp/views/project_project_views.xml:21`, `addons/project_mrp/views/project_project_views.xml:31`, `addons/project_mrp/views/project_project_views.xml:41`, `addons/project_mrp/views/project_project_views.xml:51`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/project_mrp/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/project_mrp/tests/test_mto_replenishment.py`, `addons/project_mrp/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `mrp_bom_form_view_inherited_project_mrp`, `view_production_tree_view_inherit_project_mrp`, `mrp_production_form_view_inherit_project_mrp`, `project_view_form_inherit_project_mrp`, `project_embedded_action_bills_of_materials`, `project_embedded_action_bills_of_materials_dashboard`, `project_embedded_action_manufacturing_orders`, `project_embedded_action_manufacturing_orders_dashboard`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 8; representative evidence: `addons/project_mrp/views/mrp_bom_views.xml:5`, `addons/project_mrp/views/mrp_bom_views.xml:7`, `addons/project_mrp/views/mrp_production_views.xml:5`, `addons/project_mrp/views/mrp_production_views.xml:7`, `addons/project_mrp/views/mrp_production_views.xml:16`, `addons/project_mrp/views/mrp_production_views.xml:18`, `addons/project_mrp/views/project_project_views.xml:5`, `addons/project_mrp/views/project_project_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/project_mrp/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `stock.rule` (addons/project_mrp/models/stock.py:6); inherits `stock.move` (addons/project_mrp/models/stock.py:16); inherits `project.project` (addons/project_mrp/models/project_project.py:6); inherits `mrp.production` (addons/project_mrp/models/mrp_production.py:6); inherits `mrp.bom` (addons/project_mrp/models/mrp_bom.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mrp`, `project`
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

- `addons/project_mrp/__init__.py`
- `addons/project_mrp/__manifest__.py`
- `addons/project_mrp/i18n/ar.po`
- `addons/project_mrp/i18n/az.po`
- `addons/project_mrp/i18n/bg.po`
- `addons/project_mrp/i18n/bs.po`
- `addons/project_mrp/i18n/ca.po`
- `addons/project_mrp/i18n/cs.po`
- `addons/project_mrp/i18n/da.po`
- `addons/project_mrp/i18n/de.po`
- `addons/project_mrp/i18n/el.po`
- `addons/project_mrp/i18n/es.po`
- `addons/project_mrp/i18n/es_419.po`
- `addons/project_mrp/i18n/et.po`
- `addons/project_mrp/i18n/fa.po`
- `addons/project_mrp/i18n/fi.po`
- `addons/project_mrp/i18n/fr.po`
- `addons/project_mrp/i18n/he.po`
- `addons/project_mrp/i18n/hi.po`
- `addons/project_mrp/i18n/hr.po`
- `addons/project_mrp/i18n/hu.po`
- `addons/project_mrp/i18n/id.po`
- `addons/project_mrp/i18n/it.po`
- `addons/project_mrp/i18n/ja.po`
- `addons/project_mrp/i18n/kab.po`
- `addons/project_mrp/i18n/ko.po`
- `addons/project_mrp/i18n/ku.po`
- `addons/project_mrp/i18n/lo.po`
- `addons/project_mrp/i18n/lt.po`
- `addons/project_mrp/i18n/lv.po`
- `addons/project_mrp/i18n/mn.po`
- `addons/project_mrp/i18n/my.po`
- `addons/project_mrp/i18n/nb.po`
- `addons/project_mrp/i18n/nl.po`
- `addons/project_mrp/i18n/pl.po`
- `addons/project_mrp/i18n/project_mrp.pot`
- `addons/project_mrp/i18n/pt.po`
- `addons/project_mrp/i18n/pt_BR.po`
- `addons/project_mrp/i18n/ro.po`
- `addons/project_mrp/i18n/ru.po`
- `addons/project_mrp/i18n/sk.po`
- `addons/project_mrp/i18n/sl.po`
- `addons/project_mrp/i18n/sr@latin.po`
- `addons/project_mrp/i18n/sv.po`
- `addons/project_mrp/i18n/th.po`
- `addons/project_mrp/i18n/tr.po`
- `addons/project_mrp/i18n/uk.po`
- `addons/project_mrp/i18n/uz.po`
- `addons/project_mrp/i18n/vi.po`
- `addons/project_mrp/i18n/zh_CN.po`
- `addons/project_mrp/i18n/zh_TW.po`
- `addons/project_mrp/models/__init__.py`
- `addons/project_mrp/models/mrp_bom.py`
- `addons/project_mrp/models/mrp_production.py`
- `addons/project_mrp/models/project_project.py`
- `addons/project_mrp/models/stock.py`
- `addons/project_mrp/security/ir.access.csv`
- `addons/project_mrp/tests/__init__.py`
- `addons/project_mrp/tests/test_mto_replenishment.py`
- `addons/project_mrp/views/mrp_bom_views.xml`
- `addons/project_mrp/views/mrp_production_views.xml`
- `addons/project_mrp/views/project_project_views.xml`
