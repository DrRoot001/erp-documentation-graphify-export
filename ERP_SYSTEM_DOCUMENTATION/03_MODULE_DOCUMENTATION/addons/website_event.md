# Module: website_event

- **Module ID:** MOD-606
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_event`
- **Manifest:** `addons/website_event/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Marketing/Events`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Publish events, sell tickets

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 166 files, including 28 Python, 35 XML, and 23 JavaScript/TypeScript files. The manifest declares dependencies: `event`, `website`, `website_partner`, `website_mail`, `html_builder`.

## 2. Module structure

- Model/business logic files: 12
- Controller/API files: 3
- XML/data/view/template files: 35
- Browser asset files: 23
- Security files: 2
- Test files: 10
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_event/security/ir.access.csv`, `addons/website_event/security/event_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 12 model declarations, 136 methods, 1 constraint handlers, 0 onchange handlers, and 15 dependency declarations.
- **Evidence:** `addons/website_event/models/website_track.py:6`, `addons/website_event/models/website_menu.py:9`, `addons/website_event/models/website_snippet_filter.py:9`, `addons/website_event/models/event_slot.py:6`, `addons/website_event/models/event_type.py:6`, `addons/website_event/models/event_tag_category.py:7`, `addons/website_event/models/website_visitor.py:8`, `addons/website_event/models/event_tag.py:6`, `addons/website_event/models/website_event_menu.py:9`, `addons/website_event/models/event_event.py:21`, `addons/website_event/models/event_registration.py:6`, `addons/website_event/models/website.py:10`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 9 route declarations.
- **Evidence:** `addons/website_event/controllers/community.py:10`, `addons/website_event/controllers/main.py:39`, `addons/website_event/controllers/main.py:196`, `addons/website_event/controllers/main.py:244`, `addons/website_event/controllers/main.py:254`, `addons/website_event/controllers/main.py:309`, `addons/website_event/controllers/main.py:372`, `addons/website_event/controllers/main.py:490`, `addons/website_event/controllers/main.py:517`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 35 XML files and 23 JavaScript/TypeScript files; static XML analysis found 180 record/template/menu identifiers.
- **Evidence:** `addons/website_event/security/event_security.xml:2`, `addons/website_event/data/website_snippet_data.xml:5`, `addons/website_event/data/website_snippet_data.xml:15`, `addons/website_event/data/website_snippet_data.xml:23`, `addons/website_event/data/website_snippet_data.xml:30`, `addons/website_event/data/event_data.xml:5`, `addons/website_event/data/event_data.xml:11`, `addons/website_event/data/event_data.xml:16`, `addons/website_event/data/event_data.xml:21`, `addons/website_event/data/event_data.xml:27`, `addons/website_event/data/event_data.xml:33`, `addons/website_event/data/event_data.xml:39`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/website_event/security/ir.access.csv`, `addons/website_event/security/event_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 10 test files are present.
- **Evidence:** `addons/website_event/tests/test_fuzzy.py`, `addons/website_event/tests/test_event_ics.py`, `addons/website_event/tests/test_website_event_technical_page.py`, `addons/website_event/tests/test_event_mail.py`, `addons/website_event/tests/test_event_visitor.py`, `addons/website_event/tests/common.py`, `addons/website_event/tests/test_event_internals.py`, `addons/website_event/tests/test_event_menus.py`, `addons/website_event/tests/test_website_event.py`, `addons/website_event/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 35; representative identifiers: `event.group_event_manager`, `ir_filters_event_list_snippet`, `website_snippet_filter_event_list`, `ir_filters_event_list_snippet_unfinished`, `website_snippet_filter_event_list_unfinished`, `menu_events`, `action_open_website`, `base.open_menu`, `mt_event_published`, `mt_event_unpublished`, `mt_event_scheduled`, `mt_event_unscheduled`, `event_registration_0_0_registration_answer_0`, `event_registration_0_0_registration_answer_1`, `event_registration_0_0_registration_answer_2`, `event_registration_0_1_registration_answer_0`, `event_registration_0_1_registration_answer_1`, `event_registration_0_2_registration_answer_0`, `event_registration_0_2_registration_answer_1`, `event_registration_7_0_registration_answer_0`
- Menus: 2; representative evidence: `addons/website_event/views/website_pages_views.xml:94`, `addons/website_event/views/event_menus.xml:4`
- Templates: 74; representative evidence: `addons/website_event/views/event_templates_page_misc.xml:5`, `addons/website_event/views/event_templates_svg.xml:3`, `addons/website_event/views/event_templates_widgets.xml:5`, `addons/website_event/views/event_templates_widgets.xml:30`, `addons/website_event/views/portal_templates.xml:3`, `addons/website_event/views/event_templates_page.xml:5`, `addons/website_event/views/event_templates_page.xml:23`, `addons/website_event/views/event_templates_page.xml:90`, `addons/website_event/views/event_templates_page_registration.xml:5`, `addons/website_event/views/event_templates_page_registration.xml:14`, `addons/website_event/views/event_templates_page_registration.xml:149`, `addons/website_event/views/event_templates_page_registration.xml:190`
- View/action field declarations: 58; representative evidence: `addons/website_event/data/event_data.xml:23`, `addons/website_event/data/event_data.xml:29`, `addons/website_event/data/event_data.xml:35`, `addons/website_event/data/event_data.xml:41`, `addons/website_event/views/website_pages_views.xml:6`, `addons/website_event/views/website_pages_views.xml:10`, `addons/website_event/views/website_pages_views.xml:42`, `addons/website_event/views/website_pages_views.xml:46`, `addons/website_event/views/website_pages_views.xml:84`, `addons/website_event/views/website_pages_views.xml:86`, `addons/website_event/views/event_event_add.xml:6`, `addons/website_event/views/event_event_add.xml:9`
- Browser assets: 23; representative files: `addons/website_event/static/src/website_builder/dynamic_snippet_events_option_plugin.js`, `addons/website_event/static/src/website_builder/event_searchbar_option_plugin.js`, `addons/website_event/static/src/website_builder/event_page_option_plugin.js`, `addons/website_event/static/src/website_builder/dynamic_snippet_events_option.js`, `addons/website_event/static/src/website_builder/dynamic_snippet_events_carousel_option.js`, `addons/website_event/static/src/website_builder/dark_palette_content.js`, `addons/website_event/static/src/interactions/website_event_ticket_details.js`, `addons/website_event/static/src/interactions/display_timer.js`, `addons/website_event/static/src/interactions/register_toaster.js`, `addons/website_event/static/src/interactions/modal_registration.js`, `addons/website_event/static/src/interactions/event_page.js`, `addons/website_event/static/src/interactions/website_event_slot_details.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_event/__manifest__.py`
- **HTTP entry points:** `addons/website_event/controllers/community.py:10`, `addons/website_event/controllers/main.py:39`, `addons/website_event/controllers/main.py:196`, `addons/website_event/controllers/main.py:244`, `addons/website_event/controllers/main.py:254`, `addons/website_event/controllers/main.py:309`, `addons/website_event/controllers/main.py:372`, `addons/website_event/controllers/main.py:490`, `addons/website_event/controllers/main.py:517`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 12
- Representative model evidence: inherits `website.track` (addons/website_event/models/website_track.py:6); inherits `website.menu` (addons/website_event/models/website_menu.py:9); inherits `website.snippet.filter` (addons/website_event/models/website_snippet_filter.py:9); inherits `event.slot` (addons/website_event/models/event_slot.py:6); inherits `event.type` (addons/website_event/models/event_type.py:6); `event.tag.category` (addons/website_event/models/event_tag_category.py:7); inherits `website.visitor` (addons/website_event/models/website_visitor.py:8); `event.tag` (addons/website_event/models/event_tag.py:6); `website.event.menu` (addons/website_event/models/website_event_menu.py:9); `event.event` (addons/website_event/models/event_event.py:21); inherits `event.registration` (addons/website_event/models/event_registration.py:6); inherits `website` (addons/website_event/models/website.py:10)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 9
- Route evidence: `addons/website_event/controllers/community.py:10`, `addons/website_event/controllers/main.py:39`, `addons/website_event/controllers/main.py:196`, `addons/website_event/controllers/main.py:244`, `addons/website_event/controllers/main.py:254`, `addons/website_event/controllers/main.py:309`, `addons/website_event/controllers/main.py:372`, `addons/website_event/controllers/main.py:490`, `addons/website_event/controllers/main.py:517`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `event`, `website`, `website_partner`, `website_mail`, `html_builder`
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

