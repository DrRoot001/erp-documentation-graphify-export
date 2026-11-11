# Module: l10n_eu_oss

- **Module ID:** MOD-186
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_eu_oss`
- **Manifest:** `addons/l10n_eu_oss/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

EU One Stop Shop (OSS) VAT
==========================

From July 1st 2021, EU businesses that are selling goods within the EU above EUR 10 000 to buyers located in another EU Member State need to register and pay VAT in the buyers’ Member State.
Below this new EU-wide threshold you can continue to apply the domestic rules for VAT on your cross-border sales. In order to simplify the application of this EU directive, the One Stop Shop (OSS) registration scheme allows businesses to make a unique tax declaration.

This module makes it possible by helping with the creation of the required EU fiscal positions and taxes in order to automatically apply and record the required taxes.

All you have to do is check that the proposed mapping is suitable for the products and services you sell.

References
++++++++++
Council Directive (EU) 2017/2455 Council Directive (EU) 2019/1995
Council Implementing Regulation (EU) 2019/2026

**Scope evidence:** The module contains 34 files, including 11 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 2
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

- **Description:** 2 model declarations, 21 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/l10n_eu_oss/models/res_config_settings.py:7`, `addons/l10n_eu_oss/models/res_company.py:13`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/l10n_eu_oss/data/account_account_tag.xml:5`, `addons/l10n_eu_oss/data/account_account_tag.xml:19`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_eu_oss/tests/test_oss.py`, `addons/l10n_eu_oss/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `tag_oss`, `tag_eu_import`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_eu_oss/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `res.config.settings` (addons/l10n_eu_oss/models/res_config_settings.py:7); inherits `res.company` (addons/l10n_eu_oss/models/res_company.py:13)
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
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_eu_oss/__init__.py`
- `addons/l10n_eu_oss/__manifest__.py`
- `addons/l10n_eu_oss/data/account_account_tag.xml`
- `addons/l10n_eu_oss/i18n/bg.po`
- `addons/l10n_eu_oss/i18n/cs.po`
- `addons/l10n_eu_oss/i18n/da.po`
- `addons/l10n_eu_oss/i18n/de.po`
- `addons/l10n_eu_oss/i18n/el.po`
- `addons/l10n_eu_oss/i18n/es.po`
- `addons/l10n_eu_oss/i18n/et.po`
- `addons/l10n_eu_oss/i18n/fi.po`
- `addons/l10n_eu_oss/i18n/fr.po`
- `addons/l10n_eu_oss/i18n/hr.po`
- `addons/l10n_eu_oss/i18n/hu.po`
- `addons/l10n_eu_oss/i18n/it.po`
- `addons/l10n_eu_oss/i18n/l10n_eu_oss.pot`
- `addons/l10n_eu_oss/i18n/lt.po`
- `addons/l10n_eu_oss/i18n/lv.po`
- `addons/l10n_eu_oss/i18n/nl.po`
- `addons/l10n_eu_oss/i18n/pl.po`
- `addons/l10n_eu_oss/i18n/pt.po`
- `addons/l10n_eu_oss/i18n/ro.po`
- `addons/l10n_eu_oss/i18n/sk.po`
- `addons/l10n_eu_oss/i18n/sl.po`
- `addons/l10n_eu_oss/i18n/sv.po`
- `addons/l10n_eu_oss/models/__init__.py`
- `addons/l10n_eu_oss/models/eu_account_map.py`
- `addons/l10n_eu_oss/models/eu_field_map.py`
- `addons/l10n_eu_oss/models/eu_tag_map.py`
- `addons/l10n_eu_oss/models/eu_tax_map.py`
- `addons/l10n_eu_oss/models/res_company.py`
- `addons/l10n_eu_oss/models/res_config_settings.py`
- `addons/l10n_eu_oss/tests/__init__.py`
- `addons/l10n_eu_oss/tests/test_oss.py`
