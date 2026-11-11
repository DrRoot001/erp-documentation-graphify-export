# Module: l10n_pe

- **Module ID:** MOD-290
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_pe`
- **Manifest:** `addons/l10n_pe/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 39 files, including 20 Python, 7 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_latam_invoice_document`, `account_debit_note`, `account`.

## 2. Module structure

- Model/business logic files: 9
- Controller/API files: 2
- XML/data/view/template files: 7
- Browser asset files: 1
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_pe/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 9 model declarations, 22 methods, 0 constraint handlers, 3 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/l10n_pe/demo/account_demo.py:6`, `addons/l10n_pe/models/res_partner.py:15`, `addons/l10n_pe/models/template_pe.py:6`, `addons/l10n_pe/models/res_city_district.py:5`, `addons/l10n_pe/models/account_tax.py:5`, `addons/l10n_pe/models/res_city.py:5`, `addons/l10n_pe/models/res_country.py:6`, `addons/l10n_pe/models/account_move.py:12`, `addons/l10n_pe/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/l10n_pe/controllers/portal.py:27`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 1 JavaScript/TypeScript files; static XML analysis found 68 record/template/menu identifiers.
- **Evidence:** `addons/l10n_pe/demo/demo_company.xml:3`, `addons/l10n_pe/demo/demo_company.xml:16`, `addons/l10n_pe/demo/demo_partner.xml:2`, `addons/l10n_pe/data/res_country_data.xml:3`, `addons/l10n_pe/data/res_country_data.xml:42`, `addons/l10n_pe/data/l10n_latam_document_type_data.xml:3`, `addons/l10n_pe/data/l10n_latam_document_type_data.xml:14`, `addons/l10n_pe/data/l10n_latam_document_type_data.xml:25`, `addons/l10n_pe/data/l10n_latam_document_type_data.xml:36`, `addons/l10n_pe/data/l10n_latam_document_type_data.xml:47`, `addons/l10n_pe/data/l10n_latam_document_type_data.xml:58`, `addons/l10n_pe/data/l10n_latam_document_type_data.xml:69`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_pe/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_pe/data/l10n_latam_document_type_data.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_pe/tests/test_l10n_latam_doc_types.py`, `addons/l10n_pe/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `base.partner_demo_company_pe`, `base.demo_company_pe`, `l10n_pe_partner_1`, `pe_partner_address_form`, `base.pe`, `document_type01`, `document_type03`, `document_type02`, `document_type04`, `document_type05`, `document_type06`, `document_type07`, `document_type07b`, `document_type08`, `document_type08b`, `document_type10`, `document_type11`, `document_type12`, `document_type13`, `document_type14`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/l10n_pe/views/portal_address_templates.xml:4`
- View/action field declarations: 6; representative evidence: `addons/l10n_pe/data/res_country_data.xml:5`, `addons/l10n_pe/data/res_country_data.xml:7`, `addons/l10n_pe/views/res_city_view.xml:6`, `addons/l10n_pe/views/res_city_view.xml:8`, `addons/l10n_pe/views/account_tax_view.xml:5`, `addons/l10n_pe/views/account_tax_view.xml:8`
- Browser assets: 1; representative files: `addons/l10n_pe/static/src/interactions/address.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_pe/__manifest__.py`
- **HTTP entry points:** `addons/l10n_pe/controllers/portal.py:27`
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/l10n_pe/data/l10n_latam_document_type_data.xml`

## 7. Database interactions

- Model declarations: 9
- Representative model evidence: inherits `account.chart.template` (addons/l10n_pe/demo/account_demo.py:6); inherits `res.partner` (addons/l10n_pe/models/res_partner.py:15); inherits `account.chart.template` (addons/l10n_pe/models/template_pe.py:6); `l10n_pe.res.city.district` (addons/l10n_pe/models/res_city_district.py:5); inherits `account.tax` (addons/l10n_pe/models/account_tax.py:5); inherits `res.city` (addons/l10n_pe/models/res_city.py:5); inherits `res.country` (addons/l10n_pe/models/res_country.py:6); inherits `account.move` (addons/l10n_pe/models/account_move.py:12); inherits `res.company` (addons/l10n_pe/models/res_company.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/l10n_pe/controllers/portal.py:27`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_latam_invoice_document`, `account_debit_note`, `account`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_pe/README.rst`
- `addons/l10n_pe/__init__.py`
- `addons/l10n_pe/__manifest__.py`
- `addons/l10n_pe/controllers/__init__.py`
- `addons/l10n_pe/controllers/portal.py`
- `addons/l10n_pe/data/l10n_latam_document_type_data.xml`
- `addons/l10n_pe/data/l10n_pe.res.city.district.csv`
- `addons/l10n_pe/data/res.city.csv`
- `addons/l10n_pe/data/res_country_data.xml`
- `addons/l10n_pe/data/template/account.account-pe.csv`
- `addons/l10n_pe/data/template/account.asset-pe.csv`
- `addons/l10n_pe/data/template/account.fiscal.position-pe.csv`
- `addons/l10n_pe/data/template/account.tax-pe.csv`
- `addons/l10n_pe/data/template/account.tax.group-pe.csv`
- `addons/l10n_pe/demo/__init__.py`
- `addons/l10n_pe/demo/account_demo.py`
- `addons/l10n_pe/demo/demo_company.xml`
- `addons/l10n_pe/demo/demo_partner.xml`
- `addons/l10n_pe/i18n/es_419.po`
- `addons/l10n_pe/i18n/l10n_pe.pot`
- `addons/l10n_pe/migrations/3.1/end-migrate_upgrade_taxes.py`
- `addons/l10n_pe/models/__init__.py`
- `addons/l10n_pe/models/account_move.py`
- `addons/l10n_pe/models/account_tax.py`
- `addons/l10n_pe/models/res_city.py`
- `addons/l10n_pe/models/res_city_district.py`
- `addons/l10n_pe/models/res_company.py`
- `addons/l10n_pe/models/res_country.py`
- `addons/l10n_pe/models/res_partner.py`
- `addons/l10n_pe/models/template_pe.py`
- `addons/l10n_pe/security/ir.access.csv`
- `addons/l10n_pe/static/src/interactions/address.js`
- `addons/l10n_pe/tests/__init__.py`
- `addons/l10n_pe/tests/test_l10n_latam_doc_types.py`
- `addons/l10n_pe/tools/__init__.py`
- `addons/l10n_pe/tools/partner_identifiers.py`
- `addons/l10n_pe/views/account_tax_view.xml`
- `addons/l10n_pe/views/portal_address_templates.xml`
- `addons/l10n_pe/views/res_city_view.xml`
