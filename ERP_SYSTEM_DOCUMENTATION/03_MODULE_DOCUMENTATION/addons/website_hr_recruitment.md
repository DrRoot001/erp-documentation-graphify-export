# Module: website_hr_recruitment

- **Module ID:** MOD-620
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_hr_recruitment`
- **Manifest:** `addons/website_hr_recruitment/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Manage your online hiring process

**Manifest description:**

This module allows to publish your available job positions on your website and keep track of application submissions easily.

**Scope evidence:** The module contains 114 files, including 15 Python, 11 XML, and 7 JavaScript/TypeScript files. The manifest declares dependencies: `hr_recruitment`, `website_mail`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 2
- XML/data/view/template files: 11
- Browser asset files: 7
- Security files: 2
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_hr_recruitment/security/ir.access.csv`, `addons/website_hr_recruitment/security/website_hr_recruitment_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 34 methods, 0 constraint handlers, 1 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/website_hr_recruitment/models/website_published_multi_mixin.py:8`, `addons/website_hr_recruitment/models/hr_department.py:6`, `addons/website_hr_recruitment/models/hr_recruitment_source.py:9`, `addons/website_hr_recruitment/models/hr_job.py:10`, `addons/website_hr_recruitment/models/website.py:7`, `addons/website_hr_recruitment/models/hr_applicant.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 5 route declarations.
- **Evidence:** `addons/website_hr_recruitment/controllers/main.py:22`, `addons/website_hr_recruitment/controllers/main.py:165`, `addons/website_hr_recruitment/controllers/main.py:179`, `addons/website_hr_recruitment/controllers/main.py:184`, `addons/website_hr_recruitment/controllers/main.py:192`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 11 XML files and 7 JavaScript/TypeScript files; static XML analysis found 44 record/template/menu identifiers.
- **Evidence:** `addons/website_hr_recruitment/security/website_hr_recruitment_security.xml:2`, `addons/website_hr_recruitment/data/website_snippet_filter_data.xml:4`, `addons/website_hr_recruitment/data/website_snippet_filter_data.xml:12`, `addons/website_hr_recruitment/data/config_data.xml:4`, `addons/website_hr_recruitment/data/config_data.xml:9`, `addons/website_hr_recruitment/data/config_data.xml:13`, `addons/website_hr_recruitment/data/config_data.xml:21`, `addons/website_hr_recruitment/data/hr_job_demo.xml:4`, `addons/website_hr_recruitment/data/hr_job_demo.xml:229`, `addons/website_hr_recruitment/data/hr_job_demo.xml:452`, `addons/website_hr_recruitment/data/hr_job_demo.xml:677`, `addons/website_hr_recruitment/data/hr_job_demo.xml:852`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/website_hr_recruitment/security/ir.access.csv`, `addons/website_hr_recruitment/security/website_hr_recruitment_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/website_hr_recruitment/tests/test_website_hr_recruitment.py`, `addons/website_hr_recruitment/tests/__init__.py`, `addons/website_hr_recruitment/tests/test_website_hr_recruitment_technical_page.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 11; representative identifiers: `hr_recruitment.group_hr_recruitment_user`, `dynamic_snippet_latest_job_positions_filter`, `dynamic_filter_latest_job_positions`, `action_open_website`, `base.open_menu`, `website_menu_jobs`, `hr_recruitment.model_hr_applicant`, `hr.job_marketing`, `hr.job_developer`, `hr.job_consultant`, `hr.job_cto`, `hr.job_trainee`, `hr.job_hrm`, `job_pages_tree_view`, `job_pages_kanban_view`, `action_job_pages_list`, `Jobs`, `hr_job_website_inherit`, `hr_job_form_inherit`, `view_hr_job_kanban_referal_extends`
- Menus: 1; representative evidence: `addons/website_hr_recruitment/views/website_pages_views.xml:59`
- Templates: 18; representative evidence: `addons/website_hr_recruitment/views/website_hr_recruitment_templates.xml:5`, `addons/website_hr_recruitment/views/website_hr_recruitment_templates.xml:46`, `addons/website_hr_recruitment/views/website_hr_recruitment_templates.xml:110`, `addons/website_hr_recruitment/views/website_hr_recruitment_templates.xml:183`, `addons/website_hr_recruitment/views/website_hr_recruitment_templates.xml:387`, `addons/website_hr_recruitment/views/website_hr_recruitment_templates.xml:463`, `addons/website_hr_recruitment/views/website_hr_recruitment_templates.xml:701`, `addons/website_hr_recruitment/views/website_hr_recruitment_templates.xml:741`, `addons/website_hr_recruitment/views/website_hr_recruitment_templates.xml:788`, `addons/website_hr_recruitment/views/website_hr_recruitment_templates.xml:874`, `addons/website_hr_recruitment/views/website_hr_recruitment_templates.xml:901`, `addons/website_hr_recruitment/views/website_hr_recruitment_templates.xml:928`
- View/action field declarations: 23; representative evidence: `addons/website_hr_recruitment/views/website_pages_views.xml:6`, `addons/website_hr_recruitment/views/website_pages_views.xml:10`, `addons/website_hr_recruitment/views/website_pages_views.xml:34`, `addons/website_hr_recruitment/views/website_pages_views.xml:38`, `addons/website_hr_recruitment/views/website_pages_views.xml:49`, `addons/website_hr_recruitment/views/website_pages_views.xml:51`, `addons/website_hr_recruitment/views/hr_job_views.xml:5`, `addons/website_hr_recruitment/views/hr_job_views.xml:7`, `addons/website_hr_recruitment/views/hr_job_views.xml:37`, `addons/website_hr_recruitment/views/hr_job_views.xml:39`, `addons/website_hr_recruitment/views/hr_job_views.xml:51`, `addons/website_hr_recruitment/views/hr_job_views.xml:54`
- Browser assets: 7; representative files: `addons/website_hr_recruitment/static/src/website_builder/website_hr_recruitment_floating_snippets_plugin.js`, `addons/website_hr_recruitment/static/src/js/website_hr_recruitment_editor.edit.js`, `addons/website_hr_recruitment/static/src/js/website_hr_recruitment_editor.js`, `addons/website_hr_recruitment/static/src/interactions/hr_recruitment_form.js`, `addons/website_hr_recruitment/static/src/js/widgets/copy_link_menuitem.js`, `addons/website_hr_recruitment/static/src/js/systray_items/new_content.js`, `addons/website_hr_recruitment/static/tests/tours/website_hr_recruitment.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_hr_recruitment/__manifest__.py`
- **HTTP entry points:** `addons/website_hr_recruitment/controllers/main.py:22`, `addons/website_hr_recruitment/controllers/main.py:165`, `addons/website_hr_recruitment/controllers/main.py:179`, `addons/website_hr_recruitment/controllers/main.py:184`, `addons/website_hr_recruitment/controllers/main.py:192`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `website.published.multi.mixin` (addons/website_hr_recruitment/models/website_published_multi_mixin.py:8); inherits `hr.department` (addons/website_hr_recruitment/models/hr_department.py:6); inherits `hr.recruitment.source` (addons/website_hr_recruitment/models/hr_recruitment_source.py:9); `hr.job` (addons/website_hr_recruitment/models/hr_job.py:10); inherits `website` (addons/website_hr_recruitment/models/website.py:7); inherits `hr.applicant` (addons/website_hr_recruitment/models/hr_applicant.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 5
- Route evidence: `addons/website_hr_recruitment/controllers/main.py:22`, `addons/website_hr_recruitment/controllers/main.py:165`, `addons/website_hr_recruitment/controllers/main.py:179`, `addons/website_hr_recruitment/controllers/main.py:184`, `addons/website_hr_recruitment/controllers/main.py:192`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr_recruitment`, `website_mail`
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

- `addons/website_hr_recruitment/README.md`
- `addons/website_hr_recruitment/__init__.py`
- `addons/website_hr_recruitment/__manifest__.py`
- `addons/website_hr_recruitment/controllers/__init__.py`
- `addons/website_hr_recruitment/controllers/main.py`
- `addons/website_hr_recruitment/data/config_data.xml`
- `addons/website_hr_recruitment/data/hr_job_demo.xml`
- `addons/website_hr_recruitment/data/website_snippet_filter_data.xml`
- `addons/website_hr_recruitment/i18n/af.po`
- `addons/website_hr_recruitment/i18n/ar.po`
- `addons/website_hr_recruitment/i18n/az.po`
- `addons/website_hr_recruitment/i18n/bg.po`
- `addons/website_hr_recruitment/i18n/bs.po`
- `addons/website_hr_recruitment/i18n/ca.po`
- `addons/website_hr_recruitment/i18n/cs.po`
- `addons/website_hr_recruitment/i18n/da.po`
- `addons/website_hr_recruitment/i18n/de.po`
- `addons/website_hr_recruitment/i18n/el.po`
- `addons/website_hr_recruitment/i18n/es.po`
- `addons/website_hr_recruitment/i18n/es_419.po`
- `addons/website_hr_recruitment/i18n/et.po`
- `addons/website_hr_recruitment/i18n/fa.po`
- `addons/website_hr_recruitment/i18n/fi.po`
- `addons/website_hr_recruitment/i18n/fr.po`
- `addons/website_hr_recruitment/i18n/gu.po`
- `addons/website_hr_recruitment/i18n/he.po`
- `addons/website_hr_recruitment/i18n/hi.po`
- `addons/website_hr_recruitment/i18n/hr.po`
- `addons/website_hr_recruitment/i18n/hu.po`
- `addons/website_hr_recruitment/i18n/id.po`
- `addons/website_hr_recruitment/i18n/is.po`
- `addons/website_hr_recruitment/i18n/it.po`
- `addons/website_hr_recruitment/i18n/ja.po`
- `addons/website_hr_recruitment/i18n/kab.po`
- `addons/website_hr_recruitment/i18n/km.po`
- `addons/website_hr_recruitment/i18n/ko.po`
- `addons/website_hr_recruitment/i18n/ku.po`
- `addons/website_hr_recruitment/i18n/lo.po`
- `addons/website_hr_recruitment/i18n/lt.po`
- `addons/website_hr_recruitment/i18n/lv.po`
- `addons/website_hr_recruitment/i18n/mk.po`
- `addons/website_hr_recruitment/i18n/mn.po`
- `addons/website_hr_recruitment/i18n/my.po`
- `addons/website_hr_recruitment/i18n/nb.po`
- `addons/website_hr_recruitment/i18n/nl.po`
- `addons/website_hr_recruitment/i18n/pl.po`
- `addons/website_hr_recruitment/i18n/pt.po`
- `addons/website_hr_recruitment/i18n/pt_BR.po`
- `addons/website_hr_recruitment/i18n/ro.po`
- `addons/website_hr_recruitment/i18n/ru.po`
- `addons/website_hr_recruitment/i18n/sk.po`
- `addons/website_hr_recruitment/i18n/sl.po`
- `addons/website_hr_recruitment/i18n/sr@latin.po`
- `addons/website_hr_recruitment/i18n/sv.po`
- `addons/website_hr_recruitment/i18n/th.po`
- `addons/website_hr_recruitment/i18n/tr.po`
- `addons/website_hr_recruitment/i18n/uk.po`
- `addons/website_hr_recruitment/i18n/uz.po`
- `addons/website_hr_recruitment/i18n/vi.po`
- `addons/website_hr_recruitment/i18n/website_hr_recruitment.pot`
- `addons/website_hr_recruitment/i18n/zh_CN.po`
- `addons/website_hr_recruitment/i18n/zh_TW.po`
- `addons/website_hr_recruitment/migrations/17.0.1.1/pre-migrate.py`
- `addons/website_hr_recruitment/models/__init__.py`
- `addons/website_hr_recruitment/models/hr_applicant.py`
- `addons/website_hr_recruitment/models/hr_department.py`
- `addons/website_hr_recruitment/models/hr_job.py`
- `addons/website_hr_recruitment/models/hr_recruitment_source.py`
- `addons/website_hr_recruitment/models/website.py`
- `addons/website_hr_recruitment/models/website_published_multi_mixin.py`
- `addons/website_hr_recruitment/security/ir.access.csv`
- `addons/website_hr_recruitment/security/website_hr_recruitment_security.xml`
- `addons/website_hr_recruitment/static/description/icon.png`
- `addons/website_hr_recruitment/static/description/icon.svg`
- `addons/website_hr_recruitment/static/description/icon_hi.png`
- `addons/website_hr_recruitment/static/src/img/1010054_10151543538268963_186969588_n.jpg`
- `addons/website_hr_recruitment/static/src/img/1017407_10151536656083963_857938319_n.jpg`
- `addons/website_hr_recruitment/static/src/img/1044326_10151536655788963_587131144_n.jpg`
- `addons/website_hr_recruitment/static/src/img/882207_10151545507603963_1381082528_o.jpg`
- `addons/website_hr_recruitment/static/src/img/job_congratulations.svg`
- `addons/website_hr_recruitment/static/src/img/job_image_1.jpg`
- `addons/website_hr_recruitment/static/src/img/job_image_10.jpg`
- `addons/website_hr_recruitment/static/src/img/job_image_11.jpg`
- `addons/website_hr_recruitment/static/src/img/job_image_12.jpg`
- `addons/website_hr_recruitment/static/src/img/job_image_13.jpg`
- `addons/website_hr_recruitment/static/src/img/job_image_2.jpg`
- `addons/website_hr_recruitment/static/src/img/job_image_3.jpg`
- `addons/website_hr_recruitment/static/src/img/job_image_4.jpg`
- `addons/website_hr_recruitment/static/src/img/job_image_5.jpg`
- `addons/website_hr_recruitment/static/src/img/job_image_6.jpg`
- `addons/website_hr_recruitment/static/src/img/job_image_7.jpg`
- `addons/website_hr_recruitment/static/src/img/job_image_8.jpg`
- `addons/website_hr_recruitment/static/src/img/job_image_9.jpg`
- `addons/website_hr_recruitment/static/src/img/job_not_found.svg`
- `addons/website_hr_recruitment/static/src/img/job_product.svg`
- `addons/website_hr_recruitment/static/src/img/ui/s_hr_rating_thumb.jpg`
- `addons/website_hr_recruitment/static/src/interactions/hr_recruitment_form.js`
- `addons/website_hr_recruitment/static/src/js/systray_items/new_content.js`
- `addons/website_hr_recruitment/static/src/js/website_hr_recruitment_editor.edit.js`
- `addons/website_hr_recruitment/static/src/js/website_hr_recruitment_editor.js`
- `addons/website_hr_recruitment/static/src/js/widgets/copy_link_menuitem.js`
- `addons/website_hr_recruitment/static/src/js/widgets/copy_link_menuitem.xml`
- `addons/website_hr_recruitment/static/src/scss/website_hr_recruitment.scss`
- `addons/website_hr_recruitment/static/src/website_builder/website_hr_recruitment_floating_snippets_plugin.js`
- `addons/website_hr_recruitment/static/src/website_builder/website_hr_recruitment_option.xml`
- `addons/website_hr_recruitment/static/tests/tours/website_hr_recruitment.js`
- `addons/website_hr_recruitment/tests/__init__.py`
- `addons/website_hr_recruitment/tests/test_website_hr_recruitment.py`
- `addons/website_hr_recruitment/tests/test_website_hr_recruitment_technical_page.py`
- `addons/website_hr_recruitment/views/hr_job_views.xml`
- `addons/website_hr_recruitment/views/hr_recruitment_views.xml`
- `addons/website_hr_recruitment/views/website_hr_recruitment_snippet_templates.xml`
- `addons/website_hr_recruitment/views/website_hr_recruitment_templates.xml`
- `addons/website_hr_recruitment/views/website_pages_views.xml`
