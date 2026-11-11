# Module: account_test

- **Module ID:** MOD-015
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/account_test`
- **Manifest:** `addons/account_test/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Asserts on accounting.
======================
With this module you can manually check consistencies and inconsistencies of accounting module from menu Reporting/Accounting/Accounting Tests.

You can write a query in order to create Consistency Test and you will get the result of the test
in PDF format which can be accessed by Menu Reporting -> Accounting Tests, then select the test
and print the report from Print button in header area.

**Scope evidence:** The module contains 72 files, including 6 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 1
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/account_test/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 2 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/account_test/models/accounting_assert_test.py:15`, `addons/account_test/report/report_account_test.py:12`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 15 record/template/menu identifiers.
- **Evidence:** `addons/account_test/report/accounting_assert_test_reports.xml:3`, `addons/account_test/report/report_account_test_templates.xml:3`, `addons/account_test/data/accounting_assert_test_data.xml:4`, `addons/account_test/data/accounting_assert_test_data.xml:21`, `addons/account_test/data/accounting_assert_test_data.xml:49`, `addons/account_test/data/accounting_assert_test_data.xml:67`, `addons/account_test/data/accounting_assert_test_data.xml:83`, `addons/account_test/data/accounting_assert_test_data.xml:98`, `addons/account_test/data/accounting_assert_test_data.xml:115`, `addons/account_test/data/accounting_assert_test_data.xml:127`, `addons/account_test/views/accounting_assert_test_views.xml:4`, `addons/account_test/views/accounting_assert_test_views.xml:16`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/account_test/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/account_test/report/accounting_assert_test_reports.xml`, `addons/account_test/report/report_account_test.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `account_assert_test_report`, `report_accounttest`, `account_test_01`, `account_test_03`, `account_test_04`, `account_test_05`, `account_test_05_2`, `account_test_06`, `account_test_07`, `account_test_08`, `account_assert_tree`, `account_assert_form`, `accounting_assert_test_view_search`, `action_accounting_assert`, `menu_action_license`
- Menus: 1; representative evidence: `addons/account_test/views/accounting_assert_test_views.xml:90`
- Templates: 1; representative evidence: `addons/account_test/report/report_account_test_templates.xml:3`
- View/action field declarations: 9; representative evidence: `addons/account_test/report/accounting_assert_test_reports.xml:5`, `addons/account_test/views/accounting_assert_test_views.xml:6`, `addons/account_test/views/accounting_assert_test_views.xml:7`, `addons/account_test/views/accounting_assert_test_views.xml:18`, `addons/account_test/views/accounting_assert_test_views.xml:19`, `addons/account_test/views/accounting_assert_test_views.xml:67`, `addons/account_test/views/accounting_assert_test_views.xml:68`, `addons/account_test/views/accounting_assert_test_views.xml:80`, `addons/account_test/views/accounting_assert_test_views.xml:81`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/account_test/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/account_test/report/accounting_assert_test_reports.xml`, `addons/account_test/report/report_account_test.py`

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: `accounting.assert.test` (addons/account_test/models/accounting_assert_test.py:15); `report.account_test.report_accounttest` (addons/account_test/report/report_account_test.py:12)
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
- **Security evidence:** Present
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/account_test/__init__.py`
- `addons/account_test/__manifest__.py`
- `addons/account_test/data/accounting_assert_test_data.xml`
- `addons/account_test/i18n/account_test.pot`
- `addons/account_test/i18n/af.po`
- `addons/account_test/i18n/am.po`
- `addons/account_test/i18n/ar.po`
- `addons/account_test/i18n/az.po`
- `addons/account_test/i18n/bg.po`
- `addons/account_test/i18n/bs.po`
- `addons/account_test/i18n/ca.po`
- `addons/account_test/i18n/cs.po`
- `addons/account_test/i18n/da.po`
- `addons/account_test/i18n/de.po`
- `addons/account_test/i18n/el.po`
- `addons/account_test/i18n/es.po`
- `addons/account_test/i18n/es_CL.po`
- `addons/account_test/i18n/et.po`
- `addons/account_test/i18n/eu.po`
- `addons/account_test/i18n/fa.po`
- `addons/account_test/i18n/fi.po`
- `addons/account_test/i18n/fo.po`
- `addons/account_test/i18n/fr.po`
- `addons/account_test/i18n/fr_BE.po`
- `addons/account_test/i18n/fr_CA.po`
- `addons/account_test/i18n/gl.po`
- `addons/account_test/i18n/gu.po`
- `addons/account_test/i18n/he.po`
- `addons/account_test/i18n/hr.po`
- `addons/account_test/i18n/hu.po`
- `addons/account_test/i18n/id.po`
- `addons/account_test/i18n/is.po`
- `addons/account_test/i18n/it.po`
- `addons/account_test/i18n/ja.po`
- `addons/account_test/i18n/ka.po`
- `addons/account_test/i18n/kab.po`
- `addons/account_test/i18n/kk.po`
- `addons/account_test/i18n/km.po`
- `addons/account_test/i18n/ko.po`
- `addons/account_test/i18n/lo.po`
- `addons/account_test/i18n/lt.po`
- `addons/account_test/i18n/lv.po`
- `addons/account_test/i18n/mk.po`
- `addons/account_test/i18n/ml_IN.po`
- `addons/account_test/i18n/mn.po`
- `addons/account_test/i18n/nb.po`
- `addons/account_test/i18n/nl.po`
- `addons/account_test/i18n/pl.po`
- `addons/account_test/i18n/pt.po`
- `addons/account_test/i18n/pt_BR.po`
- `addons/account_test/i18n/ro.po`
- `addons/account_test/i18n/ru.po`
- `addons/account_test/i18n/sk.po`
- `addons/account_test/i18n/sl.po`
- `addons/account_test/i18n/sq.po`
- `addons/account_test/i18n/sr@latin.po`
- `addons/account_test/i18n/sv.po`
- `addons/account_test/i18n/ta.po`
- `addons/account_test/i18n/th.po`
- `addons/account_test/i18n/tr.po`
- `addons/account_test/i18n/uk.po`
- `addons/account_test/i18n/vi.po`
- `addons/account_test/i18n/zh_CN.po`
- `addons/account_test/i18n/zh_TW.po`
- `addons/account_test/models/__init__.py`
- `addons/account_test/models/accounting_assert_test.py`
- `addons/account_test/report/__init__.py`
- `addons/account_test/report/accounting_assert_test_reports.xml`
- `addons/account_test/report/report_account_test.py`
- `addons/account_test/report/report_account_test_templates.xml`
- `addons/account_test/security/ir.access.csv`
- `addons/account_test/views/accounting_assert_test_views.xml`
