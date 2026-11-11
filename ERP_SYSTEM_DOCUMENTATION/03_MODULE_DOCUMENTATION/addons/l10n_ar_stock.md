# Module: l10n_ar_stock

- **Module ID:** MOD-122
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ar_stock`
- **Manifest:** `addons/l10n_ar_stock/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Argentinean - Stock

**Scope evidence:** The module contains 19 files, including 10 Python, 7 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_ar`, `stock_account`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 7
- Browser asset files: 0
- Security files: 0
- Test files: 4
- Scheduled/automation evidence files: 6
- Reporting evidence files: 3

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 42 methods, 1 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/l10n_ar_stock/models/stock_picking_batch.py:4`, `addons/l10n_ar_stock/models/stock_picking_type.py:7`, `addons/l10n_ar_stock/models/stock_picking.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 0 JavaScript/TypeScript files; static XML analysis found 13 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ar_stock/data/ir_actions_server_data.xml:3`, `addons/l10n_ar_stock/data/ir_actions_server_data.xml:11`, `addons/l10n_ar_stock/data/ir_actions_server_data.xml:19`, `addons/l10n_ar_stock/data/ir_actions_server_data.xml:27`, `addons/l10n_ar_stock/data/mail_template_data.xml:5`, `addons/l10n_ar_stock/data/ir_cron_data.xml:4`, `addons/l10n_ar_stock/views/report_delivery_guide.xml:82`, `addons/l10n_ar_stock/views/report_delivery_guide.xml:5`, `addons/l10n_ar_stock/views/report_delivery_guide.xml:14`, `addons/l10n_ar_stock/views/report_delivery_guide.xml:75`, `addons/l10n_ar_stock/views/stock_picking_views.xml:4`, `addons/l10n_ar_stock/views/stock_picking_batch_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 6 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_ar_stock/__manifest__.py`, `addons/l10n_ar_stock/models/stock_picking.py`, `addons/l10n_ar_stock/data/ir_actions_server_data.xml`, `addons/l10n_ar_stock/data/ir_cron_data.xml`, `addons/l10n_ar_stock/tests/test_l10n_ar_delivery_guide_batch.py`, `addons/l10n_ar_stock/tests/test_l10n_ar_stock_batch.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 3 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_ar_stock/models/stock_picking.py`, `addons/l10n_ar_stock/views/report_delivery_guide.xml`, `addons/l10n_ar_stock/tests/test_l10n_ar_delivery_guide_batch.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/l10n_ar_stock/tests/test_l10n_ar_delivery_guide_batch.py`, `addons/l10n_ar_stock/tests/__init__.py`, `addons/l10n_ar_stock/tests/test_l10n_ar_stock_batch.py`, `addons/l10n_ar_stock/tests/test_l10n_ar_delivery_guide.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `action_generate_delivery_guide`, `action_send_delivery_guide`, `action_generate_delivery_guide_for_batch`, `action_send_delivery_guide_for_batch`, `email_template_ar_remitos_delivery_guide`, `ir_cron_l10n_ar_send_delivery_guide`, `action_delivery_guide_report_pdf`, `custom_header`, `report_delivery_document`, `report_delivery_guide`, `stock_picking_form_inherit_l10n_ar_stock`, `stock_picking_batch_form`, `view_picking_type_form_inherit_l10n_ar_stock`
- Menus: 0; representative evidence: Not found in module
- Templates: 3; representative evidence: `addons/l10n_ar_stock/views/report_delivery_guide.xml:5`, `addons/l10n_ar_stock/views/report_delivery_guide.xml:14`, `addons/l10n_ar_stock/views/report_delivery_guide.xml:75`
- View/action field declarations: 7; representative evidence: `addons/l10n_ar_stock/views/report_delivery_guide.xml:84`, `addons/l10n_ar_stock/views/stock_picking_views.xml:6`, `addons/l10n_ar_stock/views/stock_picking_views.xml:8`, `addons/l10n_ar_stock/views/stock_picking_batch_views.xml:5`, `addons/l10n_ar_stock/views/stock_picking_batch_views.xml:7`, `addons/l10n_ar_stock/views/stock_picking_type_views.xml:5`, `addons/l10n_ar_stock/views/stock_picking_type_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ar_stock/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_ar_stock/__manifest__.py`, `addons/l10n_ar_stock/models/stock_picking.py`, `addons/l10n_ar_stock/data/ir_actions_server_data.xml`, `addons/l10n_ar_stock/data/ir_cron_data.xml`, `addons/l10n_ar_stock/tests/test_l10n_ar_delivery_guide_batch.py`, `addons/l10n_ar_stock/tests/test_l10n_ar_stock_batch.py`
- **Report entry points:** `addons/l10n_ar_stock/models/stock_picking.py`, `addons/l10n_ar_stock/views/report_delivery_guide.xml`, `addons/l10n_ar_stock/tests/test_l10n_ar_delivery_guide_batch.py`

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `stock.picking.batch` (addons/l10n_ar_stock/models/stock_picking_batch.py:4); inherits `stock.picking.type` (addons/l10n_ar_stock/models/stock_picking_type.py:7); inherits `stock.picking` (addons/l10n_ar_stock/models/stock_picking.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_ar`, `stock_account`
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

- `addons/l10n_ar_stock/__init__.py`
- `addons/l10n_ar_stock/__manifest__.py`
- `addons/l10n_ar_stock/data/ir_actions_server_data.xml`
- `addons/l10n_ar_stock/data/ir_cron_data.xml`
- `addons/l10n_ar_stock/data/mail_template_data.xml`
- `addons/l10n_ar_stock/i18n/es_419.po`
- `addons/l10n_ar_stock/i18n/l10n_ar_stock.pot`
- `addons/l10n_ar_stock/models/__init__.py`
- `addons/l10n_ar_stock/models/stock_picking.py`
- `addons/l10n_ar_stock/models/stock_picking_batch.py`
- `addons/l10n_ar_stock/models/stock_picking_type.py`
- `addons/l10n_ar_stock/tests/__init__.py`
- `addons/l10n_ar_stock/tests/test_l10n_ar_delivery_guide.py`
- `addons/l10n_ar_stock/tests/test_l10n_ar_delivery_guide_batch.py`
- `addons/l10n_ar_stock/tests/test_l10n_ar_stock_batch.py`
- `addons/l10n_ar_stock/views/report_delivery_guide.xml`
- `addons/l10n_ar_stock/views/stock_picking_batch_views.xml`
- `addons/l10n_ar_stock/views/stock_picking_type_views.xml`
- `addons/l10n_ar_stock/views/stock_picking_views.xml`
