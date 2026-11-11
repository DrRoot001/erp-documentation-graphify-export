# Module: test_translation_mode

- **Module ID:** MOD-584
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/test_translation_mode`
- **Manifest:** `addons/test_translation_mode/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** In-context and interactive translation mode to streamline the module translation process using Weblate

**Manifest description:**

The translation mode is available when several languages are installed. Select the language to translate,
enable the interactive translation mode from the command palette then browse the screens to translate.
By default, the translate feature redirects to the Odoo official translation project powered by Weblate.
In the settings, a custom Weblate project can be targeted.

WARNING:
This module adds invisible meta data to the translated strings, which might interfere with certain workflows.
Do not use it on production databases

**Scope evidence:** The module contains 19 files, including 7 Python, 3 XML, and 8 JavaScript/TypeScript files. The manifest declares dependencies: `web`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 3
- Browser asset files: 8
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 3 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/test_translation_mode/models/res_config_settings.py:4`, `addons/test_translation_mode/models/ir_http.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 8 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/test_translation_mode/data/config_parameter.xml:3`, `addons/test_translation_mode/views/translation_mode_settings.xml:3`, `addons/test_translation_mode/views/translation_mode_settings.xml:31`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `translation_url`, `translation_mode_settings_form`, `translation_mode_settings_action`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/test_translation_mode/views/translation_mode_settings.xml:5`, `addons/test_translation_mode/views/translation_mode_settings.xml:6`, `addons/test_translation_mode/views/translation_mode_settings.xml:32`, `addons/test_translation_mode/views/translation_mode_settings.xml:34`
- Browser assets: 8; representative files: `addons/test_translation_mode/static/src/siphash.js`, `addons/test_translation_mode/static/src/translate_mode_debug_providers.js`, `addons/test_translation_mode/static/src/translation_mode_side_panel.js`, `addons/test_translation_mode/static/src/translation_mode_service.js`, `addons/test_translation_mode/static/src/translation.patch.js`, `addons/test_translation_mode/static/tests/translation.patch.test.js`, `addons/test_translation_mode/static/tests/translation_mode_side_panel.test.js`, `addons/test_translation_mode/static/src/@types/services.d.ts`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/test_translation_mode/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `res.config.settings` (addons/test_translation_mode/models/res_config_settings.py:4); inherits `ir.http` (addons/test_translation_mode/models/ir_http.py:7)
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

- `addons/test_translation_mode/__init__.py`
- `addons/test_translation_mode/__manifest__.py`
- `addons/test_translation_mode/data/config_parameter.xml`
- `addons/test_translation_mode/models/__init__.py`
- `addons/test_translation_mode/models/ir_http.py`
- `addons/test_translation_mode/models/res_config_settings.py`
- `addons/test_translation_mode/static/src/@types/services.d.ts`
- `addons/test_translation_mode/static/src/siphash.js`
- `addons/test_translation_mode/static/src/translate_mode_debug_providers.js`
- `addons/test_translation_mode/static/src/translation.patch.js`
- `addons/test_translation_mode/static/src/translation_mode.css`
- `addons/test_translation_mode/static/src/translation_mode_service.js`
- `addons/test_translation_mode/static/src/translation_mode_side_panel.js`
- `addons/test_translation_mode/static/src/translation_mode_side_panel.xml`
- `addons/test_translation_mode/static/tests/translation.patch.test.js`
- `addons/test_translation_mode/static/tests/translation_mode_side_panel.test.js`
- `addons/test_translation_mode/tools/__init__.py`
- `addons/test_translation_mode/tools/translate.py`
- `addons/test_translation_mode/views/translation_mode_settings.xml`
