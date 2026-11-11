# Module: website_slides

- **Module ID:** MOD-643
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_slides`
- **Manifest:** `addons/website_slides/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Website/eLearning`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Manage and publish an eLearning platform

**Manifest description:**

Create Online Courses
=====================

Featuring

 * Integrated course and lesson management
 * Fullscreen navigation
 * Support Youtube videos, Google documents, PDF, images, articles
 * Test knowledge with quizzes
 * Filter and Tag
 * Statistics

**Scope evidence:** The module contains 300 files, including 47 Python, 65 XML, and 75 JavaScript/TypeScript files. The manifest declares dependencies: `portal_rating`, `website`, `website_mail`, `website_profile`, `digest`.

## 2. Module structure

- Model/business logic files: 25
- Controller/API files: 4
- XML/data/view/template files: 65
- Browser asset files: 75
- Security files: 2
- Test files: 16
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_slides/security/ir.access.csv`, `addons/website_slides/security/website_slides_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 25 model declarations, 398 methods, 2 constraint handlers, 3 onchange handlers, and 57 dependency declarations.
- **Evidence:** `addons/website_slides/models/res_partner.py:6`, `addons/website_slides/models/slide_question.py:8`, `addons/website_slides/models/slide_question.py:62`, `addons/website_slides/models/website_track.py:6`, `addons/website_slides/models/mail_message.py:7`, `addons/website_slides/models/mail_activity.py:7`, `addons/website_slides/models/slide_channel.py:21`, `addons/website_slides/models/digest.py:6`, `addons/website_slides/models/res_groups.py:7`, `addons/website_slides/models/slide_tag.py:4`, `addons/website_slides/models/res_config_settings.py:7`, `addons/website_slides/models/slide_embed.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 4 controller files and 39 route declarations.
- **Evidence:** `addons/website_slides/controllers/legacy.py:13`, `addons/website_slides/controllers/main.py:404`, `addons/website_slides/controllers/main.py:524`, `addons/website_slides/controllers/main.py:804`, `addons/website_slides/controllers/main.py:858`, `addons/website_slides/controllers/main.py:876`, `addons/website_slides/controllers/main.py:897`, `addons/website_slides/controllers/main.py:904`, `addons/website_slides/controllers/main.py:912`, `addons/website_slides/controllers/main.py:920`, `addons/website_slides/controllers/main.py:955`, `addons/website_slides/controllers/main.py:963`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 65 XML files and 75 JavaScript/TypeScript files; static XML analysis found 325 record/template/menu identifiers.
- **Evidence:** `addons/website_slides/security/website_slides_security.xml:2`, `addons/website_slides/security/website_slides_security.xml:8`, `addons/website_slides/security/website_slides_security.xml:15`, `addons/website_slides/wizard/slide_channel_invite_views.xml:4`, `addons/website_slides/data/slides_tour.xml:3`, `addons/website_slides/data/website_snippet_filter_data.xml:4`, `addons/website_slides/data/website_snippet_filter_data.xml:12`, `addons/website_slides/data/slide_slide_demo.xml:6`, `addons/website_slides/data/slide_slide_demo.xml:22`, `addons/website_slides/data/slide_slide_demo.xml:28`, `addons/website_slides/data/slide_slide_demo.xml:42`, `addons/website_slides/data/slide_slide_demo.xml:56`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/website_slides/security/ir.access.csv`, `addons/website_slides/security/website_slides_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/website_slides/models/slide_channel_partner.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 16 test files are present.
- **Evidence:** `addons/website_slides/tests/test_slide_resource.py`, `addons/website_slides/tests/test_slide_slide.py`, `addons/website_slides/tests/test_gamification_karma.py`, `addons/website_slides/tests/test_security.py`, `addons/website_slides/tests/test_load_chatter_bundle.py`, `addons/website_slides/tests/test_slide_channel.py`, `addons/website_slides/tests/test_ui_wslides.py`, `addons/website_slides/tests/test_statistics.py`, `addons/website_slides/tests/test_slide_question.py`, `addons/website_slides/tests/test_embed_detection.py`, `addons/website_slides/tests/common.py`, `addons/website_slides/tests/test_mail.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 65; representative identifiers: `res_groups_privilege_elearning`, `group_website_slides_officer`, `group_website_slides_manager`, `slide_channel_invite_view_form`, `slides_tour`, `dynamic_snippet_latest_courses_filter`, `dynamic_filter_latest_courses`, `slide_slide_demo_0_0`, `slide_slide_demo_0_0_resource_0`, `slide_slide_demo_0_1`, `slide_slide_demo_0_2`, `slide_slide_demo_0_3`, `slide_slide_demo_0_4`, `slide_slide_demo_0_4_question_0`, `slide_slide_demo_0_4_question_0_0`, `slide_slide_demo_0_4_question_0_1`, `slide_slide_demo_0_4_question_0_2`, `slide_slide_demo_0_4_question_1`, `slide_slide_demo_0_4_question_1_0`, `slide_slide_demo_0_4_question_1_1`
- Menus: 15; representative evidence: `addons/website_slides/views/website_pages_views.xml:72`, `addons/website_slides/views/website_slides_menu_views.xml:3`, `addons/website_slides/views/website_slides_menu_views.xml:11`, `addons/website_slides/views/website_slides_menu_views.xml:15`, `addons/website_slides/views/website_slides_menu_views.xml:20`, `addons/website_slides/views/website_slides_menu_views.xml:26`, `addons/website_slides/views/website_slides_menu_views.xml:31`, `addons/website_slides/views/website_slides_menu_views.xml:38`, `addons/website_slides/views/website_slides_menu_views.xml:43`, `addons/website_slides/views/website_slides_menu_views.xml:48`, `addons/website_slides/views/website_slides_menu_views.xml:53`, `addons/website_slides/views/website_slides_menu_views.xml:58`
- Templates: 49; representative evidence: `addons/website_slides/views/website_slides_templates_lesson.xml:5`, `addons/website_slides/views/website_slides_templates_lesson.xml:64`, `addons/website_slides/views/website_slides_templates_lesson.xml:98`, `addons/website_slides/views/website_slides_templates_lesson.xml:111`, `addons/website_slides/views/website_slides_templates_lesson.xml:129`, `addons/website_slides/views/website_slides_templates_lesson.xml:208`, `addons/website_slides/views/website_slides_templates_lesson.xml:454`, `addons/website_slides/views/website_slides_templates_lesson.xml:485`, `addons/website_slides/views/website_slides_templates_lesson.xml:531`, `addons/website_slides/views/website_slides_templates_lesson_fullscreen.xml:5`, `addons/website_slides/views/website_slides_templates_lesson_fullscreen.xml:98`, `addons/website_slides/views/website_slides_templates_course.xml:5`
- View/action field declarations: 169; representative evidence: `addons/website_slides/wizard/slide_channel_invite_views.xml:6`, `addons/website_slides/wizard/slide_channel_invite_views.xml:7`, `addons/website_slides/data/slide_user_demo.xml:51`, `addons/website_slides/data/slide_user_demo.xml:68`, `addons/website_slides/data/slide_user_demo.xml:148`, `addons/website_slides/data/slide_user_demo.xml:165`, `addons/website_slides/data/slide_user_demo.xml:182`, `addons/website_slides/data/mail_message_subtype_data.xml:6`, `addons/website_slides/views/website_pages_views.xml:6`, `addons/website_slides/views/website_pages_views.xml:10`, `addons/website_slides/views/website_pages_views.xml:31`, `addons/website_slides/views/website_pages_views.xml:35`
- Browser assets: 75; representative files: `addons/website_slides/static/src/slide_category_list_renderer.js`, `addons/website_slides/static/src/slide_category_one2many_field.js`, `addons/website_slides/static/tests/website_slides_test_helpers.js`, `addons/website_slides/static/tests/activity_patch.test.js`, `addons/website_slides/static/tests/slide_category_one2many_field.test.js`, `addons/website_slides/static/src/website_builder/slides_searchbar_option_plugin.js`, `addons/website_slides/static/src/js/utils.js`, `addons/website_slides/static/src/js/slides_course_service.js`, `addons/website_slides/static/src/js/slides_embed.js`, `addons/website_slides/static/src/interactions/slides_course_fullscreen.js`, `addons/website_slides/static/src/interactions/slide_toggle_preview.js`, `addons/website_slides/static/src/interactions/slide_like.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_slides/__manifest__.py`
- **HTTP entry points:** `addons/website_slides/controllers/legacy.py:13`, `addons/website_slides/controllers/main.py:404`, `addons/website_slides/controllers/main.py:524`, `addons/website_slides/controllers/main.py:804`, `addons/website_slides/controllers/main.py:858`, `addons/website_slides/controllers/main.py:876`, `addons/website_slides/controllers/main.py:897`, `addons/website_slides/controllers/main.py:904`, `addons/website_slides/controllers/main.py:912`, `addons/website_slides/controllers/main.py:920`, `addons/website_slides/controllers/main.py:955`, `addons/website_slides/controllers/main.py:963`
- **Scheduled entry points:** `addons/website_slides/models/slide_channel_partner.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 25
- Representative model evidence: inherits `res.partner` (addons/website_slides/models/res_partner.py:6); `slide.question` (addons/website_slides/models/slide_question.py:8); `slide.answer` (addons/website_slides/models/slide_question.py:62); inherits `website.track` (addons/website_slides/models/website_track.py:6); inherits `mail.message` (addons/website_slides/models/mail_message.py:7); inherits `mail.activity` (addons/website_slides/models/mail_activity.py:7); `slide.channel` (addons/website_slides/models/slide_channel.py:21); inherits `digest.digest` (addons/website_slides/models/digest.py:6); inherits `res.groups` (addons/website_slides/models/res_groups.py:7); `slide.tag` (addons/website_slides/models/slide_tag.py:4); inherits `res.config.settings` (addons/website_slides/models/res_config_settings.py:7); `slide.embed` (addons/website_slides/models/slide_embed.py:7); `slide.slide.partner` (addons/website_slides/models/slide_slide_partner.py:4); `slide.channel.tag.group` (addons/website_slides/models/slide_channel_tag.py:9); `slide.channel.tag` (addons/website_slides/models/slide_channel_tag.py:23); inherits `website.visitor` (addons/website_slides/models/website_visitor.py:6); inherits `gamification.challenge` (addons/website_slides/models/gamification_challenge.py:7); inherits `gamification.karma.tracking` (addons/website_slides/models/gamification_karma_tracking.py:7); inherits `base.partner.merge.automatic.wizard` (addons/website_slides/models/base_partner_merge.py:7); inherits `res.users` (addons/website_slides/models/res_users.py:7); `slide.channel.partner` (addons/website_slides/models/slide_channel_partner.py:5); inherits `website` (addons/website_slides/models/website.py:7); `slide.slide.resource` (addons/website_slides/models/slide_slide_resource.py:11); `slide.slide` (addons/website_slides/models/slide_slide.py:24); `slide.channel.invite` (addons/website_slides/wizard/slide_channel_invite.py:17)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 4
- Route declarations: 39
- Route evidence: `addons/website_slides/controllers/legacy.py:13`, `addons/website_slides/controllers/main.py:404`, `addons/website_slides/controllers/main.py:524`, `addons/website_slides/controllers/main.py:804`, `addons/website_slides/controllers/main.py:858`, `addons/website_slides/controllers/main.py:876`, `addons/website_slides/controllers/main.py:897`, `addons/website_slides/controllers/main.py:904`, `addons/website_slides/controllers/main.py:912`, `addons/website_slides/controllers/main.py:920`, `addons/website_slides/controllers/main.py:955`, `addons/website_slides/controllers/main.py:963`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `portal_rating`, `website`, `website_mail`, `website_profile`, `digest`
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

