# Module: l10n_it_stock_ddt

- **Module ID:** MOD-244
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_it_stock_ddt`
- **Manifest:** `addons/l10n_it_stock_ddt/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Documento di Trasporto (DDT)

Whenever goods are transferred between A and B, the DDT serves
as a legitimation e.g. when the police would stop you.

When you want to print an outgoing picking in an Italian company,
it will print you the DDT instead.  It is like the delivery
slip, but it also contains the value of the product,
the transportation reason, the carrier, ... which make it a DDT.

We also use a separate sequence for the DDT as the number should not
have any gaps and should only be applied at the moment the goods are sent.

When invoices are related to their sale order and the sale order with the
delivery, the system will automatically calculate the linked DDTs for every
invoice line to export in the FatturaPA XML.

**Scope evidence:** The module contains 16 files, including 8 Python, 6 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_it_edi`, `stock_delivery`, `stock_account`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 0
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 21 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/l10n_it_stock_ddt/models/account_invoice.py:8`, `addons/l10n_it_stock_ddt/models/stock_picking.py:7`, `addons/l10n_it_stock_ddt/models/stock_picking.py:57`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 0 JavaScript/TypeScript files; static XML analysis found 9 record/template/menu identifiers.
- **Evidence:** `addons/l10n_it_stock_ddt/report/l10n_it_ddt_report.xml:201`, `addons/l10n_it_stock_ddt/report/l10n_it_ddt_report.xml:3`, `addons/l10n_it_stock_ddt/report/l10n_it_ddt_report.xml:192`, `addons/l10n_it_stock_ddt/report/report_invoice.xml:3`, `addons/l10n_it_stock_ddt/data/l10n_it_ddt_template.xml:3`, `addons/l10n_it_stock_ddt/views/stock_picking_views.xml:3`, `addons/l10n_it_stock_ddt/views/stock_picking_views.xml:30`, `addons/l10n_it_stock_ddt/views/stock_picking_views.xml:41`, `addons/l10n_it_stock_ddt/views/account_invoice_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_it_stock_ddt/report/l10n_it_ddt_report.xml`, `addons/l10n_it_stock_ddt/tests/test_ddt.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_it_stock_ddt/tests/test_edi.py`, `addons/l10n_it_stock_ddt/tests/test_ddt.py`, `addons/l10n_it_stock_ddt/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `action_report_ddt`, `report_ddt_view`, `report_ddt`, `report_invoice_document`, `my_view_name`, `view_picking_form_inherit_l10n_it_ddt`, `view_picking_search_inherit_l10n_it_ddt`, `view_picking_tree_inherit_l10n_it_ddt`, `account_invoice_view_form_inherit_ddt`
- Menus: 0; representative evidence: Not found in module
- Templates: 4; representative evidence: `addons/l10n_it_stock_ddt/report/l10n_it_ddt_report.xml:3`, `addons/l10n_it_stock_ddt/report/l10n_it_ddt_report.xml:192`, `addons/l10n_it_stock_ddt/report/report_invoice.xml:3`, `addons/l10n_it_stock_ddt/data/l10n_it_ddt_template.xml:3`
- View/action field declarations: 9; representative evidence: `addons/l10n_it_stock_ddt/report/l10n_it_ddt_report.xml:203`, `addons/l10n_it_stock_ddt/views/stock_picking_views.xml:5`, `addons/l10n_it_stock_ddt/views/stock_picking_views.xml:7`, `addons/l10n_it_stock_ddt/views/stock_picking_views.xml:32`, `addons/l10n_it_stock_ddt/views/stock_picking_views.xml:34`, `addons/l10n_it_stock_ddt/views/stock_picking_views.xml:43`, `addons/l10n_it_stock_ddt/views/stock_picking_views.xml:45`, `addons/l10n_it_stock_ddt/views/account_invoice_views.xml:6`, `addons/l10n_it_stock_ddt/views/account_invoice_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_it_stock_ddt/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/l10n_it_stock_ddt/report/l10n_it_ddt_report.xml`, `addons/l10n_it_stock_ddt/tests/test_ddt.py`

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `account.move` (addons/l10n_it_stock_ddt/models/account_invoice.py:8); inherits `stock.picking` (addons/l10n_it_stock_ddt/models/stock_picking.py:7); inherits `stock.picking.type` (addons/l10n_it_stock_ddt/models/stock_picking.py:57)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_it_edi`, `stock_delivery`, `stock_account`
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

- `addons/l10n_it_stock_ddt/__init__.py`
- `addons/l10n_it_stock_ddt/__manifest__.py`
- `addons/l10n_it_stock_ddt/data/l10n_it_ddt_template.xml`
- `addons/l10n_it_stock_ddt/i18n/it.po`
- `addons/l10n_it_stock_ddt/i18n/l10n_it_stock_ddt.pot`
- `addons/l10n_it_stock_ddt/models/__init__.py`
- `addons/l10n_it_stock_ddt/models/account_invoice.py`
- `addons/l10n_it_stock_ddt/models/stock_picking.py`
- `addons/l10n_it_stock_ddt/report/l10n_it_ddt_report.xml`
- `addons/l10n_it_stock_ddt/report/report_invoice.xml`
- `addons/l10n_it_stock_ddt/tests/__init__.py`
- `addons/l10n_it_stock_ddt/tests/export_xmls/deferred_invoice.xml`
- `addons/l10n_it_stock_ddt/tests/test_ddt.py`
- `addons/l10n_it_stock_ddt/tests/test_edi.py`
- `addons/l10n_it_stock_ddt/views/account_invoice_views.xml`
- `addons/l10n_it_stock_ddt/views/stock_picking_views.xml`
