# Module: account_debit_note

- **Module ID:** MOD-003
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/account_debit_note`
- **Manifest:** `addons/account_debit_note/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Debit Notes

**Manifest description:**

In a lot of countries, a debit note is used as an increase of the amounts of an existing invoice
or in some specific cases to cancel a credit note.
It is like a regular invoice, but we need to keep track of the link with the original invoice.
The wizard used is similar as the one for the credit note.

**Scope evidence:** The module contains 64 files, including 9 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/account_debit_note/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 14 methods, 0 constraint handlers, 0 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/account_debit_note/models/account_journal.py:4`, `addons/account_debit_note/models/account_move.py:7`, `addons/account_debit_note/wizard/account_debit_note.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 8 record/template/menu identifiers.
- **Evidence:** `addons/account_debit_note/wizard/account_debit_note_view.xml:4`, `addons/account_debit_note/wizard/account_debit_note_view.xml:30`, `addons/account_debit_note/views/report_invoice.xml:4`, `addons/account_debit_note/views/account_move_view.xml:3`, `addons/account_debit_note/views/account_move_view.xml:40`, `addons/account_debit_note/views/account_move_view.xml:52`, `addons/account_debit_note/views/account_move_view.xml:65`, `addons/account_debit_note/views/account_journal_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/account_debit_note/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/account_debit_note/tests/__init__.py`, `addons/account_debit_note/tests/test_out_debit_note.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `view_account_debit_note`, `action_view_account_move_debit`, `report_invoice_document_inherit_debit_note`, `view_move_form_debit`, `view_account_move_filter_debit`, `view_account_invoice_filter_debit`, `view_account_move_line_filter_debit`, `view_account_journal_form_inherit_debit_note`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/account_debit_note/views/report_invoice.xml:4`
- View/action field declarations: 14; representative evidence: `addons/account_debit_note/wizard/account_debit_note_view.xml:6`, `addons/account_debit_note/wizard/account_debit_note_view.xml:7`, `addons/account_debit_note/wizard/account_debit_note_view.xml:32`, `addons/account_debit_note/wizard/account_debit_note_view.xml:33`, `addons/account_debit_note/views/account_move_view.xml:5`, `addons/account_debit_note/views/account_move_view.xml:7`, `addons/account_debit_note/views/account_move_view.xml:42`, `addons/account_debit_note/views/account_move_view.xml:44`, `addons/account_debit_note/views/account_move_view.xml:54`, `addons/account_debit_note/views/account_move_view.xml:56`, `addons/account_debit_note/views/account_move_view.xml:67`, `addons/account_debit_note/views/account_move_view.xml:69`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/account_debit_note/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `account.journal` (addons/account_debit_note/models/account_journal.py:4); inherits `account.move` (addons/account_debit_note/models/account_move.py:7); `account.debit.note` (addons/account_debit_note/wizard/account_debit_note.py:7)
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

- `addons/account_debit_note/__init__.py`
- `addons/account_debit_note/__manifest__.py`
- `addons/account_debit_note/i18n/account_debit_note.pot`
- `addons/account_debit_note/i18n/ar.po`
- `addons/account_debit_note/i18n/az.po`
- `addons/account_debit_note/i18n/bg.po`
- `addons/account_debit_note/i18n/bs.po`
- `addons/account_debit_note/i18n/ca.po`
- `addons/account_debit_note/i18n/cs.po`
- `addons/account_debit_note/i18n/da.po`
- `addons/account_debit_note/i18n/de.po`
- `addons/account_debit_note/i18n/el.po`
- `addons/account_debit_note/i18n/es.po`
- `addons/account_debit_note/i18n/es_419.po`
- `addons/account_debit_note/i18n/et.po`
- `addons/account_debit_note/i18n/fa.po`
- `addons/account_debit_note/i18n/fi.po`
- `addons/account_debit_note/i18n/fr.po`
- `addons/account_debit_note/i18n/fr_BE.po`
- `addons/account_debit_note/i18n/he.po`
- `addons/account_debit_note/i18n/hi.po`
- `addons/account_debit_note/i18n/hr.po`
- `addons/account_debit_note/i18n/hu.po`
- `addons/account_debit_note/i18n/id.po`
- `addons/account_debit_note/i18n/it.po`
- `addons/account_debit_note/i18n/ja.po`
- `addons/account_debit_note/i18n/kab.po`
- `addons/account_debit_note/i18n/ko.po`
- `addons/account_debit_note/i18n/ku.po`
- `addons/account_debit_note/i18n/lo.po`
- `addons/account_debit_note/i18n/lt.po`
- `addons/account_debit_note/i18n/lv.po`
- `addons/account_debit_note/i18n/mn.po`
- `addons/account_debit_note/i18n/my.po`
- `addons/account_debit_note/i18n/nb.po`
- `addons/account_debit_note/i18n/nl.po`
- `addons/account_debit_note/i18n/pl.po`
- `addons/account_debit_note/i18n/pt.po`
- `addons/account_debit_note/i18n/pt_BR.po`
- `addons/account_debit_note/i18n/ro.po`
- `addons/account_debit_note/i18n/ru.po`
- `addons/account_debit_note/i18n/sk.po`
- `addons/account_debit_note/i18n/sl.po`
- `addons/account_debit_note/i18n/sr@latin.po`
- `addons/account_debit_note/i18n/sv.po`
- `addons/account_debit_note/i18n/th.po`
- `addons/account_debit_note/i18n/tr.po`
- `addons/account_debit_note/i18n/uk.po`
- `addons/account_debit_note/i18n/uz.po`
- `addons/account_debit_note/i18n/vi.po`
- `addons/account_debit_note/i18n/zh_CN.po`
- `addons/account_debit_note/i18n/zh_TW.po`
- `addons/account_debit_note/models/__init__.py`
- `addons/account_debit_note/models/account_journal.py`
- `addons/account_debit_note/models/account_move.py`
- `addons/account_debit_note/security/ir.access.csv`
- `addons/account_debit_note/tests/__init__.py`
- `addons/account_debit_note/tests/test_out_debit_note.py`
- `addons/account_debit_note/views/account_journal_views.xml`
- `addons/account_debit_note/views/account_move_view.xml`
- `addons/account_debit_note/views/report_invoice.xml`
- `addons/account_debit_note/wizard/__init__.py`
- `addons/account_debit_note/wizard/account_debit_note.py`
- `addons/account_debit_note/wizard/account_debit_note_view.xml`
