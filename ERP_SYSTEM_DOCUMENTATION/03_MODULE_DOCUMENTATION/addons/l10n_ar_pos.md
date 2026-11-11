# Module: l10n_ar_pos

- **Module ID:** MOD-121
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ar_pos`
- **Manifest:** `addons/l10n_ar_pos/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module brings the technical requirement for the Argentinean regulation.
Install this if you are using the Point of Sale app in Argentina.

**Scope evidence:** The module contains 20 files, including 10 Python, 2 XML, and 6 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_ar`, `point_of_sale`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 6
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 9 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_ar_pos/models/res_partner.py:6`, `addons/l10n_ar_pos/models/pos_config.py:4`, `addons/l10n_ar_pos/models/pos_session.py:5`, `addons/l10n_ar_pos/models/l10n_ar_afip_responsibility_type.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 6 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ar_pos/views/templates.xml:4`, `addons/l10n_ar_pos/views/res_partner_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_ar_pos/tests/__init__.py`, `addons/l10n_ar_pos/tests/test_ar_pos.py`, `addons/l10n_ar_pos/tests/test_pos_ar.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `ticket_validation_screen`, `view_partner_form_pos_ui_inherit_l10n_ar_pos`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/l10n_ar_pos/views/templates.xml:4`
- View/action field declarations: 2; representative evidence: `addons/l10n_ar_pos/views/res_partner_views.xml:5`, `addons/l10n_ar_pos/views/res_partner_views.xml:7`
- Browser assets: 6; representative files: `addons/l10n_ar_pos/static/src/app/services/pos_store.js`, `addons/l10n_ar_pos/static/src/app/models/pos_order.js`, `addons/l10n_ar_pos/static/src/app/screens/product_screen/product_screen.js`, `addons/l10n_ar_pos/static/src/app/screens/ticket_screen/ticket_screen.js`, `addons/l10n_ar_pos/static/src/app/screens/payment_screen/payment_screen.js`, `addons/l10n_ar_pos/static/tests/tours/l10n_ar_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ar_pos/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `res.partner` (addons/l10n_ar_pos/models/res_partner.py:6); inherits `pos.config` (addons/l10n_ar_pos/models/pos_config.py:4); inherits `pos.session` (addons/l10n_ar_pos/models/pos_session.py:5); `l10n_ar.afip.responsibility.type` (addons/l10n_ar_pos/models/l10n_ar_afip_responsibility_type.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_ar`, `point_of_sale`
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

- `addons/l10n_ar_pos/__init__.py`
- `addons/l10n_ar_pos/__manifest__.py`
- `addons/l10n_ar_pos/i18n/es_419.po`
- `addons/l10n_ar_pos/i18n/l10n_ar_pos.pot`
- `addons/l10n_ar_pos/models/__init__.py`
- `addons/l10n_ar_pos/models/l10n_ar_afip_responsibility_type.py`
- `addons/l10n_ar_pos/models/pos_config.py`
- `addons/l10n_ar_pos/models/pos_session.py`
- `addons/l10n_ar_pos/models/res_partner.py`
- `addons/l10n_ar_pos/static/src/app/models/pos_order.js`
- `addons/l10n_ar_pos/static/src/app/screens/payment_screen/payment_screen.js`
- `addons/l10n_ar_pos/static/src/app/screens/product_screen/product_screen.js`
- `addons/l10n_ar_pos/static/src/app/screens/ticket_screen/ticket_screen.js`
- `addons/l10n_ar_pos/static/src/app/services/pos_store.js`
- `addons/l10n_ar_pos/static/tests/tours/l10n_ar_tour.js`
- `addons/l10n_ar_pos/tests/__init__.py`
- `addons/l10n_ar_pos/tests/test_ar_pos.py`
- `addons/l10n_ar_pos/tests/test_pos_ar.py`
- `addons/l10n_ar_pos/views/res_partner_views.xml`
- `addons/l10n_ar_pos/views/templates.xml`
