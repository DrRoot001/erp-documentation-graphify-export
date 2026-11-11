# Module: website_slides_forum

- **Module ID:** MOD-644
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_slides_forum`
- **Manifest:** `addons/website_slides_forum/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/eLearning`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Allows to link forum on a course

**Manifest description:**

A Slide channel can be linked to forum. Also, profiles from slide and forum are regrouped together

**Scope evidence:** The module contains 68 files, including 9 Python, 9 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `website_slides`, `website_forum`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 2
- XML/data/view/template files: 9
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_slides_forum/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 15 methods, 0 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/website_slides_forum/models/slide_channel.py:7`, `addons/website_slides_forum/models/forum_forum.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/website_slides_forum/controllers/main.py`, `addons/website_slides_forum/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 9 XML files and 0 JavaScript/TypeScript files; static XML analysis found 22 record/template/menu identifiers.
- **Evidence:** `addons/website_slides_forum/data/slide_channel_demo.xml:4`, `addons/website_slides_forum/data/slide_channel_demo.xml:7`, `addons/website_slides_forum/data/slide_channel_demo.xml:11`, `addons/website_slides_forum/data/slide_channel_demo.xml:14`, `addons/website_slides_forum/data/slide_channel_demo.xml:18`, `addons/website_slides_forum/data/slide_channel_demo.xml:27`, `addons/website_slides_forum/data/slide_channel_demo.xml:34`, `addons/website_slides_forum/views/website_slides_templates.xml:3`, `addons/website_slides_forum/views/website_slides_templates.xml:13`, `addons/website_slides_forum/views/res_config_settings_views.xml:3`, `addons/website_slides_forum/views/forum_forum_templates.xml:4`, `addons/website_slides_forum/views/forum_forum_templates.xml:14`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_slides_forum/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/website_slides_forum/tests/__init__.py`, `addons/website_slides_forum/tests/test_website_slides_forum.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 9; representative identifiers: `forum_forum_demo_channel_0`, `website_slides.slide_channel_demo_0_gard_0`, `forum_forum_demo_channel_2`, `website_slides.slide_channel_demo_2_gard2`, `forum_post_O_0`, `forum_post_O_0_answer_0`, `forum_post_2_0`, `course_main`, `slide_fullscreen`, `res_config_settings_view_form`, `website_slides_forum_index`, `website_slides_forum_breadcrumb`, `forum_all_all_entries`, `forum_forum_view_form`, `forum_forum_view_tree_slides`, `forum_forum_action_channel`, `website_slides_menu_forum`, `website_slides_menu_forum_forum`, `website_slides_menu_forum_post`, `website_slides_forum_channel_inherit_view_form`
- Menus: 3; representative evidence: `addons/website_slides_forum/views/website_slides_menu_views.xml:3`, `addons/website_slides_forum/views/website_slides_menu_views.xml:7`, `addons/website_slides_forum/views/website_slides_menu_views.xml:12`
- Templates: 5; representative evidence: `addons/website_slides_forum/views/website_slides_templates.xml:3`, `addons/website_slides_forum/views/website_slides_templates.xml:13`, `addons/website_slides_forum/views/forum_forum_templates.xml:4`, `addons/website_slides_forum/views/forum_forum_templates.xml:14`, `addons/website_slides_forum/views/forum_forum_templates.xml:38`
- View/action field declarations: 14; representative evidence: `addons/website_slides_forum/views/res_config_settings_views.xml:5`, `addons/website_slides_forum/views/res_config_settings_views.xml:8`, `addons/website_slides_forum/views/forum_forum_views.xml:5`, `addons/website_slides_forum/views/forum_forum_views.xml:7`, `addons/website_slides_forum/views/forum_forum_views.xml:29`, `addons/website_slides_forum/views/forum_forum_views.xml:33`, `addons/website_slides_forum/views/forum_forum_views.xml:43`, `addons/website_slides_forum/views/forum_forum_views.xml:44`, `addons/website_slides_forum/views/slide_channel_views.xml:5`, `addons/website_slides_forum/views/slide_channel_views.xml:7`, `addons/website_slides_forum/views/forum_post_views.xml:6`, `addons/website_slides_forum/views/forum_post_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_slides_forum/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `slide.channel` (addons/website_slides_forum/models/slide_channel.py:7); inherits `forum.forum` (addons/website_slides_forum/models/forum_forum.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_slides`, `website_forum`
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

- `addons/website_slides_forum/__init__.py`
- `addons/website_slides_forum/__manifest__.py`
- `addons/website_slides_forum/controllers/__init__.py`
- `addons/website_slides_forum/controllers/main.py`
- `addons/website_slides_forum/data/slide_channel_demo.xml`
- `addons/website_slides_forum/i18n/ar.po`
- `addons/website_slides_forum/i18n/az.po`
- `addons/website_slides_forum/i18n/bg.po`
- `addons/website_slides_forum/i18n/bs.po`
- `addons/website_slides_forum/i18n/ca.po`
- `addons/website_slides_forum/i18n/cs.po`
- `addons/website_slides_forum/i18n/da.po`
- `addons/website_slides_forum/i18n/de.po`
- `addons/website_slides_forum/i18n/el.po`
- `addons/website_slides_forum/i18n/es.po`
- `addons/website_slides_forum/i18n/es_419.po`
- `addons/website_slides_forum/i18n/et.po`
- `addons/website_slides_forum/i18n/fa.po`
- `addons/website_slides_forum/i18n/fi.po`
- `addons/website_slides_forum/i18n/fr.po`
- `addons/website_slides_forum/i18n/he.po`
- `addons/website_slides_forum/i18n/hi.po`
- `addons/website_slides_forum/i18n/hr.po`
- `addons/website_slides_forum/i18n/hu.po`
- `addons/website_slides_forum/i18n/id.po`
- `addons/website_slides_forum/i18n/it.po`
- `addons/website_slides_forum/i18n/ja.po`
- `addons/website_slides_forum/i18n/kab.po`
- `addons/website_slides_forum/i18n/ko.po`
- `addons/website_slides_forum/i18n/ku.po`
- `addons/website_slides_forum/i18n/lo.po`
- `addons/website_slides_forum/i18n/lt.po`
- `addons/website_slides_forum/i18n/lv.po`
- `addons/website_slides_forum/i18n/mn.po`
- `addons/website_slides_forum/i18n/my.po`
- `addons/website_slides_forum/i18n/nb.po`
- `addons/website_slides_forum/i18n/nl.po`
- `addons/website_slides_forum/i18n/pl.po`
- `addons/website_slides_forum/i18n/pt.po`
- `addons/website_slides_forum/i18n/pt_BR.po`
- `addons/website_slides_forum/i18n/ro.po`
- `addons/website_slides_forum/i18n/ru.po`
- `addons/website_slides_forum/i18n/sk.po`
- `addons/website_slides_forum/i18n/sl.po`
- `addons/website_slides_forum/i18n/sr@latin.po`
- `addons/website_slides_forum/i18n/sv.po`
- `addons/website_slides_forum/i18n/th.po`
- `addons/website_slides_forum/i18n/tr.po`
- `addons/website_slides_forum/i18n/uk.po`
- `addons/website_slides_forum/i18n/uz.po`
- `addons/website_slides_forum/i18n/vi.po`
- `addons/website_slides_forum/i18n/website_slides_forum.pot`
- `addons/website_slides_forum/i18n/zh_CN.po`
- `addons/website_slides_forum/i18n/zh_TW.po`
- `addons/website_slides_forum/models/__init__.py`
- `addons/website_slides_forum/models/forum_forum.py`
- `addons/website_slides_forum/models/slide_channel.py`
- `addons/website_slides_forum/security/ir.access.csv`
- `addons/website_slides_forum/static/src/website_builder/slides_forum_page_option.xml`
- `addons/website_slides_forum/tests/__init__.py`
- `addons/website_slides_forum/tests/test_website_slides_forum.py`
- `addons/website_slides_forum/views/forum_forum_templates.xml`
- `addons/website_slides_forum/views/forum_forum_views.xml`
- `addons/website_slides_forum/views/forum_post_views.xml`
- `addons/website_slides_forum/views/res_config_settings_views.xml`
- `addons/website_slides_forum/views/slide_channel_views.xml`
- `addons/website_slides_forum/views/website_slides_menu_views.xml`
- `addons/website_slides_forum/views/website_slides_templates.xml`
