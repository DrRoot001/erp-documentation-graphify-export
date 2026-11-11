# Module: hr_recruitment

- **Module ID:** MOD-094
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_recruitment`
- **Manifest:** `addons/hr_recruitment/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Human Resources/Recruitment`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Track your recruitment pipeline

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 188 files, including 40 Python, 34 XML, and 18 JavaScript/TypeScript files. The manifest declares dependencies: `hr`, `calendar`, `utm`, `attachment_indexation`, `web_tour`, `digest`.

## 2. Module structure

- Model/business logic files: 29
- Controller/API files: 0
- XML/data/view/template files: 34
- Browser asset files: 18
- Security files: 2
- Test files: 8
- Scheduled/automation evidence files: 2
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr_recruitment/security/ir.access.csv`, `addons/hr_recruitment/security/hr_recruitment_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 29 model declarations, 203 methods, 1 constraint handlers, 1 onchange handlers, and 35 dependency declarations.
- **Evidence:** `addons/hr_recruitment/models/res_partner.py:4`, `addons/hr_recruitment/models/hr_job_tag.py:8`, `addons/hr_recruitment/models/digest.py:7`, `addons/hr_recruitment/models/res_groups.py:6`, `addons/hr_recruitment/models/res_config_settings.py:6`, `addons/hr_recruitment/models/hr_recruitment_stage.py:7`, `addons/hr_recruitment/models/hr_department.py:6`, `addons/hr_recruitment/models/hr_talent_pool.py:7`, `addons/hr_recruitment/models/calendar.py:7`, `addons/hr_recruitment/models/hr_recruitment_source.py:7`, `addons/hr_recruitment/models/mail_activity_plan.py:6`, `addons/hr_recruitment/models/utm_source.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 34 XML files and 18 JavaScript/TypeScript files; static XML analysis found 298 record/template/menu identifiers.
- **Evidence:** `addons/hr_recruitment/security/hr_recruitment_security.xml:3`, `addons/hr_recruitment/security/hr_recruitment_security.xml:9`, `addons/hr_recruitment/security/hr_recruitment_security.xml:17`, `addons/hr_recruitment/security/hr_recruitment_security.xml:24`, `addons/hr_recruitment/security/hr_recruitment_security.xml:32`, `addons/hr_recruitment/security/hr_recruitment_security.xml:36`, `addons/hr_recruitment/security/hr_recruitment_security.xml:41`, `addons/hr_recruitment/wizard/applicant_refuse_reason_views.xml:3`, `addons/hr_recruitment/wizard/applicant_refuse_reason_views.xml:59`, `addons/hr_recruitment/wizard/applicant_refuse_reason_views.xml:67`, `addons/hr_recruitment/wizard/talent_pool_add_applicants_views.xml:3`, `addons/hr_recruitment/wizard/job_add_applicants_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/hr_recruitment/security/ir.access.csv`, `addons/hr_recruitment/security/hr_recruitment_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/hr_recruitment/views/hr_job_views.xml`, `addons/hr_recruitment/views/hr_applicant_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 8 test files are present.
- **Evidence:** `addons/hr_recruitment/tests/test_recruitment_talent_pools.py`, `addons/hr_recruitment/tests/test_utm.py`, `addons/hr_recruitment/tests/test_recruitment_interviewer.py`, `addons/hr_recruitment/tests/test_recruitment.py`, `addons/hr_recruitment/tests/test_recruitment_allowed_user_ids.py`, `addons/hr_recruitment/tests/__init__.py`, `addons/hr_recruitment/tests/test_recruitment_process.py`, `addons/hr_recruitment/tests/test_recruitment_mail.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 34; representative identifiers: `res_groups_privilege_recruitment`, `group_hr_recruitment_interviewer`, `group_hr_recruitment_user`, `group_hr_recruitment_manager`, `group_applicant_cv_display`, `base.group_user`, `hr.access_hr_job_user`, `applicant_get_refuse_reason_view_form`, `applicant_get_refuse_reason_action`, `applicant_refuse_single_view_form`, `talent_pool_add_applicants_view_form`, `job_add_applicants_view_form`, `job_add_applicants_from_job_view_form`, `base.user_demo`, `base.default_user_group`, `multi_site_job_tag`, `cross_departmental_job_tag`, `recruiter_sourced_job_tag`, `hr.job_developer`, `hr.job_cto`
- Menus: 29; representative evidence: `addons/hr_recruitment/views/menuitems.xml:3`, `addons/hr_recruitment/views/menuitems.xml:10`, `addons/hr_recruitment/views/menuitems.xml:16`, `addons/hr_recruitment/views/menuitems.xml:24`, `addons/hr_recruitment/views/menuitems.xml:32`, `addons/hr_recruitment/views/menuitems.xml:40`, `addons/hr_recruitment/views/menuitems.xml:48`, `addons/hr_recruitment/views/menuitems.xml:55`, `addons/hr_recruitment/views/menuitems.xml:62`, `addons/hr_recruitment/views/menuitems.xml:69`, `addons/hr_recruitment/views/menuitems.xml:77`, `addons/hr_recruitment/views/menuitems.xml:83`
- Templates: 2; representative evidence: `addons/hr_recruitment/data/mail_templates.xml:4`, `addons/hr_recruitment/data/mail_templates.xml:8`
- View/action field declarations: 214; representative evidence: `addons/hr_recruitment/wizard/applicant_refuse_reason_views.xml:5`, `addons/hr_recruitment/wizard/applicant_refuse_reason_views.xml:6`, `addons/hr_recruitment/wizard/applicant_refuse_reason_views.xml:61`, `addons/hr_recruitment/wizard/applicant_refuse_reason_views.xml:62`, `addons/hr_recruitment/wizard/applicant_refuse_reason_views.xml:69`, `addons/hr_recruitment/wizard/applicant_refuse_reason_views.xml:70`, `addons/hr_recruitment/wizard/talent_pool_add_applicants_views.xml:5`, `addons/hr_recruitment/wizard/talent_pool_add_applicants_views.xml:6`, `addons/hr_recruitment/wizard/job_add_applicants_views.xml:5`, `addons/hr_recruitment/wizard/job_add_applicants_views.xml:6`, `addons/hr_recruitment/wizard/job_add_applicants_views.xml:40`, `addons/hr_recruitment/wizard/job_add_applicants_views.xml:41`
- Browser assets: 18; representative files: `addons/hr_recruitment/static/tests/ir_attachments.test.js`, `addons/hr_recruitment/static/src/applicant_char/applicant_char.js`, `addons/hr_recruitment/static/src/views/recruitment_list_controller.js`, `addons/hr_recruitment/static/src/views/recruitment_helper_view.js`, `addons/hr_recruitment/static/src/views/recruitment_form_controller.js`, `addons/hr_recruitment/static/src/views/form_view.js`, `addons/hr_recruitment/static/src/views/recruitment_kanban_view.js`, `addons/hr_recruitment/static/src/views/recruitment_list_view.js`, `addons/hr_recruitment/static/src/views/recruitment_form_view.js`, `addons/hr_recruitment/static/src/hr_applicant_state_selection/hr_applicant_state_selection.js`, `addons/hr_recruitment/static/src/js/tours/hr_recruitment.js`, `addons/hr_recruitment/static/src/js/fields/applicant_line_many2many.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_recruitment/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/hr_recruitment/views/hr_job_views.xml`, `addons/hr_recruitment/views/hr_applicant_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 29
- Representative model evidence: inherits `res.partner` (addons/hr_recruitment/models/res_partner.py:4); `hr.job.tag` (addons/hr_recruitment/models/hr_job_tag.py:8); inherits `digest.digest` (addons/hr_recruitment/models/digest.py:7); inherits `res.groups` (addons/hr_recruitment/models/res_groups.py:6); inherits `res.config.settings` (addons/hr_recruitment/models/res_config_settings.py:6); `hr.recruitment.stage` (addons/hr_recruitment/models/hr_recruitment_stage.py:7); inherits `hr.department` (addons/hr_recruitment/models/hr_department.py:6); `hr.talent.pool` (addons/hr_recruitment/models/hr_talent_pool.py:7); inherits `calendar.event` (addons/hr_recruitment/models/calendar.py:7); `hr.recruitment.source` (addons/hr_recruitment/models/hr_recruitment_source.py:7); inherits `mail.activity.plan` (addons/hr_recruitment/models/mail_activity_plan.py:6); inherits `utm.source` (addons/hr_recruitment/models/utm_source.py:9); `hr.job.platform` (addons/hr_recruitment/models/hr_job_platform.py:7); `hr.job` (addons/hr_recruitment/models/hr_job.py:11); inherits `utm.campaign` (addons/hr_recruitment/models/utm_campaign.py:9); `hr.recruitment.degree` (addons/hr_recruitment/models/hr_recruitment_degree.py:6); `hr.applicant.category` (addons/hr_recruitment/models/hr_applicant_category.py:9); inherits `res.users` (addons/hr_recruitment/models/res_users.py:7); inherits `hr.employee` (addons/hr_recruitment/models/hr_employee.py:6); `hr.applicant.refuse.reason` (addons/hr_recruitment/models/hr_applicant_refuse_reason.py:7); inherits `ir.ui.menu` (addons/hr_recruitment/models/ir_ui_menu.py:6); inherits `ir.attachment` (addons/hr_recruitment/models/ir_attachment.py:8); `hr.applicant` (addons/hr_recruitment/models/hr_applicant.py:23); inherits `res.company` (addons/hr_recruitment/models/res_company.py:6); `talent.pool.add.applicants` (addons/hr_recruitment/wizard/talent_pool_add_applicants.py:4); `applicant.get.refuse.reason` (addons/hr_recruitment/wizard/applicant_refuse_reason.py:9); `applicant.refuse.single` (addons/hr_recruitment/wizard/applicant_refuse_reason.py:204); inherits `mail.activity.schedule` (addons/hr_recruitment/wizard/mail_activity_schedule.py:6); `job.add.applicants` (addons/hr_recruitment/wizard/job_add_applicants.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr`, `calendar`, `utm`, `attachment_indexation`, `web_tour`, `digest`
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

