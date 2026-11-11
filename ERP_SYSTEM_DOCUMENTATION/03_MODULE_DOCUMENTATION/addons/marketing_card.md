# Module: marketing_card

- **Module ID:** MOD-360
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/marketing_card`
- **Manifest:** `addons/marketing_card/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Marketing/Marketing Card`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Generate dynamic shareable cards

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 100 files, including 19 Python, 12 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `link_tracker`, `mass_mailing`, `website`, `base_report_wkhtmltox`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 3
- XML/data/view/template files: 12
- Browser asset files: 1
- Security files: 2
- Test files: 3
- Scheduled/automation evidence files: 1
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/marketing_card/security/ir.access.csv`, `addons/marketing_card/security/marketing_card_groups.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 79 methods, 2 constraint handlers, 2 onchange handlers, and 11 dependency declarations.
- **Evidence:** `addons/marketing_card/models/card_template.py:11`, `addons/marketing_card/models/card_campaign_tag.py:6`, `addons/marketing_card/models/card_campaign.py:10`, `addons/marketing_card/models/card_card.py:6`, `addons/marketing_card/models/ir_model.py:4`, `addons/marketing_card/models/utm_source.py:4`, `addons/marketing_card/models/mailing_mailing.py:9`, `addons/marketing_card/wizards/mail_compose_message.py:10`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 6 route declarations.
- **Evidence:** `addons/marketing_card/controllers/marketing_card.py:33`, `addons/marketing_card/controllers/marketing_card.py:47`, `addons/marketing_card/controllers/marketing_card.py:65`, `addons/marketing_card/controllers/marketing_card_linkedin.py:17`, `addons/marketing_card/controllers/marketing_card_linkedin.py:44`, `addons/marketing_card/controllers/marketing_card_linkedin.py:88`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 12 XML files and 1 JavaScript/TypeScript files; static XML analysis found 45 record/template/menu identifiers.
- **Evidence:** `addons/marketing_card/demo/card_campaign_demo.xml:3`, `addons/marketing_card/demo/card_campaign_demo.xml:7`, `addons/marketing_card/security/marketing_card_groups.xml:2`, `addons/marketing_card/security/marketing_card_groups.xml:8`, `addons/marketing_card/security/marketing_card_groups.xml:15`, `addons/marketing_card/data/card_template_data.xml:2`, `addons/marketing_card/data/card_template_data.xml:8`, `addons/marketing_card/data/card_template_data.xml:18`, `addons/marketing_card/data/card_template_data.xml:29`, `addons/marketing_card/data/card_template_data.xml:40`, `addons/marketing_card/data/card_template_data.xml:47`, `addons/marketing_card/data/card_template_data.xml:58`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/marketing_card/security/ir.access.csv`, `addons/marketing_card/security/marketing_card_groups.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/marketing_card/models/card_card.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/marketing_card/models/card_campaign.py`, `addons/marketing_card/tests/common.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/marketing_card/tests/test_campaign.py`, `addons/marketing_card/tests/common.py`, `addons/marketing_card/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 12; representative identifiers: `card_campaign_tag_demo`, `card_campaign_campaign_1`, `res_groups_privilege_marketing_card`, `marketing_card_group_user`, `marketing_card_group_manager`, `card_template_light`, `card_template_dark`, `card_template_user_image`, `card_template_world_map`, `card_template_lila`, `card_template_safari`, `card_template_waves`, `card_template_lines`, `card_template_organic`, `card_template_blur`, `card_template_geometric`, `card_template_circles`, `card_template_avatar_highlight`, `card_template_drawings`, `utm_source_marketing_card`
- Menus: 4; representative evidence: `addons/marketing_card/views/card_menus.xml:3`, `addons/marketing_card/views/card_menus.xml:9`, `addons/marketing_card/views/card_menus.xml:17`, `addons/marketing_card/views/card_menus.xml:23`
- Templates: 10; representative evidence: `addons/marketing_card/views/website_templates.xml:3`, `addons/marketing_card/views/card_frontend_templates.xml:3`, `addons/marketing_card/views/card_frontend_templates.xml:64`, `addons/marketing_card/views/card_frontend_templates.xml:80`, `addons/marketing_card/views/card_card_templates.xml:8`, `addons/marketing_card/views/card_card_templates.xml:103`, `addons/marketing_card/views/card_card_templates.xml:186`, `addons/marketing_card/views/card_card_templates.xml:276`, `addons/marketing_card/views/card_card_templates.xml:367`, `addons/marketing_card/views/card_card_templates.xml:478`
- View/action field declarations: 26; representative evidence: `addons/marketing_card/views/card_card_views.xml:5`, `addons/marketing_card/views/card_card_views.xml:6`, `addons/marketing_card/views/card_card_views.xml:11`, `addons/marketing_card/views/card_card_views.xml:22`, `addons/marketing_card/views/card_card_views.xml:23`, `addons/marketing_card/views/card_card_views.xml:45`, `addons/marketing_card/views/card_card_views.xml:48`, `addons/marketing_card/views/mailing_mailing_views.xml:5`, `addons/marketing_card/views/mailing_mailing_views.xml:7`, `addons/marketing_card/views/card_campaign_views.xml:5`, `addons/marketing_card/views/card_campaign_views.xml:6`, `addons/marketing_card/views/card_campaign_views.xml:76`
- Browser assets: 1; representative files: `addons/marketing_card/static/src/interactions/linkedin_message_editor.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/marketing_card/__manifest__.py`
- **HTTP entry points:** `addons/marketing_card/controllers/marketing_card.py:33`, `addons/marketing_card/controllers/marketing_card.py:47`, `addons/marketing_card/controllers/marketing_card.py:65`, `addons/marketing_card/controllers/marketing_card_linkedin.py:17`, `addons/marketing_card/controllers/marketing_card_linkedin.py:44`, `addons/marketing_card/controllers/marketing_card_linkedin.py:88`
- **Scheduled entry points:** `addons/marketing_card/models/card_card.py`
- **Report entry points:** `addons/marketing_card/models/card_campaign.py`, `addons/marketing_card/tests/common.py`

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: `card.template` (addons/marketing_card/models/card_template.py:11); `card.campaign.tag` (addons/marketing_card/models/card_campaign_tag.py:6); `card.campaign` (addons/marketing_card/models/card_campaign.py:10); `card.card` (addons/marketing_card/models/card_card.py:6); inherits `ir.model` (addons/marketing_card/models/ir_model.py:4); inherits `utm.source` (addons/marketing_card/models/utm_source.py:4); inherits `mailing.mailing` (addons/marketing_card/models/mailing_mailing.py:9); inherits `mail.compose.message` (addons/marketing_card/wizards/mail_compose_message.py:10)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 6
- Route evidence: `addons/marketing_card/controllers/marketing_card.py:33`, `addons/marketing_card/controllers/marketing_card.py:47`, `addons/marketing_card/controllers/marketing_card.py:65`, `addons/marketing_card/controllers/marketing_card_linkedin.py:17`, `addons/marketing_card/controllers/marketing_card_linkedin.py:44`, `addons/marketing_card/controllers/marketing_card_linkedin.py:88`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `link_tracker`, `mass_mailing`, `website`, `base_report_wkhtmltox`
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

- `addons/marketing_card/__init__.py`
- `addons/marketing_card/__manifest__.py`
- `addons/marketing_card/controllers/__init__.py`
- `addons/marketing_card/controllers/marketing_card.py`
- `addons/marketing_card/controllers/marketing_card_linkedin.py`
- `addons/marketing_card/data/card_template_data.xml`
- `addons/marketing_card/data/utm_source_data.xml`
- `addons/marketing_card/demo/card_campaign_demo.xml`
- `addons/marketing_card/i18n/ar.po`
- `addons/marketing_card/i18n/az.po`
- `addons/marketing_card/i18n/bg.po`
- `addons/marketing_card/i18n/bs.po`
- `addons/marketing_card/i18n/ca.po`
- `addons/marketing_card/i18n/cs.po`
- `addons/marketing_card/i18n/da.po`
- `addons/marketing_card/i18n/de.po`
- `addons/marketing_card/i18n/el.po`
- `addons/marketing_card/i18n/es.po`
- `addons/marketing_card/i18n/es_419.po`
- `addons/marketing_card/i18n/et.po`
- `addons/marketing_card/i18n/fa.po`
- `addons/marketing_card/i18n/fi.po`
- `addons/marketing_card/i18n/fr.po`
- `addons/marketing_card/i18n/he.po`
- `addons/marketing_card/i18n/hi.po`
- `addons/marketing_card/i18n/hr.po`
- `addons/marketing_card/i18n/hu.po`
- `addons/marketing_card/i18n/id.po`
- `addons/marketing_card/i18n/it.po`
- `addons/marketing_card/i18n/ja.po`
- `addons/marketing_card/i18n/kab.po`
- `addons/marketing_card/i18n/ko.po`
- `addons/marketing_card/i18n/ku.po`
- `addons/marketing_card/i18n/lo.po`
- `addons/marketing_card/i18n/lt.po`
- `addons/marketing_card/i18n/lv.po`
- `addons/marketing_card/i18n/marketing_card.pot`
- `addons/marketing_card/i18n/mn.po`
- `addons/marketing_card/i18n/my.po`
- `addons/marketing_card/i18n/nb.po`
- `addons/marketing_card/i18n/nl.po`
- `addons/marketing_card/i18n/pl.po`
- `addons/marketing_card/i18n/pt.po`
- `addons/marketing_card/i18n/pt_BR.po`
- `addons/marketing_card/i18n/ro.po`
- `addons/marketing_card/i18n/ru.po`
- `addons/marketing_card/i18n/sk.po`
- `addons/marketing_card/i18n/sl.po`
- `addons/marketing_card/i18n/sr@latin.po`
- `addons/marketing_card/i18n/sv.po`
- `addons/marketing_card/i18n/th.po`
- `addons/marketing_card/i18n/tr.po`
- `addons/marketing_card/i18n/uk.po`
- `addons/marketing_card/i18n/uz.po`
- `addons/marketing_card/i18n/vi.po`
- `addons/marketing_card/i18n/zh_CN.po`
- `addons/marketing_card/i18n/zh_TW.po`
- `addons/marketing_card/models/__init__.py`
- `addons/marketing_card/models/card_campaign.py`
- `addons/marketing_card/models/card_campaign_tag.py`
- `addons/marketing_card/models/card_card.py`
- `addons/marketing_card/models/card_template.py`
- `addons/marketing_card/models/ir_model.py`
- `addons/marketing_card/models/mailing_mailing.py`
- `addons/marketing_card/models/utm_source.py`
- `addons/marketing_card/security/ir.access.csv`
- `addons/marketing_card/security/marketing_card_groups.xml`
- `addons/marketing_card/static/card_backgrounds/Blur.png`
- `addons/marketing_card/static/card_backgrounds/Circles.png`
- `addons/marketing_card/static/card_backgrounds/Desert.png`
- `addons/marketing_card/static/card_backgrounds/Drawings.png`
- `addons/marketing_card/static/card_backgrounds/Geometric.png`
- `addons/marketing_card/static/card_backgrounds/Highlight.png`
- `addons/marketing_card/static/card_backgrounds/Image.jpg`
- `addons/marketing_card/static/card_backgrounds/Image.png`
- `addons/marketing_card/static/card_backgrounds/Lila.png`
- `addons/marketing_card/static/card_backgrounds/Lines.png`
- `addons/marketing_card/static/card_backgrounds/Organic.png`
- `addons/marketing_card/static/card_backgrounds/Waves.png`
- `addons/marketing_card/static/card_backgrounds/WorldMap.png`
- `addons/marketing_card/static/description/icon.png`
- `addons/marketing_card/static/description/icon.svg`
- `addons/marketing_card/static/src/interactions/linkedin_message_editor.js`
- `addons/marketing_card/static/src/scss/card_campaign.scss`
- `addons/marketing_card/static/src/scss/frontend/card_website.scss`
- `addons/marketing_card/static/src/scss/linkedin_share_composer.scss`
- `addons/marketing_card/tests/__init__.py`
- `addons/marketing_card/tests/common.py`
- `addons/marketing_card/tests/test_campaign.py`
- `addons/marketing_card/utils/linkedin_api.py`
- `addons/marketing_card/views/card_campaign_views.xml`
- `addons/marketing_card/views/card_card_templates.xml`
- `addons/marketing_card/views/card_card_views.xml`
- `addons/marketing_card/views/card_frontend_templates.xml`
- `addons/marketing_card/views/card_menus.xml`
- `addons/marketing_card/views/card_template_views.xml`
- `addons/marketing_card/views/mailing_mailing_views.xml`
- `addons/marketing_card/views/website_templates.xml`
- `addons/marketing_card/wizards/__init__.py`
- `addons/marketing_card/wizards/mail_compose_message.py`
