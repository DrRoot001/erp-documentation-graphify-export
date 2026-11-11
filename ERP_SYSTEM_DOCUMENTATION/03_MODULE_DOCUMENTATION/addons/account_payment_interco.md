# Module: account_payment_interco

- **Module ID:** MOD-010
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/account_payment_interco`
- **Manifest:** `addons/account_payment_interco/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Enable Intercompany payments to reconcile with their invoices on post.

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 58 files, including 8 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account_payment`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 1
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 12 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/account_payment_interco/models/res_config_settings.py:4`, `addons/account_payment_interco/models/account_move.py:6`, `addons/account_payment_interco/models/res_company.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/account_payment_interco/views/res_config_settings_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/account_payment_interco/tests/test_interco_clearing.py`, `addons/account_payment_interco/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `res_config_settings_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/account_payment_interco/views/res_config_settings_views.xml:5`, `addons/account_payment_interco/views/res_config_settings_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/account_payment_interco/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `res.config.settings` (addons/account_payment_interco/models/res_config_settings.py:4); inherits `account.move` (addons/account_payment_interco/models/account_move.py:6); inherits `res.company` (addons/account_payment_interco/models/res_company.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account_payment`
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

- `addons/account_payment_interco/__init__.py`
- `addons/account_payment_interco/__manifest__.py`
- `addons/account_payment_interco/i18n/account_payment_interco.pot`
- `addons/account_payment_interco/i18n/ar.po`
- `addons/account_payment_interco/i18n/az.po`
- `addons/account_payment_interco/i18n/bg.po`
- `addons/account_payment_interco/i18n/bs.po`
- `addons/account_payment_interco/i18n/ca.po`
- `addons/account_payment_interco/i18n/cs.po`
- `addons/account_payment_interco/i18n/da.po`
- `addons/account_payment_interco/i18n/de.po`
- `addons/account_payment_interco/i18n/el.po`
- `addons/account_payment_interco/i18n/es.po`
- `addons/account_payment_interco/i18n/es_419.po`
- `addons/account_payment_interco/i18n/et.po`
- `addons/account_payment_interco/i18n/fa.po`
- `addons/account_payment_interco/i18n/fi.po`
- `addons/account_payment_interco/i18n/fr.po`
- `addons/account_payment_interco/i18n/he.po`
- `addons/account_payment_interco/i18n/hi.po`
- `addons/account_payment_interco/i18n/hr.po`
- `addons/account_payment_interco/i18n/hu.po`
- `addons/account_payment_interco/i18n/id.po`
- `addons/account_payment_interco/i18n/it.po`
- `addons/account_payment_interco/i18n/ja.po`
- `addons/account_payment_interco/i18n/kab.po`
- `addons/account_payment_interco/i18n/ko.po`
- `addons/account_payment_interco/i18n/ku.po`
- `addons/account_payment_interco/i18n/lo.po`
- `addons/account_payment_interco/i18n/lt.po`
- `addons/account_payment_interco/i18n/lv.po`
- `addons/account_payment_interco/i18n/mn.po`
- `addons/account_payment_interco/i18n/my.po`
- `addons/account_payment_interco/i18n/nb.po`
- `addons/account_payment_interco/i18n/nl.po`
- `addons/account_payment_interco/i18n/pl.po`
- `addons/account_payment_interco/i18n/pt.po`
- `addons/account_payment_interco/i18n/pt_BR.po`
- `addons/account_payment_interco/i18n/ro.po`
- `addons/account_payment_interco/i18n/ru.po`
- `addons/account_payment_interco/i18n/sk.po`
- `addons/account_payment_interco/i18n/sl.po`
- `addons/account_payment_interco/i18n/sr@latin.po`
- `addons/account_payment_interco/i18n/sv.po`
- `addons/account_payment_interco/i18n/th.po`
- `addons/account_payment_interco/i18n/tr.po`
- `addons/account_payment_interco/i18n/uk.po`
- `addons/account_payment_interco/i18n/uz.po`
- `addons/account_payment_interco/i18n/vi.po`
- `addons/account_payment_interco/i18n/zh_CN.po`
- `addons/account_payment_interco/i18n/zh_TW.po`
- `addons/account_payment_interco/models/__init__.py`
- `addons/account_payment_interco/models/account_move.py`
- `addons/account_payment_interco/models/res_company.py`
- `addons/account_payment_interco/models/res_config_settings.py`
- `addons/account_payment_interco/tests/__init__.py`
- `addons/account_payment_interco/tests/test_interco_clearing.py`
- `addons/account_payment_interco/views/res_config_settings_views.xml`
