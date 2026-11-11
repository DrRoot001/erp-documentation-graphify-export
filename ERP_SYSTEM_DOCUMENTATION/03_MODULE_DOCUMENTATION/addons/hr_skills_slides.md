# Module: hr_skills_slides

- **Module ID:** MOD-100
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_skills_slides`
- **Manifest:** `addons/hr_skills_slides/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources/Employees`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Add completed courses to resume of your employees

**Manifest description:**

E-learning and Skills for HR
============================

This module add completed courses to resume for employees.

**Scope evidence:** The module contains 66 files, including 9 Python, 7 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `hr_skills`, `website_slides`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 7
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

- **Description:** 5 model declarations, 16 methods, 0 constraint handlers, 1 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/hr_skills_slides/models/slide_channel.py:9`, `addons/hr_skills_slides/models/slide_channel.py:67`, `addons/hr_skills_slides/models/hr_employee_public.py:6`, `addons/hr_skills_slides/models/hr_resume_line.py:7`, `addons/hr_skills_slides/models/hr_employee.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 0 JavaScript/TypeScript files; static XML analysis found 14 record/template/menu identifiers.
- **Evidence:** `addons/hr_skills_slides/data/hr_resume_line_demo.xml:4`, `addons/hr_skills_slides/data/hr_resume_line_demo.xml:16`, `addons/hr_skills_slides/data/hr_resume_line_demo.xml:28`, `addons/hr_skills_slides/views/hr_employee_views.xml:3`, `addons/hr_skills_slides/views/hr_employee_views.xml:23`, `addons/hr_skills_slides/views/hr_employee_views.xml:34`, `addons/hr_skills_slides/views/hr_views.xml:3`, `addons/hr_skills_slides/views/hr_views.xml:9`, `addons/hr_skills_slides/views/hr_employee_public_views.xml:3`, `addons/hr_skills_slides/views/hr_resume_line_views.xml:3`, `addons/hr_skills_slides/views/hr_resume_line_views.xml:23`, `addons/hr_skills_slides/views/hr_resume_line_views.xml:40`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/hr_skills_slides/tests/test_hr_skills_slides.py`, `addons/hr_skills_slides/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `employee_niv_resume_line`, `employee_vad_resume_line`, `employee_chs_resume_line`, `hr_employee_view_form`, `hr_employee_public_resume_view_form_inherit`, `hr_employee_resume_view_form_inherit`, `Courses`, `eLearning`, `hr_employee_public_view_form`, `resume_slides_line_view_form`, `resume_slides_line_view_list`, `resume_slides_line_view_kanban`, `slide_channel_view_list`, `slide_channel_training_elearning_action`
- Menus: 2; representative evidence: `addons/hr_skills_slides/views/hr_views.xml:3`, `addons/hr_skills_slides/views/hr_views.xml:9`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 18; representative evidence: `addons/hr_skills_slides/views/hr_employee_views.xml:5`, `addons/hr_skills_slides/views/hr_employee_views.xml:8`, `addons/hr_skills_slides/views/hr_employee_views.xml:25`, `addons/hr_skills_slides/views/hr_employee_views.xml:27`, `addons/hr_skills_slides/views/hr_employee_views.xml:36`, `addons/hr_skills_slides/views/hr_employee_views.xml:38`, `addons/hr_skills_slides/views/hr_employee_public_views.xml:5`, `addons/hr_skills_slides/views/hr_employee_public_views.xml:7`, `addons/hr_skills_slides/views/hr_resume_line_views.xml:5`, `addons/hr_skills_slides/views/hr_resume_line_views.xml:7`, `addons/hr_skills_slides/views/hr_resume_line_views.xml:25`, `addons/hr_skills_slides/views/hr_resume_line_views.xml:27`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_skills_slides/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `slide.channel.partner` (addons/hr_skills_slides/models/slide_channel.py:9); inherits `slide.channel` (addons/hr_skills_slides/models/slide_channel.py:67); inherits `hr.employee.public` (addons/hr_skills_slides/models/hr_employee_public.py:6); inherits `hr.resume.line` (addons/hr_skills_slides/models/hr_resume_line.py:7); inherits `hr.employee` (addons/hr_skills_slides/models/hr_employee.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr_skills`, `website_slides`
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

