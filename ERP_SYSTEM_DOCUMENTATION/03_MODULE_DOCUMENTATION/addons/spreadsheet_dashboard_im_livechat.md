# Module: spreadsheet_dashboard_im_livechat

- **Module ID:** MOD-551
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/spreadsheet_dashboard_im_livechat`
- **Manifest:** `addons/spreadsheet_dashboard_im_livechat/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Productivity/Dashboard`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Spreadsheet

**Manifest description:**

Spreadsheet

**Scope evidence:** The module contains 57 files, including 2 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `spreadsheet_dashboard`, `im_livechat`.

## 2. Module structure

- Model/business logic files: 0
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 12 record/template/menu identifiers.
- **Evidence:** `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:3`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:21`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:38`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:55`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:72`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:14`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:31`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:48`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:65`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:82`, `addons/spreadsheet_dashboard_im_livechat/data/dashboards.xml:4`, `addons/spreadsheet_dashboard_im_livechat/data/dashboards.xml:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `ongoing_sessions_all_action`, `ongoing_sessions_escalated_action`, `ongoing_sessions_agents_in_call_action`, `ongoing_sessions_handle_by_agent_action`, `ongoing_sessions_handle_by_bot_action`, `Ongoing Sessions`, `Escalated Sessions`, `Ongoing Call Sessions`, `Sessions Handled by Agent`, `Sessions Handled by Bot`, `spreadsheet_dashboard_livechat`, `spreadsheet_dashboard_livechat_ongoing`
- Menus: 5; representative evidence: `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:14`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:31`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:48`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:65`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:82`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 5; representative evidence: `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:7`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:24`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:41`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:58`, `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml:75`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/spreadsheet_dashboard_im_livechat/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `spreadsheet_dashboard`, `im_livechat`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Not found
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/spreadsheet_dashboard_im_livechat/__init__.py`
- `addons/spreadsheet_dashboard_im_livechat/__manifest__.py`
- `addons/spreadsheet_dashboard_im_livechat/data/dashboards.xml`
- `addons/spreadsheet_dashboard_im_livechat/data/files/livechat_dashboard.json`
- `addons/spreadsheet_dashboard_im_livechat/data/files/livechat_ongoing_dashboard.json`
- `addons/spreadsheet_dashboard_im_livechat/data/files/livechat_sample_dashboard.json`
- `addons/spreadsheet_dashboard_im_livechat/data/files/livechat_sample_ongoing_dashboard.json`
- `addons/spreadsheet_dashboard_im_livechat/data/livechat_ongoing_sessions_actions.xml`
- `addons/spreadsheet_dashboard_im_livechat/i18n/ar.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/az.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/bg.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/bs.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/ca.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/cs.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/da.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/de.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/el.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/es.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/es_419.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/et.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/fa.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/fi.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/fr.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/he.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/hi.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/hr.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/hu.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/id.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/it.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/ja.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/kab.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/ko.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/ku.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/lo.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/lt.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/lv.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/mn.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/my.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/nb.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/nl.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/pl.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/pt.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/pt_BR.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/ro.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/ru.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/sk.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/sl.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/spreadsheet_dashboard_im_livechat.pot`
- `addons/spreadsheet_dashboard_im_livechat/i18n/sr@latin.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/sv.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/th.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/tr.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/uk.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/uz.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/vi.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/zh_CN.po`
- `addons/spreadsheet_dashboard_im_livechat/i18n/zh_TW.po`
