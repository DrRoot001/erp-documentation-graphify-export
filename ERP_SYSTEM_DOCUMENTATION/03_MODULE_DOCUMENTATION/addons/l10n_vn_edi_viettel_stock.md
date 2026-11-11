# Module: l10n_vn_edi_viettel_stock

- **Module ID:** MOD-344
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_vn_edi_viettel_stock`
- **Manifest:** `addons/l10n_vn_edi_viettel_stock/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Delivery E-invoicing using SInvoice by Viettel

**Manifest description:**

Vietnam - Delivery E-invoicing
==============================
Using SInvoice by Viettel

**Scope evidence:** The module contains 20 files, including 13 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_vn_edi_viettel`, `stock`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_vn_edi_viettel_stock/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 32 methods, 0 constraint handlers, 0 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/l10n_vn_edi_viettel_stock/models/res_config_settings.py:6`, `addons/l10n_vn_edi_viettel_stock/models/stock_move.py:6`, `addons/l10n_vn_edi_viettel_stock/models/stock_picking.py:11`, `addons/l10n_vn_edi_viettel_stock/models/stock_warehouse.py:6`, `addons/l10n_vn_edi_viettel_stock/models/res_company.py:6`, `addons/l10n_vn_edi_viettel_stock/wizard/l10n_vn_edi_send_wizard.py:9`, `addons/l10n_vn_edi_viettel_stock/wizard/l10n_vn_edi_template_field_line.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 5 record/template/menu identifiers.
- **Evidence:** `addons/l10n_vn_edi_viettel_stock/wizard/wizard_send_views.xml:3`, `addons/l10n_vn_edi_viettel_stock/views/stock_picking_views.xml:3`, `addons/l10n_vn_edi_viettel_stock/views/stock_picking_views.xml:41`, `addons/l10n_vn_edi_viettel_stock/views/res_config_settings_views.xml:3`, `addons/l10n_vn_edi_viettel_stock/views/stock_warehouse_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_vn_edi_viettel_stock/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_vn_edi_viettel_stock/views/stock_picking_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_vn_edi_viettel_stock/tests/test_stock_edi.py`, `addons/l10n_vn_edi_viettel_stock/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `view_l10n_vn_edi_viettel_stock_send_wizard_form`, `stock_picking_view_form_inherit_l10n_vn_edi_viettel_stock`, `l10n_vn_edi_fetch_sinvoice_files`, `res_config_settings_view_form_inherit_l10n_vn_edi_viettel_stock`, `stock_warehouse_view_form_inherit_sinvoice`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 8; representative evidence: `addons/l10n_vn_edi_viettel_stock/wizard/wizard_send_views.xml:5`, `addons/l10n_vn_edi_viettel_stock/wizard/wizard_send_views.xml:6`, `addons/l10n_vn_edi_viettel_stock/views/stock_picking_views.xml:5`, `addons/l10n_vn_edi_viettel_stock/views/stock_picking_views.xml:7`, `addons/l10n_vn_edi_viettel_stock/views/res_config_settings_views.xml:5`, `addons/l10n_vn_edi_viettel_stock/views/res_config_settings_views.xml:7`, `addons/l10n_vn_edi_viettel_stock/views/stock_warehouse_views.xml:5`, `addons/l10n_vn_edi_viettel_stock/views/stock_warehouse_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_vn_edi_viettel_stock/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_vn_edi_viettel_stock/views/stock_picking_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: inherits `res.config.settings` (addons/l10n_vn_edi_viettel_stock/models/res_config_settings.py:6); inherits `stock.move` (addons/l10n_vn_edi_viettel_stock/models/stock_move.py:6); inherits `stock.picking` (addons/l10n_vn_edi_viettel_stock/models/stock_picking.py:11); inherits `stock.warehouse` (addons/l10n_vn_edi_viettel_stock/models/stock_warehouse.py:6); inherits `res.company` (addons/l10n_vn_edi_viettel_stock/models/res_company.py:6); `l10n_vn_edi_viettel_stock.send_wizard` (addons/l10n_vn_edi_viettel_stock/wizard/l10n_vn_edi_send_wizard.py:9); `l10n_vn_edi_viettel_stock.template_field_line` (addons/l10n_vn_edi_viettel_stock/wizard/l10n_vn_edi_template_field_line.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_vn_edi_viettel`, `stock`
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

- `addons/l10n_vn_edi_viettel_stock/__init__.py`
- `addons/l10n_vn_edi_viettel_stock/__manifest__.py`
- `addons/l10n_vn_edi_viettel_stock/i18n/l10n_vn_edi_viettel_stock.pot`
- `addons/l10n_vn_edi_viettel_stock/i18n/vi.po`
- `addons/l10n_vn_edi_viettel_stock/models/__init__.py`
- `addons/l10n_vn_edi_viettel_stock/models/res_company.py`
- `addons/l10n_vn_edi_viettel_stock/models/res_config_settings.py`
- `addons/l10n_vn_edi_viettel_stock/models/stock_move.py`
- `addons/l10n_vn_edi_viettel_stock/models/stock_picking.py`
- `addons/l10n_vn_edi_viettel_stock/models/stock_warehouse.py`
- `addons/l10n_vn_edi_viettel_stock/security/ir.access.csv`
- `addons/l10n_vn_edi_viettel_stock/tests/__init__.py`
- `addons/l10n_vn_edi_viettel_stock/tests/test_stock_edi.py`
- `addons/l10n_vn_edi_viettel_stock/views/res_config_settings_views.xml`
- `addons/l10n_vn_edi_viettel_stock/views/stock_picking_views.xml`
- `addons/l10n_vn_edi_viettel_stock/views/stock_warehouse_views.xml`
- `addons/l10n_vn_edi_viettel_stock/wizard/__init__.py`
- `addons/l10n_vn_edi_viettel_stock/wizard/l10n_vn_edi_send_wizard.py`
- `addons/l10n_vn_edi_viettel_stock/wizard/l10n_vn_edi_template_field_line.py`
- `addons/l10n_vn_edi_viettel_stock/wizard/wizard_send_views.xml`
