# Module: survey_crm

- **Module ID:** MOD-568
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/survey_crm`
- **Manifest:** `addons/survey_crm/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Surveys`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Generate leads from surveys

**Manifest description:**

Bridge module between Survey and CRM.
    Enables the creation of a lead from a survey when the participant selects lead-generating answers.
    An option on the suggested answers can be activated to make them lead-generating.

**Scope evidence:** The module contains 67 files, including 11 Python, 5 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `survey`, `crm`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 1
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 18 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/survey_crm/models/survey_user_input.py:6`, `addons/survey_crm/models/survey_question_answer.py:4`, `addons/survey_crm/models/survey_survey.py:6`, `addons/survey_crm/models/survey_question.py:4`, `addons/survey_crm/models/templates/survey_survey.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 1 JavaScript/TypeScript files; static XML analysis found 40 record/template/menu identifiers.
- **Evidence:** `addons/survey_crm/demo/lead_qualification_answer_demo.xml:4`, `addons/survey_crm/demo/lead_qualification_answer_demo.xml:11`, `addons/survey_crm/demo/lead_qualification_answer_demo.xml:19`, `addons/survey_crm/demo/lead_qualification_answer_demo.xml:27`, `addons/survey_crm/demo/lead_qualification_answer_demo.xml:35`, `addons/survey_crm/demo/lead_qualification_answer_demo.xml:43`, `addons/survey_crm/demo/lead_qualification_answer_demo.xml:51`, `addons/survey_crm/demo/lead_qualification_answer_demo.xml:59`, `addons/survey_crm/demo/lead_qualification_answer_demo.xml:67`, `addons/survey_crm/demo/lead_qualification_answer_demo.xml:74`, `addons/survey_crm/demo/lead_qualification_survey_demo.xml:5`, `addons/survey_crm/demo/lead_qualification_survey_demo.xml:22`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/survey_crm/tests/__init__.py`, `addons/survey_crm/tests/test_survey_crm.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `lead_qualification_user_input_1`, `user_input_line_q1`, `user_input_line_q2`, `user_input_line_q3`, `user_input_line_q4`, `user_input_line_q6`, `user_input_line_q7_3`, `user_input_line_q8`, `user_input_line_q10`, `user_input_line_q11`, `lead_qualification_survey`, `lead_qualification_question_0`, `lead_qualification_question_1`, `lead_qualification_question_1_question_answer_1`, `lead_qualification_question_1_question_answer_2`, `lead_qualification_question_2`, `lead_qualification_question_3`, `lead_qualification_question_4`, `lead_qualification_question_5`, `lead_qualification_question_6`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 8; representative evidence: `addons/survey_crm/views/survey_user_views.xml:7`, `addons/survey_crm/views/survey_user_views.xml:9`, `addons/survey_crm/views/survey_question_views.xml:7`, `addons/survey_crm/views/survey_question_views.xml:9`, `addons/survey_crm/views/survey_survey_views.xml:7`, `addons/survey_crm/views/survey_survey_views.xml:9`, `addons/survey_crm/views/survey_survey_views.xml:35`, `addons/survey_crm/views/survey_survey_views.xml:37`
- Browser assets: 1; representative files: `addons/survey_crm/static/src/components/lead_generation_dropdown/crm_lead_gen_element.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/survey_crm/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `survey.user_input` (addons/survey_crm/models/survey_user_input.py:6); inherits `survey.question.answer` (addons/survey_crm/models/survey_question_answer.py:4); inherits `survey.survey` (addons/survey_crm/models/survey_survey.py:6); inherits `survey.question` (addons/survey_crm/models/survey_question.py:4); inherits `survey.survey` (addons/survey_crm/models/templates/survey_survey.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `survey`, `crm`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/survey_crm/__init__.py`
- `addons/survey_crm/__manifest__.py`
- `addons/survey_crm/demo/lead_qualification_answer_demo.xml`
- `addons/survey_crm/demo/lead_qualification_survey_demo.xml`
- `addons/survey_crm/i18n/ar.po`
- `addons/survey_crm/i18n/az.po`
- `addons/survey_crm/i18n/bg.po`
- `addons/survey_crm/i18n/bs.po`
- `addons/survey_crm/i18n/ca.po`
- `addons/survey_crm/i18n/cs.po`
- `addons/survey_crm/i18n/da.po`
- `addons/survey_crm/i18n/de.po`
- `addons/survey_crm/i18n/el.po`
- `addons/survey_crm/i18n/es.po`
- `addons/survey_crm/i18n/es_419.po`
- `addons/survey_crm/i18n/et.po`
- `addons/survey_crm/i18n/fa.po`
- `addons/survey_crm/i18n/fi.po`
- `addons/survey_crm/i18n/fr.po`
- `addons/survey_crm/i18n/he.po`
- `addons/survey_crm/i18n/hi.po`
- `addons/survey_crm/i18n/hr.po`
- `addons/survey_crm/i18n/hu.po`
- `addons/survey_crm/i18n/id.po`
- `addons/survey_crm/i18n/it.po`
- `addons/survey_crm/i18n/ja.po`
- `addons/survey_crm/i18n/kab.po`
- `addons/survey_crm/i18n/ko.po`
- `addons/survey_crm/i18n/ku.po`
- `addons/survey_crm/i18n/lo.po`
- `addons/survey_crm/i18n/lt.po`
- `addons/survey_crm/i18n/lv.po`
- `addons/survey_crm/i18n/mn.po`
- `addons/survey_crm/i18n/my.po`
- `addons/survey_crm/i18n/nb.po`
- `addons/survey_crm/i18n/nl.po`
- `addons/survey_crm/i18n/pl.po`
- `addons/survey_crm/i18n/pt.po`
- `addons/survey_crm/i18n/pt_BR.po`
- `addons/survey_crm/i18n/ro.po`
- `addons/survey_crm/i18n/ru.po`
- `addons/survey_crm/i18n/sk.po`
- `addons/survey_crm/i18n/sl.po`
- `addons/survey_crm/i18n/sr@latin.po`
- `addons/survey_crm/i18n/survey_crm.pot`
- `addons/survey_crm/i18n/sv.po`
- `addons/survey_crm/i18n/th.po`
- `addons/survey_crm/i18n/tr.po`
- `addons/survey_crm/i18n/uk.po`
- `addons/survey_crm/i18n/uz.po`
- `addons/survey_crm/i18n/vi.po`
- `addons/survey_crm/i18n/zh_CN.po`
- `addons/survey_crm/i18n/zh_TW.po`
- `addons/survey_crm/models/__init__.py`
- `addons/survey_crm/models/survey_question.py`
- `addons/survey_crm/models/survey_question_answer.py`
- `addons/survey_crm/models/survey_survey.py`
- `addons/survey_crm/models/survey_user_input.py`
- `addons/survey_crm/models/templates/__init__.py`
- `addons/survey_crm/models/templates/survey_survey.py`
- `addons/survey_crm/static/src/components/lead_generation_dropdown/crm_lead_gen_element.js`
- `addons/survey_crm/static/src/img/survey_sample_lead_qualification.svg`
- `addons/survey_crm/tests/__init__.py`
- `addons/survey_crm/tests/test_survey_crm.py`
- `addons/survey_crm/views/survey_question_views.xml`
- `addons/survey_crm/views/survey_survey_views.xml`
- `addons/survey_crm/views/survey_user_views.xml`
