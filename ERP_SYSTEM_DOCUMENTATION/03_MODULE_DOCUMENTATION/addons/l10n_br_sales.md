# Module: l10n_br_sales

- **Module ID:** MOD-140
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_br_sales`
- **Manifest:** `addons/l10n_br_sales/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Sale modifications for Brazil

**Scope evidence:** The module contains 9 files, including 4 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_br`, `sale`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 3
- Browser asset files: 0
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 1 model declarations, 2 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_br_sales/models/sale_order.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 4 record/template/menu identifiers.
- **Evidence:** `addons/l10n_br_sales/report/report_invoice_templates.xml:3`, `addons/l10n_br_sales/report/sale_order_templates.xml:3`, `addons/l10n_br_sales/report/sale_order_templates.xml:13`, `addons/l10n_br_sales/views/sale_portal_templates.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `document_tax_totals_brazil`, `report_saleorder_document`, `report_saleorder_document_brazil`, `sale_order_portal_content_brazil`
- Menus: 0; representative evidence: Not found in module
- Templates: 4; representative evidence: `addons/l10n_br_sales/report/report_invoice_templates.xml:3`, `addons/l10n_br_sales/report/sale_order_templates.xml:3`, `addons/l10n_br_sales/report/sale_order_templates.xml:13`, `addons/l10n_br_sales/views/sale_portal_templates.xml:3`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_br_sales/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `sale.order` (addons/l10n_br_sales/models/sale_order.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_br`, `sale`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_br_sales/__init__.py`
- `addons/l10n_br_sales/__manifest__.py`
- `addons/l10n_br_sales/i18n/l10n_br_sales.pot`
- `addons/l10n_br_sales/i18n/pt_BR.po`
- `addons/l10n_br_sales/models/__init__.py`
- `addons/l10n_br_sales/models/sale_order.py`
- `addons/l10n_br_sales/report/report_invoice_templates.xml`
- `addons/l10n_br_sales/report/sale_order_templates.xml`
- `addons/l10n_br_sales/views/sale_portal_templates.xml`
