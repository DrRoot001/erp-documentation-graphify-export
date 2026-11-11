# Module: snailmail

- **Module ID:** MOD-541
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/snailmail`
- **Manifest:** `addons/snailmail/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Allows users to send documents by post
=====================================================

**Scope evidence:** The module contains 91 files, including 19 Python, 5 XML, and 10 JavaScript/TypeScript files. The manifest declares dependencies: `iap_mail`, `mail`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 10
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 2
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/snailmail/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 52 methods, 0 constraint handlers, 1 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/snailmail/models/res_partner.py:9`, `addons/snailmail/models/mail_message.py:5`, `addons/snailmail/models/res_config_settings.py:6`, `addons/snailmail/models/ir_actions_report.py:4`, `addons/snailmail/models/snailmail_letter.py:37`, `addons/snailmail/models/mail_notification.py:6`, `addons/snailmail/models/mail_thread.py:8`, `addons/snailmail/models/res_company.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 10 JavaScript/TypeScript files; static XML analysis found 8 record/template/menu identifiers.
- **Evidence:** `addons/snailmail/data/iap_service_data.xml:4`, `addons/snailmail/data/snailmail_data.xml:4`, `addons/snailmail/views/snailmail_views.xml:3`, `addons/snailmail/views/snailmail_views.xml:18`, `addons/snailmail/views/snailmail_views.xml:52`, `addons/snailmail/views/snailmail_views.xml:60`, `addons/snailmail/views/report_assets.xml:3`, `addons/snailmail/views/report_assets.xml:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/snailmail/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/snailmail/models/snailmail_letter.py`, `addons/snailmail/data/snailmail_data.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/snailmail/models/ir_actions_report.py`, `addons/snailmail/models/snailmail_letter.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/snailmail/tests/test_snailmail_letter.py`, `addons/snailmail/tests/test_attachment_access.py`, `addons/snailmail/tests/common.py`, `addons/snailmail/tests/test_snailmail_webhook.py`, `addons/snailmail/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `iap_service_snailmail`, `snailmail_print`, `snailmail_letter_list`, `snailmail_letter_form`, `action_mail_letters`, `menu_snailmail_letters`, `report_layout`, `minimal_layout`
- Menus: 1; representative evidence: `addons/snailmail/views/snailmail_views.xml:60`
- Templates: 2; representative evidence: `addons/snailmail/views/report_assets.xml:3`, `addons/snailmail/views/report_assets.xml:8`
- View/action field declarations: 7; representative evidence: `addons/snailmail/views/snailmail_views.xml:5`, `addons/snailmail/views/snailmail_views.xml:6`, `addons/snailmail/views/snailmail_views.xml:20`, `addons/snailmail/views/snailmail_views.xml:21`, `addons/snailmail/views/snailmail_views.xml:42`, `addons/snailmail/views/snailmail_views.xml:54`, `addons/snailmail/views/snailmail_views.xml:55`
- Browser assets: 10; representative files: `addons/snailmail/static/tests/snailmail_test_helpers.js`, `addons/snailmail/static/src/messaging_menu/messaging_menu_patch.js`, `addons/snailmail/static/src/core/notification_model_patch.js`, `addons/snailmail/static/src/core/failure_model_patch.js`, `addons/snailmail/static/src/core_ui/snailmail_notification_popover.js`, `addons/snailmail/static/src/core_ui/message_patch.js`, `addons/snailmail/static/tests/message/message_patch.test.js`, `addons/snailmail/static/tests/messaging_menu/messaging_menu_patch.test.js`, `addons/snailmail/static/tests/mock_server/mock_model/snailmail_letter.js`, `addons/snailmail/static/tests/mock_server/mock_model/iap_account.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/snailmail/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/snailmail/models/snailmail_letter.py`, `addons/snailmail/data/snailmail_data.xml`
- **Report entry points:** `addons/snailmail/models/ir_actions_report.py`, `addons/snailmail/models/snailmail_letter.py`

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: inherits `res.partner` (addons/snailmail/models/res_partner.py:9); inherits `mail.message` (addons/snailmail/models/mail_message.py:5); inherits `res.config.settings` (addons/snailmail/models/res_config_settings.py:6); inherits `ir.actions.report` (addons/snailmail/models/ir_actions_report.py:4); `snailmail.letter` (addons/snailmail/models/snailmail_letter.py:37); inherits `mail.notification` (addons/snailmail/models/mail_notification.py:6); inherits `mail.thread` (addons/snailmail/models/mail_thread.py:8); inherits `res.company` (addons/snailmail/models/res_company.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `iap_mail`, `mail`
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

- `addons/snailmail/__init__.py`
- `addons/snailmail/__manifest__.py`
- `addons/snailmail/controller/__init__.py`
- `addons/snailmail/controller/snailmail_webhook.py`
- `addons/snailmail/country_utils.py`
- `addons/snailmail/data/iap_service_data.xml`
- `addons/snailmail/data/snailmail_data.xml`
- `addons/snailmail/i18n/ar.po`
- `addons/snailmail/i18n/az.po`
- `addons/snailmail/i18n/bg.po`
- `addons/snailmail/i18n/bs.po`
- `addons/snailmail/i18n/ca.po`
- `addons/snailmail/i18n/cs.po`
- `addons/snailmail/i18n/da.po`
- `addons/snailmail/i18n/de.po`
- `addons/snailmail/i18n/el.po`
- `addons/snailmail/i18n/es.po`
- `addons/snailmail/i18n/es_419.po`
- `addons/snailmail/i18n/et.po`
- `addons/snailmail/i18n/fa.po`
- `addons/snailmail/i18n/fi.po`
- `addons/snailmail/i18n/fr.po`
- `addons/snailmail/i18n/gu.po`
- `addons/snailmail/i18n/he.po`
- `addons/snailmail/i18n/hi.po`
- `addons/snailmail/i18n/hr.po`
- `addons/snailmail/i18n/hu.po`
- `addons/snailmail/i18n/id.po`
- `addons/snailmail/i18n/is.po`
- `addons/snailmail/i18n/it.po`
- `addons/snailmail/i18n/ja.po`
- `addons/snailmail/i18n/kab.po`
- `addons/snailmail/i18n/km.po`
- `addons/snailmail/i18n/ko.po`
- `addons/snailmail/i18n/ku.po`
- `addons/snailmail/i18n/lo.po`
- `addons/snailmail/i18n/lt.po`
- `addons/snailmail/i18n/lv.po`
- `addons/snailmail/i18n/mn.po`
- `addons/snailmail/i18n/my.po`
- `addons/snailmail/i18n/nb.po`
- `addons/snailmail/i18n/nl.po`
- `addons/snailmail/i18n/pl.po`
- `addons/snailmail/i18n/pt.po`
- `addons/snailmail/i18n/pt_BR.po`
- `addons/snailmail/i18n/ro.po`
- `addons/snailmail/i18n/ru.po`
- `addons/snailmail/i18n/sk.po`
- `addons/snailmail/i18n/sl.po`
- `addons/snailmail/i18n/snailmail.pot`
- `addons/snailmail/i18n/sr@latin.po`
- `addons/snailmail/i18n/sv.po`
- `addons/snailmail/i18n/th.po`
- `addons/snailmail/i18n/tr.po`
- `addons/snailmail/i18n/uk.po`
- `addons/snailmail/i18n/uz.po`
- `addons/snailmail/i18n/vi.po`
- `addons/snailmail/i18n/zh_CN.po`
- `addons/snailmail/i18n/zh_TW.po`
- `addons/snailmail/models/__init__.py`
- `addons/snailmail/models/ir_actions_report.py`
- `addons/snailmail/models/mail_message.py`
- `addons/snailmail/models/mail_notification.py`
- `addons/snailmail/models/mail_thread.py`
- `addons/snailmail/models/res_company.py`
- `addons/snailmail/models/res_config_settings.py`
- `addons/snailmail/models/res_partner.py`
- `addons/snailmail/models/snailmail_letter.py`
- `addons/snailmail/security/ir.access.csv`
- `addons/snailmail/static/description/icon.png`
- `addons/snailmail/static/description/icon.svg`
- `addons/snailmail/static/description/icon_hi.png`
- `addons/snailmail/static/img/snailmail_failure.png`
- `addons/snailmail/static/src/core/failure_model_patch.js`
- `addons/snailmail/static/src/core/notification_model_patch.js`
- `addons/snailmail/static/src/core_ui/message_patch.js`
- `addons/snailmail/static/src/core_ui/snailmail_notification_popover.js`
- `addons/snailmail/static/src/core_ui/snailmail_notification_popover.xml`
- `addons/snailmail/static/src/messaging_menu/messaging_menu_patch.js`
- `addons/snailmail/static/tests/message/message_patch.test.js`
- `addons/snailmail/static/tests/messaging_menu/messaging_menu_patch.test.js`
- `addons/snailmail/static/tests/mock_server/mock_model/iap_account.js`
- `addons/snailmail/static/tests/mock_server/mock_model/snailmail_letter.js`
- `addons/snailmail/static/tests/snailmail_test_helpers.js`
- `addons/snailmail/tests/__init__.py`
- `addons/snailmail/tests/common.py`
- `addons/snailmail/tests/test_attachment_access.py`
- `addons/snailmail/tests/test_snailmail_letter.py`
- `addons/snailmail/tests/test_snailmail_webhook.py`
- `addons/snailmail/views/report_assets.xml`
- `addons/snailmail/views/snailmail_views.xml`
