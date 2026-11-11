# Module: test_mail_full

- **Module ID:** MOD-576
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/test_mail_full`
- **Manifest:** `addons/test_mail_full/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Mail Tests: performances and tests specific to mail with all sub-modules

**Manifest description:**

This module contains tests related to various mail features
and mail-related sub modules. Those tests are present in a separate module as it
contains models used only to perform tests independently to functional aspects of
real applications.

**Scope evidence:** The module contains 36 files, including 21 Python, 2 XML, and 11 JavaScript/TypeScript files. The manifest declares dependencies: `mail`, `mail_bot`, `mail_tracking_mass_mailing`, `mass_mailing`, `mass_mailing_sms`, `phone_validation`, `portal`, `rating`, `sms`, `test_mail`, `test_mail_sms`, `test_mass_mailing`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 2
- XML/data/view/template files: 2
- Browser asset files: 11
- Security files: 1
- Test files: 16
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/test_mail_full/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 99 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/test_mail_full/models/test_mail_models_mail.py:7`, `addons/test_mail_full/models/test_mail_models_mail.py:27`, `addons/test_mail_full/models/test_mail_models_mail.py:44`, `addons/test_mail_full/models/test_mail_models_mail.py:55`, `addons/test_mail_full/models/test_mail_models_mail.py:79`, `addons/test_mail_full/models/test_mail_models_mail.py:133`, `addons/test_mail_full/models/test_mail_models_mail.py:156`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 5 route declarations.
- **Evidence:** `addons/test_mail_full/controllers/portal.py:8`, `addons/test_mail_full/controllers/portal.py:12`, `addons/test_mail_full/controllers/portal.py:23`, `addons/test_mail_full/controllers/portal.py:40`, `addons/test_mail_full/controllers/portal.py:44`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 11 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/test_mail_full/data/mail_message_subtype_data.xml:3`, `addons/test_mail_full/views/test_portal_template.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/test_mail_full/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 16 test files are present.
- **Evidence:** `addons/test_mail_full/models/test_mail_models_mail.py`, `addons/test_mail_full/tests/test_res_users.py`, `addons/test_mail_full/tests/test_rating.py`, `addons/test_mail_full/tests/test_ir_mail_server.py`, `addons/test_mail_full/tests/test_controller_attachment.py`, `addons/test_mail_full/tests/test_controller_update.py`, `addons/test_mail_full/tests/common.py`, `addons/test_mail_full/tests/test_portal.py`, `addons/test_mail_full/tests/test_ui.py`, `addons/test_mail_full/tests/test_mail_performance.py`, `addons/test_mail_full/tests/__init__.py`, `addons/test_mail_full/tests/test_mail_thread_internals.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `mt_mail_test_rating_rating_done`, `Test Portal`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/test_mail_full/views/test_portal_template.xml:4`
- View/action field declarations: 1; representative evidence: `addons/test_mail_full/data/mail_message_subtype_data.xml:6`
- Browser assets: 11; representative files: `addons/test_mail_full/static/tests/messaging_menu_patch.test.js`, `addons/test_mail_full/static/tests/test_mail_full_test_helpers.js`, `addons/test_mail_full/static/tests/tours/portal_rating_pagination_tour.js`, `addons/test_mail_full/static/tests/tours/portal_copy_link_tour.js`, `addons/test_mail_full/static/tests/tours/message_actions_tour.js`, `addons/test_mail_full/static/tests/tours/portal_composer_actions_tour.js`, `addons/test_mail_full/static/tests/tours/portal_message_highlight_tour.js`, `addons/test_mail_full/static/tests/tours/portal_rating_tour.js.js`, `addons/test_mail_full/static/tests/tours/load_more_tour.js`, `addons/test_mail_full/static/tests/tours/portal_no_copy_link_tour.js`, `addons/test_mail_full/static/tests/mock_server/models/mail_test_rating.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/test_mail_full/__manifest__.py`
- **HTTP entry points:** `addons/test_mail_full/controllers/portal.py:8`, `addons/test_mail_full/controllers/portal.py:12`, `addons/test_mail_full/controllers/portal.py:23`, `addons/test_mail_full/controllers/portal.py:40`, `addons/test_mail_full/controllers/portal.py:44`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: `mail.test.portal` (addons/test_mail_full/models/test_mail_models_mail.py:7); `mail.test.portal.no.partner` (addons/test_mail_full/models/test_mail_models_mail.py:27); `mail.test.portal.no.access` (addons/test_mail_full/models/test_mail_models_mail.py:44); `mail.test.portal.public.access.action` (addons/test_mail_full/models/test_mail_models_mail.py:55); `mail.test.rating` (addons/test_mail_full/models/test_mail_models_mail.py:79); `mail.test.rating.thread` (addons/test_mail_full/models/test_mail_models_mail.py:133); `mail.test.rating.thread.read` (addons/test_mail_full/models/test_mail_models_mail.py:156)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 5
- Route evidence: `addons/test_mail_full/controllers/portal.py:8`, `addons/test_mail_full/controllers/portal.py:12`, `addons/test_mail_full/controllers/portal.py:23`, `addons/test_mail_full/controllers/portal.py:40`, `addons/test_mail_full/controllers/portal.py:44`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mail`, `mail_bot`, `mail_tracking_mass_mailing`, `mass_mailing`, `mass_mailing_sms`, `phone_validation`, `portal`, `rating`, `sms`, `test_mail`, `test_mail_sms`, `test_mass_mailing`
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

