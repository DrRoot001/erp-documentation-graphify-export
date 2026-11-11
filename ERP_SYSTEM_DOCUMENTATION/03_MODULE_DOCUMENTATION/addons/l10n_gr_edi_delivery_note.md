# Module: l10n_gr_edi_delivery_note

- **Module ID:** MOD-209
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_gr_edi_delivery_note`
- **Manifest:** `addons/l10n_gr_edi_delivery_note/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Transmit Greece myDATA EDI for Delivery Notes

**Manifest description:**

This module allows transmitting electronic Delivery Notes
        to Greece's tax authority myDATA platform.

**Scope evidence:** The module contains 16 files, including 9 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_gr_edi`, `stock`, `sale`, `sale_stock`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_gr_edi_delivery_note/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 31 methods, 0 constraint handlers, 4 onchange handlers, and 5 dependency declarations.
- **Evidence:** `addons/l10n_gr_edi_delivery_note/models/stock_move.py:14`, `addons/l10n_gr_edi_delivery_note/models/stock_picking.py:9`, `addons/l10n_gr_edi_delivery_note/models/l10n_gr_edi_document.py:4`, `addons/l10n_gr_edi_delivery_note/models/account_move.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 5 record/template/menu identifiers.
- **Evidence:** `addons/l10n_gr_edi_delivery_note/views/stock_picking_views.xml:4`, `addons/l10n_gr_edi_delivery_note/views/stock_picking_views.xml:115`, `addons/l10n_gr_edi_delivery_note/views/res_company_views.xml:4`, `addons/l10n_gr_edi_delivery_note/views/report_deliveryslip.xml:4`, `addons/l10n_gr_edi_delivery_note/views/res_partner_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_gr_edi_delivery_note/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_gr_edi_delivery_note/models/stock_picking.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_gr_edi_delivery_note/tests/test_mydata_delivery_note.py`, `addons/l10n_gr_edi_delivery_note/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `stock_picking_form_inherit_l10n_gr_edi`, `view_out_vpicktree_inherit_l10n_gr_edi`, `view_company_form_inherit_mydata_required_fields`, `report_delivery_document`, `view_partner_form_inherit_mydata_required_fields`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/l10n_gr_edi_delivery_note/views/report_deliveryslip.xml:4`
- View/action field declarations: 8; representative evidence: `addons/l10n_gr_edi_delivery_note/views/stock_picking_views.xml:6`, `addons/l10n_gr_edi_delivery_note/views/stock_picking_views.xml:8`, `addons/l10n_gr_edi_delivery_note/views/stock_picking_views.xml:117`, `addons/l10n_gr_edi_delivery_note/views/stock_picking_views.xml:119`, `addons/l10n_gr_edi_delivery_note/views/res_company_views.xml:6`, `addons/l10n_gr_edi_delivery_note/views/res_company_views.xml:9`, `addons/l10n_gr_edi_delivery_note/views/res_partner_views.xml:6`, `addons/l10n_gr_edi_delivery_note/views/res_partner_views.xml:9`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_gr_edi_delivery_note/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/l10n_gr_edi_delivery_note/models/stock_picking.py`

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `stock.move` (addons/l10n_gr_edi_delivery_note/models/stock_move.py:14); inherits `stock.picking` (addons/l10n_gr_edi_delivery_note/models/stock_picking.py:9); inherits `l10n_gr_edi.document` (addons/l10n_gr_edi_delivery_note/models/l10n_gr_edi_document.py:4); inherits `account.move` (addons/l10n_gr_edi_delivery_note/models/account_move.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_gr_edi`, `stock`, `sale`, `sale_stock`
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

- `addons/l10n_gr_edi_delivery_note/__init__.py`
- `addons/l10n_gr_edi_delivery_note/__manifest__.py`
- `addons/l10n_gr_edi_delivery_note/i18n/el.po`
- `addons/l10n_gr_edi_delivery_note/i18n/l10n_gr_edi_delivery_note.pot`
- `addons/l10n_gr_edi_delivery_note/models/__init__.py`
- `addons/l10n_gr_edi_delivery_note/models/account_move.py`
- `addons/l10n_gr_edi_delivery_note/models/l10n_gr_edi_document.py`
- `addons/l10n_gr_edi_delivery_note/models/stock_move.py`
- `addons/l10n_gr_edi_delivery_note/models/stock_picking.py`
- `addons/l10n_gr_edi_delivery_note/security/ir.access.csv`
- `addons/l10n_gr_edi_delivery_note/tests/__init__.py`
- `addons/l10n_gr_edi_delivery_note/tests/test_mydata_delivery_note.py`
- `addons/l10n_gr_edi_delivery_note/views/report_deliveryslip.xml`
- `addons/l10n_gr_edi_delivery_note/views/res_company_views.xml`
- `addons/l10n_gr_edi_delivery_note/views/res_partner_views.xml`
- `addons/l10n_gr_edi_delivery_note/views/stock_picking_views.xml`
