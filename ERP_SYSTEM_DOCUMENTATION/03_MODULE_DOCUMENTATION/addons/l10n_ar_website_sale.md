# Module: l10n_ar_website_sale

- **Module ID:** MOD-123
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ar_website_sale`
- **Manifest:** `addons/l10n_ar_website_sale/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Bridge Website Sale for Argentina

**Scope evidence:** The module contains 13 files, including 8 Python, 2 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `website_sale`, `l10n_ar`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 2
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

- **Description:** 3 model declarations, 11 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/l10n_ar_website_sale/models/product_template.py:4`, `addons/l10n_ar_website_sale/models/res_config_settings.py:4`, `addons/l10n_ar_website_sale/models/website.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 1 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ar_website_sale/views/res_config_settings_views.xml:4`, `addons/l10n_ar_website_sale/views/templates.xml:4`, `addons/l10n_ar_website_sale/views/templates.xml:20`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_ar_website_sale/tests/test_l10n_ar_website_sale.py`, `addons/l10n_ar_website_sale/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `res_config_settings_view_form`, `l10n_ar_website_sale_product_price_inherit`, `l10n_ar_website_sale_products_item_inherit`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/l10n_ar_website_sale/views/templates.xml:4`, `addons/l10n_ar_website_sale/views/templates.xml:20`
- View/action field declarations: 2; representative evidence: `addons/l10n_ar_website_sale/views/res_config_settings_views.xml:6`, `addons/l10n_ar_website_sale/views/res_config_settings_views.xml:8`
- Browser assets: 1; representative files: `addons/l10n_ar_website_sale/static/src/interactions/product_page.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ar_website_sale/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `product.template` (addons/l10n_ar_website_sale/models/product_template.py:4); inherits `res.config.settings` (addons/l10n_ar_website_sale/models/res_config_settings.py:4); inherits `website` (addons/l10n_ar_website_sale/models/website.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_sale`, `l10n_ar`
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

- `addons/l10n_ar_website_sale/__init__.py`
- `addons/l10n_ar_website_sale/__manifest__.py`
- `addons/l10n_ar_website_sale/i18n/es_419.po`
- `addons/l10n_ar_website_sale/i18n/l10n_ar_website_sale.pot`
- `addons/l10n_ar_website_sale/models/__init__.py`
- `addons/l10n_ar_website_sale/models/product_template.py`
- `addons/l10n_ar_website_sale/models/res_config_settings.py`
- `addons/l10n_ar_website_sale/models/website.py`
- `addons/l10n_ar_website_sale/static/src/interactions/product_page.js`
- `addons/l10n_ar_website_sale/tests/__init__.py`
- `addons/l10n_ar_website_sale/tests/test_l10n_ar_website_sale.py`
- `addons/l10n_ar_website_sale/views/res_config_settings_views.xml`
- `addons/l10n_ar_website_sale/views/templates.xml`
