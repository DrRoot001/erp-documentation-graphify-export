# Module: website

- **Module ID:** MOD-596
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website`
- **Manifest:** `addons/website/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Enterprise website builder

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 1812 files, including 103 Python, 418 XML, and 674 JavaScript/TypeScript files. The manifest declares dependencies: `digest`, `web`, `html_editor`, `http_routing`, `portal`, `social_media`, `auth_signup`, `mail`, `google_recaptcha`, `utm`, `html_builder`.

## 2. Module structure

- Model/business logic files: 68
- Controller/API files: 7
- XML/data/view/template files: 418
- Browser asset files: 674
- Security files: 2
- Test files: 49
- Scheduled/automation evidence files: 12
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website/security/ir.access.csv`, `addons/website/security/website_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 68 model declarations, 1170 methods, 13 constraint handlers, 5 onchange handlers, and 50 dependency declarations.
- **Evidence:** `addons/website/models/res_partner.py:8`, `addons/website/models/ir_access.py:4`, `addons/website/models/html_text_processor.py:15`, `addons/website/models/res_lang.py:8`, `addons/website/models/digest.py:6`, `addons/website/models/website_menu.py:15`, `addons/website/models/ir_ui_view.py:19`, `addons/website/models/res_groups.py:6`, `addons/website/models/website_snippet_filter.py:14`, `addons/website/models/ir_asset.py:7`, `addons/website/models/res_config_settings.py:11`, `addons/website/models/ir_qweb.py:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 7 controller files and 65 route declarations.
- **Evidence:** `addons/website/controllers/form.py:24`, `addons/website/controllers/form.py:30`, `addons/website/controllers/binary.py:7`, `addons/website/controllers/backend.py:10`, `addons/website/controllers/backend.py:35`, `addons/website/controllers/backend.py:39`, `addons/website/controllers/backend.py:46`, `addons/website/controllers/webclient.py:9`, `addons/website/controllers/model_page.py:12`, `addons/website/controllers/main.py:189`, `addons/website/controllers/main.py:244`, `addons/website/controllers/main.py:254`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 418 XML files and 674 JavaScript/TypeScript files; static XML analysis found 812 record/template/menu identifiers.
- **Evidence:** `addons/website/security/website_security.xml:2`, `addons/website/security/website_security.xml:8`, `addons/website/security/website_security.xml:14`, `addons/website/security/website_security.xml:26`, `addons/website/security/website_security.xml:30`, `addons/website/security/website_security.xml:34`, `addons/website/wizard/website_robots.xml:4`, `addons/website/wizard/website_llms.xml:4`, `addons/website/wizard/base_language_install_views.xml:4`, `addons/website/wizard/blocked_third_party_domains.xml:4`, `addons/website/data/digest_data.xml:4`, `addons/website/data/digest_data.xml:11`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/website/security/ir.access.csv`, `addons/website/security/website_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 12 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/website/__manifest__.py`, `addons/website/models/website_snippet_filter.py`, `addons/website/models/website_visitor.py`, `addons/website/models/ir_actions_server.py`, `addons/website/models/mixins.py`, `addons/website/controllers/main.py`, `addons/website/data/ir_cron_data.xml`, `addons/website/data/website_visitor_cron.xml`, `addons/website/views/ir_actions_server_views.xml`, `addons/website/views/website_views.xml`, `addons/website/tests/test_controllers.py`, `addons/website/tests/test_website_visitor.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 49 test files are present.
- **Evidence:** `addons/website/tests/test_header_search.py`, `addons/website/tests/test_grid_layout.py`, `addons/website/tests/test_fuzzy.py`, `addons/website/tests/test_website_website_builder_assets_bundle.py`, `addons/website/tests/test_skip_website_configurator.py`, `addons/website/tests/test_controllers.py`, `addons/website/tests/test_menu.py`, `addons/website/tests/test_performance.py`, `addons/website/tests/test_lang_url.py`, `addons/website/tests/test_client_action.py`, `addons/website/tests/test_crawl.py`, `addons/website/tests/test_iap.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 418; representative identifiers: `res_groups_privilege_website`, `group_website_restricted_editor`, `group_website_designer`, `website_page_controller_expose`, `base.group_public`, `base.group_portal`, `view_edit_robots`, `view_edit_llms`, `view_base_language_install`, `view_edit_third_party_domains`, `digest.digest_digest_default`, `digest_tip_website_0`, `digest_tip_website_1`, `digest_tip_website_2`, `digest_tip_website_3`, `digest_tip_website_4`, `bs_debug_view`, `color_combinations_debug_view`, `snippets_debug_view`, `base.default_user_group`
- Menus: 24; representative evidence: `addons/website/views/website_pages_views.xml:213`, `addons/website/views/website_visitor_views.xml:317`, `addons/website/views/website_visitor_views.xml:321`, `addons/website/views/res_config_settings_views.xml:291`, `addons/website/views/res_config_settings_views.xml:294`, `addons/website/views/res_config_settings_views.xml:301`, `addons/website/views/res_config_settings_views.xml:304`, `addons/website/views/res_config_settings_views.xml:312`, `addons/website/views/website_controller_pages_views.xml:107`, `addons/website/views/website_views.xml:341`, `addons/website/views/website_views.xml:347`, `addons/website/views/website_views.xml:352`
- Templates: 412; representative evidence: `addons/website/data/website_data.xml:17`, `addons/website/data/website_data.xml:22`, `addons/website/data/website_data.xml:246`, `addons/website/data/website_data.xml:390`, `addons/website/data/website_data.xml:408`, `addons/website/data/website_data.xml:426`, `addons/website/data/website_data.xml:444`, `addons/website/views/neutralize_views.xml:3`, `addons/website/views/theme_colors_preview.xml:4`, `addons/website/views/http_routing_template.xml:4`, `addons/website/views/http_routing_template.xml:12`, `addons/website/views/http_routing_template.xml:20`
- View/action field declarations: 177; representative evidence: `addons/website/wizard/website_robots.xml:6`, `addons/website/wizard/website_robots.xml:7`, `addons/website/wizard/website_llms.xml:6`, `addons/website/wizard/website_llms.xml:7`, `addons/website/wizard/base_language_install_views.xml:6`, `addons/website/wizard/base_language_install_views.xml:8`, `addons/website/wizard/blocked_third_party_domains.xml:6`, `addons/website/wizard/blocked_third_party_domains.xml:7`, `addons/website/data/website_demo.xml:8`, `addons/website/data/website_demo.xml:471`, `addons/website/data/website_demo.xml:592`, `addons/website/data/website_data.xml:222`
- Browser assets: 674; representative files: `addons/website/static/tests/publish_website_systray_item.test.js`, `addons/website/static/tests/page_url_field.test.js`, `addons/website/static/tests/new_content_systray_item.test.js`, `addons/website/static/tests/website_loader.test.js`, `addons/website/static/tests/redirect_field.test.js`, `addons/website/static/tests/helpers.js`, `addons/website/static/lib/multirange/multirange_custom.js`, `addons/website/static/src/services/website_service.js`, `addons/website/static/src/services/website_custom_menus.js`, `addons/website/static/src/services/google_maps_service.js`, `addons/website/static/src/@types/registries.d.ts`, `addons/website/static/src/@types/plugins.d.ts`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website/__manifest__.py`
- **HTTP entry points:** `addons/website/controllers/form.py:24`, `addons/website/controllers/form.py:30`, `addons/website/controllers/binary.py:7`, `addons/website/controllers/backend.py:10`, `addons/website/controllers/backend.py:35`, `addons/website/controllers/backend.py:39`, `addons/website/controllers/backend.py:46`, `addons/website/controllers/webclient.py:9`, `addons/website/controllers/model_page.py:12`, `addons/website/controllers/main.py:189`, `addons/website/controllers/main.py:244`, `addons/website/controllers/main.py:254`
- **Scheduled entry points:** `addons/website/__manifest__.py`, `addons/website/models/website_snippet_filter.py`, `addons/website/models/website_visitor.py`, `addons/website/models/ir_actions_server.py`, `addons/website/models/mixins.py`, `addons/website/controllers/main.py`, `addons/website/data/ir_cron_data.xml`, `addons/website/data/website_visitor_cron.xml`, `addons/website/views/ir_actions_server_views.xml`, `addons/website/views/website_views.xml`, `addons/website/tests/test_controllers.py`, `addons/website/tests/test_website_visitor.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 68
- Representative model evidence: `res.partner` (addons/website/models/res_partner.py:8); inherits `ir.access` (addons/website/models/ir_access.py:4); `website.html.text.processor` (addons/website/models/html_text_processor.py:15); inherits `res.lang` (addons/website/models/res_lang.py:8); inherits `digest.digest` (addons/website/models/digest.py:6); `website.menu` (addons/website/models/website_menu.py:15); `ir.ui.view` (addons/website/models/ir_ui_view.py:19); inherits `res.groups` (addons/website/models/res_groups.py:6); `website.snippet.filter` (addons/website/models/website_snippet_filter.py:14); inherits `ir.asset` (addons/website/models/ir_asset.py:7); inherits `res.config.settings` (addons/website/models/res_config_settings.py:11); inherits `ir.qweb` (addons/website/models/ir_qweb.py:15); inherits `base` (addons/website/models/ir_model.py:6); `website.controller.page` (addons/website/models/website_controller_page.py:7); inherits `website` (addons/website/models/website_form.py:13); inherits `ir.model` (addons/website/models/website_form.py:22); inherits `ir.model.fields` (addons/website/models/website_form.py:153); `website.configurator.feature` (addons/website/models/website_configurator_feature.py:7); inherits `ir.binary` (addons/website/models/ir_binary.py:4); `website.route` (addons/website/models/website_rewrite.py:13); `website.rewrite` (addons/website/models/website_rewrite.py:52); `website.track` (addons/website/models/website_visitor.py:17); `website.visitor` (addons/website/models/website_visitor.py:29); `website.page.properties.base` (addons/website/models/website_page_properties.py:6); `website.page.properties` (addons/website/models/website_page_properties.py:194); `theme.ir.asset` (addons/website/models/theme_models.py:13); `theme.ir.ui.view` (addons/website/models/theme_models.py:51); `theme.ir.attachment` (addons/website/models/theme_models.py:111); `theme.website.menu` (addons/website/models/theme_models.py:135); `theme.website.page` (addons/website/models/theme_models.py:176)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 7
- Route declarations: 65
- Route evidence: `addons/website/controllers/form.py:24`, `addons/website/controllers/form.py:30`, `addons/website/controllers/binary.py:7`, `addons/website/controllers/backend.py:10`, `addons/website/controllers/backend.py:35`, `addons/website/controllers/backend.py:39`, `addons/website/controllers/backend.py:46`, `addons/website/controllers/webclient.py:9`, `addons/website/controllers/model_page.py:12`, `addons/website/controllers/main.py:189`, `addons/website/controllers/main.py:244`, `addons/website/controllers/main.py:254`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `digest`, `web`, `html_editor`, `http_routing`, `portal`, `social_media`, `auth_signup`, `mail`, `google_recaptcha`, `utm`, `html_builder`
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

