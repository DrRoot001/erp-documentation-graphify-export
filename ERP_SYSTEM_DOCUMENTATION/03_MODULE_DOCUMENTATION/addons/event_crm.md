# Module: event_crm

- **Module ID:** MOD-067
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/event_crm`
- **Manifest:** `addons/event_crm/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Events`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Create leads from event registrations.

**Scope evidence:** The module contains 74 files, including 14 Python, 9 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `event`, `crm`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 9
- Browser asset files: 1
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 6
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/event_crm/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 45 methods, 0 constraint handlers, 1 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/event_crm/models/event_question_answer.py:4`, `addons/event_crm/models/event_lead_request.py:6`, `addons/event_crm/models/event_lead_rule.py:10`, `addons/event_crm/models/event_event.py:8`, `addons/event_crm/models/event_registration.py:9`, `addons/event_crm/models/crm_lead.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 9 XML files and 1 JavaScript/TypeScript files; static XML analysis found 18 record/template/menu identifiers.
- **Evidence:** `addons/event_crm/data/ir_action_data.xml:4`, `addons/event_crm/data/event_crm_demo.xml:5`, `addons/event_crm/data/event_crm_demo.xml:13`, `addons/event_crm/data/event_crm_demo.xml:19`, `addons/event_crm/data/ir_cron_data.xml:5`, `addons/event_crm/data/crm_lead_merge_template.xml:4`, `addons/event_crm/views/event_lead_rule_views.xml:4`, `addons/event_crm/views/event_lead_rule_views.xml:18`, `addons/event_crm/views/event_lead_rule_views.xml:33`, `addons/event_crm/views/event_lead_rule_views.xml:84`, `addons/event_crm/views/event_lead_rule_views.xml:94`, `addons/event_crm/views/event_lead_rule_views.xml:100`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/event_crm/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 6 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/event_crm/__manifest__.py`, `addons/event_crm/models/event_lead_request.py`, `addons/event_crm/models/event_event.py`, `addons/event_crm/data/ir_action_data.xml`, `addons/event_crm/data/ir_cron_data.xml`, `addons/event_crm/tests/test_event_crm_flow.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/event_crm/tests/common.py`, `addons/event_crm/tests/test_event_crm_flow.py`, `addons/event_crm/tests/test_crm_lead_merge.py`, `addons/event_crm/tests/test_event_crm_http.py`, `addons/event_crm/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 9; representative identifiers: `action_generate_leads`, `event_lead_rule_0`, `event_registration_0_rule_0`, `event_registration_1_rule_0`, `ir_cron_generate_leads`, `crm_lead_merge_summary_inherit_event_crm`, `event_lead_rule_view_search`, `event_lead_rule_view_tree`, `event_lead_rule_view_form`, `event_lead_rule_action`, `event_lead_rule_answer_action`, `event_lead_rule_menu`, `event_registration_action_from_lead`, `crm_lead_view_form`, `event_registration_view_form`, `event_view_form`, `event_view_tree`, `event_question_view_form`
- Menus: 1; representative evidence: `addons/event_crm/views/event_lead_rule_views.xml:100`
- Templates: 1; representative evidence: `addons/event_crm/data/crm_lead_merge_template.xml:4`
- View/action field declarations: 22; representative evidence: `addons/event_crm/views/event_lead_rule_views.xml:6`, `addons/event_crm/views/event_lead_rule_views.xml:7`, `addons/event_crm/views/event_lead_rule_views.xml:20`, `addons/event_crm/views/event_lead_rule_views.xml:21`, `addons/event_crm/views/event_lead_rule_views.xml:35`, `addons/event_crm/views/event_lead_rule_views.xml:36`, `addons/event_crm/views/event_lead_rule_views.xml:86`, `addons/event_crm/views/event_lead_rule_views.xml:87`, `addons/event_crm/views/event_lead_rule_views.xml:96`, `addons/event_crm/views/event_lead_rule_views.xml:97`, `addons/event_crm/views/crm_lead_views.xml:5`, `addons/event_crm/views/crm_lead_views.xml:6`
- Browser assets: 1; representative files: `addons/event_crm/static/tests/tours/event_question_answers_rule_creation_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/event_crm/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/event_crm/__manifest__.py`, `addons/event_crm/models/event_lead_request.py`, `addons/event_crm/models/event_event.py`, `addons/event_crm/data/ir_action_data.xml`, `addons/event_crm/data/ir_cron_data.xml`, `addons/event_crm/tests/test_event_crm_flow.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `event.question.answer` (addons/event_crm/models/event_question_answer.py:4); `event.lead.request` (addons/event_crm/models/event_lead_request.py:6); `event.lead.rule` (addons/event_crm/models/event_lead_rule.py:10); inherits `event.event` (addons/event_crm/models/event_event.py:8); inherits `event.registration` (addons/event_crm/models/event_registration.py:9); inherits `crm.lead` (addons/event_crm/models/crm_lead.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `event`, `crm`
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

- `addons/event_crm/__init__.py`
- `addons/event_crm/__manifest__.py`
- `addons/event_crm/data/crm_lead_merge_template.xml`
- `addons/event_crm/data/event_crm_demo.xml`
- `addons/event_crm/data/ir_action_data.xml`
- `addons/event_crm/data/ir_cron_data.xml`
- `addons/event_crm/i18n/ar.po`
- `addons/event_crm/i18n/az.po`
- `addons/event_crm/i18n/bg.po`
- `addons/event_crm/i18n/bs.po`
- `addons/event_crm/i18n/ca.po`
- `addons/event_crm/i18n/cs.po`
- `addons/event_crm/i18n/da.po`
- `addons/event_crm/i18n/de.po`
- `addons/event_crm/i18n/el.po`
- `addons/event_crm/i18n/es.po`
- `addons/event_crm/i18n/es_419.po`
- `addons/event_crm/i18n/et.po`
- `addons/event_crm/i18n/event_crm.pot`
- `addons/event_crm/i18n/fa.po`
- `addons/event_crm/i18n/fi.po`
- `addons/event_crm/i18n/fr.po`
- `addons/event_crm/i18n/he.po`
- `addons/event_crm/i18n/hi.po`
- `addons/event_crm/i18n/hr.po`
- `addons/event_crm/i18n/hu.po`
- `addons/event_crm/i18n/id.po`
- `addons/event_crm/i18n/it.po`
- `addons/event_crm/i18n/ja.po`
- `addons/event_crm/i18n/kab.po`
- `addons/event_crm/i18n/ko.po`
- `addons/event_crm/i18n/ku.po`
- `addons/event_crm/i18n/lo.po`
- `addons/event_crm/i18n/lt.po`
- `addons/event_crm/i18n/lv.po`
- `addons/event_crm/i18n/mn.po`
- `addons/event_crm/i18n/my.po`
- `addons/event_crm/i18n/nb.po`
- `addons/event_crm/i18n/nl.po`
- `addons/event_crm/i18n/pl.po`
- `addons/event_crm/i18n/pt.po`
- `addons/event_crm/i18n/pt_BR.po`
- `addons/event_crm/i18n/ro.po`
- `addons/event_crm/i18n/ru.po`
- `addons/event_crm/i18n/sk.po`
- `addons/event_crm/i18n/sl.po`
- `addons/event_crm/i18n/sr@latin.po`
- `addons/event_crm/i18n/sv.po`
- `addons/event_crm/i18n/th.po`
- `addons/event_crm/i18n/tr.po`
- `addons/event_crm/i18n/uk.po`
- `addons/event_crm/i18n/uz.po`
- `addons/event_crm/i18n/vi.po`
- `addons/event_crm/i18n/zh_CN.po`
- `addons/event_crm/i18n/zh_TW.po`
- `addons/event_crm/models/__init__.py`
- `addons/event_crm/models/crm_lead.py`
- `addons/event_crm/models/event_event.py`
- `addons/event_crm/models/event_lead_request.py`
- `addons/event_crm/models/event_lead_rule.py`
- `addons/event_crm/models/event_question_answer.py`
- `addons/event_crm/models/event_registration.py`
- `addons/event_crm/security/ir.access.csv`
- `addons/event_crm/static/tests/tours/event_question_answers_rule_creation_tour.js`
- `addons/event_crm/tests/__init__.py`
- `addons/event_crm/tests/common.py`
- `addons/event_crm/tests/test_crm_lead_merge.py`
- `addons/event_crm/tests/test_event_crm_flow.py`
- `addons/event_crm/tests/test_event_crm_http.py`
- `addons/event_crm/views/crm_lead_views.xml`
- `addons/event_crm/views/event_event_views.xml`
- `addons/event_crm/views/event_lead_rule_views.xml`
- `addons/event_crm/views/event_question_views.xml`
- `addons/event_crm/views/event_registration_views.xml`
