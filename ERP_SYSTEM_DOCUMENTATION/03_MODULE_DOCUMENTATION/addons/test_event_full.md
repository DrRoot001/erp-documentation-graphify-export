# Module: test_event_full

- **Module ID:** MOD-572
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/test_event_full`
- **Manifest:** `addons/test_event_full/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tests`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module will test the main event flows of Odoo, both frontend and backend.
It installs sale capabilities, front-end flow, eCommerce, questions and
automatic lead generation, full Online support, ...

**Scope evidence:** The module contains 18 files, including 12 Python, 2 XML, and 4 JavaScript/TypeScript files. The manifest declares dependencies: `event`, `event_booth`, `event_crm`, `event_crm_sale`, `event_sale`, `event_sms`, `payment_demo`, `website_event_booth_sale_exhibitor`, `website_event_exhibitor`, `website_event_sale`, `website_event_track`, `website_event_track_live`, `website_event_track_quiz`.

## 2. Module structure

- Model/business logic files: 0
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 4
- Security files: 0
- Test files: 10
- Scheduled/automation evidence files: 2
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### User interface and data

- **Description:** 2 XML files and 4 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/test_event_full/data/ir_actions_report_data.xml:3`, `addons/test_event_full/views/event_registration_templates_reports.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/test_event_full/tests/test_event_mail.py`, `addons/test_event_full/tests/common.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/test_event_full/data/ir_actions_report_data.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 10 test files are present.
- **Evidence:** `addons/test_event_full/tests/test_event_event.py`, `addons/test_event_full/tests/test_event_portal.py`, `addons/test_event_full/tests/test_performance.py`, `addons/test_event_full/tests/test_wevent_register.py`, `addons/test_event_full/tests/test_event_crm.py`, `addons/test_event_full/tests/test_wevent_menu.py`, `addons/test_event_full/tests/test_event_mail.py`, `addons/test_event_full/tests/common.py`, `addons/test_event_full/tests/__init__.py`, `addons/test_event_full/tests/test_event_security.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `event_registration_report_test`, `event_registration_template_report`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/test_event_full/views/event_registration_templates_reports.xml:3`
- View/action field declarations: 1; representative evidence: `addons/test_event_full/data/ir_actions_report_data.xml:5`
- Browser assets: 4; representative files: `addons/test_event_full/static/src/js/tours/wevent_performance_tour.js`, `addons/test_event_full/static/src/js/tours/event_portal_tour.js`, `addons/test_event_full/static/src/js/tours/wevent_register_tour.js`, `addons/test_event_full/static/src/js/tests/test_template_reference_field_widget.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/test_event_full/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/test_event_full/tests/test_event_mail.py`, `addons/test_event_full/tests/common.py`
- **Report entry points:** `addons/test_event_full/data/ir_actions_report_data.xml`

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `event`, `event_booth`, `event_crm`, `event_crm_sale`, `event_sale`, `event_sms`, `payment_demo`, `website_event_booth_sale_exhibitor`, `website_event_exhibitor`, `website_event_sale`, `website_event_track`, `website_event_track_live`, `website_event_track_quiz`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Not found
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/test_event_full/__init__.py`
- `addons/test_event_full/__manifest__.py`
- `addons/test_event_full/data/ir_actions_report_data.xml`
- `addons/test_event_full/static/src/js/tests/test_template_reference_field_widget.test.js`
- `addons/test_event_full/static/src/js/tours/event_portal_tour.js`
- `addons/test_event_full/static/src/js/tours/wevent_performance_tour.js`
- `addons/test_event_full/static/src/js/tours/wevent_register_tour.js`
- `addons/test_event_full/tests/__init__.py`
- `addons/test_event_full/tests/common.py`
- `addons/test_event_full/tests/test_event_crm.py`
- `addons/test_event_full/tests/test_event_event.py`
- `addons/test_event_full/tests/test_event_mail.py`
- `addons/test_event_full/tests/test_event_portal.py`
- `addons/test_event_full/tests/test_event_security.py`
- `addons/test_event_full/tests/test_performance.py`
- `addons/test_event_full/tests/test_wevent_menu.py`
- `addons/test_event_full/tests/test_wevent_register.py`
- `addons/test_event_full/views/event_registration_templates_reports.xml`