- `addons/hr_skills_slides/__init__.py`
- `addons/hr_skills_slides/__manifest__.py`
- `addons/hr_skills_slides/data/hr_resume_line_demo.xml`
- `addons/hr_skills_slides/i18n/ar.po`
- `addons/hr_skills_slides/i18n/az.po`
- `addons/hr_skills_slides/i18n/bg.po`
- `addons/hr_skills_slides/i18n/bs.po`
- `addons/hr_skills_slides/i18n/ca.po`
- `addons/hr_skills_slides/i18n/cs.po`
- `addons/hr_skills_slides/i18n/da.po`
- `addons/hr_skills_slides/i18n/de.po`
- `addons/hr_skills_slides/i18n/el.po`
- `addons/hr_skills_slides/i18n/es.po`
- `addons/hr_skills_slides/i18n/es_419.po`
- `addons/hr_skills_slides/i18n/et.po`
- `addons/hr_skills_slides/i18n/fa.po`
- `addons/hr_skills_slides/i18n/fi.po`
- `addons/hr_skills_slides/i18n/fr.po`
- `addons/hr_skills_slides/i18n/he.po`
- `addons/hr_skills_slides/i18n/hi.po`
- `addons/hr_skills_slides/i18n/hr.po`
- `addons/hr_skills_slides/i18n/hr_skills_slides.pot`
- `addons/hr_skills_slides/i18n/hu.po`
- `addons/hr_skills_slides/i18n/id.po`
- `addons/hr_skills_slides/i18n/it.po`
- `addons/hr_skills_slides/i18n/ja.po`
- `addons/hr_skills_slides/i18n/kab.po`
- `addons/hr_skills_slides/i18n/ko.po`
- `addons/hr_skills_slides/i18n/ku.po`
- `addons/hr_skills_slides/i18n/lo.po`
- `addons/hr_skills_slides/i18n/lt.po`
- `addons/hr_skills_slides/i18n/lv.po`
- `addons/hr_skills_slides/i18n/mn.po`
- `addons/hr_skills_slides/i18n/my.po`
- `addons/hr_skills_slides/i18n/nb.po`
- `addons/hr_skills_slides/i18n/nl.po`
- `addons/hr_skills_slides/i18n/pl.po`
- `addons/hr_skills_slides/i18n/pt.po`
- `addons/hr_skills_slides/i18n/pt_BR.po`
- `addons/hr_skills_slides/i18n/ro.po`
- `addons/hr_skills_slides/i18n/ru.po`
- `addons/hr_skills_slides/i18n/sk.po`
- `addons/hr_skills_slides/i18n/sl.po`
- `addons/hr_skills_slides/i18n/sr@latin.po`
- `addons/hr_skills_slides/i18n/sv.po`
- `addons/hr_skills_slides/i18n/th.po`
- `addons/hr_skills_slides/i18n/tr.po`
- `addons/hr_skills_slides/i18n/uk.po`
- `addons/hr_skills_slides/i18n/uz.po`
- `addons/hr_skills_slides/i18n/vi.po`
- `addons/hr_skills_slides/i18n/zh_CN.po`
- `addons/hr_skills_slides/i18n/zh_TW.po`
- `addons/hr_skills_slides/models/__init__.py`
- `addons/hr_skills_slides/models/hr_employee.py`
- `addons/hr_skills_slides/models/hr_employee_public.py`
- `addons/hr_skills_slides/models/hr_resume_line.py`
- `addons/hr_skills_slides/models/slide_channel.py`
- `addons/hr_skills_slides/static/src/fields/resume_one2many/resume_one2many.xml`
- `addons/hr_skills_slides/static/src/scss/hr_skills.scss`
- `addons/hr_skills_slides/tests/__init__.py`
- `addons/hr_skills_slides/tests/test_hr_skills_slides.py`
- `addons/hr_skills_slides/views/hr_employee_public_views.xml`
- `addons/hr_skills_slides/views/hr_employee_views.xml`
- `addons/hr_skills_slides/views/hr_resume_line_views.xml`
- `addons/hr_skills_slides/views/hr_views.xml`
- `addons/hr_skills_slides/views/slide_channel_views.xml`
