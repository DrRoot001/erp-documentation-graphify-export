# Module: l10n_in_ewaybill

- **Module ID:** MOD-230
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_in_ewaybill`
- **Manifest:** `addons/l10n_in_ewaybill/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Indian - E-waybill
====================================
To submit E-waybill through API to the government.
We use "Tera Software Limited" as GSP

Step 1: First you need to create an API username and password in the E-waybill portal.
Step 2: Switch to company related to that GST number
Step 3: Set that username and password in Odoo (Goto: Invoicing/Accounting -> Configration -> Settings -> Indian Electronic WayBill or find "E-waybill" in search bar)
Step 4: Repeat steps 1,2,3 for all GSTIN you have in odoo. If you have a multi-company with the same GST number then perform step 1 for the first company only.

**Scope evidence:** The module contains 30 files, including 18 Python, 8 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_in`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 0
- XML/data/view/template files: 8
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_in_ewaybill/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 87 methods, 0 constraint handlers, 0 onchange handlers, and 9 dependency declarations.
- **Evidence:** `addons/l10n_in_ewaybill/demo/account_demo.py:8`, `addons/l10n_in_ewaybill/models/res_config_settings.py:9`, `addons/l10n_in_ewaybill/models/ewaybill_type.py:6`, `addons/l10n_in_ewaybill/models/account_move.py:7`, `addons/l10n_in_ewaybill/models/ir_attachment.py:5`, `addons/l10n_in_ewaybill/models/l10n_in_ewaybill.py:18`, `addons/l10n_in_ewaybill/models/res_company.py:6`, `addons/l10n_in_ewaybill/wizard/l10n_in_ewaybill_cancel.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 8 XML files and 0 JavaScript/TypeScript files; static XML analysis found 18 record/template/menu identifiers.
- **Evidence:** `addons/l10n_in_ewaybill/report/ewaybill_report_views.xml:4`, `addons/l10n_in_ewaybill/report/ewaybill_report_views.xml:20`, `addons/l10n_in_ewaybill/report/ewaybill_report.xml:4`, `addons/l10n_in_ewaybill/wizard/l10n_in_ewaybill_cancel_views.xml:4`, `addons/l10n_in_ewaybill/data/ewaybill_type_data.xml:4`, `addons/l10n_in_ewaybill/data/ewaybill_type_data.xml:13`, `addons/l10n_in_ewaybill/data/ewaybill_type_data.xml:22`, `addons/l10n_in_ewaybill/data/ewaybill_type_data.xml:31`, `addons/l10n_in_ewaybill/data/ewaybill_type_data.xml:40`, `addons/l10n_in_ewaybill/data/ewaybill_type_data.xml:49`, `addons/l10n_in_ewaybill/data/ewaybill_type_data.xml:58`, `addons/l10n_in_ewaybill/data/ewaybill_type_data.xml:67`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_in_ewaybill/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_in_ewaybill/models/l10n_in_ewaybill.py`, `addons/l10n_in_ewaybill/report/ewaybill_report_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_in_ewaybill/tests/test_ewaybill_json.py`, `addons/l10n_in_ewaybill/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 8; representative identifiers: `paperformat_ewaybill`, `action_report_ewaybill`, `report_ewaybill`, `view_ewaybill_cancel_form`, `type_tax_invoice_sub_type_supply`, `type_tax_invoice_sub_type_export`, `type_tax_invoice_sub_type_skd_ckd_lots`, `type_bill_of_supply_sub_type_supply`, `type_bill_of_supply_sub_type_export`, `type_bill_of_supply_sub_type_skd_ckd_lots`, `type_bill_of_entry_sub_type_import`, `type_bill_of_entry_sub_skd_ckd_lots`, `res_config_settings_view_form_inherit_l10n_in_edi_ewaybill`, `l10n_in_ewaybill_report_invoice_document_inherit`, `invoice_form_inherit_l10n_in_ewaybill`, `view_invoice_list_inherit_l10n_in_ewaybill`, `l10n_in_ewaybill_form_view`, `l10n_in_ewaybill_form_action`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/l10n_in_ewaybill/report/ewaybill_report.xml:4`, `addons/l10n_in_ewaybill/views/edi_pdf_report.xml:3`
- View/action field declarations: 13; representative evidence: `addons/l10n_in_ewaybill/report/ewaybill_report_views.xml:22`, `addons/l10n_in_ewaybill/wizard/l10n_in_ewaybill_cancel_views.xml:6`, `addons/l10n_in_ewaybill/wizard/l10n_in_ewaybill_cancel_views.xml:7`, `addons/l10n_in_ewaybill/views/res_config_settings_views.xml:5`, `addons/l10n_in_ewaybill/views/res_config_settings_views.xml:7`, `addons/l10n_in_ewaybill/views/account_move_views.xml:5`, `addons/l10n_in_ewaybill/views/account_move_views.xml:7`, `addons/l10n_in_ewaybill/views/account_move_views.xml:39`, `addons/l10n_in_ewaybill/views/account_move_views.xml:41`, `addons/l10n_in_ewaybill/views/l10n_in_ewaybill_views.xml:5`, `addons/l10n_in_ewaybill/views/l10n_in_ewaybill_views.xml:6`, `addons/l10n_in_ewaybill/views/l10n_in_ewaybill_views.xml:178`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_in_ewaybill/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/l10n_in_ewaybill/models/l10n_in_ewaybill.py`, `addons/l10n_in_ewaybill/report/ewaybill_report_views.xml`

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: inherits `account.chart.template` (addons/l10n_in_ewaybill/demo/account_demo.py:8); inherits `res.config.settings` (addons/l10n_in_ewaybill/models/res_config_settings.py:9); `l10n.in.ewaybill.type` (addons/l10n_in_ewaybill/models/ewaybill_type.py:6); inherits `account.move` (addons/l10n_in_ewaybill/models/account_move.py:7); inherits `ir.attachment` (addons/l10n_in_ewaybill/models/ir_attachment.py:5); `l10n.in.ewaybill` (addons/l10n_in_ewaybill/models/l10n_in_ewaybill.py:18); inherits `res.company` (addons/l10n_in_ewaybill/models/res_company.py:6); `l10n.in.ewaybill.cancel` (addons/l10n_in_ewaybill/wizard/l10n_in_ewaybill_cancel.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_in`
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

- `addons/l10n_in_ewaybill/__init__.py`
- `addons/l10n_in_ewaybill/__manifest__.py`
- `addons/l10n_in_ewaybill/data/ewaybill_type_data.xml`
- `addons/l10n_in_ewaybill/data/neutralize.sql`
- `addons/l10n_in_ewaybill/demo/__init__.py`
- `addons/l10n_in_ewaybill/demo/account_demo.py`
- `addons/l10n_in_ewaybill/i18n/hi.po`
- `addons/l10n_in_ewaybill/i18n/l10n_in_ewaybill.pot`
- `addons/l10n_in_ewaybill/models/__init__.py`
- `addons/l10n_in_ewaybill/models/account_move.py`
- `addons/l10n_in_ewaybill/models/error_codes.py`
- `addons/l10n_in_ewaybill/models/ewaybill_type.py`
- `addons/l10n_in_ewaybill/models/ir_attachment.py`
- `addons/l10n_in_ewaybill/models/l10n_in_ewaybill.py`
- `addons/l10n_in_ewaybill/models/res_company.py`
- `addons/l10n_in_ewaybill/models/res_config_settings.py`
- `addons/l10n_in_ewaybill/report/ewaybill_report.xml`
- `addons/l10n_in_ewaybill/report/ewaybill_report_views.xml`
- `addons/l10n_in_ewaybill/security/ir.access.csv`
- `addons/l10n_in_ewaybill/tests/__init__.py`
- `addons/l10n_in_ewaybill/tests/test_ewaybill_json.py`
- `addons/l10n_in_ewaybill/tools/__init__.py`
- `addons/l10n_in_ewaybill/tools/ewaybill_api.py`
- `addons/l10n_in_ewaybill/views/account_move_views.xml`
- `addons/l10n_in_ewaybill/views/edi_pdf_report.xml`
- `addons/l10n_in_ewaybill/views/l10n_in_ewaybill_views.xml`
- `addons/l10n_in_ewaybill/views/res_config_settings_views.xml`
- `addons/l10n_in_ewaybill/wizard/__init__.py`
- `addons/l10n_in_ewaybill/wizard/l10n_in_ewaybill_cancel.py`
- `addons/l10n_in_ewaybill/wizard/l10n_in_ewaybill_cancel_views.xml`
