# Module: spreadsheet_account

- **Module ID:** MOD-545
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/spreadsheet_account`
- **Manifest:** `addons/spreadsheet_account/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Spreadsheet Accounting formulas

**Manifest description:**

Spreadsheet Accounting formulas

**Scope evidence:** The module contains 78 files, including 12 Python, 0 XML, and 17 JavaScript/TypeScript files. The manifest declares dependencies: `spreadsheet`, `account`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 0
- Browser asset files: 17
- Security files: 0
- Test files: 7
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 68 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/spreadsheet_account/models/account.py:13`, `addons/spreadsheet_account/models/res_company.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 0 XML files and 17 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 7 test files are present.
- **Evidence:** `addons/spreadsheet_account/tests/test_partner_balance.py`, `addons/spreadsheet_account/tests/test_debit_credit.py`, `addons/spreadsheet_account/tests/test_residual_amount.py`, `addons/spreadsheet_account/tests/test_balance_tag.py`, `addons/spreadsheet_account/tests/__init__.py`, `addons/spreadsheet_account/tests/test_company_fiscal_year.py`, `addons/spreadsheet_account/tests/test_account_group.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 0; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 17; representative files: `addons/spreadsheet_account/static/src/accounting_functions.js`, `addons/spreadsheet_account/static/src/index.js`, `addons/spreadsheet_account/static/src/utils.js`, `addons/spreadsheet_account/static/src/fiscal_year_global_filter.js`, `addons/spreadsheet_account/static/src/account_group_auto_complete.js`, `addons/spreadsheet_account/static/tests/mock_server.js`, `addons/spreadsheet_account/static/tests/accounting_test_data.js`, `addons/spreadsheet_account/static/src/plugins/accounting_plugin.js`, `addons/spreadsheet_account/static/tests/ui/accounting_drilldown.test.js`, `addons/spreadsheet_account/static/tests/model/residual_amount.test.js`, `addons/spreadsheet_account/static/tests/model/fiscal_year.test.js`, `addons/spreadsheet_account/static/tests/model/account_groups.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/spreadsheet_account/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `account.account` (addons/spreadsheet_account/models/account.py:13); inherits `res.company` (addons/spreadsheet_account/models/res_company.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `spreadsheet`, `account`
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

- `addons/spreadsheet_account/__init__.py`
- `addons/spreadsheet_account/__manifest__.py`
- `addons/spreadsheet_account/i18n/ar.po`
- `addons/spreadsheet_account/i18n/az.po`
- `addons/spreadsheet_account/i18n/bg.po`
- `addons/spreadsheet_account/i18n/bs.po`
- `addons/spreadsheet_account/i18n/ca.po`
- `addons/spreadsheet_account/i18n/cs.po`
- `addons/spreadsheet_account/i18n/da.po`
- `addons/spreadsheet_account/i18n/de.po`
- `addons/spreadsheet_account/i18n/el.po`
- `addons/spreadsheet_account/i18n/es.po`
- `addons/spreadsheet_account/i18n/es_419.po`
- `addons/spreadsheet_account/i18n/et.po`
- `addons/spreadsheet_account/i18n/fa.po`
- `addons/spreadsheet_account/i18n/fi.po`
- `addons/spreadsheet_account/i18n/fr.po`
- `addons/spreadsheet_account/i18n/he.po`
- `addons/spreadsheet_account/i18n/hi.po`
- `addons/spreadsheet_account/i18n/hr.po`
- `addons/spreadsheet_account/i18n/hu.po`
- `addons/spreadsheet_account/i18n/id.po`
- `addons/spreadsheet_account/i18n/it.po`
- `addons/spreadsheet_account/i18n/ja.po`
- `addons/spreadsheet_account/i18n/kab.po`
- `addons/spreadsheet_account/i18n/ko.po`
- `addons/spreadsheet_account/i18n/ku.po`
- `addons/spreadsheet_account/i18n/lo.po`
- `addons/spreadsheet_account/i18n/lt.po`
- `addons/spreadsheet_account/i18n/lv.po`
- `addons/spreadsheet_account/i18n/mn.po`
- `addons/spreadsheet_account/i18n/my.po`
- `addons/spreadsheet_account/i18n/nb.po`
- `addons/spreadsheet_account/i18n/nl.po`
- `addons/spreadsheet_account/i18n/pl.po`
- `addons/spreadsheet_account/i18n/pt.po`
- `addons/spreadsheet_account/i18n/pt_BR.po`
- `addons/spreadsheet_account/i18n/ro.po`
- `addons/spreadsheet_account/i18n/ru.po`
- `addons/spreadsheet_account/i18n/sk.po`
- `addons/spreadsheet_account/i18n/sl.po`
- `addons/spreadsheet_account/i18n/spreadsheet_account.pot`
- `addons/spreadsheet_account/i18n/sr@latin.po`
- `addons/spreadsheet_account/i18n/sv.po`
- `addons/spreadsheet_account/i18n/th.po`
- `addons/spreadsheet_account/i18n/tr.po`
- `addons/spreadsheet_account/i18n/uk.po`
- `addons/spreadsheet_account/i18n/uz.po`
- `addons/spreadsheet_account/i18n/vi.po`
- `addons/spreadsheet_account/i18n/zh_CN.po`
- `addons/spreadsheet_account/i18n/zh_TW.po`
- `addons/spreadsheet_account/models/__init__.py`
- `addons/spreadsheet_account/models/account.py`
- `addons/spreadsheet_account/models/res_company.py`
- `addons/spreadsheet_account/static/src/account_group_auto_complete.js`
- `addons/spreadsheet_account/static/src/accounting_functions.js`
- `addons/spreadsheet_account/static/src/fiscal_year_global_filter.js`
- `addons/spreadsheet_account/static/src/index.js`
- `addons/spreadsheet_account/static/src/plugins/accounting_plugin.js`
- `addons/spreadsheet_account/static/src/utils.js`
- `addons/spreadsheet_account/static/tests/accounting_test_data.js`
- `addons/spreadsheet_account/static/tests/mock_server.js`
- `addons/spreadsheet_account/static/tests/model/account_groups.test.js`
- `addons/spreadsheet_account/static/tests/model/account_groups_auto_complete.test.js`
- `addons/spreadsheet_account/static/tests/model/accounting.test.js`
- `addons/spreadsheet_account/static/tests/model/balance_tag.test.js`
- `addons/spreadsheet_account/static/tests/model/fiscal_year.test.js`
- `addons/spreadsheet_account/static/tests/model/fiscal_year_global_filter.test.js`
- `addons/spreadsheet_account/static/tests/model/partner_balance.test.js`
- `addons/spreadsheet_account/static/tests/model/residual_amount.test.js`
- `addons/spreadsheet_account/static/tests/ui/accounting_drilldown.test.js`
- `addons/spreadsheet_account/tests/__init__.py`
- `addons/spreadsheet_account/tests/test_account_group.py`
- `addons/spreadsheet_account/tests/test_balance_tag.py`
- `addons/spreadsheet_account/tests/test_company_fiscal_year.py`
- `addons/spreadsheet_account/tests/test_debit_credit.py`
- `addons/spreadsheet_account/tests/test_partner_balance.py`
- `addons/spreadsheet_account/tests/test_residual_amount.py`
