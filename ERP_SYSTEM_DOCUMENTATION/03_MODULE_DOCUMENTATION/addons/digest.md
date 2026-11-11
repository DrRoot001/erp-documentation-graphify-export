# Module: digest

- **Module ID:** MOD-063
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/digest`
- **Manifest:** `addons/digest/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Send KPI Digests periodically
=============================

**Scope evidence:** The module contains 83 files, including 14 Python, 8 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `mail`, `portal`, `resource`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 2
- XML/data/view/template files: 8
- Browser asset files: 0
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 3
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/digest/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 56 methods, 0 constraint handlers, 1 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/digest/models/digest.py:24`, `addons/digest/models/res_config_settings.py:6`, `addons/digest/models/digest_tip.py:7`, `addons/digest/models/res_users.py:4`, `addons/digest/wizard/digest_test.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 3 route declarations.
- **Evidence:** `addons/digest/controllers/portal.py:14`, `addons/digest/controllers/portal.py:25`, `addons/digest/controllers/portal.py:62`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 8 XML files and 0 JavaScript/TypeScript files; static XML analysis found 28 record/template/menu identifiers.
- **Evidence:** `addons/digest/wizard/digest_test_views.xml:3`, `addons/digest/data/digest_data.xml:5`, `addons/digest/data/digest_data.xml:275`, `addons/digest/data/digest_data.xml:469`, `addons/digest/data/digest_data.xml:511`, `addons/digest/data/digest_tips_data.xml:4`, `addons/digest/data/digest_tips_data.xml:14`, `addons/digest/data/digest_tips_data.xml:26`, `addons/digest/data/digest_tips_data.xml:38`, `addons/digest/data/digest_tips_data.xml:50`, `addons/digest/data/digest_tips_data.xml:62`, `addons/digest/data/digest_tips_data.xml:75`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/digest/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 3 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/digest/__manifest__.py`, `addons/digest/models/digest.py`, `addons/digest/data/ir_cron_data.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/digest/tests/common.py`, `addons/digest/tests/test_digest.py`, `addons/digest/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 8; representative identifiers: `digest_test_view_form`, `digest_mail_layout`, `digest_mail_main`, `digest_section_mobile`, `digest_tool_kpi`, `digest_digest_default`, `digest_tip_digest_0`, `digest_tip_digest_1`, `digest_tip_digest_2`, `digest_tip_digest_3`, `digest_tip_digest_4`, `digest_tip_digest_5`, `digest_tip_digest_6`, `ir_cron_digest_scheduler_action`, `default_emails_digest`, `default_digest`, `digest_digest_view_tree`, `digest_digest_view_form`, `digest_digest_view_search`, `digest_digest_action`
- Menus: 2; representative evidence: `addons/digest/views/digest_views.xml:101`, `addons/digest/views/digest_views.xml:152`
- Templates: 5; representative evidence: `addons/digest/data/digest_data.xml:5`, `addons/digest/data/digest_data.xml:275`, `addons/digest/data/digest_data.xml:469`, `addons/digest/data/digest_data.xml:511`, `addons/digest/views/digest_templates.xml:2`
- View/action field declarations: 18; representative evidence: `addons/digest/wizard/digest_test_views.xml:5`, `addons/digest/wizard/digest_test_views.xml:6`, `addons/digest/views/digest_views.xml:5`, `addons/digest/views/digest_views.xml:6`, `addons/digest/views/digest_views.xml:18`, `addons/digest/views/digest_views.xml:19`, `addons/digest/views/digest_views.xml:81`, `addons/digest/views/digest_views.xml:82`, `addons/digest/views/digest_views.xml:96`, `addons/digest/views/digest_views.xml:110`, `addons/digest/views/digest_views.xml:111`, `addons/digest/views/digest_views.xml:121`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/digest/__manifest__.py`
- **HTTP entry points:** `addons/digest/controllers/portal.py:14`, `addons/digest/controllers/portal.py:25`, `addons/digest/controllers/portal.py:62`
- **Scheduled entry points:** `addons/digest/__manifest__.py`, `addons/digest/models/digest.py`, `addons/digest/data/ir_cron_data.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: `digest.digest` (addons/digest/models/digest.py:24); inherits `res.config.settings` (addons/digest/models/res_config_settings.py:6); `digest.tip` (addons/digest/models/digest_tip.py:7); inherits `res.users` (addons/digest/models/res_users.py:4); `digest.test` (addons/digest/wizard/digest_test.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 3
- Route evidence: `addons/digest/controllers/portal.py:14`, `addons/digest/controllers/portal.py:25`, `addons/digest/controllers/portal.py:62`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mail`, `portal`, `resource`
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

- `addons/digest/__init__.py`
- `addons/digest/__manifest__.py`
- `addons/digest/controllers/__init__.py`
- `addons/digest/controllers/portal.py`
- `addons/digest/data/digest_data.xml`
- `addons/digest/data/digest_tips_data.xml`
- `addons/digest/data/ir_cron_data.xml`
- `addons/digest/data/res_config_settings_data.xml`
- `addons/digest/i18n/ar.po`
- `addons/digest/i18n/az.po`
- `addons/digest/i18n/bg.po`
- `addons/digest/i18n/bs.po`
- `addons/digest/i18n/ca.po`
- `addons/digest/i18n/cs.po`
- `addons/digest/i18n/da.po`
- `addons/digest/i18n/de.po`
- `addons/digest/i18n/digest.pot`
- `addons/digest/i18n/el.po`
- `addons/digest/i18n/es.po`
- `addons/digest/i18n/es_419.po`
- `addons/digest/i18n/et.po`
- `addons/digest/i18n/fa.po`
- `addons/digest/i18n/fi.po`
- `addons/digest/i18n/fr.po`
- `addons/digest/i18n/gu.po`
- `addons/digest/i18n/he.po`
- `addons/digest/i18n/hi.po`
- `addons/digest/i18n/hr.po`
- `addons/digest/i18n/hu.po`
- `addons/digest/i18n/id.po`
- `addons/digest/i18n/is.po`
- `addons/digest/i18n/it.po`
- `addons/digest/i18n/ja.po`
- `addons/digest/i18n/kab.po`
- `addons/digest/i18n/km.po`
- `addons/digest/i18n/ko.po`
- `addons/digest/i18n/ku.po`
- `addons/digest/i18n/lo.po`
- `addons/digest/i18n/lt.po`
- `addons/digest/i18n/lv.po`
- `addons/digest/i18n/mn.po`
- `addons/digest/i18n/my.po`
- `addons/digest/i18n/nb.po`
- `addons/digest/i18n/nl.po`
- `addons/digest/i18n/pl.po`
- `addons/digest/i18n/pt.po`
- `addons/digest/i18n/pt_BR.po`
- `addons/digest/i18n/ro.po`
- `addons/digest/i18n/ru.po`
- `addons/digest/i18n/sk.po`
- `addons/digest/i18n/sl.po`
- `addons/digest/i18n/sr@latin.po`
- `addons/digest/i18n/sv.po`
- `addons/digest/i18n/th.po`
- `addons/digest/i18n/tr.po`
- `addons/digest/i18n/uk.po`
- `addons/digest/i18n/uz.po`
- `addons/digest/i18n/vi.po`
- `addons/digest/i18n/zh_CN.po`
- `addons/digest/i18n/zh_TW.po`
- `addons/digest/models/__init__.py`
- `addons/digest/models/digest.py`
- `addons/digest/models/digest_tip.py`
- `addons/digest/models/res_config_settings.py`
- `addons/digest/models/res_users.py`
- `addons/digest/security/ir.access.csv`
- `addons/digest/static/src/img/app_store.png`
- `addons/digest/static/src/img/google_play.png`
- `addons/digest/static/src/img/milk-alt-shortcuts.gif`
- `addons/digest/static/src/img/milk-avatar.gif`
- `addons/digest/static/src/img/milk-calculator.gif`
- `addons/digest/static/src/img/milk-ctrl+k.gif`
- `addons/digest/static/src/img/milk-following.png`
- `addons/digest/static/src/img/milk-notifications.png`
- `addons/digest/tests/__init__.py`
- `addons/digest/tests/common.py`
- `addons/digest/tests/test_digest.py`
- `addons/digest/views/digest_templates.xml`
- `addons/digest/views/digest_views.xml`
- `addons/digest/views/res_config_settings_views.xml`
- `addons/digest/wizard/__init__.py`
- `addons/digest/wizard/digest_test.py`
- `addons/digest/wizard/digest_test_views.xml`
