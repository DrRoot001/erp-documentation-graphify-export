# Module: l10n_latam_check

- **Module ID:** MOD-259
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_latam_check`
- **Manifest:** `addons/l10n_latam_check/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Checks Management

**Manifest description:**

Own Checks Management
---------------------

Extends 'Check Printing Base' module to manage own checks with more features:

* allow using own checks that are not printed but filled manually by the user
* allow to use deferred or electronic checks
  * printing is disabled
  * check number is set manually by the user
* add an optional "Check Cash-In Date" for post-dated checks (deferred payments)
* add a menu to track own checks

Third Party Checks Management
-----------------------------

Add new "Third party check Management" feature.

There are 2 main Payment Methods additions:

* New Third Party Checks:

  * Payments of this payment method represent the check you get from a customer when getting paid (from an invoice or a manual payment)

* Existing Third Party check.

  * Payments of this payment method are to track moves of the check, for eg:

    * Use a check to pay a vendor
    * Deposit the check on the bank
    * Get the check back from the bank (rejection)
    * Get the check back from the vendor (a rejection or return)
    * Transfer the check from one third party check journal to the other (one shop to another)

  * Those operations can be done with multiple checks at once

**Scope evidence:** The module contains 28 files, including 18 Python, 6 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 10
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 0
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_latam_check/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 10 model declarations, 88 methods, 4 constraint handlers, 4 onchange handlers, and 15 dependency declarations.
- **Evidence:** `addons/l10n_latam_check/models/account_payment_method.py:4`, `addons/l10n_latam_check/models/account_payment.py:6`, `addons/l10n_latam_check/models/l10n_latam_check.py:14`, `addons/l10n_latam_check/models/account_journal.py:4`, `addons/l10n_latam_check/models/account_chart_template.py:5`, `addons/l10n_latam_check/models/account_move.py:5`, `addons/l10n_latam_check/models/account_move_line.py:5`, `addons/l10n_latam_check/wizard/l10n_latam_payment_mass_transfer.py:5`, `addons/l10n_latam_check/wizard/l10n_latam_payment_register_check.py:11`, `addons/l10n_latam_check/wizard/account_payment_register.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 0 JavaScript/TypeScript files; static XML analysis found 22 record/template/menu identifiers.
- **Evidence:** `addons/l10n_latam_check/wizard/account_payment_register_views.xml:4`, `addons/l10n_latam_check/wizard/l10n_latam_payment_mass_transfer_views.xml:3`, `addons/l10n_latam_check/wizard/l10n_latam_payment_mass_transfer_views.xml:29`, `addons/l10n_latam_check/data/account_payment_method_data.xml:4`, `addons/l10n_latam_check/data/account_payment_method_data.xml:12`, `addons/l10n_latam_check/data/account_payment_method_data.xml:19`, `addons/l10n_latam_check/data/account_payment_method_data.xml:26`, `addons/l10n_latam_check/data/account_payment_method_data.xml:33`, `addons/l10n_latam_check/views/l10n_latam_check_view.xml:4`, `addons/l10n_latam_check/views/l10n_latam_check_view.xml:37`, `addons/l10n_latam_check/views/l10n_latam_check_view.xml:63`, `addons/l10n_latam_check/views/l10n_latam_check_view.xml:79`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_latam_check/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/l10n_latam_check/tests/test_own_checks.py`, `addons/l10n_latam_check/tests/test_third_party_checks.py`, `addons/l10n_latam_check/tests/common.py`, `addons/l10n_latam_check/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `view_account_payment_register_form`, `view_l10n_latam_payment_mass_transfer_form`, `action_view_l10n_latam_payment_mass_transfer`, `account_payment_method_own_checks`, `account_payment_method_new_third_party_checks`, `account_payment_method_in_third_party_checks`, `account_payment_method_out_third_party_checks`, `account_payment_method_return_third_party_checks`, `view_account_payment_search`, `view_account_payment_third_party_checks_search`, `view_account_third_party_check_operations_tree`, `view_account_check_calendar`, `view_account_check_pivot`, `l10n_latam_check_view_form`, `view_account_own_check_tree`, `action_own_check`, `view_account_third_party_check_tree`, `action_third_party_check`, `menu_own_check`, `menu_third_party_check`
- Menus: 2; representative evidence: `addons/l10n_latam_check/views/l10n_latam_check_view.xml:185`, `addons/l10n_latam_check/views/l10n_latam_check_view.xml:233`
- Templates: 1; representative evidence: `addons/l10n_latam_check/views/report_payment_receipt_templates.xml:2`
- View/action field declarations: 28; representative evidence: `addons/l10n_latam_check/wizard/account_payment_register_views.xml:6`, `addons/l10n_latam_check/wizard/account_payment_register_views.xml:9`, `addons/l10n_latam_check/wizard/l10n_latam_payment_mass_transfer_views.xml:5`, `addons/l10n_latam_check/wizard/l10n_latam_payment_mass_transfer_views.xml:6`, `addons/l10n_latam_check/wizard/l10n_latam_payment_mass_transfer_views.xml:31`, `addons/l10n_latam_check/wizard/l10n_latam_payment_mass_transfer_views.xml:32`, `addons/l10n_latam_check/views/l10n_latam_check_view.xml:6`, `addons/l10n_latam_check/views/l10n_latam_check_view.xml:8`, `addons/l10n_latam_check/views/l10n_latam_check_view.xml:39`, `addons/l10n_latam_check/views/l10n_latam_check_view.xml:42`, `addons/l10n_latam_check/views/l10n_latam_check_view.xml:65`, `addons/l10n_latam_check/views/l10n_latam_check_view.xml:67`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_latam_check/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 10
- Representative model evidence: inherits `account.payment.method` (addons/l10n_latam_check/models/account_payment_method.py:4); inherits `account.payment` (addons/l10n_latam_check/models/account_payment.py:6); `l10n_latam.check` (addons/l10n_latam_check/models/l10n_latam_check.py:14); inherits `account.journal` (addons/l10n_latam_check/models/account_journal.py:4); inherits `account.chart.template` (addons/l10n_latam_check/models/account_chart_template.py:5); inherits `account.move` (addons/l10n_latam_check/models/account_move.py:5); inherits `account.move.line` (addons/l10n_latam_check/models/account_move_line.py:5); `l10n_latam.payment.mass.transfer` (addons/l10n_latam_check/wizard/l10n_latam_payment_mass_transfer.py:5); `l10n_latam.payment.register.check` (addons/l10n_latam_check/wizard/l10n_latam_payment_register_check.py:11); inherits `account.payment.register` (addons/l10n_latam_check/wizard/account_payment_register.py:5)
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

- `addons/l10n_latam_check/__init__.py`
- `addons/l10n_latam_check/__manifest__.py`
- `addons/l10n_latam_check/data/account_payment_method_data.xml`
- `addons/l10n_latam_check/i18n/es_419.po`
- `addons/l10n_latam_check/i18n/l10n_latam_check.pot`
- `addons/l10n_latam_check/i18n/pt_BR.po`
- `addons/l10n_latam_check/models/__init__.py`
- `addons/l10n_latam_check/models/account_chart_template.py`
- `addons/l10n_latam_check/models/account_journal.py`
- `addons/l10n_latam_check/models/account_move.py`
- `addons/l10n_latam_check/models/account_move_line.py`
- `addons/l10n_latam_check/models/account_payment.py`
- `addons/l10n_latam_check/models/account_payment_method.py`
- `addons/l10n_latam_check/models/l10n_latam_check.py`
- `addons/l10n_latam_check/security/ir.access.csv`
- `addons/l10n_latam_check/tests/__init__.py`
- `addons/l10n_latam_check/tests/common.py`
- `addons/l10n_latam_check/tests/test_own_checks.py`
- `addons/l10n_latam_check/tests/test_third_party_checks.py`
- `addons/l10n_latam_check/views/account_payment_view.xml`
- `addons/l10n_latam_check/views/l10n_latam_check_view.xml`
- `addons/l10n_latam_check/views/report_payment_receipt_templates.xml`
- `addons/l10n_latam_check/wizard/__init__.py`
- `addons/l10n_latam_check/wizard/account_payment_register.py`
- `addons/l10n_latam_check/wizard/account_payment_register_views.xml`
- `addons/l10n_latam_check/wizard/l10n_latam_payment_mass_transfer.py`
- `addons/l10n_latam_check/wizard/l10n_latam_payment_mass_transfer_views.xml`
- `addons/l10n_latam_check/wizard/l10n_latam_payment_register_check.py`
