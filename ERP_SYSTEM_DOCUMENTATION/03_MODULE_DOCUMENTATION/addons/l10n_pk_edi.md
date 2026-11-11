# Module: l10n_pk_edi

- **Module ID:** MOD-296
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_pk_edi`
- **Manifest:** `addons/l10n_pk_edi/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Electronic Invoicing for Pakistan FBR(v1.12)

**Manifest description:**

Pakistan - E-invoicing
======================

To submit invoices through API to the Pakistan government:

- Step 1: Generate an API token from the Pakistan E-Invoice portal.
- Step 2: Switch to the company associated with that API token in Odoo.
- Step 3: Configure the token in Odoo, by going to Invoicing/Accounting → Configuration →
  Settings, then searching for “Pakistan Electronic Invoicing” and pasting the token.
- Step 4: Create a customer invoice and use Send & Print to submit it to the Pakistan
  E-Invoicing system.

**Scope evidence:** The module contains 36 files, including 21 Python, 11 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account_debit_note`, `iap`, `l10n_pk`, `stock_delivery`.

## 2. Module structure

- Model/business logic files: 14
- Controller/API files: 0
- XML/data/view/template files: 11
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 1
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_pk_edi/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 14 model declarations, 71 methods, 2 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/l10n_pk_edi/models/res_partner.py:5`, `addons/l10n_pk_edi/models/product_product.py:4`, `addons/l10n_pk_edi/models/iap_account.py:24`, `addons/l10n_pk_edi/models/uom_uom.py:4`, `addons/l10n_pk_edi/models/product_template.py:6`, `addons/l10n_pk_edi/models/res_config_settings.py:5`, `addons/l10n_pk_edi/models/account_tax.py:4`, `addons/l10n_pk_edi/models/l10n_pk_edi_sro_item.py:5`, `addons/l10n_pk_edi/models/account_move.py:25`, `addons/l10n_pk_edi/models/account_move_line.py:6`, `addons/l10n_pk_edi/models/account_move_send.py:4`, `addons/l10n_pk_edi/models/l10n_pk_edi_sro.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 11 XML files and 0 JavaScript/TypeScript files; static XML analysis found 141 record/template/menu identifiers.
- **Evidence:** `addons/l10n_pk_edi/demo/demo_company.xml:3`, `addons/l10n_pk_edi/data/l10n_pk_edi_sro_data.xml:5`, `addons/l10n_pk_edi/data/l10n_pk_edi_sro_data.xml:9`, `addons/l10n_pk_edi/data/l10n_pk_edi_sro_data.xml:13`, `addons/l10n_pk_edi/data/l10n_pk_edi_sro_data.xml:17`, `addons/l10n_pk_edi/data/l10n_pk_edi_sro_data.xml:21`, `addons/l10n_pk_edi/data/l10n_pk_edi_sro_data.xml:25`, `addons/l10n_pk_edi/data/l10n_pk_edi_sro_data.xml:29`, `addons/l10n_pk_edi/data/l10n_pk_edi_sro_data.xml:33`, `addons/l10n_pk_edi/data/l10n_pk_edi_sro_data.xml:37`, `addons/l10n_pk_edi/data/l10n_pk_edi_sro_data.xml:41`, `addons/l10n_pk_edi/data/l10n_pk_edi_sro_data.xml:45`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_pk_edi/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_pk_edi/views/res_partner_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_pk_edi/models/account_move.py`, `addons/l10n_pk_edi/tests/test_l10n_pk_edi_payload.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_pk_edi/tests/__init__.py`, `addons/l10n_pk_edi/tests/test_l10n_pk_edi_payload.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 11; representative identifiers: `base.demo_company_pk`, `l10n_pk_edi_sro_297_i_2023_table_1`, `l10n_pk_edi_sro_297_i_2023_table_2`, `l10n_pk_edi_sro_327_i_2008`, `l10n_pk_edi_sro_3rd_schedule_goods`, `l10n_pk_edi_sro_587_1_2017`, `l10n_pk_edi_sro_6th_schd_table_1`, `l10n_pk_edi_sro_6th_schd_table_2`, `l10n_pk_edi_sro_6th_schd_table_3`, `l10n_pk_edi_sro_eighth_schedule_table_1`, `l10n_pk_edi_sro_fifth_schedule`, `l10n_pk_edi_sro_icto_table_1`, `l10n_pk_edi_sro_icto_table_2`, `l10n_pk_edi_sro_section_4b`, `l10n_pk_edi_sro_section_49`, `l10n_pk_edi_sro_item_297_i_2023_table_1_1`, `l10n_pk_edi_sro_item_297_i_2023_table_2_1`, `l10n_pk_edi_sro_item_327_i_2008_1`, `l10n_pk_edi_sro_item_587_1_2017_1`, `l10n_pk_edi_sro_item_eighth_schedule_77`
- Menus: 2; representative evidence: `addons/l10n_pk_edi/views/l10n_pk_edi_menus.xml:3`, `addons/l10n_pk_edi/views/l10n_pk_edi_menus.xml:9`
- Templates: 2; representative evidence: `addons/l10n_pk_edi/views/report_invoice.xml:3`, `addons/l10n_pk_edi/views/report_invoice.xml:27`
- View/action field declarations: 17; representative evidence: `addons/l10n_pk_edi/views/uom_uom_views.xml:5`, `addons/l10n_pk_edi/views/uom_uom_views.xml:7`, `addons/l10n_pk_edi/views/uom_uom_views.xml:15`, `addons/l10n_pk_edi/views/uom_uom_views.xml:17`, `addons/l10n_pk_edi/views/res_config_settings_views.xml:5`, `addons/l10n_pk_edi/views/res_config_settings_views.xml:7`, `addons/l10n_pk_edi/views/l10n_pk_edi_sro.xml:5`, `addons/l10n_pk_edi/views/l10n_pk_edi_sro.xml:6`, `addons/l10n_pk_edi/views/l10n_pk_edi_sro.xml:17`, `addons/l10n_pk_edi/views/l10n_pk_edi_sro.xml:18`, `addons/l10n_pk_edi/views/l10n_pk_edi_sro.xml:45`, `addons/l10n_pk_edi/views/account_move_views.xml:5`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_pk_edi/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_pk_edi/views/res_partner_views.xml`
- **Report entry points:** `addons/l10n_pk_edi/models/account_move.py`, `addons/l10n_pk_edi/tests/test_l10n_pk_edi_payload.py`

