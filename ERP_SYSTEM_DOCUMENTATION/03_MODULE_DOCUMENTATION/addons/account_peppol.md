# Module: account_peppol

- **Module ID:** MOD-011
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/account_peppol`
- **Manifest:** `addons/account_peppol/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** This module is used to send/receive documents with Peppol

**Manifest description:**

- Register as a Peppol participant
- Send and receive documents via Peppol network in Peppol BIS Billing 3.0 format

**Scope evidence:** The module contains 121 files, including 37 Python, 15 XML, and 7 JavaScript/TypeScript files. The manifest declares dependencies: `account_edi_proxy_client`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 15
- Controller/API files: 4
- XML/data/view/template files: 15
- Browser asset files: 7
- Security files: 1
- Test files: 9
- Scheduled/automation evidence files: 7
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/account_peppol/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 15 model declarations, 265 methods, 3 constraint handlers, 3 onchange handlers, and 32 dependency declarations.
- **Evidence:** `addons/account_peppol/models/res_partner.py:20`, `addons/account_peppol/models/account_edi_proxy_user.py:29`, `addons/account_peppol/models/account_peppol_clarification.py:4`, `addons/account_peppol/models/account_edi_ubl_xml.py:4`, `addons/account_peppol/models/res_config_settings.py:4`, `addons/account_peppol/models/account_journal.py:6`, `addons/account_peppol/models/account_peppol_response.py:4`, `addons/account_peppol/models/account_move.py:12`, `addons/account_peppol/models/account_edi_common.py:4`, `addons/account_peppol/models/account_move_send.py:14`, `addons/account_peppol/models/res_company.py:20`, `addons/account_peppol/wizard/peppol_registration.py:22`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 4 controller files and 5 route declarations.
- **Evidence:** `addons/account_peppol/controllers/authentication.py:12`, `addons/account_peppol/controllers/authentication.py:56`, `addons/account_peppol/controllers/webhooks.py:7`, `addons/account_peppol/controllers/webhooks.py:26`, `addons/account_peppol/controllers/webhooks.py:45`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 15 XML files and 7 JavaScript/TypeScript files; static XML analysis found 41 record/template/menu identifiers.
- **Evidence:** `addons/account_peppol/demo/account_peppol_demo.xml:3`, `addons/account_peppol/wizard/peppol_rejection_wizard_views.xml:3`, `addons/account_peppol/wizard/peppol_registration_views.xml:3`, `addons/account_peppol/data/peppol_clarification_data.xml:7`, `addons/account_peppol/data/peppol_clarification_data.xml:13`, `addons/account_peppol/data/peppol_clarification_data.xml:20`, `addons/account_peppol/data/peppol_clarification_data.xml:27`, `addons/account_peppol/data/peppol_clarification_data.xml:34`, `addons/account_peppol/data/peppol_clarification_data.xml:41`, `addons/account_peppol/data/peppol_clarification_data.xml:48`, `addons/account_peppol/data/peppol_clarification_data.xml:55`, `addons/account_peppol/data/peppol_clarification_data.xml:62`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/account_peppol/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 7 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/account_peppol/models/account_edi_proxy_user.py`, `addons/account_peppol/models/account_move_send.py`, `addons/account_peppol/models/res_company.py`, `addons/account_peppol/controllers/webhooks.py`, `addons/account_peppol/tools/demo_utils.py`, `addons/account_peppol/data/cron.xml`, `addons/account_peppol/tests/test_peppol_messages.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 9 test files are present.
- **Evidence:** `addons/account_peppol/tests/test_peppol_messages.py`, `addons/account_peppol/tests/common.py`, `addons/account_peppol/tests/test_peppol_kyc.py`, `addons/account_peppol/tests/test_peppol_participant.py`, `addons/account_peppol/tests/__init__.py`, `addons/account_peppol/tests/test_ubl_export_bis3_be.py`, `addons/account_peppol/tests/test_account_journal.py`, `addons/account_peppol/tests/test_account_move.py`, `addons/account_peppol/tests/test_peppol_out_of_sync_resolution.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 15; representative identifiers: `default_account_peppol_edi_mode`, `account_peppol_rejection_wizard_view_form`, `peppol_registration_form`, `peppol_clarification_reason_non`, `peppol_clarification_reason_ref`, `peppol_clarification_reason_leg`, `peppol_clarification_reason_rec`, `peppol_clarification_reason_qua`, `peppol_clarification_reason_del`, `peppol_clarification_reason_pri`, `peppol_clarification_reason_qty`, `peppol_clarification_reason_itm`, `peppol_clarification_reason_pay`, `peppol_clarification_reason_unr`, `peppol_clarification_reason_fin`, `peppol_clarification_reason_ppd`, `peppol_clarification_reason_oth`, `peppol_clarification_action_noa`, `peppol_clarification_action_pin`, `peppol_clarification_action_nin`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/account_peppol/data/mail_templates_email_layouts.xml:4`, `addons/account_peppol/views/account_portal_templates.xml:2`
- View/action field declarations: 20; representative evidence: `addons/account_peppol/wizard/peppol_rejection_wizard_views.xml:5`, `addons/account_peppol/wizard/peppol_rejection_wizard_views.xml:6`, `addons/account_peppol/wizard/peppol_registration_views.xml:5`, `addons/account_peppol/wizard/peppol_registration_views.xml:7`, `addons/account_peppol/views/res_config_settings_views.xml:5`, `addons/account_peppol/views/res_config_settings_views.xml:7`, `addons/account_peppol/views/account_move_views.xml:5`, `addons/account_peppol/views/account_move_views.xml:8`, `addons/account_peppol/views/account_move_views.xml:39`, `addons/account_peppol/views/account_move_views.xml:41`, `addons/account_peppol/views/account_move_views.xml:50`, `addons/account_peppol/views/account_move_views.xml:52`
- Browser assets: 7; representative files: `addons/account_peppol/static/src/web/account_move_form_controller.js`, `addons/account_peppol/static/src/web/account_move_list_controller.js`, `addons/account_peppol/static/src/interactions/invoice_sending_method.js`, `addons/account_peppol/static/src/components/peppol_auth/peppol_auth_callback_action.js`, `addons/account_peppol/static/src/components/peppol_auth/peppol_auth_service.js`, `addons/account_peppol/static/src/components/peppol_info/peppol_info.js`, `addons/account_peppol/static/src/components/peppol_filterable_selection/peppol_non_focusable_selection.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/account_peppol/__manifest__.py`
- **HTTP entry points:** `addons/account_peppol/controllers/authentication.py:12`, `addons/account_peppol/controllers/authentication.py:56`, `addons/account_peppol/controllers/webhooks.py:7`, `addons/account_peppol/controllers/webhooks.py:26`, `addons/account_peppol/controllers/webhooks.py:45`
- **Scheduled entry points:** `addons/account_peppol/models/account_edi_proxy_user.py`, `addons/account_peppol/models/account_move_send.py`, `addons/account_peppol/models/res_company.py`, `addons/account_peppol/controllers/webhooks.py`, `addons/account_peppol/tools/demo_utils.py`, `addons/account_peppol/data/cron.xml`, `addons/account_peppol/tests/test_peppol_messages.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 15
- Representative model evidence: inherits `res.partner` (addons/account_peppol/models/res_partner.py:20); inherits `account_edi_proxy_client.user` (addons/account_peppol/models/account_edi_proxy_user.py:29); `account.peppol.clarification` (addons/account_peppol/models/account_peppol_clarification.py:4); inherits `account.edi.ubl` (addons/account_peppol/models/account_edi_ubl_xml.py:4); inherits `res.config.settings` (addons/account_peppol/models/res_config_settings.py:4); inherits `account.journal` (addons/account_peppol/models/account_journal.py:6); `account.peppol.response` (addons/account_peppol/models/account_peppol_response.py:4); inherits `account.move` (addons/account_peppol/models/account_move.py:12); inherits `account.edi.common` (addons/account_peppol/models/account_edi_common.py:4); inherits `account.move.send` (addons/account_peppol/models/account_move_send.py:14); inherits `res.company` (addons/account_peppol/models/res_company.py:20); `peppol.registration` (addons/account_peppol/wizard/peppol_registration.py:22); inherits `account.move.send.wizard` (addons/account_peppol/wizard/account_move_send_wizard.py:6); `account.peppol.rejection.wizard` (addons/account_peppol/wizard/peppol_rejection_wizard.py:5); inherits `account.move.send.batch.wizard` (addons/account_peppol/wizard/account_move_send_batch_wizard.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 4
- Route declarations: 5
- Route evidence: `addons/account_peppol/controllers/authentication.py:12`, `addons/account_peppol/controllers/authentication.py:56`, `addons/account_peppol/controllers/webhooks.py:7`, `addons/account_peppol/controllers/webhooks.py:26`, `addons/account_peppol/controllers/webhooks.py:45`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account_edi_proxy_client`, `account_edi_ubl_cii`
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

