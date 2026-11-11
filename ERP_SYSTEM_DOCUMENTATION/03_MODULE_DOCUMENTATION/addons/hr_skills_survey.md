# Module: hr_skills_survey

- **Module ID:** MOD-101
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_skills_survey`
- **Manifest:** `addons/hr_skills_survey/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources/Employees`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Add certification to resume of your employees

**Manifest description:**

Certification and Skills for HR
===============================

This module adds certification to resume for employees.

**Scope evidence:** The module contains 61 files, including 8 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `hr_skills`, `survey`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 5 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/hr_skills_survey/models/survey_user.py:10`, `addons/hr_skills_survey/models/hr_resume_line.py:8`, `addons/hr_skills_survey/models/survey_survey.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/hr_skills_survey/data/hr_resume_data.xml:4`, `addons/hr_skills_survey/data/hr_resume_demo.xml:5`, `addons/hr_skills_survey/data/hr_resume_demo.xml:14`, `addons/hr_skills_survey/data/hr_resume_demo.xml:23`, `addons/hr_skills_survey/views/hr_templates.xml:3`, `addons/hr_skills_survey/views/survey_survey_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/hr_skills_survey/tests/__init__.py`, `addons/hr_skills_survey/tests/test_certification_flow.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `resume_type_certification`, `resume_line_valid`, `resume_line_expiring`, `resume_line_aws`, `resume_survey_line_view_form`, `survey_survey_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/hr_skills_survey/views/hr_templates.xml:5`, `addons/hr_skills_survey/views/hr_templates.xml:8`, `addons/hr_skills_survey/views/survey_survey_views.xml:6`, `addons/hr_skills_survey/views/survey_survey_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_skills_survey/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `survey.user_input` (addons/hr_skills_survey/models/survey_user.py:10); inherits `hr.resume.line` (addons/hr_skills_survey/models/hr_resume_line.py:8); inherits `survey.survey` (addons/hr_skills_survey/models/survey_survey.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr_skills`, `survey`
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

- `addons/hr_skills_survey/__init__.py`
- `addons/hr_skills_survey/__manifest__.py`
- `addons/hr_skills_survey/data/hr_resume_data.xml`
- `addons/hr_skills_survey/data/hr_resume_demo.xml`
- `addons/hr_skills_survey/i18n/ar.po`
- `addons/hr_skills_survey/i18n/az.po`
- `addons/hr_skills_survey/i18n/bg.po`
- `addons/hr_skills_survey/i18n/bs.po`
- `addons/hr_skills_survey/i18n/ca.po`
- `addons/hr_skills_survey/i18n/cs.po`
- `addons/hr_skills_survey/i18n/da.po`
- `addons/hr_skills_survey/i18n/de.po`
- `addons/hr_skills_survey/i18n/el.po`
- `addons/hr_skills_survey/i18n/es.po`
- `addons/hr_skills_survey/i18n/es_419.po`
- `addons/hr_skills_survey/i18n/et.po`
- `addons/hr_skills_survey/i18n/fa.po`
- `addons/hr_skills_survey/i18n/fi.po`
- `addons/hr_skills_survey/i18n/fr.po`
- `addons/hr_skills_survey/i18n/he.po`
- `addons/hr_skills_survey/i18n/hi.po`
- `addons/hr_skills_survey/i18n/hr.po`
- `addons/hr_skills_survey/i18n/hr_skills_survey.pot`
- `addons/hr_skills_survey/i18n/hu.po`
- `addons/hr_skills_survey/i18n/id.po`
- `addons/hr_skills_survey/i18n/it.po`
- `addons/hr_skills_survey/i18n/ja.po`
- `addons/hr_skills_survey/i18n/kab.po`
- `addons/hr_skills_survey/i18n/ko.po`
- `addons/hr_skills_survey/i18n/ku.po`
- `addons/hr_skills_survey/i18n/lo.po`
- `addons/hr_skills_survey/i18n/lt.po`
- `addons/hr_skills_survey/i18n/lv.po`
- `addons/hr_skills_survey/i18n/mn.po`
- `addons/hr_skills_survey/i18n/my.po`
- `addons/hr_skills_survey/i18n/nb.po`
- `addons/hr_skills_survey/i18n/nl.po`
- `addons/hr_skills_survey/i18n/pl.po`
- `addons/hr_skills_survey/i18n/pt.po`
- `addons/hr_skills_survey/i18n/pt_BR.po`
- `addons/hr_skills_survey/i18n/ro.po`
- `addons/hr_skills_survey/i18n/ru.po`
- `addons/hr_skills_survey/i18n/sk.po`
- `addons/hr_skills_survey/i18n/sl.po`
- `addons/hr_skills_survey/i18n/sr@latin.po`
- `addons/hr_skills_survey/i18n/sv.po`
- `addons/hr_skills_survey/i18n/th.po`
- `addons/hr_skills_survey/i18n/tr.po`
- `addons/hr_skills_survey/i18n/uk.po`
- `addons/hr_skills_survey/i18n/uz.po`
- `addons/hr_skills_survey/i18n/vi.po`
- `addons/hr_skills_survey/i18n/zh_CN.po`
- `addons/hr_skills_survey/i18n/zh_TW.po`
- `addons/hr_skills_survey/models/__init__.py`
- `addons/hr_skills_survey/models/hr_resume_line.py`
- `addons/hr_skills_survey/models/survey_survey.py`
- `addons/hr_skills_survey/models/survey_user.py`
- `addons/hr_skills_survey/tests/__init__.py`
- `addons/hr_skills_survey/tests/test_certification_flow.py`
- `addons/hr_skills_survey/views/hr_templates.xml`
- `addons/hr_skills_survey/views/survey_survey_views.xml`
