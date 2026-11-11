# Module: l10n_latam_invoice_document

- **Module ID:** MOD-260
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_latam_invoice_document`
- **Manifest:** `addons/l10n_latam_invoice_document/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** LATAM Document Types

**Manifest description:**

Functional
----------

In some Latinamerica countries, including Argentina and Chile, some accounting transactions like invoices and vendor bills are classified by a document types defined by the government fiscal authorities (In Argentina case ARCA, Chile case SII).

This module is intended to be extended by localizations in order to manage these document types and is an essential information that needs to be displayed in the printed reports and that needs to be easily identified, within the set of invoices as well of account moves.

Each document type have their own rules and sequence number, this last one is integrated with the invoice number and journal sequence in order to be easy for the localization user. In order to support or not this document types a Journal has a new option that lets to use document or not.

Technical
---------

If your localization needs this logic will then need to add this module as dependency and in your localization module extend:

* extend company's _localization_use_documents() method.
* create the data of the document types that exists for the specific country. The document type has a country field

**Scope evidence:** The module contains 26 files, including 15 Python, 7 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_debit_note`.

## 2. Module structure

- Model/business logic files: 9
- Controller/API files: 0
- XML/data/view/template files: 7
- Browser asset files: 0
- Security files: 1
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_latam_invoice_document/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 9 model declarations, 41 methods, 3 constraint handlers, 4 onchange handlers, and 14 dependency declarations.
- **Evidence:** `addons/l10n_latam_invoice_document/models/account_journal.py:7`, `addons/l10n_latam_invoice_document/models/account_chart_template.py:6`, `addons/l10n_latam_invoice_document/models/l10n_latam_document_type.py:5`, `addons/l10n_latam_invoice_document/models/account_move.py:9`, `addons/l10n_latam_invoice_document/models/account_move_line.py:6`, `addons/l10n_latam_invoice_document/models/res_company.py:5`, `addons/l10n_latam_invoice_document/wizards/account_move_reversal.py:7`, `addons/l10n_latam_invoice_document/wizards/account_debit_note.py:4`, `addons/l10n_latam_invoice_document/report/invoice_report.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 0 JavaScript/TypeScript files; static XML analysis found 21 record/template/menu identifiers.
- **Evidence:** `addons/l10n_latam_invoice_document/wizards/account_move_reversal_view.xml:4`, `addons/l10n_latam_invoice_document/report/invoice_report_view.xml:4`, `addons/l10n_latam_invoice_document/views/report_templates.xml:4`, `addons/l10n_latam_invoice_document/views/report_templates.xml:18`, `addons/l10n_latam_invoice_document/views/report_templates.xml:30`, `addons/l10n_latam_invoice_document/views/report_templates.xml:42`, `addons/l10n_latam_invoice_document/views/report_templates.xml:54`, `addons/l10n_latam_invoice_document/views/report_templates.xml:66`, `addons/l10n_latam_invoice_document/views/report_templates.xml:78`, `addons/l10n_latam_invoice_document/views/report_templates.xml:90`, `addons/l10n_latam_invoice_document/views/report_templates.xml:102`, `addons/l10n_latam_invoice_document/views/account_move_view.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_latam_invoice_document/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_latam_invoice_document/models/l10n_latam_document_type.py`, `addons/l10n_latam_invoice_document/views/l10n_latam_document_type_view.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `view_account_move_reversal`, `view_account_invoice_report_search`, `external_layout_footer_content`, `external_layout_standard`, `external_layout_bubble`, `external_layout_wave`, `external_layout_folder`, `external_layout_center`, `external_layout_dual`, `external_layout_lines`, `external_layout_compact`, `view_account_invoice_filter`, `view_account_move_filter`, `view_move_form`, `view_account_move_line_filter`, `view_account_journal_form`, `view_document_type_form`, `view_document_type_tree`, `view_document_type_filter`, `action_document_type`
- Menus: 1; representative evidence: `addons/l10n_latam_invoice_document/views/l10n_latam_document_type_view.xml:63`
- Templates: 9; representative evidence: `addons/l10n_latam_invoice_document/views/report_templates.xml:4`, `addons/l10n_latam_invoice_document/views/report_templates.xml:18`, `addons/l10n_latam_invoice_document/views/report_templates.xml:30`, `addons/l10n_latam_invoice_document/views/report_templates.xml:42`, `addons/l10n_latam_invoice_document/views/report_templates.xml:54`, `addons/l10n_latam_invoice_document/views/report_templates.xml:66`, `addons/l10n_latam_invoice_document/views/report_templates.xml:78`, `addons/l10n_latam_invoice_document/views/report_templates.xml:90`, `addons/l10n_latam_invoice_document/views/report_templates.xml:102`
- View/action field declarations: 21; representative evidence: `addons/l10n_latam_invoice_document/wizards/account_move_reversal_view.xml:6`, `addons/l10n_latam_invoice_document/wizards/account_move_reversal_view.xml:8`, `addons/l10n_latam_invoice_document/report/invoice_report_view.xml:6`, `addons/l10n_latam_invoice_document/report/invoice_report_view.xml:8`, `addons/l10n_latam_invoice_document/views/account_move_view.xml:6`, `addons/l10n_latam_invoice_document/views/account_move_view.xml:8`, `addons/l10n_latam_invoice_document/views/account_move_view.xml:20`, `addons/l10n_latam_invoice_document/views/account_move_view.xml:22`, `addons/l10n_latam_invoice_document/views/account_move_view.xml:34`, `addons/l10n_latam_invoice_document/views/account_move_view.xml:36`, `addons/l10n_latam_invoice_document/views/account_move_line_view.xml:6`, `addons/l10n_latam_invoice_document/views/account_move_line_view.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_latam_invoice_document/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/l10n_latam_invoice_document/models/l10n_latam_document_type.py`, `addons/l10n_latam_invoice_document/views/l10n_latam_document_type_view.xml`

## 7. Database interactions

- Model declarations: 9
- Representative model evidence: inherits `account.journal` (addons/l10n_latam_invoice_document/models/account_journal.py:7); inherits `account.chart.template` (addons/l10n_latam_invoice_document/models/account_chart_template.py:6); `l10n_latam.document.type` (addons/l10n_latam_invoice_document/models/l10n_latam_document_type.py:5); inherits `account.move` (addons/l10n_latam_invoice_document/models/account_move.py:9); inherits `account.move.line` (addons/l10n_latam_invoice_document/models/account_move_line.py:6); inherits `res.company` (addons/l10n_latam_invoice_document/models/res_company.py:5); inherits `account.move.reversal` (addons/l10n_latam_invoice_document/wizards/account_move_reversal.py:7); inherits `account.debit.note` (addons/l10n_latam_invoice_document/wizards/account_debit_note.py:4); inherits `account.invoice.report` (addons/l10n_latam_invoice_document/report/invoice_report.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `account_debit_note`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Present
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_latam_invoice_document/__init__.py`
- `addons/l10n_latam_invoice_document/__manifest__.py`
- `addons/l10n_latam_invoice_document/i18n/es_419.po`
- `addons/l10n_latam_invoice_document/i18n/l10n_latam_invoice_document.pot`
- `addons/l10n_latam_invoice_document/i18n/pt_BR.po`
- `addons/l10n_latam_invoice_document/migrations/1.1/post-migration.py`
- `addons/l10n_latam_invoice_document/models/__init__.py`
- `addons/l10n_latam_invoice_document/models/account_chart_template.py`
- `addons/l10n_latam_invoice_document/models/account_journal.py`
- `addons/l10n_latam_invoice_document/models/account_move.py`
- `addons/l10n_latam_invoice_document/models/account_move_line.py`
- `addons/l10n_latam_invoice_document/models/l10n_latam_document_type.py`
- `addons/l10n_latam_invoice_document/models/res_company.py`
- `addons/l10n_latam_invoice_document/report/__init__.py`
- `addons/l10n_latam_invoice_document/report/invoice_report.py`
- `addons/l10n_latam_invoice_document/report/invoice_report_view.xml`
- `addons/l10n_latam_invoice_document/security/ir.access.csv`
- `addons/l10n_latam_invoice_document/views/account_journal_view.xml`
- `addons/l10n_latam_invoice_document/views/account_move_line_view.xml`
- `addons/l10n_latam_invoice_document/views/account_move_view.xml`
- `addons/l10n_latam_invoice_document/views/l10n_latam_document_type_view.xml`
- `addons/l10n_latam_invoice_document/views/report_templates.xml`
- `addons/l10n_latam_invoice_document/wizards/__init__.py`
- `addons/l10n_latam_invoice_document/wizards/account_debit_note.py`
- `addons/l10n_latam_invoice_document/wizards/account_move_reversal.py`
- `addons/l10n_latam_invoice_document/wizards/account_move_reversal_view.xml`
