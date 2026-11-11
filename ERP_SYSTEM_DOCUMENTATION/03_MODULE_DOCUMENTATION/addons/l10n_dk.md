# Module: l10n_dk

- **Module ID:** MOD-164
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_dk`
- **Manifest:** `addons/l10n_dk/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Localization Module for Denmark
===============================

This is the module to manage the **accounting chart for Denmark**. Cover both one-man business as well as I/S, IVS, ApS and A/S
Also provides Nemhandel registration and invoice sending throught the Odoo Access Point

**Scope evidence:** The module contains 66 files, including 32 Python, 20 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_proxy_client`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 15
- Controller/API files: 2
- XML/data/view/template files: 20
- Browser asset files: 2
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 7
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_dk/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 15 model declarations, 153 methods, 3 constraint handlers, 2 onchange handlers, and 15 dependency declarations.
- **Evidence:** `addons/l10n_dk/models/res_partner.py:18`, `addons/l10n_dk/models/account_edi_proxy_user.py:16`, `addons/l10n_dk/models/account_edi_xml_oioubl_21.py:40`, `addons/l10n_dk/models/nemhandel_response.py:4`, `addons/l10n_dk/models/res_config_settings.py:7`, `addons/l10n_dk/models/account_journal.py:4`, `addons/l10n_dk/models/account_account.py:7`, `addons/l10n_dk/models/account_move.py:5`, `addons/l10n_dk/models/account_move_send.py:8`, `addons/l10n_dk/models/template_dk.py:7`, `addons/l10n_dk/models/res_company.py:14`, `addons/l10n_dk/wizard/nemhandel_registration.py:14`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 3 route declarations.
- **Evidence:** `addons/l10n_dk/controllers/webhooks.py:7`, `addons/l10n_dk/controllers/webhooks.py:26`, `addons/l10n_dk/controllers/webhooks.py:45`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 20 XML files and 2 JavaScript/TypeScript files; static XML analysis found 60 record/template/menu identifiers.
- **Evidence:** `addons/l10n_dk/demo/nemhandel_mode_demo.xml:3`, `addons/l10n_dk/demo/demo_company.xml:3`, `addons/l10n_dk/demo/demo_company.xml:16`, `addons/l10n_dk/demo/demo_company.xml:21`, `addons/l10n_dk/wizard/nemhandel_rejection_wizard_views.xml:3`, `addons/l10n_dk/wizard/nemhandel_registration_views.xml:3`, `addons/l10n_dk/data/account_tax_report_data.xml:3`, `addons/l10n_dk/data/account_tax_report_data.xml:11`, `addons/l10n_dk/data/account_tax_report_data.xml:18`, `addons/l10n_dk/data/account_tax_report_data.xml:25`, `addons/l10n_dk/data/account_tax_report_data.xml:30`, `addons/l10n_dk/data/account_tax_report_data.xml:37`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_dk/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 7 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_dk/models/account_edi_proxy_user.py`, `addons/l10n_dk/models/account_move_send.py`, `addons/l10n_dk/controllers/webhooks.py`, `addons/l10n_dk/tools/demo_utils.py`, `addons/l10n_dk/data/cron.xml`, `addons/l10n_dk/tests/test_nemhandel_messages.py`, `addons/l10n_dk/tests/test_nemhandel_participant.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/l10n_dk/tests/test_nemhandel_messages.py`, `addons/l10n_dk/tests/test_xml_oioubl_21.py`, `addons/l10n_dk/tests/test_nemhandel_participant.py`, `addons/l10n_dk/tests/common.py`, `addons/l10n_dk/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 20; representative identifiers: `default_l10n_dk_edi_mode`, `base.partner_demo_company_dk`, `base.demo_company_dk`, `base.demo_bank_dk`, `nemhandel_rejection_wizard_view_form`, `nemhandel_registration_form`, `account_tax_report_skat_dk`, `account_tax_report_skat_dk_balance`, `account_tax_report_line_sales_group`, `account_tax_report_line_sales_tax`, `account_tax_report_line_sales_tax_tag`, `account_tax_report_line_international_purchase_products`, `account_tax_report_line_international_purchase_products_tag`, `account_tax_report_line_international_purchase_services`, `account_tax_report_line_international_purchase_services_tag`, `account_tax_report_line_deduction_group`, `account_tax_report_line_deduction_purchase_tax`, `account_tax_report_line_deduction_purchase_tax_tag`, `account_tax_report_line_deduction_oil_bottle_tax`, `account_tax_report_line_deduction_oil_bottle_tax_tag`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 22; representative evidence: `addons/l10n_dk/wizard/nemhandel_rejection_wizard_views.xml:5`, `addons/l10n_dk/wizard/nemhandel_rejection_wizard_views.xml:6`, `addons/l10n_dk/wizard/nemhandel_registration_views.xml:5`, `addons/l10n_dk/wizard/nemhandel_registration_views.xml:7`, `addons/l10n_dk/views/nemhandel_response_views.xml:5`, `addons/l10n_dk/views/nemhandel_response_views.xml:6`, `addons/l10n_dk/views/nemhandel_response_views.xml:18`, `addons/l10n_dk/views/nemhandel_response_views.xml:19`, `addons/l10n_dk/views/res_config_settings_views.xml:5`, `addons/l10n_dk/views/res_config_settings_views.xml:7`, `addons/l10n_dk/views/account_move_views.xml:5`, `addons/l10n_dk/views/account_move_views.xml:8`
- Browser assets: 2; representative files: `addons/l10n_dk/static/src/tours/nemhandel_onboarding.js`, `addons/l10n_dk/static/src/components/verification_code_widget/verification_code_widget.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_dk/__manifest__.py`
- **HTTP entry points:** `addons/l10n_dk/controllers/webhooks.py:7`, `addons/l10n_dk/controllers/webhooks.py:26`, `addons/l10n_dk/controllers/webhooks.py:45`
- **Scheduled entry points:** `addons/l10n_dk/models/account_edi_proxy_user.py`, `addons/l10n_dk/models/account_move_send.py`, `addons/l10n_dk/controllers/webhooks.py`, `addons/l10n_dk/tools/demo_utils.py`, `addons/l10n_dk/data/cron.xml`, `addons/l10n_dk/tests/test_nemhandel_messages.py`, `addons/l10n_dk/tests/test_nemhandel_participant.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 15
- Representative model evidence: inherits `res.partner` (addons/l10n_dk/models/res_partner.py:18); inherits `account_edi_proxy_client.user` (addons/l10n_dk/models/account_edi_proxy_user.py:16); `account.edi.xml.oioubl_21` (addons/l10n_dk/models/account_edi_xml_oioubl_21.py:40); `nemhandel.response` (addons/l10n_dk/models/nemhandel_response.py:4); inherits `res.config.settings` (addons/l10n_dk/models/res_config_settings.py:7); inherits `account.journal` (addons/l10n_dk/models/account_journal.py:4); `account.account` (addons/l10n_dk/models/account_account.py:7); inherits `account.move` (addons/l10n_dk/models/account_move.py:5); inherits `account.move.send` (addons/l10n_dk/models/account_move_send.py:8); inherits `account.chart.template` (addons/l10n_dk/models/template_dk.py:7); inherits `res.company` (addons/l10n_dk/models/res_company.py:14); `nemhandel.registration` (addons/l10n_dk/wizard/nemhandel_registration.py:14); inherits `account.move.send.wizard` (addons/l10n_dk/wizard/account_move_send_wizard.py:5); inherits `account.move.send.batch.wizard` (addons/l10n_dk/wizard/account_move_send_batch_wizard.py:4); `nemhandel.rejection.wizard` (addons/l10n_dk/wizard/nemhandel_rejection_wizard.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 3
- Route evidence: `addons/l10n_dk/controllers/webhooks.py:7`, `addons/l10n_dk/controllers/webhooks.py:26`, `addons/l10n_dk/controllers/webhooks.py:45`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `account_edi_proxy_client`, `account_edi_ubl_cii`
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

- `addons/l10n_dk/__init__.py`
- `addons/l10n_dk/__manifest__.py`
- `addons/l10n_dk/controllers/__init__.py`
- `addons/l10n_dk/controllers/webhooks.py`
- `addons/l10n_dk/data/account.account.tag.csv`
- `addons/l10n_dk/data/account_tax_report_data.xml`
- `addons/l10n_dk/data/cron.xml`
- `addons/l10n_dk/data/nemhandel_onboarding_tour.xml`
- `addons/l10n_dk/data/neutralize.sql`
- `addons/l10n_dk/data/template/account.account-dk.csv`
- `addons/l10n_dk/data/template/account.fiscal.position-dk.csv`
- `addons/l10n_dk/data/template/account.tax-dk.csv`
- `addons/l10n_dk/data/template/account.tax.group-dk.csv`
- `addons/l10n_dk/demo/demo_company.xml`
- `addons/l10n_dk/demo/nemhandel_mode_demo.xml`
- `addons/l10n_dk/i18n/da.po`
- `addons/l10n_dk/i18n/l10n_dk.pot`
- `addons/l10n_dk/migrations/1.2/end-migrate.py`
- `addons/l10n_dk/migrations/1.3/end-migrate.py`
- `addons/l10n_dk/migrations/1.4/end-migrate.py`
- `addons/l10n_dk/migrations/1.4/post-migrate.py`
- `addons/l10n_dk/models/__init__.py`
- `addons/l10n_dk/models/account_account.py`
- `addons/l10n_dk/models/account_edi_proxy_user.py`
- `addons/l10n_dk/models/account_edi_xml_oioubl_21.py`
- `addons/l10n_dk/models/account_journal.py`
- `addons/l10n_dk/models/account_move.py`
- `addons/l10n_dk/models/account_move_send.py`
- `addons/l10n_dk/models/nemhandel_response.py`
- `addons/l10n_dk/models/res_company.py`
- `addons/l10n_dk/models/res_config_settings.py`
- `addons/l10n_dk/models/res_partner.py`
- `addons/l10n_dk/models/template_dk.py`
- `addons/l10n_dk/security/ir.access.csv`
- `addons/l10n_dk/static/src/components/verification_code_widget/verification_code_widget.js`
- `addons/l10n_dk/static/src/components/verification_code_widget/verification_code_widget.xml`
- `addons/l10n_dk/static/src/tours/nemhandel_onboarding.js`
- `addons/l10n_dk/tests/__init__.py`
- `addons/l10n_dk/tests/assets/document`
- `addons/l10n_dk/tests/assets/enc_key`
- `addons/l10n_dk/tests/assets/private_key.pem`
- `addons/l10n_dk/tests/common.py`
- `addons/l10n_dk/tests/test_files/from_odoo/oioubl_out_invoice_child_partner.xml`
- `addons/l10n_dk/tests/test_files/from_odoo/oioubl_out_invoice_discount.xml`
- `addons/l10n_dk/tests/test_files/from_odoo/oioubl_out_invoice_foreign_partner_be.xml`
- `addons/l10n_dk/tests/test_files/from_odoo/oioubl_out_invoice_foreign_partner_fr.xml`
- `addons/l10n_dk/tests/test_files/from_odoo/oioubl_out_invoice_partner_dk.xml`
- `addons/l10n_dk/tests/test_files/from_odoo/oioubl_out_refund_foreign_partner_fr.xml`
- `addons/l10n_dk/tests/test_files/from_odoo/oioubl_out_refund_partner_dk.xml`
- `addons/l10n_dk/tests/test_nemhandel_messages.py`
- `addons/l10n_dk/tests/test_nemhandel_participant.py`
- `addons/l10n_dk/tests/test_xml_oioubl_21.py`
- `addons/l10n_dk/tools/__init__.py`
- `addons/l10n_dk/tools/demo_utils.py`
- `addons/l10n_dk/views/account_journal_views.xml`
- `addons/l10n_dk/views/account_move_views.xml`
- `addons/l10n_dk/views/nemhandel_response_views.xml`
- `addons/l10n_dk/views/res_config_settings_views.xml`
- `addons/l10n_dk/views/res_partner_views.xml`
- `addons/l10n_dk/wizard/__init__.py`
- `addons/l10n_dk/wizard/account_move_send_batch_wizard.py`
- `addons/l10n_dk/wizard/account_move_send_wizard.py`
- `addons/l10n_dk/wizard/nemhandel_registration.py`
- `addons/l10n_dk/wizard/nemhandel_registration_views.xml`
- `addons/l10n_dk/wizard/nemhandel_rejection_wizard.py`
- `addons/l10n_dk/wizard/nemhandel_rejection_wizard_views.xml`
