# Module: mass_mailing_themes

- **Module ID:** MOD-373
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/mass_mailing_themes`
- **Manifest:** `addons/mass_mailing_themes/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Email Marketing`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Design gorgeous mails

**Manifest description:**

Design gorgeous mails

**Scope evidence:** The module contains 132 files, including 2 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `mass_mailing`.

## 2. Module structure

- Model/business logic files: 0
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 23 record/template/menu identifiers.
- **Evidence:** `addons/mass_mailing_themes/data/ir_attachment_data.xml:6`, `addons/mass_mailing_themes/data/ir_attachment_data.xml:16`, `addons/mass_mailing_themes/data/ir_attachment_data.xml:26`, `addons/mass_mailing_themes/data/ir_attachment_data.xml:36`, `addons/mass_mailing_themes/data/ir_attachment_data.xml:44`, `addons/mass_mailing_themes/data/ir_attachment_data.xml:52`, `addons/mass_mailing_themes/data/ir_attachment_data.xml:60`, `addons/mass_mailing_themes/data/ir_attachment_data.xml:68`, `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:4`, `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:77`, `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:241`, `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:390`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `mass_mailing_themes.s_tech_default_image`, `mass_mailing_themes.s_default_image_block_image`, `mass_mailing_themes.s_picture_default_image_2`, `mass_mailing_themes.s_company_team_default_image_1`, `mass_mailing_themes.s_company_team_default_image_2`, `mass_mailing_themes.s_company_team_default_image_3`, `mass_mailing_themes.s_company_team_default_image_4`, `mass_mailing_themes.s_picture_default_image`, `email_designer_themes`, `theme_event_template`, `theme_blogging_template`, `theme_coupon_template`, `theme_magazine_template`, `theme_bignews_template`, `theme_promotion_template`, `theme_coffeebreak_template`, `theme_newsletter_template`, `theme_roadshow1_template`, `theme_roadshow2_template`, `theme_training_template`
- Menus: 0; representative evidence: Not found in module
- Templates: 15; representative evidence: `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:4`, `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:77`, `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:241`, `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:390`, `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:488`, `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:659`, `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:804`, `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:1006`, `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:1168`, `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:1364`, `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:1489`, `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml:1565`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/mass_mailing_themes/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mass_mailing`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Not found
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/mass_mailing_themes/__init__.py`
- `addons/mass_mailing_themes/__manifest__.py`
- `addons/mass_mailing_themes/data/ir_attachment_data.xml`
- `addons/mass_mailing_themes/i18n/ar.po`
- `addons/mass_mailing_themes/i18n/az.po`
- `addons/mass_mailing_themes/i18n/bg.po`
- `addons/mass_mailing_themes/i18n/bs.po`
- `addons/mass_mailing_themes/i18n/ca.po`
- `addons/mass_mailing_themes/i18n/cs.po`
- `addons/mass_mailing_themes/i18n/da.po`
- `addons/mass_mailing_themes/i18n/de.po`
- `addons/mass_mailing_themes/i18n/el.po`
- `addons/mass_mailing_themes/i18n/es.po`
- `addons/mass_mailing_themes/i18n/es_419.po`
- `addons/mass_mailing_themes/i18n/et.po`
- `addons/mass_mailing_themes/i18n/fa.po`
- `addons/mass_mailing_themes/i18n/fi.po`
- `addons/mass_mailing_themes/i18n/fr.po`
- `addons/mass_mailing_themes/i18n/he.po`
- `addons/mass_mailing_themes/i18n/hi.po`
- `addons/mass_mailing_themes/i18n/hr.po`
- `addons/mass_mailing_themes/i18n/hu.po`
- `addons/mass_mailing_themes/i18n/id.po`
- `addons/mass_mailing_themes/i18n/it.po`
- `addons/mass_mailing_themes/i18n/ja.po`
- `addons/mass_mailing_themes/i18n/kab.po`
- `addons/mass_mailing_themes/i18n/ko.po`
- `addons/mass_mailing_themes/i18n/ku.po`
- `addons/mass_mailing_themes/i18n/lo.po`
- `addons/mass_mailing_themes/i18n/lt.po`
- `addons/mass_mailing_themes/i18n/lv.po`
- `addons/mass_mailing_themes/i18n/mass_mailing_themes.pot`
- `addons/mass_mailing_themes/i18n/mn.po`
- `addons/mass_mailing_themes/i18n/my.po`
- `addons/mass_mailing_themes/i18n/nb.po`
- `addons/mass_mailing_themes/i18n/nl.po`
- `addons/mass_mailing_themes/i18n/pl.po`
- `addons/mass_mailing_themes/i18n/pt.po`
- `addons/mass_mailing_themes/i18n/pt_BR.po`
- `addons/mass_mailing_themes/i18n/ro.po`
- `addons/mass_mailing_themes/i18n/ru.po`
- `addons/mass_mailing_themes/i18n/sk.po`
- `addons/mass_mailing_themes/i18n/sl.po`
- `addons/mass_mailing_themes/i18n/sr@latin.po`
- `addons/mass_mailing_themes/i18n/sv.po`
- `addons/mass_mailing_themes/i18n/th.po`
- `addons/mass_mailing_themes/i18n/tr.po`
- `addons/mass_mailing_themes/i18n/uk.po`
- `addons/mass_mailing_themes/i18n/uz.po`
- `addons/mass_mailing_themes/i18n/vi.po`
- `addons/mass_mailing_themes/i18n/zh_CN.po`
- `addons/mass_mailing_themes/i18n/zh_TW.po`
- `addons/mass_mailing_themes/static/src/img/theme_bignews/s_default_image_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_bignews/s_picture_default_image_2.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_bignews/set_ui_landscape_sm_1.webp`
- `addons/mass_mailing_themes/static/src/img/theme_bignews/set_ui_landscape_sm_2.webp`
- `addons/mass_mailing_themes/static/src/img/theme_bignews/set_ui_landscape_sm_3.webp`
- `addons/mass_mailing_themes/static/src/img/theme_bignews/set_ui_landscape_sm_4.webp`
- `addons/mass_mailing_themes/static/src/img/theme_blogging/s_default_image_media_list_1.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_blogging/s_default_image_media_list_2.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_blogging/s_default_image_media_list_3.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_blogging/s_tech_default_image.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_blogging/tech_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_coffeebreak/s_default_image_block_banner.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_coffeebreak/s_default_image_block_image_text.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_coffeebreak/s_default_image_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_coupon/company_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_cta_centric/company_logo_dark.png`
- `addons/mass_mailing_themes/static/src/img/theme_cta_centric/s_bento_block_default_image_1.webp`
- `addons/mass_mailing_themes/static/src/img/theme_cta_centric/s_bento_block_default_image_2.webp`
- `addons/mass_mailing_themes/static/src/img/theme_event/s_cover_default_image.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_event/s_default_image_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_event/s_default_image_media_list_1.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_event/s_default_image_media_list_2.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_event/s_default_image_media_list_3.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/bignews_thumb_large.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/bignews_thumb_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/bignews_thumb_small.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/blogging_thumb_large.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/blogging_thumb_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/blogging_thumb_small.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/catalog_thumb_large.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/catalog_thumb_small.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/coffee_break_thumb_large.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/coffee_break_thumb_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/coffee_break_thumb_small.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/coupon_thumb_large.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/coupon_thumb_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/coupon_thumb_small.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/event_thumb_large.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/event_thumb_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/event_thumb_small.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/event_updates_thumb_large.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/event_updates_thumb_small.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/magazine_thumb_large.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/magazine_thumb_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/magazine_thumb_small.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/newsletter_thumb_large.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/newsletter_thumb_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/newsletter_thumb_small.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/promotion_thumb_large.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/promotion_thumb_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/promotion_thumb_small.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/roadshow_followup_thumb_large.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/roadshow_followup_thumb_small.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/roadshow_schedule_thumb_large.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/roadshow_schedule_thumb_small.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/roadshow_thumb_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/terms_thumb_large.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/terms_thumb_small.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/training_thumb_large.webp`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/training_thumb_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_imgs/training_thumb_small.webp`
- `addons/mass_mailing_themes/static/src/img/theme_magazine/s_default_image_image_text.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_magazine/s_default_image_image_text_2.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_magazine/s_default_image_product_1.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_magazine/s_default_image_product_2.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_newsletter/FPsignature.gif`
- `addons/mass_mailing_themes/static/src/img/theme_newsletter/s_default_image_block_banner.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_newsletter/s_default_image_block_banner_2.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_newsletter/s_default_image_block_banner_3.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_newsletter/social-facebook.png`
- `addons/mass_mailing_themes/static/src/img/theme_newsletter/social-linkedin.png`
- `addons/mass_mailing_themes/static/src/img/theme_newsletter/social-twitter.png`
- `addons/mass_mailing_themes/static/src/img/theme_promotion/company_logo.png`
- `addons/mass_mailing_themes/static/src/img/theme_promotion/company_logo_dark.png`
- `addons/mass_mailing_themes/static/src/img/theme_promotion/s_picture_default_image.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_training/s_default_image_block_banner.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_training/s_default_image_block_image.jpg`
- `addons/mass_mailing_themes/static/src/img/theme_training/see_you_soon.svg`
- `addons/mass_mailing_themes/static/src/img/theme_vip/vip_logo.png`
- `addons/mass_mailing_themes/views/mass_mailing_themes_templates.xml`
