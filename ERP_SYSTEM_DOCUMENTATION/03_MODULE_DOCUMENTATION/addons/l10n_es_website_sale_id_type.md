# Module: l10n_es_website_sale_id_type

- **Module ID:** MOD-183
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_es_website_sale_id_type`
- **Manifest:** `addons/l10n_es_website_sale_id_type/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Let customers pick the type of their identification document at checkout

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 11 files, including 8 Python, 1 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_es_website_sale`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 2
- XML/data/view/template files: 1
- Browser asset files: 1
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 1 model declarations, 28 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_es_website_sale_id_type/models/res_partner.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/l10n_es_website_sale_id_type/controllers/main.py`, `addons/l10n_es_website_sale_id_type/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 1 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/l10n_es_website_sale_id_type/views/address_form_templates.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_es_website_sale_id_type/tests/test_checkout_identification.py`, `addons/l10n_es_website_sale_id_type/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `Address Form: Spain ID Type`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/l10n_es_website_sale_id_type/views/address_form_templates.xml:3`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 1; representative files: `addons/l10n_es_website_sale_id_type/static/src/interactions/l10n_es_id_type.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_es_website_sale_id_type/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `res.partner` (addons/l10n_es_website_sale_id_type/models/res_partner.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_es_website_sale`
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

- `addons/l10n_es_website_sale_id_type/__init__.py`
- `addons/l10n_es_website_sale_id_type/__manifest__.py`
- `addons/l10n_es_website_sale_id_type/controllers/__init__.py`
- `addons/l10n_es_website_sale_id_type/controllers/main.py`
- `addons/l10n_es_website_sale_id_type/i18n/l10n_es_website_sale_id_type.pot`
- `addons/l10n_es_website_sale_id_type/models/__init__.py`
- `addons/l10n_es_website_sale_id_type/models/res_partner.py`
- `addons/l10n_es_website_sale_id_type/static/src/interactions/l10n_es_id_type.js`
- `addons/l10n_es_website_sale_id_type/tests/__init__.py`
- `addons/l10n_es_website_sale_id_type/tests/test_checkout_identification.py`
- `addons/l10n_es_website_sale_id_type/views/address_form_templates.xml`
