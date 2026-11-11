# Module: test_http

- **Module ID:** MOD-656
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `odoo/addons/test_http`
- **Manifest:** `odoo/addons/test_http/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tests`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

A module to test HTTP

**Scope evidence:** The module contains 34 files, including 27 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `web`, `web_tour`, `mail`, `rpc`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 1
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 0
- Test files: 20
- Scheduled/automation evidence files: 2
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 335 methods, 0 constraint handlers, 0 onchange handlers, and 4 dependency declarations.
- **Evidence:** `odoo/addons/test_http/models/stargate.py:10`, `odoo/addons/test_http/models/stargate.py:68`, `odoo/addons/test_http/models/stargate.py:84`, `odoo/addons/test_http/models/rpc.py:6`, `odoo/addons/test_http/models/rpc.py:26`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 1 controller files and 44 route declarations.
- **Evidence:** `odoo/addons/test_http/controllers.py:43`, `odoo/addons/test_http/controllers.py:47`, `odoo/addons/test_http/controllers.py:53`, `odoo/addons/test_http/controllers.py:59`, `odoo/addons/test_http/controllers.py:65`, `odoo/addons/test_http/controllers.py:69`, `odoo/addons/test_http/controllers.py:82`, `odoo/addons/test_http/controllers.py:86`, `odoo/addons/test_http/controllers.py:92`, `odoo/addons/test_http/controllers.py:109`, `odoo/addons/test_http/controllers.py:113`, `odoo/addons/test_http/controllers.py:117`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 21 record/template/menu identifiers.
- **Evidence:** `odoo/addons/test_http/data.xml:4`, `odoo/addons/test_http/data.xml:12`, `odoo/addons/test_http/data.xml:19`, `odoo/addons/test_http/data.xml:27`, `odoo/addons/test_http/data.xml:34`, `odoo/addons/test_http/data.xml:39`, `odoo/addons/test_http/data.xml:44`, `odoo/addons/test_http/data.xml:54`, `odoo/addons/test_http/data.xml:62`, `odoo/addons/test_http/data.xml:70`, `odoo/addons/test_http/data.xml:78`, `odoo/addons/test_http/views.xml:26`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `odoo/addons/test_http/tests/test_webjson.py`, `odoo/addons/test_http/tests/test_webjson2.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 20 test files are present.
- **Evidence:** `odoo/addons/test_http/tests/test_device.py`, `odoo/addons/test_http/tests/test_web_server.py`, `odoo/addons/test_http/tests/test_xss.py`, `odoo/addons/test_http/tests/test_misc.py`, `odoo/addons/test_http/tests/test_security.py`, `odoo/addons/test_http/tests/test_echo_reply.py`, `odoo/addons/test_http/tests/test_bearer_scope.py`, `odoo/addons/test_http/tests/test_static.py`, `odoo/addons/test_http/tests/test_error_rpc.py`, `odoo/addons/test_http/tests/test_common.py`, `odoo/addons/test_http/tests/test_auth_custom.py`, `odoo/addons/test_http/tests/test_models.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `gizeh_png`, `gizeh_url`, `xss_svg`, `rickroll`, `milky_way`, `pegasus`, `earth`, `abydos`, `dakara`, `lantea`, `athos`, `test_http_stargate_list`, `test_http_stargate_form`, `test_http_galaxy_form`, `test_http_stargate_pivot`, `test_http_stargate_graph`, `test_http_stargate_activity`, `test_http_stargate_calendar`, `action_window_stargate`, `tmpl_galaxy`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `odoo/addons/test_http/views.xml:3`, `odoo/addons/test_http/views.xml:14`
- View/action field declarations: 16; representative evidence: `odoo/addons/test_http/views.xml:27`, `odoo/addons/test_http/views.xml:28`, `odoo/addons/test_http/views.xml:37`, `odoo/addons/test_http/views.xml:38`, `odoo/addons/test_http/views.xml:58`, `odoo/addons/test_http/views.xml:59`, `odoo/addons/test_http/views.xml:75`, `odoo/addons/test_http/views.xml:76`, `odoo/addons/test_http/views.xml:86`, `odoo/addons/test_http/views.xml:87`, `odoo/addons/test_http/views.xml:95`, `odoo/addons/test_http/views.xml:96`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `odoo/addons/test_http/__manifest__.py`
- **HTTP entry points:** `odoo/addons/test_http/controllers.py:43`, `odoo/addons/test_http/controllers.py:47`, `odoo/addons/test_http/controllers.py:53`, `odoo/addons/test_http/controllers.py:59`, `odoo/addons/test_http/controllers.py:65`, `odoo/addons/test_http/controllers.py:69`, `odoo/addons/test_http/controllers.py:82`, `odoo/addons/test_http/controllers.py:86`, `odoo/addons/test_http/controllers.py:92`, `odoo/addons/test_http/controllers.py:109`, `odoo/addons/test_http/controllers.py:113`, `odoo/addons/test_http/controllers.py:117`
- **Scheduled entry points:** `odoo/addons/test_http/tests/test_webjson.py`, `odoo/addons/test_http/tests/test_webjson2.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: `test_http.stargate` (odoo/addons/test_http/models/stargate.py:10); `test_http.galaxy` (odoo/addons/test_http/models/stargate.py:68); inherits `ir.http` (odoo/addons/test_http/models/stargate.py:84); `test_rpc.model_a` (odoo/addons/test_http/models/rpc.py:6); `test_rpc.model_b` (odoo/addons/test_http/models/rpc.py:26)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 1
- Route declarations: 44
- Route evidence: `odoo/addons/test_http/controllers.py:43`, `odoo/addons/test_http/controllers.py:47`, `odoo/addons/test_http/controllers.py:53`, `odoo/addons/test_http/controllers.py:59`, `odoo/addons/test_http/controllers.py:65`, `odoo/addons/test_http/controllers.py:69`, `odoo/addons/test_http/controllers.py:82`, `odoo/addons/test_http/controllers.py:86`, `odoo/addons/test_http/controllers.py:92`, `odoo/addons/test_http/controllers.py:109`, `odoo/addons/test_http/controllers.py:113`, `odoo/addons/test_http/controllers.py:117`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `web`, `web_tour`, `mail`, `rpc`
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

- `odoo/addons/test_http/__init__.py`
- `odoo/addons/test_http/__manifest__.py`
- `odoo/addons/test_http/controllers.py`
- `odoo/addons/test_http/data.xml`
- `odoo/addons/test_http/ir.access.csv`
- `odoo/addons/test_http/models/__init__.py`
- `odoo/addons/test_http/models/rpc.py`
- `odoo/addons/test_http/models/stargate.py`
- `odoo/addons/test_http/static/src/img/gizeh.png`
- `odoo/addons/test_http/static/src/img/milky_way.jpg`
- `odoo/addons/test_http/static/src/img/pegasus.jpg`
- `odoo/addons/test_http/static/src/img/xss.svg`
- `odoo/addons/test_http/tests/__init__.py`
- `odoo/addons/test_http/tests/test_auth_custom.py`
- `odoo/addons/test_http/tests/test_bearer_scope.py`
- `odoo/addons/test_http/tests/test_captcha.py`
- `odoo/addons/test_http/tests/test_common.py`
- `odoo/addons/test_http/tests/test_device.py`
- `odoo/addons/test_http/tests/test_echo_reply.py`
- `odoo/addons/test_http/tests/test_error_http.py`
- `odoo/addons/test_http/tests/test_error_rpc.py`
- `odoo/addons/test_http/tests/test_greeting.py`
- `odoo/addons/test_http/tests/test_misc.py`
- `odoo/addons/test_http/tests/test_models.py`
- `odoo/addons/test_http/tests/test_rpc_path.py`
- `odoo/addons/test_http/tests/test_security.py`
- `odoo/addons/test_http/tests/test_session.py`
- `odoo/addons/test_http/tests/test_static.py`
- `odoo/addons/test_http/tests/test_web_server.py`
- `odoo/addons/test_http/tests/test_webjson.py`
- `odoo/addons/test_http/tests/test_webjson2.py`
- `odoo/addons/test_http/tests/test_xss.py`
- `odoo/addons/test_http/utils.py`
- `odoo/addons/test_http/views.xml`
