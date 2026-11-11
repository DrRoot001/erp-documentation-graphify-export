# Module: l10n_eu_account_vies

- **Module ID:** MOD-185
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_eu_account_vies`
- **Manifest:** `addons/l10n_eu_account_vies/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

VAT validation for Partner's VAT numbers.
=========================================

After installing this module, values entered in the VAT field of Partners will
be validated using VIES for all supported countries. The country is inferred from the
2-letter country code that prefixes the VAT number, e.g. ``BE0477472701``
will be validated using the Belgian rules.

    * When the "VAT VIES Check" option is enabled (in the configuration of the user's
      Company), VAT numbers will be submitted to the online EU VIES database,
      which will truly verify that the number is valid and currently
      allocated to a EU company. This is a little bit slower than the simple
      off-line check, requires an Internet connection, and may not be available
      all the time. If the service is not available or does not support the
      requested country (e.g. for non-EU countries), a simple check will be performed
      instead.

Supported countries currently include EU countries, and a few non-EU countries
such as Chile, Colombia, Mexico, Norway or Russia. For unsupported countries,
only the country code will be validated.

**Scope evidence:** The module contains 35 files, including 10 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 2
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 4
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 29 methods, 0 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/l10n_eu_account_vies/models/res_partner.py:14`, `addons/l10n_eu_account_vies/models/res_country.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/l10n_eu_account_vies/controllers/webhook.py:11`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/l10n_eu_account_vies/data/ir_cron.xml:5`, `addons/l10n_eu_account_vies/views/res_partner_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 4 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_eu_account_vies/__manifest__.py`, `addons/l10n_eu_account_vies/models/res_partner.py`, `addons/l10n_eu_account_vies/data/ir_cron.xml`, `addons/l10n_eu_account_vies/tests/test_vies_iap.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_eu_account_vies/tests/test_vies_iap.py`, `addons/l10n_eu_account_vies/tests/test_vat_numbers.py`, `addons/l10n_eu_account_vies/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `vies_iap_check_update`, `view_partner_l10n_eu_account_vies_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/l10n_eu_account_vies/views/res_partner_views.xml:5`, `addons/l10n_eu_account_vies/views/res_partner_views.xml:9`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_eu_account_vies/__manifest__.py`
- **HTTP entry points:** `addons/l10n_eu_account_vies/controllers/webhook.py:11`
- **Scheduled entry points:** `addons/l10n_eu_account_vies/__manifest__.py`, `addons/l10n_eu_account_vies/models/res_partner.py`, `addons/l10n_eu_account_vies/data/ir_cron.xml`, `addons/l10n_eu_account_vies/tests/test_vies_iap.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `res.partner` (addons/l10n_eu_account_vies/models/res_partner.py:14); inherits `res.country` (addons/l10n_eu_account_vies/models/res_country.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/l10n_eu_account_vies/controllers/webhook.py:11`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_eu_account_vies/__init__.py`
- `addons/l10n_eu_account_vies/__manifest__.py`
- `addons/l10n_eu_account_vies/controllers/__init__.py`
- `addons/l10n_eu_account_vies/controllers/webhook.py`
- `addons/l10n_eu_account_vies/data/ir_cron.xml`
- `addons/l10n_eu_account_vies/data/neutralize.sql`
- `addons/l10n_eu_account_vies/i18n/bg.po`
- `addons/l10n_eu_account_vies/i18n/cs.po`
- `addons/l10n_eu_account_vies/i18n/da.po`
- `addons/l10n_eu_account_vies/i18n/de.po`
- `addons/l10n_eu_account_vies/i18n/el.po`
- `addons/l10n_eu_account_vies/i18n/es.po`
- `addons/l10n_eu_account_vies/i18n/et.po`
- `addons/l10n_eu_account_vies/i18n/fi.po`
- `addons/l10n_eu_account_vies/i18n/fr.po`
- `addons/l10n_eu_account_vies/i18n/hr.po`
- `addons/l10n_eu_account_vies/i18n/hu.po`
- `addons/l10n_eu_account_vies/i18n/it.po`
- `addons/l10n_eu_account_vies/i18n/l10n_eu_account_vies.pot`
- `addons/l10n_eu_account_vies/i18n/lt.po`
- `addons/l10n_eu_account_vies/i18n/lv.po`
- `addons/l10n_eu_account_vies/i18n/nl.po`
- `addons/l10n_eu_account_vies/i18n/pl.po`
- `addons/l10n_eu_account_vies/i18n/pt.po`
- `addons/l10n_eu_account_vies/i18n/ro.po`
- `addons/l10n_eu_account_vies/i18n/sk.po`
- `addons/l10n_eu_account_vies/i18n/sl.po`
- `addons/l10n_eu_account_vies/i18n/sv.po`
- `addons/l10n_eu_account_vies/models/__init__.py`
- `addons/l10n_eu_account_vies/models/res_country.py`
- `addons/l10n_eu_account_vies/models/res_partner.py`
- `addons/l10n_eu_account_vies/tests/__init__.py`
- `addons/l10n_eu_account_vies/tests/test_vat_numbers.py`
- `addons/l10n_eu_account_vies/tests/test_vies_iap.py`
- `addons/l10n_eu_account_vies/views/res_partner_views.xml`
