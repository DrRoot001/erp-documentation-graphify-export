# Module: l10n_tw_edi_ecpay_website_sale

- **Module ID:** MOD-331
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_tw_edi_ecpay_website_sale`
- **Manifest:** `addons/l10n_tw_edi_ecpay_website_sale/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website Sale/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** ECpay E-invoice bridge module for Ecommerce

**Manifest description:**

This bridge module allows the user to input Ecpay information in ecommerce for sending their invoices to the Ecpay system

**Scope evidence:** The module contains 18 files, including 10 Python, 2 XML, and 4 JavaScript/TypeScript files. The manifest declares dependencies: `website_sale`, `l10n_tw_edi_ecpay_sale`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 2
- XML/data/view/template files: 2
- Browser asset files: 4
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 25 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_tw_edi_ecpay_website_sale/models/res_partner.py:4`, `addons/l10n_tw_edi_ecpay_website_sale/models/website_checkout_step.py:6`, `addons/l10n_tw_edi_ecpay_website_sale/models/website.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 4 route declarations.
- **Evidence:** `addons/l10n_tw_edi_ecpay_website_sale/controllers/main.py:56`, `addons/l10n_tw_edi_ecpay_website_sale/controllers/main.py:77`, `addons/l10n_tw_edi_ecpay_website_sale/controllers/main.py:139`, `addons/l10n_tw_edi_ecpay_website_sale/controllers/main.py:148`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 4 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/l10n_tw_edi_ecpay_website_sale/data/data.xml:5`, `addons/l10n_tw_edi_ecpay_website_sale/views/templates.xml:4`, `addons/l10n_tw_edi_ecpay_website_sale/views/templates.xml:118`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_tw_edi_ecpay_website_sale/tests/test_l10n_tw_edi_website_sale.py`, `addons/l10n_tw_edi_ecpay_website_sale/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `l10n_tw_edi_ecpay_website_sale.checkout_step_invoicing`, `l10n_tw_edi_invoicing_info`, `address`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/l10n_tw_edi_ecpay_website_sale/views/templates.xml:4`, `addons/l10n_tw_edi_ecpay_website_sale/views/templates.xml:118`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 4; representative files: `addons/l10n_tw_edi_ecpay_website_sale/static/src/js/address.js`, `addons/l10n_tw_edi_ecpay_website_sale/static/src/js/invoicing_info.js`, `addons/l10n_tw_edi_ecpay_website_sale/static/src/js/edi_invoicing_info.js`, `addons/l10n_tw_edi_ecpay_website_sale/static/tests/tours/test_checkout.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_tw_edi_ecpay_website_sale/__manifest__.py`
- **HTTP entry points:** `addons/l10n_tw_edi_ecpay_website_sale/controllers/main.py:56`, `addons/l10n_tw_edi_ecpay_website_sale/controllers/main.py:77`, `addons/l10n_tw_edi_ecpay_website_sale/controllers/main.py:139`, `addons/l10n_tw_edi_ecpay_website_sale/controllers/main.py:148`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `res.partner` (addons/l10n_tw_edi_ecpay_website_sale/models/res_partner.py:4); inherits `website.checkout.step` (addons/l10n_tw_edi_ecpay_website_sale/models/website_checkout_step.py:6); inherits `website` (addons/l10n_tw_edi_ecpay_website_sale/models/website.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 4
- Route evidence: `addons/l10n_tw_edi_ecpay_website_sale/controllers/main.py:56`, `addons/l10n_tw_edi_ecpay_website_sale/controllers/main.py:77`, `addons/l10n_tw_edi_ecpay_website_sale/controllers/main.py:139`, `addons/l10n_tw_edi_ecpay_website_sale/controllers/main.py:148`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_sale`, `l10n_tw_edi_ecpay_sale`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_tw_edi_ecpay_website_sale/__init__.py`
- `addons/l10n_tw_edi_ecpay_website_sale/__manifest__.py`
- `addons/l10n_tw_edi_ecpay_website_sale/controllers/__init__.py`
- `addons/l10n_tw_edi_ecpay_website_sale/controllers/main.py`
- `addons/l10n_tw_edi_ecpay_website_sale/data/data.xml`
- `addons/l10n_tw_edi_ecpay_website_sale/i18n/l10n_tw_edi_ecpay_website_sale.pot`
- `addons/l10n_tw_edi_ecpay_website_sale/i18n/zh_TW.po`
- `addons/l10n_tw_edi_ecpay_website_sale/models/__init__.py`
- `addons/l10n_tw_edi_ecpay_website_sale/models/res_partner.py`
- `addons/l10n_tw_edi_ecpay_website_sale/models/website.py`
- `addons/l10n_tw_edi_ecpay_website_sale/models/website_checkout_step.py`
- `addons/l10n_tw_edi_ecpay_website_sale/static/src/js/address.js`
- `addons/l10n_tw_edi_ecpay_website_sale/static/src/js/edi_invoicing_info.js`
- `addons/l10n_tw_edi_ecpay_website_sale/static/src/js/invoicing_info.js`
- `addons/l10n_tw_edi_ecpay_website_sale/static/tests/tours/test_checkout.js`
- `addons/l10n_tw_edi_ecpay_website_sale/tests/__init__.py`
- `addons/l10n_tw_edi_ecpay_website_sale/tests/test_l10n_tw_edi_website_sale.py`
- `addons/l10n_tw_edi_ecpay_website_sale/views/templates.xml`
