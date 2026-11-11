# Module: test_mail

- **Module ID:** MOD-575
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/test_mail`
- **Manifest:** `addons/test_mail/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Mail Tests: performances and tests specific to mail

**Manifest description:**

This module contains tests related to mail. Those are
present in a separate module as it contains models used only to perform
tests independently to functional aspects of other models.

**Scope evidence:** The module contains 64 files, including 43 Python, 3 XML, and 17 JavaScript/TypeScript files. The manifest declares dependencies: `mail`, `test_base`, `phone_validation`, `mail_tracking`.

## 2. Module structure

- Model/business logic files: 48
- Controller/API files: 0
- XML/data/view/template files: 3
- Browser asset files: 17
- Security files: 1
- Test files: 36
- Scheduled/automation evidence files: 5
- Reporting evidence files: 4

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/test_mail/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 48 model declarations, 751 methods, 0 constraint handlers, 0 onchange handlers, and 7 dependency declarations.
- **Evidence:** `addons/test_mail/models/test_mail_corner_case_models.py:7`, `addons/test_mail/models/test_mail_corner_case_models.py:24`, `addons/test_mail/models/test_mail_corner_case_models.py:37`, `addons/test_mail/models/test_mail_corner_case_models.py:48`, `addons/test_mail/models/test_mail_corner_case_models.py:73`, `addons/test_mail/models/test_mail_corner_case_models.py:100`, `addons/test_mail/models/test_mail_corner_case_models.py:124`, `addons/test_mail/models/test_mail_corner_case_models.py:132`, `addons/test_mail/models/test_mail_corner_case_models.py:141`, `addons/test_mail/models/test_mail_corner_case_models.py:149`, `addons/test_mail/models/test_mail_corner_case_models.py:185`, `addons/test_mail/models/test_mail_corner_case_models.py:196`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 17 JavaScript/TypeScript files; static XML analysis found 19 record/template/menu identifiers.
- **Evidence:** `addons/test_mail/data/mail_template_data.xml:3`, `addons/test_mail/data/mail_template_data.xml:13`, `addons/test_mail/data/mail_template_data.xml:23`, `addons/test_mail/data/mail_template_data.xml:27`, `addons/test_mail/data/mail_template_data.xml:37`, `addons/test_mail/data/mail_template_data.xml:47`, `addons/test_mail/data/mail_template_data.xml:60`, `addons/test_mail/data/data.xml:4`, `addons/test_mail/data/data.xml:10`, `addons/test_mail/data/data.xml:16`, `addons/test_mail/data/data.xml:22`, `addons/test_mail/data/data.xml:30`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/test_mail/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 5 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/test_mail/tests/test_message_post.py`, `addons/test_mail/tests/test_ir_actions.py`, `addons/test_mail/tests/test_mail_push.py`, `addons/test_mail/tests/test_mail_composer.py`, `addons/test_mail/tests/test_mail_scheduled_message.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 4 files contain report-action/template indicators.
- **Evidence:** `addons/test_mail/tests/test_mail_template.py`, `addons/test_mail/tests/test_mail_template_preview.py`, `addons/test_mail/tests/test_mail_composer.py`, `addons/test_mail/tests/test_mail_thread_internals.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 36 test files are present.
- **Evidence:** `addons/test_mail/models/test_mail_corner_case_models.py`, `addons/test_mail/models/test_mail_feature_models.py`, `addons/test_mail/models/test_mail_models.py`, `addons/test_mail/data/test_mail_data.py`, `addons/test_mail/tests/test_mail_alias.py`, `addons/test_mail/tests/test_mail_message.py`, `addons/test_mail/tests/test_mail_message_security.py`, `addons/test_mail/tests/test_mail_security.py`, `addons/test_mail/tests/test_mail_followers.py`, `addons/test_mail/tests/test_controller_binary.py`, `addons/test_mail/tests/test_mail_template.py`, `addons/test_mail/tests/test_performance.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `mail_test_ticket_tracking_tpl`, `mail_test_container_tpl`, `mail_test_ticket_tracking_view`, `mail_test_ticket_test_template`, `mail_test_ticket_test_template_2`, `mail_test_ticket_test_variable_template`, `mail_template_simple_test`, `mail_act_test_todo`, `mail_act_test_meeting`, `mail_act_test_call`, `mail_act_test_upload_document`, `mail_act_test_todo_generic`, `st_mail_test_simple_external`, `st_mail_test_ticket_container_upd`, `st_mail_test_container_default`, `st_mail_test_container_child_full`, `st_mail_test_ticket_container_mc_upd`, `st_mail_test_ticket_internal`, `st_mail_test_ticket_partner_new`
- Menus: 0; representative evidence: Not found in module
- Templates: 5; representative evidence: `addons/test_mail/data/mail_template_data.xml:23`, `addons/test_mail/data/mail_template_data.xml:27`, `addons/test_mail/data/mail_template_data.xml:37`, `addons/test_mail/data/mail_template_data.xml:47`, `addons/test_mail/data/mail_template_data.xml:60`
- View/action field declarations: 11; representative evidence: `addons/test_mail/data/data.xml:8`, `addons/test_mail/data/data.xml:14`, `addons/test_mail/data/data.xml:20`, `addons/test_mail/data/data.xml:27`, `addons/test_mail/data/subtype_data.xml:8`, `addons/test_mail/data/subtype_data.xml:17`, `addons/test_mail/data/subtype_data.xml:25`, `addons/test_mail/data/subtype_data.xml:32`, `addons/test_mail/data/subtype_data.xml:43`, `addons/test_mail/data/subtype_data.xml:50`, `addons/test_mail/data/subtype_data.xml:59`
- Browser assets: 17; representative files: `addons/test_mail/static/tests/attachment_view.test.js`, `addons/test_mail/static/tests/properties_field.test.js`, `addons/test_mail/static/tests/activity_mobile.test.js`, `addons/test_mail/static/tests/activity.test.js`, `addons/test_mail/static/tests/test_mail_test_helpers.js`, `addons/test_mail/static/tests/chatter.test.js`, `addons/test_mail/static/tests/systray_activity_menu.test.js`, `addons/test_mail/static/tests/tours/mail_activity_view_tour.js`, `addons/test_mail/static/tests/tours/access_inbox_records_tour.js`, `addons/test_mail/static/tests/mock_server/models/mail_test_multi_company_read.js`, `addons/test_mail/static/tests/mock_server/models/mail_test_multi_company.js`, `addons/test_mail/static/tests/mock_server/models/mail_test_simple_main_attachment.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/test_mail/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/test_mail/tests/test_message_post.py`, `addons/test_mail/tests/test_ir_actions.py`, `addons/test_mail/tests/test_mail_push.py`, `addons/test_mail/tests/test_mail_composer.py`, `addons/test_mail/tests/test_mail_scheduled_message.py`
- **Report entry points:** `addons/test_mail/tests/test_mail_template.py`, `addons/test_mail/tests/test_mail_template_preview.py`, `addons/test_mail/tests/test_mail_composer.py`, `addons/test_mail/tests/test_mail_thread_internals.py`

