# Module: l10n_es_edi_sii

- **Module ID:** MOD-176
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_es_edi_sii`
- **Manifest:** `addons/l10n_es_edi_sii/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module sends the taxes information (mostly VAT) of the
vendor bills and customer invoices to the SII.  It is called
Procedimiento G417 - IVA. Llevanza de libros registro.  It is
required for every company with a turnover of +6M€ and others can
already make use of it.  The invoices are automatically
sent after validation.

How the information is sent to the SII depends on the
configuration that is put in the taxes.  The taxes
that were in the chart template (l10n_es) are automatically
configured to have the right type.  It is possible however
that extra taxes need to be created for certain exempt/no sujeta reasons.

You need to configure your certificate and the tax agency.

**Scope evidence:** The module contains 28 files, including 17 Python, 6 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `certificate`, `l10n_es`.

## 2. Module structure

- Model/business logic files: 9
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 0
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_es_edi_sii/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 9 model declarations, 84 methods, 0 constraint handlers, 0 onchange handlers, and 7 dependency declarations.
- **Evidence:** `addons/l10n_es_edi_sii/models/res_config_settings.py:6`, `addons/l10n_es_edi_sii/models/account_journal.py:9`, `addons/l10n_es_edi_sii/models/certificate.py:4`, `addons/l10n_es_edi_sii/models/account_move.py:15`, `addons/l10n_es_edi_sii/models/l10n_es_edi_sii_document.py:75`, `addons/l10n_es_edi_sii/models/account_move_send.py:5`, `addons/l10n_es_edi_sii/models/account_move_send.py:56`, `addons/l10n_es_edi_sii/models/res_company.py:6`, `addons/l10n_es_edi_sii/wizard/account_move_send_wizard.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 0 JavaScript/TypeScript files; static XML analysis found 14 record/template/menu identifiers.
- **Evidence:** `addons/l10n_es_edi_sii/demo/demo_company.xml:3`, `addons/l10n_es_edi_sii/demo/demo_certificate.xml:4`, `addons/l10n_es_edi_sii/views/res_config_settings_views.xml:3`, `addons/l10n_es_edi_sii/views/account_move_views.xml:4`, `addons/l10n_es_edi_sii/views/account_move_views.xml:13`, `addons/l10n_es_edi_sii/views/account_move_views.xml:93`, `addons/l10n_es_edi_sii/views/account_move_views.xml:115`, `addons/l10n_es_edi_sii/views/account_move_views.xml:127`, `addons/l10n_es_edi_sii/views/account_journal_dashboard_views.xml:3`, `addons/l10n_es_edi_sii/views/l10n_es_edi_sii_certificate_views.xml:4`, `addons/l10n_es_edi_sii/views/l10n_es_edi_sii_certificate_views.xml:15`, `addons/l10n_es_edi_sii/views/l10n_es_edi_sii_certificate_views.xml:25`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_es_edi_sii/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_es_edi_sii/views/account_move_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/l10n_es_edi_sii/tests/test_edi_xml.py`, `addons/l10n_es_edi_sii/tests/common.py`, `addons/l10n_es_edi_sii/tests/__init__.py`, `addons/l10n_es_edi_sii/tests/test_account_journal.py`, `addons/l10n_es_edi_sii/tests/test_edi_web_services.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `base.demo_company_es`, `demo_certificate`, `res_config_settings_view_form`, `action_l10n_es_send_sii`, `view_move_form_inherit_l10n_es_edi`, `view_invoice_tree_inherit_l10n_es_edi_sii`, `action_request_cancel`, `view_account_invoice_filter_inherit_l10n_es_edi_sii`, `account_journal_dashboard_kanban_view_sii`, `certificate_certificate_view_search`, `l10n_es_edi_sii_certificate_action`, `certificate_certificate_view_form`, `Spain SII`, `Certificates`
- Menus: 2; representative evidence: `addons/l10n_es_edi_sii/views/l10n_es_edi_sii_certificate_views.xml:36`, `addons/l10n_es_edi_sii/views/l10n_es_edi_sii_certificate_views.xml:41`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 16; representative evidence: `addons/l10n_es_edi_sii/views/res_config_settings_views.xml:5`, `addons/l10n_es_edi_sii/views/res_config_settings_views.xml:7`, `addons/l10n_es_edi_sii/views/account_move_views.xml:15`, `addons/l10n_es_edi_sii/views/account_move_views.xml:17`, `addons/l10n_es_edi_sii/views/account_move_views.xml:95`, `addons/l10n_es_edi_sii/views/account_move_views.xml:97`, `addons/l10n_es_edi_sii/views/account_move_views.xml:129`, `addons/l10n_es_edi_sii/views/account_move_views.xml:131`, `addons/l10n_es_edi_sii/views/account_journal_dashboard_views.xml:5`, `addons/l10n_es_edi_sii/views/account_journal_dashboard_views.xml:7`, `addons/l10n_es_edi_sii/views/l10n_es_edi_sii_certificate_views.xml:6`, `addons/l10n_es_edi_sii/views/l10n_es_edi_sii_certificate_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_es_edi_sii/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_es_edi_sii/views/account_move_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 9
- Representative model evidence: inherits `res.config.settings` (addons/l10n_es_edi_sii/models/res_config_settings.py:6); inherits `account.journal` (addons/l10n_es_edi_sii/models/account_journal.py:9); inherits `certificate.certificate` (addons/l10n_es_edi_sii/models/certificate.py:4); inherits `account.move` (addons/l10n_es_edi_sii/models/account_move.py:15); `l10n_es_edi_sii.document` (addons/l10n_es_edi_sii/models/l10n_es_edi_sii_document.py:75); inherits `account.move.send` (addons/l10n_es_edi_sii/models/account_move_send.py:5); inherits `account.move.send.batch.wizard` (addons/l10n_es_edi_sii/models/account_move_send.py:56); inherits `res.company` (addons/l10n_es_edi_sii/models/res_company.py:6); inherits `account.move.send.wizard` (addons/l10n_es_edi_sii/wizard/account_move_send_wizard.py:5)
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

