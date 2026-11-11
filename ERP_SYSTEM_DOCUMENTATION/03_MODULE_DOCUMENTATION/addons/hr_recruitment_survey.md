# Module: hr_recruitment_survey

- **Module ID:** MOD-097
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_recruitment_survey`
- **Manifest:** `addons/hr_recruitment_survey/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Surveys

**Manifest description:**

Use interview forms during recruitment process.
This module is integrated with the survey module
to allow you to define interviews for different jobs.

**Scope evidence:** The module contains 80 files, including 16 Python, 9 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `survey`, `hr_recruitment`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 2
- XML/data/view/template files: 9
- Browser asset files: 0
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr_recruitment_survey/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 51 methods, 1 constraint handlers, 2 onchange handlers, and 12 dependency declarations.
- **Evidence:** `addons/hr_recruitment_survey/models/survey_user_input.py:6`, `addons/hr_recruitment_survey/models/hr_job.py:6`, `addons/hr_recruitment_survey/models/survey_survey.py:6`, `addons/hr_recruitment_survey/models/hr_applicant.py:10`, `addons/hr_recruitment_survey/wizard/hr_recruitment_survey_invite.py:16`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/hr_recruitment_survey/controllers/main.py`, `addons/hr_recruitment_survey/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 9 XML files and 0 JavaScript/TypeScript files; static XML analysis found 41 record/template/menu identifiers.
- **Evidence:** `addons/hr_recruitment_survey/wizard/survey_invite_views.xml:4`, `addons/hr_recruitment_survey/data/mail_template_data.xml:4`, `addons/hr_recruitment_survey/data/survey_demo.xml:3`, `addons/hr_recruitment_survey/data/survey_demo.xml:20`, `addons/hr_recruitment_survey/data/survey_demo.xml:30`, `addons/hr_recruitment_survey/data/survey_demo.xml:36`, `addons/hr_recruitment_survey/data/survey_demo.xml:42`, `addons/hr_recruitment_survey/data/survey_demo.xml:49`, `addons/hr_recruitment_survey/data/survey_demo.xml:57`, `addons/hr_recruitment_survey/data/survey_demo.xml:65`, `addons/hr_recruitment_survey/data/survey_demo.xml:73`, `addons/hr_recruitment_survey/data/survey_demo.xml:82`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/hr_recruitment_survey/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/hr_recruitment_survey/views/hr_applicant_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/hr_recruitment_survey/tests/recruitment_survey_common.py`, `addons/hr_recruitment_survey/tests/test_recruitment_survey_link_expiration.py`, `addons/hr_recruitment_survey/tests/test_recruitment_survey_link_permissions.py`, `addons/hr_recruitment_survey/tests/test_recruitment_survey.py`, `addons/hr_recruitment_survey/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 9; representative identifiers: `hr_recruitment_survey_invite_view_form`, `mail_template_applicant_interview_invite`, `survey_recruitment_form`, `survey_recruitment_form_p1`, `survey_recruitment_form_p1_q1`, `survey_recruitment_form_p1_q2`, `survey_recruitment_form_p1_q3`, `survey_recruitment_form_p1_q4`, `survey_recruitment_form_p1_q5`, `survey_recruitment_form_p1_q6`, `survey_recruitment_form_p1_q7`, `survey_recruitment_form_p1_q8`, `survey_recruitment_form_p1_q8_col1`, `survey_recruitment_form_p1_q8_col2`, `survey_recruitment_form_p1_q8_col3`, `survey_recruitment_form_p1_q8_row1`, `survey_recruitment_form_p1_q8_row2`, `survey_recruitment_form_p1_q8_row3`, `survey_recruitment_form_p1_q8_row4`, `survey_recruitment_form_p1_q8_row5`
- Menus: 1; representative evidence: `addons/hr_recruitment_survey/views/survey_survey_views.xml:92`
- Templates: 1; representative evidence: `addons/hr_recruitment_survey/views/survey_templates_statistics.xml:4`
- View/action field declarations: 20; representative evidence: `addons/hr_recruitment_survey/wizard/survey_invite_views.xml:7`, `addons/hr_recruitment_survey/wizard/survey_invite_views.xml:9`, `addons/hr_recruitment_survey/views/hr_job_views.xml:5`, `addons/hr_recruitment_survey/views/hr_job_views.xml:7`, `addons/hr_recruitment_survey/views/hr_job_views.xml:20`, `addons/hr_recruitment_survey/views/hr_job_views.xml:22`, `addons/hr_recruitment_survey/views/res_config_setting_views.xml:5`, `addons/hr_recruitment_survey/views/res_config_setting_views.xml:7`, `addons/hr_recruitment_survey/views/hr_applicant_views.xml:5`, `addons/hr_recruitment_survey/views/hr_applicant_views.xml:7`, `addons/hr_recruitment_survey/views/hr_applicant_views.xml:25`, `addons/hr_recruitment_survey/views/hr_applicant_views.xml:27`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_recruitment_survey/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/hr_recruitment_survey/views/hr_applicant_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `survey.user_input` (addons/hr_recruitment_survey/models/survey_user_input.py:6); inherits `hr.job` (addons/hr_recruitment_survey/models/hr_job.py:6); inherits `survey.survey` (addons/hr_recruitment_survey/models/survey_survey.py:6); inherits `hr.applicant` (addons/hr_recruitment_survey/models/hr_applicant.py:10); `hr.recruitment.survey.invite` (addons/hr_recruitment_survey/wizard/hr_recruitment_survey_invite.py:16)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `survey`, `hr_recruitment`
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

