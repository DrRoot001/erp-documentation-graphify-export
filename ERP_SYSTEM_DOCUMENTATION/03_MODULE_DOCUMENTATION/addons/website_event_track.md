# Module: website_event_track

- **Module ID:** MOD-614
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_event_track`
- **Manifest:** `addons/website_event_track/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Sponsors, Tracks, Agenda, Event News

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 150 files, including 29 Python, 33 XML, and 11 JavaScript/TypeScript files. The manifest declares dependencies: `website_event`.

## 2. Module structure

- Model/business logic files: 13
- Controller/API files: 5
- XML/data/view/template files: 33
- Browser asset files: 11
- Security files: 1
- Test files: 8
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_event_track/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 13 model declarations, 123 methods, 1 constraint handlers, 0 onchange handlers, and 31 dependency declarations.
- **Evidence:** `addons/website_event_track/models/event_track_stage.py:7`, `addons/website_event_track/models/event_track_location.py:4`, `addons/website_event_track/models/website_menu.py:7`, `addons/website_event_track/models/res_config_settings.py:7`, `addons/website_event_track/models/event_track_visitor.py:7`, `addons/website_event_track/models/event_type.py:7`, `addons/website_event_track/models/event_track_tag_category.py:7`, `addons/website_event_track/models/website_visitor.py:8`, `addons/website_event_track/models/website_event_menu.py:7`, `addons/website_event_track/models/event_track_tag.py:9`, `addons/website_event_track/models/event_event.py:7`, `addons/website_event_track/models/website.py:10`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 5 controller files and 14 route declarations.
- **Evidence:** `addons/website_event_track/controllers/location_display.py:110`, `addons/website_event_track/controllers/location_display.py:118`, `addons/website_event_track/controllers/webmanifest.py:14`, `addons/website_event_track/controllers/webmanifest.py:42`, `addons/website_event_track/controllers/webmanifest.py:59`, `addons/website_event_track/controllers/event_track.py:55`, `addons/website_event_track/controllers/event_track.py:188`, `addons/website_event_track/controllers/event_track.py:360`, `addons/website_event_track/controllers/event_track.py:398`, `addons/website_event_track/controllers/event_track.py:427`, `addons/website_event_track/controllers/event_track.py:460`, `addons/website_event_track/controllers/event_track.py:468`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 33 XML files and 11 JavaScript/TypeScript files; static XML analysis found 183 record/template/menu identifiers.
- **Evidence:** `addons/website_event_track/data/event_track_visitor_demo.xml:4`, `addons/website_event_track/data/event_track_visitor_demo.xml:9`, `addons/website_event_track/data/mail_template_data.xml:3`, `addons/website_event_track/data/mail_template_data.xml:33`, `addons/website_event_track/data/event_track_location_demo.xml:4`, `addons/website_event_track/data/event_track_location_demo.xml:7`, `addons/website_event_track/data/event_track_location_demo.xml:10`, `addons/website_event_track/data/event_track_location_demo.xml:13`, `addons/website_event_track/data/event_track_location_demo.xml:16`, `addons/website_event_track/data/event_track_location_demo.xml:19`, `addons/website_event_track/data/event_track_location_demo.xml:23`, `addons/website_event_track/data/event_track_location_demo.xml:26`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_event_track/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 8 test files are present.
- **Evidence:** `addons/website_event_track/tests/test_mail_features.py`, `addons/website_event_track/tests/test_website_visitor.py`, `addons/website_event_track/tests/test_location_display.py`, `addons/website_event_track/tests/test_event_menus.py`, `addons/website_event_track/tests/test_website_event.py`, `addons/website_event_track/tests/test_track_internals.py`, `addons/website_event_track/tests/__init__.py`, `addons/website_event_track/tests/test_website_event_track.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 33; representative identifiers: `event_7_track_2_visitor_0`, `event_7_track_2_visitor_2`, `mail_template_data_track_confirmation`, `mail_template_data_track_reminder`, `event_track_location5`, `event_track_location6`, `event_track_location7`, `event_track_location8`, `event_track_location9`, `event_track_location10`, `event_track_location_online_1`, `event_track_location_online_2`, `event_track_location_online_3`, `event_track1`, `event_track2`, `event_track3`, `event_track4`, `event_track5`, `event_track6`, `event_track7`
- Menus: 6; representative evidence: `addons/website_event_track/views/event_menus.xml:5`, `addons/website_event_track/views/event_menus.xml:13`, `addons/website_event_track/views/event_menus.xml:20`, `addons/website_event_track/views/event_menus.xml:26`, `addons/website_event_track/views/event_menus.xml:33`, `addons/website_event_track/views/event_menus.xml:41`
- Templates: 40; representative evidence: `addons/website_event_track/data/mail_templates.xml:5`, `addons/website_event_track/views/event_track_templates_agenda.xml:5`, `addons/website_event_track/views/event_track_templates_agenda.xml:49`, `addons/website_event_track/views/event_track_templates_agenda.xml:65`, `addons/website_event_track/views/event_track_templates_agenda.xml:78`, `addons/website_event_track/views/event_track_templates_agenda.xml:176`, `addons/website_event_track/views/event_track_templates_list.xml:4`, `addons/website_event_track/views/event_track_templates_list.xml:29`, `addons/website_event_track/views/event_track_templates_list.xml:123`, `addons/website_event_track/views/event_track_templates_list.xml:151`, `addons/website_event_track/views/event_track_templates_list.xml:164`, `addons/website_event_track/views/event_track_templates_list.xml:184`
- View/action field declarations: 71; representative evidence: `addons/website_event_track/data/mail_message_subtype_data.xml:6`, `addons/website_event_track/data/mail_message_subtype_data.xml:13`, `addons/website_event_track/data/mail_message_subtype_data.xml:20`, `addons/website_event_track/views/website_visitor_views.xml:6`, `addons/website_event_track/views/website_visitor_views.xml:8`, `addons/website_event_track/views/website_visitor_views.xml:17`, `addons/website_event_track/views/website_visitor_views.xml:19`, `addons/website_event_track/views/event_track_stage_views.xml:7`, `addons/website_event_track/views/event_track_stage_views.xml:8`, `addons/website_event_track/views/event_track_stage_views.xml:17`, `addons/website_event_track/views/event_track_stage_views.xml:18`, `addons/website_event_track/views/event_track_stage_views.xml:62`
- Browser assets: 11; representative files: `addons/website_event_track/static/lib/idb-keyval/idb-keyval.js`, `addons/website_event_track/static/src/js/service_worker.js`, `addons/website_event_track/static/src/interactions/website_event_track_proposal_form_tags.js`, `addons/website_event_track/static/src/interactions/website_event_track_proposal_form.js`, `addons/website_event_track/static/src/interactions/track_wishlist_counter.js`, `addons/website_event_track/static/src/interactions/website_event_track.js`, `addons/website_event_track/static/src/interactions/event_track_location_display.js`, `addons/website_event_track/static/src/interactions/event_track_timer.js`, `addons/website_event_track/static/src/interactions/website_event_pwa.js`, `addons/website_event_track/static/src/interactions/event_track_reminder.js`, `addons/website_event_track/static/tests/tours/email_reminder_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_event_track/__manifest__.py`
- **HTTP entry points:** `addons/website_event_track/controllers/location_display.py:110`, `addons/website_event_track/controllers/location_display.py:118`, `addons/website_event_track/controllers/webmanifest.py:14`, `addons/website_event_track/controllers/webmanifest.py:42`, `addons/website_event_track/controllers/webmanifest.py:59`, `addons/website_event_track/controllers/event_track.py:55`, `addons/website_event_track/controllers/event_track.py:188`, `addons/website_event_track/controllers/event_track.py:360`, `addons/website_event_track/controllers/event_track.py:398`, `addons/website_event_track/controllers/event_track.py:427`, `addons/website_event_track/controllers/event_track.py:460`, `addons/website_event_track/controllers/event_track.py:468`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 13
- Representative model evidence: `event.track.stage` (addons/website_event_track/models/event_track_stage.py:7); `event.track.location` (addons/website_event_track/models/event_track_location.py:4); inherits `website.menu` (addons/website_event_track/models/website_menu.py:7); inherits `res.config.settings` (addons/website_event_track/models/res_config_settings.py:7); `event.track.visitor` (addons/website_event_track/models/event_track_visitor.py:7); inherits `event.type` (addons/website_event_track/models/event_type.py:7); `event.track.tag.category` (addons/website_event_track/models/event_track_tag_category.py:7); inherits `website.visitor` (addons/website_event_track/models/website_visitor.py:8); inherits `website.event.menu` (addons/website_event_track/models/website_event_menu.py:7); `event.track.tag` (addons/website_event_track/models/event_track_tag.py:9); inherits `event.event` (addons/website_event_track/models/event_event.py:7); inherits `website` (addons/website_event_track/models/website.py:10); `event.track` (addons/website_event_track/models/event_track.py:29)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 5
- Route declarations: 14
- Route evidence: `addons/website_event_track/controllers/location_display.py:110`, `addons/website_event_track/controllers/location_display.py:118`, `addons/website_event_track/controllers/webmanifest.py:14`, `addons/website_event_track/controllers/webmanifest.py:42`, `addons/website_event_track/controllers/webmanifest.py:59`, `addons/website_event_track/controllers/event_track.py:55`, `addons/website_event_track/controllers/event_track.py:188`, `addons/website_event_track/controllers/event_track.py:360`, `addons/website_event_track/controllers/event_track.py:398`, `addons/website_event_track/controllers/event_track.py:427`, `addons/website_event_track/controllers/event_track.py:460`, `addons/website_event_track/controllers/event_track.py:468`
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

- `addons/website_event_track/README.md`
- `addons/website_event_track/__init__.py`
- `addons/website_event_track/__manifest__.py`
- `addons/website_event_track/controllers/__init__.py`
- `addons/website_event_track/controllers/event.py`
- `addons/website_event_track/controllers/event_track.py`
- `addons/website_event_track/controllers/location_display.py`
- `addons/website_event_track/controllers/webmanifest.py`
- `addons/website_event_track/data/event_data.xml`
- `addons/website_event_track/data/event_demo.xml`
- `addons/website_event_track/data/event_track_data.xml`
- `addons/website_event_track/data/event_track_demo.xml`
- `addons/website_event_track/data/event_track_demo_description.xml`
- `addons/website_event_track/data/event_track_location_demo.xml`
- `addons/website_event_track/data/event_track_tag_demo.xml`
- `addons/website_event_track/data/event_track_visitor_demo.xml`
- `addons/website_event_track/data/mail_message_subtype_data.xml`
- `addons/website_event_track/data/mail_template_data.xml`
- `addons/website_event_track/data/mail_templates.xml`
- `addons/website_event_track/i18n/af.po`
- `addons/website_event_track/i18n/ar.po`
- `addons/website_event_track/i18n/az.po`
- `addons/website_event_track/i18n/bg.po`
- `addons/website_event_track/i18n/bs.po`
- `addons/website_event_track/i18n/ca.po`
- `addons/website_event_track/i18n/cs.po`
- `addons/website_event_track/i18n/da.po`
- `addons/website_event_track/i18n/de.po`
- `addons/website_event_track/i18n/el.po`
- `addons/website_event_track/i18n/es.po`
- `addons/website_event_track/i18n/es_419.po`
- `addons/website_event_track/i18n/es_CL.po`
- `addons/website_event_track/i18n/et.po`
- `addons/website_event_track/i18n/eu.po`
- `addons/website_event_track/i18n/fa.po`
- `addons/website_event_track/i18n/fi.po`
- `addons/website_event_track/i18n/fr.po`
- `addons/website_event_track/i18n/fr_BE.po`
- `addons/website_event_track/i18n/fr_CA.po`
- `addons/website_event_track/i18n/gl.po`
- `addons/website_event_track/i18n/gu.po`
- `addons/website_event_track/i18n/he.po`
- `addons/website_event_track/i18n/hi.po`
- `addons/website_event_track/i18n/hr.po`
- `addons/website_event_track/i18n/hu.po`
- `addons/website_event_track/i18n/id.po`
- `addons/website_event_track/i18n/is.po`
- `addons/website_event_track/i18n/it.po`
- `addons/website_event_track/i18n/ja.po`
- `addons/website_event_track/i18n/ka.po`
- `addons/website_event_track/i18n/kab.po`
- `addons/website_event_track/i18n/km.po`
- `addons/website_event_track/i18n/ko.po`
- `addons/website_event_track/i18n/ku.po`
- `addons/website_event_track/i18n/lo.po`
- `addons/website_event_track/i18n/lt.po`
- `addons/website_event_track/i18n/lv.po`
- `addons/website_event_track/i18n/mk.po`
- `addons/website_event_track/i18n/mn.po`
- `addons/website_event_track/i18n/my.po`
- `addons/website_event_track/i18n/nb.po`
- `addons/website_event_track/i18n/nl.po`
- `addons/website_event_track/i18n/pl.po`
- `addons/website_event_track/i18n/pt.po`
- `addons/website_event_track/i18n/pt_BR.po`
- `addons/website_event_track/i18n/ro.po`
- `addons/website_event_track/i18n/ru.po`
- `addons/website_event_track/i18n/sk.po`
- `addons/website_event_track/i18n/sl.po`
- `addons/website_event_track/i18n/sq.po`
- `addons/website_event_track/i18n/sr@latin.po`
- `addons/website_event_track/i18n/sv.po`
- `addons/website_event_track/i18n/th.po`
- `addons/website_event_track/i18n/tr.po`
- `addons/website_event_track/i18n/uk.po`
- `addons/website_event_track/i18n/uz.po`
- `addons/website_event_track/i18n/vi.po`
- `addons/website_event_track/i18n/website_event_track.pot`
- `addons/website_event_track/i18n/zh_CN.po`
- `addons/website_event_track/i18n/zh_TW.po`
- `addons/website_event_track/models/__init__.py`
- `addons/website_event_track/models/event_event.py`
- `addons/website_event_track/models/event_track.py`
- `addons/website_event_track/models/event_track_location.py`
- `addons/website_event_track/models/event_track_stage.py`
- `addons/website_event_track/models/event_track_tag.py`
- `addons/website_event_track/models/event_track_tag_category.py`
- `addons/website_event_track/models/event_track_visitor.py`
- `addons/website_event_track/models/event_type.py`
- `addons/website_event_track/models/res_config_settings.py`
- `addons/website_event_track/models/website.py`
- `addons/website_event_track/models/website_event_menu.py`
- `addons/website_event_track/models/website_menu.py`
- `addons/website_event_track/models/website_visitor.py`
- `addons/website_event_track/security/ir.access.csv`
- `addons/website_event_track/static/description/blog.png`
- `addons/website_event_track/static/description/event.png`
- `addons/website_event_track/static/description/icon.png`
- `addons/website_event_track/static/description/icon.svg`
- `addons/website_event_track/static/description/icon_hi.png`
- `addons/website_event_track/static/description/index.html`
- `addons/website_event_track/static/description/sponsor.png`
- `addons/website_event_track/static/description/tracks.png`
- `addons/website_event_track/static/lib/idb-keyval/idb-keyval.js`
- `addons/website_event_track/static/src/img/event_track_default_0.jpeg`
- `addons/website_event_track/static/src/img/event_track_default_1.jpeg`
- `addons/website_event_track/static/src/interactions/event_track_location_display.js`
- `addons/website_event_track/static/src/interactions/event_track_reminder.js`
- `addons/website_event_track/static/src/interactions/event_track_timer.js`
- `addons/website_event_track/static/src/interactions/track_wishlist_counter.js`
- `addons/website_event_track/static/src/interactions/website_event_pwa.js`
- `addons/website_event_track/static/src/interactions/website_event_track.js`
- `addons/website_event_track/static/src/interactions/website_event_track_proposal_form.js`
- `addons/website_event_track/static/src/interactions/website_event_track_proposal_form_tags.js`
- `addons/website_event_track/static/src/js/service_worker.js`
- `addons/website_event_track/static/src/scss/event_track_location_display.scss`
- `addons/website_event_track/static/src/scss/event_track_templates.scss`
- `addons/website_event_track/static/src/scss/event_track_templates_online.scss`
- `addons/website_event_track/static/src/scss/pwa_frontend.scss`
- `addons/website_event_track/static/src/website_builder/event_track_page_option.xml`
- `addons/website_event_track/static/src/xml/event_track_proposal_templates.xml`
- `addons/website_event_track/static/src/xml/website_event_pwa.xml`
- `addons/website_event_track/static/src/xml/website_event_track_email_reminder.xml`
- `addons/website_event_track/static/src/xml/website_event_track_form_tags_wrapper.xml`
- `addons/website_event_track/static/tests/tours/email_reminder_tour.js`
- `addons/website_event_track/tests/__init__.py`
- `addons/website_event_track/tests/test_event_menus.py`
- `addons/website_event_track/tests/test_location_display.py`
- `addons/website_event_track/tests/test_mail_features.py`
- `addons/website_event_track/tests/test_track_internals.py`
- `addons/website_event_track/tests/test_website_event.py`
- `addons/website_event_track/tests/test_website_event_track.py`
- `addons/website_event_track/tests/test_website_visitor.py`
- `addons/website_event_track/views/event_event_views.xml`
- `addons/website_event_track/views/event_menus.xml`
- `addons/website_event_track/views/event_templates.xml`
- `addons/website_event_track/views/event_track_location_views.xml`
- `addons/website_event_track/views/event_track_stage_views.xml`
- `addons/website_event_track/views/event_track_tag_views.xml`
- `addons/website_event_track/views/event_track_templates_agenda.xml`
- `addons/website_event_track/views/event_track_templates_list.xml`
- `addons/website_event_track/views/event_track_templates_location_display.xml`
- `addons/website_event_track/views/event_track_templates_page.xml`
- `addons/website_event_track/views/event_track_templates_proposal.xml`
- `addons/website_event_track/views/event_track_templates_reminder.xml`
- `addons/website_event_track/views/event_track_views.xml`
- `addons/website_event_track/views/event_track_visitor_views.xml`
- `addons/website_event_track/views/event_type_views.xml`
- `addons/website_event_track/views/res_config_settings_view.xml`
- `addons/website_event_track/views/website_visitor_views.xml`
