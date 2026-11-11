# Module: l10n_fr_pdp_penalty_rate

- **Module ID:** MOD-195
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_fr_pdp_penalty_rate`
- **Manifest:** `addons/l10n_fr_pdp_penalty_rate/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Adds the mandatory late payment penalty information to French invoices.

**Scope evidence:** The module contains 15 files, including 11 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_fr_pdp`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_fr_pdp_penalty_rate/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 34 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/l10n_fr_pdp_penalty_rate/models/res_config_settings.py:4`, `addons/l10n_fr_pdp_penalty_rate/models/late_payment_penalty_rate.py:13`, `addons/l10n_fr_pdp_penalty_rate/models/account_move.py:5`, `addons/l10n_fr_pdp_penalty_rate/models/account_edi_common.py:4`, `addons/l10n_fr_pdp_penalty_rate/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/l10n_fr_pdp_penalty_rate/views/res_config_settings_views.xml:3`, `addons/l10n_fr_pdp_penalty_rate/views/account_invoice_report_templates.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_fr_pdp_penalty_rate/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_fr_pdp_penalty_rate/tests/test_late_payment_penalties.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_fr_pdp_penalty_rate/tests/test_late_payment_penalties.py`, `addons/l10n_fr_pdp_penalty_rate/tests/test_pdp_notes.py`, `addons/l10n_fr_pdp_penalty_rate/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `res_config_settings_view_form`, `report_invoice_document`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/l10n_fr_pdp_penalty_rate/views/account_invoice_report_templates.xml:3`
- View/action field declarations: 2; representative evidence: `addons/l10n_fr_pdp_penalty_rate/views/res_config_settings_views.xml:5`, `addons/l10n_fr_pdp_penalty_rate/views/res_config_settings_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_fr_pdp_penalty_rate/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/l10n_fr_pdp_penalty_rate/tests/test_late_payment_penalties.py`

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `res.config.settings` (addons/l10n_fr_pdp_penalty_rate/models/res_config_settings.py:4); `l10n_fr_pdp.late.payment.penalty.rate` (addons/l10n_fr_pdp_penalty_rate/models/late_payment_penalty_rate.py:13); inherits `account.move` (addons/l10n_fr_pdp_penalty_rate/models/account_move.py:5); inherits `account.edi.common` (addons/l10n_fr_pdp_penalty_rate/models/account_edi_common.py:4); inherits `res.company` (addons/l10n_fr_pdp_penalty_rate/models/res_company.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_fr_pdp`
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

- `addons/l10n_fr_pdp_penalty_rate/__init__.py`
- `addons/l10n_fr_pdp_penalty_rate/__manifest__.py`
- `addons/l10n_fr_pdp_penalty_rate/i18n/l10n_fr_pdp_penalty_rate.pot`
- `addons/l10n_fr_pdp_penalty_rate/models/__init__.py`
- `addons/l10n_fr_pdp_penalty_rate/models/account_edi_common.py`
- `addons/l10n_fr_pdp_penalty_rate/models/account_move.py`
- `addons/l10n_fr_pdp_penalty_rate/models/late_payment_penalty_rate.py`
- `addons/l10n_fr_pdp_penalty_rate/models/res_company.py`
- `addons/l10n_fr_pdp_penalty_rate/models/res_config_settings.py`
- `addons/l10n_fr_pdp_penalty_rate/security/ir.access.csv`
- `addons/l10n_fr_pdp_penalty_rate/tests/__init__.py`
- `addons/l10n_fr_pdp_penalty_rate/tests/test_late_payment_penalties.py`
- `addons/l10n_fr_pdp_penalty_rate/tests/test_pdp_notes.py`
- `addons/l10n_fr_pdp_penalty_rate/views/account_invoice_report_templates.xml`
- `addons/l10n_fr_pdp_penalty_rate/views/res_config_settings_views.xml`
