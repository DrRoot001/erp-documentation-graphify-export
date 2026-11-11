# Module: link_tracker

- **Module ID:** MOD-348
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/link_tracker`
- **Manifest:** `addons/link_tracker/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Shorten URLs and use them to track clicks and UTMs

**Scope evidence:** The module contains 82 files, including 15 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `utm`, `mail`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/link_tracker/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 53 methods, 1 constraint handlers, 0 onchange handlers, and 5 dependency declarations.
- **Evidence:** `addons/link_tracker/models/mail_render_mixin.py:16`, `addons/link_tracker/models/link_tracker.py:23`, `addons/link_tracker/models/link_tracker.py:345`, `addons/link_tracker/models/link_tracker.py:373`, `addons/link_tracker/models/utm.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 14 record/template/menu identifiers.
- **Evidence:** `addons/link_tracker/views/utm_campaign_views.xml:3`, `addons/link_tracker/views/utm_campaign_views.xml:17`, `addons/link_tracker/views/link_tracker_views.xml:5`, `addons/link_tracker/views/link_tracker_views.xml:24`, `addons/link_tracker/views/link_tracker_views.xml:73`, `addons/link_tracker/views/link_tracker_views.xml:91`, `addons/link_tracker/views/link_tracker_views.xml:102`, `addons/link_tracker/views/link_tracker_views.xml:117`, `addons/link_tracker/views/link_tracker_views.xml:132`, `addons/link_tracker/views/link_tracker_views.xml:148`, `addons/link_tracker/views/link_tracker_views.xml:160`, `addons/link_tracker/views/link_tracker_views.xml:172`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/link_tracker/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/link_tracker/tests/test_link_tracker.py`, `addons/link_tracker/tests/test_tracker_http_requests.py`, `addons/link_tracker/tests/test_mail_render_mixin.py`, `addons/link_tracker/tests/common.py`, `addons/link_tracker/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `utm_campaign_view_form`, `utm_campaign_view_kanban`, `link_tracker_view_search`, `link_tracker_view_form`, `link_tracker_view_tree`, `link_tracker_view_graph`, `link_tracker_action`, `link_tracker_click_view_search`, `link_tracker_click_view_form`, `link_tracker_click_view_tree`, `link_tracker_click_view_graph`, `link_tracker_click_action_statistics`, `link_tracker_action_campaign`, `Link Tracker`
- Menus: 1; representative evidence: `addons/link_tracker/views/link_tracker_views.xml:201`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 26; representative evidence: `addons/link_tracker/views/utm_campaign_views.xml:5`, `addons/link_tracker/views/utm_campaign_views.xml:7`, `addons/link_tracker/views/utm_campaign_views.xml:19`, `addons/link_tracker/views/utm_campaign_views.xml:21`, `addons/link_tracker/views/link_tracker_views.xml:7`, `addons/link_tracker/views/link_tracker_views.xml:8`, `addons/link_tracker/views/link_tracker_views.xml:26`, `addons/link_tracker/views/link_tracker_views.xml:27`, `addons/link_tracker/views/link_tracker_views.xml:75`, `addons/link_tracker/views/link_tracker_views.xml:76`, `addons/link_tracker/views/link_tracker_views.xml:93`, `addons/link_tracker/views/link_tracker_views.xml:94`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/link_tracker/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `mail.render.mixin` (addons/link_tracker/models/mail_render_mixin.py:16); `link.tracker` (addons/link_tracker/models/link_tracker.py:23); `link.tracker.code` (addons/link_tracker/models/link_tracker.py:345); `link.tracker.click` (addons/link_tracker/models/link_tracker.py:373); inherits `utm.campaign` (addons/link_tracker/models/utm.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `utm`, `mail`
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

- `addons/link_tracker/__init__.py`
- `addons/link_tracker/__manifest__.py`
- `addons/link_tracker/controller/__init__.py`
- `addons/link_tracker/controller/main.py`
- `addons/link_tracker/i18n/af.po`
- `addons/link_tracker/i18n/ar.po`
- `addons/link_tracker/i18n/az.po`
- `addons/link_tracker/i18n/bg.po`
- `addons/link_tracker/i18n/bs.po`
- `addons/link_tracker/i18n/ca.po`
- `addons/link_tracker/i18n/cs.po`
- `addons/link_tracker/i18n/da.po`
- `addons/link_tracker/i18n/de.po`
- `addons/link_tracker/i18n/el.po`
- `addons/link_tracker/i18n/es.po`
- `addons/link_tracker/i18n/es_419.po`
- `addons/link_tracker/i18n/es_CL.po`
- `addons/link_tracker/i18n/et.po`
- `addons/link_tracker/i18n/eu.po`
- `addons/link_tracker/i18n/fa.po`
- `addons/link_tracker/i18n/fi.po`
- `addons/link_tracker/i18n/fo.po`
- `addons/link_tracker/i18n/fr.po`
- `addons/link_tracker/i18n/fr_BE.po`
- `addons/link_tracker/i18n/fr_CA.po`
- `addons/link_tracker/i18n/gl.po`
- `addons/link_tracker/i18n/gu.po`
- `addons/link_tracker/i18n/he.po`
- `addons/link_tracker/i18n/hi.po`
- `addons/link_tracker/i18n/hr.po`
- `addons/link_tracker/i18n/hu.po`
- `addons/link_tracker/i18n/id.po`
- `addons/link_tracker/i18n/is.po`
- `addons/link_tracker/i18n/it.po`
- `addons/link_tracker/i18n/ja.po`
- `addons/link_tracker/i18n/ka.po`
- `addons/link_tracker/i18n/kab.po`
- `addons/link_tracker/i18n/km.po`
- `addons/link_tracker/i18n/ko.po`
- `addons/link_tracker/i18n/ku.po`
- `addons/link_tracker/i18n/link_tracker.pot`
- `addons/link_tracker/i18n/lo.po`
- `addons/link_tracker/i18n/lt.po`
- `addons/link_tracker/i18n/lv.po`
- `addons/link_tracker/i18n/mk.po`
- `addons/link_tracker/i18n/ml_IN.po`
- `addons/link_tracker/i18n/mn.po`
- `addons/link_tracker/i18n/my.po`
- `addons/link_tracker/i18n/nb.po`
- `addons/link_tracker/i18n/nl.po`
- `addons/link_tracker/i18n/pl.po`
- `addons/link_tracker/i18n/pt.po`
- `addons/link_tracker/i18n/pt_BR.po`
- `addons/link_tracker/i18n/ro.po`
- `addons/link_tracker/i18n/ru.po`
- `addons/link_tracker/i18n/sk.po`
- `addons/link_tracker/i18n/sl.po`
- `addons/link_tracker/i18n/sq.po`
- `addons/link_tracker/i18n/sr@latin.po`
- `addons/link_tracker/i18n/sv.po`
- `addons/link_tracker/i18n/ta.po`
- `addons/link_tracker/i18n/th.po`
- `addons/link_tracker/i18n/tr.po`
- `addons/link_tracker/i18n/uk.po`
- `addons/link_tracker/i18n/uz.po`
- `addons/link_tracker/i18n/vi.po`
- `addons/link_tracker/i18n/zh_CN.po`
- `addons/link_tracker/i18n/zh_TW.po`
- `addons/link_tracker/models/__init__.py`
- `addons/link_tracker/models/link_tracker.py`
- `addons/link_tracker/models/mail_render_mixin.py`
- `addons/link_tracker/models/utm.py`
- `addons/link_tracker/security/ir.access.csv`
- `addons/link_tracker/tests/__init__.py`
- `addons/link_tracker/tests/common.py`
- `addons/link_tracker/tests/test_link_tracker.py`
- `addons/link_tracker/tests/test_mail_render_mixin.py`
- `addons/link_tracker/tests/test_tracker_http_requests.py`
- `addons/link_tracker/tools/__init__.py`
- `addons/link_tracker/tools/html.py`
- `addons/link_tracker/views/link_tracker_views.xml`
- `addons/link_tracker/views/utm_campaign_views.xml`
