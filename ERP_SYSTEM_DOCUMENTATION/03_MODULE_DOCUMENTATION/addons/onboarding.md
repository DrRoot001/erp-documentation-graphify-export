# Module: onboarding

- **Module ID:** MOD-389
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/onboarding`
- **Manifest:** `addons/onboarding/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module allows to manage onboardings and their progress
================================================================================

**Scope evidence:** The module contains 70 files, including 12 Python, 3 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `web`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 3
- Browser asset files: 1
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/onboarding/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 41 methods, 1 constraint handlers, 0 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/onboarding/models/onboarding_progress.py:14`, `addons/onboarding/models/onboarding_progress_step.py:8`, `addons/onboarding/models/onboarding_onboarding.py:8`, `addons/onboarding/models/onboarding_onboarding_step.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 1 JavaScript/TypeScript files; static XML analysis found 11 record/template/menu identifiers.
- **Evidence:** `addons/onboarding/views/onboarding_views.xml:3`, `addons/onboarding/views/onboarding_views.xml:20`, `addons/onboarding/views/onboarding_views.xml:49`, `addons/onboarding/views/onboarding_views.xml:63`, `addons/onboarding/views/onboarding_views.xml:98`, `addons/onboarding/views/onboarding_views.xml:104`, `addons/onboarding/views/onboarding_templates.xml:3`, `addons/onboarding/views/onboarding_templates.xml:25`, `addons/onboarding/views/onboarding_templates.xml:67`, `addons/onboarding/views/onboarding_menus.xml:4`, `addons/onboarding/views/onboarding_menus.xml:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/onboarding/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/onboarding/tests/test_onboarding_concurrency.py`, `addons/onboarding/tests/case.py`, `addons/onboarding/tests/common.py`, `addons/onboarding/tests/test_onboarding.py`, `addons/onboarding/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `onboarding_onboarding_view_tree`, `onboarding_onboarding_view_form`, `onboarding_onboarding_step_view_tree`, `onboarding_onboarding_step_view_form`, `action_view_onboarding_onboarding`, `action_view_onboarding_step`, `onboarding_panel`, `onboarding_container`, `onboarding_step`, `menu_onboarding`, `menu_onboarding_step`
- Menus: 2; representative evidence: `addons/onboarding/views/onboarding_menus.xml:4`, `addons/onboarding/views/onboarding_menus.xml:9`
- Templates: 3; representative evidence: `addons/onboarding/views/onboarding_templates.xml:3`, `addons/onboarding/views/onboarding_templates.xml:25`, `addons/onboarding/views/onboarding_templates.xml:67`
- View/action field declarations: 12; representative evidence: `addons/onboarding/views/onboarding_views.xml:5`, `addons/onboarding/views/onboarding_views.xml:6`, `addons/onboarding/views/onboarding_views.xml:22`, `addons/onboarding/views/onboarding_views.xml:23`, `addons/onboarding/views/onboarding_views.xml:51`, `addons/onboarding/views/onboarding_views.xml:52`, `addons/onboarding/views/onboarding_views.xml:65`, `addons/onboarding/views/onboarding_views.xml:66`, `addons/onboarding/views/onboarding_views.xml:100`, `addons/onboarding/views/onboarding_views.xml:101`, `addons/onboarding/views/onboarding_views.xml:106`, `addons/onboarding/views/onboarding_views.xml:107`
- Browser assets: 1; representative files: `addons/onboarding/static/src/views/form/onboarding_step_form_controller.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/onboarding/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: `onboarding.progress` (addons/onboarding/models/onboarding_progress.py:14); `onboarding.progress.step` (addons/onboarding/models/onboarding_progress_step.py:8); `onboarding.onboarding` (addons/onboarding/models/onboarding_onboarding.py:8); `onboarding.onboarding.step` (addons/onboarding/models/onboarding_onboarding_step.py:9)
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

- `addons/onboarding/__init__.py`
- `addons/onboarding/__manifest__.py`
- `addons/onboarding/i18n/ar.po`
- `addons/onboarding/i18n/az.po`
- `addons/onboarding/i18n/bg.po`
- `addons/onboarding/i18n/bs.po`
- `addons/onboarding/i18n/ca.po`
- `addons/onboarding/i18n/cs.po`
- `addons/onboarding/i18n/da.po`
- `addons/onboarding/i18n/de.po`
- `addons/onboarding/i18n/el.po`
- `addons/onboarding/i18n/es.po`
- `addons/onboarding/i18n/es_419.po`
- `addons/onboarding/i18n/et.po`
- `addons/onboarding/i18n/fa.po`
- `addons/onboarding/i18n/fi.po`
- `addons/onboarding/i18n/fr.po`
- `addons/onboarding/i18n/he.po`
- `addons/onboarding/i18n/hi.po`
- `addons/onboarding/i18n/hr.po`
- `addons/onboarding/i18n/hu.po`
- `addons/onboarding/i18n/id.po`
- `addons/onboarding/i18n/it.po`
- `addons/onboarding/i18n/ja.po`
- `addons/onboarding/i18n/kab.po`
- `addons/onboarding/i18n/ko.po`
- `addons/onboarding/i18n/ku.po`
- `addons/onboarding/i18n/lo.po`
- `addons/onboarding/i18n/lt.po`
- `addons/onboarding/i18n/lv.po`
- `addons/onboarding/i18n/mn.po`
- `addons/onboarding/i18n/my.po`
- `addons/onboarding/i18n/nb.po`
- `addons/onboarding/i18n/nl.po`
- `addons/onboarding/i18n/onboarding.pot`
- `addons/onboarding/i18n/pl.po`
- `addons/onboarding/i18n/pt.po`
- `addons/onboarding/i18n/pt_BR.po`
- `addons/onboarding/i18n/ro.po`
- `addons/onboarding/i18n/ru.po`
- `addons/onboarding/i18n/sk.po`
- `addons/onboarding/i18n/sl.po`
- `addons/onboarding/i18n/sr@latin.po`
- `addons/onboarding/i18n/sv.po`
- `addons/onboarding/i18n/th.po`
- `addons/onboarding/i18n/tr.po`
- `addons/onboarding/i18n/uk.po`
- `addons/onboarding/i18n/uz.po`
- `addons/onboarding/i18n/vi.po`
- `addons/onboarding/i18n/zh_CN.po`
- `addons/onboarding/i18n/zh_TW.po`
- `addons/onboarding/models/__init__.py`
- `addons/onboarding/models/onboarding_onboarding.py`
- `addons/onboarding/models/onboarding_onboarding_step.py`
- `addons/onboarding/models/onboarding_progress.py`
- `addons/onboarding/models/onboarding_progress_step.py`
- `addons/onboarding/security/ir.access.csv`
- `addons/onboarding/static/src/img/onboarding_bg.png`
- `addons/onboarding/static/src/scss/onboarding.scss`
- `addons/onboarding/static/src/scss/onboarding.variables.dark.scss`
- `addons/onboarding/static/src/scss/onboarding.variables.scss`
- `addons/onboarding/static/src/views/form/onboarding_step_form_controller.js`
- `addons/onboarding/tests/__init__.py`
- `addons/onboarding/tests/case.py`
- `addons/onboarding/tests/common.py`
- `addons/onboarding/tests/test_onboarding.py`
- `addons/onboarding/tests/test_onboarding_concurrency.py`
- `addons/onboarding/views/onboarding_menus.xml`
- `addons/onboarding/views/onboarding_templates.xml`
- `addons/onboarding/views/onboarding_views.xml`