- `addons/account_peppol/__init__.py`
- `addons/account_peppol/__manifest__.py`
- `addons/account_peppol/controllers/__init__.py`
- `addons/account_peppol/controllers/authentication.py`
- `addons/account_peppol/controllers/portal.py`
- `addons/account_peppol/controllers/webhooks.py`
- `addons/account_peppol/data/cron.xml`
- `addons/account_peppol/data/mail_templates_email_layouts.xml`
- `addons/account_peppol/data/neutralize.sql`
- `addons/account_peppol/data/peppol_clarification_data.xml`
- `addons/account_peppol/data/res_partner_data.xml`
- `addons/account_peppol/demo/account_peppol_demo.xml`
- `addons/account_peppol/exceptions.py`
- `addons/account_peppol/i18n/account_peppol.pot`
- `addons/account_peppol/i18n/ar.po`
- `addons/account_peppol/i18n/az.po`
- `addons/account_peppol/i18n/bg.po`
- `addons/account_peppol/i18n/bs.po`
- `addons/account_peppol/i18n/ca.po`
- `addons/account_peppol/i18n/cs.po`
- `addons/account_peppol/i18n/da.po`
- `addons/account_peppol/i18n/de.po`
- `addons/account_peppol/i18n/el.po`
- `addons/account_peppol/i18n/es.po`
- `addons/account_peppol/i18n/es_419.po`
- `addons/account_peppol/i18n/et.po`
- `addons/account_peppol/i18n/fa.po`
- `addons/account_peppol/i18n/fi.po`
- `addons/account_peppol/i18n/fr.po`
- `addons/account_peppol/i18n/he.po`
- `addons/account_peppol/i18n/hi.po`
- `addons/account_peppol/i18n/hr.po`
- `addons/account_peppol/i18n/hu.po`
- `addons/account_peppol/i18n/id.po`
- `addons/account_peppol/i18n/it.po`
- `addons/account_peppol/i18n/ja.po`
- `addons/account_peppol/i18n/kab.po`
- `addons/account_peppol/i18n/ko.po`
- `addons/account_peppol/i18n/ku.po`
- `addons/account_peppol/i18n/lo.po`
- `addons/account_peppol/i18n/lt.po`
- `addons/account_peppol/i18n/lv.po`
- `addons/account_peppol/i18n/mn.po`
- `addons/account_peppol/i18n/my.po`
- `addons/account_peppol/i18n/nb.po`
- `addons/account_peppol/i18n/nl.po`
- `addons/account_peppol/i18n/pl.po`
- `addons/account_peppol/i18n/pt.po`
- `addons/account_peppol/i18n/pt_BR.po`
- `addons/account_peppol/i18n/ro.po`
- `addons/account_peppol/i18n/ru.po`
- `addons/account_peppol/i18n/sk.po`
- `addons/account_peppol/i18n/sl.po`
- `addons/account_peppol/i18n/sr@latin.po`
- `addons/account_peppol/i18n/sv.po`
- `addons/account_peppol/i18n/th.po`
- `addons/account_peppol/i18n/tr.po`
- `addons/account_peppol/i18n/uk.po`
- `addons/account_peppol/i18n/uz.po`
- `addons/account_peppol/i18n/vi.po`
- `addons/account_peppol/i18n/zh_CN.po`
- `addons/account_peppol/i18n/zh_TW.po`
- `addons/account_peppol/models/__init__.py`
- `addons/account_peppol/models/account_edi_common.py`
- `addons/account_peppol/models/account_edi_proxy_user.py`
- `addons/account_peppol/models/account_edi_ubl_xml.py`
- `addons/account_peppol/models/account_journal.py`
- `addons/account_peppol/models/account_move.py`
- `addons/account_peppol/models/account_move_send.py`
- `addons/account_peppol/models/account_peppol_clarification.py`
- `addons/account_peppol/models/account_peppol_response.py`
- `addons/account_peppol/models/res_company.py`
- `addons/account_peppol/models/res_config_settings.py`
- `addons/account_peppol/models/res_partner.py`
- `addons/account_peppol/security/ir.access.csv`
- `addons/account_peppol/static/img/itsme.svg`
- `addons/account_peppol/static/src/components/peppol_auth/peppol_auth_callback_action.js`
- `addons/account_peppol/static/src/components/peppol_auth/peppol_auth_service.js`
- `addons/account_peppol/static/src/components/peppol_filterable_selection/peppol_non_focusable_selection.js`
- `addons/account_peppol/static/src/components/peppol_filterable_selection/peppol_non_focusable_selection.xml`
- `addons/account_peppol/static/src/components/peppol_info/peppol_info.js`
- `addons/account_peppol/static/src/components/peppol_info/peppol_info.xml`
- `addons/account_peppol/static/src/css/account_peppol.scss`
- `addons/account_peppol/static/src/interactions/invoice_sending_method.js`
- `addons/account_peppol/static/src/web/account_move_form_controller.js`
- `addons/account_peppol/static/src/web/account_move_list_controller.js`
- `addons/account_peppol/tests/__init__.py`
- `addons/account_peppol/tests/assets/enc_key`
- `addons/account_peppol/tests/assets/incoming_invoice`
- `addons/account_peppol/tests/assets/incoming_self_billed_invoice`
- `addons/account_peppol/tests/assets/peppol_identification_test.pdf`
- `addons/account_peppol/tests/assets/private_key.pem`
- `addons/account_peppol/tests/assets/response_document`
- `addons/account_peppol/tests/common.py`
- `addons/account_peppol/tests/test_account_journal.py`
- `addons/account_peppol/tests/test_account_move.py`
- `addons/account_peppol/tests/test_peppol_kyc.py`
- `addons/account_peppol/tests/test_peppol_messages.py`
- `addons/account_peppol/tests/test_peppol_out_of_sync_resolution.py`
- `addons/account_peppol/tests/test_peppol_participant.py`
- `addons/account_peppol/tests/test_ubl_export_bis3_be.py`
- `addons/account_peppol/tools/__init__.py`
- `addons/account_peppol/tools/demo_bill`
- `addons/account_peppol/tools/demo_utils.py`
- `addons/account_peppol/tools/enc_key`
- `addons/account_peppol/tools/peppol_errors.py`
- `addons/account_peppol/tools/peppol_iap_connector.py`
- `addons/account_peppol/tools/private_key.pem`
- `addons/account_peppol/views/account_move_views.xml`
- `addons/account_peppol/views/account_peppol_response_views.xml`
- `addons/account_peppol/views/account_portal_templates.xml`
- `addons/account_peppol/views/peppol_authentication_views.xml`
- `addons/account_peppol/views/res_config_settings_views.xml`
- `addons/account_peppol/views/res_partner_views.xml`
- `addons/account_peppol/wizard/__init__.py`
- `addons/account_peppol/wizard/account_move_send_batch_wizard.py`
- `addons/account_peppol/wizard/account_move_send_wizard.py`
- `addons/account_peppol/wizard/peppol_registration.py`
- `addons/account_peppol/wizard/peppol_registration_views.xml`
- `addons/account_peppol/wizard/peppol_rejection_wizard.py`
- `addons/account_peppol/wizard/peppol_rejection_wizard_views.xml`
