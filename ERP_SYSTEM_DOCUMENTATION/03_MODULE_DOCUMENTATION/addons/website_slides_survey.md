# Module: website_slides_survey

- **Module ID:** MOD-645
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_slides_survey`
- **Manifest:** `addons/website_slides_survey/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/eLearning`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Add certification capabilities to your courses

**Manifest description:**

This module lets you use the full power of certifications within your courses.

**Scope evidence:** The module contains 93 files, including 15 Python, 21 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `website_slides`, `survey`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 4
- XML/data/view/template files: 21
- Browser asset files: 3
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_slides_survey/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 41 methods, 0 constraint handlers, 0 onchange handlers, and 7 dependency declarations.
- **Evidence:** `addons/website_slides_survey/models/slide_channel.py:9`, `addons/website_slides_survey/models/slide_channel.py:16`, `addons/website_slides_survey/models/survey_user.py:6`, `addons/website_slides_survey/models/survey_survey.py:10`, `addons/website_slides_survey/models/slide_slide.py:7`, `addons/website_slides_survey/models/slide_slide.py:45`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 4 controller files and 3 route declarations.
- **Evidence:** `addons/website_slides_survey/controllers/slides.py:18`, `addons/website_slides_survey/controllers/slides.py:31`, `addons/website_slides_survey/controllers/slides.py:43`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 21 XML files and 3 JavaScript/TypeScript files; static XML analysis found 55 record/template/menu identifiers.
- **Evidence:** `addons/website_slides_survey/data/slide_slide_demo.xml:6`, `addons/website_slides_survey/data/slide_slide_demo.xml:22`, `addons/website_slides_survey/data/mail_template_data.xml:4`, `addons/website_slides_survey/data/gamification_data.xml:3`, `addons/website_slides_survey/data/gamification_data.xml:6`, `addons/website_slides_survey/data/survey_demo.xml:5`, `addons/website_slides_survey/data/survey_demo.xml:21`, `addons/website_slides_survey/data/survey_demo.xml:30`, `addons/website_slides_survey/data/survey_demo.xml:37`, `addons/website_slides_survey/data/survey_demo.xml:42`, `addons/website_slides_survey/data/survey_demo.xml:49`, `addons/website_slides_survey/data/survey_demo.xml:54`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_slides_survey/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/website_slides_survey/tests/test_course_certification_stats.py`, `addons/website_slides_survey/tests/test_course_certification_unlink.py`, `addons/website_slides_survey/tests/test_course_certification_failure.py`, `addons/website_slides_survey/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 21; representative identifiers: `slide_slide_demo_5_4`, `slide_slide_demo_6_0`, `mail_template_user_input_certification_failed`, `website_slides.badge_data_certification`, `website_slides.badge_data_certification_goal`, `furniture_certification`, `furniture_certification_page_1`, `furniture_certification_page_1_question_1`, `furniture_certification_page_1_question_1_choice_1`, `furniture_certification_page_1_question_1_choice_2`, `furniture_certification_page_1_question_1_choice_3`, `furniture_certification_page_1_question_1_choice_4`, `furniture_certification_page_1_question_2`, `furniture_certification_page_1_question_2_choice_1`, `furniture_certification_page_1_question_2_choice_2`, `furniture_certification_page_1_question_2_choice_3`, `furniture_certification_page_1_question_2_choice_4`, `furniture_certification_page_1_question_2_choice_5`, `furniture_certification_page_1_question_3`, `furniture_certification_answer_1`
- Menus: 1; representative evidence: `addons/website_slides_survey/views/website_slides_menu_views.xml:3`
- Templates: 16; representative evidence: `addons/website_slides_survey/views/website_slides_templates_lesson.xml:4`, `addons/website_slides_survey/views/website_slides_templates_lesson_fullscreen.xml:4`, `addons/website_slides_survey/views/website_slides_templates_course.xml:4`, `addons/website_slides_survey/views/website_slides_templates_course.xml:21`, `addons/website_slides_survey/views/website_slides_templates_course.xml:33`, `addons/website_slides_survey/views/website_profile.xml:3`, `addons/website_slides_survey/views/website_profile.xml:66`, `addons/website_slides_survey/views/website_profile.xml:113`, `addons/website_slides_survey/views/website_profile.xml:119`, `addons/website_slides_survey/views/website_profile.xml:127`, `addons/website_slides_survey/views/website_slides_templates_homepage.xml:4`, `addons/website_slides_survey/views/website_slides_templates_homepage.xml:16`
- View/action field declarations: 31; representative evidence: `addons/website_slides_survey/views/slide_slide_views.xml:5`, `addons/website_slides_survey/views/slide_slide_views.xml:7`, `addons/website_slides_survey/views/slide_slide_views.xml:22`, `addons/website_slides_survey/views/slide_slide_views.xml:23`, `addons/website_slides_survey/views/slide_slide_partner_views.xml:6`, `addons/website_slides_survey/views/slide_slide_partner_views.xml:8`, `addons/website_slides_survey/views/slide_slide_partner_views.xml:17`, `addons/website_slides_survey/views/slide_slide_partner_views.xml:19`, `addons/website_slides_survey/views/slide_slide_partner_views.xml:28`, `addons/website_slides_survey/views/slide_slide_partner_views.xml:30`, `addons/website_slides_survey/views/res_config_settings_views.xml:5`, `addons/website_slides_survey/views/res_config_settings_views.xml:8`
- Browser assets: 3; representative files: `addons/website_slides_survey/static/src/interactions/slides_course_fullscreen.js`, `addons/website_slides_survey/static/src/js/public/components/slide_upload_dialog/slide_upload_dialog.js`, `addons/website_slides_survey/static/src/js/public/components/slide_upload_dialog/slide_upload_category.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_slides_survey/__manifest__.py`
- **HTTP entry points:** `addons/website_slides_survey/controllers/slides.py:18`, `addons/website_slides_survey/controllers/slides.py:31`, `addons/website_slides_survey/controllers/slides.py:43`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `slide.channel.partner` (addons/website_slides_survey/models/slide_channel.py:9); inherits `slide.channel` (addons/website_slides_survey/models/slide_channel.py:16); inherits `survey.user_input` (addons/website_slides_survey/models/survey_user.py:6); inherits `survey.survey` (addons/website_slides_survey/models/survey_survey.py:10); inherits `slide.slide.partner` (addons/website_slides_survey/models/slide_slide.py:7); inherits `slide.slide` (addons/website_slides_survey/models/slide_slide.py:45)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 4
- Route declarations: 3
- Route evidence: `addons/website_slides_survey/controllers/slides.py:18`, `addons/website_slides_survey/controllers/slides.py:31`, `addons/website_slides_survey/controllers/slides.py:43`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_slides`, `survey`
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

