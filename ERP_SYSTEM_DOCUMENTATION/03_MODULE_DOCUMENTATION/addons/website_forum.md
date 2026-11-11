# Module: website_forum

- **Module ID:** MOD-618
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_forum`
- **Manifest:** `addons/website_forum/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Manage a forum with FAQ and Q&A

**Manifest description:**

Ask questions, get answers, no distractions

**Scope evidence:** The module contains 155 files, including 34 Python, 35 XML, and 21 JavaScript/TypeScript files. The manifest declares dependencies: `auth_signup`, `website_mail`, `website_profile`.

## 2. Module structure

- Model/business logic files: 13
- Controller/API files: 5
- XML/data/view/template files: 35
- Browser asset files: 21
- Security files: 1
- Test files: 13
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_forum/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 13 model declarations, 234 methods, 1 constraint handlers, 0 onchange handlers, and 23 dependency declarations.
- **Evidence:** `addons/website_forum/models/forum_post_comment.py:7`, `addons/website_forum/models/forum_post_reason.py:6`, `addons/website_forum/models/forum_post_vote.py:7`, `addons/website_forum/models/ir_http.py:5`, `addons/website_forum/models/gamification_challenge.py:6`, `addons/website_forum/models/forum_post.py:18`, `addons/website_forum/models/gamification_karma_tracking.py:6`, `addons/website_forum/models/mail_thread.py:7`, `addons/website_forum/models/res_users.py:6`, `addons/website_forum/models/website.py:6`, `addons/website_forum/models/forum_tag.py:8`, `addons/website_forum/models/forum_forum.py:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 5 controller files and 41 route declarations.
- **Evidence:** `addons/website_forum/controllers/website_forum.py:76`, `addons/website_forum/controllers/website_forum.py:113`, `addons/website_forum/controllers/website_forum.py:199`, `addons/website_forum/controllers/website_forum.py:205`, `addons/website_forum/controllers/website_forum.py:214`, `addons/website_forum/controllers/website_forum.py:227`, `addons/website_forum/controllers/website_forum.py:288`, `addons/website_forum/controllers/website_forum.py:322`, `addons/website_forum/controllers/website_forum.py:345`, `addons/website_forum/controllers/website_forum.py:354`, `addons/website_forum/controllers/website_forum.py:367`, `addons/website_forum/controllers/website_forum.py:379`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 35 XML files and 21 JavaScript/TypeScript files; static XML analysis found 228 record/template/menu identifiers.
- **Evidence:** `addons/website_forum/data/forum_forum_data.xml:4`, `addons/website_forum/data/forum_post_demo.xml:4`, `addons/website_forum/data/forum_post_demo.xml:12`, `addons/website_forum/data/forum_post_demo.xml:27`, `addons/website_forum/data/forum_post_demo.xml:40`, `addons/website_forum/data/forum_post_demo.xml:52`, `addons/website_forum/data/forum_post_demo.xml:58`, `addons/website_forum/data/gamification_badge_data_answer.xml:7`, `addons/website_forum/data/gamification_badge_data_answer.xml:13`, `addons/website_forum/data/gamification_badge_data_answer.xml:25`, `addons/website_forum/data/gamification_badge_data_answer.xml:36`, `addons/website_forum/data/gamification_badge_data_answer.xml:42`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_forum/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/website_forum/data/forum_post_demo.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 13 test files are present.
- **Evidence:** `addons/website_forum/tests/test_forum_tag.py`, `addons/website_forum/tests/test_forum_tours.py`, `addons/website_forum/tests/test_performance.py`, `addons/website_forum/tests/test_forum_internals.py`, `addons/website_forum/tests/test_website_forum_technical_page.py`, `addons/website_forum/tests/test_sitemap.py`, `addons/website_forum/tests/test_forum_post.py`, `addons/website_forum/tests/test_web_editor.py`, `addons/website_forum/tests/test_forum_notifications.py`, `addons/website_forum/tests/test_forum_controller.py`, `addons/website_forum/tests/common.py`, `addons/website_forum/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 35; representative identifiers: `forum_help`, `question_0`, `question_1`, `answer_0`, `answer_1`, `post_vote_0`, `post_vote_1`, `badge_a_1`, `definition_teacher`, `challenge_teacher`, `line_teacher`, `badge_a_2`, `definition_nice_answer`, `challenge_nice_answer`, `line_nice_answer`, `badge_a_3`, `definition_good_answer`, `challenge_good_answer`, `line_good_answer`, `badge_a_4`
- Menus: 7; representative evidence: `addons/website_forum/views/forum_menus.xml:4`, `addons/website_forum/views/forum_menus.xml:11`, `addons/website_forum/views/forum_menus.xml:17`, `addons/website_forum/views/forum_menus.xml:23`, `addons/website_forum/views/forum_menus.xml:29`, `addons/website_forum/views/forum_menus.xml:35`, `addons/website_forum/views/forum_menus.xml:43`
- Templates: 52; representative evidence: `addons/website_forum/data/mail_templates.xml:3`, `addons/website_forum/data/mail_templates.xml:8`, `addons/website_forum/data/mail_templates.xml:13`, `addons/website_forum/data/mail_templates.xml:18`, `addons/website_forum/views/forum_forum_templates_moderation.xml:5`, `addons/website_forum/views/forum_forum_templates_moderation.xml:15`, `addons/website_forum/views/forum_forum_templates_moderation.xml:55`, `addons/website_forum/views/forum_forum_templates_moderation.xml:61`, `addons/website_forum/views/base_contact_templates.xml:4`, `addons/website_forum/views/forum_forum_templates_forum_all.xml:6`, `addons/website_forum/views/forum_forum_templates_forum_all.xml:26`, `addons/website_forum/views/forum_forum_templates_forum_all.xml:68`
- View/action field declarations: 49; representative evidence: `addons/website_forum/data/mail_message_subtype_data.xml:7`, `addons/website_forum/data/mail_message_subtype_data.xml:15`, `addons/website_forum/data/mail_message_subtype_data.xml:22`, `addons/website_forum/data/mail_message_subtype_data.xml:29`, `addons/website_forum/data/mail_message_subtype_data.xml:35`, `addons/website_forum/data/mail_message_subtype_data.xml:41`, `addons/website_forum/data/mail_message_subtype_data.xml:48`, `addons/website_forum/data/mail_message_subtype_data.xml:56`, `addons/website_forum/data/forum_forum_template_faq.xml:7`, `addons/website_forum/views/forum_tag_views.xml:6`, `addons/website_forum/views/forum_tag_views.xml:7`, `addons/website_forum/views/forum_tag_views.xml:18`
- Browser assets: 21; representative files: `addons/website_forum/static/src/website_builder/forum_floating_snippets_plugin.js`, `addons/website_forum/static/src/website_builder/forum_searchbar_option_plugin.js`, `addons/website_forum/static/src/components/website_forum_tags_wrapper.js`, `addons/website_forum/static/src/interactions/loader_loading.js`, `addons/website_forum/static/src/interactions/website_forum_spam.js`, `addons/website_forum/static/src/interactions/website_forum_share.js`, `addons/website_forum/static/src/interactions/website_forum_activity.js`, `addons/website_forum/static/src/interactions/website_forum.js`, `addons/website_forum/static/src/plugins/font_type_plugin.js`, `addons/website_forum/static/src/plugins/plugin_sets.js`, `addons/website_forum/static/src/js/systray_items/forum_forum_add_form.js`, `addons/website_forum/static/src/js/systray_items/new_content.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_forum/__manifest__.py`
- **HTTP entry points:** `addons/website_forum/controllers/website_forum.py:76`, `addons/website_forum/controllers/website_forum.py:113`, `addons/website_forum/controllers/website_forum.py:199`, `addons/website_forum/controllers/website_forum.py:205`, `addons/website_forum/controllers/website_forum.py:214`, `addons/website_forum/controllers/website_forum.py:227`, `addons/website_forum/controllers/website_forum.py:288`, `addons/website_forum/controllers/website_forum.py:322`, `addons/website_forum/controllers/website_forum.py:345`, `addons/website_forum/controllers/website_forum.py:354`, `addons/website_forum/controllers/website_forum.py:367`, `addons/website_forum/controllers/website_forum.py:379`
- **Scheduled entry points:** `addons/website_forum/data/forum_post_demo.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 13
- Representative model evidence: `forum.post.comment` (addons/website_forum/models/forum_post_comment.py:7); `forum.post.reason` (addons/website_forum/models/forum_post_reason.py:6); `forum.post.vote` (addons/website_forum/models/forum_post_vote.py:7); inherits `ir.http` (addons/website_forum/models/ir_http.py:5); inherits `gamification.challenge` (addons/website_forum/models/gamification_challenge.py:6); `forum.post` (addons/website_forum/models/forum_post.py:18); inherits `gamification.karma.tracking` (addons/website_forum/models/gamification_karma_tracking.py:6); inherits `mail.thread` (addons/website_forum/models/mail_thread.py:7); inherits `res.users` (addons/website_forum/models/res_users.py:6); inherits `website` (addons/website_forum/models/website.py:6); `forum.tag` (addons/website_forum/models/forum_tag.py:8); `forum.forum` (addons/website_forum/models/forum_forum.py:15); inherits `ir.attachment` (addons/website_forum/models/ir_attachment.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 5
- Route declarations: 41
- Route evidence: `addons/website_forum/controllers/website_forum.py:76`, `addons/website_forum/controllers/website_forum.py:113`, `addons/website_forum/controllers/website_forum.py:199`, `addons/website_forum/controllers/website_forum.py:205`, `addons/website_forum/controllers/website_forum.py:214`, `addons/website_forum/controllers/website_forum.py:227`, `addons/website_forum/controllers/website_forum.py:288`, `addons/website_forum/controllers/website_forum.py:322`, `addons/website_forum/controllers/website_forum.py:345`, `addons/website_forum/controllers/website_forum.py:354`, `addons/website_forum/controllers/website_forum.py:367`, `addons/website_forum/controllers/website_forum.py:379`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `auth_signup`, `website_mail`, `website_profile`
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

- `addons/website_forum/__init__.py`
- `addons/website_forum/__manifest__.py`
- `addons/website_forum/controllers/__init__.py`
- `addons/website_forum/controllers/legacy.py`
- `addons/website_forum/controllers/website.py`
- `addons/website_forum/controllers/website_forum.py`
- `addons/website_forum/controllers/website_mail.py`
- `addons/website_forum/data/forum_forum_data.xml`
- `addons/website_forum/data/forum_forum_template_faq.xml`
- `addons/website_forum/data/forum_post_demo.xml`
- `addons/website_forum/data/forum_post_reason_data.xml`
- `addons/website_forum/data/forum_tag_demo.xml`
- `addons/website_forum/data/gamification_badge_data_answer.xml`
- `addons/website_forum/data/gamification_badge_data_moderation.xml`
- `addons/website_forum/data/gamification_badge_data_participation.xml`
- `addons/website_forum/data/gamification_badge_data_question.xml`
- `addons/website_forum/data/ir_actions_data.xml`
- `addons/website_forum/data/ir_config_parameter_data.xml`
- `addons/website_forum/data/mail_message_subtype_data.xml`
- `addons/website_forum/data/mail_templates.xml`
- `addons/website_forum/data/website_forum_tour.xml`
- `addons/website_forum/data/website_menu_data.xml`
- `addons/website_forum/i18n/af.po`
- `addons/website_forum/i18n/ar.po`
- `addons/website_forum/i18n/az.po`
- `addons/website_forum/i18n/bg.po`
- `addons/website_forum/i18n/bs.po`
- `addons/website_forum/i18n/ca.po`
- `addons/website_forum/i18n/cs.po`
- `addons/website_forum/i18n/da.po`
- `addons/website_forum/i18n/de.po`
- `addons/website_forum/i18n/el.po`
- `addons/website_forum/i18n/es.po`
- `addons/website_forum/i18n/es_419.po`
- `addons/website_forum/i18n/et.po`
- `addons/website_forum/i18n/fa.po`
- `addons/website_forum/i18n/fi.po`
- `addons/website_forum/i18n/fr.po`
- `addons/website_forum/i18n/gu.po`
- `addons/website_forum/i18n/he.po`
- `addons/website_forum/i18n/hi.po`
- `addons/website_forum/i18n/hr.po`
- `addons/website_forum/i18n/hu.po`
- `addons/website_forum/i18n/id.po`
- `addons/website_forum/i18n/is.po`
- `addons/website_forum/i18n/it.po`
- `addons/website_forum/i18n/ja.po`
- `addons/website_forum/i18n/ka.po`
- `addons/website_forum/i18n/kab.po`
- `addons/website_forum/i18n/km.po`
- `addons/website_forum/i18n/ko.po`
- `addons/website_forum/i18n/ku.po`
- `addons/website_forum/i18n/lo.po`
- `addons/website_forum/i18n/lt.po`
- `addons/website_forum/i18n/lv.po`
- `addons/website_forum/i18n/mk.po`
- `addons/website_forum/i18n/mn.po`
- `addons/website_forum/i18n/my.po`
- `addons/website_forum/i18n/nb.po`
- `addons/website_forum/i18n/nl.po`
- `addons/website_forum/i18n/pl.po`
- `addons/website_forum/i18n/pt.po`
- `addons/website_forum/i18n/pt_BR.po`
- `addons/website_forum/i18n/ro.po`
- `addons/website_forum/i18n/ru.po`
- `addons/website_forum/i18n/sk.po`
- `addons/website_forum/i18n/sl.po`
- `addons/website_forum/i18n/sr@latin.po`
- `addons/website_forum/i18n/sv.po`
- `addons/website_forum/i18n/th.po`
- `addons/website_forum/i18n/tr.po`
- `addons/website_forum/i18n/uk.po`
- `addons/website_forum/i18n/uz.po`
- `addons/website_forum/i18n/vi.po`
- `addons/website_forum/i18n/website_forum.pot`
- `addons/website_forum/i18n/zh_CN.po`
- `addons/website_forum/i18n/zh_TW.po`
- `addons/website_forum/models/__init__.py`
- `addons/website_forum/models/forum_forum.py`
- `addons/website_forum/models/forum_post.py`
- `addons/website_forum/models/forum_post_comment.py`
- `addons/website_forum/models/forum_post_reason.py`
- `addons/website_forum/models/forum_post_vote.py`
- `addons/website_forum/models/forum_tag.py`
- `addons/website_forum/models/gamification_challenge.py`
- `addons/website_forum/models/gamification_karma_tracking.py`
- `addons/website_forum/models/ir_attachment.py`
- `addons/website_forum/models/ir_http.py`
- `addons/website_forum/models/mail_thread.py`
- `addons/website_forum/models/res_users.py`
- `addons/website_forum/models/website.py`
- `addons/website_forum/security/ir.access.csv`
- `addons/website_forum/static/description/icon.png`
- `addons/website_forum/static/description/icon.svg`
- `addons/website_forum/static/description/icon_hi.png`
- `addons/website_forum/static/src/components/flag_mark_as_offensive/flag_mark_as_offensive.js`
- `addons/website_forum/static/src/components/flag_mark_as_offensive/flag_mark_as_offensive.xml`
- `addons/website_forum/static/src/components/website_forum_tags_wrapper.js`
- `addons/website_forum/static/src/components/website_forum_wysiwyg/resizer.scss`
- `addons/website_forum/static/src/components/website_forum_wysiwyg/resizer_hook.js`
- `addons/website_forum/static/src/components/website_forum_wysiwyg/website_forum_wysiwyg.js`
- `addons/website_forum/static/src/components/website_forum_wysiwyg/website_forum_wysiwyg.xml`
- `addons/website_forum/static/src/img/empty.svg`
- `addons/website_forum/static/src/img/help.jpg`
- `addons/website_forum/static/src/img/tasks.svg`
- `addons/website_forum/static/src/interactions/loader_loading.js`
- `addons/website_forum/static/src/interactions/website_forum.js`
- `addons/website_forum/static/src/interactions/website_forum_activity.js`
- `addons/website_forum/static/src/interactions/website_forum_share.js`
- `addons/website_forum/static/src/interactions/website_forum_spam.js`
- `addons/website_forum/static/src/js/systray_items/forum_forum_add_form.js`
- `addons/website_forum/static/src/js/systray_items/new_content.js`
- `addons/website_forum/static/src/js/tours/website_forum.js`
- `addons/website_forum/static/src/plugins/font_type_plugin.js`
- `addons/website_forum/static/src/plugins/plugin_sets.js`
- `addons/website_forum/static/src/scss/website_forum.scss`
- `addons/website_forum/static/src/scss/website_forum_wysiwyg.scss`
- `addons/website_forum/static/src/website_builder/forum_floating_snippets_plugin.js`
- `addons/website_forum/static/src/website_builder/forum_page_option.xml`
- `addons/website_forum/static/src/website_builder/forum_searchbar_option_plugin.js`
- `addons/website_forum/static/src/xml/public_templates.xml`
- `addons/website_forum/static/src/xml/website_forum_tags_wrapper.xml`
- `addons/website_forum/static/tests/interactions/website_forum_editor.test.js`
- `addons/website_forum/static/tests/interactions/website_forum_share.test.js`
- `addons/website_forum/static/tests/interactions/website_forum_spam.test.js`
- `addons/website_forum/static/tests/tours/forum_cover_dropzone.js`
- `addons/website_forum/static/tests/tours/website_forum_question.js`
- `addons/website_forum/tests/__init__.py`
- `addons/website_forum/tests/common.py`
- `addons/website_forum/tests/test_forum_controller.py`
- `addons/website_forum/tests/test_forum_internals.py`
- `addons/website_forum/tests/test_forum_karma_access.py`
- `addons/website_forum/tests/test_forum_notifications.py`
- `addons/website_forum/tests/test_forum_post.py`
- `addons/website_forum/tests/test_forum_tag.py`
- `addons/website_forum/tests/test_forum_tours.py`
- `addons/website_forum/tests/test_performance.py`
- `addons/website_forum/tests/test_sitemap.py`
- `addons/website_forum/tests/test_web_editor.py`
- `addons/website_forum/tests/test_website_forum_technical_page.py`
- `addons/website_forum/views/base_contact_templates.xml`
- `addons/website_forum/views/forum_forum_templates.xml`
- `addons/website_forum/views/forum_forum_templates_follow.xml`
- `addons/website_forum/views/forum_forum_templates_forum_all.xml`
- `addons/website_forum/views/forum_forum_templates_layout.xml`
- `addons/website_forum/views/forum_forum_templates_moderation.xml`
- `addons/website_forum/views/forum_forum_templates_post.xml`
- `addons/website_forum/views/forum_forum_templates_tools.xml`
- `addons/website_forum/views/forum_forum_views.xml`
- `addons/website_forum/views/forum_menus.xml`
- `addons/website_forum/views/forum_post_reason_views.xml`
- `addons/website_forum/views/forum_post_views.xml`
- `addons/website_forum/views/forum_tag_views.xml`
- `addons/website_forum/views/gamification_karma_tracking_views.xml`
- `addons/website_forum/views/website_profile_templates.xml`
