# Module: web_hierarchy

- **Module ID:** MOD-593
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/web_hierarchy`
- **Manifest:** `addons/web_hierarchy/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Odoo Web Hierarchy view
=======================

This module adds a new view called to be able to define a view to display
an organization such as an Organization Chart for employees for instance.

**Scope evidence:** The module contains 72 files, including 6 Python, 3 XML, and 10 JavaScript/TypeScript files. The manifest declares dependencies: `web`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 3
- Browser asset files: 10
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 4 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/web_hierarchy/models/ir_ui_view.py:24`, `addons/web_hierarchy/models/ir_actions.py:6`, `addons/web_hierarchy/models/models.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 10 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 10; representative files: `addons/web_hierarchy/static/src/hierarchy_view.js`, `addons/web_hierarchy/static/src/hierarchy_arch_parser.js`, `addons/web_hierarchy/static/src/hierarchy_compiler.js`, `addons/web_hierarchy/static/src/hierarchy_controller.js`, `addons/web_hierarchy/static/src/hierarchy_node_draggable.js`, `addons/web_hierarchy/static/src/hierarchy_card.js`, `addons/web_hierarchy/static/src/hierarchy_model.js`, `addons/web_hierarchy/static/src/hierarchy_renderer.js`, `addons/web_hierarchy/static/tests/hierarchy_mock_server.js`, `addons/web_hierarchy/static/tests/hierarchy_view.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/web_hierarchy/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `ir.ui.view` (addons/web_hierarchy/models/ir_ui_view.py:24); inherits `ir.actions.act_window.view` (addons/web_hierarchy/models/ir_actions.py:6); inherits `base` (addons/web_hierarchy/models/models.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `web`
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

- `addons/web_hierarchy/__init__.py`
- `addons/web_hierarchy/__manifest__.py`
- `addons/web_hierarchy/i18n/ar.po`
- `addons/web_hierarchy/i18n/az.po`
- `addons/web_hierarchy/i18n/bg.po`
- `addons/web_hierarchy/i18n/bs.po`
- `addons/web_hierarchy/i18n/ca.po`
- `addons/web_hierarchy/i18n/cs.po`
- `addons/web_hierarchy/i18n/da.po`
- `addons/web_hierarchy/i18n/de.po`
- `addons/web_hierarchy/i18n/el.po`
- `addons/web_hierarchy/i18n/es.po`
- `addons/web_hierarchy/i18n/es_419.po`
- `addons/web_hierarchy/i18n/et.po`
- `addons/web_hierarchy/i18n/fa.po`
- `addons/web_hierarchy/i18n/fi.po`
- `addons/web_hierarchy/i18n/fr.po`
- `addons/web_hierarchy/i18n/he.po`
- `addons/web_hierarchy/i18n/hi.po`
- `addons/web_hierarchy/i18n/hr.po`
- `addons/web_hierarchy/i18n/hu.po`
- `addons/web_hierarchy/i18n/id.po`
- `addons/web_hierarchy/i18n/it.po`
- `addons/web_hierarchy/i18n/ja.po`
- `addons/web_hierarchy/i18n/kab.po`
- `addons/web_hierarchy/i18n/ko.po`
- `addons/web_hierarchy/i18n/ku.po`
- `addons/web_hierarchy/i18n/lo.po`
- `addons/web_hierarchy/i18n/lt.po`
- `addons/web_hierarchy/i18n/lv.po`
- `addons/web_hierarchy/i18n/mn.po`
- `addons/web_hierarchy/i18n/my.po`
- `addons/web_hierarchy/i18n/nb.po`
- `addons/web_hierarchy/i18n/nl.po`
- `addons/web_hierarchy/i18n/pl.po`
- `addons/web_hierarchy/i18n/pt.po`
- `addons/web_hierarchy/i18n/pt_BR.po`
- `addons/web_hierarchy/i18n/ro.po`
- `addons/web_hierarchy/i18n/ru.po`
- `addons/web_hierarchy/i18n/sk.po`
- `addons/web_hierarchy/i18n/sl.po`
- `addons/web_hierarchy/i18n/sr@latin.po`
- `addons/web_hierarchy/i18n/sv.po`
- `addons/web_hierarchy/i18n/th.po`
- `addons/web_hierarchy/i18n/tr.po`
- `addons/web_hierarchy/i18n/uk.po`
- `addons/web_hierarchy/i18n/uz.po`
- `addons/web_hierarchy/i18n/vi.po`
- `addons/web_hierarchy/i18n/web_hierarchy.pot`
- `addons/web_hierarchy/i18n/zh_CN.po`
- `addons/web_hierarchy/i18n/zh_TW.po`
- `addons/web_hierarchy/models/__init__.py`
- `addons/web_hierarchy/models/ir_actions.py`
- `addons/web_hierarchy/models/ir_ui_view.py`
- `addons/web_hierarchy/models/models.py`
- `addons/web_hierarchy/static/src/hierarchy.variables.dark.scss`
- `addons/web_hierarchy/static/src/hierarchy.variables.scss`
- `addons/web_hierarchy/static/src/hierarchy_arch_parser.js`
- `addons/web_hierarchy/static/src/hierarchy_card.js`
- `addons/web_hierarchy/static/src/hierarchy_card.scss`
- `addons/web_hierarchy/static/src/hierarchy_card.xml`
- `addons/web_hierarchy/static/src/hierarchy_compiler.js`
- `addons/web_hierarchy/static/src/hierarchy_controller.js`
- `addons/web_hierarchy/static/src/hierarchy_controller.xml`
- `addons/web_hierarchy/static/src/hierarchy_model.js`
- `addons/web_hierarchy/static/src/hierarchy_node_draggable.js`
- `addons/web_hierarchy/static/src/hierarchy_renderer.js`
- `addons/web_hierarchy/static/src/hierarchy_renderer.scss`
- `addons/web_hierarchy/static/src/hierarchy_renderer.xml`
- `addons/web_hierarchy/static/src/hierarchy_view.js`
- `addons/web_hierarchy/static/tests/hierarchy_mock_server.js`
- `addons/web_hierarchy/static/tests/hierarchy_view.test.js`
