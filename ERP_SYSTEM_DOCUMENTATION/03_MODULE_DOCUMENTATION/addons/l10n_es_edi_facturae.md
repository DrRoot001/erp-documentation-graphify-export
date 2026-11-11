# Module: l10n_es_edi_facturae

- **Module ID:** MOD-175
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_es_edi_facturae`
- **Manifest:** `addons/l10n_es_edi_facturae/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module create the Facturae file required to send the invoices information to the General State Administrations.
It allows the export and signature of the signing of Facturae files.
The current version of Facturae supported is the 3.2.2

for more informations, see https://www.facturae.gob.es/face/Paginas/FACE.aspx

**Scope evidence:** The module contains 49 files, including 17 Python, 24 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `certificate`, `l10n_es`.

## 2. Module structure

- Model/business logic files: 11
- Controller/API files: 0
- XML/data/view/template files: 24
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_es_edi_facturae/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 11 model declarations, 75 methods, 2 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/l10n_es_edi_facturae/models/res_partner.py:6`, `addons/l10n_es_edi_facturae/models/res_partner.py:14`, `addons/l10n_es_edi_facturae/models/uom_uom.py:4`, `addons/l10n_es_edi_facturae/models/account_tax.py:4`, `addons/l10n_es_edi_facturae/models/account_chart_template.py:5`, `addons/l10n_es_edi_facturae/models/certificate.py:6`, `addons/l10n_es_edi_facturae/models/account_move.py:79`, `addons/l10n_es_edi_facturae/models/account_move_send.py:9`, `addons/l10n_es_edi_facturae/models/res_company.py:4`, `addons/l10n_es_edi_facturae/wizard/account_move_send_wizard.py:4`, `addons/l10n_es_edi_facturae/wizard/account_move_reversal.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 24 XML files and 0 JavaScript/TypeScript files; static XML analysis found 29 record/template/menu identifiers.
- **Evidence:** `addons/l10n_es_edi_facturae/demo/l10n_es_edi_facturae_demo.xml:4`, `addons/l10n_es_edi_facturae/demo/l10n_es_edi_facturae_demo.xml:12`, `addons/l10n_es_edi_facturae/demo/l10n_es_edi_facturae_demo.xml:25`, `addons/l10n_es_edi_facturae/wizard/account_move_reversal_view.xml:5`, `addons/l10n_es_edi_facturae/wizard/account_move_reversal_view.xml:17`, `addons/l10n_es_edi_facturae/data/signature_templates.xml:3`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:5`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:26`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:35`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:45`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:56`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:65`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_es_edi_facturae/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_es_edi_facturae/tests/test_edi_xml.py`, `addons/l10n_es_edi_facturae/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 24; representative identifiers: `face_certificate_demo`, `partner_demo_bilbao_es`, `partner_demo_bilbao_ac_es`, `view_tax_tree_inherit_l10n_es_edi_facturae`, `view_account_move_reversal_inherit_l10n_es_edi_facturae`, `template_xades_signature`, `address_type`, `contact_details_type`, `legal_entity_type`, `individual_type`, `tax_identification_type`, `administrative_centers_type`, `business_type`, `tax_type`, `invoice_line_type`, `corrective_type`, `invoice_type`, `account_invoice_facturae_export`, `uom_uom_view_list`, `uom_uom_view_form`
- Menus: 2; representative evidence: `addons/l10n_es_edi_facturae/views/account_menuitem.xml:4`, `addons/l10n_es_edi_facturae/views/account_menuitem.xml:6`
- Templates: 13; representative evidence: `addons/l10n_es_edi_facturae/data/signature_templates.xml:3`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:5`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:26`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:35`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:45`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:56`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:65`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:84`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:96`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:125`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:170`, `addons/l10n_es_edi_facturae/data/facturae_templates.xml:185`
- View/action field declarations: 22; representative evidence: `addons/l10n_es_edi_facturae/wizard/account_move_reversal_view.xml:8`, `addons/l10n_es_edi_facturae/wizard/account_move_reversal_view.xml:9`, `addons/l10n_es_edi_facturae/wizard/account_move_reversal_view.xml:20`, `addons/l10n_es_edi_facturae/wizard/account_move_reversal_view.xml:21`, `addons/l10n_es_edi_facturae/views/uom_uom_views.xml:5`, `addons/l10n_es_edi_facturae/views/uom_uom_views.xml:7`, `addons/l10n_es_edi_facturae/views/uom_uom_views.xml:15`, `addons/l10n_es_edi_facturae/views/uom_uom_views.xml:17`, `addons/l10n_es_edi_facturae/views/account_move_views.xml:6`, `addons/l10n_es_edi_facturae/views/account_move_views.xml:8`, `addons/l10n_es_edi_facturae/views/account_tax_views.xml:7`, `addons/l10n_es_edi_facturae/views/account_tax_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_es_edi_facturae/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 11
- Representative model evidence: `l10n_es_edi_facturae.ac_role_type` (addons/l10n_es_edi_facturae/models/res_partner.py:6); inherits `res.partner` (addons/l10n_es_edi_facturae/models/res_partner.py:14); inherits `uom.uom` (addons/l10n_es_edi_facturae/models/uom_uom.py:4); inherits `account.tax` (addons/l10n_es_edi_facturae/models/account_tax.py:4); inherits `account.chart.template` (addons/l10n_es_edi_facturae/models/account_chart_template.py:5); inherits `certificate.certificate` (addons/l10n_es_edi_facturae/models/certificate.py:6); inherits `account.move` (addons/l10n_es_edi_facturae/models/account_move.py:79); inherits `account.move.send` (addons/l10n_es_edi_facturae/models/account_move_send.py:9); inherits `res.company` (addons/l10n_es_edi_facturae/models/res_company.py:4); inherits `account.move.send.wizard` (addons/l10n_es_edi_facturae/wizard/account_move_send_wizard.py:4); inherits `account.move.reversal` (addons/l10n_es_edi_facturae/wizard/account_move_reversal.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `certificate`, `l10n_es`
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

- `addons/l10n_es_edi_facturae/__init__.py`
- `addons/l10n_es_edi_facturae/__manifest__.py`
- `addons/l10n_es_edi_facturae/data/facturae_templates.xml`
- `addons/l10n_es_edi_facturae/data/l10n_es_edi_facturae.ac_role_type.csv`
- `addons/l10n_es_edi_facturae/data/signature_templates.xml`
- `addons/l10n_es_edi_facturae/data/template/account.tax-es_common.csv`
- `addons/l10n_es_edi_facturae/data/uom.uom.csv`
- `addons/l10n_es_edi_facturae/demo/certificate_demo.pfx`
- `addons/l10n_es_edi_facturae/demo/l10n_es_edi_facturae_demo.xml`
- `addons/l10n_es_edi_facturae/i18n/es.po`
- `addons/l10n_es_edi_facturae/i18n/l10n_es_edi_facturae.pot`
- `addons/l10n_es_edi_facturae/models/__init__.py`
- `addons/l10n_es_edi_facturae/models/account_chart_template.py`
- `addons/l10n_es_edi_facturae/models/account_move.py`
- `addons/l10n_es_edi_facturae/models/account_move_send.py`
- `addons/l10n_es_edi_facturae/models/account_tax.py`
- `addons/l10n_es_edi_facturae/models/certificate.py`
- `addons/l10n_es_edi_facturae/models/res_company.py`
- `addons/l10n_es_edi_facturae/models/res_partner.py`
- `addons/l10n_es_edi_facturae/models/uom_uom.py`
- `addons/l10n_es_edi_facturae/security/ir.access.csv`
- `addons/l10n_es_edi_facturae/tests/__init__.py`
- `addons/l10n_es_edi_facturae/tests/data/certificate_test.pfx`
- `addons/l10n_es_edi_facturae/tests/data/expected_ac_document.xml`
- `addons/l10n_es_edi_facturae/tests/data/expected_in_invoice_document.xml`
- `addons/l10n_es_edi_facturae/tests/data/expected_invoice_payment_means.xml`
- `addons/l10n_es_edi_facturae/tests/data/expected_invoice_period_document.xml`
- `addons/l10n_es_edi_facturae/tests/data/expected_out_invoice_4_decimals.xml`
- `addons/l10n_es_edi_facturae/tests/data/expected_out_invoice_negative.xml`
- `addons/l10n_es_edi_facturae/tests/data/expected_out_invoice_round_2.xml`
- `addons/l10n_es_edi_facturae/tests/data/expected_out_invoice_round_glob.xml`
- `addons/l10n_es_edi_facturae/tests/data/expected_out_invoice_withhold.xml`
- `addons/l10n_es_edi_facturae/tests/data/expected_refund_document.xml`
- `addons/l10n_es_edi_facturae/tests/data/expected_signed_document.xml`
- `addons/l10n_es_edi_facturae/tests/data/expected_simplified_document.xml`
- `addons/l10n_es_edi_facturae/tests/data/import_multiple_invoices.xml`
- `addons/l10n_es_edi_facturae/tests/data/import_withholding_invoice.xml`
- `addons/l10n_es_edi_facturae/tests/test_edi_xml.py`
- `addons/l10n_es_edi_facturae/views/account_menuitem.xml`
- `addons/l10n_es_edi_facturae/views/account_move_views.xml`
- `addons/l10n_es_edi_facturae/views/account_tax_views.xml`
- `addons/l10n_es_edi_facturae/views/l10n_es_edi_facturae_views.xml`
- `addons/l10n_es_edi_facturae/views/res_partner_views.xml`
- `addons/l10n_es_edi_facturae/views/uom_uom_views.xml`
- `addons/l10n_es_edi_facturae/wizard/__init__.py`
- `addons/l10n_es_edi_facturae/wizard/account_move_reversal.py`
- `addons/l10n_es_edi_facturae/wizard/account_move_reversal_view.xml`
- `addons/l10n_es_edi_facturae/wizard/account_move_send_wizard.py`
- `addons/l10n_es_edi_facturae/xml_utils.py`
