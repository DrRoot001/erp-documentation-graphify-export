# Module: website_links

- **Module ID:** MOD-622
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_links`
- **Manifest:** `addons/website_links/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Generate trackable & short URLs

**Manifest description:**

Generate short links with analytics trackers (UTM) to share your pages through marketing campaigns.
Those trackers can be used in Google Analytics to track clicks and visitors, or in Odoo reports to analyze the efficiency of those campaigns in terms of lead generation, related revenues (sales orders), recruitment, etc.

**Scope evidence:** The module contains 81 files, including 10 Python, 5 XML, and 6 JavaScript/TypeScript files. The manifest declares dependencies: `website`, `link_tracker`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 6
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_links/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 1 model declarations, 16 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/website_links/models/link_tracker.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 6 JavaScript/TypeScript files; static XML analysis found 5 record/template/menu identifiers.
- **Evidence:** `addons/website_links/views/link_tracker_views.xml:3`, `addons/website_links/views/link_tracker_views.xml:14`, `addons/website_links/views/website_links_graphs.xml:3`, `addons/website_links/views/website_links_template.xml:3`, `addons/website_links/views/website_links_template.xml:99`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_links/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/website_links/tests/test_link_tracker.py`, `addons/website_links/tests/test_controller.py`, `addons/website_links/tests/test_ui.py`, `addons/website_links/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `link_tracker_view_tree`, `Link Tracker`, `Link Statistics`, `create_shorten_url`, `Link Tracker`
- Menus: 1; representative evidence: `addons/website_links/views/link_tracker_views.xml:14`
- Templates: 3; representative evidence: `addons/website_links/views/website_links_graphs.xml:3`, `addons/website_links/views/website_links_template.xml:3`, `addons/website_links/views/website_links_template.xml:99`
- View/action field declarations: 2; representative evidence: `addons/website_links/views/link_tracker_views.xml:5`, `addons/website_links/views/link_tracker_views.xml:7`
- Browser assets: 6; representative files: `addons/website_links/static/src/services/website_custom_menus.js`, `addons/website_links/static/src/components/website_links_tags_wrapper.js`, `addons/website_links/static/src/interactions/website_links_code_editor.js`, `addons/website_links/static/src/interactions/website_links.js`, `addons/website_links/static/src/interactions/website_links_charts.js`, `addons/website_links/static/tests/tours/website_links.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_links/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `link.tracker` (addons/website_links/models/link_tracker.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website`, `link_tracker`
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

- `addons/website_links/__init__.py`
- `addons/website_links/__manifest__.py`
- `addons/website_links/controller/__init__.py`
- `addons/website_links/controller/main.py`
- `addons/website_links/i18n/af.po`
- `addons/website_links/i18n/ar.po`
- `addons/website_links/i18n/az.po`
- `addons/website_links/i18n/bg.po`
- `addons/website_links/i18n/bs.po`
- `addons/website_links/i18n/ca.po`
- `addons/website_links/i18n/cs.po`
- `addons/website_links/i18n/da.po`
- `addons/website_links/i18n/de.po`
- `addons/website_links/i18n/el.po`
- `addons/website_links/i18n/es.po`
- `addons/website_links/i18n/es_419.po`
- `addons/website_links/i18n/et.po`
- `addons/website_links/i18n/fa.po`
- `addons/website_links/i18n/fi.po`
- `addons/website_links/i18n/fr.po`
- `addons/website_links/i18n/gu.po`
- `addons/website_links/i18n/he.po`
- `addons/website_links/i18n/hi.po`
- `addons/website_links/i18n/hr.po`
- `addons/website_links/i18n/hu.po`
- `addons/website_links/i18n/id.po`
- `addons/website_links/i18n/is.po`
- `addons/website_links/i18n/it.po`
- `addons/website_links/i18n/ja.po`
- `addons/website_links/i18n/kab.po`
- `addons/website_links/i18n/km.po`
- `addons/website_links/i18n/ko.po`
- `addons/website_links/i18n/ku.po`
- `addons/website_links/i18n/lo.po`
- `addons/website_links/i18n/lt.po`
- `addons/website_links/i18n/lv.po`
- `addons/website_links/i18n/mk.po`
- `addons/website_links/i18n/mn.po`
- `addons/website_links/i18n/my.po`
- `addons/website_links/i18n/nb.po`
- `addons/website_links/i18n/nl.po`
- `addons/website_links/i18n/pl.po`
- `addons/website_links/i18n/pt.po`
- `addons/website_links/i18n/pt_BR.po`
- `addons/website_links/i18n/ro.po`
- `addons/website_links/i18n/ru.po`
- `addons/website_links/i18n/sk.po`
- `addons/website_links/i18n/sl.po`
- `addons/website_links/i18n/sr@latin.po`
- `addons/website_links/i18n/sv.po`
- `addons/website_links/i18n/th.po`
- `addons/website_links/i18n/tr.po`
- `addons/website_links/i18n/uk.po`
- `addons/website_links/i18n/uz.po`
- `addons/website_links/i18n/vi.po`
- `addons/website_links/i18n/website_links.pot`
- `addons/website_links/i18n/zh_CN.po`
- `addons/website_links/i18n/zh_TW.po`
- `addons/website_links/models/__init__.py`
- `addons/website_links/models/link_tracker.py`
- `addons/website_links/security/ir.access.csv`
- `addons/website_links/static/description/icon.png`
- `addons/website_links/static/description/icon.svg`
- `addons/website_links/static/description/icon_hi.png`
- `addons/website_links/static/img/default_favicon.png`
- `addons/website_links/static/src/components/website_links_tags_wrapper.js`
- `addons/website_links/static/src/css/website_links.css`
- `addons/website_links/static/src/interactions/website_links.js`
- `addons/website_links/static/src/interactions/website_links_charts.js`
- `addons/website_links/static/src/interactions/website_links_code_editor.js`
- `addons/website_links/static/src/services/website_custom_menus.js`
- `addons/website_links/static/src/xml/recent_link.xml`
- `addons/website_links/static/src/xml/website_links_tags_wrapper.xml`
- `addons/website_links/static/tests/tours/website_links.js`
- `addons/website_links/tests/__init__.py`
- `addons/website_links/tests/test_controller.py`
- `addons/website_links/tests/test_link_tracker.py`
- `addons/website_links/tests/test_ui.py`
- `addons/website_links/views/link_tracker_views.xml`
- `addons/website_links/views/website_links_graphs.xml`
- `addons/website_links/views/website_links_template.xml`