- `addons/hr_recruitment_survey/README.md`
- `addons/hr_recruitment_survey/__init__.py`
- `addons/hr_recruitment_survey/__manifest__.py`
- `addons/hr_recruitment_survey/controllers/__init__.py`
- `addons/hr_recruitment_survey/controllers/main.py`
- `addons/hr_recruitment_survey/data/hr_job_demo.xml`
- `addons/hr_recruitment_survey/data/mail_template_data.xml`
- `addons/hr_recruitment_survey/data/survey_demo.xml`
- `addons/hr_recruitment_survey/i18n/af.po`
- `addons/hr_recruitment_survey/i18n/ar.po`
- `addons/hr_recruitment_survey/i18n/az.po`
- `addons/hr_recruitment_survey/i18n/bg.po`
- `addons/hr_recruitment_survey/i18n/bs.po`
- `addons/hr_recruitment_survey/i18n/ca.po`
- `addons/hr_recruitment_survey/i18n/cs.po`
- `addons/hr_recruitment_survey/i18n/da.po`
- `addons/hr_recruitment_survey/i18n/de.po`
- `addons/hr_recruitment_survey/i18n/el.po`
- `addons/hr_recruitment_survey/i18n/es.po`
- `addons/hr_recruitment_survey/i18n/es_419.po`
- `addons/hr_recruitment_survey/i18n/et.po`
- `addons/hr_recruitment_survey/i18n/fa.po`
- `addons/hr_recruitment_survey/i18n/fi.po`
- `addons/hr_recruitment_survey/i18n/fr.po`
- `addons/hr_recruitment_survey/i18n/gu.po`
- `addons/hr_recruitment_survey/i18n/he.po`
- `addons/hr_recruitment_survey/i18n/hi.po`
- `addons/hr_recruitment_survey/i18n/hr.po`
- `addons/hr_recruitment_survey/i18n/hr_recruitment_survey.pot`
- `addons/hr_recruitment_survey/i18n/hu.po`
- `addons/hr_recruitment_survey/i18n/id.po`
- `addons/hr_recruitment_survey/i18n/is.po`
- `addons/hr_recruitment_survey/i18n/it.po`
- `addons/hr_recruitment_survey/i18n/ja.po`
- `addons/hr_recruitment_survey/i18n/kab.po`
- `addons/hr_recruitment_survey/i18n/km.po`
- `addons/hr_recruitment_survey/i18n/ko.po`
- `addons/hr_recruitment_survey/i18n/ku.po`
- `addons/hr_recruitment_survey/i18n/lo.po`
- `addons/hr_recruitment_survey/i18n/lt.po`
- `addons/hr_recruitment_survey/i18n/lv.po`
- `addons/hr_recruitment_survey/i18n/mn.po`
- `addons/hr_recruitment_survey/i18n/my.po`
- `addons/hr_recruitment_survey/i18n/nb.po`
- `addons/hr_recruitment_survey/i18n/nl.po`
- `addons/hr_recruitment_survey/i18n/pl.po`
- `addons/hr_recruitment_survey/i18n/pt.po`
- `addons/hr_recruitment_survey/i18n/pt_BR.po`
- `addons/hr_recruitment_survey/i18n/ro.po`
- `addons/hr_recruitment_survey/i18n/ru.po`
- `addons/hr_recruitment_survey/i18n/sk.po`
- `addons/hr_recruitment_survey/i18n/sl.po`
- `addons/hr_recruitment_survey/i18n/sr@latin.po`
- `addons/hr_recruitment_survey/i18n/sv.po`
- `addons/hr_recruitment_survey/i18n/th.po`
- `addons/hr_recruitment_survey/i18n/tr.po`
- `addons/hr_recruitment_survey/i18n/uk.po`
- `addons/hr_recruitment_survey/i18n/uz.po`
- `addons/hr_recruitment_survey/i18n/vi.po`
- `addons/hr_recruitment_survey/i18n/zh_CN.po`
- `addons/hr_recruitment_survey/i18n/zh_TW.po`
- `addons/hr_recruitment_survey/models/__init__.py`
- `addons/hr_recruitment_survey/models/hr_applicant.py`
- `addons/hr_recruitment_survey/models/hr_job.py`
- `addons/hr_recruitment_survey/models/survey_survey.py`
- `addons/hr_recruitment_survey/models/survey_user_input.py`
- `addons/hr_recruitment_survey/security/ir.access.csv`
- `addons/hr_recruitment_survey/tests/__init__.py`
- `addons/hr_recruitment_survey/tests/recruitment_survey_common.py`
- `addons/hr_recruitment_survey/tests/test_recruitment_survey.py`
- `addons/hr_recruitment_survey/tests/test_recruitment_survey_link_expiration.py`
- `addons/hr_recruitment_survey/tests/test_recruitment_survey_link_permissions.py`
- `addons/hr_recruitment_survey/views/hr_applicant_views.xml`
- `addons/hr_recruitment_survey/views/hr_job_views.xml`
- `addons/hr_recruitment_survey/views/res_config_setting_views.xml`
- `addons/hr_recruitment_survey/views/survey_survey_views.xml`
- `addons/hr_recruitment_survey/views/survey_templates_statistics.xml`
- `addons/hr_recruitment_survey/wizard/__init__.py`
- `addons/hr_recruitment_survey/wizard/hr_recruitment_survey_invite.py`
- `addons/hr_recruitment_survey/wizard/survey_invite_views.xml`