- `addons/website_slides/__init__.py`
- `addons/website_slides/__manifest__.py`
- `addons/website_slides/controllers/__init__.py`
- `addons/website_slides/controllers/legacy.py`
- `addons/website_slides/controllers/main.py`
- `addons/website_slides/controllers/portal.py`
- `addons/website_slides/data/digest_data.xml`
- `addons/website_slides/data/gamification_data.xml`
- `addons/website_slides/data/mail_message_subtype_data.xml`
- `addons/website_slides/data/mail_template_data.xml`
- `addons/website_slides/data/portal_entry_data.xml`
- `addons/website_slides/data/res_users_demo.xml`
- `addons/website_slides/data/slide_channel_demo.xml`
- `addons/website_slides/data/slide_channel_tag_demo.xml`
- `addons/website_slides/data/slide_data.xml`
- `addons/website_slides/data/slide_slide_demo.xml`
- `addons/website_slides/data/slide_user_demo.xml`
- `addons/website_slides/data/slide_user_gamification_demo.xml`
- `addons/website_slides/data/slides_tour.xml`
- `addons/website_slides/data/website_data.xml`
- `addons/website_slides/data/website_snippet_filter_data.xml`
- `addons/website_slides/i18n/af.po`
- `addons/website_slides/i18n/ar.po`
- `addons/website_slides/i18n/az.po`
- `addons/website_slides/i18n/bg.po`
- `addons/website_slides/i18n/bs.po`
- `addons/website_slides/i18n/ca.po`
- `addons/website_slides/i18n/cs.po`
- `addons/website_slides/i18n/da.po`
- `addons/website_slides/i18n/de.po`
- `addons/website_slides/i18n/el.po`
- `addons/website_slides/i18n/es.po`
- `addons/website_slides/i18n/es_419.po`
- `addons/website_slides/i18n/es_CL.po`
- `addons/website_slides/i18n/et.po`
- `addons/website_slides/i18n/eu.po`
- `addons/website_slides/i18n/fa.po`
- `addons/website_slides/i18n/fi.po`
- `addons/website_slides/i18n/fr.po`
- `addons/website_slides/i18n/gl.po`
- `addons/website_slides/i18n/gu.po`
- `addons/website_slides/i18n/he.po`
- `addons/website_slides/i18n/hi.po`
- `addons/website_slides/i18n/hr.po`
- `addons/website_slides/i18n/hu.po`
- `addons/website_slides/i18n/id.po`
- `addons/website_slides/i18n/is.po`
- `addons/website_slides/i18n/it.po`
- `addons/website_slides/i18n/ja.po`
- `addons/website_slides/i18n/ka.po`
- `addons/website_slides/i18n/kab.po`
- `addons/website_slides/i18n/km.po`
- `addons/website_slides/i18n/ko.po`
- `addons/website_slides/i18n/ku.po`
- `addons/website_slides/i18n/lb.po`
- `addons/website_slides/i18n/lo.po`
- `addons/website_slides/i18n/lt.po`
- `addons/website_slides/i18n/lv.po`
- `addons/website_slides/i18n/mk.po`
- `addons/website_slides/i18n/mn.po`
- `addons/website_slides/i18n/my.po`
- `addons/website_slides/i18n/nb.po`
- `addons/website_slides/i18n/nl.po`
- `addons/website_slides/i18n/pl.po`
- `addons/website_slides/i18n/pt.po`
- `addons/website_slides/i18n/pt_BR.po`
- `addons/website_slides/i18n/ro.po`
- `addons/website_slides/i18n/ru.po`
- `addons/website_slides/i18n/sk.po`
- `addons/website_slides/i18n/sl.po`
- `addons/website_slides/i18n/sq.po`
- `addons/website_slides/i18n/sr@latin.po`
- `addons/website_slides/i18n/sv.po`
- `addons/website_slides/i18n/th.po`
- `addons/website_slides/i18n/tr.po`
- `addons/website_slides/i18n/uk.po`
- `addons/website_slides/i18n/uz.po`
- `addons/website_slides/i18n/vi.po`
- `addons/website_slides/i18n/website_slides.pot`
- `addons/website_slides/i18n/zh_CN.po`
- `addons/website_slides/i18n/zh_TW.po`
- `addons/website_slides/models/__init__.py`
- `addons/website_slides/models/base_partner_merge.py`
- `addons/website_slides/models/digest.py`
- `addons/website_slides/models/gamification_challenge.py`
- `addons/website_slides/models/gamification_karma_tracking.py`
- `addons/website_slides/models/mail_activity.py`
- `addons/website_slides/models/mail_message.py`
- `addons/website_slides/models/res_config_settings.py`
- `addons/website_slides/models/res_groups.py`
- `addons/website_slides/models/res_partner.py`
- `addons/website_slides/models/res_users.py`
- `addons/website_slides/models/slide_channel.py`
- `addons/website_slides/models/slide_channel_partner.py`
- `addons/website_slides/models/slide_channel_tag.py`
- `addons/website_slides/models/slide_embed.py`
- `addons/website_slides/models/slide_question.py`
- `addons/website_slides/models/slide_slide.py`
- `addons/website_slides/models/slide_slide_partner.py`
- `addons/website_slides/models/slide_slide_resource.py`
- `addons/website_slides/models/slide_tag.py`
- `addons/website_slides/models/website.py`
- `addons/website_slides/models/website_track.py`
- `addons/website_slides/models/website_visitor.py`
- `addons/website_slides/security/ir.access.csv`
- `addons/website_slides/security/website_slides_security.xml`
- `addons/website_slides/static/description/icon.png`
- `addons/website_slides/static/description/icon.svg`
- `addons/website_slides/static/description/icon_hi.png`
- `addons/website_slides/static/src/chatter/portal/chatter_patch.js`
- `addons/website_slides/static/src/chatter/portal/message_model_patch.js`
- `addons/website_slides/static/src/core/common/@types/models.d.ts`
- `addons/website_slides/static/src/core/common/activity_model_patch.js`
- `addons/website_slides/static/src/core/common/thread_model_patch.js`
- `addons/website_slides/static/src/core/web/activity_patch.js`
- `addons/website_slides/static/src/core/web/activity_patch.xml`
- `addons/website_slides/static/src/img/banner_default.svg`
- `addons/website_slides/static/src/img/banner_default_all.svg`
- `addons/website_slides/static/src/img/banner_heroes_default.svg`
- `addons/website_slides/static/src/img/channel-documentation-default.jpg`
- `addons/website_slides/static/src/img/channel-documentation-layout.png`
- `addons/website_slides/static/src/img/channel-training-default.jpg`
- `addons/website_slides/static/src/img/channel-training-layout.png`
- `addons/website_slides/static/src/img/channel_demo_furniture.jpg`
- `addons/website_slides/static/src/img/channel_demo_furniture_2.jpg`
- `addons/website_slides/static/src/img/channel_demo_furniture_3.jpg`
- `addons/website_slides/static/src/img/channel_demo_gardening.jpg`
- `addons/website_slides/static/src/img/channel_demo_gardening_2.jpg`
- `addons/website_slides/static/src/img/channel_demo_gardening_3.jpg`
- `addons/website_slides/static/src/img/channel_demo_tree_1.jpg`
- `addons/website_slides/static/src/img/courses.svg`
- `addons/website_slides/static/src/img/document.png`
- `addons/website_slides/static/src/img/onboarding-quiz.png`
- `addons/website_slides/static/src/img/presentation.pdf`
- `addons/website_slides/static/src/img/quiz_modal_success.svg`
- `addons/website_slides/static/src/img/slide_demo_furniture.jpg`
- `addons/website_slides/static/src/img/slide_demo_furniture_2.jpg`
- `addons/website_slides/static/src/img/slide_demo_furniture_img.jpg`
- `addons/website_slides/static/src/img/slide_demo_furniture_img_1.jpg`
- `addons/website_slides/static/src/img/slide_demo_gardening.jpg`
- `addons/website_slides/static/src/img/slide_demo_gardening_1.jpg`
- `addons/website_slides/static/src/img/slide_demo_gardening_2.jpg`
- `addons/website_slides/static/src/img/slide_demo_owl.jpg`
- `addons/website_slides/static/src/img/slide_demo_thumb_5WMqwTnZ-qs.jpg`
- `addons/website_slides/static/src/img/slide_demo_thumb_PYr1rK8pS30.jpg`
- `addons/website_slides/static/src/img/slide_demo_thumb_QYmgrw0PgLU.jpg`
- `addons/website_slides/static/src/img/slide_demo_thumb_bvSe6r5BpaY.jpg`
- `addons/website_slides/static/src/img/slide_demo_thumb_ebBez6bcSEc.jpg`
- `addons/website_slides/static/src/img/slide_demo_thumb_grrXe1QZNzQ.jpg`
- `addons/website_slides/static/src/img/slide_demo_thumb_l0JZ25VvbwE.jpg`
- `addons/website_slides/static/src/img/slide_demo_tree_img_1.jpg`
- `addons/website_slides/static/src/img/slide_demo_tree_img_2.jpg`
- `addons/website_slides/static/src/img/slide_demo_tree_img_3.jpg`
- `addons/website_slides/static/src/img/slide_demo_tree_infographic_1.jpg`
- `addons/website_slides/static/src/img/slide_demo_tree_infographic_2.jpg`
- `addons/website_slides/static/src/img/slide_demo_tree_infographic_3.jpg`
- `addons/website_slides/static/src/img/slide_demo_wood_infographic_1.jpg`
- `addons/website_slides/static/src/img/standard_badge_bronze.svg`
- `addons/website_slides/static/src/img/standard_badge_gold.svg`
- `addons/website_slides/static/src/img/standard_badge_silver.svg`
- `addons/website_slides/static/src/interactions/animation.js`
- `addons/website_slides/static/src/interactions/category_add.js`
- `addons/website_slides/static/src/interactions/category_delete.js`
- `addons/website_slides/static/src/interactions/chatter_auto_expand.js`
- `addons/website_slides/static/src/interactions/course_prerequisite.js`
- `addons/website_slides/static/src/interactions/enroll_email.js`
- `addons/website_slides/static/src/interactions/portal_rating_composer.js`
- `addons/website_slides/static/src/interactions/share.js`
- `addons/website_slides/static/src/interactions/slide_archive.js`
- `addons/website_slides/static/src/interactions/slide_like.js`
- `addons/website_slides/static/src/interactions/slide_toggle_preview.js`
- `addons/website_slides/static/src/interactions/slide_upload.js`
- `addons/website_slides/static/src/interactions/slides.js`
- `addons/website_slides/static/src/interactions/slides_course_common.js`
- `addons/website_slides/static/src/interactions/slides_course_fullscreen.js`
- `addons/website_slides/static/src/interactions/slides_course_join.js`
- `addons/website_slides/static/src/interactions/slides_course_non_fullscreen.js`
- `addons/website_slides/static/src/interactions/slides_course_progressbar.js`
- `addons/website_slides/static/src/interactions/slides_course_quiz.js`
- `addons/website_slides/static/src/interactions/slides_course_quiz_edit.js`
- `addons/website_slides/static/src/interactions/slides_course_slides_sort.js`
- `addons/website_slides/static/src/interactions/tag_add.js`
- `addons/website_slides/static/src/interactions/unsubscribe.js`
- `addons/website_slides/static/src/js/components/edit_website_systray_item.js`
- `addons/website_slides/static/src/js/public/components/category_add_dialog/category_add_dialog.js`
- `addons/website_slides/static/src/js/public/components/category_add_dialog/category_add_dialog.xml`
- `addons/website_slides/static/src/js/public/components/course_join_popup/course_join_popup.js`
- `addons/website_slides/static/src/js/public/components/course_join_popup/course_join_popup.xml`
- `addons/website_slides/static/src/js/public/components/course_tag_add_dialog/course_tag_add_dialog.js`
- `addons/website_slides/static/src/js/public/components/course_tag_add_dialog/course_tag_add_dialog.xml`
- `addons/website_slides/static/src/js/public/components/slide_quiz_finish_dialog/slide_quiz_finish_dialog.js`
- `addons/website_slides/static/src/js/public/components/slide_quiz_finish_dialog/slide_quiz_finish_dialog.xml`
- `addons/website_slides/static/src/js/public/components/slide_quiz_finish_dialog/slide_xp_progress_bar.js`
- `addons/website_slides/static/src/js/public/components/slide_quiz_finish_dialog/slide_xp_progress_bar.scss`
- `addons/website_slides/static/src/js/public/components/slide_quiz_finish_dialog/slide_xp_progress_bar.xml`
- `addons/website_slides/static/src/js/public/components/slide_share_dialog/email_sharing_input.js`
- `addons/website_slides/static/src/js/public/components/slide_share_dialog/email_sharing_input.xml`
- `addons/website_slides/static/src/js/public/components/slide_share_dialog/slide_share_dialog.js`
- `addons/website_slides/static/src/js/public/components/slide_share_dialog/slide_share_dialog.xml`
- `addons/website_slides/static/src/js/public/components/slide_unsubscribe_dialog/slide_unsubscribe_dialog.js`
- `addons/website_slides/static/src/js/public/components/slide_unsubscribe_dialog/slide_unsubscribe_dialog.xml`
- `addons/website_slides/static/src/js/public/components/slide_upload_dialog/slide_install_module.js`
- `addons/website_slides/static/src/js/public/components/slide_upload_dialog/slide_install_module.xml`
- `addons/website_slides/static/src/js/public/components/slide_upload_dialog/slide_upload_category.js`
- `addons/website_slides/static/src/js/public/components/slide_upload_dialog/slide_upload_category.xml`
- `addons/website_slides/static/src/js/public/components/slide_upload_dialog/slide_upload_dialog.js`
- `addons/website_slides/static/src/js/public/components/slide_upload_dialog/slide_upload_dialog.xml`
- `addons/website_slides/static/src/js/public/components/slide_upload_dialog/slide_upload_dialog_select.js`
- `addons/website_slides/static/src/js/public/components/slide_upload_dialog/slide_upload_dialog_select.xml`
- `addons/website_slides/static/src/js/public/components/slide_upload_dialog/slide_upload_source_types.js`
- `addons/website_slides/static/src/js/public/components/slide_upload_dialog/slide_upload_source_types.xml`
- `addons/website_slides/static/src/js/public/components/slides_course_quiz_question_form/slides_course_quiz_question_form.js`
- `addons/website_slides/static/src/js/public/components/slides_course_quiz_question_form/slides_course_quiz_question_form.xml`
- `addons/website_slides/static/src/js/slides_course_service.js`
- `addons/website_slides/static/src/js/slides_embed.js`
- `addons/website_slides/static/src/js/systray_items/new_content.js`
- `addons/website_slides/static/src/js/tours/slides_tour.js`
- `addons/website_slides/static/src/js/utils.js`
- `addons/website_slides/static/src/scss/slide_views.scss`
- `addons/website_slides/static/src/scss/slides_slide_fullscreen.scss`
- `addons/website_slides/static/src/scss/website_slides.scss`
- `addons/website_slides/static/src/scss/website_slides_profile.scss`
- `addons/website_slides/static/src/slide_category_list_renderer.js`
- `addons/website_slides/static/src/slide_category_one2many_field.js`
- `addons/website_slides/static/src/views/slide_channel_partner_list/slide_channel_partner_list_controller.js`
- `addons/website_slides/static/src/views/slide_channel_partner_list/slide_channel_partner_list_view.js`
- `addons/website_slides/static/src/views/slide_channel_partner_list/slide_channel_partner_list_view.xml`
- `addons/website_slides/static/src/website_builder/courses_list_page_option.xml`
- `addons/website_slides/static/src/website_builder/slides_searchbar_option_plugin.js`
- `addons/website_slides/static/src/xml/slide_course_join.xml`
- `addons/website_slides/static/src/xml/slide_course_prerequisite.xml`
- `addons/website_slides/static/src/xml/slide_management.xml`
- `addons/website_slides/static/src/xml/slide_quiz.xml`
- `addons/website_slides/static/src/xml/website_slides_fullscreen.xml`
- `addons/website_slides/static/src/xml/website_slides_sidebar.xml`
- `addons/website_slides/static/tests/activity_patch.test.js`
- `addons/website_slides/static/tests/interactions/animation.test.js`
- `addons/website_slides/static/tests/mock_server/models/mail_activity.js`
- `addons/website_slides/static/tests/mock_server/models/slide_channel.js`
- `addons/website_slides/static/tests/slide_category_one2many_field.test.js`
- `addons/website_slides/static/tests/tours/slide_course_publisher_standard.js`
- `addons/website_slides/static/tests/tours/slide_portal_chatter_bundle.js`
- `addons/website_slides/static/tests/tours/slides_course_member.js`
- `addons/website_slides/static/tests/tours/slides_course_member_invited_logged.js`
- `addons/website_slides/static/tests/tours/slides_course_member_invited_public.js`
- `addons/website_slides/static/tests/tours/slides_course_member_yt.js`
- `addons/website_slides/static/tests/tours/slides_course_publisher.js`
- `addons/website_slides/static/tests/tours/slides_course_review_modification.js`
- `addons/website_slides/static/tests/tours/slides_course_reviews.js`
- `addons/website_slides/static/tests/tours/slides_course_reviews_comment.js`
- Additional source files not expanded in this page: 50; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
