# Module: website_event_exhibitor

- **Module ID:** MOD-612
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_event_exhibitor`
- **Manifest:** `addons/website_event_exhibitor/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Events`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Event: manage sponsors and exhibitors

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 84 files, including 14 Python, 14 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `website_event`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 2
- XML/data/view/template files: 14
- Browser asset files: 2
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_event_exhibitor/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 41 methods, 0 constraint handlers, 0 onchange handlers, and 13 dependency declarations.
- **Evidence:** `addons/website_event_exhibitor/models/event_sponsor.py:12`, `addons/website_event_exhibitor/models/event_sponsor_type.py:7`, `addons/website_event_exhibitor/models/event_type.py:7`, `addons/website_event_exhibitor/models/website_event_menu.py:7`, `addons/website_event_exhibitor/models/event_event.py:7`, `addons/website_event_exhibitor/models/website.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 3 route declarations.
- **Evidence:** `addons/website_event_exhibitor/controllers/exhibitor.py:30`, `addons/website_event_exhibitor/controllers/exhibitor.py:128`, `addons/website_event_exhibitor/controllers/exhibitor.py:183`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 14 XML files and 2 JavaScript/TypeScript files; static XML analysis found 46 record/template/menu identifiers.
- **Evidence:** `addons/website_event_exhibitor/report/website_event_exhibitor_reports.xml:4`, `addons/website_event_exhibitor/report/website_event_exhibitor_templates.xml:3`, `addons/website_event_exhibitor/data/event_sponsor_demo.xml:3`, `addons/website_event_exhibitor/data/event_sponsor_demo.xml:9`, `addons/website_event_exhibitor/data/event_sponsor_demo.xml:15`, `addons/website_event_exhibitor/data/event_sponsor_demo.xml:20`, `addons/website_event_exhibitor/data/event_sponsor_demo.xml:27`, `addons/website_event_exhibitor/data/event_sponsor_demo.xml:36`, `addons/website_event_exhibitor/data/event_sponsor_demo.xml:45`, `addons/website_event_exhibitor/data/event_sponsor_demo.xml:54`, `addons/website_event_exhibitor/data/event_sponsor_demo.xml:63`, `addons/website_event_exhibitor/data/event_sponsor_demo.xml:72`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_event_exhibitor/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/website_event_exhibitor/tests/test_sponsor_internals.py`, `addons/website_event_exhibitor/tests/common.py`, `addons/website_event_exhibitor/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 14; representative identifiers: `event.paperformat_event_full_page_ticket`, `event_report_full_page_ticket_layout_inherit_exhibitor`, `event_sponsor_0`, `event_sponsor_1`, `event_sponsor_2`, `event_sponsor_3`, `event_7_sponsor_0`, `event_7_sponsor_1`, `event_7_sponsor_2`, `event_7_sponsor_3`, `event_7_sponsor_4`, `event_7_sponsor_5`, `event_7_sponsor_6`, `event_7_sponsor_7`, `event_7_sponsor_8`, `event_7_sponsor_9`, `event.event_7`, `event_sponsor_type1`, `event_sponsor_type2`, `event_sponsor_type3`
- Menus: 1; representative evidence: `addons/website_event_exhibitor/views/event_menus.xml:4`
- Templates: 14; representative evidence: `addons/website_event_exhibitor/report/website_event_exhibitor_templates.xml:3`, `addons/website_event_exhibitor/views/event_exhibitor_templates_page.xml:4`, `addons/website_event_exhibitor/views/event_exhibitor_templates_page.xml:37`, `addons/website_event_exhibitor/views/event_exhibitor_templates_page.xml:135`, `addons/website_event_exhibitor/views/event_templates_sponsor.xml:4`, `addons/website_event_exhibitor/views/event_templates_sponsor.xml:33`, `addons/website_event_exhibitor/views/event_exhibitor_templates_list.xml:4`, `addons/website_event_exhibitor/views/event_exhibitor_templates_list.xml:33`, `addons/website_event_exhibitor/views/event_exhibitor_templates_list.xml:74`, `addons/website_event_exhibitor/views/event_exhibitor_templates_list.xml:139`, `addons/website_event_exhibitor/views/event_exhibitor_templates_list.xml:207`, `addons/website_event_exhibitor/views/event_exhibitor_templates_list.xml:225`
- View/action field declarations: 23; representative evidence: `addons/website_event_exhibitor/views/event_event_views.xml:6`, `addons/website_event_exhibitor/views/event_event_views.xml:9`, `addons/website_event_exhibitor/views/event_event_views.xml:29`, `addons/website_event_exhibitor/views/event_event_views.xml:31`, `addons/website_event_exhibitor/views/event_type_views.xml:5`, `addons/website_event_exhibitor/views/event_type_views.xml:7`, `addons/website_event_exhibitor/views/event_sponsor_views.xml:7`, `addons/website_event_exhibitor/views/event_sponsor_views.xml:8`, `addons/website_event_exhibitor/views/event_sponsor_views.xml:23`, `addons/website_event_exhibitor/views/event_sponsor_views.xml:24`, `addons/website_event_exhibitor/views/event_sponsor_views.xml:35`, `addons/website_event_exhibitor/views/event_sponsor_views.xml:47`
- Browser assets: 2; representative files: `addons/website_event_exhibitor/static/src/interactions/exhibitor_connect.js`, `addons/website_event_exhibitor/static/src/components/exhibitor_connect_closed_dialog/exhibitor_connect_closed_dialog.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_event_exhibitor/__manifest__.py`
- **HTTP entry points:** `addons/website_event_exhibitor/controllers/exhibitor.py:30`, `addons/website_event_exhibitor/controllers/exhibitor.py:128`, `addons/website_event_exhibitor/controllers/exhibitor.py:183`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: `event.sponsor` (addons/website_event_exhibitor/models/event_sponsor.py:12); `event.sponsor.type` (addons/website_event_exhibitor/models/event_sponsor_type.py:7); inherits `event.type` (addons/website_event_exhibitor/models/event_type.py:7); inherits `website.event.menu` (addons/website_event_exhibitor/models/website_event_menu.py:7); inherits `event.event` (addons/website_event_exhibitor/models/event_event.py:7); inherits `website` (addons/website_event_exhibitor/models/website.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 3
- Route evidence: `addons/website_event_exhibitor/controllers/exhibitor.py:30`, `addons/website_event_exhibitor/controllers/exhibitor.py:128`, `addons/website_event_exhibitor/controllers/exhibitor.py:183`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_event`
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

- `addons/website_event_exhibitor/__init__.py`
- `addons/website_event_exhibitor/__manifest__.py`
- `addons/website_event_exhibitor/controllers/__init__.py`
- `addons/website_event_exhibitor/controllers/exhibitor.py`
- `addons/website_event_exhibitor/data/event_demo.xml`
- `addons/website_event_exhibitor/data/event_sponsor_data.xml`
- `addons/website_event_exhibitor/data/event_sponsor_demo.xml`
- `addons/website_event_exhibitor/i18n/ar.po`
- `addons/website_event_exhibitor/i18n/az.po`
- `addons/website_event_exhibitor/i18n/bg.po`
- `addons/website_event_exhibitor/i18n/bs.po`
- `addons/website_event_exhibitor/i18n/ca.po`
- `addons/website_event_exhibitor/i18n/cs.po`
- `addons/website_event_exhibitor/i18n/da.po`
- `addons/website_event_exhibitor/i18n/de.po`
- `addons/website_event_exhibitor/i18n/el.po`
- `addons/website_event_exhibitor/i18n/es.po`
- `addons/website_event_exhibitor/i18n/es_419.po`
- `addons/website_event_exhibitor/i18n/et.po`
- `addons/website_event_exhibitor/i18n/fa.po`
- `addons/website_event_exhibitor/i18n/fi.po`
- `addons/website_event_exhibitor/i18n/fr.po`
- `addons/website_event_exhibitor/i18n/he.po`
- `addons/website_event_exhibitor/i18n/hi.po`
- `addons/website_event_exhibitor/i18n/hr.po`
- `addons/website_event_exhibitor/i18n/hu.po`
- `addons/website_event_exhibitor/i18n/id.po`
- `addons/website_event_exhibitor/i18n/it.po`
- `addons/website_event_exhibitor/i18n/ja.po`
- `addons/website_event_exhibitor/i18n/kab.po`
- `addons/website_event_exhibitor/i18n/ko.po`
- `addons/website_event_exhibitor/i18n/ku.po`
- `addons/website_event_exhibitor/i18n/lo.po`
- `addons/website_event_exhibitor/i18n/lt.po`
- `addons/website_event_exhibitor/i18n/lv.po`
- `addons/website_event_exhibitor/i18n/mn.po`
- `addons/website_event_exhibitor/i18n/my.po`
- `addons/website_event_exhibitor/i18n/nb.po`
- `addons/website_event_exhibitor/i18n/nl.po`
- `addons/website_event_exhibitor/i18n/pl.po`
- `addons/website_event_exhibitor/i18n/pt.po`
- `addons/website_event_exhibitor/i18n/pt_BR.po`
- `addons/website_event_exhibitor/i18n/ro.po`
- `addons/website_event_exhibitor/i18n/ru.po`
- `addons/website_event_exhibitor/i18n/sk.po`
- `addons/website_event_exhibitor/i18n/sl.po`
- `addons/website_event_exhibitor/i18n/sr@latin.po`
- `addons/website_event_exhibitor/i18n/sv.po`
- `addons/website_event_exhibitor/i18n/th.po`
- `addons/website_event_exhibitor/i18n/tr.po`
- `addons/website_event_exhibitor/i18n/uk.po`
- `addons/website_event_exhibitor/i18n/uz.po`
- `addons/website_event_exhibitor/i18n/vi.po`
- `addons/website_event_exhibitor/i18n/website_event_exhibitor.pot`
- `addons/website_event_exhibitor/i18n/zh_CN.po`
- `addons/website_event_exhibitor/i18n/zh_TW.po`
- `addons/website_event_exhibitor/models/__init__.py`
- `addons/website_event_exhibitor/models/event_event.py`
- `addons/website_event_exhibitor/models/event_sponsor.py`
- `addons/website_event_exhibitor/models/event_sponsor_type.py`
- `addons/website_event_exhibitor/models/event_type.py`
- `addons/website_event_exhibitor/models/website.py`
- `addons/website_event_exhibitor/models/website_event_menu.py`
- `addons/website_event_exhibitor/report/website_event_exhibitor_reports.xml`
- `addons/website_event_exhibitor/report/website_event_exhibitor_templates.xml`
- `addons/website_event_exhibitor/security/ir.access.csv`
- `addons/website_event_exhibitor/static/src/components/exhibitor_connect_closed_dialog/exhibitor_connect_closed_dialog.js`
- `addons/website_event_exhibitor/static/src/components/exhibitor_connect_closed_dialog/exhibitor_connect_closed_dialog.xml`
- `addons/website_event_exhibitor/static/src/img/event_sponsor_default.svg`
- `addons/website_event_exhibitor/static/src/interactions/exhibitor_connect.js`
- `addons/website_event_exhibitor/static/src/scss/event_exhibitor_templates.scss`
- `addons/website_event_exhibitor/static/src/scss/event_full_page_ticket_report.scss`
- `addons/website_event_exhibitor/static/src/scss/event_templates_sponsor.scss`
- `addons/website_event_exhibitor/static/src/website_builder/event_page_option.xml`
- `addons/website_event_exhibitor/tests/__init__.py`
- `addons/website_event_exhibitor/tests/common.py`
- `addons/website_event_exhibitor/tests/test_sponsor_internals.py`
- `addons/website_event_exhibitor/views/event_event_views.xml`
- `addons/website_event_exhibitor/views/event_exhibitor_templates_list.xml`
- `addons/website_event_exhibitor/views/event_exhibitor_templates_page.xml`
- `addons/website_event_exhibitor/views/event_menus.xml`
- `addons/website_event_exhibitor/views/event_sponsor_views.xml`
- `addons/website_event_exhibitor/views/event_templates_sponsor.xml`
- `addons/website_event_exhibitor/views/event_type_views.xml`
