# Module: pos_partner_autocomplete

- **Module ID:** MOD-442
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_partner_autocomplete`
- **Manifest:** `addons/pos_partner_autocomplete/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Link module between Partner Autocomplete and Point of Sale

**Manifest description:**

This module links Partner Autocomplete with the Point of Sale, allowing partner data to be auto-completed from the POS frontend.
This module ensures that the Point of Sale remains independent of Partner Autocomplete.

**Scope evidence:** The module contains 51 files, including 2 Python, 0 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `partner_autocomplete`, `point_of_sale`.

## 2. Module structure

- Model/business logic files: 0
- Controller/API files: 0
- XML/data/view/template files: 0
- Browser asset files: 0
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

No functional artifact beyond the manifest was found. **Status:** Manifest only / requires verification.

## 5. Screens and user interface

- XML files: 0; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_partner_autocomplete/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `partner_autocomplete`, `point_of_sale`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** No
- **Backend/model evidence:** Not found
- **UI/data evidence:** Not found
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/pos_partner_autocomplete/__init__.py`
- `addons/pos_partner_autocomplete/__manifest__.py`
- `addons/pos_partner_autocomplete/i18n/ar.po`
- `addons/pos_partner_autocomplete/i18n/az.po`
- `addons/pos_partner_autocomplete/i18n/bg.po`
- `addons/pos_partner_autocomplete/i18n/bs.po`
- `addons/pos_partner_autocomplete/i18n/ca.po`
- `addons/pos_partner_autocomplete/i18n/cs.po`
- `addons/pos_partner_autocomplete/i18n/da.po`
- `addons/pos_partner_autocomplete/i18n/de.po`
- `addons/pos_partner_autocomplete/i18n/el.po`
- `addons/pos_partner_autocomplete/i18n/es.po`
- `addons/pos_partner_autocomplete/i18n/es_419.po`
- `addons/pos_partner_autocomplete/i18n/et.po`
- `addons/pos_partner_autocomplete/i18n/fa.po`
- `addons/pos_partner_autocomplete/i18n/fi.po`
- `addons/pos_partner_autocomplete/i18n/fr.po`
- `addons/pos_partner_autocomplete/i18n/he.po`
- `addons/pos_partner_autocomplete/i18n/hi.po`
- `addons/pos_partner_autocomplete/i18n/hr.po`
- `addons/pos_partner_autocomplete/i18n/hu.po`
- `addons/pos_partner_autocomplete/i18n/id.po`
- `addons/pos_partner_autocomplete/i18n/it.po`
- `addons/pos_partner_autocomplete/i18n/ja.po`
- `addons/pos_partner_autocomplete/i18n/kab.po`
- `addons/pos_partner_autocomplete/i18n/ko.po`
- `addons/pos_partner_autocomplete/i18n/ku.po`
- `addons/pos_partner_autocomplete/i18n/lo.po`
- `addons/pos_partner_autocomplete/i18n/lt.po`
- `addons/pos_partner_autocomplete/i18n/lv.po`
- `addons/pos_partner_autocomplete/i18n/mn.po`
- `addons/pos_partner_autocomplete/i18n/my.po`
- `addons/pos_partner_autocomplete/i18n/nb.po`
- `addons/pos_partner_autocomplete/i18n/nl.po`
- `addons/pos_partner_autocomplete/i18n/pl.po`
- `addons/pos_partner_autocomplete/i18n/pos_partner_autocomplete.pot`
- `addons/pos_partner_autocomplete/i18n/pt.po`
- `addons/pos_partner_autocomplete/i18n/pt_BR.po`
- `addons/pos_partner_autocomplete/i18n/ro.po`
- `addons/pos_partner_autocomplete/i18n/ru.po`
- `addons/pos_partner_autocomplete/i18n/sk.po`
- `addons/pos_partner_autocomplete/i18n/sl.po`
- `addons/pos_partner_autocomplete/i18n/sr@latin.po`
- `addons/pos_partner_autocomplete/i18n/sv.po`
- `addons/pos_partner_autocomplete/i18n/th.po`
- `addons/pos_partner_autocomplete/i18n/tr.po`
- `addons/pos_partner_autocomplete/i18n/uk.po`
- `addons/pos_partner_autocomplete/i18n/uz.po`
- `addons/pos_partner_autocomplete/i18n/vi.po`
- `addons/pos_partner_autocomplete/i18n/zh_CN.po`
- `addons/pos_partner_autocomplete/i18n/zh_TW.po`