- `addons/test_mail_full/__init__.py`
- `addons/test_mail_full/__manifest__.py`
- `addons/test_mail_full/controllers/__init__.py`
- `addons/test_mail_full/controllers/portal.py`
- `addons/test_mail_full/data/mail_message_subtype_data.xml`
- `addons/test_mail_full/i18n/test_mail_full.pot`
- `addons/test_mail_full/models/__init__.py`
- `addons/test_mail_full/models/test_mail_models_mail.py`
- `addons/test_mail_full/security/ir.access.csv`
- `addons/test_mail_full/static/tests/messaging_menu_patch.test.js`
- `addons/test_mail_full/static/tests/mock_server/models/mail_test_rating.js`
- `addons/test_mail_full/static/tests/test_mail_full_test_helpers.js`
- `addons/test_mail_full/static/tests/tours/load_more_tour.js`
- `addons/test_mail_full/static/tests/tours/message_actions_tour.js`
- `addons/test_mail_full/static/tests/tours/portal_composer_actions_tour.js`
- `addons/test_mail_full/static/tests/tours/portal_copy_link_tour.js`
- `addons/test_mail_full/static/tests/tours/portal_message_highlight_tour.js`
- `addons/test_mail_full/static/tests/tours/portal_no_copy_link_tour.js`
- `addons/test_mail_full/static/tests/tours/portal_rating_pagination_tour.js`
- `addons/test_mail_full/static/tests/tours/portal_rating_tour.js.js`
- `addons/test_mail_full/tests/__init__.py`
- `addons/test_mail_full/tests/common.py`
- `addons/test_mail_full/tests/test_controller_attachment.py`
- `addons/test_mail_full/tests/test_controller_reaction.py`
- `addons/test_mail_full/tests/test_controller_thread.py`
- `addons/test_mail_full/tests/test_controller_update.py`
- `addons/test_mail_full/tests/test_ir_mail_server.py`
- `addons/test_mail_full/tests/test_mail_bot.py`
- `addons/test_mail_full/tests/test_mail_performance.py`
- `addons/test_mail_full/tests/test_mail_thread_internals.py`
- `addons/test_mail_full/tests/test_mass_mailing.py`
- `addons/test_mail_full/tests/test_portal.py`
- `addons/test_mail_full/tests/test_rating.py`
- `addons/test_mail_full/tests/test_res_users.py`
- `addons/test_mail_full/tests/test_ui.py`
- `addons/test_mail_full/views/test_portal_template.xml`
