# Module: product_matrix

- **Module ID:** MOD-474
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/product_matrix`
- **Manifest:** `addons/product_matrix/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Technical module: Matrix Implementation

**Manifest description:**

Please refer to Sale Matrix or Purchase Matrix for the use of this module.

**Scope evidence:** The module contains 64 files, including 6 Python, 5 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 2
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 3 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/product_matrix/models/product_template.py:7`, `addons/product_matrix/models/product_template.py:69`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 2 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/product_matrix/data/product_matrix_demo.xml:4`, `addons/product_matrix/data/product_matrix_demo.xml:15`, `addons/product_matrix/data/product_matrix_demo.xml:33`, `addons/product_matrix/data/res_groups.xml:4`, `addons/product_matrix/views/matrix_templates.xml:3`, `addons/product_matrix/views/matrix_templates.xml:35`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/product_matrix/tests/common.py`, `addons/product_matrix/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `matrix_product_template_shirt`, `product_template_attribute_line_size`, `product_template_attribute_line_color`, `base.group_user`, `matrix`, `extra_price`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/product_matrix/views/matrix_templates.xml:3`, `addons/product_matrix/views/matrix_templates.xml:35`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 2; representative files: `addons/product_matrix/static/src/js/matrix_configurator_hook.js`, `addons/product_matrix/static/src/js/product_matrix_dialog.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/product_matrix/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `product.template` (addons/product_matrix/models/product_template.py:7); inherits `product.template.attribute.value` (addons/product_matrix/models/product_template.py:69)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`
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

- `addons/product_matrix/__init__.py`
- `addons/product_matrix/__manifest__.py`
- `addons/product_matrix/data/product_matrix_demo.xml`
- `addons/product_matrix/data/res_groups.xml`
- `addons/product_matrix/i18n/ar.po`
- `addons/product_matrix/i18n/az.po`
- `addons/product_matrix/i18n/bg.po`
- `addons/product_matrix/i18n/bs.po`
- `addons/product_matrix/i18n/ca.po`
- `addons/product_matrix/i18n/cs.po`
- `addons/product_matrix/i18n/da.po`
- `addons/product_matrix/i18n/de.po`
- `addons/product_matrix/i18n/el.po`
- `addons/product_matrix/i18n/es.po`
- `addons/product_matrix/i18n/es_419.po`
- `addons/product_matrix/i18n/et.po`
- `addons/product_matrix/i18n/fa.po`
- `addons/product_matrix/i18n/fi.po`
- `addons/product_matrix/i18n/fr.po`
- `addons/product_matrix/i18n/he.po`
- `addons/product_matrix/i18n/hi.po`
- `addons/product_matrix/i18n/hr.po`
- `addons/product_matrix/i18n/hu.po`
- `addons/product_matrix/i18n/id.po`
- `addons/product_matrix/i18n/it.po`
- `addons/product_matrix/i18n/ja.po`
- `addons/product_matrix/i18n/kab.po`
- `addons/product_matrix/i18n/ko.po`
- `addons/product_matrix/i18n/ku.po`
- `addons/product_matrix/i18n/lo.po`
- `addons/product_matrix/i18n/lt.po`
- `addons/product_matrix/i18n/lv.po`
- `addons/product_matrix/i18n/mn.po`
- `addons/product_matrix/i18n/my.po`
- `addons/product_matrix/i18n/nb.po`
- `addons/product_matrix/i18n/nl.po`
- `addons/product_matrix/i18n/pl.po`
- `addons/product_matrix/i18n/product_matrix.pot`
- `addons/product_matrix/i18n/pt.po`
- `addons/product_matrix/i18n/pt_BR.po`
- `addons/product_matrix/i18n/ro.po`
- `addons/product_matrix/i18n/ru.po`
- `addons/product_matrix/i18n/sk.po`
- `addons/product_matrix/i18n/sl.po`
- `addons/product_matrix/i18n/sr@latin.po`
- `addons/product_matrix/i18n/sv.po`
- `addons/product_matrix/i18n/th.po`
- `addons/product_matrix/i18n/tr.po`
- `addons/product_matrix/i18n/uk.po`
- `addons/product_matrix/i18n/uz.po`
- `addons/product_matrix/i18n/vi.po`
- `addons/product_matrix/i18n/zh_CN.po`
- `addons/product_matrix/i18n/zh_TW.po`
- `addons/product_matrix/models/__init__.py`
- `addons/product_matrix/models/product_template.py`
- `addons/product_matrix/static/img/matrix_mycompany_tshirt.jpeg`
- `addons/product_matrix/static/src/js/matrix_configurator_hook.js`
- `addons/product_matrix/static/src/js/product_matrix_dialog.js`
- `addons/product_matrix/static/src/scss/product_matrix.scss`
- `addons/product_matrix/static/src/xml/product_matrix.xml`
- `addons/product_matrix/static/src/xml/product_matrix_dialog.xml`
- `addons/product_matrix/tests/__init__.py`
- `addons/product_matrix/tests/common.py`
- `addons/product_matrix/views/matrix_templates.xml`