- `addons/l10n_es_edi_sii/__init__.py`
- `addons/l10n_es_edi_sii/__manifest__.py`
- `addons/l10n_es_edi_sii/data/neutralize.sql`
- `addons/l10n_es_edi_sii/demo/certificates/aeat_1234.p12`
- `addons/l10n_es_edi_sii/demo/demo_certificate.xml`
- `addons/l10n_es_edi_sii/demo/demo_company.xml`
- `addons/l10n_es_edi_sii/i18n/es.po`
- `addons/l10n_es_edi_sii/i18n/l10n_es_edi_sii.pot`
- `addons/l10n_es_edi_sii/models/__init__.py`
- `addons/l10n_es_edi_sii/models/account_journal.py`
- `addons/l10n_es_edi_sii/models/account_move.py`
- `addons/l10n_es_edi_sii/models/account_move_send.py`
- `addons/l10n_es_edi_sii/models/certificate.py`
- `addons/l10n_es_edi_sii/models/l10n_es_edi_sii_document.py`
- `addons/l10n_es_edi_sii/models/res_company.py`
- `addons/l10n_es_edi_sii/models/res_config_settings.py`
- `addons/l10n_es_edi_sii/security/ir.access.csv`
- `addons/l10n_es_edi_sii/tests/__init__.py`
- `addons/l10n_es_edi_sii/tests/common.py`
- `addons/l10n_es_edi_sii/tests/test_account_journal.py`
- `addons/l10n_es_edi_sii/tests/test_edi_web_services.py`
- `addons/l10n_es_edi_sii/tests/test_edi_xml.py`
- `addons/l10n_es_edi_sii/views/account_journal_dashboard_views.xml`
- `addons/l10n_es_edi_sii/views/account_move_views.xml`
- `addons/l10n_es_edi_sii/views/l10n_es_edi_sii_certificate_views.xml`
- `addons/l10n_es_edi_sii/views/res_config_settings_views.xml`
- `addons/l10n_es_edi_sii/wizard/__init__.py`
- `addons/l10n_es_edi_sii/wizard/account_move_send_wizard.py`
