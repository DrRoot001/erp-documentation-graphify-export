# Module: l10n_it_edi_doi

- **Module ID:** MOD-242
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_it_edi_doi`
- **Manifest:** `addons/l10n_it_edi_doi/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Add support for the Declaration of Intent (Dichiarazione di Intento) to the Italian localization.

**Scope evidence:** The module contains 26 files, including 14 Python, 7 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_it_edi`, `sale`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 0
- XML/data/view/template files: 7
- Browser asset files: 0
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_it_edi_doi/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 58 methods, 2 constraint handlers, 0 onchange handlers, and 16 dependency declarations.
- **Evidence:** `addons/l10n_it_edi_doi/models/res_partner.py:6`, `addons/l10n_it_edi_doi/models/sale_order.py:7`, `addons/l10n_it_edi_doi/models/declaration_of_intent.py:8`, `addons/l10n_it_edi_doi/models/account_tax.py:5`, `addons/l10n_it_edi_doi/models/account_fiscal_position.py:7`, `addons/l10n_it_edi_doi/models/account_chart_template.py:6`, `addons/l10n_it_edi_doi/models/account_move.py:7`, `addons/l10n_it_edi_doi/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 0 JavaScript/TypeScript files; static XML analysis found 14 record/template/menu identifiers.
- **Evidence:** `addons/l10n_it_edi_doi/data/invoice_it_template.xml:5`, `addons/l10n_it_edi_doi/views/sale_ir_actions_report_templates.xml:3`, `addons/l10n_it_edi_doi/views/report_invoice.xml:3`, `addons/l10n_it_edi_doi/views/sale_order_views.xml:3`, `addons/l10n_it_edi_doi/views/sale_order_views.xml:21`, `addons/l10n_it_edi_doi/views/sale_order_views.xml:44`, `addons/l10n_it_edi_doi/views/l10n_it_edi_doi_declaration_of_intent_views.xml:4`, `addons/l10n_it_edi_doi/views/l10n_it_edi_doi_declaration_of_intent_views.xml:31`, `addons/l10n_it_edi_doi/views/l10n_it_edi_doi_declaration_of_intent_views.xml:107`, `addons/l10n_it_edi_doi/views/account_move_views.xml:4`, `addons/l10n_it_edi_doi/views/account_move_views.xml:25`, `addons/l10n_it_edi_doi/views/account_move_views.xml:42`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_it_edi_doi/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_it_edi_doi/tests/common.py`, `addons/l10n_it_edi_doi/tests/__init__.py`, `addons/l10n_it_edi_doi/tests/test_amounts_and_warnings.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `account_invoice_line_it_FatturaPA`, `report_saleorder_document`, `report_invoice_document`, `view_sales_order_filter`, `view_quotation_tree`, `view_order_form`, `view_l10n_it_edi_doi_tree`, `view_l10n_it_edi_doi_form`, `view_l10n_it_edi_doi_declaration_of_intent_search`, `view_account_invoice_filter`, `view_move_tree`, `view_move_form`, `res_partner_view_search`, `view_partner_l10n_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 3; representative evidence: `addons/l10n_it_edi_doi/data/invoice_it_template.xml:5`, `addons/l10n_it_edi_doi/views/sale_ir_actions_report_templates.xml:3`, `addons/l10n_it_edi_doi/views/report_invoice.xml:3`
- View/action field declarations: 22; representative evidence: `addons/l10n_it_edi_doi/views/sale_order_views.xml:5`, `addons/l10n_it_edi_doi/views/sale_order_views.xml:7`, `addons/l10n_it_edi_doi/views/sale_order_views.xml:23`, `addons/l10n_it_edi_doi/views/sale_order_views.xml:25`, `addons/l10n_it_edi_doi/views/sale_order_views.xml:46`, `addons/l10n_it_edi_doi/views/sale_order_views.xml:48`, `addons/l10n_it_edi_doi/views/l10n_it_edi_doi_declaration_of_intent_views.xml:6`, `addons/l10n_it_edi_doi/views/l10n_it_edi_doi_declaration_of_intent_views.xml:7`, `addons/l10n_it_edi_doi/views/l10n_it_edi_doi_declaration_of_intent_views.xml:33`, `addons/l10n_it_edi_doi/views/l10n_it_edi_doi_declaration_of_intent_views.xml:34`, `addons/l10n_it_edi_doi/views/l10n_it_edi_doi_declaration_of_intent_views.xml:109`, `addons/l10n_it_edi_doi/views/l10n_it_edi_doi_declaration_of_intent_views.xml:111`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_it_edi_doi/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: inherits `res.partner` (addons/l10n_it_edi_doi/models/res_partner.py:6); inherits `sale.order` (addons/l10n_it_edi_doi/models/sale_order.py:7); `l10n_it_edi_doi.declaration_of_intent` (addons/l10n_it_edi_doi/models/declaration_of_intent.py:8); inherits `account.tax` (addons/l10n_it_edi_doi/models/account_tax.py:5); inherits `account.fiscal.position` (addons/l10n_it_edi_doi/models/account_fiscal_position.py:7); inherits `account.chart.template` (addons/l10n_it_edi_doi/models/account_chart_template.py:6); inherits `account.move` (addons/l10n_it_edi_doi/models/account_move.py:7); inherits `res.company` (addons/l10n_it_edi_doi/models/res_company.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_it_edi`, `sale`
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

- `addons/l10n_it_edi_doi/__init__.py`
- `addons/l10n_it_edi_doi/__manifest__.py`
- `addons/l10n_it_edi_doi/data/invoice_it_template.xml`
- `addons/l10n_it_edi_doi/data/template/account.fiscal.position-it.csv`
- `addons/l10n_it_edi_doi/data/template/account.tax-it.csv`
- `addons/l10n_it_edi_doi/i18n/it.po`
- `addons/l10n_it_edi_doi/i18n/l10n_it_edi_doi.pot`
- `addons/l10n_it_edi_doi/models/__init__.py`
- `addons/l10n_it_edi_doi/models/account_chart_template.py`
- `addons/l10n_it_edi_doi/models/account_fiscal_position.py`
- `addons/l10n_it_edi_doi/models/account_move.py`
- `addons/l10n_it_edi_doi/models/account_tax.py`
- `addons/l10n_it_edi_doi/models/declaration_of_intent.py`
- `addons/l10n_it_edi_doi/models/res_company.py`
- `addons/l10n_it_edi_doi/models/res_partner.py`
- `addons/l10n_it_edi_doi/models/sale_order.py`
- `addons/l10n_it_edi_doi/security/ir.access.csv`
- `addons/l10n_it_edi_doi/tests/__init__.py`
- `addons/l10n_it_edi_doi/tests/common.py`
- `addons/l10n_it_edi_doi/tests/test_amounts_and_warnings.py`
- `addons/l10n_it_edi_doi/views/account_move_views.xml`
- `addons/l10n_it_edi_doi/views/l10n_it_edi_doi_declaration_of_intent_views.xml`
- `addons/l10n_it_edi_doi/views/report_invoice.xml`
- `addons/l10n_it_edi_doi/views/res_partner_views.xml`
- `addons/l10n_it_edi_doi/views/sale_ir_actions_report_templates.xml`
- `addons/l10n_it_edi_doi/views/sale_order_views.xml`
