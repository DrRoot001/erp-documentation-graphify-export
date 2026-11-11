# Module: l10n_ro_edi_stock

- **Module ID:** MOD-306
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ro_edi_stock`
- **Manifest:** `addons/l10n_ro_edi_stock/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

E-Transport implementation for Romania

**Scope evidence:** The module contains 29 files, including 13 Python, 13 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `stock_delivery`, `l10n_ro_edi`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 13
- Browser asset files: 1
- Security files: 0
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 78 methods, 0 constraint handlers, 2 onchange handlers, and 20 dependency declarations.
- **Evidence:** `addons/l10n_ro_edi_stock/models/delivery_carrier.py:4`, `addons/l10n_ro_edi_stock/models/stock_picking_batch.py:12`, `addons/l10n_ro_edi_stock/models/l10n_ro_edi_stock_document.py:10`, `addons/l10n_ro_edi_stock/models/stock_picking.py:249`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 13 XML files and 1 JavaScript/TypeScript files; static XML analysis found 11 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ro_edi_stock/report/report_picking_batch.xml:3`, `addons/l10n_ro_edi_stock/report/report_deliveryslip.xml:3`, `addons/l10n_ro_edi_stock/data/template_etransport.xml:3`, `addons/l10n_ro_edi_stock/views/stock_picking_views.xml:3`, `addons/l10n_ro_edi_stock/views/stock_picking_views.xml:104`, `addons/l10n_ro_edi_stock/views/stock_picking_views.xml:117`, `addons/l10n_ro_edi_stock/views/res_config_settings_views.xml:3`, `addons/l10n_ro_edi_stock/views/stock_picking_batch_views.xml:3`, `addons/l10n_ro_edi_stock/views/stock_picking_batch_views.xml:101`, `addons/l10n_ro_edi_stock/views/stock_picking_batch_views.xml:116`, `addons/l10n_ro_edi_stock/views/delivery_carrier_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/l10n_ro_edi_stock/tests/test_etransport_dropship_flows.py`, `addons/l10n_ro_edi_stock/tests/test_etransport_flows.py`, `addons/l10n_ro_edi_stock/tests/common.py`, `addons/l10n_ro_edi_stock/tests/__init__.py`, `addons/l10n_ro_edi_stock/tests/test_batch_stock_etransport.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 13; representative identifiers: `report_picking_batch`, `l10n_ro_edi_stock_report_delivery_document`, `l10n_ro_template_etransport`, `l10n_ro_edi_stock_view_picking_form`, `l10n_ro_edi_stock_stock_picking_view_tree`, `l10n_ro_edi_stock_stock_picking_filter`, `res_config_settings_form_inherit_l10n_ro_edi`, `stock_picking_batch_form`, `stock_picking_batch_tree`, `stock_picking_batch_filter`, `l10n_ro_edi_stock_view_delivery_carrier_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 3; representative evidence: `addons/l10n_ro_edi_stock/report/report_picking_batch.xml:3`, `addons/l10n_ro_edi_stock/report/report_deliveryslip.xml:3`, `addons/l10n_ro_edi_stock/data/template_etransport.xml:3`
- View/action field declarations: 16; representative evidence: `addons/l10n_ro_edi_stock/views/stock_picking_views.xml:5`, `addons/l10n_ro_edi_stock/views/stock_picking_views.xml:7`, `addons/l10n_ro_edi_stock/views/stock_picking_views.xml:105`, `addons/l10n_ro_edi_stock/views/stock_picking_views.xml:107`, `addons/l10n_ro_edi_stock/views/stock_picking_views.xml:118`, `addons/l10n_ro_edi_stock/views/stock_picking_views.xml:120`, `addons/l10n_ro_edi_stock/views/res_config_settings_views.xml:5`, `addons/l10n_ro_edi_stock/views/res_config_settings_views.xml:7`, `addons/l10n_ro_edi_stock/views/stock_picking_batch_views.xml:5`, `addons/l10n_ro_edi_stock/views/stock_picking_batch_views.xml:7`, `addons/l10n_ro_edi_stock/views/stock_picking_batch_views.xml:102`, `addons/l10n_ro_edi_stock/views/stock_picking_batch_views.xml:104`
- Browser assets: 1; representative files: `addons/l10n_ro_edi_stock/static/src/components/document_state/document_state_field.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ro_edi_stock/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `delivery.carrier` (addons/l10n_ro_edi_stock/models/delivery_carrier.py:4); inherits `stock.picking.batch` (addons/l10n_ro_edi_stock/models/stock_picking_batch.py:12); inherits `l10n_ro_edi.document` (addons/l10n_ro_edi_stock/models/l10n_ro_edi_stock_document.py:10); inherits `stock.picking` (addons/l10n_ro_edi_stock/models/stock_picking.py:249)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `stock_delivery`, `l10n_ro_edi`
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

- `addons/l10n_ro_edi_stock/__init__.py`
- `addons/l10n_ro_edi_stock/__manifest__.py`
- `addons/l10n_ro_edi_stock/data/template_etransport.xml`
- `addons/l10n_ro_edi_stock/i18n/l10n_ro_edi_stock.pot`
- `addons/l10n_ro_edi_stock/i18n/ro.po`
- `addons/l10n_ro_edi_stock/models/__init__.py`
- `addons/l10n_ro_edi_stock/models/delivery_carrier.py`
- `addons/l10n_ro_edi_stock/models/etransport_api.py`
- `addons/l10n_ro_edi_stock/models/l10n_ro_edi_stock_document.py`
- `addons/l10n_ro_edi_stock/models/stock_picking.py`
- `addons/l10n_ro_edi_stock/models/stock_picking_batch.py`
- `addons/l10n_ro_edi_stock/report/report_deliveryslip.xml`
- `addons/l10n_ro_edi_stock/report/report_picking_batch.xml`
- `addons/l10n_ro_edi_stock/static/src/components/document_state/document_state_field.js`
- `addons/l10n_ro_edi_stock/tests/__init__.py`
- `addons/l10n_ro_edi_stock/tests/common.py`
- `addons/l10n_ro_edi_stock/tests/test_batch_stock_etransport.py`
- `addons/l10n_ro_edi_stock/tests/test_etransport_dropship_flows.py`
- `addons/l10n_ro_edi_stock/tests/test_etransport_flows.py`
- `addons/l10n_ro_edi_stock/tests/test_files/test_dropship_domestic_vendor_b2c_1.xml`
- `addons/l10n_ro_edi_stock/tests/test_files/test_dropship_foreign_vendor_b2c_1.xml`
- `addons/l10n_ro_edi_stock/tests/test_files/test_export_1.xml`
- `addons/l10n_ro_edi_stock/tests/test_files/test_intra_community_purchase_1.xml`
- `addons/l10n_ro_edi_stock/tests/test_files/test_send_and_amend_etransport_1.xml`
- `addons/l10n_ro_edi_stock/tests/test_files/test_send_and_amend_etransport_2.xml`
- `addons/l10n_ro_edi_stock/views/delivery_carrier_views.xml`
- `addons/l10n_ro_edi_stock/views/res_config_settings_views.xml`
- `addons/l10n_ro_edi_stock/views/stock_picking_batch_views.xml`
- `addons/l10n_ro_edi_stock/views/stock_picking_views.xml`
