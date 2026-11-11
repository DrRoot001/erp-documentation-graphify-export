# Module: l10n_hr_kuna

- **Module ID:** MOD-218
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_hr_kuna`
- **Manifest:** `addons/l10n_hr_kuna/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Croatian localisation.
======================

Author: Goran Kliska, Slobodni programi d.o.o., Zagreb
        https://www.slobodni-programi.hr

Contributions:
  Tomislav Bošnjaković, Storm Computers: tipovi konta
  Ivan Vađić, Slobodni programi: tipovi konta

Description:

Croatian Chart of Accounts (RRIF ver.2012)

RRIF-ov računski plan za poduzetnike za 2012.
Vrste konta
Kontni plan prema RRIF-u, dorađen u smislu kraćenja naziva i dodavanja analitika
Porezne grupe prema poreznoj prijavi
Porezi PDV obrasca
Ostali porezi
Osnovne fiskalne pozicije

Izvori podataka:
 https://www.rrif.hr/dok/preuzimanje/rrif-rp2011.rar
 https://www.rrif.hr/dok/preuzimanje/rrif-rp2012.rar

**Scope evidence:** The module contains 12 files, including 4 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 2
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

- **Description:** 1 model declarations, 2 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_hr_kuna/models/template_hr_kuna.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 143 record/template/menu identifiers.
- **Evidence:** `addons/l10n_hr_kuna/demo/demo_company.xml:3`, `addons/l10n_hr_kuna/demo/demo_company.xml:16`, `addons/l10n_hr_kuna/data/account_tax_report_data.xml:3`, `addons/l10n_hr_kuna/data/account_tax_report_data.xml:10`, `addons/l10n_hr_kuna/data/account_tax_report_data.xml:16`, `addons/l10n_hr_kuna/data/account_tax_report_data.xml:21`, `addons/l10n_hr_kuna/data/account_tax_report_data.xml:25`, `addons/l10n_hr_kuna/data/account_tax_report_data.xml:35`, `addons/l10n_hr_kuna/data/account_tax_report_data.xml:40`, `addons/l10n_hr_kuna/data/account_tax_report_data.xml:44`, `addons/l10n_hr_kuna/data/account_tax_report_data.xml:48`, `addons/l10n_hr_kuna/data/account_tax_report_data.xml:52`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `base.partner_demo_company_hr_kuna`, `base.demo_company_hr_kuna`, `tax_report`, `tax_report_balance`, `account_tax_report_line_ostali_porezi`, `account_tax_report_line_porez`, `account_tax_report_line_porez_formula`, `account_tax_report_line_pdv`, `account_tax_report_line_obrazac_pdv`, `account_tax_report_line_osnovica`, `account_tax_report_line_obracun`, `account_tax_report_line_obracun_isporuke`, `account_tax_report_line_koje`, `account_tax_report_line_koje_tag`, `account_tax_report_line_oslobodene`, `account_tax_report_line_izvozne`, `account_tax_report_line_izvozne_tag`, `account_tax_report_line_isporuke`, `account_tax_report_line_isporuke_tag`, `account_tax_report_line_tuzemne`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_hr_kuna/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `account.chart.template` (addons/l10n_hr_kuna/models/template_hr_kuna.py:6)
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

- `addons/l10n_hr_kuna/__init__.py`
- `addons/l10n_hr_kuna/__manifest__.py`
- `addons/l10n_hr_kuna/data/account_tax_report_data.xml`
- `addons/l10n_hr_kuna/data/template/account.account-hr_kuna.csv`
- `addons/l10n_hr_kuna/data/template/account.fiscal.position-hr_kuna.csv`
- `addons/l10n_hr_kuna/data/template/account.tax-hr_kuna.csv`
- `addons/l10n_hr_kuna/data/template/account.tax.group-hr_kuna.csv`
- `addons/l10n_hr_kuna/demo/demo_company.xml`
- `addons/l10n_hr_kuna/i18n/hr.po`
- `addons/l10n_hr_kuna/i18n/l10n_hr_kuna.pot`
- `addons/l10n_hr_kuna/models/__init__.py`
- `addons/l10n_hr_kuna/models/template_hr_kuna.py`
