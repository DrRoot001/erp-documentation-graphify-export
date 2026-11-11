# Module: test_sale_product_configurators

- **Module ID:** MOD-581
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/test_sale_product_configurators`
- **Manifest:** `addons/test_sale_product_configurators/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Test Suite for Sale Product Configurator

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 18 files, including 6 Python, 0 XML, and 12 JavaScript/TypeScript files. The manifest declares dependencies: `event_sale`, `sale_management`, `sale_product_matrix`.

## 2. Module structure

- Model/business logic files: 0
- Controller/API files: 0
- XML/data/view/template files: 0
- Browser asset files: 12
- Security files: 0
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### User interface and data

- **Description:** 0 XML files and 12 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/test_sale_product_configurators/tests/test_sale_product_matrix.py`, `addons/test_sale_product_configurators/tests/test_sale_product_configurator.py`, `addons/test_sale_product_configurators/tests/test_event_sale_with_product_configurator.py`, `addons/test_sale_product_configurators/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 0; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 12; representative files: `addons/test_sale_product_configurators/static/tests/tours/product_configurator_custom_value_update_tour.js`, `addons/test_sale_product_configurators/static/tests/tours/product_configurator_pricelist_ui.js`, `addons/test_sale_product_configurators/static/tests/tours/product_configurator_uom_choice.js`, `addons/test_sale_product_configurators/static/tests/tours/product_configurator_ui.js`, `addons/test_sale_product_configurators/static/tests/tours/product_configurator_recursive_optional_products.js`, `addons/test_sale_product_configurators/static/tests/tours/product_matrix_tour.js`, `addons/test_sale_product_configurators/static/tests/tours/product_configurator_advanced_ui.js`, `addons/test_sale_product_configurators/static/tests/tours/product_configurator_edition_ui.js`, `addons/test_sale_product_configurators/static/tests/tours/product_attribute_with_multi_type.js`, `addons/test_sale_product_configurators/static/tests/tours/product_configurator_single_custom_attribute_ui.js`, `addons/test_sale_product_configurators/static/tests/tours/product_configurator_optional_products_ui.js`, `addons/test_sale_product_configurators/static/tests/tours/event_sale_with_product_configurator_ui.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/test_sale_product_configurators/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `event_sale`, `sale_management`, `sale_product_matrix`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Not found
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/test_sale_product_configurators/__init__.py`
- `addons/test_sale_product_configurators/__manifest__.py`
- `addons/test_sale_product_configurators/static/tests/tours/event_sale_with_product_configurator_ui.js`
- `addons/test_sale_product_configurators/static/tests/tours/product_attribute_with_multi_type.js`
- `addons/test_sale_product_configurators/static/tests/tours/product_configurator_advanced_ui.js`
- `addons/test_sale_product_configurators/static/tests/tours/product_configurator_custom_value_update_tour.js`
- `addons/test_sale_product_configurators/static/tests/tours/product_configurator_edition_ui.js`
- `addons/test_sale_product_configurators/static/tests/tours/product_configurator_optional_products_ui.js`
- `addons/test_sale_product_configurators/static/tests/tours/product_configurator_pricelist_ui.js`
- `addons/test_sale_product_configurators/static/tests/tours/product_configurator_recursive_optional_products.js`
- `addons/test_sale_product_configurators/static/tests/tours/product_configurator_single_custom_attribute_ui.js`
- `addons/test_sale_product_configurators/static/tests/tours/product_configurator_ui.js`
- `addons/test_sale_product_configurators/static/tests/tours/product_configurator_uom_choice.js`
- `addons/test_sale_product_configurators/static/tests/tours/product_matrix_tour.js`
- `addons/test_sale_product_configurators/tests/__init__.py`
- `addons/test_sale_product_configurators/tests/test_event_sale_with_product_configurator.py`
- `addons/test_sale_product_configurators/tests/test_sale_product_configurator.py`
- `addons/test_sale_product_configurators/tests/test_sale_product_matrix.py`
