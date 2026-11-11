# Module: web_tour

- **Module ID:** MOD-594
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/web_tour`
- **Manifest:** `addons/web_tour/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Odoo Web tours.
========================

**Scope evidence:** The module contains 97 files, including 9 Python, 6 XML, and 28 JavaScript/TypeScript files. The manifest declares dependencies: `web`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 28
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/web_tour/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 20 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/web_tour/models/ir_http.py:4`, `addons/web_tour/models/tour.py:5`, `addons/web_tour/models/tour.py:82`, `addons/web_tour/models/res_users.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 28 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/web_tour/views/tour_views.xml:3`, `addons/web_tour/views/tour_views.xml:45`, `addons/web_tour/views/tour_views.xml:59`, `addons/web_tour/views/tour_views.xml:69`, `addons/web_tour/views/tour_views.xml:78`, `addons/web_tour/views/tour_views.xml:75`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/web_tour/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/web_tour/views/tour_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/web_tour/tests/test_onboarding_tours.py`, `addons/web_tour/tests/test_tours.py`, `addons/web_tour/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `tour_form`, `tour_list`, `tour_search`, `tour_action`, `tour_export_js_action`, `menu_tour_action`
- Menus: 1; representative evidence: `addons/web_tour/views/tour_views.xml:75`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 7; representative evidence: `addons/web_tour/views/tour_views.xml:4`, `addons/web_tour/views/tour_views.xml:5`, `addons/web_tour/views/tour_views.xml:46`, `addons/web_tour/views/tour_views.xml:47`, `addons/web_tour/views/tour_views.xml:61`, `addons/web_tour/views/tour_views.xml:62`, `addons/web_tour/views/tour_views.xml:71`
- Browser assets: 28; representative files: `addons/web_tour/static/src/tour_state.js`, `addons/web_tour/static/src/tour_step.js`, `addons/web_tour/static/src/tour_scenarios.js`, `addons/web_tour/static/src/tour_utils.js`, `addons/web_tour/static/src/tour_plugin.js`, `addons/web_tour/static/tests/tour_list.test.js`, `addons/web_tour/static/tests/tour_interactive.test.js`, `addons/web_tour/static/tests/tour_models.js`, `addons/web_tour/static/tests/tour_automatic.test.js`, `addons/web_tour/static/tests/tour_recorder.test.js`, `addons/web_tour/static/tests/tour_pointer.test.js`, `addons/web_tour/static/src/@types/registries.d.ts`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/web_tour/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/web_tour/views/tour_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `ir.http` (addons/web_tour/models/ir_http.py:4); `web_tour.tour` (addons/web_tour/models/tour.py:5); `web_tour.tour.step` (addons/web_tour/models/tour.py:82); inherits `res.users` (addons/web_tour/models/res_users.py:4)
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
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/web_tour/__init__.py`
- `addons/web_tour/__manifest__.py`
- `addons/web_tour/i18n/ar.po`
- `addons/web_tour/i18n/az.po`
- `addons/web_tour/i18n/bg.po`
- `addons/web_tour/i18n/bs.po`
- `addons/web_tour/i18n/ca.po`
- `addons/web_tour/i18n/cs.po`
- `addons/web_tour/i18n/da.po`
- `addons/web_tour/i18n/de.po`
- `addons/web_tour/i18n/el.po`
- `addons/web_tour/i18n/es.po`
- `addons/web_tour/i18n/es_419.po`
- `addons/web_tour/i18n/et.po`
- `addons/web_tour/i18n/fa.po`
- `addons/web_tour/i18n/fi.po`
- `addons/web_tour/i18n/fr.po`
- `addons/web_tour/i18n/gu.po`
- `addons/web_tour/i18n/he.po`
- `addons/web_tour/i18n/hi.po`
- `addons/web_tour/i18n/hr.po`
- `addons/web_tour/i18n/hu.po`
- `addons/web_tour/i18n/id.po`
- `addons/web_tour/i18n/is.po`
- `addons/web_tour/i18n/it.po`
- `addons/web_tour/i18n/ja.po`
- `addons/web_tour/i18n/kab.po`
- `addons/web_tour/i18n/km.po`
- `addons/web_tour/i18n/ko.po`
- `addons/web_tour/i18n/ku.po`
- `addons/web_tour/i18n/lo.po`
- `addons/web_tour/i18n/lt.po`
- `addons/web_tour/i18n/lv.po`
- `addons/web_tour/i18n/mn.po`
- `addons/web_tour/i18n/my.po`
- `addons/web_tour/i18n/nb.po`
- `addons/web_tour/i18n/nl.po`
- `addons/web_tour/i18n/pl.po`
- `addons/web_tour/i18n/pt.po`
- `addons/web_tour/i18n/pt_BR.po`
- `addons/web_tour/i18n/ro.po`
- `addons/web_tour/i18n/ru.po`
- `addons/web_tour/i18n/sk.po`
- `addons/web_tour/i18n/sl.po`
- `addons/web_tour/i18n/sr@latin.po`
- `addons/web_tour/i18n/sv.po`
- `addons/web_tour/i18n/th.po`
- `addons/web_tour/i18n/tr.po`
- `addons/web_tour/i18n/uk.po`
- `addons/web_tour/i18n/uz.po`
- `addons/web_tour/i18n/vi.po`
- `addons/web_tour/i18n/web_tour.pot`
- `addons/web_tour/i18n/zh_CN.po`
- `addons/web_tour/i18n/zh_TW.po`
- `addons/web_tour/models/__init__.py`
- `addons/web_tour/models/ir_http.py`
- `addons/web_tour/models/res_users.py`
- `addons/web_tour/models/tour.py`
- `addons/web_tour/security/ir.access.csv`
- `addons/web_tour/static/src/@types/registries.d.ts`
- `addons/web_tour/static/src/tour_automatic/tour_automatic.js`
- `addons/web_tour/static/src/tour_automatic/tour_step_automatic.js`
- `addons/web_tour/static/src/tour_helpers/tour_helpers.js`
- `addons/web_tour/static/src/tour_helpers/tour_helpers_clipboard.js`
- `addons/web_tour/static/src/tour_helpers/tour_helpers_hoot.js`
- `addons/web_tour/static/src/tour_interactive/tour_interactive.js`
- `addons/web_tour/static/src/tour_interactive/tour_interactive_observer.js`
- `addons/web_tour/static/src/tour_interactive/tour_step_interactive.js`
- `addons/web_tour/static/src/tour_plugin.js`
- `addons/web_tour/static/src/tour_pointer/tour_pointer.js`
- `addons/web_tour/static/src/tour_pointer/tour_pointer.scss`
- `addons/web_tour/static/src/tour_pointer/tour_pointer.xml`
- `addons/web_tour/static/src/tour_recorder/tour_recorder.js`
- `addons/web_tour/static/src/tour_recorder/tour_recorder.xml`
- `addons/web_tour/static/src/tour_recorder/tour_recorder_command_provider.js`
- `addons/web_tour/static/src/tour_recorder/tour_recorder_plugin.js`
- `addons/web_tour/static/src/tour_recorder/tour_recorder_state.js`
- `addons/web_tour/static/src/tour_scenarios.js`
- `addons/web_tour/static/src/tour_state.js`
- `addons/web_tour/static/src/tour_step.js`
- `addons/web_tour/static/src/tour_utils.js`
- `addons/web_tour/static/src/views/tour_controller.xml`
- `addons/web_tour/static/src/views/tour_list.js`
- `addons/web_tour/static/src/widgets/onboarding_item.js`
- `addons/web_tour/static/src/widgets/onboarding_item.xml`
- `addons/web_tour/static/src/widgets/tour_start.js`
- `addons/web_tour/static/src/widgets/tour_start.xml`
- `addons/web_tour/static/tests/tour_automatic.test.js`
- `addons/web_tour/static/tests/tour_interactive.test.js`
- `addons/web_tour/static/tests/tour_list.test.js`
- `addons/web_tour/static/tests/tour_models.js`
- `addons/web_tour/static/tests/tour_pointer.test.js`
- `addons/web_tour/static/tests/tour_recorder.test.js`
- `addons/web_tour/tests/__init__.py`
- `addons/web_tour/tests/test_onboarding_tours.py`
- `addons/web_tour/tests/test_tours.py`
- `addons/web_tour/views/tour_views.xml`
