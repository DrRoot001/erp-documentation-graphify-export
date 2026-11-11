# Module: hr_skills_event

- **Module ID:** MOD-099
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_skills_event`
- **Manifest:** `addons/hr_skills_event/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Link training events to resume of your employees

**Manifest description:**

Events and Skills for HR
============================

This module add completed course events to resume for employees.

**Scope evidence:** The module contains 60 files, including 7 Python, 3 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `hr_skills`, `event`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 3
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

- **Description:** 2 model declarations, 6 methods, 0 constraint handlers, 1 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/hr_skills_event/models/hr_resume_line.py:6`, `addons/hr_skills_event/models/event_event.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 1 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/hr_skills_event/views/hr_views.xml:3`, `addons/hr_skills_event/views/hr_views.xml:9`, `addons/hr_skills_event/views/event_event_views.xml:3`, `addons/hr_skills_event/views/hr_resume_line_views.xml:3`, `addons/hr_skills_event/views/hr_resume_line_views.xml:24`, `addons/hr_skills_event/views/hr_resume_line_views.xml:41`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/hr_skills_event/tests/__init__.py`, `addons/hr_skills_event/tests/test_onsite.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `Courses`, `Onsite`, `event_training_onsite_action`, `resume_slides_line_view_form`, `resume_slides_line_view_list`, `resume_slides_line_view_kanban`
- Menus: 2; representative evidence: `addons/hr_skills_event/views/hr_views.xml:3`, `addons/hr_skills_event/views/hr_views.xml:9`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 8; representative evidence: `addons/hr_skills_event/views/event_event_views.xml:5`, `addons/hr_skills_event/views/event_event_views.xml:6`, `addons/hr_skills_event/views/hr_resume_line_views.xml:5`, `addons/hr_skills_event/views/hr_resume_line_views.xml:7`, `addons/hr_skills_event/views/hr_resume_line_views.xml:26`, `addons/hr_skills_event/views/hr_resume_line_views.xml:28`, `addons/hr_skills_event/views/hr_resume_line_views.xml:43`, `addons/hr_skills_event/views/hr_resume_line_views.xml:45`
- Browser assets: 1; representative files: `addons/hr_skills_event/static/tests/tours/onsite_skill_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_skills_event/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `hr.resume.line` (addons/hr_skills_event/models/hr_resume_line.py:6); inherits `event.event` (addons/hr_skills_event/models/event_event.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr_skills`, `event`
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

- `addons/hr_skills_event/__init__.py`
- `addons/hr_skills_event/__manifest__.py`
- `addons/hr_skills_event/i18n/ar.po`
- `addons/hr_skills_event/i18n/az.po`
- `addons/hr_skills_event/i18n/bg.po`
- `addons/hr_skills_event/i18n/bs.po`
- `addons/hr_skills_event/i18n/ca.po`
- `addons/hr_skills_event/i18n/cs.po`
- `addons/hr_skills_event/i18n/da.po`
- `addons/hr_skills_event/i18n/de.po`
- `addons/hr_skills_event/i18n/el.po`
- `addons/hr_skills_event/i18n/es.po`
- `addons/hr_skills_event/i18n/es_419.po`
- `addons/hr_skills_event/i18n/et.po`
- `addons/hr_skills_event/i18n/fa.po`
- `addons/hr_skills_event/i18n/fi.po`
- `addons/hr_skills_event/i18n/fr.po`
- `addons/hr_skills_event/i18n/he.po`
- `addons/hr_skills_event/i18n/hi.po`
- `addons/hr_skills_event/i18n/hr.po`
- `addons/hr_skills_event/i18n/hr_skills_event.pot`
- `addons/hr_skills_event/i18n/hu.po`
- `addons/hr_skills_event/i18n/id.po`
- `addons/hr_skills_event/i18n/it.po`
- `addons/hr_skills_event/i18n/ja.po`
- `addons/hr_skills_event/i18n/kab.po`
- `addons/hr_skills_event/i18n/ko.po`
- `addons/hr_skills_event/i18n/ku.po`
- `addons/hr_skills_event/i18n/lo.po`
- `addons/hr_skills_event/i18n/lt.po`
- `addons/hr_skills_event/i18n/lv.po`
- `addons/hr_skills_event/i18n/mn.po`
- `addons/hr_skills_event/i18n/my.po`
- `addons/hr_skills_event/i18n/nb.po`
- `addons/hr_skills_event/i18n/nl.po`
- `addons/hr_skills_event/i18n/pl.po`
- `addons/hr_skills_event/i18n/pt.po`
- `addons/hr_skills_event/i18n/pt_BR.po`
- `addons/hr_skills_event/i18n/ro.po`
- `addons/hr_skills_event/i18n/ru.po`
- `addons/hr_skills_event/i18n/sk.po`
- `addons/hr_skills_event/i18n/sl.po`
- `addons/hr_skills_event/i18n/sr@latin.po`
- `addons/hr_skills_event/i18n/sv.po`
- `addons/hr_skills_event/i18n/th.po`
- `addons/hr_skills_event/i18n/tr.po`
- `addons/hr_skills_event/i18n/uk.po`
- `addons/hr_skills_event/i18n/uz.po`
- `addons/hr_skills_event/i18n/vi.po`
- `addons/hr_skills_event/i18n/zh_CN.po`
- `addons/hr_skills_event/i18n/zh_TW.po`
- `addons/hr_skills_event/models/__init__.py`
- `addons/hr_skills_event/models/event_event.py`
- `addons/hr_skills_event/models/hr_resume_line.py`
- `addons/hr_skills_event/static/tests/tours/onsite_skill_tour.js`
- `addons/hr_skills_event/tests/__init__.py`
- `addons/hr_skills_event/tests/test_onsite.py`
- `addons/hr_skills_event/views/event_event_views.xml`
- `addons/hr_skills_event/views/hr_resume_line_views.xml`
- `addons/hr_skills_event/views/hr_views.xml`
