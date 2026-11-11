# Module: http_routing

- **Module ID:** MOD-107
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/http_routing`
- **Manifest:** `addons/http_routing/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Web Routing

**Manifest description:**

Proposes advanced routing options not available in web or base to keep
base modules simple.

**Scope evidence:** The module contains 63 files, including 11 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `web`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 2
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 30 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/http_routing/models/res_lang.py:7`, `addons/http_routing/models/ir_qweb.py:6`, `addons/http_routing/models/ir_http.py:49`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 2 route declarations.
- **Evidence:** `addons/http_routing/controllers/main.py:12`, `addons/http_routing/controllers/main.py:23`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 18 record/template/menu identifiers.
- **Evidence:** `addons/http_routing/views/http_routing_template.xml:3`, `addons/http_routing/views/http_routing_template.xml:16`, `addons/http_routing/views/http_routing_template.xml:23`, `addons/http_routing/views/http_routing_template.xml:62`, `addons/http_routing/views/http_routing_template.xml:73`, `addons/http_routing/views/http_routing_template.xml:84`, `addons/http_routing/views/http_routing_template.xml:94`, `addons/http_routing/views/http_routing_template.xml:105`, `addons/http_routing/views/http_routing_template.xml:116`, `addons/http_routing/views/http_routing_template.xml:127`, `addons/http_routing/views/http_routing_template.xml:138`, `addons/http_routing/views/http_routing_template.xml:174`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/http_routing/tests/test_res_lang.py`, `addons/http_routing/tests/common.py`, `addons/http_routing/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `HTTP Error`, `error_message`, `http_error_debug`, `http_error_container`, `4xx`, `4xx (oe_structure_4xx_layout_1)`, `400`, `400 (oe_structure_400_layout_1)`, `403`, `403 (oe_structure_403_layout_1)`, `Page Not Found`, `415`, `415 (oe_structure_415_layout_1)`, `422`, `422 (oe_structure_422_layout_1)`, `500`, `res_lang_form_inherit_model`, `res_lang_tree_inherit_model`
- Menus: 0; representative evidence: Not found in module
- Templates: 16; representative evidence: `addons/http_routing/views/http_routing_template.xml:3`, `addons/http_routing/views/http_routing_template.xml:16`, `addons/http_routing/views/http_routing_template.xml:23`, `addons/http_routing/views/http_routing_template.xml:62`, `addons/http_routing/views/http_routing_template.xml:73`, `addons/http_routing/views/http_routing_template.xml:84`, `addons/http_routing/views/http_routing_template.xml:94`, `addons/http_routing/views/http_routing_template.xml:105`, `addons/http_routing/views/http_routing_template.xml:116`, `addons/http_routing/views/http_routing_template.xml:127`, `addons/http_routing/views/http_routing_template.xml:138`, `addons/http_routing/views/http_routing_template.xml:174`
- View/action field declarations: 4; representative evidence: `addons/http_routing/views/res_lang_views.xml:5`, `addons/http_routing/views/res_lang_views.xml:7`, `addons/http_routing/views/res_lang_views.xml:16`, `addons/http_routing/views/res_lang_views.xml:18`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/http_routing/__manifest__.py`
- **HTTP entry points:** `addons/http_routing/controllers/main.py:12`, `addons/http_routing/controllers/main.py:23`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `res.lang` (addons/http_routing/models/res_lang.py:7); inherits `ir.qweb` (addons/http_routing/models/ir_qweb.py:6); inherits `ir.http` (addons/http_routing/models/ir_http.py:49)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 2
- Route evidence: `addons/http_routing/controllers/main.py:12`, `addons/http_routing/controllers/main.py:23`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `web`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/http_routing/__init__.py`
- `addons/http_routing/__manifest__.py`
- `addons/http_routing/controllers/__init__.py`
- `addons/http_routing/controllers/main.py`
- `addons/http_routing/i18n/ar.po`
- `addons/http_routing/i18n/az.po`
- `addons/http_routing/i18n/bg.po`
- `addons/http_routing/i18n/bs.po`
- `addons/http_routing/i18n/ca.po`
- `addons/http_routing/i18n/cs.po`
- `addons/http_routing/i18n/da.po`
- `addons/http_routing/i18n/de.po`
- `addons/http_routing/i18n/el.po`
- `addons/http_routing/i18n/es.po`
- `addons/http_routing/i18n/es_419.po`
- `addons/http_routing/i18n/et.po`
- `addons/http_routing/i18n/fa.po`
- `addons/http_routing/i18n/fi.po`
- `addons/http_routing/i18n/fr.po`
- `addons/http_routing/i18n/he.po`
- `addons/http_routing/i18n/hi.po`
- `addons/http_routing/i18n/hr.po`
- `addons/http_routing/i18n/http_routing.pot`
- `addons/http_routing/i18n/hu.po`
- `addons/http_routing/i18n/id.po`
- `addons/http_routing/i18n/it.po`
- `addons/http_routing/i18n/ja.po`
- `addons/http_routing/i18n/kab.po`
- `addons/http_routing/i18n/ko.po`
- `addons/http_routing/i18n/ku.po`
- `addons/http_routing/i18n/lo.po`
- `addons/http_routing/i18n/lt.po`
- `addons/http_routing/i18n/lv.po`
- `addons/http_routing/i18n/mn.po`
- `addons/http_routing/i18n/my.po`
- `addons/http_routing/i18n/nb.po`
- `addons/http_routing/i18n/nl.po`
- `addons/http_routing/i18n/pl.po`
- `addons/http_routing/i18n/pt.po`
- `addons/http_routing/i18n/pt_BR.po`
- `addons/http_routing/i18n/ro.po`
- `addons/http_routing/i18n/ru.po`
- `addons/http_routing/i18n/sk.po`
- `addons/http_routing/i18n/sl.po`
- `addons/http_routing/i18n/sr@latin.po`
- `addons/http_routing/i18n/sv.po`
- `addons/http_routing/i18n/th.po`
- `addons/http_routing/i18n/tr.po`
- `addons/http_routing/i18n/uk.po`
- `addons/http_routing/i18n/uz.po`
- `addons/http_routing/i18n/vi.po`
- `addons/http_routing/i18n/zh_CN.po`
- `addons/http_routing/i18n/zh_TW.po`
- `addons/http_routing/models/__init__.py`
- `addons/http_routing/models/ir_http.py`
- `addons/http_routing/models/ir_qweb.py`
- `addons/http_routing/models/res_lang.py`
- `addons/http_routing/static/shapes/404.svg`
- `addons/http_routing/tests/__init__.py`
- `addons/http_routing/tests/common.py`
- `addons/http_routing/tests/test_res_lang.py`
- `addons/http_routing/views/http_routing_template.xml`
- `addons/http_routing/views/res_lang_views.xml`
