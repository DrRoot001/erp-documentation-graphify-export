# Module: l10n_fr_pdp

- **Module ID:** MOD-194
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_fr_pdp`
- **Manifest:** `addons/l10n_fr_pdp/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

- Support for the mandatory electronic invoicing in France
        - Send and receive documents via the Odoo Approved Platform

**Scope evidence:** The module contains 100 files, including 43 Python, 48 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_fr_account`, `account_peppol`, `iap`.

## 2. Module structure

- Model/business logic files: 23
- Controller/API files: 3
- XML/data/view/template files: 48
- Browser asset files: 2
- Security files: 1
- Test files: 9
- Scheduled/automation evidence files: 10
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_fr_pdp/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 23 model declarations, 484 methods, 1 constraint handlers, 1 onchange handlers, and 34 dependency declarations.
- **Evidence:** `addons/l10n_fr_pdp/models/account_edi_xml_ubl_21_fr.py:15`, `addons/l10n_fr_pdp/models/res_partner.py:20`, `addons/l10n_fr_pdp/models/account_edi_proxy_user.py:92`, `addons/l10n_fr_pdp/models/pdp_flow.py:30`, `addons/l10n_fr_pdp/models/res_config_settings.py:4`, `addons/l10n_fr_pdp/models/account_edi_xml_cii_facturx.py:5`, `addons/l10n_fr_pdp/models/account_journal.py:4`, `addons/l10n_fr_pdp/models/account_tax.py:4`, `addons/l10n_fr_pdp/models/account_peppol_response.py:36`, `addons/l10n_fr_pdp/models/pdp_flow_xml_builder.py:24`, `addons/l10n_fr_pdp/models/account_move.py:26`, `addons/l10n_fr_pdp/models/account_edi_common.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 2 route declarations.
- **Evidence:** `addons/l10n_fr_pdp/controllers/routes.py:12`, `addons/l10n_fr_pdp/controllers/webhooks.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 48 XML files and 2 JavaScript/TypeScript files; static XML analysis found 35 record/template/menu identifiers.
- **Evidence:** `addons/l10n_fr_pdp/wizard/pdp_response_wizard_views.xml:3`, `addons/l10n_fr_pdp/wizard/l10n_fr_pdp_partner_lookup.xml:3`, `addons/l10n_fr_pdp/wizard/l10n_fr_pdp_partner_lookup.xml:21`, `addons/l10n_fr_pdp/wizard/pdp_registration_views.xml:3`, `addons/l10n_fr_pdp/data/ir_cron.xml:3`, `addons/l10n_fr_pdp/data/ir_cron.xml:12`, `addons/l10n_fr_pdp/data/ir_cron.xml:22`, `addons/l10n_fr_pdp/views/pdp_flow_views.xml:3`, `addons/l10n_fr_pdp/views/pdp_flow_views.xml:27`, `addons/l10n_fr_pdp/views/pdp_flow_views.xml:102`, `addons/l10n_fr_pdp/views/pdp_flow_views.xml:122`, `addons/l10n_fr_pdp/views/pdp_flow_views.xml:130`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_fr_pdp/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 10 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_fr_pdp/__manifest__.py`, `addons/l10n_fr_pdp/models/account_edi_proxy_user.py`, `addons/l10n_fr_pdp/models/pdp_flow.py`, `addons/l10n_fr_pdp/controllers/webhooks.py`, `addons/l10n_fr_pdp/data/ir_cron.xml`, `addons/l10n_fr_pdp/views/pdp_flow_views.xml`, `addons/l10n_fr_pdp/views/account_move_views.xml`, `addons/l10n_fr_pdp/tests/test_flow_lifecycle.py`, `addons/l10n_fr_pdp/tests/test_messages.py`, `addons/l10n_fr_pdp/tests/test_user.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 9 test files are present.
- **Evidence:** `addons/l10n_fr_pdp/tests/test_cii_export_facturx_fr.py`, `addons/l10n_fr_pdp/tests/test_cii_import_facturx_fr.py`, `addons/l10n_fr_pdp/tests/common.py`, `addons/l10n_fr_pdp/tests/test_flow_lifecycle.py`, `addons/l10n_fr_pdp/tests/__init__.py`, `addons/l10n_fr_pdp/tests/test_partner.py`, `addons/l10n_fr_pdp/tests/test_xml_ubl_21_fr.py`, `addons/l10n_fr_pdp/tests/test_messages.py`, `addons/l10n_fr_pdp/tests/test_user.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 48; representative identifiers: `pdp_response_wizard_form`, `view_l10n_fr_pdp_partner_lookup_form`, `view_l10n_fr_pdp_annuaire_line_tree`, `pdp_registration_form`, `ir_cron_pdp_get_regulatory_documents`, `ir_cron_pdp_send_lifecycles`, `ir_cron_l10n_fr_pdp_generate_flows`, `l10n_fr_pdp_reports_view_flow_list`, `l10n_fr_pdp_reports_view_flow_form`, `l10n_fr_pdp_reports_view_flow_search`, `l10n_fr_pdp_reports_action_flows`, `l10n_fr_pdp_reports_action_build_multi`, `l10n_fr_pdp_reports_action_error_moves`, `E-reporting`, `res_config_settings_view_form`, `l10n_fr_pdp_view_out_invoice_tree`, `l10n_fr_pdp_view_out_credit_note_tree`, `l10n_fr_pdp_view_in_invoice_refund_tree_inherit`, `l10n_fr_pdp_view_in_bill_tree_inherit`, `l10n_fr_pdp_view_move_form`
- Menus: 1; representative evidence: `addons/l10n_fr_pdp/views/pdp_flow_views.xml:149`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 56; representative evidence: `addons/l10n_fr_pdp/wizard/pdp_response_wizard_views.xml:5`, `addons/l10n_fr_pdp/wizard/pdp_response_wizard_views.xml:6`, `addons/l10n_fr_pdp/wizard/l10n_fr_pdp_partner_lookup.xml:5`, `addons/l10n_fr_pdp/wizard/l10n_fr_pdp_partner_lookup.xml:6`, `addons/l10n_fr_pdp/wizard/l10n_fr_pdp_partner_lookup.xml:23`, `addons/l10n_fr_pdp/wizard/l10n_fr_pdp_partner_lookup.xml:24`, `addons/l10n_fr_pdp/wizard/pdp_registration_views.xml:5`, `addons/l10n_fr_pdp/wizard/pdp_registration_views.xml:7`, `addons/l10n_fr_pdp/views/pdp_flow_views.xml:5`, `addons/l10n_fr_pdp/views/pdp_flow_views.xml:6`, `addons/l10n_fr_pdp/views/pdp_flow_views.xml:29`, `addons/l10n_fr_pdp/views/pdp_flow_views.xml:30`
- Browser assets: 2; representative files: `addons/l10n_fr_pdp/static/src/js/status_listener.js`, `addons/l10n_fr_pdp/static/src/js/pdp_info.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_fr_pdp/__manifest__.py`
- **HTTP entry points:** `addons/l10n_fr_pdp/controllers/routes.py:12`, `addons/l10n_fr_pdp/controllers/webhooks.py:7`
- **Scheduled entry points:** `addons/l10n_fr_pdp/__manifest__.py`, `addons/l10n_fr_pdp/models/account_edi_proxy_user.py`, `addons/l10n_fr_pdp/models/pdp_flow.py`, `addons/l10n_fr_pdp/controllers/webhooks.py`, `addons/l10n_fr_pdp/data/ir_cron.xml`, `addons/l10n_fr_pdp/views/pdp_flow_views.xml`, `addons/l10n_fr_pdp/views/account_move_views.xml`, `addons/l10n_fr_pdp/tests/test_flow_lifecycle.py`, `addons/l10n_fr_pdp/tests/test_messages.py`, `addons/l10n_fr_pdp/tests/test_user.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 23
- Representative model evidence: `account.edi.xml.ubl_21_fr` (addons/l10n_fr_pdp/models/account_edi_xml_ubl_21_fr.py:15); inherits `res.partner` (addons/l10n_fr_pdp/models/res_partner.py:20); inherits `account_edi_proxy_client.user` (addons/l10n_fr_pdp/models/account_edi_proxy_user.py:92); `l10n.fr.pdp.reports.flow` (addons/l10n_fr_pdp/models/pdp_flow.py:30); inherits `res.config.settings` (addons/l10n_fr_pdp/models/res_config_settings.py:4); inherits `account.edi.xml.cii` (addons/l10n_fr_pdp/models/account_edi_xml_cii_facturx.py:5); inherits `account.journal` (addons/l10n_fr_pdp/models/account_journal.py:4); inherits `account.tax` (addons/l10n_fr_pdp/models/account_tax.py:4); inherits `account.peppol.response` (addons/l10n_fr_pdp/models/account_peppol_response.py:36); `pdp.flow.10.xml.builder` (addons/l10n_fr_pdp/models/pdp_flow_xml_builder.py:24); inherits `account.move` (addons/l10n_fr_pdp/models/account_move.py:26); inherits `account.edi.common` (addons/l10n_fr_pdp/models/account_edi_common.py:8); inherits `account.move.send` (addons/l10n_fr_pdp/models/account_move_send.py:4); inherits `account.edi.ubl` (addons/l10n_fr_pdp/models/account_edi_ubl.py:10); inherits `account.edi.cii` (addons/l10n_fr_pdp/models/account_edi_cii.py:6); inherits `ir.attachment` (addons/l10n_fr_pdp/models/ir_attachment.py:6); inherits `res.company` (addons/l10n_fr_pdp/models/res_company.py:20); `l10n.fr.pdp.reports.send.wizard` (addons/l10n_fr_pdp/wizard/pdp_send_wizard.py:4); inherits `account.move.send.wizard` (addons/l10n_fr_pdp/wizard/account_move_send_wizard.py:4); `pdp.registration` (addons/l10n_fr_pdp/wizard/pdp_registration.py:14); `l10n_fr_pdp.partner.lookup` (addons/l10n_fr_pdp/wizard/l10n_fr_pdp_partner_lookup.py:4); `l10n_fr_pdp.annuaire.line` (addons/l10n_fr_pdp/wizard/l10n_fr_pdp_partner_lookup.py:35); `pdp.response.wizard` (addons/l10n_fr_pdp/wizard/pdp_response_wizard.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 2
- Route evidence: `addons/l10n_fr_pdp/controllers/routes.py:12`, `addons/l10n_fr_pdp/controllers/webhooks.py:7`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_fr_account`, `account_peppol`, `iap`
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

