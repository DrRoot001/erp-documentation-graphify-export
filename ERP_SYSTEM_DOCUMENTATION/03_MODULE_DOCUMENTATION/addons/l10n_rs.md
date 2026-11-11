# Module: l10n_rs

- **Module ID:** MOD-307
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_rs`
- **Manifest:** `addons/l10n_rs/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the base module of the Serbian localization. It manages chart of accounts and taxes.
This module is based on the official document "Pravilnik o kontnom okviru i sadržini računa u kontnom okviru za privredna društva, zadruge i preduzetnike ("Sl. glasnik RS", br. 89/2020)"
Source: https://www.paragraf.rs/propisi/pravilnik-o-kontnom-okviru-sadrzini-racuna-za-privredna-drustva-zadruge.html

**Scope evidence:** The module contains 16 files, including 5 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 0
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 2 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_rs/models/template_rs.py:6`, `addons/l10n_rs/models/account_move.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 49 record/template/menu identifiers.
- **Evidence:** `addons/l10n_rs/demo/demo_company.xml:3`, `addons/l10n_rs/demo/demo_company.xml:15`, `addons/l10n_rs/demo/demo_company.xml:20`, `addons/l10n_rs/data/account_tax_report_data.xml:3`, `addons/l10n_rs/data/account_tax_report_data.xml:11`, `addons/l10n_rs/data/account_tax_report_data.xml:18`, `addons/l10n_rs/data/account_tax_report_data.xml:23`, `addons/l10n_rs/data/account_tax_report_data.xml:27`, `addons/l10n_rs/data/account_tax_report_data.xml:32`, `addons/l10n_rs/data/account_tax_report_data.xml:39`, `addons/l10n_rs/data/account_tax_report_data.xml:44`, `addons/l10n_rs/data/account_tax_report_data.xml:51`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `base.partner_demo_company_rs`, `base.demo_company_rs`, `base.demo_bank_rs`, `tax_report_vat`, `tax_report_vat_balance`, `tax_report_title_operations`, `tax_report_title_operations_turnover`, `tax_report_line_001`, `tax_report_line_001_tag`, `tax_report_line_002`, `tax_report_line_002_tag`, `tax_report_line_003`, `tax_report_line_003_tag`, `tax_report_line_004`, `tax_report_line_004_tag`, `tax_report_line_005`, `tax_report_line_005_formula`, `tax_report_title_operations_previous_tax`, `tax_report_line_006`, `tax_report_line_006_tag`
- Menus: 1; representative evidence: `addons/l10n_rs/data/menuitem_data.xml:3`
- Templates: 1; representative evidence: `addons/l10n_rs/views/report_invoice.xml:4`
- View/action field declarations: 2; representative evidence: `addons/l10n_rs/views/account_move.xml:6`, `addons/l10n_rs/views/account_move.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_rs/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `account.chart.template` (addons/l10n_rs/models/template_rs.py:6); inherits `account.move` (addons/l10n_rs/models/account_move.py:7)
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
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_rs/__init__.py`
- `addons/l10n_rs/__manifest__.py`
- `addons/l10n_rs/data/account_tax_report_data.xml`
- `addons/l10n_rs/data/menuitem_data.xml`
- `addons/l10n_rs/data/template/account.account-rs.csv`
- `addons/l10n_rs/data/template/account.fiscal.position-rs.csv`
- `addons/l10n_rs/data/template/account.tax-rs.csv`
- `addons/l10n_rs/data/template/account.tax.group-rs.csv`
- `addons/l10n_rs/demo/demo_company.xml`
- `addons/l10n_rs/i18n/l10n_rs.pot`
- `addons/l10n_rs/i18n/sr@latin.po`
- `addons/l10n_rs/models/__init__.py`
- `addons/l10n_rs/models/account_move.py`
- `addons/l10n_rs/models/template_rs.py`
- `addons/l10n_rs/views/account_move.xml`
- `addons/l10n_rs/views/report_invoice.xml`
