# Module: l10n_gr_edi

- **Module ID:** MOD-208
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_gr_edi`
- **Manifest:** `addons/l10n_gr_edi/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Connect to myDATA API implementation for Greece

**Manifest description:**

myDATA is a platform created by Greece's tax authority,
        The Independent Authority for Public Revenue (IAPR),
        to digitize business tax and accounting information declaration.

**Scope evidence:** The module contains 41 files, including 21 Python, 16 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account_edi_ubl_cii`, `l10n_gr`.

## 2. Module structure

- Model/business logic files: 13
- Controller/API files: 0
- XML/data/view/template files: 16
- Browser asset files: 0
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 4
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_gr_edi/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 13 model declarations, 99 methods, 1 constraint handlers, 2 onchange handlers, and 20 dependency declarations.
- **Evidence:** `addons/l10n_gr_edi/models/res_partner.py:9`, `addons/l10n_gr_edi/models/product_template.py:4`, `addons/l10n_gr_edi/models/res_config_settings.py:4`, `addons/l10n_gr_edi/models/account_tax.py:8`, `addons/l10n_gr_edi/models/account_fiscal_position.py:4`, `addons/l10n_gr_edi/models/preferred_classification.py:864`, `addons/l10n_gr_edi/models/l10n_gr_edi_document.py:71`, `addons/l10n_gr_edi/models/account_edi_xml_ubl_gr.py:6`, `addons/l10n_gr_edi/models/account_move.py:27`, `addons/l10n_gr_edi/models/account_move_line.py:13`, `addons/l10n_gr_edi/models/account_move_send.py:4`, `addons/l10n_gr_edi/models/res_company.py:16`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 16 XML files and 0 JavaScript/TypeScript files; static XML analysis found 17 record/template/menu identifiers.
- **Evidence:** `addons/l10n_gr_edi/data/ir_cron.xml:4`, `addons/l10n_gr_edi/data/template.xml:4`, `addons/l10n_gr_edi/data/template.xml:126`, `addons/l10n_gr_edi/views/res_config_settings_views.xml:4`, `addons/l10n_gr_edi/views/report_invoice.xml:4`, `addons/l10n_gr_edi/views/report_invoice.xml:24`, `addons/l10n_gr_edi/views/res_company_views.xml:5`, `addons/l10n_gr_edi/views/account_move_views.xml:4`, `addons/l10n_gr_edi/views/account_move_views.xml:123`, `addons/l10n_gr_edi/views/account_move_views.xml:134`, `addons/l10n_gr_edi/views/account_move_views.xml:145`, `addons/l10n_gr_edi/views/account_move_views.xml:156`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_gr_edi/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 4 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_gr_edi/__manifest__.py`, `addons/l10n_gr_edi/models/res_company.py`, `addons/l10n_gr_edi/data/ir_cron.xml`, `addons/l10n_gr_edi/views/account_move_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_gr_edi/tests/test_xml_ubl_gr.py`, `addons/l10n_gr_edi/tests/test_mydata_invoice.py`, `addons/l10n_gr_edi/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 16; representative identifiers: `ir_cron_mydata_fetch_third_party_invoices`, `mydata_invoice`, `mydata_expense_classification`, `res_config_settings_form_inherit_l10n_gr_edi`, `report_invoice_document`, `report_invoice`, `view_company_form`, `account_move_form_inherit_l10n_gr_edi`, `view_out_invoice_tree_inherit_l10n_gr_edi`, `view_out_credit_note_tree_inherit_l10n_gr_edi`, `view_in_invoice_bill_tree_inherit_l10n_gr_edi`, `view_account_invoice_filter_inherit_l10n_gr_edi`, `l10n_gr_edi_action_try_send_batch`, `view_account_position_form`, `view_account_tax_form_inherit`, `product_template_form_view_inherit_l10n_gr_edi`, `view_partner_property_form_inherit_l10n_gr_edi`
- Menus: 0; representative evidence: Not found in module
- Templates: 4; representative evidence: `addons/l10n_gr_edi/data/template.xml:4`, `addons/l10n_gr_edi/data/template.xml:126`, `addons/l10n_gr_edi/views/report_invoice.xml:4`, `addons/l10n_gr_edi/views/report_invoice.xml:24`
- View/action field declarations: 22; representative evidence: `addons/l10n_gr_edi/views/res_config_settings_views.xml:6`, `addons/l10n_gr_edi/views/res_config_settings_views.xml:8`, `addons/l10n_gr_edi/views/res_company_views.xml:7`, `addons/l10n_gr_edi/views/res_company_views.xml:9`, `addons/l10n_gr_edi/views/account_move_views.xml:6`, `addons/l10n_gr_edi/views/account_move_views.xml:8`, `addons/l10n_gr_edi/views/account_move_views.xml:125`, `addons/l10n_gr_edi/views/account_move_views.xml:127`, `addons/l10n_gr_edi/views/account_move_views.xml:136`, `addons/l10n_gr_edi/views/account_move_views.xml:138`, `addons/l10n_gr_edi/views/account_move_views.xml:147`, `addons/l10n_gr_edi/views/account_move_views.xml:149`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_gr_edi/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_gr_edi/__manifest__.py`, `addons/l10n_gr_edi/models/res_company.py`, `addons/l10n_gr_edi/data/ir_cron.xml`, `addons/l10n_gr_edi/views/account_move_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 13
- Representative model evidence: inherits `res.partner` (addons/l10n_gr_edi/models/res_partner.py:9); inherits `product.template` (addons/l10n_gr_edi/models/product_template.py:4); inherits `res.config.settings` (addons/l10n_gr_edi/models/res_config_settings.py:4); inherits `account.tax` (addons/l10n_gr_edi/models/account_tax.py:8); inherits `account.fiscal.position` (addons/l10n_gr_edi/models/account_fiscal_position.py:4); `l10n_gr_edi.preferred_classification` (addons/l10n_gr_edi/models/preferred_classification.py:864); `l10n_gr_edi.document` (addons/l10n_gr_edi/models/l10n_gr_edi_document.py:71); `account.edi.xml.ubl_gr` (addons/l10n_gr_edi/models/account_edi_xml_ubl_gr.py:6); inherits `account.move` (addons/l10n_gr_edi/models/account_move.py:27); inherits `account.move.line` (addons/l10n_gr_edi/models/account_move_line.py:13); inherits `account.move.send` (addons/l10n_gr_edi/models/account_move_send.py:4); inherits `res.company` (addons/l10n_gr_edi/models/res_company.py:16); inherits `account.move.reversal` (addons/l10n_gr_edi/wizard/account_move_reversal.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account_edi_ubl_cii`, `l10n_gr`
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

