# Module: test_mass_mailing

- **Module ID:** MOD-578
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/test_mass_mailing`
- **Manifest:** `addons/test_mass_mailing/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Email Marketing`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Mass Mail Tests: feature and performance tests for mass mailing

**Manifest description:**

This module contains tests related to mass mailing. Those
are present in a separate module to use specific test models defined in
test_mail.

**Scope evidence:** The module contains 27 files, including 26 Python, 0 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `mail_tracking_mass_mailing`, `mass_mailing`, `mass_mailing_sms`, `sms_twilio`, `test_mail`, `test_mail_sms`.

## 2. Module structure

- Model/business logic files: 10
- Controller/API files: 0
- XML/data/view/template files: 0
- Browser asset files: 0
- Security files: 1
- Test files: 18
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/test_mass_mailing/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 10 model declarations, 106 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/test_mass_mailing/models/mailing_models.py:7`, `addons/test_mass_mailing/models/mailing_models.py:27`, `addons/test_mass_mailing/models/mailing_models.py:39`, `addons/test_mass_mailing/models/mailing_models.py:49`, `addons/test_mass_mailing/models/mailing_models.py:67`, `addons/test_mass_mailing/models/mailing_models.py:93`, `addons/test_mass_mailing/models/mailing_models.py:104`, `addons/test_mass_mailing/models/mailing_models.py:115`, `addons/test_mass_mailing/models/ir_qweb.py:5`, `addons/test_mass_mailing/models/mailing_models_cornercase.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/test_mass_mailing/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/test_mass_mailing/tests/test_mailing_test.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 18 test files are present.
- **Evidence:** `addons/test_mass_mailing/tests/test_link_tracker.py`, `addons/test_mass_mailing/tests/test_link_tracker_sms.py`, `addons/test_mass_mailing/tests/test_mail_message.py`, `addons/test_mass_mailing/tests/test_performance.py`, `addons/test_mass_mailing/tests/test_blacklist_mixin.py`, `addons/test_mass_mailing/tests/test_mailing_statistics_sms.py`, `addons/test_mass_mailing/tests/test_blacklist_behavior.py`, `addons/test_mass_mailing/tests/test_blacklist.py`, `addons/test_mass_mailing/tests/test_mailing_statistics.py`, `addons/test_mass_mailing/tests/common.py`, `addons/test_mass_mailing/tests/test_mailing_list.py`, `addons/test_mass_mailing/tests/test_mailing_server.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 0; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/test_mass_mailing/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/test_mass_mailing/tests/test_mailing_test.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 10
- Representative model evidence: `mailing.test.customer` (addons/test_mass_mailing/models/mailing_models.py:7); `mailing.test.simple` (addons/test_mass_mailing/models/mailing_models.py:27); `mailing.test.utm` (addons/test_mass_mailing/models/mailing_models.py:39); `mailing.test.blacklist` (addons/test_mass_mailing/models/mailing_models.py:49); `mailing.test.optout` (addons/test_mass_mailing/models/mailing_models.py:67); `mailing.test.partner` (addons/test_mass_mailing/models/mailing_models.py:93); `mailing.performance` (addons/test_mass_mailing/models/mailing_models.py:104); `mailing.performance.blacklist` (addons/test_mass_mailing/models/mailing_models.py:115); inherits `ir.qweb` (addons/test_mass_mailing/models/ir_qweb.py:5); `mailing.test.partner.unstored` (addons/test_mass_mailing/models/mailing_models_cornercase.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mail_tracking_mass_mailing`, `mass_mailing`, `mass_mailing_sms`, `sms_twilio`, `test_mail`, `test_mail_sms`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Not found
- **API evidence:** Not found
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/test_mass_mailing/__init__.py`
- `addons/test_mass_mailing/__manifest__.py`
- `addons/test_mass_mailing/data/__init__.py`
- `addons/test_mass_mailing/data/mail_test_data.py`
- `addons/test_mass_mailing/models/__init__.py`
- `addons/test_mass_mailing/models/ir_qweb.py`
- `addons/test_mass_mailing/models/mailing_models.py`
- `addons/test_mass_mailing/models/mailing_models_cornercase.py`
- `addons/test_mass_mailing/security/ir.access.csv`
- `addons/test_mass_mailing/tests/__init__.py`
- `addons/test_mass_mailing/tests/common.py`
- `addons/test_mass_mailing/tests/test_blacklist.py`
- `addons/test_mass_mailing/tests/test_blacklist_behavior.py`
- `addons/test_mass_mailing/tests/test_blacklist_mixin.py`
- `addons/test_mass_mailing/tests/test_link_tracker.py`
- `addons/test_mass_mailing/tests/test_link_tracker_sms.py`
- `addons/test_mass_mailing/tests/test_mail_composer.py`
- `addons/test_mass_mailing/tests/test_mail_message.py`
- `addons/test_mass_mailing/tests/test_mailing.py`
- `addons/test_mass_mailing/tests/test_mailing_list.py`
- `addons/test_mass_mailing/tests/test_mailing_server.py`
- `addons/test_mass_mailing/tests/test_mailing_sms.py`
- `addons/test_mass_mailing/tests/test_mailing_statistics.py`
- `addons/test_mass_mailing/tests/test_mailing_statistics_sms.py`
- `addons/test_mass_mailing/tests/test_mailing_test.py`
- `addons/test_mass_mailing/tests/test_performance.py`
- `addons/test_mass_mailing/tests/test_sms_controller.py`
