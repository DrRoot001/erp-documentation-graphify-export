# Module: l10n_id_efaktur_coretax

- **Module ID:** MOD-222
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_id_efaktur_coretax`
- **Manifest:** `addons/l10n_id_efaktur_coretax/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

E-invoicing feature provided by DJP (Indonesian Tax Office). As of January 1st 2025,
        Indonesia is using CoreTax system, which changes the file format and content of E-Faktur.
        We're changing from CSV files into XML.
        At the same time, due to tax regulation changes back and forth, for general E-Faktur now,
        TaxBase (DPP) has to be mulitplied by factor of 11/12 while multiplied to tax of 12% which
        is resulting to 11%.

**Scope evidence:** The module contains 33 files, including 17 Python, 10 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_id`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 2
- XML/data/view/template files: 10
- Browser asset files: 0
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 2
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_id_efaktur_coretax/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 63 methods, 0 constraint handlers, 0 onchange handlers, and 9 dependency declarations.
- **Evidence:** `addons/l10n_id_efaktur_coretax/models/uom_code.py:5`, `addons/l10n_id_efaktur_coretax/models/res_partner.py:7`, `addons/l10n_id_efaktur_coretax/models/uom_uom.py:5`, `addons/l10n_id_efaktur_coretax/models/product_template.py:5`, `addons/l10n_id_efaktur_coretax/models/efaktur_document.py:9`, `addons/l10n_id_efaktur_coretax/models/product_code.py:6`, `addons/l10n_id_efaktur_coretax/models/account_move.py:50`, `addons/l10n_id_efaktur_coretax/models/account_move_line.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/l10n_id_efaktur_coretax/controllers/download_efaktur.py:21`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 10 XML files and 0 JavaScript/TypeScript files; static XML analysis found 15 record/template/menu identifiers.
- **Evidence:** `addons/l10n_id_efaktur_coretax/data/efaktur_templates.xml:4`, `addons/l10n_id_efaktur_coretax/data/efaktur_templates.xml:22`, `addons/l10n_id_efaktur_coretax/data/efaktur_templates.xml:49`, `addons/l10n_id_efaktur_coretax/data/ir_action.xml:3`, `addons/l10n_id_efaktur_coretax/views/product_template.xml:4`, `addons/l10n_id_efaktur_coretax/views/uom_uom.xml:3`, `addons/l10n_id_efaktur_coretax/views/efaktur_document.xml:4`, `addons/l10n_id_efaktur_coretax/views/efaktur_document.xml:54`, `addons/l10n_id_efaktur_coretax/views/efaktur_document.xml:65`, `addons/l10n_id_efaktur_coretax/views/uom_code.xml:4`, `addons/l10n_id_efaktur_coretax/views/account_move.xml:3`, `addons/l10n_id_efaktur_coretax/views/account_move.xml:24`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_id_efaktur_coretax/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_id_efaktur_coretax/data/ir_action.xml`, `addons/l10n_id_efaktur_coretax/views/account_move.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/l10n_id_efaktur_coretax/tests/test_l10n_id_efaktur_download.py`, `addons/l10n_id_efaktur_coretax/tests/test_l10n_id_efaktur_coretax.py`, `addons/l10n_id_efaktur_coretax/tests/test_l10n_id_is_company.py`, `addons/l10n_id_efaktur_coretax/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 10; representative identifiers: `efaktur_coretax_invoice_line`, `efaktur_coretax_invoice`, `efaktur_coretax_template`, `download_efaktur`, `product_template_inherit`, `uom_uom_view_form`, `l10n_id_efaktur_document_form_view`, `l10n_id_efaktur_document_list_view`, `l10n_id_efaktur_document_filter_view`, `uom_code_list`, `account_move_efaktur_form_view`, `dowload_efaktur_action`, `view_account_invoice_filter`, `res_partner_tax_form_view`, `produc_code_list`
- Menus: 0; representative evidence: Not found in module
- Templates: 3; representative evidence: `addons/l10n_id_efaktur_coretax/data/efaktur_templates.xml:4`, `addons/l10n_id_efaktur_coretax/data/efaktur_templates.xml:22`, `addons/l10n_id_efaktur_coretax/data/efaktur_templates.xml:49`
- View/action field declarations: 20; representative evidence: `addons/l10n_id_efaktur_coretax/views/product_template.xml:6`, `addons/l10n_id_efaktur_coretax/views/product_template.xml:8`, `addons/l10n_id_efaktur_coretax/views/uom_uom.xml:5`, `addons/l10n_id_efaktur_coretax/views/uom_uom.xml:7`, `addons/l10n_id_efaktur_coretax/views/efaktur_document.xml:6`, `addons/l10n_id_efaktur_coretax/views/efaktur_document.xml:7`, `addons/l10n_id_efaktur_coretax/views/efaktur_document.xml:56`, `addons/l10n_id_efaktur_coretax/views/efaktur_document.xml:57`, `addons/l10n_id_efaktur_coretax/views/efaktur_document.xml:67`, `addons/l10n_id_efaktur_coretax/views/efaktur_document.xml:68`, `addons/l10n_id_efaktur_coretax/views/uom_code.xml:6`, `addons/l10n_id_efaktur_coretax/views/uom_code.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_id_efaktur_coretax/__manifest__.py`
- **HTTP entry points:** `addons/l10n_id_efaktur_coretax/controllers/download_efaktur.py:21`
- **Scheduled entry points:** `addons/l10n_id_efaktur_coretax/data/ir_action.xml`, `addons/l10n_id_efaktur_coretax/views/account_move.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: `l10n_id_efaktur_coretax.uom.code` (addons/l10n_id_efaktur_coretax/models/uom_code.py:5); inherits `res.partner` (addons/l10n_id_efaktur_coretax/models/res_partner.py:7); inherits `uom.uom` (addons/l10n_id_efaktur_coretax/models/uom_uom.py:5); inherits `product.template` (addons/l10n_id_efaktur_coretax/models/product_template.py:5); `l10n_id_efaktur_coretax.document` (addons/l10n_id_efaktur_coretax/models/efaktur_document.py:9); `l10n_id_efaktur_coretax.product.code` (addons/l10n_id_efaktur_coretax/models/product_code.py:6); inherits `account.move` (addons/l10n_id_efaktur_coretax/models/account_move.py:50); inherits `account.move.line` (addons/l10n_id_efaktur_coretax/models/account_move_line.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/l10n_id_efaktur_coretax/controllers/download_efaktur.py:21`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_id`
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

- `addons/l10n_id_efaktur_coretax/__init__.py`
- `addons/l10n_id_efaktur_coretax/__manifest__.py`
- `addons/l10n_id_efaktur_coretax/controllers/__init__.py`
- `addons/l10n_id_efaktur_coretax/controllers/download_efaktur.py`
- `addons/l10n_id_efaktur_coretax/data/efaktur_templates.xml`
- `addons/l10n_id_efaktur_coretax/data/ir_action.xml`
- `addons/l10n_id_efaktur_coretax/data/l10n_id_efaktur_coretax.product.code.csv`
- `addons/l10n_id_efaktur_coretax/data/l10n_id_efaktur_coretax.uom.code.csv`
- `addons/l10n_id_efaktur_coretax/data/uom.uom.csv`
- `addons/l10n_id_efaktur_coretax/i18n/id.po`
- `addons/l10n_id_efaktur_coretax/i18n/l10n_id_efaktur_coretax.pot`
- `addons/l10n_id_efaktur_coretax/models/__init__.py`
- `addons/l10n_id_efaktur_coretax/models/account_move.py`
- `addons/l10n_id_efaktur_coretax/models/account_move_line.py`
- `addons/l10n_id_efaktur_coretax/models/efaktur_document.py`
- `addons/l10n_id_efaktur_coretax/models/product_code.py`
- `addons/l10n_id_efaktur_coretax/models/product_template.py`
- `addons/l10n_id_efaktur_coretax/models/res_partner.py`
- `addons/l10n_id_efaktur_coretax/models/uom_code.py`
- `addons/l10n_id_efaktur_coretax/models/uom_uom.py`
- `addons/l10n_id_efaktur_coretax/security/ir.access.csv`
- `addons/l10n_id_efaktur_coretax/tests/__init__.py`
- `addons/l10n_id_efaktur_coretax/tests/results/sample.xml`
- `addons/l10n_id_efaktur_coretax/tests/test_l10n_id_efaktur_coretax.py`
- `addons/l10n_id_efaktur_coretax/tests/test_l10n_id_efaktur_download.py`
- `addons/l10n_id_efaktur_coretax/tests/test_l10n_id_is_company.py`
- `addons/l10n_id_efaktur_coretax/views/account_move.xml`
- `addons/l10n_id_efaktur_coretax/views/efaktur_document.xml`
- `addons/l10n_id_efaktur_coretax/views/product_code.xml`
- `addons/l10n_id_efaktur_coretax/views/product_template.xml`
- `addons/l10n_id_efaktur_coretax/views/res_partner.xml`
- `addons/l10n_id_efaktur_coretax/views/uom_code.xml`
- `addons/l10n_id_efaktur_coretax/views/uom_uom.xml`
