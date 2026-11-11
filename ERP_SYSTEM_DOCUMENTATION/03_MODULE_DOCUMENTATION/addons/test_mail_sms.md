# Module: test_mail_sms

- **Module ID:** MOD-577
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/test_mail_sms`
- **Manifest:** `addons/test_mail_sms/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** SMS Tests: performances and tests specific to SMS

**Manifest description:**

This module contains tests related to SMS. Those are
present in a separate module as it contains models used only to perform
tests independently to functional aspects of other models.

**Scope evidence:** The module contains 19 files, including 18 Python, 0 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `mail`, `mail_tracking_sms`, `sms`, `sms_twilio`, `test_base`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 0
- XML/data/view/template files: 0
- Browser asset files: 0
- Security files: 1
- Test files: 15
- Scheduled/automation evidence files: 2
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/test_mail_sms/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 144 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/test_mail_sms/models/test_mail_sms_models.py:7`, `addons/test_mail_sms/models/test_mail_sms_models.py:32`, `addons/test_mail_sms/models/test_mail_sms_models.py:60`, `addons/test_mail_sms/models/test_mail_sms_models.py:73`, `addons/test_mail_sms/models/test_mail_sms_models.py:104`, `addons/test_mail_sms/models/test_mail_sms_models.py:127`, `addons/test_mail_sms/models/test_mail_sms_models.py:153`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/test_mail_sms/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/test_mail_sms/tests/test_sms_server_actions.py`, `addons/test_mail_sms/tests/test_sms_post.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 15 test files are present.
- **Evidence:** `addons/test_mail_sms/models/test_mail_sms_models.py`, `addons/test_mail_sms/tests/test_sms_composer.py`, `addons/test_mail_sms/tests/test_sms_performance.py`, `addons/test_mail_sms/tests/test_phone_blacklist.py`, `addons/test_mail_sms/tests/test_sms_template.py`, `addons/test_mail_sms/tests/test_mail_thread_phone.py`, `addons/test_mail_sms/tests/test_sms_sms.py`, `addons/test_mail_sms/tests/test_phone_format.py`, `addons/test_mail_sms/tests/common.py`, `addons/test_mail_sms/tests/test_sms_management.py`, `addons/test_mail_sms/tests/test_sms_controller.py`, `addons/test_mail_sms/tests/test_sms_mixin.py`
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

- **Entry point evidence:** `addons/test_mail_sms/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/test_mail_sms/tests/test_sms_server_actions.py`, `addons/test_mail_sms/tests/test_sms_post.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: `mail.test.sms` (addons/test_mail_sms/models/test_mail_sms_models.py:7); `mail.test.sms.bl` (addons/test_mail_sms/models/test_mail_sms_models.py:32); `mail.test.sms.bl.activity` (addons/test_mail_sms/models/test_mail_sms_models.py:60); `mail.test.sms.bl.optout` (addons/test_mail_sms/models/test_mail_sms_models.py:73); `mail.test.sms.partner` (addons/test_mail_sms/models/test_mail_sms_models.py:104); `mail.test.sms.partner.2many` (addons/test_mail_sms/models/test_mail_sms_models.py:127); `sms.test.nothread` (addons/test_mail_sms/models/test_mail_sms_models.py:153)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mail`, `mail_tracking_sms`, `sms`, `sms_twilio`, `test_base`
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

- `addons/test_mail_sms/__init__.py`
- `addons/test_mail_sms/__manifest__.py`
- `addons/test_mail_sms/models/__init__.py`
- `addons/test_mail_sms/models/test_mail_sms_models.py`
- `addons/test_mail_sms/security/ir.access.csv`
- `addons/test_mail_sms/tests/__init__.py`
- `addons/test_mail_sms/tests/common.py`
- `addons/test_mail_sms/tests/test_mail_thread_phone.py`
- `addons/test_mail_sms/tests/test_phone_blacklist.py`
- `addons/test_mail_sms/tests/test_phone_format.py`
- `addons/test_mail_sms/tests/test_sms_composer.py`
- `addons/test_mail_sms/tests/test_sms_controller.py`
- `addons/test_mail_sms/tests/test_sms_management.py`
- `addons/test_mail_sms/tests/test_sms_mixin.py`
- `addons/test_mail_sms/tests/test_sms_performance.py`
- `addons/test_mail_sms/tests/test_sms_post.py`
- `addons/test_mail_sms/tests/test_sms_server_actions.py`
- `addons/test_mail_sms/tests/test_sms_sms.py`
- `addons/test_mail_sms/tests/test_sms_template.py`
