# Module: l10n_sa_edi_pos

- **Module ID:** MOD-312
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_sa_edi_pos`
- **Manifest:** `addons/l10n_sa_edi_pos/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** ZATCA E-Invoicing, support for PoS

**Manifest description:**

E-invoice implementation for Saudi Arabia; Integration with ZATCA (POS)

**Scope evidence:** The module contains 24 files, including 13 Python, 2 XML, and 7 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_sa_pos`, `l10n_sa_edi`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 7
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 24 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_sa_edi_pos/models/account_edi_xml_ubl_21_zatca.py:4`, `addons/l10n_sa_edi_pos/models/pos_order.py:4`, `addons/l10n_sa_edi_pos/models/l10n_sa_edi_document.py:4`, `addons/l10n_sa_edi_pos/models/account_move.py:4`, `addons/l10n_sa_edi_pos/models/res_company.py:4`, `addons/l10n_sa_edi_pos/receipt/pos_order_receipt.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 7 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/l10n_sa_edi_pos/receipt/pos_order_receipt.xml:4`, `addons/l10n_sa_edi_pos/receipt/pos_receipt_common.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_sa_edi_pos/tests/test_sa_edi_pos.py`, `addons/l10n_sa_edi_pos/tests/__init__.py`, `addons/l10n_sa_edi_pos/tests/test_order_receipt.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `l10n_sa_edi_pos.pos_order_receipt_header`, `l10n_sa_edi_pos.company_info_receipt`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/l10n_sa_edi_pos/receipt/pos_order_receipt.xml:4`, `addons/l10n_sa_edi_pos/receipt/pos_receipt_common.xml:4`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 7; representative files: `addons/l10n_sa_edi_pos/static/src/overrides/models/pos_store.js`, `addons/l10n_sa_edi_pos/static/src/overrides/models/pos_order.js`, `addons/l10n_sa_edi_pos/static/src/overrides/components/invoice_button/invoice_button.js`, `addons/l10n_sa_edi_pos/static/src/overrides/utils/printer/generate_printer_data.js`, `addons/l10n_sa_edi_pos/static/src/app/utils/order_payment_validation.js`, `addons/l10n_sa_edi_pos/static/tests/tours/test_zatca_pos_invoice.js`, `addons/l10n_sa_edi_pos/static/tests/tours/generic_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_sa_edi_pos/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `account.edi.xml.ubl_21.zatca` (addons/l10n_sa_edi_pos/models/account_edi_xml_ubl_21_zatca.py:4); inherits `pos.order` (addons/l10n_sa_edi_pos/models/pos_order.py:4); inherits `l10n_sa_edi.document` (addons/l10n_sa_edi_pos/models/l10n_sa_edi_document.py:4); inherits `account.move` (addons/l10n_sa_edi_pos/models/account_move.py:4); inherits `res.company` (addons/l10n_sa_edi_pos/models/res_company.py:4); inherits `pos.order.receipt` (addons/l10n_sa_edi_pos/receipt/pos_order_receipt.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_sa_pos`, `l10n_sa_edi`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_sa_edi_pos/__init__.py`
- `addons/l10n_sa_edi_pos/__manifest__.py`
- `addons/l10n_sa_edi_pos/i18n/ar.po`
- `addons/l10n_sa_edi_pos/i18n/l10n_sa_edi_pos.pot`
- `addons/l10n_sa_edi_pos/models/__init__.py`
- `addons/l10n_sa_edi_pos/models/account_edi_xml_ubl_21_zatca.py`
- `addons/l10n_sa_edi_pos/models/account_move.py`
- `addons/l10n_sa_edi_pos/models/l10n_sa_edi_document.py`
- `addons/l10n_sa_edi_pos/models/pos_order.py`
- `addons/l10n_sa_edi_pos/models/res_company.py`
- `addons/l10n_sa_edi_pos/receipt/__init__.py`
- `addons/l10n_sa_edi_pos/receipt/pos_order_receipt.py`
- `addons/l10n_sa_edi_pos/receipt/pos_order_receipt.xml`
- `addons/l10n_sa_edi_pos/receipt/pos_receipt_common.xml`
- `addons/l10n_sa_edi_pos/static/src/app/utils/order_payment_validation.js`
- `addons/l10n_sa_edi_pos/static/src/overrides/components/invoice_button/invoice_button.js`
- `addons/l10n_sa_edi_pos/static/src/overrides/models/pos_order.js`
- `addons/l10n_sa_edi_pos/static/src/overrides/models/pos_store.js`
- `addons/l10n_sa_edi_pos/static/src/overrides/utils/printer/generate_printer_data.js`
- `addons/l10n_sa_edi_pos/static/tests/tours/generic_tour.js`
- `addons/l10n_sa_edi_pos/static/tests/tours/test_zatca_pos_invoice.js`
- `addons/l10n_sa_edi_pos/tests/__init__.py`
- `addons/l10n_sa_edi_pos/tests/test_order_receipt.py`
- `addons/l10n_sa_edi_pos/tests/test_sa_edi_pos.py`