- `addons/website_event/README.md`
- `addons/website_event/__init__.py`
- `addons/website_event/__manifest__.py`
- `addons/website_event/controllers/__init__.py`
- `addons/website_event/controllers/community.py`
- `addons/website_event/controllers/main.py`
- `addons/website_event/data/event_data.xml`
- `addons/website_event/data/event_demo.xml`
- `addons/website_event/data/event_question_demo.xml`
- `addons/website_event/data/event_registration_answer_demo.xml`
- `addons/website_event/data/event_registration_demo.xml`
- `addons/website_event/data/res_partner_demo.xml`
- `addons/website_event/data/website_snippet_data.xml`
- `addons/website_event/i18n/af.po`
- `addons/website_event/i18n/ar.po`
- `addons/website_event/i18n/az.po`
- `addons/website_event/i18n/bg.po`
- `addons/website_event/i18n/bs.po`
- `addons/website_event/i18n/ca.po`
- `addons/website_event/i18n/cs.po`
- `addons/website_event/i18n/da.po`
- `addons/website_event/i18n/de.po`
- `addons/website_event/i18n/el.po`
- `addons/website_event/i18n/es.po`
- `addons/website_event/i18n/es_419.po`
- `addons/website_event/i18n/et.po`
- `addons/website_event/i18n/fa.po`
- `addons/website_event/i18n/fi.po`
- `addons/website_event/i18n/fr.po`
- `addons/website_event/i18n/gl.po`
- `addons/website_event/i18n/gu.po`
- `addons/website_event/i18n/he.po`
- `addons/website_event/i18n/hi.po`
- `addons/website_event/i18n/hr.po`
- `addons/website_event/i18n/hu.po`
- `addons/website_event/i18n/id.po`
- `addons/website_event/i18n/is.po`
- `addons/website_event/i18n/it.po`
- `addons/website_event/i18n/ja.po`
- `addons/website_event/i18n/ka.po`
- `addons/website_event/i18n/kab.po`
- `addons/website_event/i18n/km.po`
- `addons/website_event/i18n/ko.po`
- `addons/website_event/i18n/ku.po`
- `addons/website_event/i18n/lo.po`
- `addons/website_event/i18n/lt.po`
- `addons/website_event/i18n/lv.po`
- `addons/website_event/i18n/mk.po`
- `addons/website_event/i18n/mn.po`
- `addons/website_event/i18n/my.po`
- `addons/website_event/i18n/nb.po`
- `addons/website_event/i18n/nl.po`
- `addons/website_event/i18n/pl.po`
- `addons/website_event/i18n/pt.po`
- `addons/website_event/i18n/pt_BR.po`
- `addons/website_event/i18n/ro.po`
- `addons/website_event/i18n/ru.po`
- `addons/website_event/i18n/sk.po`
- `addons/website_event/i18n/sl.po`
- `addons/website_event/i18n/sr@latin.po`
- `addons/website_event/i18n/sv.po`
- `addons/website_event/i18n/th.po`
- `addons/website_event/i18n/tr.po`
- `addons/website_event/i18n/uk.po`
- `addons/website_event/i18n/uz.po`
- `addons/website_event/i18n/vi.po`
- `addons/website_event/i18n/website_event.pot`
- `addons/website_event/i18n/zh_CN.po`
- `addons/website_event/i18n/zh_TW.po`
- `addons/website_event/models/__init__.py`
- `addons/website_event/models/event_event.py`
- `addons/website_event/models/event_registration.py`
- `addons/website_event/models/event_slot.py`
- `addons/website_event/models/event_tag.py`
- `addons/website_event/models/event_tag_category.py`
- `addons/website_event/models/event_type.py`
- `addons/website_event/models/website.py`
- `addons/website_event/models/website_event_menu.py`
- `addons/website_event/models/website_menu.py`
- `addons/website_event/models/website_snippet_filter.py`
- `addons/website_event/models/website_track.py`
- `addons/website_event/models/website_visitor.py`
- `addons/website_event/security/event_security.xml`
- `addons/website_event/security/ir.access.csv`
- `addons/website_event/static/description/icon.png`
- `addons/website_event/static/description/icon.svg`
- `addons/website_event/static/description/icon_hi.png`
- `addons/website_event/static/src/img/event_cover_0.jpg`
- `addons/website_event/static/src/img/event_cover_1.jpg`
- `addons/website_event/static/src/img/event_cover_2.jpg`
- `addons/website_event/static/src/img/event_cover_3.jpg`
- `addons/website_event/static/src/img/event_cover_4.jpg`
- `addons/website_event/static/src/img/event_cover_5.jpg`
- `addons/website_event/static/src/img/event_cover_7.jpg`
- `addons/website_event/static/src/img/event_past_0.jpg`
- `addons/website_event/static/src/img/event_previews/event_1.jpg`
- `addons/website_event/static/src/img/event_previews/event_2.jpg`
- `addons/website_event/static/src/img/event_previews/event_3.jpg`
- `addons/website_event/static/src/img/event_training_0.jpg`
- `addons/website_event/static/src/img/openerp_enterprise_of_the_year.png`
- `addons/website_event/static/src/img/speaker.png`
- `addons/website_event/static/src/img/training.jpg`
- `addons/website_event/static/src/interactions/display_timer.js`
- `addons/website_event/static/src/interactions/event_page.js`
- `addons/website_event/static/src/interactions/modal_registration.js`
- `addons/website_event/static/src/interactions/register_toaster.js`
- `addons/website_event/static/src/interactions/website_event_slot_details.js`
- `addons/website_event/static/src/interactions/website_event_ticket_details.js`
- `addons/website_event/static/src/js/systray_items/new_content.js`
- `addons/website_event/static/src/js/tours/event_tour.js`
- `addons/website_event/static/src/scss/event_templates_common.scss`
- `addons/website_event/static/src/scss/event_templates_list.scss`
- `addons/website_event/static/src/scss/event_templates_page.scss`
- `addons/website_event/static/src/snippets/s_events/000.scss`
- `addons/website_event/static/src/snippets/s_events/events.js`
- `addons/website_event/static/src/snippets/s_events/events_carousel.js`
- `addons/website_event/static/src/snippets/s_events/events_mixin.js`
- `addons/website_event/static/src/website_builder/dark_palette_content.js`
- `addons/website_event/static/src/website_builder/dynamic_snippet_events_carousel_option.js`
- `addons/website_event/static/src/website_builder/dynamic_snippet_events_carousel_option.xml`
- `addons/website_event/static/src/website_builder/dynamic_snippet_events_option.js`
- `addons/website_event/static/src/website_builder/dynamic_snippet_events_option.xml`
- `addons/website_event/static/src/website_builder/dynamic_snippet_events_option_plugin.js`
- `addons/website_event/static/src/website_builder/dynamic_snippet_events_shared_option.xml`
- `addons/website_event/static/src/website_builder/event_page_option.xml`
- `addons/website_event/static/src/website_builder/event_page_option_plugin.js`
- `addons/website_event/static/src/website_builder/event_searchbar_option_plugin.js`
- `addons/website_event/static/src/website_builder/events_list_page_option.xml`
- `addons/website_event/static/tests/interactions/snippets/events.test.js`
- `addons/website_event/static/tests/tours/sub_templates_config.js`
- `addons/website_event/static/tests/tours/tickets_questions.js`
- `addons/website_event/static/tests/tours/website_event.js`
- `addons/website_event/static/tests/tours/website_event_pages_seo.js`
- `addons/website_event/static/tests/tours/website_event_search.js`
- `addons/website_event/tests/__init__.py`
- `addons/website_event/tests/common.py`
- `addons/website_event/tests/test_event_ics.py`
- `addons/website_event/tests/test_event_internals.py`
- `addons/website_event/tests/test_event_mail.py`
- `addons/website_event/tests/test_event_menus.py`
- `addons/website_event/tests/test_event_visitor.py`
- `addons/website_event/tests/test_fuzzy.py`
- `addons/website_event/tests/test_website_event.py`
- `addons/website_event/tests/test_website_event_technical_page.py`
- `addons/website_event/views/event_event_add.xml`
- `addons/website_event/views/event_event_views.xml`
- `addons/website_event/views/event_menus.xml`
- `addons/website_event/views/event_registration_views.xml`
- `addons/website_event/views/event_tag_category_views.xml`
- `addons/website_event/views/event_tag_views.xml`
- `addons/website_event/views/event_templates_list.xml`
- `addons/website_event/views/event_templates_page.xml`
- `addons/website_event/views/event_templates_page_misc.xml`
- `addons/website_event/views/event_templates_page_registration.xml`
- `addons/website_event/views/event_templates_svg.xml`
- `addons/website_event/views/event_templates_widgets.xml`
- `addons/website_event/views/event_type_views.xml`
- `addons/website_event/views/portal_templates.xml`
- `addons/website_event/views/snippets/s_event_carousel_preview_data.xml`
- `addons/website_event/views/snippets/s_event_upcoming_snippet_preview_data.xml`
- `addons/website_event/views/snippets/s_events.xml`
- `addons/website_event/views/snippets/s_events_carousel.xml`
- `addons/website_event/views/snippets/snippets.xml`
- `addons/website_event/views/website_event_menu_views.xml`
- `addons/website_event/views/website_pages_views.xml`
- `addons/website_event/views/website_visitor_views.xml`
