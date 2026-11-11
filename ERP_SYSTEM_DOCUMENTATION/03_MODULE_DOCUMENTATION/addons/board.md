# Module: board

- **Module ID:** MOD-044
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/board`
- **Manifest:** `addons/board/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Productivity`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Build your own dashboards

**Manifest description:**

Lets the user create a custom dashboard.
========================================

Allows users to create custom dashboard.

**Scope evidence:** The module contains 92 files, including 6 Python, 4 XML, and 6 JavaScript/TypeScript files. The manifest declares dependencies: `spreadsheet_dashboard`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 2
- XML/data/view/template files: 4
- Browser asset files: 6
- Security files: 1
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/board/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 1 model declarations, 4 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/board/models/board.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/board/controllers/main.py:11`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 6 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/board/views/board_views.xml:5`, `addons/board/views/board_views.xml:19`, `addons/board/views/board_views.xml:31`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/board/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `board_my_dash_view`, `open_board_my_dash_action`, `My Dashboard`
- Menus: 1; representative evidence: `addons/board/views/board_views.xml:31`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/board/views/board_views.xml:7`, `addons/board/views/board_views.xml:8`, `addons/board/views/board_views.xml:21`, `addons/board/views/board_views.xml:22`
- Browser assets: 6; representative files: `addons/board/static/src/board_action.js`, `addons/board/static/src/board_controller.js`, `addons/board/static/src/board_view.js`, `addons/board/static/tests/board.test.js`, `addons/board/static/tests/add_to_dashboard.test.js`, `addons/board/static/src/add_to_board/add_to_board.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/board/__manifest__.py`
- **HTTP entry points:** `addons/board/controllers/main.py:11`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: `board.board` (addons/board/models/board.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/board/controllers/main.py:11`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `spreadsheet_dashboard`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/board/__init__.py`
- `addons/board/__manifest__.py`
- `addons/board/controllers/__init__.py`
- `addons/board/controllers/main.py`
- `addons/board/i18n/af.po`
- `addons/board/i18n/ar.po`
- `addons/board/i18n/az.po`
- `addons/board/i18n/bg.po`
- `addons/board/i18n/bn.po`
- `addons/board/i18n/board.pot`
- `addons/board/i18n/bs.po`
- `addons/board/i18n/ca.po`
- `addons/board/i18n/cs.po`
- `addons/board/i18n/da.po`
- `addons/board/i18n/de.po`
- `addons/board/i18n/el.po`
- `addons/board/i18n/es.po`
- `addons/board/i18n/es_419.po`
- `addons/board/i18n/es_CL.po`
- `addons/board/i18n/et.po`
- `addons/board/i18n/eu.po`
- `addons/board/i18n/fa.po`
- `addons/board/i18n/fi.po`
- `addons/board/i18n/fo.po`
- `addons/board/i18n/fr.po`
- `addons/board/i18n/fr_BE.po`
- `addons/board/i18n/fr_CA.po`
- `addons/board/i18n/gl.po`
- `addons/board/i18n/gu.po`
- `addons/board/i18n/he.po`
- `addons/board/i18n/hi.po`
- `addons/board/i18n/hr.po`
- `addons/board/i18n/hu.po`
- `addons/board/i18n/id.po`
- `addons/board/i18n/is.po`
- `addons/board/i18n/it.po`
- `addons/board/i18n/ja.po`
- `addons/board/i18n/ka.po`
- `addons/board/i18n/kab.po`
- `addons/board/i18n/km.po`
- `addons/board/i18n/ko.po`
- `addons/board/i18n/ku.po`
- `addons/board/i18n/lo.po`
- `addons/board/i18n/lt.po`
- `addons/board/i18n/lv.po`
- `addons/board/i18n/mk.po`
- `addons/board/i18n/ml_IN.po`
- `addons/board/i18n/mn.po`
- `addons/board/i18n/my.po`
- `addons/board/i18n/nb.po`
- `addons/board/i18n/nl.po`
- `addons/board/i18n/pl.po`
- `addons/board/i18n/pt.po`
- `addons/board/i18n/pt_BR.po`
- `addons/board/i18n/ro.po`
- `addons/board/i18n/ru.po`
- `addons/board/i18n/sk.po`
- `addons/board/i18n/sl.po`
- `addons/board/i18n/sq.po`
- `addons/board/i18n/sr@latin.po`
- `addons/board/i18n/sv.po`
- `addons/board/i18n/ta.po`
- `addons/board/i18n/th.po`
- `addons/board/i18n/tr.po`
- `addons/board/i18n/uk.po`
- `addons/board/i18n/uz.po`
- `addons/board/i18n/vi.po`
- `addons/board/i18n/zh_CN.po`
- `addons/board/i18n/zh_TW.po`
- `addons/board/models/__init__.py`
- `addons/board/models/board.py`
- `addons/board/security/ir.access.csv`
- `addons/board/static/description/icon.png`
- `addons/board/static/description/icon.svg`
- `addons/board/static/description/icon_hi.png`
- `addons/board/static/img/layout_1-1-1.png`
- `addons/board/static/img/layout_1-1.png`
- `addons/board/static/img/layout_1-2.png`
- `addons/board/static/img/layout_1.png`
- `addons/board/static/img/layout_2-1.png`
- `addons/board/static/img/view_todo_arrow.png`
- `addons/board/static/src/add_to_board/add_to_board.js`
- `addons/board/static/src/add_to_board/add_to_board.xml`
- `addons/board/static/src/board_action.js`
- `addons/board/static/src/board_action.xml`
- `addons/board/static/src/board_controller.js`
- `addons/board/static/src/board_controller.scss`
- `addons/board/static/src/board_controller.xml`
- `addons/board/static/src/board_view.js`
- `addons/board/static/tests/add_to_dashboard.test.js`
- `addons/board/static/tests/board.test.js`
- `addons/board/views/board_views.xml`