- `addons/l10n_fr_pdp/__init__.py`
- `addons/l10n_fr_pdp/__manifest__.py`
- `addons/l10n_fr_pdp/controllers/__init__.py`
- `addons/l10n_fr_pdp/controllers/routes.py`
- `addons/l10n_fr_pdp/controllers/webhooks.py`
- `addons/l10n_fr_pdp/data/ir_cron.xml`
- `addons/l10n_fr_pdp/i18n/fr.po`
- `addons/l10n_fr_pdp/i18n/l10n_fr_pdp.pot`
- `addons/l10n_fr_pdp/models/__init__.py`
- `addons/l10n_fr_pdp/models/account_edi_cii.py`
- `addons/l10n_fr_pdp/models/account_edi_common.py`
- `addons/l10n_fr_pdp/models/account_edi_proxy_user.py`
- `addons/l10n_fr_pdp/models/account_edi_ubl.py`
- `addons/l10n_fr_pdp/models/account_edi_xml_cii_facturx.py`
- `addons/l10n_fr_pdp/models/account_edi_xml_ubl_21_fr.py`
- `addons/l10n_fr_pdp/models/account_journal.py`
- `addons/l10n_fr_pdp/models/account_move.py`
- `addons/l10n_fr_pdp/models/account_move_send.py`
- `addons/l10n_fr_pdp/models/account_peppol_response.py`
- `addons/l10n_fr_pdp/models/account_tax.py`
- `addons/l10n_fr_pdp/models/ir_attachment.py`
- `addons/l10n_fr_pdp/models/pdp_flow.py`
- `addons/l10n_fr_pdp/models/pdp_flow_xml_builder.py`
- `addons/l10n_fr_pdp/models/res_company.py`
- `addons/l10n_fr_pdp/models/res_config_settings.py`
- `addons/l10n_fr_pdp/models/res_partner.py`
- `addons/l10n_fr_pdp/security/ir.access.csv`
- `addons/l10n_fr_pdp/static/src/js/pdp_info.js`
- `addons/l10n_fr_pdp/static/src/js/pdp_info.xml`
- `addons/l10n_fr_pdp/static/src/js/status_listener.js`
- `addons/l10n_fr_pdp/static/src/js/status_listener.xml`
- `addons/l10n_fr_pdp/tests/__init__.py`
- `addons/l10n_fr_pdp/tests/common.py`
- `addons/l10n_fr_pdp/tests/data/FACT_REPORT2025_S2F3.xml`
- `addons/l10n_fr_pdp/tests/data/FACT_REPORT2025_S2F4.xml`
- `addons/l10n_fr_pdp/tests/data/FFE1025A_PPF262_PPF2621025000000000000290.xml`
- `addons/l10n_fr_pdp/tests/data/FFE1025A_PPF262_PPF2621025000000000000292.xml`
- `addons/l10n_fr_pdp/tests/data/FFE1025A_PPF262_PPF2621025000000000000294.xml`
- `addons/l10n_fr_pdp/tests/test_cii_export_facturx_fr.py`
- `addons/l10n_fr_pdp/tests/test_cii_import_facturx_fr.py`
- `addons/l10n_fr_pdp/tests/test_files/assets/document`
- `addons/l10n_fr_pdp/tests/test_files/assets/document_factur_x_self_bill`
- `addons/l10n_fr_pdp/tests/test_files/assets/enc_key`
- `addons/l10n_fr_pdp/tests/test_files/assets/private_key.pem`
- `addons/l10n_fr_pdp/tests/test_files/export/facturx/invoice/fr/facturx_fr_out_downpayment_credit_note.xml`
- `addons/l10n_fr_pdp/tests/test_files/export/facturx/invoice/fr/facturx_fr_out_downpayment_invoice.xml`
- `addons/l10n_fr_pdp/tests/test_files/export/facturx/invoice/fr/facturx_fr_out_final_invoice.xml`
- `addons/l10n_fr_pdp/tests/test_files/export/facturx/invoice/fr/test_invoice_narration.xml`
- `addons/l10n_fr_pdp/tests/test_files/export/facturx/invoice/fr/test_invoice_narration_early_payment_discount.xml`
- `addons/l10n_fr_pdp/tests/test_files/export/facturx/invoice/fr/test_invoice_profile_id_goods.xml`
- `addons/l10n_fr_pdp/tests/test_files/export/facturx/invoice/fr/test_invoice_profile_id_mixed.xml`
- `addons/l10n_fr_pdp/tests/test_files/export/facturx/invoice/fr/test_invoice_profile_id_services.xml`
- `addons/l10n_fr_pdp/tests/test_files/export/ubl_21_fr/invoice/fr/ubl_21_fr_out_credit_note.xml`
- `addons/l10n_fr_pdp/tests/test_files/export/ubl_21_fr/invoice/fr/ubl_21_fr_out_downpayment_credit_note.xml`
- `addons/l10n_fr_pdp/tests/test_files/export/ubl_21_fr/invoice/fr/ubl_21_fr_out_downpayment_invoice.xml`
- `addons/l10n_fr_pdp/tests/test_files/export/ubl_21_fr/invoice/fr/ubl_21_fr_out_final_invoice.xml`
- `addons/l10n_fr_pdp/tests/test_files/export/ubl_21_fr/invoice/fr/ubl_21_fr_out_invoice.xml`
- `addons/l10n_fr_pdp/tests/test_files/export/ubl_21_fr/invoice/fr/ubl_21_fr_out_invoice_b2g.xml`
- `addons/l10n_fr_pdp/tests/test_files/export/ubl_21_fr/invoice/fr/ubl_21_fr_out_invoice_rounding.xml`
- `addons/l10n_fr_pdp/tests/test_files/export/ubl_21_fr/invoice/fr/ubl_21_fr_out_no_vat_invoice.xml`
- `addons/l10n_fr_pdp/tests/test_files/import/facturx/invoice/fr/facturx_fr_in_downpayment_credit_note.xml`
- `addons/l10n_fr_pdp/tests/test_files/import/facturx/invoice/fr/facturx_fr_in_downpayment_invoice.xml`
- `addons/l10n_fr_pdp/tests/test_files/import/facturx/invoice/fr/facturx_fr_in_final_invoice_copied_lines.xml`
- `addons/l10n_fr_pdp/tests/test_files/import/facturx/invoice/fr/facturx_fr_in_final_invoice_prepaid_amount.xml`
- `addons/l10n_fr_pdp/tests/test_files/import/facturx/invoice/fr/facturx_fr_in_partial_invoice_line_charges_price_details.xml`
- `addons/l10n_fr_pdp/tests/test_files/import/facturx/invoice/fr/facturx_fr_in_partial_invoice_line_wrong_unit_price.xml`
- `addons/l10n_fr_pdp/tests/test_files/import/ubl_21_fr/invoice/fr/ubl_21_fr_in_downpayment_credit_note.xml`
- `addons/l10n_fr_pdp/tests/test_files/import/ubl_21_fr/invoice/fr/ubl_21_fr_in_downpayment_invoice.xml`
- `addons/l10n_fr_pdp/tests/test_files/import/ubl_21_fr/invoice/fr/ubl_21_fr_in_final_invoice_copied_lines.xml`
- `addons/l10n_fr_pdp/tests/test_files/import/ubl_21_fr/invoice/fr/ubl_21_fr_in_final_invoice_prepaid_amount.xml`
- `addons/l10n_fr_pdp/tests/test_files/import/ubl_21_fr/invoice/fr/ubl_21_fr_in_invoice_establishment.xml`
- `addons/l10n_fr_pdp/tests/test_files/import/ubl_21_fr/invoice/fr/ubl_21_fr_in_partial_invoice_en16931_customization_id.xml`
- `addons/l10n_fr_pdp/tests/test_files/import/ubl_21_fr/invoice/fr/ubl_21_fr_in_partial_invoice_line_charges_price_details.xml`
- `addons/l10n_fr_pdp/tests/test_files/import/ubl_21_fr/invoice/fr/ubl_21_fr_in_partial_invoice_line_wrong_unit_price.xml`
- `addons/l10n_fr_pdp/tests/test_flow_lifecycle.py`
- `addons/l10n_fr_pdp/tests/test_messages.py`
- `addons/l10n_fr_pdp/tests/test_partner.py`
- `addons/l10n_fr_pdp/tests/test_user.py`
- `addons/l10n_fr_pdp/tests/test_xml_ubl_21_fr.py`
- `addons/l10n_fr_pdp/tools/__init__.py`
- `addons/l10n_fr_pdp/tools/demo_utils.py`
- `addons/l10n_fr_pdp/utils/__init__.py`
- `addons/l10n_fr_pdp/utils/cdar.py`
- `addons/l10n_fr_pdp/utils/drom_com_territories.py`
- `addons/l10n_fr_pdp/views/account_move_views.xml`
- `addons/l10n_fr_pdp/views/account_peppol_response_views.xml`
- `addons/l10n_fr_pdp/views/l10n_fr_account_inherit.xml`
- `addons/l10n_fr_pdp/views/pdp_flow_views.xml`
- `addons/l10n_fr_pdp/views/pdp_send_wizard_views.xml`
- `addons/l10n_fr_pdp/views/res_config_settings_views.xml`
- `addons/l10n_fr_pdp/views/res_partner_views.xml`
- `addons/l10n_fr_pdp/wizard/__init__.py`
- `addons/l10n_fr_pdp/wizard/account_move_send_wizard.py`
- `addons/l10n_fr_pdp/wizard/l10n_fr_pdp_partner_lookup.py`
- `addons/l10n_fr_pdp/wizard/l10n_fr_pdp_partner_lookup.xml`
- `addons/l10n_fr_pdp/wizard/pdp_registration.py`
- `addons/l10n_fr_pdp/wizard/pdp_registration_views.xml`
- `addons/l10n_fr_pdp/wizard/pdp_response_wizard.py`
- `addons/l10n_fr_pdp/wizard/pdp_response_wizard_views.xml`
- `addons/l10n_fr_pdp/wizard/pdp_send_wizard.py`
