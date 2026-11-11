# Module: pos_edi_ubl

- **Module ID:** MOD-429
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_edi_ubl`
- **Manifest:** `addons/pos_edi_ubl/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** UBL in the Point of Sale

**Manifest description:**

This module provides helpers for exporting POS orders in various UBL 2.1 formats.

**Scope evidence:** The module contains 53 files, including 4 Python, 0 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `point_of_sale`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 1
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

### Model and business logic

- **Description:** 1 model declarations, 27 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/pos_edi_ubl/models/pos_edi_ubl_21.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 0; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_edi_ubl/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: `pos.edi.xml.ubl_21` (addons/pos_edi_ubl/models/pos_edi_ubl_21.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `point_of_sale`, `account_edi_ubl_cii`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Not found
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/pos_edi_ubl/__init__.py`
- `addons/pos_edi_ubl/__manifest__.py`
- `addons/pos_edi_ubl/i18n/ar.po`
- `addons/pos_edi_ubl/i18n/az.po`
- `addons/pos_edi_ubl/i18n/bg.po`
- `addons/pos_edi_ubl/i18n/bs.po`
- `addons/pos_edi_ubl/i18n/ca.po`
- `addons/pos_edi_ubl/i18n/cs.po`
- `addons/pos_edi_ubl/i18n/da.po`
- `addons/pos_edi_ubl/i18n/de.po`
- `addons/pos_edi_ubl/i18n/el.po`
- `addons/pos_edi_ubl/i18n/es.po`
- `addons/pos_edi_ubl/i18n/es_419.po`
- `addons/pos_edi_ubl/i18n/et.po`
- `addons/pos_edi_ubl/i18n/fa.po`
- `addons/pos_edi_ubl/i18n/fi.po`
- `addons/pos_edi_ubl/i18n/fr.po`
- `addons/pos_edi_ubl/i18n/he.po`
- `addons/pos_edi_ubl/i18n/hi.po`
- `addons/pos_edi_ubl/i18n/hr.po`
- `addons/pos_edi_ubl/i18n/hu.po`
- `addons/pos_edi_ubl/i18n/id.po`
- `addons/pos_edi_ubl/i18n/it.po`
- `addons/pos_edi_ubl/i18n/ja.po`
- `addons/pos_edi_ubl/i18n/kab.po`
- `addons/pos_edi_ubl/i18n/ko.po`
- `addons/pos_edi_ubl/i18n/ku.po`
- `addons/pos_edi_ubl/i18n/lo.po`
- `addons/pos_edi_ubl/i18n/lt.po`
- `addons/pos_edi_ubl/i18n/lv.po`
- `addons/pos_edi_ubl/i18n/mn.po`
- `addons/pos_edi_ubl/i18n/my.po`
- `addons/pos_edi_ubl/i18n/nb.po`
- `addons/pos_edi_ubl/i18n/nl.po`
- `addons/pos_edi_ubl/i18n/pl.po`
- `addons/pos_edi_ubl/i18n/pos_edi_ubl.pot`
- `addons/pos_edi_ubl/i18n/pt.po`
- `addons/pos_edi_ubl/i18n/pt_BR.po`
- `addons/pos_edi_ubl/i18n/ro.po`
- `addons/pos_edi_ubl/i18n/ru.po`
- `addons/pos_edi_ubl/i18n/sk.po`
- `addons/pos_edi_ubl/i18n/sl.po`
- `addons/pos_edi_ubl/i18n/sr@latin.po`
- `addons/pos_edi_ubl/i18n/sv.po`
- `addons/pos_edi_ubl/i18n/th.po`
- `addons/pos_edi_ubl/i18n/tr.po`
- `addons/pos_edi_ubl/i18n/uk.po`
- `addons/pos_edi_ubl/i18n/uz.po`
- `addons/pos_edi_ubl/i18n/vi.po`
- `addons/pos_edi_ubl/i18n/zh_CN.po`
- `addons/pos_edi_ubl/i18n/zh_TW.po`
- `addons/pos_edi_ubl/models/__init__.py`
- `addons/pos_edi_ubl/models/pos_edi_ubl_21.py`
