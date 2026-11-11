# Module: sms

- **Module ID:** MOD-539
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sms`
- **Manifest:** `addons/sms/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** SMS Text Messaging

**Manifest description:**

This module gives a framework for SMS text messaging
----------------------------------------------------

The service is provided by the In App Purchase Odoo platform.

**Scope evidence:** The module contains 123 files, including 31 Python, 20 XML, and 15 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `iap_mail`, `mail`, `phone_validation`.

## 2. Module structure

- Model/business logic files: 18
- Controller/API files: 2
- XML/data/view/template files: 20
- Browser asset files: 15
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 7
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/sms/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 18 model declarations, 150 methods, 1 constraint handlers, 0 onchange handlers, and 19 dependency declarations.
- **Evidence:** `addons/sms/models/mail_message.py:6`, `addons/sms/models/sms_sms.py:17`, `addons/sms/models/iap_account.py:6`, `addons/sms/models/mail_followers.py:7`, `addons/sms/models/ir_model.py:7`, `addons/sms/models/mail_notification.py:7`, `addons/sms/models/mail_thread.py:13`, `addons/sms/models/ir_actions_server.py:7`, `addons/sms/models/sms_template.py:6`, `addons/sms/models/mail_scheduled_message.py:5`, `addons/sms/models/res_company.py:6`, `addons/sms/models/sms_tracker.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/sms/controllers/main.py:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 20 XML files and 15 JavaScript/TypeScript files; static XML analysis found 43 record/template/menu identifiers.
- **Evidence:** `addons/sms/wizard/sms_composer_views.xml:3`, `addons/sms/wizard/sms_composer_views.xml:82`, `addons/sms/wizard/sms_composer_views.xml:99`, `addons/sms/wizard/sms_account_code_views.xml:3`, `addons/sms/wizard/sms_template_preview_views.xml:5`, `addons/sms/wizard/sms_template_preview_views.xml:31`, `addons/sms/wizard/sms_account_sender_views.xml:3`, `addons/sms/wizard/sms_template_reset_views.xml:4`, `addons/sms/wizard/sms_template_reset_views.xml:21`, `addons/sms/wizard/sms_account_phone_views.xml:3`, `addons/sms/data/iap_service_data.xml:4`, `addons/sms/data/mail_demo.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/sms/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 7 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/sms/__manifest__.py`, `addons/sms/models/sms_sms.py`, `addons/sms/models/ir_actions_server.py`, `addons/sms/data/ir_cron_data.xml`, `addons/sms/views/ir_actions_server_views.xml`, `addons/sms/views/sms_sms_views.xml`, `addons/sms/tests/test_sms_composer.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/sms/tests/test_sms_composer.py`, `addons/sms/tests/test_sms_template.py`, `addons/sms/tests/common.py`, `addons/sms/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 20; representative identifiers: `sms_composer_view_form`, `sms_composer_view_form_template_save`, `sms_composer_action_form`, `sms_account_code_view_form`, `sms_template_preview_form`, `sms_template_preview_action`, `sms_account_sender_view_form`, `sms_template_reset_view_form`, `sms_template_reset_action`, `sms_account_phone_view_form`, `iap_service_sms`, `message_demo_partner_1_0`, `message_demo_partner_1_1`, `message_demo_partner_1_2_notif_0`, `message_demo_partner_1_2`, `message_demo_partner_1_3`, `message_demo_partner_1_3_notif_0`, `message_demo_partner_1_4`, `message_demo_partner_1_4_notif_0`, `message_demo_partner_1_5`
- Menus: 2; representative evidence: `addons/sms/views/sms_sms_views.xml:69`, `addons/sms/views/sms_template_views.xml:94`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 61; representative evidence: `addons/sms/wizard/sms_composer_views.xml:5`, `addons/sms/wizard/sms_composer_views.xml:6`, `addons/sms/wizard/sms_composer_views.xml:33`, `addons/sms/wizard/sms_composer_views.xml:84`, `addons/sms/wizard/sms_composer_views.xml:86`, `addons/sms/wizard/sms_composer_views.xml:101`, `addons/sms/wizard/sms_composer_views.xml:102`, `addons/sms/wizard/sms_account_code_views.xml:5`, `addons/sms/wizard/sms_account_code_views.xml:6`, `addons/sms/wizard/sms_template_preview_views.xml:7`, `addons/sms/wizard/sms_template_preview_views.xml:8`, `addons/sms/wizard/sms_template_preview_views.xml:33`
- Browser assets: 15; representative files: `addons/sms/static/tests/sms_test_helpers.js`, `addons/sms/static/src/thread/message_patch.js`, `addons/sms/static/src/messaging_menu/messaging_menu_patch.js`, `addons/sms/static/src/core/sms_char_counter_utils.js`, `addons/sms/static/src/core/notification_model_patch.js`, `addons/sms/static/src/core/failure_model_patch.js`, `addons/sms/static/src/components/phone_field/phone_field.js`, `addons/sms/static/src/components/sms_widget/fields_sms_widget.js`, `addons/sms/static/src/components/sms_widget/sms_composer_template_selector.js`, `addons/sms/static/src/components/sms_widget/sms_char_counter.js`, `addons/sms/static/tests/thread/message_patch.test.js`, `addons/sms/static/tests/web/sms_button.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sms/__manifest__.py`
- **HTTP entry points:** `addons/sms/controllers/main.py:15`
- **Scheduled entry points:** `addons/sms/__manifest__.py`, `addons/sms/models/sms_sms.py`, `addons/sms/models/ir_actions_server.py`, `addons/sms/data/ir_cron_data.xml`, `addons/sms/views/ir_actions_server_views.xml`, `addons/sms/views/sms_sms_views.xml`, `addons/sms/tests/test_sms_composer.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 18
- Representative model evidence: inherits `mail.message` (addons/sms/models/mail_message.py:6); `sms.sms` (addons/sms/models/sms_sms.py:17); inherits `iap.account` (addons/sms/models/iap_account.py:6); inherits `mail.followers` (addons/sms/models/mail_followers.py:7); inherits `ir.model` (addons/sms/models/ir_model.py:7); inherits `mail.notification` (addons/sms/models/mail_notification.py:7); inherits `mail.thread` (addons/sms/models/mail_thread.py:13); inherits `ir.actions.server` (addons/sms/models/ir_actions_server.py:7); `sms.template` (addons/sms/models/sms_template.py:6); inherits `mail.scheduled.message` (addons/sms/models/mail_scheduled_message.py:5); inherits `res.company` (addons/sms/models/res_company.py:6); `sms.tracker` (addons/sms/models/sms_tracker.py:6); `sms.template.preview` (addons/sms/wizard/sms_template_preview.py:7); `sms.template.reset` (addons/sms/wizard/sms_template_reset.py:7); `sms.account.sender` (addons/sms/wizard/sms_account_sender.py:9); `sms.account.phone` (addons/sms/wizard/sms_account_phone.py:8); `sms.composer` (addons/sms/wizard/sms_composer.py:14); `sms.account.code` (addons/sms/wizard/sms_account_code.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/sms/controllers/main.py:15`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `iap_mail`, `mail`, `phone_validation`
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

