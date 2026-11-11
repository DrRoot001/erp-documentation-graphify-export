# Module: account_edi

- **Module ID:** MOD-004
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/account_edi`
- **Manifest:** `addons/account_edi/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Electronic Data Interchange
=======================================
EDI is the electronic interchange of business information using a standardized format.

This is the base module for import and export of invoices in various EDI formats, and the
the transmission of said documents to various parties involved in the exchange (other company,
governements, etc.)

**Scope evidence:** The module contains 70 files, including 16 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 6
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/account_edi/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 72 methods, 0 constraint handlers, 0 onchange handlers, and 11 dependency declarations.
- **Evidence:** `addons/account_edi/models/account_edi_document.py:14`, `addons/account_edi/models/account_edi_format.py:7`, `addons/account_edi/models/ir_actions_report.py:9`, `addons/account_edi/models/account_journal.py:10`, `addons/account_edi/models/account_move.py:12`, `addons/account_edi/models/account_move_send.py:4`, `addons/account_edi/models/ir_attachment.py:7`, `addons/account_edi/wizard/account_resequence.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 10 record/template/menu identifiers.
- **Evidence:** `addons/account_edi/data/cron.xml:2`, `addons/account_edi/views/account_edi_document_views.xml:4`, `addons/account_edi/views/account_move_views.xml:5`, `addons/account_edi/views/account_move_views.xml:12`, `addons/account_edi/views/account_move_views.xml:29`, `addons/account_edi/views/account_move_views.xml:42`, `addons/account_edi/views/account_move_views.xml:55`, `addons/account_edi/views/account_move_views.xml:68`, `addons/account_edi/views/account_move_views.xml:83`, `addons/account_edi/views/account_journal_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/account_edi/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 6 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/account_edi/models/account_edi_document.py`, `addons/account_edi/models/account_edi_format.py`, `addons/account_edi/models/account_move.py`, `addons/account_edi/data/cron.xml`, `addons/account_edi/tests/test_edi.py`, `addons/account_edi/tests/common.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/account_edi/models/ir_actions_report.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/account_edi/tests/test_edi.py`, `addons/account_edi/tests/test_import_vendor_bill.py`, `addons/account_edi/tests/common.py`, `addons/account_edi/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `ir_cron_edi_network`, `view_tree_account_edi_document`, `account_edi.action_open_edi_documents`, `view_out_invoice_tree_inherit`, `view_out_credit_note_tree_inherit`, `view_in_invoice_refund_tree_inherit`, `view_in_bill_tree_inherit`, `view_account_invoice_filter`, `view_move_form_inherit`, `view_account_journal_form_inherited`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 18; representative evidence: `addons/account_edi/views/account_edi_document_views.xml:6`, `addons/account_edi/views/account_edi_document_views.xml:7`, `addons/account_edi/views/account_move_views.xml:7`, `addons/account_edi/views/account_move_views.xml:8`, `addons/account_edi/views/account_move_views.xml:14`, `addons/account_edi/views/account_move_views.xml:16`, `addons/account_edi/views/account_move_views.xml:31`, `addons/account_edi/views/account_move_views.xml:33`, `addons/account_edi/views/account_move_views.xml:44`, `addons/account_edi/views/account_move_views.xml:46`, `addons/account_edi/views/account_move_views.xml:57`, `addons/account_edi/views/account_move_views.xml:59`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/account_edi/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/account_edi/models/account_edi_document.py`, `addons/account_edi/models/account_edi_format.py`, `addons/account_edi/models/account_move.py`, `addons/account_edi/data/cron.xml`, `addons/account_edi/tests/test_edi.py`, `addons/account_edi/tests/common.py`
- **Report entry points:** `addons/account_edi/models/ir_actions_report.py`

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: `account.edi.document` (addons/account_edi/models/account_edi_document.py:14); `account.edi.format` (addons/account_edi/models/account_edi_format.py:7); inherits `ir.actions.report` (addons/account_edi/models/ir_actions_report.py:9); inherits `account.journal` (addons/account_edi/models/account_journal.py:10); inherits `account.move` (addons/account_edi/models/account_move.py:12); inherits `account.move.send` (addons/account_edi/models/account_move_send.py:4); inherits `ir.attachment` (addons/account_edi/models/ir_attachment.py:7); inherits `account.resequence.wizard` (addons/account_edi/wizard/account_resequence.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`
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

