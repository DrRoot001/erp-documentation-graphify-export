# Module: rpc

- **Module ID:** MOD-508
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/rpc`
- **Manifest:** `addons/rpc/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Extra Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Standard Odoo RPC endpoints to models
=====================================

This module provides the /xmlrpc and /jsonrpc endpoints used to
programmatically access models.

**Scope evidence:** The module contains 57 files, including 8 Python, 0 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `base`.

## 2. Module structure

- Model/business logic files: 0
- Controller/API files: 4
- XML/data/view/template files: 0
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### HTTP/API surface

- **Description:** 4 controller files and 6 route declarations.
- **Evidence:** `addons/rpc/controllers/json2.py:37`, `addons/rpc/controllers/json2.py:48`, `addons/rpc/controllers/xmlrpc.py:139`, `addons/rpc/controllers/xmlrpc.py:158`, `addons/rpc/controllers/__init__.py:24`, `addons/rpc/controllers/jsonrpc.py:12`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/rpc/tests/__init__.py`, `addons/rpc/tests/test_xmlrpc.py`
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

- **Entry point evidence:** `addons/rpc/__manifest__.py`
- **HTTP entry points:** `addons/rpc/controllers/json2.py:37`, `addons/rpc/controllers/json2.py:48`, `addons/rpc/controllers/xmlrpc.py:139`, `addons/rpc/controllers/xmlrpc.py:158`, `addons/rpc/controllers/__init__.py:24`, `addons/rpc/controllers/jsonrpc.py:12`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 4
- Route declarations: 6
- Route evidence: `addons/rpc/controllers/json2.py:37`, `addons/rpc/controllers/json2.py:48`, `addons/rpc/controllers/xmlrpc.py:139`, `addons/rpc/controllers/xmlrpc.py:158`, `addons/rpc/controllers/__init__.py:24`, `addons/rpc/controllers/jsonrpc.py:12`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** No
- **Backend/model evidence:** Not found
- **UI/data evidence:** Not found
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/rpc/__init__.py`
- `addons/rpc/__manifest__.py`
- `addons/rpc/controllers/__init__.py`
- `addons/rpc/controllers/json2.py`
- `addons/rpc/controllers/jsonrpc.py`
- `addons/rpc/controllers/xmlrpc.py`
- `addons/rpc/i18n/ar.po`
- `addons/rpc/i18n/az.po`
- `addons/rpc/i18n/bg.po`
- `addons/rpc/i18n/bs.po`
- `addons/rpc/i18n/ca.po`
- `addons/rpc/i18n/cs.po`
- `addons/rpc/i18n/da.po`
- `addons/rpc/i18n/de.po`
- `addons/rpc/i18n/el.po`
- `addons/rpc/i18n/es.po`
- `addons/rpc/i18n/es_419.po`
- `addons/rpc/i18n/et.po`
- `addons/rpc/i18n/fa.po`
- `addons/rpc/i18n/fi.po`
- `addons/rpc/i18n/fr.po`
- `addons/rpc/i18n/he.po`
- `addons/rpc/i18n/hi.po`
- `addons/rpc/i18n/hr.po`
- `addons/rpc/i18n/hu.po`
- `addons/rpc/i18n/id.po`
- `addons/rpc/i18n/it.po`
- `addons/rpc/i18n/ja.po`
- `addons/rpc/i18n/kab.po`
- `addons/rpc/i18n/ko.po`
- `addons/rpc/i18n/ku.po`
- `addons/rpc/i18n/lo.po`
- `addons/rpc/i18n/lt.po`
- `addons/rpc/i18n/lv.po`
- `addons/rpc/i18n/mn.po`
- `addons/rpc/i18n/my.po`
- `addons/rpc/i18n/nb.po`
- `addons/rpc/i18n/nl.po`
- `addons/rpc/i18n/pl.po`
- `addons/rpc/i18n/pt.po`
- `addons/rpc/i18n/pt_BR.po`
- `addons/rpc/i18n/ro.po`
- `addons/rpc/i18n/rpc.pot`
- `addons/rpc/i18n/ru.po`
- `addons/rpc/i18n/sk.po`
- `addons/rpc/i18n/sl.po`
- `addons/rpc/i18n/sr@latin.po`
- `addons/rpc/i18n/sv.po`
- `addons/rpc/i18n/th.po`
- `addons/rpc/i18n/tr.po`
- `addons/rpc/i18n/uk.po`
- `addons/rpc/i18n/uz.po`
- `addons/rpc/i18n/vi.po`
- `addons/rpc/i18n/zh_CN.po`
- `addons/rpc/i18n/zh_TW.po`
- `addons/rpc/tests/__init__.py`
- `addons/rpc/tests/test_xmlrpc.py`
