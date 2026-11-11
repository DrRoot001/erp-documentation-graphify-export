# Module: bus

- **Module ID:** MOD-045
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/bus`
- **Manifest:** `addons/bus/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Instant Messaging Bus allow you to send messages to users, in live.

**Scope evidence:** The module contains 141 files, including 41 Python, 1 XML, and 34 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `web`.

## 2. Module structure

- Model/business logic files: 11
- Controller/API files: 4
- XML/data/view/template files: 1
- Browser asset files: 34
- Security files: 0
- Test files: 15
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 11 model declarations, 192 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/bus/models/res_partner.py:6`, `addons/bus/models/res_groups.py:6`, `addons/bus/models/bus_listener_mixin.py:6`, `addons/bus/models/ir_qweb.py:5`, `addons/bus/models/ir_websocket.py:17`, `addons/bus/models/ir_model.py:6`, `addons/bus/models/res_users_settings.py:6`, `addons/bus/models/ir_http.py:7`, `addons/bus/models/bus.py:71`, `addons/bus/models/res_users.py:6`, `addons/bus/models/ir_attachment.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 4 controller files and 6 route declarations.
- **Evidence:** `addons/bus/controllers/websocket.py:12`, `addons/bus/controllers/websocket.py:23`, `addons/bus/controllers/websocket.py:32`, `addons/bus/controllers/websocket.py:46`, `addons/bus/controllers/websocket.py:52`, `addons/bus/controllers/main.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 34 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/bus/models/bus.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 15 test files are present.
- **Evidence:** `addons/bus/tests/test_websocket_check_session.py`, `addons/bus/tests/test_ir_model.py`, `addons/bus/tests/test_websocket_controller.py`, `addons/bus/tests/test_websocket_timeouts.py`, `addons/bus/tests/test_websocket_rate_limiting.py`, `addons/bus/tests/test_health.py`, `addons/bus/tests/test_assetsbundle.py`, `addons/bus/tests/common.py`, `addons/bus/tests/test_bus_gc.py`, `addons/bus/tests/test_notify.py`, `addons/bus/tests/__init__.py`, `addons/bus/tests/test_close_websocket_after_tour.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 34; representative files: `addons/bus/static/src/multi_tab_shared_worker_plugin.js`, `addons/bus/static/src/bus_parameters_plugin.js`, `addons/bus/static/src/multi_tab_fallback_plugin.js`, `addons/bus/static/src/multi_tab_plugin.js`, `addons/bus/static/src/misc.js`, `addons/bus/static/src/simple_notification_plugin.js`, `addons/bus/static/tests/multi_tab_shared_worker_plugin.test.js`, `addons/bus/static/tests/bus_test_helpers.js`, `addons/bus/static/tests/assets_watchdog.test.js`, `addons/bus/static/tests/simple_notification.test.js`, `addons/bus/static/tests/mock_election_worker.js`, `addons/bus/static/tests/bus_logger.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/bus/__manifest__.py`
- **HTTP entry points:** `addons/bus/controllers/websocket.py:12`, `addons/bus/controllers/websocket.py:23`, `addons/bus/controllers/websocket.py:32`, `addons/bus/controllers/websocket.py:46`, `addons/bus/controllers/websocket.py:52`, `addons/bus/controllers/main.py:9`
- **Scheduled entry points:** `addons/bus/models/bus.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 11
- Representative model evidence: `res.partner` (addons/bus/models/res_partner.py:6); `res.groups` (addons/bus/models/res_groups.py:6); `bus.listener.mixin` (addons/bus/models/bus_listener_mixin.py:6); inherits `ir.qweb` (addons/bus/models/ir_qweb.py:5); `ir.websocket` (addons/bus/models/ir_websocket.py:17); inherits `ir.model` (addons/bus/models/ir_model.py:6); `res.users.settings` (addons/bus/models/res_users_settings.py:6); inherits `ir.http` (addons/bus/models/ir_http.py:7); `bus.bus` (addons/bus/models/bus.py:71); `res.users` (addons/bus/models/res_users.py:6); `ir.attachment` (addons/bus/models/ir_attachment.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 4
- Route declarations: 6
- Route evidence: `addons/bus/controllers/websocket.py:12`, `addons/bus/controllers/websocket.py:23`, `addons/bus/controllers/websocket.py:32`, `addons/bus/controllers/websocket.py:46`, `addons/bus/controllers/websocket.py:52`, `addons/bus/controllers/main.py:9`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `web`
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

- `addons/bus/__init__.py`
- `addons/bus/__manifest__.py`
- `addons/bus/bus_dispatcher.py`
- `addons/bus/controllers/__init__.py`
- `addons/bus/controllers/home.py`
- `addons/bus/controllers/main.py`
- `addons/bus/controllers/websocket.py`
- `addons/bus/i18n/af.po`
- `addons/bus/i18n/ar.po`
- `addons/bus/i18n/az.po`
- `addons/bus/i18n/bg.po`
- `addons/bus/i18n/bs.po`
- `addons/bus/i18n/bus.pot`
- `addons/bus/i18n/ca.po`
- `addons/bus/i18n/cs.po`
- `addons/bus/i18n/da.po`
- `addons/bus/i18n/de.po`
- `addons/bus/i18n/el.po`
- `addons/bus/i18n/es.po`
- `addons/bus/i18n/es_419.po`
- `addons/bus/i18n/es_CL.po`
- `addons/bus/i18n/et.po`
- `addons/bus/i18n/eu.po`
- `addons/bus/i18n/fa.po`
- `addons/bus/i18n/fi.po`
- `addons/bus/i18n/fo.po`
- `addons/bus/i18n/fr.po`
- `addons/bus/i18n/fr_BE.po`
- `addons/bus/i18n/fr_CA.po`
- `addons/bus/i18n/gl.po`
- `addons/bus/i18n/gu.po`
- `addons/bus/i18n/he.po`
- `addons/bus/i18n/hi.po`
- `addons/bus/i18n/hr.po`
- `addons/bus/i18n/hu.po`
- `addons/bus/i18n/hy.po`
- `addons/bus/i18n/id.po`
- `addons/bus/i18n/is.po`
- `addons/bus/i18n/it.po`
- `addons/bus/i18n/ja.po`
- `addons/bus/i18n/ka.po`
- `addons/bus/i18n/kab.po`
- `addons/bus/i18n/km.po`
- `addons/bus/i18n/ko.po`
- `addons/bus/i18n/ku.po`
- `addons/bus/i18n/lo.po`
- `addons/bus/i18n/lt.po`
- `addons/bus/i18n/lv.po`
- `addons/bus/i18n/mk.po`
- `addons/bus/i18n/ml_IN.po`
- `addons/bus/i18n/mn.po`
- `addons/bus/i18n/my.po`
- `addons/bus/i18n/nb.po`
- `addons/bus/i18n/nl.po`
- `addons/bus/i18n/pl.po`
- `addons/bus/i18n/pt.po`
- `addons/bus/i18n/pt_BR.po`
- `addons/bus/i18n/ro.po`
- `addons/bus/i18n/ru.po`
- `addons/bus/i18n/sk.po`
- `addons/bus/i18n/sl.po`
- `addons/bus/i18n/sq.po`
- `addons/bus/i18n/sr@latin.po`
- `addons/bus/i18n/sv.po`
- `addons/bus/i18n/ta.po`
- `addons/bus/i18n/th.po`
- `addons/bus/i18n/tr.po`
- `addons/bus/i18n/uk.po`
- `addons/bus/i18n/uz.po`
- `addons/bus/i18n/vi.po`
- `addons/bus/i18n/zh_CN.po`
- `addons/bus/i18n/zh_TW.po`
- `addons/bus/models/__init__.py`
- `addons/bus/models/bus.py`
- `addons/bus/models/bus_listener_mixin.py`
- `addons/bus/models/ir_attachment.py`
- `addons/bus/models/ir_http.py`
- `addons/bus/models/ir_model.py`
- `addons/bus/models/ir_qweb.py`
- `addons/bus/models/ir_websocket.py`
- `addons/bus/models/res_groups.py`
- `addons/bus/models/res_partner.py`
- `addons/bus/models/res_users.py`
- `addons/bus/models/res_users_settings.py`
- `addons/bus/session_helpers.py`
- `addons/bus/static/src/@types/services.d.ts`
- `addons/bus/static/src/bus_parameters_plugin.js`
- `addons/bus/static/src/debug/bus_logs_menu_item.js`
- `addons/bus/static/src/debug/bus_logs_menu_item.xml`
- `addons/bus/static/src/debug/bus_logs_plugin.js`
- `addons/bus/static/src/misc.js`
- `addons/bus/static/src/multi_tab_fallback_plugin.js`
- `addons/bus/static/src/multi_tab_plugin.js`
- `addons/bus/static/src/multi_tab_shared_worker_plugin.js`
- `addons/bus/static/src/services/assets_watchdog_plugin.js`
- `addons/bus/static/src/services/bus_monitoring_plugin.js`
- `addons/bus/static/src/services/bus_plugin.js`
- `addons/bus/static/src/services/presence_plugin.js`
- `addons/bus/static/src/services/worker_plugin.js`
- `addons/bus/static/src/simple_notification_plugin.js`
- `addons/bus/static/src/workers/base_worker.js`
- `addons/bus/static/src/workers/bus_worker_script.js`
- `addons/bus/static/src/workers/bus_worker_utils.js`
- `addons/bus/static/src/workers/election_worker.js`
- `addons/bus/static/src/workers/websocket_worker.js`
- `addons/bus/static/tests/assets_watchdog.test.js`
- `addons/bus/static/tests/bus_logger.test.js`
- `addons/bus/static/tests/bus_monitoring_plugin.test.js`
- `addons/bus/static/tests/bus_plugin.test.js`
- `addons/bus/static/tests/bus_test_helpers.js`
- `addons/bus/static/tests/mock_base_worker.js`
- `addons/bus/static/tests/mock_election_worker.js`
- `addons/bus/static/tests/mock_server/mock_models/@types/mock_models.d.ts`
- `addons/bus/static/tests/mock_server/mock_models/bus_bus.js`
- `addons/bus/static/tests/mock_server/mock_models/ir_websocket.js`
- `addons/bus/static/tests/mock_websocket.js`
- `addons/bus/static/tests/multi_tab_fallback_plugin.test.js`
- `addons/bus/static/tests/multi_tab_shared_worker_plugin.test.js`
- `addons/bus/static/tests/simple_notification.test.js`
- `addons/bus/static/tests/websocket_worker.test.js`
- `addons/bus/tests/__init__.py`
- `addons/bus/tests/common.py`
- `addons/bus/tests/test_assetsbundle.py`
- `addons/bus/tests/test_bus_gc.py`
- `addons/bus/tests/test_close_websocket_after_tour.py`
- `addons/bus/tests/test_health.py`
- `addons/bus/tests/test_ir_model.py`
- `addons/bus/tests/test_ir_websocket.py`
- `addons/bus/tests/test_notify.py`
- `addons/bus/tests/test_websocket_caryall.py`
- `addons/bus/tests/test_websocket_check_session.py`
- `addons/bus/tests/test_websocket_controller.py`
- `addons/bus/tests/test_websocket_dispatching.py`
- `addons/bus/tests/test_websocket_rate_limiting.py`
- `addons/bus/tests/test_websocket_timeouts.py`
- `addons/bus/tools/__init__.py`
- `addons/bus/tools/misc.py`
- `addons/bus/tools/notifications.py`
- `addons/bus/tools/orjson.py`
- `addons/bus/websocket.py`
- `addons/bus/websocket_protocol.py`