## 7. Database interactions

- Model declarations: 48
- Representative model evidence: `mail.performance.thread` (addons/test_mail/models/test_mail_corner_case_models.py:7); `mail.performance.thread.recipients` (addons/test_mail/models/test_mail_corner_case_models.py:24); `mail.performance.tracking` (addons/test_mail/models/test_mail_corner_case_models.py:37); `mail.test.field.type` (addons/test_mail/models/test_mail_corner_case_models.py:48); `mail.test.lang` (addons/test_mail/models/test_mail_corner_case_models.py:73); `mail.test.track` (addons/test_mail/models/test_mail_corner_case_models.py:100); `mail.test.track.all.m2m` (addons/test_mail/models/test_mail_corner_case_models.py:124); `mail.test.track.all.o2m` (addons/test_mail/models/test_mail_corner_case_models.py:132); `mail.test.track.all.properties.parent` (addons/test_mail/models/test_mail_corner_case_models.py:141); `mail.test.track.all` (addons/test_mail/models/test_mail_corner_case_models.py:149); `mail.test.track.compute` (addons/test_mail/models/test_mail_corner_case_models.py:185); `mail.test.track.duration.mixin` (addons/test_mail/models/test_mail_corner_case_models.py:196); `mail.test.track.duration.mixin.stage` (addons/test_mail/models/test_mail_corner_case_models.py:219); `mail.test.track.groups` (addons/test_mail/models/test_mail_corner_case_models.py:227); `mail.test.track.mixin` (addons/test_mail/models/test_mail_corner_case_models.py:237); `mail.test.track.monetary` (addons/test_mail/models/test_mail_corner_case_models.py:267); `mail.test.track.selection` (addons/test_mail/models/test_mail_corner_case_models.py:277); `mail.test.multi.company` (addons/test_mail/models/test_mail_corner_case_models.py:292); `mail.test.multi.company.read` (addons/test_mail/models/test_mail_corner_case_models.py:303); `mail.test.multi.company.with.activity` (addons/test_mail/models/test_mail_corner_case_models.py:312); `mail.test.nothread` (addons/test_mail/models/test_mail_corner_case_models.py:322); `mail.test.ticket` (addons/test_mail/models/mail_test_ticket.py:7); `mail.test.ticket.el` (addons/test_mail/models/mail_test_ticket.py:90); `mail.test.ticket.mc` (addons/test_mail/models/mail_test_ticket.py:112); `mail.test.ticket.partner` (addons/test_mail/models/mail_test_ticket.py:158); `mail.test.container` (addons/test_mail/models/mail_test_ticket.py:214); `mail.test.container.mc` (addons/test_mail/models/mail_test_ticket.py:248); `mail.test.recipients` (addons/test_mail/models/test_mail_feature_models.py:9); `mail.test.thread.customer` (addons/test_mail/models/test_mail_feature_models.py:37); `mail.test.properties` (addons/test_mail/models/test_mail_feature_models.py:49)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mail`, `test_base`, `phone_validation`, `mail_tracking`
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

- `addons/test_mail/__init__.py`
- `addons/test_mail/__manifest__.py`
- `addons/test_mail/data/__init__.py`
- `addons/test_mail/data/data.xml`
- `addons/test_mail/data/mail_template_data.xml`
- `addons/test_mail/data/subtype_data.xml`
- `addons/test_mail/data/test_mail_data.py`
- `addons/test_mail/models/__init__.py`
- `addons/test_mail/models/mail_test_access.py`
- `addons/test_mail/models/mail_test_lead.py`
- `addons/test_mail/models/mail_test_ticket.py`
- `addons/test_mail/models/test_mail_corner_case_models.py`
- `addons/test_mail/models/test_mail_feature_models.py`
- `addons/test_mail/models/test_mail_models.py`
- `addons/test_mail/security/ir.access.csv`
- `addons/test_mail/static/tests/activity.test.js`
- `addons/test_mail/static/tests/activity_mobile.test.js`
- `addons/test_mail/static/tests/attachment_view.test.js`
- `addons/test_mail/static/tests/chatter.test.js`
- `addons/test_mail/static/tests/mock_server/models/mail_test_activity.js`
- `addons/test_mail/static/tests/mock_server/models/mail_test_multi_company.js`
- `addons/test_mail/static/tests/mock_server/models/mail_test_multi_company_read.js`
- `addons/test_mail/static/tests/mock_server/models/mail_test_properties.js`
- `addons/test_mail/static/tests/mock_server/models/mail_test_simple.js`
- `addons/test_mail/static/tests/mock_server/models/mail_test_simple_main_attachment.js`
- `addons/test_mail/static/tests/mock_server/models/mail_test_track_all.js`
- `addons/test_mail/static/tests/mock_server/models/res_currency.js`
- `addons/test_mail/static/tests/properties_field.test.js`
- `addons/test_mail/static/tests/systray_activity_menu.test.js`
- `addons/test_mail/static/tests/test_mail_test_helpers.js`
- `addons/test_mail/static/tests/tours/access_inbox_records_tour.js`
- `addons/test_mail/static/tests/tours/mail_activity_view_tour.js`
- `addons/test_mail/tests/__init__.py`
- `addons/test_mail/tests/common.py`
- `addons/test_mail/tests/test_controller_attachment.py`
- `addons/test_mail/tests/test_controller_binary.py`
- `addons/test_mail/tests/test_controller_thread.py`
- `addons/test_mail/tests/test_invite.py`
- `addons/test_mail/tests/test_ir_actions.py`
- `addons/test_mail/tests/test_ir_attachment.py`
- `addons/test_mail/tests/test_mail_activity.py`
- `addons/test_mail/tests/test_mail_activity_mixin.py`
- `addons/test_mail/tests/test_mail_activity_plan.py`
- `addons/test_mail/tests/test_mail_alias.py`
- `addons/test_mail/tests/test_mail_composer.py`
- `addons/test_mail/tests/test_mail_composer_mixin.py`
- `addons/test_mail/tests/test_mail_flow.py`
- `addons/test_mail/tests/test_mail_followers.py`
- `addons/test_mail/tests/test_mail_gateway.py`
- `addons/test_mail/tests/test_mail_mail.py`
- `addons/test_mail/tests/test_mail_management.py`
- `addons/test_mail/tests/test_mail_message.py`
- `addons/test_mail/tests/test_mail_message_security.py`
- `addons/test_mail/tests/test_mail_multicompany.py`
- `addons/test_mail/tests/test_mail_push.py`
- `addons/test_mail/tests/test_mail_scheduled_message.py`
- `addons/test_mail/tests/test_mail_security.py`
- `addons/test_mail/tests/test_mail_template.py`
- `addons/test_mail/tests/test_mail_template_preview.py`
- `addons/test_mail/tests/test_mail_thread_internals.py`
- `addons/test_mail/tests/test_mail_thread_mixins.py`
- `addons/test_mail/tests/test_message_post.py`
- `addons/test_mail/tests/test_message_track.py`
- `addons/test_mail/tests/test_performance.py`
