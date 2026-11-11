# Module: account_tax_python

- **Module ID:** MOD-014
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/account_tax_python`
- **Manifest:** `addons/account_tax_python/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Use python code to define taxes

**Manifest description:**

A tax defined as python code consists of two snippets of python code which are executed in a local environment containing data such as the unit price, product or partner.

"Applicable Code" defines if the tax is to be applied.

"Python Code" defines the amount of the tax.

**Scope evidence:** The module contains 64 files, including 8 Python, 1 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 1
- Browser asset files: 1
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 1 model declarations, 22 methods, 1 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/account_tax_python/models/account_tax.py:12`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 1 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/account_tax_python/views/account_tax_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/account_tax_python/tests/common.py`, `addons/account_tax_python/tests/test_taxes_computation.py`, `addons/account_tax_python/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `view_tax_form_inherited`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/account_tax_python/views/account_tax_views.xml:5`, `addons/account_tax_python/views/account_tax_views.xml:7`
- Browser assets: 1; representative files: `addons/account_tax_python/static/src/helpers/account_tax.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/account_tax_python/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `account.tax` (addons/account_tax_python/models/account_tax.py:12)
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

- `addons/account_tax_python/__init__.py`
- `addons/account_tax_python/__manifest__.py`
- `addons/account_tax_python/i18n/account_tax_python.pot`
- `addons/account_tax_python/i18n/ar.po`
- `addons/account_tax_python/i18n/az.po`
- `addons/account_tax_python/i18n/bg.po`
- `addons/account_tax_python/i18n/bs.po`
- `addons/account_tax_python/i18n/ca.po`
- `addons/account_tax_python/i18n/cs.po`
- `addons/account_tax_python/i18n/da.po`
- `addons/account_tax_python/i18n/de.po`
- `addons/account_tax_python/i18n/el.po`
- `addons/account_tax_python/i18n/es.po`
- `addons/account_tax_python/i18n/es_419.po`
- `addons/account_tax_python/i18n/et.po`
- `addons/account_tax_python/i18n/fa.po`
- `addons/account_tax_python/i18n/fi.po`
- `addons/account_tax_python/i18n/fr.po`
- `addons/account_tax_python/i18n/gu.po`
- `addons/account_tax_python/i18n/he.po`
- `addons/account_tax_python/i18n/hi.po`
- `addons/account_tax_python/i18n/hr.po`
- `addons/account_tax_python/i18n/hu.po`
- `addons/account_tax_python/i18n/id.po`
- `addons/account_tax_python/i18n/is.po`
- `addons/account_tax_python/i18n/it.po`
- `addons/account_tax_python/i18n/ja.po`
- `addons/account_tax_python/i18n/kab.po`
- `addons/account_tax_python/i18n/kk.po`
- `addons/account_tax_python/i18n/ko.po`
- `addons/account_tax_python/i18n/ku.po`
- `addons/account_tax_python/i18n/lo.po`
- `addons/account_tax_python/i18n/lt.po`
- `addons/account_tax_python/i18n/lv.po`
- `addons/account_tax_python/i18n/mn.po`
- `addons/account_tax_python/i18n/my.po`
- `addons/account_tax_python/i18n/nb.po`
- `addons/account_tax_python/i18n/nl.po`
- `addons/account_tax_python/i18n/pl.po`
- `addons/account_tax_python/i18n/pt.po`
- `addons/account_tax_python/i18n/pt_BR.po`
- `addons/account_tax_python/i18n/ro.po`
- `addons/account_tax_python/i18n/ru.po`
- `addons/account_tax_python/i18n/sk.po`
- `addons/account_tax_python/i18n/sl.po`
- `addons/account_tax_python/i18n/sr@latin.po`
- `addons/account_tax_python/i18n/sv.po`
- `addons/account_tax_python/i18n/ta.po`
- `addons/account_tax_python/i18n/te.po`
- `addons/account_tax_python/i18n/th.po`
- `addons/account_tax_python/i18n/tr.po`
- `addons/account_tax_python/i18n/uk.po`
- `addons/account_tax_python/i18n/uz.po`
- `addons/account_tax_python/i18n/vi.po`
- `addons/account_tax_python/i18n/zh_CN.po`
- `addons/account_tax_python/i18n/zh_TW.po`
- `addons/account_tax_python/models/__init__.py`
- `addons/account_tax_python/models/account_tax.py`
- `addons/account_tax_python/static/src/helpers/account_tax.js`
- `addons/account_tax_python/tests/__init__.py`
- `addons/account_tax_python/tests/common.py`
- `addons/account_tax_python/tests/test_taxes_computation.py`
- `addons/account_tax_python/tools/formula_utils.py`
- `addons/account_tax_python/views/account_tax_views.xml`
