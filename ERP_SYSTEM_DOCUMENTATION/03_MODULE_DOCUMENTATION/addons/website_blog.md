# Module: website_blog

- **Module ID:** MOD-598
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_blog`
- **Manifest:** `addons/website_blog/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Publish blog posts, announces, news

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 165 files, including 18 Python, 27 XML, and 33 JavaScript/TypeScript files. The manifest declares dependencies: `website_mail`, `website_partner`, `html_builder`.

## 2. Module structure

- Model/business logic files: 9
- Controller/API files: 2
- XML/data/view/template files: 27
- Browser asset files: 33
- Security files: 2
- Test files: 7
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_blog/security/ir.access.csv`, `addons/website_blog/security/website_blog_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 9 model declarations, 82 methods, 0 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/website_blog/models/res_partner.py:6`, `addons/website_blog/models/website_track.py:6`, `addons/website_blog/models/website_snippet_filter.py:9`, `addons/website_blog/models/website_visitor.py:6`, `addons/website_blog/models/website_blog.py:15`, `addons/website_blog/models/website_blog.py:132`, `addons/website_blog/models/website_blog.py:146`, `addons/website_blog/models/website_blog.py:163`, `addons/website_blog/models/website.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 4 route declarations.
- **Evidence:** `addons/website_blog/controllers/main.py:196`, `addons/website_blog/controllers/main.py:242`, `addons/website_blog/controllers/main.py:255`, `addons/website_blog/controllers/main.py:279`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 27 XML files and 33 JavaScript/TypeScript files; static XML analysis found 200 record/template/menu identifiers.
- **Evidence:** `addons/website_blog/security/website_blog_security.xml:3`, `addons/website_blog/security/website_blog_security.xml:8`, `addons/website_blog/data/blog_snippet_template_data.xml:5`, `addons/website_blog/data/blog_snippet_template_data.xml:13`, `addons/website_blog/data/blog_snippet_template_data.xml:22`, `addons/website_blog/data/blog_snippet_template_data.xml:28`, `addons/website_blog/data/website_blog_tour.xml:3`, `addons/website_blog/data/mail_message_subtype_data.xml:5`, `addons/website_blog/data/website_blog_data.xml:4`, `addons/website_blog/data/website_blog_data.xml:10`, `addons/website_blog/data/website_blog_data.xml:18`, `addons/website_blog/data/website_blog_data.xml:30`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/website_blog/security/ir.access.csv`, `addons/website_blog/security/website_blog_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 7 test files are present.
- **Evidence:** `addons/website_blog/tests/test_performance.py`, `addons/website_blog/tests/test_sitemap.py`, `addons/website_blog/tests/test_website_blog_flow.py`, `addons/website_blog/tests/common.py`, `addons/website_blog/tests/test_ui.py`, `addons/website_blog/tests/__init__.py`, `addons/website_blog/tests/test_website_blog_technical_page.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 27; representative identifiers: `res_groups_privilege_blog`, `group_website_blog_manager`, `dynamic_snippet_latest_blog_post_filter`, `dynamic_snippet_most_viewed_blog_post_filter`, `dynamic_filter_latest_blog_posts`, `dynamic_filter_most_viewed_blog_posts`, `blog`, `mt_blog_blog_published`, `blog_blog_1`, `menu_blog`, `mt_blog_blog_published`, `action_open_website`, `base.open_menu`, `blog_post_template_new_post`, `base.user_demo`, `base.default_user_group`, `blog_blog_1`, `blog_blog_2`, `blog_blog_3`, `blog_blog_4`
- Menus: 5; representative evidence: `addons/website_blog/views/website_pages_views.xml:156`, `addons/website_blog/views/website_blog_views.xml:123`, `addons/website_blog/views/website_blog_views.xml:129`, `addons/website_blog/views/website_blog_views.xml:131`, `addons/website_blog/views/website_blog_views.xml:133`
- Templates: 117; representative evidence: `addons/website_blog/data/mail_templates.xml:3`, `addons/website_blog/views/website_blog_posts_loop.xml:8`, `addons/website_blog/views/website_blog_posts_loop.xml:177`, `addons/website_blog/views/website_blog_posts_loop.xml:209`, `addons/website_blog/views/website_blog_posts_loop.xml:227`, `addons/website_blog/views/website_blog_posts_loop.xml:267`, `addons/website_blog/views/website_blog_posts_loop.xml:308`, `addons/website_blog/views/website_blog_posts_loop.xml:317`, `addons/website_blog/views/website_blog_posts_loop.xml:327`, `addons/website_blog/views/website_blog_posts_loop.xml:340`, `addons/website_blog/views/website_blog_posts_loop.xml:345`, `addons/website_blog/views/website_blog_posts_loop.xml:357`
- View/action field declarations: 55; representative evidence: `addons/website_blog/data/mail_message_subtype_data.xml:7`, `addons/website_blog/data/website_blog_data.xml:20`, `addons/website_blog/data/website_blog_demo.xml:495`, `addons/website_blog/data/website_blog_demo.xml:504`, `addons/website_blog/data/website_blog_demo.xml:513`, `addons/website_blog/data/website_blog_demo.xml:522`, `addons/website_blog/data/website_blog_demo.xml:531`, `addons/website_blog/data/website_blog_demo.xml:540`, `addons/website_blog/data/website_blog_demo.xml:549`, `addons/website_blog/views/website_pages_views.xml:6`, `addons/website_blog/views/website_pages_views.xml:7`, `addons/website_blog/views/website_pages_views.xml:59`
- Browser assets: 33; representative files: `addons/website_blog/static/src/website_builder/dynamic_snippet_blog_posts_option.js`, `addons/website_blog/static/src/website_builder/blog_searchbar_option_plugin.js`, `addons/website_blog/static/src/website_builder/dynamic_snippet_blog_posts_carousel_option.js`, `addons/website_blog/static/src/website_builder/author_avatar_sync_plugin.js`, `addons/website_blog/static/src/website_builder/blog_post_page_option_plugin.js`, `addons/website_blog/static/src/website_builder/blog_post_tags_option.js`, `addons/website_blog/static/src/website_builder/dynamic_snippet_blog_posts_option_plugin.js`, `addons/website_blog/static/src/website_builder/blog_page_option_plugin.js`, `addons/website_blog/static/src/@types/plugins.d.ts`, `addons/website_blog/static/src/interactions/blog_table_of_contents.edit.js`, `addons/website_blog/static/src/interactions/blog_table_of_contents.js`, `addons/website_blog/static/src/interactions/website_blog.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_blog/__manifest__.py`
- **HTTP entry points:** `addons/website_blog/controllers/main.py:196`, `addons/website_blog/controllers/main.py:242`, `addons/website_blog/controllers/main.py:255`, `addons/website_blog/controllers/main.py:279`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 9
- Representative model evidence: inherits `res.partner` (addons/website_blog/models/res_partner.py:6); inherits `website.track` (addons/website_blog/models/website_track.py:6); inherits `website.snippet.filter` (addons/website_blog/models/website_snippet_filter.py:9); inherits `website.visitor` (addons/website_blog/models/website_visitor.py:6); `blog.blog` (addons/website_blog/models/website_blog.py:15); `blog.tag.category` (addons/website_blog/models/website_blog.py:132); `blog.tag` (addons/website_blog/models/website_blog.py:146); `blog.post` (addons/website_blog/models/website_blog.py:163); inherits `website` (addons/website_blog/models/website.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 4
- Route evidence: `addons/website_blog/controllers/main.py:196`, `addons/website_blog/controllers/main.py:242`, `addons/website_blog/controllers/main.py:255`, `addons/website_blog/controllers/main.py:279`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_mail`, `website_partner`, `html_builder`
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

