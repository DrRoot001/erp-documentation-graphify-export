# Module: l10n_in_ewaybill_stock

- **Module ID:** MOD-232
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_in_ewaybill_stock`
- **Manifest:** `addons/l10n_in_ewaybill_stock/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Indian E-waybill for Stock
==========================

This module enables users to create E-waybill from Inventory App without generating an invoice

**Scope evidence:** The module contains 15 files, including 8 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_in_stock`, `l10n_in_ewaybill`.

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

**Security evidence:** `addons/l10n_in_ewaybill_stock/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 29 methods, 0 constraint handlers, 0 onchange handlers, and 5 dependency declarations.
- **Evidence:** `addons/l10n_in_ewaybill_stock/models/stock_move.py:9`, `addons/l10n_in_ewaybill_stock/models/stock_picking.py:7`, `addons/l10n_in_ewaybill_stock/models/l10n_in_ewaybill.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 13 record/template/menu identifiers.
- **Evidence:** `addons/l10n_in_ewaybill_stock/report/ewaybill_report_inherit.xml:3`, `addons/l10n_in_ewaybill_stock/data/ewaybill_type_data.xml:3`, `addons/l10n_in_ewaybill_stock/data/ewaybill_type_data.xml:11`, `addons/l10n_in_ewaybill_stock/data/ewaybill_type_data.xml:19`, `addons/l10n_in_ewaybill_stock/data/ewaybill_type_data.xml:27`, `addons/l10n_in_ewaybill_stock/data/ewaybill_type_data.xml:35`, `addons/l10n_in_ewaybill_stock/data/ewaybill_type_data.xml:43`, `addons/l10n_in_ewaybill_stock/data/ewaybill_type_data.xml:51`, `addons/l10n_in_ewaybill_stock/data/ewaybill_type_data.xml:59`, `addons/l10n_in_ewaybill_stock/data/ewaybill_type_data.xml:67`, `addons/l10n_in_ewaybill_stock/views/stock_picking_views.xml:3`, `addons/l10n_in_ewaybill_stock/views/stock_picking_views.xml:35`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_in_ewaybill_stock/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_in_ewaybill_stock/tests/test_ewaybill_stock.py`, `addons/l10n_in_ewaybill_stock/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `l10n_in_ewaybill_stock_inherit_report`, `type_delivery_challan_sub_job_work`, `type_delivery_challan_sub_skd_ckd_work`, `type_delivery_challan_sub_recipient_not_known`, `type_delivery_challan_sub_for_own_use`, `type_delivery_challan_sub_exhibition_or_fairs`, `type_delivery_challan_sub_line_sales`, `type_delivery_challan_sub_others`, `type_delivery_challan_sub_job_work_returns`, `type_delivery_challan_sub_sales_return`, `view_picking_form_inherit_ewaybill`, `view_picking_list_inherit_ewaybill`, `view_l10n_in_ewaybill_stock_inherit`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/l10n_in_ewaybill_stock/report/ewaybill_report_inherit.xml:3`
- View/action field declarations: 6; representative evidence: `addons/l10n_in_ewaybill_stock/views/stock_picking_views.xml:5`, `addons/l10n_in_ewaybill_stock/views/stock_picking_views.xml:7`, `addons/l10n_in_ewaybill_stock/views/stock_picking_views.xml:37`, `addons/l10n_in_ewaybill_stock/views/stock_picking_views.xml:39`, `addons/l10n_in_ewaybill_stock/views/l10n_in_ewaybill_views.xml:5`, `addons/l10n_in_ewaybill_stock/views/l10n_in_ewaybill_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_in_ewaybill_stock/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `stock.move` (addons/l10n_in_ewaybill_stock/models/stock_move.py:9); inherits `stock.picking` (addons/l10n_in_ewaybill_stock/models/stock_picking.py:7); inherits `l10n.in.ewaybill` (addons/l10n_in_ewaybill_stock/models/l10n_in_ewaybill.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_in_stock`, `l10n_in_ewaybill`
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

- `addons/l10n_in_ewaybill_stock/__init__.py`
- `addons/l10n_in_ewaybill_stock/__manifest__.py`
- `addons/l10n_in_ewaybill_stock/data/ewaybill_type_data.xml`
- `addons/l10n_in_ewaybill_stock/i18n/hi.po`
- `addons/l10n_in_ewaybill_stock/i18n/l10n_in_ewaybill_stock.pot`
- `addons/l10n_in_ewaybill_stock/models/__init__.py`
- `addons/l10n_in_ewaybill_stock/models/l10n_in_ewaybill.py`
- `addons/l10n_in_ewaybill_stock/models/stock_move.py`
- `addons/l10n_in_ewaybill_stock/models/stock_picking.py`
- `addons/l10n_in_ewaybill_stock/report/ewaybill_report_inherit.xml`
- `addons/l10n_in_ewaybill_stock/security/ir.access.csv`
- `addons/l10n_in_ewaybill_stock/tests/__init__.py`
- `addons/l10n_in_ewaybill_stock/tests/test_ewaybill_stock.py`
- `addons/l10n_in_ewaybill_stock/views/l10n_in_ewaybill_views.xml`
- `addons/l10n_in_ewaybill_stock/views/stock_picking_views.xml`
