# Module: survey

- **Module ID:** MOD-567
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/survey`
- **Manifest:** `addons/survey/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Marketing/Surveys`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Send your surveys or share them live.

**Manifest description:**

Create beautiful surveys and visualize answers
==============================================

It depends on the answers or reviews of some questions by different users. A
survey may have multiple pages. Each page may contain multiple questions and
each question may have multiple answers. Different users may give different
answers of question and according to that survey is done. Partners are also
sent mails with personal token for the invitation of the survey.

**Scope evidence:** The module contains 206 files, including 37 Python, 39 XML, and 46 JavaScript/TypeScript files. The manifest declares dependencies: `auth_signup`, `http_routing`, `mail`, `web_tour`, `gamification`, `digest`.

## 2. Module structure

- Model/business logic files: 13
- Controller/API files: 3
- XML/data/view/template files: 39
- Browser asset files: 46
- Security files: 2
- Test files: 18
- Scheduled/automation evidence files: 2
- Reporting evidence files: 3

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/survey/security/ir.access.csv`, `addons/survey/security/survey_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 13 model declarations, 353 methods, 6 constraint handlers, 6 onchange handlers, and 51 dependency declarations.
- **Evidence:** `addons/survey/models/res_partner.py:7`, `addons/survey/models/res_lang.py:7`, `addons/survey/models/survey_user_input.py:17`, `addons/survey/models/survey_user_input.py:721`, `addons/survey/models/digest.py:6`, `addons/survey/models/ir_http.py:21`, `addons/survey/models/survey_survey.py:19`, `addons/survey/models/badge.py:7`, `addons/survey/models/survey_question.py:15`, `addons/survey/models/survey_question.py:856`, `addons/survey/models/challenge.py:7`, `addons/survey/wizard/survey_invite.py:17`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 23 route declarations.
- **Evidence:** `addons/survey/controllers/survey_session_manage.py:41`, `addons/survey/controllers/survey_session_manage.py:70`, `addons/survey/controllers/survey_session_manage.py:77`, `addons/survey/controllers/survey_session_manage.py:129`, `addons/survey/controllers/survey_session_manage.py:150`, `addons/survey/controllers/survey_session_manage.py:172`, `addons/survey/controllers/survey_session_manage.py:179`, `addons/survey/controllers/survey_session_manage.py:191`, `addons/survey/controllers/main.py:160`, `addons/survey/controllers/main.py:171`, `addons/survey/controllers/main.py:213`, `addons/survey/controllers/main.py:434`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 39 XML files and 46 JavaScript/TypeScript files; static XML analysis found 382 record/template/menu identifiers.
- **Evidence:** `addons/survey/security/survey_security.xml:3`, `addons/survey/security/survey_security.xml:10`, `addons/survey/security/survey_security.xml:17`, `addons/survey/report/survey_reports.xml:5`, `addons/survey/report/survey_reports.xml:20`, `addons/survey/report/survey_templates.xml:4`, `addons/survey/report/survey_templates.xml:140`, `addons/survey/wizard/survey_invite_views.xml:4`, `addons/survey/data/ir_actions_server_data.xml:3`, `addons/survey/data/survey_demo_certification.xml:5`, `addons/survey/data/survey_demo_certification.xml:27`, `addons/survey/data/survey_demo_certification.xml:36`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/survey/security/ir.access.csv`, `addons/survey/security/survey_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/survey/models/survey_user_input.py`, `addons/survey/data/ir_actions_server_data.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 3 files contain report-action/template indicators.
- **Evidence:** `addons/survey/controllers/main.py`, `addons/survey/report/survey_reports.xml`, `addons/survey/tests/test_certification_flow.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 18 test files are present.
- **Evidence:** `addons/survey/tests/test_survey_results.py`, `addons/survey/tests/test_survey.py`, `addons/survey/tests/test_ir_http.py`, `addons/survey/tests/test_certification_badge.py`, `addons/survey/tests/test_survey_invite.py`, `addons/survey/tests/test_survey_ui_backend.py`, `addons/survey/tests/test_survey_randomize.py`, `addons/survey/tests/test_survey_ui_feedback.py`, `addons/survey/tests/test_survey_controller.py`, `addons/survey/tests/test_survey_flow_with_conditions.py`, `addons/survey/tests/test_survey_flow.py`, `addons/survey/tests/test_survey_ui_certification.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 39; representative identifiers: `res_groups_privilege_surveys`, `group_survey_user`, `group_survey_manager`, `paperformat_survey_certification`, `certification_report`, `certification_report_view_general`, `certification_report_view`, `survey_invite_view_form`, `action_survey_print`, `vendor_certification`, `vendor_certification_page_1`, `vendor_certification_page_1_question_1`, `vendor_certification_page_1_question_1_choice_1`, `vendor_certification_page_1_question_1_choice_2`, `vendor_certification_page_1_question_2`, `vendor_certification_page_1_question_2_choice_1`, `vendor_certification_page_1_question_2_choice_2`, `vendor_certification_page_1_question_2_choice_3`, `vendor_certification_page_1_question_2_choice_4`, `vendor_certification_page_1_question_2_choice_5`
- Menus: 7; representative evidence: `addons/survey/views/survey_menus.xml:5`, `addons/survey/views/survey_menus.xml:12`, `addons/survey/views/survey_user_views.xml:263`, `addons/survey/views/survey_question_views.xml:342`, `addons/survey/views/survey_question_views.xml:347`, `addons/survey/views/survey_question_views.xml:352`, `addons/survey/views/survey_survey_views.xml:435`
- Templates: 52; representative evidence: `addons/survey/report/survey_templates.xml:4`, `addons/survey/report/survey_templates.xml:140`, `addons/survey/views/survey_templates_management.xml:9`, `addons/survey/views/survey_templates_management.xml:26`, `addons/survey/views/survey_templates_management.xml:51`, `addons/survey/views/survey_templates_management.xml:67`, `addons/survey/views/survey_templates_management.xml:81`, `addons/survey/views/survey_templates_management.xml:102`, `addons/survey/views/survey_templates_management.xml:116`, `addons/survey/views/survey_templates_management.xml:137`, `addons/survey/views/survey_templates_management.xml:168`, `addons/survey/views/survey_templates_print.xml:5`
- View/action field declarations: 65; representative evidence: `addons/survey/report/survey_reports.xml:22`, `addons/survey/wizard/survey_invite_views.xml:6`, `addons/survey/wizard/survey_invite_views.xml:7`, `addons/survey/data/mail_message_subtype_data.xml:5`, `addons/survey/data/mail_message_subtype_data.xml:13`, `addons/survey/views/digest_views.xml:5`, `addons/survey/views/digest_views.xml:7`, `addons/survey/views/gamification_badge_views.xml:5`, `addons/survey/views/gamification_badge_views.xml:7`, `addons/survey/views/survey_user_views.xml:7`, `addons/survey/views/survey_user_views.xml:8`, `addons/survey/views/survey_user_views.xml:38`
- Browser assets: 46; representative files: `addons/survey/static/src/utils.js`, `addons/survey/static/src/js/survey_preload_image_mixin.js`, `addons/survey/static/src/question_page/question_page_one2many_field.js`, `addons/survey/static/src/question_page/question_page_list_renderer.js`, `addons/survey/static/src/question_page/description_page_field.js`, `addons/survey/static/src/interactions/survey_enter_tooltip.js`, `addons/survey/static/src/interactions/survey_session_chart.js`, `addons/survey/static/src/interactions/survey_result.js`, `addons/survey/static/src/interactions/survey_session_text_answers.js`, `addons/survey/static/src/interactions/survey_session_leaderboard.js`, `addons/survey/static/src/interactions/survey_print.js`, `addons/survey/static/src/interactions/utils.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/survey/__manifest__.py`
- **HTTP entry points:** `addons/survey/controllers/survey_session_manage.py:41`, `addons/survey/controllers/survey_session_manage.py:70`, `addons/survey/controllers/survey_session_manage.py:77`, `addons/survey/controllers/survey_session_manage.py:129`, `addons/survey/controllers/survey_session_manage.py:150`, `addons/survey/controllers/survey_session_manage.py:172`, `addons/survey/controllers/survey_session_manage.py:179`, `addons/survey/controllers/survey_session_manage.py:191`, `addons/survey/controllers/main.py:160`, `addons/survey/controllers/main.py:171`, `addons/survey/controllers/main.py:213`, `addons/survey/controllers/main.py:434`
- **Scheduled entry points:** `addons/survey/models/survey_user_input.py`, `addons/survey/data/ir_actions_server_data.xml`
- **Report entry points:** `addons/survey/controllers/main.py`, `addons/survey/report/survey_reports.xml`, `addons/survey/tests/test_certification_flow.py`

## 7. Database interactions

- Model declarations: 13
- Representative model evidence: inherits `res.partner` (addons/survey/models/res_partner.py:7); inherits `res.lang` (addons/survey/models/res_lang.py:7); `survey.user_input` (addons/survey/models/survey_user_input.py:17); `survey.user_input.line` (addons/survey/models/survey_user_input.py:721); inherits `digest.digest` (addons/survey/models/digest.py:6); inherits `ir.http` (addons/survey/models/ir_http.py:21); `survey.survey` (addons/survey/models/survey_survey.py:19); inherits `gamification.badge` (addons/survey/models/badge.py:7); `survey.question` (addons/survey/models/survey_question.py:15); `survey.question.answer` (addons/survey/models/survey_question.py:856); inherits `gamification.challenge` (addons/survey/models/challenge.py:7); `survey.invite` (addons/survey/wizard/survey_invite.py:17); inherits `survey.survey` (addons/survey/models/templates/survey_survey.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 23
- Route evidence: `addons/survey/controllers/survey_session_manage.py:41`, `addons/survey/controllers/survey_session_manage.py:70`, `addons/survey/controllers/survey_session_manage.py:77`, `addons/survey/controllers/survey_session_manage.py:129`, `addons/survey/controllers/survey_session_manage.py:150`, `addons/survey/controllers/survey_session_manage.py:172`, `addons/survey/controllers/survey_session_manage.py:179`, `addons/survey/controllers/survey_session_manage.py:191`, `addons/survey/controllers/main.py:160`, `addons/survey/controllers/main.py:171`, `addons/survey/controllers/main.py:213`, `addons/survey/controllers/main.py:434`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `auth_signup`, `http_routing`, `mail`, `web_tour`, `gamification`, `digest`
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

- `addons/survey/__init__.py`
- `addons/survey/__manifest__.py`
- `addons/survey/controllers/__init__.py`
- `addons/survey/controllers/main.py`
- `addons/survey/controllers/survey_session_manage.py`
- `addons/survey/data/digest_data.xml`
- `addons/survey/data/gamification_badge_demo.xml`
- `addons/survey/data/ir_actions_server_data.xml`
- `addons/survey/data/mail_message_subtype_data.xml`
- `addons/survey/data/mail_template_data.xml`
- `addons/survey/data/res_users_demo.xml`
- `addons/survey/data/survey_demo_certification.xml`
- `addons/survey/data/survey_demo_certification_user_input.xml`
- `addons/survey/data/survey_demo_certification_user_input_line.xml`
- `addons/survey/data/survey_demo_conditional.xml`
- `addons/survey/data/survey_demo_feedback.xml`
- `addons/survey/data/survey_demo_feedback_user_input.xml`
- `addons/survey/data/survey_demo_feedback_user_input_line.xml`
- `addons/survey/data/survey_tour.xml`
- `addons/survey/i18n/af.po`
- `addons/survey/i18n/ar.po`
- `addons/survey/i18n/az.po`
- `addons/survey/i18n/bg.po`
- `addons/survey/i18n/bs.po`
- `addons/survey/i18n/ca.po`
- `addons/survey/i18n/cs.po`
- `addons/survey/i18n/da.po`
- `addons/survey/i18n/de.po`
- `addons/survey/i18n/el.po`
- `addons/survey/i18n/es.po`
- `addons/survey/i18n/es_419.po`
- `addons/survey/i18n/es_CL.po`
- `addons/survey/i18n/et.po`
- `addons/survey/i18n/fa.po`
- `addons/survey/i18n/fi.po`
- `addons/survey/i18n/fr.po`
- `addons/survey/i18n/gl.po`
- `addons/survey/i18n/gu.po`
- `addons/survey/i18n/he.po`
- `addons/survey/i18n/hi.po`
- `addons/survey/i18n/hr.po`
- `addons/survey/i18n/hu.po`
- `addons/survey/i18n/id.po`
- `addons/survey/i18n/is.po`
- `addons/survey/i18n/it.po`
- `addons/survey/i18n/ja.po`
- `addons/survey/i18n/ka.po`
- `addons/survey/i18n/kab.po`
- `addons/survey/i18n/km.po`
- `addons/survey/i18n/ko.po`
- `addons/survey/i18n/ku.po`
- `addons/survey/i18n/lo.po`
- `addons/survey/i18n/lt.po`
- `addons/survey/i18n/lv.po`
- `addons/survey/i18n/mk.po`
- `addons/survey/i18n/mn.po`
- `addons/survey/i18n/my.po`
- `addons/survey/i18n/nb.po`
- `addons/survey/i18n/nl.po`
- `addons/survey/i18n/pl.po`
- `addons/survey/i18n/pt.po`
- `addons/survey/i18n/pt_BR.po`
- `addons/survey/i18n/ro.po`
- `addons/survey/i18n/ru.po`
- `addons/survey/i18n/sk.po`
- `addons/survey/i18n/sl.po`
- `addons/survey/i18n/sr@latin.po`
- `addons/survey/i18n/survey.pot`
- `addons/survey/i18n/sv.po`
- `addons/survey/i18n/th.po`
- `addons/survey/i18n/tr.po`
- `addons/survey/i18n/uk.po`
- `addons/survey/i18n/uz.po`
- `addons/survey/i18n/vi.po`
- `addons/survey/i18n/zh_CN.po`
- `addons/survey/i18n/zh_TW.po`
- `addons/survey/models/__init__.py`
- `addons/survey/models/badge.py`
- `addons/survey/models/challenge.py`
- `addons/survey/models/digest.py`
- `addons/survey/models/ir_http.py`
- `addons/survey/models/res_lang.py`
- `addons/survey/models/res_partner.py`
- `addons/survey/models/survey_question.py`
- `addons/survey/models/survey_survey.py`
- `addons/survey/models/survey_user_input.py`
- `addons/survey/models/templates/__init__.py`
- `addons/survey/models/templates/survey_survey.py`
- `addons/survey/report/survey_reports.xml`
- `addons/survey/report/survey_templates.xml`
- `addons/survey/security/ir.access.csv`
- `addons/survey/security/survey_security.xml`
- `addons/survey/static/description/icon.png`
- `addons/survey/static/description/icon.svg`
- `addons/survey/static/description/icon_hi.png`
- `addons/survey/static/src/img/burger_quiz_background.txt`
- `addons/survey/static/src/img/burger_quiz_background.webp`
- `addons/survey/static/src/img/burger_quiz_cubism_klein.jpg`
- `addons/survey/static/src/img/burger_quiz_don_quixote.jpg`
- `addons/survey/static/src/img/burger_quiz_guernica.jpg`
- `addons/survey/static/src/img/burger_quiz_self_portrait.jpg`
- `addons/survey/static/src/img/certification_classic-1_bg.svg`
- `addons/survey/static/src/img/certification_classic-2_bg.svg`
- `addons/survey/static/src/img/certification_minimal_number_bg.svg`
- `addons/survey/static/src/img/certification_modern_bg.svg`
- `addons/survey/static/src/img/classic-seal.png`
- `addons/survey/static/src/img/survey_background_2.webp`
- `addons/survey/static/src/img/survey_background_sample.svg`
- `addons/survey/static/src/img/survey_sample_assessment.png`
- `addons/survey/static/src/img/survey_sample_live_session.png`
- `addons/survey/static/src/img/survey_sample_survey.png`
- `addons/survey/static/src/img/watermark.png`
- `addons/survey/static/src/interactions/survey_breadcrumb_templates.xml`
- `addons/survey/static/src/interactions/survey_enter_tooltip.js`
- `addons/survey/static/src/interactions/survey_form.js`
- `addons/survey/static/src/interactions/survey_image_zoomer.js`
- `addons/survey/static/src/interactions/survey_image_zoomer_templates.xml`
- `addons/survey/static/src/interactions/survey_print.js`
- `addons/survey/static/src/interactions/survey_quick_access.js`
- `addons/survey/static/src/interactions/survey_result.js`
- `addons/survey/static/src/interactions/survey_result_chart.js`
- `addons/survey/static/src/interactions/survey_result_pagination.js`
- `addons/survey/static/src/interactions/survey_session_chart.js`
- `addons/survey/static/src/interactions/survey_session_leaderboard.js`
- `addons/survey/static/src/interactions/survey_session_manage.js`
- `addons/survey/static/src/interactions/survey_session_text_answers.js`
- `addons/survey/static/src/interactions/survey_timer.js`
- `addons/survey/static/src/interactions/utils.js`
- `addons/survey/static/src/js/libs/chartjs-plugin-datalabels.js`
- `addons/survey/static/src/js/survey_preload_image_mixin.js`
- `addons/survey/static/src/js/tours/survey_tour.js`
- `addons/survey/static/src/question_page/description_page_field.js`
- `addons/survey/static/src/question_page/description_page_field.xml`
- `addons/survey/static/src/question_page/question_page_list_renderer.js`
- `addons/survey/static/src/question_page/question_page_one2many_field.js`
- `addons/survey/static/src/scss/survey_question_views.scss`
- `addons/survey/static/src/scss/survey_reports.scss`
- `addons/survey/static/src/scss/survey_survey_views.dark.scss`
- `addons/survey/static/src/scss/survey_survey_views.scss`
- `addons/survey/static/src/scss/survey_templates_form.scss`
- `addons/survey/static/src/scss/survey_templates_results.scss`
- `addons/survey/static/src/utils.js`
- `addons/survey/static/src/views/components/survey_survey_action_helper/survey_survey_action_helper.js`
- `addons/survey/static/src/views/components/survey_survey_action_helper/survey_survey_action_helper.xml`
- `addons/survey/static/src/views/form/survey_invite_form_controller.js`
- `addons/survey/static/src/views/kanban/kanban_record.js`
- `addons/survey/static/src/views/kanban/kanban_renderer.js`
- `addons/survey/static/src/views/kanban/kanban_renderer.xml`
- `addons/survey/static/src/views/kanban/kanban_view.js`
- `addons/survey/static/src/views/list/list_renderer.js`
- `addons/survey/static/src/views/list/list_renderer.xml`
- `addons/survey/static/src/views/list/list_view.js`
- `addons/survey/static/src/views/widgets/boolean_update_flag_field/boolean_update_flag_fields.js`
- `addons/survey/static/src/views/widgets/integer_update_flag_field/integer_update_flag_fields.js`
- `addons/survey/static/src/views/widgets/radio_selection_with_filter/radio_selection_field_with_filter.js`
- `addons/survey/static/src/views/widgets/survey_question_trigger/survey_question_trigger.js`
- `addons/survey/static/src/views/widgets/survey_question_trigger/survey_question_trigger.xml`
- `addons/survey/static/src/xml/survey_paginated_results_rows_template.xml`
- `addons/survey/static/src/xml/survey_session_text_answer_template.xml`
- `addons/survey/static/tests/components/description_page_field.test.js`
- `addons/survey/static/tests/components/question_page_list_renderer.test.js`
- `addons/survey/static/tests/components/question_page_one2many_field.test.js`
- `addons/survey/static/tests/components/survey_question_trigger_widget.test.js`
- `addons/survey/static/tests/components/update_flag_field.test.js`
- `addons/survey/static/tests/fields/radio_selection_field_with_filter.test.js`
- `addons/survey/static/tests/tours/certification_failure.js`
- `addons/survey/static/tests/tours/certification_success.js`
- `addons/survey/static/tests/tours/survey.js`
- `addons/survey/static/tests/tours/survey_chained_conditional_questions.js`
- `addons/survey/static/tests/tours/survey_conditional_questions_on_different_page.js`
- `addons/survey/static/tests/tours/survey_form.js`
- `addons/survey/static/tests/tours/survey_prefill.js`
- `addons/survey/static/tests/tours/survey_roaming_mandatory_questions.js`
- `addons/survey/tests/__init__.py`
- `addons/survey/tests/common.py`
- `addons/survey/tests/test_certification_badge.py`
- `addons/survey/tests/test_certification_flow.py`
- `addons/survey/tests/test_ir_http.py`
- `addons/survey/tests/test_survey.py`
- `addons/survey/tests/test_survey_compute_pages_questions.py`
- `addons/survey/tests/test_survey_controller.py`
- `addons/survey/tests/test_survey_flow.py`
- `addons/survey/tests/test_survey_flow_with_conditions.py`
- `addons/survey/tests/test_survey_invite.py`
- `addons/survey/tests/test_survey_performance.py`
- `addons/survey/tests/test_survey_randomize.py`
- `addons/survey/tests/test_survey_results.py`
- `addons/survey/tests/test_survey_security.py`
- `addons/survey/tests/test_survey_ui_backend.py`
- `addons/survey/tests/test_survey_ui_certification.py`
- `addons/survey/tests/test_survey_ui_feedback.py`
- `addons/survey/views/digest_views.xml`
- `addons/survey/views/gamification_badge_views.xml`
- `addons/survey/views/res_partner_views.xml`
- `addons/survey/views/survey_menus.xml`
- `addons/survey/views/survey_question_views.xml`
- `addons/survey/views/survey_survey_views.xml`
- `addons/survey/views/survey_templates.xml`
- `addons/survey/views/survey_templates_management.xml`
- `addons/survey/views/survey_templates_print.xml`
- `addons/survey/views/survey_templates_statistics.xml`
- `addons/survey/views/survey_templates_user_input_session.xml`
- `addons/survey/views/survey_user_views.xml`
- `addons/survey/wizard/__init__.py`
- `addons/survey/wizard/survey_invite.py`
- `addons/survey/wizard/survey_invite_views.xml`