## 7. Database interactions

- Model declarations: 14
- Representative model evidence: inherits `res.partner` (addons/l10n_pk_edi/models/res_partner.py:5); inherits `product.product` (addons/l10n_pk_edi/models/product_product.py:4); inherits `iap.account` (addons/l10n_pk_edi/models/iap_account.py:24); inherits `uom.uom` (addons/l10n_pk_edi/models/uom_uom.py:4); inherits `product.template` (addons/l10n_pk_edi/models/product_template.py:6); inherits `res.config.settings` (addons/l10n_pk_edi/models/res_config_settings.py:5); inherits `account.tax` (addons/l10n_pk_edi/models/account_tax.py:4); `l10n_pk_edi.sro.item` (addons/l10n_pk_edi/models/l10n_pk_edi_sro_item.py:5); inherits `account.move` (addons/l10n_pk_edi/models/account_move.py:25); inherits `account.move.line` (addons/l10n_pk_edi/models/account_move_line.py:6); inherits `account.move.send` (addons/l10n_pk_edi/models/account_move_send.py:4); `l10n_pk_edi.sro` (addons/l10n_pk_edi/models/l10n_pk_edi_sro.py:7); inherits `res.company` (addons/l10n_pk_edi/models/res_company.py:18); inherits `account.debit.note` (addons/l10n_pk_edi/wizard/account_debit_note.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account_debit_note`, `iap`, `l10n_pk`, `stock_delivery`
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

- `addons/l10n_pk_edi/__init__.py`
- `addons/l10n_pk_edi/__manifest__.py`
- `addons/l10n_pk_edi/data/ir_config_data.xml`
- `addons/l10n_pk_edi/data/l10n_pk_edi_data.py`
- `addons/l10n_pk_edi/data/l10n_pk_edi_sro_data.xml`
- `addons/l10n_pk_edi/data/neutralize.sql`
- `addons/l10n_pk_edi/data/uom.uom.csv`
- `addons/l10n_pk_edi/demo/demo_company.xml`
- `addons/l10n_pk_edi/models/__init__.py`
- `addons/l10n_pk_edi/models/account_move.py`
- `addons/l10n_pk_edi/models/account_move_line.py`
- `addons/l10n_pk_edi/models/account_move_send.py`
- `addons/l10n_pk_edi/models/account_tax.py`
- `addons/l10n_pk_edi/models/iap_account.py`
- `addons/l10n_pk_edi/models/l10n_pk_edi_sro.py`
- `addons/l10n_pk_edi/models/l10n_pk_edi_sro_item.py`
- `addons/l10n_pk_edi/models/product_product.py`
- `addons/l10n_pk_edi/models/product_template.py`
- `addons/l10n_pk_edi/models/res_company.py`
- `addons/l10n_pk_edi/models/res_config_settings.py`
- `addons/l10n_pk_edi/models/res_partner.py`
- `addons/l10n_pk_edi/models/uom_uom.py`
- `addons/l10n_pk_edi/security/ir.access.csv`
- `addons/l10n_pk_edi/static/src/img/img_fbr_einvoice.png`
- `addons/l10n_pk_edi/tests/__init__.py`
- `addons/l10n_pk_edi/tests/test_l10n_pk_edi_payload.py`
- `addons/l10n_pk_edi/views/account_move_views.xml`
- `addons/l10n_pk_edi/views/l10n_pk_edi_menus.xml`
- `addons/l10n_pk_edi/views/l10n_pk_edi_sro.xml`
- `addons/l10n_pk_edi/views/product_views.xml`
- `addons/l10n_pk_edi/views/report_invoice.xml`
- `addons/l10n_pk_edi/views/res_config_settings_views.xml`
- `addons/l10n_pk_edi/views/res_partner_views.xml`
- `addons/l10n_pk_edi/views/uom_uom_views.xml`
- `addons/l10n_pk_edi/wizard/__init__.py`
- `addons/l10n_pk_edi/wizard/account_debit_note.py`