- `addons/l10n_gr_edi/__init__.py`
- `addons/l10n_gr_edi/__manifest__.py`
- `addons/l10n_gr_edi/data/ir_cron.xml`
- `addons/l10n_gr_edi/data/neutralize.sql`
- `addons/l10n_gr_edi/data/template.xml`
- `addons/l10n_gr_edi/i18n/el.po`
- `addons/l10n_gr_edi/i18n/l10n_gr_edi.pot`
- `addons/l10n_gr_edi/models/__init__.py`
- `addons/l10n_gr_edi/models/account_edi_xml_ubl_gr.py`
- `addons/l10n_gr_edi/models/account_fiscal_position.py`
- `addons/l10n_gr_edi/models/account_move.py`
- `addons/l10n_gr_edi/models/account_move_line.py`
- `addons/l10n_gr_edi/models/account_move_send.py`
- `addons/l10n_gr_edi/models/account_tax.py`
- `addons/l10n_gr_edi/models/l10n_gr_edi_document.py`
- `addons/l10n_gr_edi/models/preferred_classification.py`
- `addons/l10n_gr_edi/models/product_template.py`
- `addons/l10n_gr_edi/models/res_company.py`
- `addons/l10n_gr_edi/models/res_config_settings.py`
- `addons/l10n_gr_edi/models/res_partner.py`
- `addons/l10n_gr_edi/security/ir.access.csv`
- `addons/l10n_gr_edi/tests/__init__.py`
- `addons/l10n_gr_edi/tests/test_files/from_odoo/grcius_out_invoice.xml`
- `addons/l10n_gr_edi/tests/test_files/from_odoo/grcius_out_refund.xml`
- `addons/l10n_gr_edi/tests/test_files/from_odoo/mydata_cls_expense.xml`
- `addons/l10n_gr_edi/tests/test_files/from_odoo/mydata_invoice.xml`
- `addons/l10n_gr_edi/tests/test_files/from_odoo/mydata_invoice_11_2.xml`
- `addons/l10n_gr_edi/tests/test_files/from_odoo/mydata_multi_invoices.xml`
- `addons/l10n_gr_edi/tests/test_mydata_invoice.py`
- `addons/l10n_gr_edi/tests/test_xml_ubl_gr.py`
- `addons/l10n_gr_edi/utils.py`
- `addons/l10n_gr_edi/views/account_fiscal_position_views.xml`
- `addons/l10n_gr_edi/views/account_move_views.xml`
- `addons/l10n_gr_edi/views/account_tax_views.xml`
- `addons/l10n_gr_edi/views/product_template_views.xml`
- `addons/l10n_gr_edi/views/report_invoice.xml`
- `addons/l10n_gr_edi/views/res_company_views.xml`
- `addons/l10n_gr_edi/views/res_config_settings_views.xml`
- `addons/l10n_gr_edi/views/res_partner_views.xml`
- `addons/l10n_gr_edi/wizard/__init__.py`
- `addons/l10n_gr_edi/wizard/account_move_reversal.py`
