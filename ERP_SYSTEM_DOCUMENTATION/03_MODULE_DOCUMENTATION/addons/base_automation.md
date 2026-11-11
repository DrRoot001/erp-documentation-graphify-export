# Module: base_automation

- **Module ID:** MOD-035
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/base_automation`
- **Manifest:** `addons/base_automation/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module allows to implement automation rules for any object.
================================================================

Use automation rules to automatically trigger actions for various screens.

**Example:** A lead created by a specific user may be automatically set to a specific
Sales Team, or an opportunity which still has status pending after 14 days might
trigger an automatic reminder email.

**Scope evidence:** The module contains 92 files, including 10 Python, 7 XML, and 8 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `digest`, `resource`, `mail`, `sms`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 2
- XML/data/view/template files: 7
- Browser asset files: 8
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 8
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/base_automation/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 68 methods, 4 constraint handlers, 3 onchange handlers, and 14 dependency declarations.
- **Evidence:** `addons/base_automation/models/ir_actions_server.py:11`, `addons/base_automation/models/ir_actions_server.py:74`, `addons/base_automation/models/base_automation.py:129`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/base_automation/controllers/main.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 8 JavaScript/TypeScript files; static XML analysis found 9 record/template/menu identifiers.
- **Evidence:** `addons/base_automation/data/digest_data.xml:4`, `addons/base_automation/data/base_automation_data.xml:4`, `addons/base_automation/views/ir_actions_server_views.xml:5`, `addons/base_automation/views/base_automation_views.xml:5`, `addons/base_automation/views/base_automation_views.xml:160`, `addons/base_automation/views/base_automation_views.xml:173`, `addons/base_automation/views/base_automation_views.xml:229`, `addons/base_automation/views/base_automation_views.xml:243`, `addons/base_automation/views/base_automation_views.xml:265`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/base_automation/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 8 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/base_automation/models/ir_actions_server.py`, `addons/base_automation/models/base_automation.py`, `addons/base_automation/controllers/main.py`, `addons/base_automation/data/base_automation_data.xml`, `addons/base_automation/views/ir_actions_server_views.xml`, `addons/base_automation/views/base_automation_views.xml`, `addons/base_automation/tests/test_mail_composer.py`, `addons/base_automation/tests/test_automation.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/base_automation/tests/__init__.py`, `addons/base_automation/tests/test_mail_composer.py`, `addons/base_automation/tests/test_automation.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `digest_tip_base_automation_0`, `ir_cron_data_base_automation_check`, `view_server_action_form`, `view_base_automation_form`, `view_base_automation_tree`, `view_base_automation_kanban`, `view_base_automation_search`, `base_automation_act`, `menu_base_automation_form`
- Menus: 1; representative evidence: `addons/base_automation/views/base_automation_views.xml:265`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 12; representative evidence: `addons/base_automation/views/ir_actions_server_views.xml:7`, `addons/base_automation/views/ir_actions_server_views.xml:9`, `addons/base_automation/views/base_automation_views.xml:7`, `addons/base_automation/views/base_automation_views.xml:8`, `addons/base_automation/views/base_automation_views.xml:162`, `addons/base_automation/views/base_automation_views.xml:163`, `addons/base_automation/views/base_automation_views.xml:175`, `addons/base_automation/views/base_automation_views.xml:176`, `addons/base_automation/views/base_automation_views.xml:231`, `addons/base_automation/views/base_automation_views.xml:232`, `addons/base_automation/views/base_automation_views.xml:245`, `addons/base_automation/views/base_automation_views.xml:247`
- Browser assets: 8; representative files: `addons/base_automation/static/src/utils.js`, `addons/base_automation/static/src/group_config_menu_patch.js`, `addons/base_automation/static/src/base_automation_error_dialog.js`, `addons/base_automation/static/src/base_automation_trigger_selection_field.js`, `addons/base_automation/static/src/base_automation_actions_one2many_field.js`, `addons/base_automation/static/tests/base_automation_error_dialog.test.js`, `addons/base_automation/static/tests/base_automation.test.js`, `addons/base_automation/static/tests/kanban_header_patch.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/base_automation/__manifest__.py`
- **HTTP entry points:** `addons/base_automation/controllers/main.py:6`
- **Scheduled entry points:** `addons/base_automation/models/ir_actions_server.py`, `addons/base_automation/models/base_automation.py`, `addons/base_automation/controllers/main.py`, `addons/base_automation/data/base_automation_data.xml`, `addons/base_automation/views/ir_actions_server_views.xml`, `addons/base_automation/views/base_automation_views.xml`, `addons/base_automation/tests/test_mail_composer.py`, `addons/base_automation/tests/test_automation.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `ir.actions.server` (addons/base_automation/models/ir_actions_server.py:11); inherits `ir.cron` (addons/base_automation/models/ir_actions_server.py:74); `base.automation` (addons/base_automation/models/base_automation.py:129)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/base_automation/controllers/main.py:6`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `digest`, `resource`, `mail`, `sms`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/base_automation/__init__.py`
- `addons/base_automation/__manifest__.py`
- `addons/base_automation/controllers/__init__.py`
- `addons/base_automation/controllers/main.py`
- `addons/base_automation/data/base_automation_data.xml`
- `addons/base_automation/data/digest_data.xml`
- `addons/base_automation/i18n/af.po`
- `addons/base_automation/i18n/ar.po`
- `addons/base_automation/i18n/az.po`
- `addons/base_automation/i18n/base_automation.pot`
- `addons/base_automation/i18n/bg.po`
- `addons/base_automation/i18n/bs.po`
- `addons/base_automation/i18n/ca.po`
- `addons/base_automation/i18n/cs.po`
- `addons/base_automation/i18n/da.po`
- `addons/base_automation/i18n/de.po`
- `addons/base_automation/i18n/el.po`
- `addons/base_automation/i18n/es.po`
- `addons/base_automation/i18n/es_419.po`
- `addons/base_automation/i18n/es_CL.po`
- `addons/base_automation/i18n/et.po`
- `addons/base_automation/i18n/eu.po`
- `addons/base_automation/i18n/fa.po`
- `addons/base_automation/i18n/fi.po`
- `addons/base_automation/i18n/fo.po`
- `addons/base_automation/i18n/fr.po`
- `addons/base_automation/i18n/fr_BE.po`
- `addons/base_automation/i18n/fr_CA.po`
- `addons/base_automation/i18n/gl.po`
- `addons/base_automation/i18n/gu.po`
- `addons/base_automation/i18n/he.po`
- `addons/base_automation/i18n/hi.po`
- `addons/base_automation/i18n/hr.po`
- `addons/base_automation/i18n/hu.po`
- `addons/base_automation/i18n/id.po`
- `addons/base_automation/i18n/is.po`
- `addons/base_automation/i18n/it.po`
- `addons/base_automation/i18n/ja.po`
- `addons/base_automation/i18n/ka.po`
- `addons/base_automation/i18n/kab.po`
- `addons/base_automation/i18n/kk.po`
- `addons/base_automation/i18n/km.po`
- `addons/base_automation/i18n/ko.po`
- `addons/base_automation/i18n/ku.po`
- `addons/base_automation/i18n/lo.po`
- `addons/base_automation/i18n/lt.po`
- `addons/base_automation/i18n/lv.po`
- `addons/base_automation/i18n/mk.po`
- `addons/base_automation/i18n/mn.po`
- `addons/base_automation/i18n/my.po`
- `addons/base_automation/i18n/nb.po`
- `addons/base_automation/i18n/nl.po`
- `addons/base_automation/i18n/pl.po`
- `addons/base_automation/i18n/pt.po`
- `addons/base_automation/i18n/pt_BR.po`
- `addons/base_automation/i18n/ro.po`
- `addons/base_automation/i18n/ru.po`
- `addons/base_automation/i18n/sk.po`
- `addons/base_automation/i18n/sl.po`
- `addons/base_automation/i18n/sq.po`
- `addons/base_automation/i18n/sr@latin.po`
- `addons/base_automation/i18n/sv.po`
- `addons/base_automation/i18n/ta.po`
- `addons/base_automation/i18n/th.po`
- `addons/base_automation/i18n/tr.po`
- `addons/base_automation/i18n/uk.po`
- `addons/base_automation/i18n/uz.po`
- `addons/base_automation/i18n/vi.po`
- `addons/base_automation/i18n/zh_CN.po`
- `addons/base_automation/i18n/zh_TW.po`
- `addons/base_automation/models/__init__.py`
- `addons/base_automation/models/base_automation.py`
- `addons/base_automation/models/ir_actions_server.py`
- `addons/base_automation/security/ir.access.csv`
- `addons/base_automation/static/img/automation.svg`
- `addons/base_automation/static/src/base_automation.scss`
- `addons/base_automation/static/src/base_automation_actions_one2many_field.js`
- `addons/base_automation/static/src/base_automation_actions_one2many_field.xml`
- `addons/base_automation/static/src/base_automation_error_dialog.js`
- `addons/base_automation/static/src/base_automation_error_dialog.xml`
- `addons/base_automation/static/src/base_automation_trigger_selection_field.js`
- `addons/base_automation/static/src/base_automation_trigger_selection_field.xml`
- `addons/base_automation/static/src/group_config_menu_patch.js`
- `addons/base_automation/static/src/utils.js`
- `addons/base_automation/static/tests/base_automation.test.js`
- `addons/base_automation/static/tests/base_automation_error_dialog.test.js`
- `addons/base_automation/static/tests/kanban_header_patch.test.js`
- `addons/base_automation/tests/__init__.py`
- `addons/base_automation/tests/test_automation.py`
- `addons/base_automation/tests/test_mail_composer.py`
- `addons/base_automation/views/base_automation_views.xml`
- `addons/base_automation/views/ir_actions_server_views.xml`
