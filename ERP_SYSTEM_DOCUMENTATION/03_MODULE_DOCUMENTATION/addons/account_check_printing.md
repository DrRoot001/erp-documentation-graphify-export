# Module: account_check_printing

- **Module ID:** MOD-002
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/account_check_printing`
- **Manifest:** `addons/account_check_printing/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Check printing basic features

**Manifest description:**

This module offers the basic functionalities to make payments by printing checks.
It must be used as a dependency for modules that provide country-specific check templates.
The check settings are located in the accounting journals configuration page.

**Scope evidence:** The module contains 88 files, including 12 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/account_check_printing/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 46 methods, 3 constraint handlers, 0 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/account_check_printing/models/account_payment_method.py:7`, `addons/account_check_printing/models/res_config_settings.py:7`, `addons/account_check_printing/models/account_payment.py:10`, `addons/account_check_printing/models/account_journal.py:10`, `addons/account_check_printing/models/res_company.py:6`, `addons/account_check_printing/wizard/print_prenumbered_checks.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 8 record/template/menu identifiers.
- **Evidence:** `addons/account_check_printing/wizard/print_prenumbered_checks_views.xml:4`, `addons/account_check_printing/data/account_check_printing_data.xml:5`, `addons/account_check_printing/data/account_check_printing_data.xml:11`, `addons/account_check_printing/views/res_config_settings_views.xml:3`, `addons/account_check_printing/views/account_payment_views.xml:3`, `addons/account_check_printing/views/account_payment_views.xml:24`, `addons/account_check_printing/views/account_journal_views.xml:3`, `addons/account_check_printing/views/account_journal_views.xml:23`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/account_check_printing/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/account_check_printing/data/account_check_printing_data.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/account_check_printing/tests/test_print_check.py`, `addons/account_check_printing/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `print_pre_numbered_checks_view`, `account_payment_method_check`, `action_account_print_checks`, `res_config_settings_view_form`, `view_account_payment_form_inherited`, `view_payment_check_printing_search`, `account_journal_dashboard_kanban_view_inherited`, `view_account_journal_form_inherited`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 12; representative evidence: `addons/account_check_printing/wizard/print_prenumbered_checks_views.xml:6`, `addons/account_check_printing/wizard/print_prenumbered_checks_views.xml:7`, `addons/account_check_printing/views/res_config_settings_views.xml:5`, `addons/account_check_printing/views/res_config_settings_views.xml:7`, `addons/account_check_printing/views/account_payment_views.xml:5`, `addons/account_check_printing/views/account_payment_views.xml:7`, `addons/account_check_printing/views/account_payment_views.xml:26`, `addons/account_check_printing/views/account_payment_views.xml:28`, `addons/account_check_printing/views/account_journal_views.xml:5`, `addons/account_check_printing/views/account_journal_views.xml:7`, `addons/account_check_printing/views/account_journal_views.xml:25`, `addons/account_check_printing/views/account_journal_views.xml:27`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/account_check_printing/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/account_check_printing/data/account_check_printing_data.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `account.payment.method` (addons/account_check_printing/models/account_payment_method.py:7); inherits `res.config.settings` (addons/account_check_printing/models/res_config_settings.py:7); inherits `account.payment` (addons/account_check_printing/models/account_payment.py:10); inherits `account.journal` (addons/account_check_printing/models/account_journal.py:10); inherits `res.company` (addons/account_check_printing/models/res_company.py:6); `print.prenumbered.checks` (addons/account_check_printing/wizard/print_prenumbered_checks.py:9)
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
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/account_check_printing/__init__.py`
- `addons/account_check_printing/__manifest__.py`
- `addons/account_check_printing/data/account_check_printing_data.xml`
- `addons/account_check_printing/i18n/account_check_printing.pot`
- `addons/account_check_printing/i18n/af.po`
- `addons/account_check_printing/i18n/am.po`
- `addons/account_check_printing/i18n/ar.po`
- `addons/account_check_printing/i18n/az.po`
- `addons/account_check_printing/i18n/bg.po`
- `addons/account_check_printing/i18n/bs.po`
- `addons/account_check_printing/i18n/ca.po`
- `addons/account_check_printing/i18n/cs.po`
- `addons/account_check_printing/i18n/da.po`
- `addons/account_check_printing/i18n/de.po`
- `addons/account_check_printing/i18n/el.po`
- `addons/account_check_printing/i18n/en_AU.po`
- `addons/account_check_printing/i18n/en_CA.po`
- `addons/account_check_printing/i18n/es.po`
- `addons/account_check_printing/i18n/es_419.po`
- `addons/account_check_printing/i18n/es_CL.po`
- `addons/account_check_printing/i18n/et.po`
- `addons/account_check_printing/i18n/eu.po`
- `addons/account_check_printing/i18n/fa.po`
- `addons/account_check_printing/i18n/fi.po`
- `addons/account_check_printing/i18n/fo.po`
- `addons/account_check_printing/i18n/fr.po`
- `addons/account_check_printing/i18n/fr_BE.po`
- `addons/account_check_printing/i18n/fr_CA.po`
- `addons/account_check_printing/i18n/gl.po`
- `addons/account_check_printing/i18n/gu.po`
- `addons/account_check_printing/i18n/he.po`
- `addons/account_check_printing/i18n/hi.po`
- `addons/account_check_printing/i18n/hr.po`
- `addons/account_check_printing/i18n/hu.po`
- `addons/account_check_printing/i18n/id.po`
- `addons/account_check_printing/i18n/is.po`
- `addons/account_check_printing/i18n/it.po`
- `addons/account_check_printing/i18n/ja.po`
- `addons/account_check_printing/i18n/ka.po`
- `addons/account_check_printing/i18n/kab.po`
- `addons/account_check_printing/i18n/km.po`
- `addons/account_check_printing/i18n/ko.po`
- `addons/account_check_printing/i18n/ku.po`
- `addons/account_check_printing/i18n/lo.po`
- `addons/account_check_printing/i18n/lt.po`
- `addons/account_check_printing/i18n/lv.po`
- `addons/account_check_printing/i18n/mk.po`
- `addons/account_check_printing/i18n/ml_IN.po`
- `addons/account_check_printing/i18n/mn.po`
- `addons/account_check_printing/i18n/my.po`
- `addons/account_check_printing/i18n/nb.po`
- `addons/account_check_printing/i18n/nl.po`
- `addons/account_check_printing/i18n/pl.po`
- `addons/account_check_printing/i18n/pt.po`
- `addons/account_check_printing/i18n/pt_BR.po`
- `addons/account_check_printing/i18n/ro.po`
- `addons/account_check_printing/i18n/ru.po`
- `addons/account_check_printing/i18n/sk.po`
- `addons/account_check_printing/i18n/sl.po`
- `addons/account_check_printing/i18n/sq.po`
- `addons/account_check_printing/i18n/sr@latin.po`
- `addons/account_check_printing/i18n/sv.po`
- `addons/account_check_printing/i18n/ta.po`
- `addons/account_check_printing/i18n/th.po`
- `addons/account_check_printing/i18n/tr.po`
- `addons/account_check_printing/i18n/uk.po`
- `addons/account_check_printing/i18n/uz.po`
- `addons/account_check_printing/i18n/vi.po`
- `addons/account_check_printing/i18n/zh_CN.po`
- `addons/account_check_printing/i18n/zh_TW.po`
- `addons/account_check_printing/models/__init__.py`
- `addons/account_check_printing/models/account_journal.py`
- `addons/account_check_printing/models/account_payment.py`
- `addons/account_check_printing/models/account_payment_method.py`
- `addons/account_check_printing/models/res_company.py`
- `addons/account_check_printing/models/res_config_settings.py`
- `addons/account_check_printing/security/ir.access.csv`
- `addons/account_check_printing/static/description/icon.png`
- `addons/account_check_printing/static/description/icon.svg`
- `addons/account_check_printing/static/description/icon_hi.png`
- `addons/account_check_printing/tests/__init__.py`
- `addons/account_check_printing/tests/test_print_check.py`
- `addons/account_check_printing/views/account_journal_views.xml`
- `addons/account_check_printing/views/account_payment_views.xml`
- `addons/account_check_printing/views/res_config_settings_views.xml`
- `addons/account_check_printing/wizard/__init__.py`
- `addons/account_check_printing/wizard/print_prenumbered_checks.py`
- `addons/account_check_printing/wizard/print_prenumbered_checks_views.xml`