- `addons/hr_recruitment/README.md`
- `addons/hr_recruitment/__init__.py`
- `addons/hr_recruitment/__manifest__.py`
- `addons/hr_recruitment/data/digest_data.xml`
- `addons/hr_recruitment/data/hr_recruitment_data.xml`
- `addons/hr_recruitment/data/hr_recruitment_demo.xml`
- `addons/hr_recruitment/data/hr_recruitment_demo_jones_cv.pdf`
- `addons/hr_recruitment/data/hr_recruitment_demo_jose_cv.txt`
- `addons/hr_recruitment/data/hr_recruitment_demo_williams_cv.doc`
- `addons/hr_recruitment/data/hr_recruitment_tour.xml`
- `addons/hr_recruitment/data/mail_message_subtype_data.xml`
- `addons/hr_recruitment/data/mail_template_data.xml`
- `addons/hr_recruitment/data/mail_templates.xml`
- `addons/hr_recruitment/data/scenarios/hr_recruitment_scenario.xml`
- `addons/hr_recruitment/i18n/af.po`
- `addons/hr_recruitment/i18n/am.po`
- `addons/hr_recruitment/i18n/ar.po`
- `addons/hr_recruitment/i18n/az.po`
- `addons/hr_recruitment/i18n/bg.po`
- `addons/hr_recruitment/i18n/bs.po`
- `addons/hr_recruitment/i18n/ca.po`
- `addons/hr_recruitment/i18n/cs.po`
- `addons/hr_recruitment/i18n/da.po`
- `addons/hr_recruitment/i18n/de.po`
- `addons/hr_recruitment/i18n/el.po`
- `addons/hr_recruitment/i18n/es.po`
- `addons/hr_recruitment/i18n/es_419.po`
- `addons/hr_recruitment/i18n/es_CL.po`
- `addons/hr_recruitment/i18n/et.po`
- `addons/hr_recruitment/i18n/eu.po`
- `addons/hr_recruitment/i18n/fa.po`
- `addons/hr_recruitment/i18n/fi.po`
- `addons/hr_recruitment/i18n/fo.po`
- `addons/hr_recruitment/i18n/fr.po`
- `addons/hr_recruitment/i18n/fr_BE.po`
- `addons/hr_recruitment/i18n/fr_CA.po`
- `addons/hr_recruitment/i18n/gl.po`
- `addons/hr_recruitment/i18n/gu.po`
- `addons/hr_recruitment/i18n/he.po`
- `addons/hr_recruitment/i18n/hi.po`
- `addons/hr_recruitment/i18n/hr.po`
- `addons/hr_recruitment/i18n/hr_recruitment.pot`
- `addons/hr_recruitment/i18n/hu.po`
- `addons/hr_recruitment/i18n/id.po`
- `addons/hr_recruitment/i18n/is.po`
- `addons/hr_recruitment/i18n/it.po`
- `addons/hr_recruitment/i18n/ja.po`
- `addons/hr_recruitment/i18n/ka.po`
- `addons/hr_recruitment/i18n/kab.po`
- `addons/hr_recruitment/i18n/km.po`
- `addons/hr_recruitment/i18n/ko.po`
- `addons/hr_recruitment/i18n/ku.po`
- `addons/hr_recruitment/i18n/lb.po`
- `addons/hr_recruitment/i18n/lo.po`
- `addons/hr_recruitment/i18n/lt.po`
- `addons/hr_recruitment/i18n/lv.po`
- `addons/hr_recruitment/i18n/mk.po`
- `addons/hr_recruitment/i18n/mn.po`
- `addons/hr_recruitment/i18n/my.po`
- `addons/hr_recruitment/i18n/nb.po`
- `addons/hr_recruitment/i18n/nl.po`
- `addons/hr_recruitment/i18n/pl.po`
- `addons/hr_recruitment/i18n/pt.po`
- `addons/hr_recruitment/i18n/pt_BR.po`
- `addons/hr_recruitment/i18n/ro.po`
- `addons/hr_recruitment/i18n/ru.po`
- `addons/hr_recruitment/i18n/sk.po`
- `addons/hr_recruitment/i18n/sl.po`
- `addons/hr_recruitment/i18n/sq.po`
- `addons/hr_recruitment/i18n/sr@latin.po`
- `addons/hr_recruitment/i18n/sv.po`
- `addons/hr_recruitment/i18n/th.po`
- `addons/hr_recruitment/i18n/tr.po`
- `addons/hr_recruitment/i18n/uk.po`
- `addons/hr_recruitment/i18n/uz.po`
- `addons/hr_recruitment/i18n/vi.po`
- `addons/hr_recruitment/i18n/zh_CN.po`
- `addons/hr_recruitment/i18n/zh_TW.po`
- `addons/hr_recruitment/models/__init__.py`
- `addons/hr_recruitment/models/calendar.py`
- `addons/hr_recruitment/models/digest.py`
- `addons/hr_recruitment/models/hr_applicant.py`
- `addons/hr_recruitment/models/hr_applicant_category.py`
- `addons/hr_recruitment/models/hr_applicant_refuse_reason.py`
- `addons/hr_recruitment/models/hr_department.py`
- `addons/hr_recruitment/models/hr_employee.py`
- `addons/hr_recruitment/models/hr_job.py`
- `addons/hr_recruitment/models/hr_job_platform.py`
- `addons/hr_recruitment/models/hr_job_tag.py`
- `addons/hr_recruitment/models/hr_recruitment_degree.py`
- `addons/hr_recruitment/models/hr_recruitment_source.py`
- `addons/hr_recruitment/models/hr_recruitment_stage.py`
- `addons/hr_recruitment/models/hr_talent_pool.py`
- `addons/hr_recruitment/models/ir_attachment.py`
- `addons/hr_recruitment/models/ir_ui_menu.py`
- `addons/hr_recruitment/models/mail_activity_plan.py`
- `addons/hr_recruitment/models/res_company.py`
- `addons/hr_recruitment/models/res_config_settings.py`
- `addons/hr_recruitment/models/res_groups.py`
- `addons/hr_recruitment/models/res_partner.py`
- `addons/hr_recruitment/models/res_users.py`
- `addons/hr_recruitment/models/utm_campaign.py`
- `addons/hr_recruitment/models/utm_source.py`
- `addons/hr_recruitment/security/hr_recruitment_security.xml`
- `addons/hr_recruitment/security/ir.access.csv`
- `addons/hr_recruitment/static/applicant_cvs/Cecile_Donth_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/David_Armstrong_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/David_Billy_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/Enrique_Jones_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/Hubert_Blank_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/Johan_Duck_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/John_Bruno_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/Joren_Jacob_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/Jose_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/Kelly_Wallant_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/Marie_Justine_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/Meldona_Thang_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/Ohen_Rizome_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/Sandra_Elvis_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/Shane_Williams_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/Tina_Augustie_CV.pdf`
- `addons/hr_recruitment/static/applicant_cvs/Yin_Lee_CV.pdf`
- `addons/hr_recruitment/static/description/icon.png`
- `addons/hr_recruitment/static/description/icon.svg`
- `addons/hr_recruitment/static/description/icon_hi.png`
- `addons/hr_recruitment/static/src/applicant_char/applicant_char.js`
- `addons/hr_recruitment/static/src/applicant_char/applicant_char.scss`
- `addons/hr_recruitment/static/src/applicant_char/applicant_char.xml`
- `addons/hr_recruitment/static/src/core/common/@types/models.d.ts`
- `addons/hr_recruitment/static/src/core/common/hr_applicant_model.js`
- `addons/hr_recruitment/static/src/core/common/res_partner_model_patch.js`
- `addons/hr_recruitment/static/src/hr_applicant_state_selection/hr_applicant_state_selection.js`
- `addons/hr_recruitment/static/src/img/congratulations.png`
- `addons/hr_recruitment/static/src/js/buttons/generate_content_and_copy_button.js`
- `addons/hr_recruitment/static/src/js/fields/applicant_line_many2many.js`
- `addons/hr_recruitment/static/src/js/fields/recruitment_copy_clipboard_char_field/recruitment_copy_clipboard_char_field.js`
- `addons/hr_recruitment/static/src/js/fields/recruitment_copy_clipboard_char_field/recruitment_copy_clipboard_char_field.xml`
- `addons/hr_recruitment/static/src/js/tours/hr_recruitment.js`
- `addons/hr_recruitment/static/src/scss/hr_applicant.scss`
- `addons/hr_recruitment/static/src/scss/hr_job.scss`
- `addons/hr_recruitment/static/src/scss/hr_recruitment_widgets.scss`
- `addons/hr_recruitment/static/src/scss/job_add_applicants.scss`
- `addons/hr_recruitment/static/src/views/form_view.js`
- `addons/hr_recruitment/static/src/views/recruitment_form_controller.js`
- `addons/hr_recruitment/static/src/views/recruitment_form_view.js`
- `addons/hr_recruitment/static/src/views/recruitment_helper_view.js`
- `addons/hr_recruitment/static/src/views/recruitment_helper_view.xml`
- `addons/hr_recruitment/static/src/views/recruitment_kanban_view.js`
- `addons/hr_recruitment/static/src/views/recruitment_kanban_view.xml`
- `addons/hr_recruitment/static/src/views/recruitment_list_controller.js`
- `addons/hr_recruitment/static/src/views/recruitment_list_view.js`
- `addons/hr_recruitment/static/src/views/recruitment_list_view.xml`
- `addons/hr_recruitment/static/tests/ir_attachments.test.js`
- `addons/hr_recruitment/static/tests/mock_server/mock_models/hr_applicant.js`
- `addons/hr_recruitment/tests/__init__.py`
- `addons/hr_recruitment/tests/resume.eml`
- `addons/hr_recruitment/tests/test_recruitment.py`
- `addons/hr_recruitment/tests/test_recruitment_allowed_user_ids.py`
- `addons/hr_recruitment/tests/test_recruitment_interviewer.py`
- `addons/hr_recruitment/tests/test_recruitment_mail.py`
- `addons/hr_recruitment/tests/test_recruitment_process.py`
- `addons/hr_recruitment/tests/test_recruitment_talent_pools.py`
- `addons/hr_recruitment/tests/test_utm.py`
- `addons/hr_recruitment/views/digest_views.xml`
- `addons/hr_recruitment/views/hr_applicant_category_views.xml`
- `addons/hr_recruitment/views/hr_applicant_refuse_reason_views.xml`
- `addons/hr_recruitment/views/hr_applicant_views.xml`
- `addons/hr_recruitment/views/hr_department_views.xml`
- `addons/hr_recruitment/views/hr_employee_views.xml`
- `addons/hr_recruitment/views/hr_job_tag_views.xml`
- `addons/hr_recruitment/views/hr_job_views.xml`
- `addons/hr_recruitment/views/hr_recruitment_degree_views.xml`
- `addons/hr_recruitment/views/hr_recruitment_source_views.xml`
- `addons/hr_recruitment/views/hr_recruitment_stage_views.xml`
- `addons/hr_recruitment/views/hr_talent_pool_views.xml`
- `addons/hr_recruitment/views/ir_attachment_views.xml`
- `addons/hr_recruitment/views/mail_activity_plan_views.xml`
- `addons/hr_recruitment/views/mail_activity_views.xml`
- `addons/hr_recruitment/views/menuitems.xml`
- `addons/hr_recruitment/views/res_config_settings_views.xml`
- `addons/hr_recruitment/wizard/__init__.py`
- `addons/hr_recruitment/wizard/applicant_refuse_reason.py`
- `addons/hr_recruitment/wizard/applicant_refuse_reason_views.xml`
- `addons/hr_recruitment/wizard/job_add_applicants.py`
- `addons/hr_recruitment/wizard/job_add_applicants_views.xml`
- `addons/hr_recruitment/wizard/mail_activity_schedule.py`
- `addons/hr_recruitment/wizard/talent_pool_add_applicants.py`
- `addons/hr_recruitment/wizard/talent_pool_add_applicants_views.xml`
