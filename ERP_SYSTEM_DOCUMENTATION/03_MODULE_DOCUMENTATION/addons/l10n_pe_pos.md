# Module: l10n_pe_pos

- **Module ID:** MOD-291
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_pe_pos`
- **Manifest:** `addons/l10n_pe_pos/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module brings the technical requirement for the Peruvian regulation.
Install this if you are using the Point of Sale app in Peru.

**Scope evidence:** The module contains 22 files, including 12 Python, 3 XML, and 5 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_pe`, `point_of_sale`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 3
- Browser asset files: 5
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 11 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_pe_pos/models/res_partner.py:6`, `addons/l10n_pe_pos/models/pos_config.py:4`, `addons/l10n_pe_pos/models/pos_session.py:5`, `addons/l10n_pe_pos/models/res_city.py:5`, `addons/l10n_pe_pos/models/l10n_pe_res_city_district.py:5`, `addons/l10n_pe_pos/receipt/pos_order_receipt.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 5 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/l10n_pe_pos/data/res_partner_data.xml:4`, `addons/l10n_pe_pos/views/templates.xml:4`, `addons/l10n_pe_pos/views/res_partner_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_pe_pos/tests/test_pe_pos.py`, `addons/l10n_pe_pos/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `partner_pe_cf`, `ticket_validation_screen`, `view_partner_form_pos_ui_inherit_l10n_pe_pos`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/l10n_pe_pos/views/templates.xml:4`
- View/action field declarations: 2; representative evidence: `addons/l10n_pe_pos/views/res_partner_views.xml:5`, `addons/l10n_pe_pos/views/res_partner_views.xml:7`
- Browser assets: 5; representative files: `addons/l10n_pe_pos/static/src/overrides/components/ticket_screen/ticket_screen.js`, `addons/l10n_pe_pos/static/src/overrides/components/paymentt_screen/payment_screen.js`, `addons/l10n_pe_pos/static/src/app/services/pos_store.js`, `addons/l10n_pe_pos/static/src/app/utils/order_payment_validation.js`, `addons/l10n_pe_pos/static/src/app/utils/printer/generate_printer_data.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_pe_pos/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `res.partner` (addons/l10n_pe_pos/models/res_partner.py:6); inherits `pos.config` (addons/l10n_pe_pos/models/pos_config.py:4); inherits `pos.session` (addons/l10n_pe_pos/models/pos_session.py:5); `res.city` (addons/l10n_pe_pos/models/res_city.py:5); `l10n_pe.res.city.district` (addons/l10n_pe_pos/models/l10n_pe_res_city_district.py:5); inherits `pos.order.receipt` (addons/l10n_pe_pos/receipt/pos_order_receipt.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_pe`, `point_of_sale`
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

- `addons/l10n_pe_pos/__init__.py`
- `addons/l10n_pe_pos/__manifest__.py`
- `addons/l10n_pe_pos/data/res_partner_data.xml`
- `addons/l10n_pe_pos/i18n/es_419.po`
- `addons/l10n_pe_pos/i18n/l10n_pe_pos.pot`
- `addons/l10n_pe_pos/models/__init__.py`
- `addons/l10n_pe_pos/models/l10n_pe_res_city_district.py`
- `addons/l10n_pe_pos/models/pos_config.py`
- `addons/l10n_pe_pos/models/pos_session.py`
- `addons/l10n_pe_pos/models/res_city.py`
- `addons/l10n_pe_pos/models/res_partner.py`
- `addons/l10n_pe_pos/receipt/__init__.py`
- `addons/l10n_pe_pos/receipt/pos_order_receipt.py`
- `addons/l10n_pe_pos/static/src/app/services/pos_store.js`
- `addons/l10n_pe_pos/static/src/app/utils/order_payment_validation.js`
- `addons/l10n_pe_pos/static/src/app/utils/printer/generate_printer_data.js`
- `addons/l10n_pe_pos/static/src/overrides/components/paymentt_screen/payment_screen.js`
- `addons/l10n_pe_pos/static/src/overrides/components/ticket_screen/ticket_screen.js`
- `addons/l10n_pe_pos/tests/__init__.py`
- `addons/l10n_pe_pos/tests/test_pe_pos.py`
- `addons/l10n_pe_pos/views/res_partner_views.xml`
- `addons/l10n_pe_pos/views/templates.xml`