- `addons/website_blog/README.md`
- `addons/website_blog/__init__.py`
- `addons/website_blog/__manifest__.py`
- `addons/website_blog/controllers/__init__.py`
- `addons/website_blog/controllers/main.py`
- `addons/website_blog/data/blog_snippet_template_data.xml`
- `addons/website_blog/data/mail_message_subtype_data.xml`
- `addons/website_blog/data/mail_templates.xml`
- `addons/website_blog/data/website_blog_data.xml`
- `addons/website_blog/data/website_blog_demo.xml`
- `addons/website_blog/data/website_blog_tour.xml`
- `addons/website_blog/i18n/af.po`
- `addons/website_blog/i18n/ar.po`
- `addons/website_blog/i18n/az.po`
- `addons/website_blog/i18n/bg.po`
- `addons/website_blog/i18n/bs.po`
- `addons/website_blog/i18n/ca.po`
- `addons/website_blog/i18n/cs.po`
- `addons/website_blog/i18n/da.po`
- `addons/website_blog/i18n/de.po`
- `addons/website_blog/i18n/el.po`
- `addons/website_blog/i18n/es.po`
- `addons/website_blog/i18n/es_419.po`
- `addons/website_blog/i18n/es_CL.po`
- `addons/website_blog/i18n/et.po`
- `addons/website_blog/i18n/eu.po`
- `addons/website_blog/i18n/fa.po`
- `addons/website_blog/i18n/fi.po`
- `addons/website_blog/i18n/fr.po`
- `addons/website_blog/i18n/fr_BE.po`
- `addons/website_blog/i18n/fr_CA.po`
- `addons/website_blog/i18n/gl.po`
- `addons/website_blog/i18n/gu.po`
- `addons/website_blog/i18n/he.po`
- `addons/website_blog/i18n/hi.po`
- `addons/website_blog/i18n/hr.po`
- `addons/website_blog/i18n/hu.po`
- `addons/website_blog/i18n/id.po`
- `addons/website_blog/i18n/is.po`
- `addons/website_blog/i18n/it.po`
- `addons/website_blog/i18n/ja.po`
- `addons/website_blog/i18n/ka.po`
- `addons/website_blog/i18n/kab.po`
- `addons/website_blog/i18n/km.po`
- `addons/website_blog/i18n/ko.po`
- `addons/website_blog/i18n/ku.po`
- `addons/website_blog/i18n/lo.po`
- `addons/website_blog/i18n/lt.po`
- `addons/website_blog/i18n/lv.po`
- `addons/website_blog/i18n/mk.po`
- `addons/website_blog/i18n/mn.po`
- `addons/website_blog/i18n/my.po`
- `addons/website_blog/i18n/nb.po`
- `addons/website_blog/i18n/nl.po`
- `addons/website_blog/i18n/pl.po`
- `addons/website_blog/i18n/pt.po`
- `addons/website_blog/i18n/pt_BR.po`
- `addons/website_blog/i18n/ro.po`
- `addons/website_blog/i18n/ru.po`
- `addons/website_blog/i18n/sk.po`
- `addons/website_blog/i18n/sl.po`
- `addons/website_blog/i18n/sq.po`
- `addons/website_blog/i18n/sr@latin.po`
- `addons/website_blog/i18n/sv.po`
- `addons/website_blog/i18n/th.po`
- `addons/website_blog/i18n/tr.po`
- `addons/website_blog/i18n/uk.po`
- `addons/website_blog/i18n/uz.po`
- `addons/website_blog/i18n/vi.po`
- `addons/website_blog/i18n/website_blog.pot`
- `addons/website_blog/i18n/zh_CN.po`
- `addons/website_blog/i18n/zh_TW.po`
- `addons/website_blog/models/__init__.py`
- `addons/website_blog/models/res_partner.py`
- `addons/website_blog/models/website.py`
- `addons/website_blog/models/website_blog.py`
- `addons/website_blog/models/website_snippet_filter.py`
- `addons/website_blog/models/website_track.py`
- `addons/website_blog/models/website_visitor.py`
- `addons/website_blog/security/ir.access.csv`
- `addons/website_blog/security/website_blog_security.xml`
- `addons/website_blog/static/description/icon.png`
- `addons/website_blog/static/description/icon.svg`
- `addons/website_blog/static/description/icon_hi.png`
- `addons/website_blog/static/src/@types/plugins.d.ts`
- `addons/website_blog/static/src/img/anonymous.png`
- `addons/website_blog/static/src/img/blog_1.webp`
- `addons/website_blog/static/src/img/blog_2.webp`
- `addons/website_blog/static/src/img/blog_3.webp`
- `addons/website_blog/static/src/img/blog_4.webp`
- `addons/website_blog/static/src/img/content_1_1.webp`
- `addons/website_blog/static/src/img/content_2_1.webp`
- `addons/website_blog/static/src/img/content_3_1.webp`
- `addons/website_blog/static/src/img/content_4_1.webp`
- `addons/website_blog/static/src/img/content_5_1.webp`
- `addons/website_blog/static/src/img/content_6_1.webp`
- `addons/website_blog/static/src/img/content_7_1.webp`
- `addons/website_blog/static/src/img/cover_1.webp`
- `addons/website_blog/static/src/img/cover_2.webp`
- `addons/website_blog/static/src/img/cover_3.webp`
- `addons/website_blog/static/src/img/cover_4.webp`
- `addons/website_blog/static/src/img/cover_5.webp`
- `addons/website_blog/static/src/img/cover_6.webp`
- `addons/website_blog/static/src/img/cover_7.webp`
- `addons/website_blog/static/src/interactions/blog_table_of_contents.edit.js`
- `addons/website_blog/static/src/interactions/blog_table_of_contents.js`
- `addons/website_blog/static/src/interactions/components/blog_nav_sheet.js`
- `addons/website_blog/static/src/interactions/components/blog_nav_sheet.xml`
- `addons/website_blog/static/src/interactions/website_blog.edit.js`
- `addons/website_blog/static/src/interactions/website_blog.js`
- `addons/website_blog/static/src/js/systray_items/new_content.js`
- `addons/website_blog/static/src/scss/website_blog.scss`
- `addons/website_blog/static/src/snippets/s_blog_posts/000.scss`
- `addons/website_blog/static/src/snippets/s_blog_posts/blog_posts.js`
- `addons/website_blog/static/src/snippets/s_blog_posts/blog_posts_carousel.js`
- `addons/website_blog/static/src/snippets/s_blog_posts/blog_posts_mixin.js`
- `addons/website_blog/static/src/tours/website_blog.js`
- `addons/website_blog/static/src/website_builder/author_avatar_sync_plugin.js`
- `addons/website_blog/static/src/website_builder/blog_content_width_option.xml`
- `addons/website_blog/static/src/website_builder/blog_page_option.xml`
- `addons/website_blog/static/src/website_builder/blog_page_option_plugin.js`
- `addons/website_blog/static/src/website_builder/blog_post_page_option.xml`
- `addons/website_blog/static/src/website_builder/blog_post_page_option_plugin.js`
- `addons/website_blog/static/src/website_builder/blog_post_tags_option.js`
- `addons/website_blog/static/src/website_builder/blog_post_tags_option.xml`
- `addons/website_blog/static/src/website_builder/blog_searchbar_option_plugin.js`
- `addons/website_blog/static/src/website_builder/dynamic_snippet_blog_posts_carousel_option.js`
- `addons/website_blog/static/src/website_builder/dynamic_snippet_blog_posts_carousel_option.xml`
- `addons/website_blog/static/src/website_builder/dynamic_snippet_blog_posts_option.js`
- `addons/website_blog/static/src/website_builder/dynamic_snippet_blog_posts_option.xml`
- `addons/website_blog/static/src/website_builder/dynamic_snippet_blog_posts_option_plugin.js`
- `addons/website_blog/static/src/website_builder/dynamic_snippet_blog_posts_shared_option.xml`
- `addons/website_blog/static/tests/interactions/snippets/blog_posts.test.js`
- `addons/website_blog/static/tests/interactions/snippets/website_blog.test.js`
- `addons/website_blog/static/tests/tours/blog_context.js`
- `addons/website_blog/static/tests/tours/blog_manager_tour.js`
- `addons/website_blog/static/tests/tours/blog_posts_dynamic_snippet.js`
- `addons/website_blog/static/tests/tours/blog_posts_dynamic_snippet_visibility.js`
- `addons/website_blog/static/tests/tours/blog_search_with_date.js`
- `addons/website_blog/static/tests/tours/blog_sidebar_with_date_and_tag.js`
- `addons/website_blog/static/tests/tours/blog_tags_tour.js`
- `addons/website_blog/static/tests/tours/blog_tags_with_date.js`
- `addons/website_blog/static/tests/tours/snippet_blog_post.js`
- `addons/website_blog/static/tests/tours/sub_templates_config.js`
- `addons/website_blog/static/tests/website_builder/many2one_option.test.js`
- `addons/website_blog/static/tests/website_builder/snippet_filter.test.js`
- `addons/website_blog/tests/__init__.py`
- `addons/website_blog/tests/common.py`
- `addons/website_blog/tests/test_performance.py`
- `addons/website_blog/tests/test_sitemap.py`
- `addons/website_blog/tests/test_ui.py`
- `addons/website_blog/tests/test_website_blog_flow.py`
- `addons/website_blog/tests/test_website_blog_technical_page.py`
- `addons/website_blog/views/blog_post_add.xml`
- `addons/website_blog/views/snippets/s_blog_posts.xml`
- `addons/website_blog/views/snippets/s_blog_posts_carousel.xml`
- `addons/website_blog/views/snippets/s_dynamic_snippet_blog_posts_carousel_preview_data.xml`
- `addons/website_blog/views/snippets/s_dynamic_snippet_blog_posts_preview_data.xml`
- `addons/website_blog/views/snippets/snippets.xml`
- `addons/website_blog/views/website_blog_components.xml`
- `addons/website_blog/views/website_blog_posts_loop.xml`
- `addons/website_blog/views/website_blog_templates.xml`
- `addons/website_blog/views/website_blog_views.xml`
- `addons/website_blog/views/website_blog_visitor_views.xml`
- `addons/website_blog/views/website_pages_views.xml`
