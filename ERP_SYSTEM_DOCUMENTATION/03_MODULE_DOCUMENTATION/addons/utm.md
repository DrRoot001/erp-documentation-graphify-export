# Module: utm

- **Module ID:** MOD-591
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/utm`
- **Manifest:** `addons/utm/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Enable management of UTM trackers: campaign, medium, source.

**Scope evidence:** The module contains 98 files, including 16 Python, 12 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `web`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 0
- XML/data/view/template files: 12
- Browser asset files: 1
- Security files: 1
- Test files: 6
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/utm/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 35 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/utm/models/utm_mixin.py:13`, `addons/utm/models/utm_tag.py:9`, `addons/utm/models/utm_source.py:7`, `addons/utm/models/ir_http.py:7`, `addons/utm/models/utm_campaign.py:7`, `addons/utm/models/utm_stage.py:8`, `addons/utm/models/utm_medium.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 12 XML files and 1 JavaScript/TypeScript files; static XML analysis found 51 record/template/menu identifiers.
- **Evidence:** `addons/utm/data/utm_campaign_demo.xml:4`, `addons/utm/data/utm_campaign_demo.xml:9`, `addons/utm/data/utm_stage_data.xml:5`, `addons/utm/data/utm_stage_demo.xml:4`, `addons/utm/data/utm_stage_demo.xml:8`, `addons/utm/data/utm_stage_demo.xml:12`, `addons/utm/data/utm_tag_data.xml:4`, `addons/utm/data/utm_source_data.xml:3`, `addons/utm/data/utm_source_data.xml:6`, `addons/utm/data/utm_source_data.xml:9`, `addons/utm/data/utm_source_data.xml:12`, `addons/utm/data/utm_source_data.xml:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/utm/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 6 test files are present.
- **Evidence:** `addons/utm/tests/test_utm.py`, `addons/utm/tests/test_routes.py`, `addons/utm/tests/common.py`, `addons/utm/tests/test_utm_security.py`, `addons/utm/tests/__init__.py`, `addons/utm/tests/test_utm_consistency.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 12; representative identifiers: `utm_campaign_black_friday`, `utm_campaign_christmas_special`, `default_utm_stage`, `campaign_stage_1`, `campaign_stage_2`, `campaign_stage_3`, `utm_tag_1`, `utm_source_google`, `utm_source_mailing`, `utm_source_newsletter`, `utm_source_monster`, `utm_source_glassdoor`, `utm_source_craigslist`, `utm_source_survey`, `utm_source_referral`, `utm_source_livechat`, `utm_source_facebook`, `utm_source_twitter`, `utm_source_linkedin`, `utm_source_instagram`
- Menus: 5; representative evidence: `addons/utm/views/utm_menus.xml:3`, `addons/utm/views/utm_menus.xml:9`, `addons/utm/views/utm_menus.xml:15`, `addons/utm/views/utm_menus.xml:20`, `addons/utm/views/utm_menus.xml:25`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 37; representative evidence: `addons/utm/views/utm_campaign_views.xml:5`, `addons/utm/views/utm_campaign_views.xml:6`, `addons/utm/views/utm_campaign_views.xml:30`, `addons/utm/views/utm_campaign_views.xml:31`, `addons/utm/views/utm_campaign_views.xml:56`, `addons/utm/views/utm_campaign_views.xml:57`, `addons/utm/views/utm_campaign_views.xml:71`, `addons/utm/views/utm_campaign_views.xml:73`, `addons/utm/views/utm_campaign_views.xml:87`, `addons/utm/views/utm_campaign_views.xml:88`, `addons/utm/views/utm_campaign_views.xml:122`, `addons/utm/views/utm_campaign_views.xml:123`
- Browser assets: 1; representative files: `addons/utm/static/src/js/utm_campaign_kanban_examples.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/utm/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: `utm.mixin` (addons/utm/models/utm_mixin.py:13); `utm.tag` (addons/utm/models/utm_tag.py:9); `utm.source` (addons/utm/models/utm_source.py:7); inherits `ir.http` (addons/utm/models/ir_http.py:7); `utm.campaign` (addons/utm/models/utm_campaign.py:7); `utm.stage` (addons/utm/models/utm_stage.py:8); `utm.medium` (addons/utm/models/utm_medium.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `web`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/utm/__init__.py`
- `addons/utm/__manifest__.py`
- `addons/utm/data/utm_campaign_demo.xml`
- `addons/utm/data/utm_medium_data.xml`
- `addons/utm/data/utm_source_data.xml`
- `addons/utm/data/utm_stage_data.xml`
- `addons/utm/data/utm_stage_demo.xml`
- `addons/utm/data/utm_tag_data.xml`
- `addons/utm/i18n/af.po`
- `addons/utm/i18n/ar.po`
- `addons/utm/i18n/az.po`
- `addons/utm/i18n/bg.po`
- `addons/utm/i18n/bs.po`
- `addons/utm/i18n/ca.po`
- `addons/utm/i18n/cs.po`
- `addons/utm/i18n/da.po`
- `addons/utm/i18n/de.po`
- `addons/utm/i18n/el.po`
- `addons/utm/i18n/es.po`
- `addons/utm/i18n/es_419.po`
- `addons/utm/i18n/es_CL.po`
- `addons/utm/i18n/et.po`
- `addons/utm/i18n/eu.po`
- `addons/utm/i18n/fa.po`
- `addons/utm/i18n/fi.po`
- `addons/utm/i18n/fo.po`
- `addons/utm/i18n/fr.po`
- `addons/utm/i18n/fr_BE.po`
- `addons/utm/i18n/fr_CA.po`
- `addons/utm/i18n/gl.po`
- `addons/utm/i18n/gu.po`
- `addons/utm/i18n/he.po`
- `addons/utm/i18n/hi.po`
- `addons/utm/i18n/hr.po`
- `addons/utm/i18n/hu.po`
- `addons/utm/i18n/id.po`
- `addons/utm/i18n/is.po`
- `addons/utm/i18n/it.po`
- `addons/utm/i18n/ja.po`
- `addons/utm/i18n/ka.po`
- `addons/utm/i18n/kab.po`
- `addons/utm/i18n/km.po`
- `addons/utm/i18n/ko.po`
- `addons/utm/i18n/ku.po`
- `addons/utm/i18n/lo.po`
- `addons/utm/i18n/lt.po`
- `addons/utm/i18n/lv.po`
- `addons/utm/i18n/mk.po`
- `addons/utm/i18n/ml_IN.po`
- `addons/utm/i18n/mn.po`
- `addons/utm/i18n/my.po`
- `addons/utm/i18n/nb.po`
- `addons/utm/i18n/nl.po`
- `addons/utm/i18n/pl.po`
- `addons/utm/i18n/pt.po`
- `addons/utm/i18n/pt_BR.po`
- `addons/utm/i18n/ro.po`
- `addons/utm/i18n/ru.po`
- `addons/utm/i18n/sk.po`
- `addons/utm/i18n/sl.po`
- `addons/utm/i18n/sq.po`
- `addons/utm/i18n/sr@latin.po`
- `addons/utm/i18n/sv.po`
- `addons/utm/i18n/ta.po`
- `addons/utm/i18n/th.po`
- `addons/utm/i18n/tr.po`
- `addons/utm/i18n/uk.po`
- `addons/utm/i18n/utm.pot`
- `addons/utm/i18n/uz.po`
- `addons/utm/i18n/vi.po`
- `addons/utm/i18n/zh_CN.po`
- `addons/utm/i18n/zh_TW.po`
- `addons/utm/models/__init__.py`
- `addons/utm/models/ir_http.py`
- `addons/utm/models/utm_campaign.py`
- `addons/utm/models/utm_medium.py`
- `addons/utm/models/utm_mixin.py`
- `addons/utm/models/utm_source.py`
- `addons/utm/models/utm_stage.py`
- `addons/utm/models/utm_tag.py`
- `addons/utm/security/ir.access.csv`
- `addons/utm/static/description/icon.png`
- `addons/utm/static/description/icon.svg`
- `addons/utm/static/description/icon_hi.png`
- `addons/utm/static/src/js/utm_campaign_kanban_examples.js`
- `addons/utm/static/src/scss/utm_views.scss`
- `addons/utm/tests/__init__.py`
- `addons/utm/tests/common.py`
- `addons/utm/tests/test_routes.py`
- `addons/utm/tests/test_utm.py`
- `addons/utm/tests/test_utm_consistency.py`
- `addons/utm/tests/test_utm_security.py`
- `addons/utm/views/utm_campaign_views.xml`
- `addons/utm/views/utm_medium_views.xml`
- `addons/utm/views/utm_menus.xml`
- `addons/utm/views/utm_source_views.xml`
- `addons/utm/views/utm_stage_views.xml`
- `addons/utm/views/utm_tag_views.xml`