- `addons/website/README.md`
- `addons/website/__init__.py`
- `addons/website/__manifest__.py`
- `addons/website/controllers/__init__.py`
- `addons/website/controllers/backend.py`
- `addons/website/controllers/binary.py`
- `addons/website/controllers/form.py`
- `addons/website/controllers/main.py`
- `addons/website/controllers/model_page.py`
- `addons/website/controllers/webclient.py`
- `addons/website/data/digest_data.xml`
- `addons/website/data/image_library.xml`
- `addons/website/data/ir_asset.xml`
- `addons/website/data/ir_cron_data.xml`
- `addons/website/data/mail_mail_data.xml`
- `addons/website/data/neutralize.sql`
- `addons/website/data/update_theme_images.xml`
- `addons/website/data/website_data.xml`
- `addons/website/data/website_demo.xml`
- `addons/website/data/website_visitor_cron.xml`
- `addons/website/data/website_visitor_demo.xml`
- `addons/website/doc/website.snippet.rst`
- `addons/website/i18n/ar.po`
- `addons/website/i18n/az.po`
- `addons/website/i18n/bg.po`
- `addons/website/i18n/bs.po`
- `addons/website/i18n/ca.po`
- `addons/website/i18n/cs.po`
- `addons/website/i18n/da.po`
- `addons/website/i18n/de.po`
- `addons/website/i18n/el.po`
- `addons/website/i18n/es.po`
- `addons/website/i18n/es_419.po`
- `addons/website/i18n/et.po`
- `addons/website/i18n/fa.po`
- `addons/website/i18n/fi.po`
- `addons/website/i18n/fr.po`
- `addons/website/i18n/gu.po`
- `addons/website/i18n/he.po`
- `addons/website/i18n/hi.po`
- `addons/website/i18n/hr.po`
- `addons/website/i18n/hu.po`
- `addons/website/i18n/id.po`
- `addons/website/i18n/is.po`
- `addons/website/i18n/it.po`
- `addons/website/i18n/ja.po`
- `addons/website/i18n/ka.po`
- `addons/website/i18n/kab.po`
- `addons/website/i18n/km.po`
- `addons/website/i18n/ko.po`
- `addons/website/i18n/ku.po`
- `addons/website/i18n/lb.po`
- `addons/website/i18n/lo.po`
- `addons/website/i18n/lt.po`
- `addons/website/i18n/lv.po`
- `addons/website/i18n/mk.po`
- `addons/website/i18n/mn.po`
- `addons/website/i18n/my.po`
- `addons/website/i18n/nb.po`
- `addons/website/i18n/nl.po`
- `addons/website/i18n/pl.po`
- `addons/website/i18n/pt.po`
- `addons/website/i18n/pt_BR.po`
- `addons/website/i18n/ro.po`
- `addons/website/i18n/ru.po`
- `addons/website/i18n/sk.po`
- `addons/website/i18n/sl.po`
- `addons/website/i18n/sr@latin.po`
- `addons/website/i18n/sv.po`
- `addons/website/i18n/th.po`
- `addons/website/i18n/tr.po`
- `addons/website/i18n/uk.po`
- `addons/website/i18n/uz.po`
- `addons/website/i18n/vi.po`
- `addons/website/i18n/website.pot`
- `addons/website/i18n/zh_CN.po`
- `addons/website/i18n/zh_TW.po`
- `addons/website/models/__init__.py`
- `addons/website/models/assets.py`
- `addons/website/models/base_partner_merge.py`
- `addons/website/models/digest.py`
- `addons/website/models/html_text_processor.py`
- `addons/website/models/ir_access.py`
- `addons/website/models/ir_actions_server.py`
- `addons/website/models/ir_asset.py`
- `addons/website/models/ir_attachment.py`
- `addons/website/models/ir_binary.py`
- `addons/website/models/ir_http.py`
- `addons/website/models/ir_model.py`
- `addons/website/models/ir_model_data.py`
- `addons/website/models/ir_module_module.py`
- `addons/website/models/ir_qweb.py`
- `addons/website/models/ir_qweb_fields.py`
- `addons/website/models/ir_ui_menu.py`
- `addons/website/models/ir_ui_view.py`
- `addons/website/models/mixins.py`
- `addons/website/models/models.py`
- `addons/website/models/res_company.py`
- `addons/website/models/res_config_settings.py`
- `addons/website/models/res_groups.py`
- `addons/website/models/res_lang.py`
- `addons/website/models/res_partner.py`
- `addons/website/models/res_users.py`
- `addons/website/models/theme_models.py`
- `addons/website/models/website.py`
- `addons/website/models/website_configurator_feature.py`
- `addons/website/models/website_controller_page.py`
- `addons/website/models/website_form.py`
- `addons/website/models/website_menu.py`
- `addons/website/models/website_page.py`
- `addons/website/models/website_page_properties.py`
- `addons/website/models/website_rewrite.py`
- `addons/website/models/website_snippet_filter.py`
- `addons/website/models/website_technical_page.py`
- `addons/website/models/website_visitor.py`
- `addons/website/security/ir.access.csv`
- `addons/website/security/website_security.xml`
- `addons/website/static/description/icon.png`
- `addons/website/static/description/icon.svg`
- `addons/website/static/description/icon_hi.png`
- `addons/website/static/lib/multirange/LICENSE`
- `addons/website/static/lib/multirange/multirange_custom.js`
- `addons/website/static/lib/multirange/multirange_custom.scss`
- `addons/website/static/shapes/footer_mega_cards_image.svg`
- `addons/website/static/shapes/s_attributes_1.svg`
- `addons/website/static/shapes/s_attributes_2.svg`
- `addons/website/static/shapes/s_attributes_3.svg`
- `addons/website/static/shapes/s_attributes_4.svg`
- `addons/website/static/shapes/s_hero_maintenance.svg`
- `addons/website/static/src/@types/plugins.d.ts`
- `addons/website/static/src/@types/registries.d.ts`
- `addons/website/static/src/@types/services.d.ts`
- `addons/website/static/src/builder/builder_urlpicker.js`
- `addons/website/static/src/builder/builder_urlpicker.xml`
- `addons/website/static/src/builder/icon_selector.js`
- `addons/website/static/src/builder/plugins/achievements_list_option.xml`
- `addons/website/static/src/builder/plugins/achievements_list_option_plugin.js`
- `addons/website/static/src/builder/plugins/bootstrap_option_plugin.js`
- `addons/website/static/src/builder/plugins/carousel_bottom_controllers_option.xml`
- `addons/website/static/src/builder/plugins/carousel_cards.edit.xml`
- `addons/website/static/src/builder/plugins/carousel_cards_option.xml`
- `addons/website/static/src/builder/plugins/carousel_item_header_buttons.js`
- `addons/website/static/src/builder/plugins/carousel_option.js`
- `addons/website/static/src/builder/plugins/carousel_option.xml`
- `addons/website/static/src/builder/plugins/carousel_option_plugin.js`
- `addons/website/static/src/builder/plugins/collapse_plugin.js`
- `addons/website/static/src/builder/plugins/company_team_plugin.js`
- `addons/website/static/src/builder/plugins/content_width_option.edit.scss`
- `addons/website/static/src/builder/plugins/content_width_option.xml`
- `addons/website/static/src/builder/plugins/content_width_option_plugin.js`
- `addons/website/static/src/builder/plugins/customize_website_plugin.js`
- `addons/website/static/src/builder/plugins/dynamic_svg_option.js`
- `addons/website/static/src/builder/plugins/dynamic_svg_option.xml`
- `addons/website/static/src/builder/plugins/dynamic_svg_option_plugin.js`
- `addons/website/static/src/builder/plugins/edit_interaction_plugin.js`
- `addons/website/static/src/builder/plugins/editable_button_plugin.js`
- `addons/website/static/src/builder/plugins/floating_blocks/floating_blocks.edit.xml`
- `addons/website/static/src/builder/plugins/floating_blocks/floating_blocks_block_mobile_option.js`
- `addons/website/static/src/builder/plugins/floating_blocks/floating_blocks_block_option.js`
- `addons/website/static/src/builder/plugins/floating_blocks/floating_blocks_block_option_plugin.js`
- `addons/website/static/src/builder/plugins/floating_blocks/floating_blocks_option.xml`
- `addons/website/static/src/builder/plugins/floating_blocks/floating_blocks_option_plugin.js`
- `addons/website/static/src/builder/plugins/floating_snippets_plugin.js`
- `addons/website/static/src/builder/plugins/font/add_font_dialog.js`
- `addons/website/static/src/builder/plugins/font/add_font_dialog.xml`
- `addons/website/static/src/builder/plugins/font/builder.fonts.scss`
- `addons/website/static/src/builder/plugins/font/font_plugin.js`
- `addons/website/static/src/builder/plugins/font_awesome_option.xml`
- `addons/website/static/src/builder/plugins/font_awesome_option_plugin.js`
- `addons/website/static/src/builder/plugins/form/form.edit.xml`
- `addons/website/static/src/builder/plugins/form/form_action_fields_option.js`
- `addons/website/static/src/builder/plugins/form/form_field_option.js`
- `addons/website/static/src/builder/plugins/form/form_field_option_redraw.js`
- `addons/website/static/src/builder/plugins/form/form_option.edit.scss`
- `addons/website/static/src/builder/plugins/form/form_option.js`
- `addons/website/static/src/builder/plugins/form/form_option.xml`
- `addons/website/static/src/builder/plugins/form/form_option_add_field_button.js`
- `addons/website/static/src/builder/plugins/form/form_option_plugin.js`
- `addons/website/static/src/builder/plugins/form/utils.js`
- `addons/website/static/src/builder/plugins/highlight/highlight_configurator.js`
- `addons/website/static/src/builder/plugins/highlight/highlight_configurator.xml`
- `addons/website/static/src/builder/plugins/highlight/highlight_picker.js`
- `addons/website/static/src/builder/plugins/highlight/highlight_picker.xml`
- `addons/website/static/src/builder/plugins/highlight/highlight_plugin.js`
- `addons/website/static/src/builder/plugins/highlight/stacking_component.js`
- `addons/website/static/src/builder/plugins/http_error_option.js`
- `addons/website/static/src/builder/plugins/http_error_option.xml`
- `addons/website/static/src/builder/plugins/image/grid_image_option.js`
- `addons/website/static/src/builder/plugins/image/grid_image_option.xml`
- `addons/website/static/src/builder/plugins/image/grid_image_option_plugin.js`
- `addons/website/static/src/builder/plugins/image/image_hover_plugin.js`
- `addons/website/static/src/builder/plugins/image/image_popup_option.js`
- `addons/website/static/src/builder/plugins/image/image_popup_option.xml`
- `addons/website/static/src/builder/plugins/image/image_tool_option.xml`
- `addons/website/static/src/builder/plugins/layout_option/grid_column_option.xml`
- `addons/website/static/src/builder/plugins/layout_option/grid_column_option_plugin.js`
- `addons/website/static/src/builder/plugins/layout_option/layout_option.js`
- `addons/website/static/src/builder/plugins/layout_option/layout_option.xml`
- `addons/website/static/src/builder/plugins/layout_option/layout_option_plugin.js`
- `addons/website/static/src/builder/plugins/layout_option/spacing_option.js`
- `addons/website/static/src/builder/plugins/layout_option/spacing_option.xml`
- `addons/website/static/src/builder/plugins/layout_option/spacing_option_plugin.js`
- `addons/website/static/src/builder/plugins/menu_data_plugin.js`
- `addons/website/static/src/builder/plugins/navbar_link_popover/navbar_link_popover.js`
- `addons/website/static/src/builder/plugins/navbar_link_popover/navbar_link_popover.xml`
- `addons/website/static/src/builder/plugins/options/accordion_option.xml`
- `addons/website/static/src/builder/plugins/options/accordion_option_plugin.js`
- `addons/website/static/src/builder/plugins/options/age_verification_popup.edit.xml`
- `addons/website/static/src/builder/plugins/options/age_verification_popup_option.xml`
- `addons/website/static/src/builder/plugins/options/age_verification_popup_option_plugin.js`
- `addons/website/static/src/builder/plugins/options/animate_option.js`
- `addons/website/static/src/builder/plugins/options/animate_option.xml`
- `addons/website/static/src/builder/plugins/options/animate_option_plugin.js`
- `addons/website/static/src/builder/plugins/options/animate_text.js`
- `addons/website/static/src/builder/plugins/options/animate_text.scss`
- `addons/website/static/src/builder/plugins/options/animate_text.xml`
- `addons/website/static/src/builder/plugins/options/animated_number_option.xml`
- `addons/website/static/src/builder/plugins/options/animated_number_option_plugin.js`
- `addons/website/static/src/builder/plugins/options/announcement_scroll_option.xml`
- `addons/website/static/src/builder/plugins/options/announcement_scroll_option_plugin.js`
- `addons/website/static/src/builder/plugins/options/avatars_header_buttons.js`
- `addons/website/static/src/builder/plugins/options/avatars_option.xml`
- `addons/website/static/src/builder/plugins/options/avatars_option_plugin.js`
- `addons/website/static/src/builder/plugins/options/background_option.js`
- `addons/website/static/src/builder/plugins/options/background_option.xml`
- `addons/website/static/src/builder/plugins/options/background_option_plugin.js`
- `addons/website/static/src/builder/plugins/options/background_video_option.xml`
- `addons/website/static/src/builder/plugins/options/base_visibility_option.js`
- `addons/website/static/src/builder/plugins/options/base_visibility_option.xml`
- `addons/website/static/src/builder/plugins/options/bento_border_option.xml`
- `addons/website/static/src/builder/plugins/options/bg_blur_option.xml`
- `addons/website/static/src/builder/plugins/options/bg_blur_option_plugin.js`
- `addons/website/static/src/builder/plugins/options/blockquote_option.js`
- `addons/website/static/src/builder/plugins/options/blockquote_option.xml`
- `addons/website/static/src/builder/plugins/options/blockquote_option_plugin.js`
- `addons/website/static/src/builder/plugins/options/border_option.xml`
- `addons/website/static/src/builder/plugins/options/breadcrumb_option.js`
- `addons/website/static/src/builder/plugins/options/breadcrumb_option.xml`
- `addons/website/static/src/builder/plugins/options/button_option_plugin.js`
- `addons/website/static/src/builder/plugins/options/card_image.edit.xml`
- `addons/website/static/src/builder/plugins/options/card_image_option.js`
- `addons/website/static/src/builder/plugins/options/card_image_option.xml`
- `addons/website/static/src/builder/plugins/options/card_image_option_plugin.js`
- `addons/website/static/src/builder/plugins/options/card_image_position_option.js`
- `addons/website/static/src/builder/plugins/options/card_image_position_option.xml`
- `addons/website/static/src/builder/plugins/options/card_option.js`
- `addons/website/static/src/builder/plugins/options/card_option.xml`
- `addons/website/static/src/builder/plugins/options/card_option_plugin.js`
- `addons/website/static/src/builder/plugins/options/card_width_option.xml`
- `addons/website/static/src/builder/plugins/options/card_width_option_plugin.js`
- Additional source files not expanded in this page: 1562; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