- `addons/sms/__init__.py`
- `addons/sms/__manifest__.py`
- `addons/sms/controllers/__init__.py`
- `addons/sms/controllers/main.py`
- `addons/sms/data/iap_service_data.xml`
- `addons/sms/data/ir_cron_data.xml`
- `addons/sms/data/mail_demo.xml`
- `addons/sms/data/sms_demo.xml`
- `addons/sms/i18n/ar.po`
- `addons/sms/i18n/az.po`
- `addons/sms/i18n/bg.po`
- `addons/sms/i18n/bs.po`
- `addons/sms/i18n/ca.po`
- `addons/sms/i18n/cs.po`
- `addons/sms/i18n/da.po`
- `addons/sms/i18n/de.po`
- `addons/sms/i18n/el.po`
- `addons/sms/i18n/es.po`
- `addons/sms/i18n/es_419.po`
- `addons/sms/i18n/et.po`
- `addons/sms/i18n/fa.po`
- `addons/sms/i18n/fi.po`
- `addons/sms/i18n/fr.po`
- `addons/sms/i18n/gu.po`
- `addons/sms/i18n/he.po`
- `addons/sms/i18n/hi.po`
- `addons/sms/i18n/hr.po`
- `addons/sms/i18n/hu.po`
- `addons/sms/i18n/id.po`
- `addons/sms/i18n/is.po`
- `addons/sms/i18n/it.po`
- `addons/sms/i18n/ja.po`
- `addons/sms/i18n/kab.po`
- `addons/sms/i18n/km.po`
- `addons/sms/i18n/ko.po`
- `addons/sms/i18n/ku.po`
- `addons/sms/i18n/lo.po`
- `addons/sms/i18n/lt.po`
- `addons/sms/i18n/lv.po`
- `addons/sms/i18n/mn.po`
- `addons/sms/i18n/my.po`
- `addons/sms/i18n/nb.po`
- `addons/sms/i18n/nl.po`
- `addons/sms/i18n/pl.po`
- `addons/sms/i18n/pt.po`
- `addons/sms/i18n/pt_BR.po`
- `addons/sms/i18n/ro.po`
- `addons/sms/i18n/ru.po`
- `addons/sms/i18n/sk.po`
- `addons/sms/i18n/sl.po`
- `addons/sms/i18n/sms.pot`
- `addons/sms/i18n/sr@latin.po`
- `addons/sms/i18n/sv.po`
- `addons/sms/i18n/th.po`
- `addons/sms/i18n/tr.po`
- `addons/sms/i18n/uk.po`
- `addons/sms/i18n/uz.po`
- `addons/sms/i18n/vi.po`
- `addons/sms/i18n/zh_CN.po`
- `addons/sms/i18n/zh_TW.po`
- `addons/sms/models/__init__.py`
- `addons/sms/models/iap_account.py`
- `addons/sms/models/ir_actions_server.py`
- `addons/sms/models/ir_model.py`
- `addons/sms/models/mail_followers.py`
- `addons/sms/models/mail_message.py`
- `addons/sms/models/mail_notification.py`
- `addons/sms/models/mail_scheduled_message.py`
- `addons/sms/models/mail_thread.py`
- `addons/sms/models/res_company.py`
- `addons/sms/models/sms_sms.py`
- `addons/sms/models/sms_template.py`
- `addons/sms/models/sms_tracker.py`
- `addons/sms/security/ir.access.csv`
- `addons/sms/static/description/icon.png`
- `addons/sms/static/description/icon.svg`
- `addons/sms/static/description/icon_hi.png`
- `addons/sms/static/img/sms_failure.svg`
- `addons/sms/static/src/components/phone_field/phone_field.js`
- `addons/sms/static/src/components/sms_widget/fields_sms_widget.js`
- `addons/sms/static/src/components/sms_widget/fields_sms_widget.xml`
- `addons/sms/static/src/components/sms_widget/sms_char_counter.js`
- `addons/sms/static/src/components/sms_widget/sms_composer_template_selector.js`
- `addons/sms/static/src/components/sms_widget/sms_composer_template_selector.xml`
- `addons/sms/static/src/core/failure_model_patch.js`
- `addons/sms/static/src/core/notification_model_patch.js`
- `addons/sms/static/src/core/sms_char_counter_utils.js`
- `addons/sms/static/src/messaging_menu/messaging_menu_patch.js`
- `addons/sms/static/src/thread/message_patch.js`
- `addons/sms/static/tests/messaging_menu/messaging_menu_patch.test.js`
- `addons/sms/static/tests/mock_server/mock_models/partner.js`
- `addons/sms/static/tests/mock_server/mock_models/visitor.js`
- `addons/sms/static/tests/sms_test_helpers.js`
- `addons/sms/static/tests/thread/message_patch.test.js`
- `addons/sms/static/tests/web/sms_button.test.js`
- `addons/sms/tests/__init__.py`
- `addons/sms/tests/common.py`
- `addons/sms/tests/test_sms_composer.py`
- `addons/sms/tests/test_sms_template.py`
- `addons/sms/tests/test_sms_template.xml`
- `addons/sms/tools/__init__.py`
- `addons/sms/tools/sms_api.py`
- `addons/sms/tools/sms_tools.py`
- `addons/sms/views/iap_account_views.xml`
- `addons/sms/views/ir_actions_server_views.xml`
- `addons/sms/views/mail_notification_views.xml`
- `addons/sms/views/res_config_settings_views.xml`
- `addons/sms/views/res_partner_views.xml`
- `addons/sms/views/sms_sms_views.xml`
- `addons/sms/views/sms_template_views.xml`
- `addons/sms/wizard/__init__.py`
- `addons/sms/wizard/sms_account_code.py`
- `addons/sms/wizard/sms_account_code_views.xml`
- `addons/sms/wizard/sms_account_phone.py`
- `addons/sms/wizard/sms_account_phone_views.xml`
- `addons/sms/wizard/sms_account_sender.py`
- `addons/sms/wizard/sms_account_sender_views.xml`
- `addons/sms/wizard/sms_composer.py`
- `addons/sms/wizard/sms_composer_views.xml`
- `addons/sms/wizard/sms_template_preview.py`
- `addons/sms/wizard/sms_template_preview_views.xml`
- `addons/sms/wizard/sms_template_reset.py`
- `addons/sms/wizard/sms_template_reset_views.xml`
