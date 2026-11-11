# Module: iot_drivers

- **Module ID:** MOD-112
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/iot_drivers`
- **Manifest:** `addons/iot_drivers/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Connect the Web Client to Hardware Peripherals

**Manifest description:**

Hardware Poxy
=============

This module allows you to remotely use peripherals connected to this server.

This modules only contains the enabling framework. The actual devices drivers
are found in other modules that must be installed separately.

**Scope evidence:** The module contains 79 files, including 51 Python, 0 XML, and 19 JavaScript/TypeScript files. The manifest declares dependencies: None declared.

## 2. Module structure

- Model/business logic files: 0
- Controller/API files: 5
- XML/data/view/template files: 0
- Browser asset files: 19
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### HTTP/API surface

- **Description:** 5 controller files and 0 route declarations.
- **Evidence:** `addons/iot_drivers/controllers/homepage.py`, `addons/iot_drivers/controllers/driver.py`, `addons/iot_drivers/controllers/proxy.py`, `addons/iot_drivers/controllers/__init__.py`, `addons/iot_drivers/controllers/l10n_eg_eta_usb.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 0 XML files and 19 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 0; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 19; representative files: `addons/iot_drivers/static/src/app/homepage.js`, `addons/iot_drivers/static/src/app/main.js`, `addons/iot_drivers/static/src/app/logs.js`, `addons/iot_drivers/static/src/app/store.js`, `addons/iot_drivers/static/src/app/status.js`, `addons/iot_drivers/static/src/app/components/loading_full_screen.js`, `addons/iot_drivers/static/src/app/components/single_data.js`, `addons/iot_drivers/static/src/app/components/footer_buttons.js`, `addons/iot_drivers/static/src/app/hooks/store_hook.js`, `addons/iot_drivers/static/src/app/components/dialog/time_dialog.js`, `addons/iot_drivers/static/src/app/components/dialog/dialog.js`, `addons/iot_drivers/static/src/app/components/dialog/credentials_dialog.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/iot_drivers/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 5
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: None declared
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Not found
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/iot_drivers/__init__.py`
- `addons/iot_drivers/__manifest__.py`
- `addons/iot_drivers/browser.py`
- `addons/iot_drivers/cli/genproxytoken.py`
- `addons/iot_drivers/connection_manager.py`
- `addons/iot_drivers/controllers/__init__.py`
- `addons/iot_drivers/controllers/driver.py`
- `addons/iot_drivers/controllers/homepage.py`
- `addons/iot_drivers/controllers/l10n_eg_eta_usb.py`
- `addons/iot_drivers/controllers/proxy.py`
- `addons/iot_drivers/driver.py`
- `addons/iot_drivers/event_manager.py`
- `addons/iot_drivers/exception_logger.py`
- `addons/iot_drivers/http.py`
- `addons/iot_drivers/interface.py`
- `addons/iot_drivers/iot_handlers/__init__.py`
- `addons/iot_drivers/iot_handlers/drivers/bluetooth_caliper_driver_L.py`
- `addons/iot_drivers/iot_handlers/drivers/camera_driver_L.py`
- `addons/iot_drivers/iot_handlers/drivers/ctypes_terminal_driver.py`
- `addons/iot_drivers/iot_handlers/drivers/display_driver_L.py`
- `addons/iot_drivers/iot_handlers/drivers/keyboard_driver_L.py`
- `addons/iot_drivers/iot_handlers/drivers/l10n_ke_edi_serial_driver.py`
- `addons/iot_drivers/iot_handlers/drivers/printer_driver_L.py`
- `addons/iot_drivers/iot_handlers/drivers/printer_driver_W.py`
- `addons/iot_drivers/iot_handlers/drivers/printer_driver_base.py`
- `addons/iot_drivers/iot_handlers/drivers/serial_blackbox_be_driver.py`
- `addons/iot_drivers/iot_handlers/drivers/serial_blackbox_se_driver.py`
- `addons/iot_drivers/iot_handlers/drivers/serial_caliper_driver.py`
- `addons/iot_drivers/iot_handlers/drivers/serial_driver_base.py`
- `addons/iot_drivers/iot_handlers/drivers/serial_scale_driver.py`
- `addons/iot_drivers/iot_handlers/drivers/six_driver.py`
- `addons/iot_drivers/iot_handlers/drivers/worldline_driver.py`
- `addons/iot_drivers/iot_handlers/interfaces/bluetooth_interface_L.py`
- `addons/iot_drivers/iot_handlers/interfaces/camera_interface_L.py`
- `addons/iot_drivers/iot_handlers/interfaces/ctep_interface.py`
- `addons/iot_drivers/iot_handlers/interfaces/display_interface_L.py`
- `addons/iot_drivers/iot_handlers/interfaces/printer_interface_L.py`
- `addons/iot_drivers/iot_handlers/interfaces/printer_interface_W.py`
- `addons/iot_drivers/iot_handlers/interfaces/serial_interface.py`
- `addons/iot_drivers/iot_handlers/interfaces/tim_interface.py`
- `addons/iot_drivers/iot_handlers/interfaces/usb_interface_L.py`
- `addons/iot_drivers/main.py`
- `addons/iot_drivers/static/img/background-light.svg`
- `addons/iot_drivers/static/img/favicon.png`
- `addons/iot_drivers/static/src/app/components/dialog/credentials_dialog.js`
- `addons/iot_drivers/static/src/app/components/dialog/database_dialog.js`
- `addons/iot_drivers/static/src/app/components/dialog/debugging_tools_dialog.js`
- `addons/iot_drivers/static/src/app/components/dialog/device_dialog.js`
- `addons/iot_drivers/static/src/app/components/dialog/dialog.js`
- `addons/iot_drivers/static/src/app/components/dialog/handlers_dialog.js`
- `addons/iot_drivers/static/src/app/components/dialog/six_terminal_dialog.js`
- `addons/iot_drivers/static/src/app/components/dialog/time_dialog.js`
- `addons/iot_drivers/static/src/app/components/dialog/update_dialog.js`
- `addons/iot_drivers/static/src/app/components/dialog/wifi_dialog.js`
- `addons/iot_drivers/static/src/app/components/footer_buttons.js`
- `addons/iot_drivers/static/src/app/components/loading_full_screen.js`
- `addons/iot_drivers/static/src/app/components/single_data.js`
- `addons/iot_drivers/static/src/app/css/homepage.css`
- `addons/iot_drivers/static/src/app/css/icons.css`
- `addons/iot_drivers/static/src/app/css/logs.css`
- `addons/iot_drivers/static/src/app/css/status_display.css`
- `addons/iot_drivers/static/src/app/homepage.js`
- `addons/iot_drivers/static/src/app/hooks/store_hook.js`
- `addons/iot_drivers/static/src/app/logs.js`
- `addons/iot_drivers/static/src/app/main.js`
- `addons/iot_drivers/static/src/app/status.js`
- `addons/iot_drivers/static/src/app/store.js`
- `addons/iot_drivers/tools/__init__.py`
- `addons/iot_drivers/tools/certificate.py`
- `addons/iot_drivers/tools/communication.py`
- `addons/iot_drivers/tools/helpers.py`
- `addons/iot_drivers/tools/route.py`
- `addons/iot_drivers/tools/system.py`
- `addons/iot_drivers/tools/upgrade.py`
- `addons/iot_drivers/tools/wifi.py`
- `addons/iot_drivers/views/index.html`
- `addons/iot_drivers/views/logs.html`
- `addons/iot_drivers/views/status_display.html`
- `addons/iot_drivers/websocket_client.py`