- `addons/account_edi/__init__.py`
- `addons/account_edi/__manifest__.py`
- `addons/account_edi/data/cron.xml`
- `addons/account_edi/i18n/account_edi.pot`
- `addons/account_edi/i18n/ar.po`
- `addons/account_edi/i18n/az.po`
- `addons/account_edi/i18n/bg.po`
- `addons/account_edi/i18n/bs.po`
- `addons/account_edi/i18n/ca.po`
- `addons/account_edi/i18n/cs.po`
- `addons/account_edi/i18n/da.po`
- `addons/account_edi/i18n/de.po`
- `addons/account_edi/i18n/el.po`
- `addons/account_edi/i18n/es.po`
- `addons/account_edi/i18n/es_419.po`
- `addons/account_edi/i18n/et.po`
- `addons/account_edi/i18n/fa.po`
- `addons/account_edi/i18n/fi.po`
- `addons/account_edi/i18n/fr.po`
- `addons/account_edi/i18n/he.po`
- `addons/account_edi/i18n/hi.po`
- `addons/account_edi/i18n/hr.po`
- `addons/account_edi/i18n/hu.po`
- `addons/account_edi/i18n/id.po`
- `addons/account_edi/i18n/it.po`
- `addons/account_edi/i18n/ja.po`
- `addons/account_edi/i18n/kab.po`
- `addons/account_edi/i18n/ko.po`
- `addons/account_edi/i18n/ku.po`
- `addons/account_edi/i18n/lo.po`
- `addons/account_edi/i18n/lt.po`
- `addons/account_edi/i18n/lv.po`
- `addons/account_edi/i18n/mn.po`
- `addons/account_edi/i18n/my.po`
- `addons/account_edi/i18n/nb.po`
- `addons/account_edi/i18n/nl.po`
- `addons/account_edi/i18n/pl.po`
- `addons/account_edi/i18n/pt.po`
- `addons/account_edi/i18n/pt_BR.po`
- `addons/account_edi/i18n/ro.po`
- `addons/account_edi/i18n/ru.po`
- `addons/account_edi/i18n/sk.po`
- `addons/account_edi/i18n/sl.po`
- `addons/account_edi/i18n/sr@latin.po`
- `addons/account_edi/i18n/sv.po`
- `addons/account_edi/i18n/th.po`
- `addons/account_edi/i18n/tr.po`
- `addons/account_edi/i18n/uk.po`
- `addons/account_edi/i18n/uz.po`
- `addons/account_edi/i18n/vi.po`
- `addons/account_edi/i18n/zh_CN.po`
- `addons/account_edi/i18n/zh_TW.po`
- `addons/account_edi/models/__init__.py`
- `addons/account_edi/models/account_edi_document.py`
- `addons/account_edi/models/account_edi_format.py`
- `addons/account_edi/models/account_journal.py`
- `addons/account_edi/models/account_move.py`
- `addons/account_edi/models/account_move_send.py`
- `addons/account_edi/models/ir_actions_report.py`
- `addons/account_edi/models/ir_attachment.py`
- `addons/account_edi/security/ir.access.csv`
- `addons/account_edi/tests/__init__.py`
- `addons/account_edi/tests/common.py`
- `addons/account_edi/tests/test_edi.py`
- `addons/account_edi/tests/test_import_vendor_bill.py`
- `addons/account_edi/views/account_edi_document_views.xml`
- `addons/account_edi/views/account_journal_views.xml`
- `addons/account_edi/views/account_move_views.xml`
- `addons/account_edi/wizard/__init__.py`
- `addons/account_edi/wizard/account_resequence.py`