- `addons/website_slides_survey/__init__.py`
- `addons/website_slides_survey/__manifest__.py`
- `addons/website_slides_survey/controllers/__init__.py`
- `addons/website_slides_survey/controllers/slides.py`
- `addons/website_slides_survey/controllers/survey.py`
- `addons/website_slides_survey/controllers/website_profile.py`
- `addons/website_slides_survey/data/gamification_data.xml`
- `addons/website_slides_survey/data/mail_template_data.xml`
- `addons/website_slides_survey/data/slide_slide_demo.xml`
- `addons/website_slides_survey/data/survey.user_input.line.csv`
- `addons/website_slides_survey/data/survey_demo.xml`
- `addons/website_slides_survey/i18n/ar.po`
- `addons/website_slides_survey/i18n/az.po`
- `addons/website_slides_survey/i18n/bg.po`
- `addons/website_slides_survey/i18n/bs.po`
- `addons/website_slides_survey/i18n/ca.po`
- `addons/website_slides_survey/i18n/cs.po`
- `addons/website_slides_survey/i18n/da.po`
- `addons/website_slides_survey/i18n/de.po`
- `addons/website_slides_survey/i18n/el.po`
- `addons/website_slides_survey/i18n/es.po`
- `addons/website_slides_survey/i18n/es_419.po`
- `addons/website_slides_survey/i18n/et.po`
- `addons/website_slides_survey/i18n/fa.po`
- `addons/website_slides_survey/i18n/fi.po`
- `addons/website_slides_survey/i18n/fr.po`
- `addons/website_slides_survey/i18n/he.po`
- `addons/website_slides_survey/i18n/hi.po`
- `addons/website_slides_survey/i18n/hr.po`
- `addons/website_slides_survey/i18n/hu.po`
- `addons/website_slides_survey/i18n/id.po`
- `addons/website_slides_survey/i18n/it.po`
- `addons/website_slides_survey/i18n/ja.po`
- `addons/website_slides_survey/i18n/kab.po`
- `addons/website_slides_survey/i18n/ko.po`
- `addons/website_slides_survey/i18n/ku.po`
- `addons/website_slides_survey/i18n/lo.po`
- `addons/website_slides_survey/i18n/lt.po`
- `addons/website_slides_survey/i18n/lv.po`
- `addons/website_slides_survey/i18n/mn.po`
- `addons/website_slides_survey/i18n/my.po`
- `addons/website_slides_survey/i18n/nb.po`
- `addons/website_slides_survey/i18n/nl.po`
- `addons/website_slides_survey/i18n/pl.po`
- `addons/website_slides_survey/i18n/pt.po`
- `addons/website_slides_survey/i18n/pt_BR.po`
- `addons/website_slides_survey/i18n/ro.po`
- `addons/website_slides_survey/i18n/ru.po`
- `addons/website_slides_survey/i18n/sk.po`
- `addons/website_slides_survey/i18n/sl.po`
- `addons/website_slides_survey/i18n/sr@latin.po`
- `addons/website_slides_survey/i18n/sv.po`
- `addons/website_slides_survey/i18n/th.po`
- `addons/website_slides_survey/i18n/tr.po`
- `addons/website_slides_survey/i18n/uk.po`
- `addons/website_slides_survey/i18n/uz.po`
- `addons/website_slides_survey/i18n/vi.po`
- `addons/website_slides_survey/i18n/website_slides_survey.pot`
- `addons/website_slides_survey/i18n/zh_CN.po`
- `addons/website_slides_survey/i18n/zh_TW.po`
- `addons/website_slides_survey/models/__init__.py`
- `addons/website_slides_survey/models/slide_channel.py`
- `addons/website_slides_survey/models/slide_slide.py`
- `addons/website_slides_survey/models/survey_survey.py`
- `addons/website_slides_survey/models/survey_user.py`
- `addons/website_slides_survey/security/ir.access.csv`
- `addons/website_slides_survey/static/src/img/certification.svg`
- `addons/website_slides_survey/static/src/interactions/slides_course_fullscreen.js`
- `addons/website_slides_survey/static/src/js/public/components/slide_upload_dialog/slide_upload_category.js`
- `addons/website_slides_survey/static/src/js/public/components/slide_upload_dialog/slide_upload_category.xml`
- `addons/website_slides_survey/static/src/js/public/components/slide_upload_dialog/slide_upload_dialog.js`
- `addons/website_slides_survey/static/src/js/public/components/slide_upload_dialog/slide_upload_dialog.xml`
- `addons/website_slides_survey/static/src/scss/website_slides_survey.scss`
- `addons/website_slides_survey/static/src/scss/website_slides_survey_result.scss`
- `addons/website_slides_survey/static/src/xml/website_slides_fullscreen.xml`
- `addons/website_slides_survey/tests/__init__.py`
- `addons/website_slides_survey/tests/test_course_certification_failure.py`
- `addons/website_slides_survey/tests/test_course_certification_stats.py`
- `addons/website_slides_survey/tests/test_course_certification_unlink.py`
- `addons/website_slides_survey/views/res_config_settings_views.xml`
- `addons/website_slides_survey/views/slide_channel_partner_views.xml`
- `addons/website_slides_survey/views/slide_channel_views.xml`
- `addons/website_slides_survey/views/slide_slide_partner_views.xml`
- `addons/website_slides_survey/views/slide_slide_views.xml`
- `addons/website_slides_survey/views/survey_survey_views.xml`
- `addons/website_slides_survey/views/survey_templates.xml`
- `addons/website_slides_survey/views/website_profile.xml`
- `addons/website_slides_survey/views/website_slides_menu_views.xml`
- `addons/website_slides_survey/views/website_slides_templates_course.xml`
- `addons/website_slides_survey/views/website_slides_templates_homepage.xml`
- `addons/website_slides_survey/views/website_slides_templates_lesson.xml`
- `addons/website_slides_survey/views/website_slides_templates_lesson_fullscreen.xml`
- `addons/website_slides_survey/views/website_slides_templates_utils.xml`
