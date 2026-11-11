# Module: l10n_es_edi_verifactu

- **Module ID:** MOD-179
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_es_edi_verifactu`
- **Manifest:** `addons/l10n_es_edi_verifactu/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Module for sending Spanish Veri*Factu XML to the AEAT

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 57 files, including 22 Python, 10 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_es`, `certificate`.

## 2. Module structure

- Model/business logic files: 12
- Controller/API files: 0
- XML/data/view/template files: 10
- Browser asset files: 0
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 5
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_es_edi_verifactu/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 12 model declarations, 128 methods, 0 constraint handlers, 0 onchange handlers, and 11 dependency declarations.
- **Evidence:** `addons/l10n_es_edi_verifactu/models/res_partner.py:4`, `addons/l10n_es_edi_verifactu/models/res_config_settings.py:4`, `addons/l10n_es_edi_verifactu/models/verifactu_issuer.py:5`, `addons/l10n_es_edi_verifactu/models/account_tax.py:4`, `addons/l10n_es_edi_verifactu/models/verifactu_document.py:83`, `addons/l10n_es_edi_verifactu/models/certificate.py:4`, `addons/l10n_es_edi_verifactu/models/account_move.py:6`, `addons/l10n_es_edi_verifactu/models/account_journal_dashboard.py:4`, `addons/l10n_es_edi_verifactu/models/account_move_send.py:5`, `addons/l10n_es_edi_verifactu/models/res_company.py:5`, `addons/l10n_es_edi_verifactu/wizard/account_move_reversal.py:4`, `addons/l10n_es_edi_verifactu/wizard/account_resequence.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 10 XML files and 0 JavaScript/TypeScript files; static XML analysis found 20 record/template/menu identifiers.
- **Evidence:** `addons/l10n_es_edi_verifactu/demo/demo_company.xml:3`, `addons/l10n_es_edi_verifactu/demo/demo_certificate.xml:3`, `addons/l10n_es_edi_verifactu/wizard/account_resequence_views.xml:4`, `addons/l10n_es_edi_verifactu/data/ir_cron.xml:2`, `addons/l10n_es_edi_verifactu/views/res_config_settings_views.xml:3`, `addons/l10n_es_edi_verifactu/views/report_invoice.xml:3`, `addons/l10n_es_edi_verifactu/views/account_journal_dashboard_view.xml:3`, `addons/l10n_es_edi_verifactu/views/account_move_views.xml:5`, `addons/l10n_es_edi_verifactu/views/account_move_views.xml:18`, `addons/l10n_es_edi_verifactu/views/account_move_views.xml:34`, `addons/l10n_es_edi_verifactu/views/account_move_views.xml:47`, `addons/l10n_es_edi_verifactu/views/account_move_views.xml:63`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_es_edi_verifactu/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 5 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_es_edi_verifactu/__manifest__.py`, `addons/l10n_es_edi_verifactu/data/ir_cron.xml`, `addons/l10n_es_edi_verifactu/views/account_move_views.xml`, `addons/l10n_es_edi_verifactu/tests/common.py`, `addons/l10n_es_edi_verifactu/tests/test_document.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/l10n_es_edi_verifactu/tests/test_verifactu_partner_id_types.py`, `addons/l10n_es_edi_verifactu/tests/test_json.py`, `addons/l10n_es_edi_verifactu/tests/common.py`, `addons/l10n_es_edi_verifactu/tests/test_document.py`, `addons/l10n_es_edi_verifactu/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 10; representative identifiers: `base.demo_company_es`, `test_certificate_juridical_person`, `view_account_resequence_inherit_l10n_es_edi_verifactu`, `cron_verifactu_batch`, `res_config_settings_view_form`, `report_invoice_document`, `account_journal_dashboard_kanban_view_inherit_verifactu`, `view_account_move_filter`, `view_account_invoice_filter`, `view_account_move_filter_vf_rejected`, `view_move_tree`, `view_invoice_tree`, `view_move_form_inherit_l10n_es_edi_verifactu`, `action_l10n_es_edi_verifactu_button_cancel`, `view_l10n_es_edi_verifactu_document_form`, `certificate_certificate_view_search`, `l10n_es_edi_verifactu_certificate_action`, `certificate_certificate_view_form`, `Veri*Factu (Spain)`, `Certificates`
- Menus: 2; representative evidence: `addons/l10n_es_edi_verifactu/views/certificate_certificate_views.xml:37`, `addons/l10n_es_edi_verifactu/views/certificate_certificate_views.xml:42`
- Templates: 1; representative evidence: `addons/l10n_es_edi_verifactu/views/report_invoice.xml:3`
- View/action field declarations: 26; representative evidence: `addons/l10n_es_edi_verifactu/wizard/account_resequence_views.xml:6`, `addons/l10n_es_edi_verifactu/wizard/account_resequence_views.xml:8`, `addons/l10n_es_edi_verifactu/views/res_config_settings_views.xml:5`, `addons/l10n_es_edi_verifactu/views/res_config_settings_views.xml:7`, `addons/l10n_es_edi_verifactu/views/account_journal_dashboard_view.xml:5`, `addons/l10n_es_edi_verifactu/views/account_journal_dashboard_view.xml:7`, `addons/l10n_es_edi_verifactu/views/account_move_views.xml:7`, `addons/l10n_es_edi_verifactu/views/account_move_views.xml:9`, `addons/l10n_es_edi_verifactu/views/account_move_views.xml:20`, `addons/l10n_es_edi_verifactu/views/account_move_views.xml:22`, `addons/l10n_es_edi_verifactu/views/account_move_views.xml:36`, `addons/l10n_es_edi_verifactu/views/account_move_views.xml:38`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_es_edi_verifactu/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_es_edi_verifactu/__manifest__.py`, `addons/l10n_es_edi_verifactu/data/ir_cron.xml`, `addons/l10n_es_edi_verifactu/views/account_move_views.xml`, `addons/l10n_es_edi_verifactu/tests/common.py`, `addons/l10n_es_edi_verifactu/tests/test_document.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 12
- Representative model evidence: inherits `res.partner` (addons/l10n_es_edi_verifactu/models/res_partner.py:4); inherits `res.config.settings` (addons/l10n_es_edi_verifactu/models/res_config_settings.py:4); `l10n_es_edi_verifactu.issuer` (addons/l10n_es_edi_verifactu/models/verifactu_issuer.py:5); inherits `account.tax` (addons/l10n_es_edi_verifactu/models/account_tax.py:4); `l10n_es_edi_verifactu.document` (addons/l10n_es_edi_verifactu/models/verifactu_document.py:83); inherits `certificate.certificate` (addons/l10n_es_edi_verifactu/models/certificate.py:4); inherits `account.move` (addons/l10n_es_edi_verifactu/models/account_move.py:6); inherits `account.journal` (addons/l10n_es_edi_verifactu/models/account_journal_dashboard.py:4); inherits `account.move.send` (addons/l10n_es_edi_verifactu/models/account_move_send.py:5); inherits `res.company` (addons/l10n_es_edi_verifactu/models/res_company.py:5); inherits `account.move.reversal` (addons/l10n_es_edi_verifactu/wizard/account_move_reversal.py:4); inherits `account.resequence.wizard` (addons/l10n_es_edi_verifactu/wizard/account_resequence.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_es`, `certificate`
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

- `addons/l10n_es_edi_verifactu/__init__.py`
- `addons/l10n_es_edi_verifactu/__manifest__.py`
- `addons/l10n_es_edi_verifactu/const.py`
- `addons/l10n_es_edi_verifactu/data/ir_cron.xml`
- `addons/l10n_es_edi_verifactu/data/neutralize.sql`
- `addons/l10n_es_edi_verifactu/data/template/account.tax-es_common.csv`
- `addons/l10n_es_edi_verifactu/demo/certificates/Certificado_PF_99999910G_CERTIFICADO_FISICA_PRUEBAS_5_Pre.pfx`
- `addons/l10n_es_edi_verifactu/demo/certificates/Certificado_RPJ_A39200019_CERTIFICADO_ENTIDAD_PRUEBAS_5_Pre.p12`
- `addons/l10n_es_edi_verifactu/demo/demo_certificate.xml`
- `addons/l10n_es_edi_verifactu/demo/demo_company.xml`
- `addons/l10n_es_edi_verifactu/i18n/es.po`
- `addons/l10n_es_edi_verifactu/i18n/l10n_es_edi_verifactu.pot`
- `addons/l10n_es_edi_verifactu/models/__init__.py`
- `addons/l10n_es_edi_verifactu/models/account_journal_dashboard.py`
- `addons/l10n_es_edi_verifactu/models/account_move.py`
- `addons/l10n_es_edi_verifactu/models/account_move_send.py`
- `addons/l10n_es_edi_verifactu/models/account_tax.py`
- `addons/l10n_es_edi_verifactu/models/certificate.py`
- `addons/l10n_es_edi_verifactu/models/res_company.py`
- `addons/l10n_es_edi_verifactu/models/res_config_settings.py`
- `addons/l10n_es_edi_verifactu/models/res_partner.py`
- `addons/l10n_es_edi_verifactu/models/verifactu_document.py`
- `addons/l10n_es_edi_verifactu/models/verifactu_issuer.py`
- `addons/l10n_es_edi_verifactu/security/ir.access.csv`
- `addons/l10n_es_edi_verifactu/static/src/css/warning.scss`
- `addons/l10n_es_edi_verifactu/tests/__init__.py`
- `addons/l10n_es_edi_verifactu/tests/common.py`
- `addons/l10n_es_edi_verifactu/tests/files/test_invoice_1.json`
- `addons/l10n_es_edi_verifactu/tests/files/test_invoice_1_correction_substitution.json`
- `addons/l10n_es_edi_verifactu/tests/files/test_invoice_1_credit_note.json`
- `addons/l10n_es_edi_verifactu/tests/files/test_invoice_1_reversal_for_substitution.json`
- `addons/l10n_es_edi_verifactu/tests/files/test_invoice_2.json`
- `addons/l10n_es_edi_verifactu/tests/files/test_invoice_3.json`
- `addons/l10n_es_edi_verifactu/tests/files/test_invoice_4.json`
- `addons/l10n_es_edi_verifactu/tests/files/test_invoice_cancellation_1.json`
- `addons/l10n_es_edi_verifactu/tests/files/test_invoice_export.json`
- `addons/l10n_es_edi_verifactu/tests/files/test_invoice_multi_currency_1.json`
- `addons/l10n_es_edi_verifactu/tests/files/test_invoice_simplified_partner.json`
- `addons/l10n_es_edi_verifactu/tests/files/test_multiple_invoices_with_predecessor.json`
- `addons/l10n_es_edi_verifactu/tests/responses/batch_single_accepted_cancellation.json`
- `addons/l10n_es_edi_verifactu/tests/responses/batch_single_accepted_registration.json`
- `addons/l10n_es_edi_verifactu/tests/responses/batch_single_duplicate_original_registered_with_errors.json`
- `addons/l10n_es_edi_verifactu/tests/responses/batch_single_registered_with_errors_registration.json`
- `addons/l10n_es_edi_verifactu/tests/responses/batch_single_rejected_registration.json`
- `addons/l10n_es_edi_verifactu/tests/test_document.py`
- `addons/l10n_es_edi_verifactu/tests/test_json.py`
- `addons/l10n_es_edi_verifactu/tests/test_verifactu_partner_id_types.py`
- `addons/l10n_es_edi_verifactu/views/account_journal_dashboard_view.xml`
- `addons/l10n_es_edi_verifactu/views/account_move_views.xml`
- `addons/l10n_es_edi_verifactu/views/certificate_certificate_views.xml`
- `addons/l10n_es_edi_verifactu/views/l10n_es_edi_verifactu_document_views.xml`
- `addons/l10n_es_edi_verifactu/views/report_invoice.xml`
- `addons/l10n_es_edi_verifactu/views/res_config_settings_views.xml`
- `addons/l10n_es_edi_verifactu/wizard/__init__.py`
- `addons/l10n_es_edi_verifactu/wizard/account_move_reversal.py`
- `addons/l10n_es_edi_verifactu/wizard/account_resequence.py`
- `addons/l10n_es_edi_verifactu/wizard/account_resequence_views.xml`
