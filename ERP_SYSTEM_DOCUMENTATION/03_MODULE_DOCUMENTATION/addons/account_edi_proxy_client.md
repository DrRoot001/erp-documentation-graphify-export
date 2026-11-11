# Module: account_edi_proxy_client

- **Module ID:** MOD-005
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/account_edi_proxy_client`
- **Manifest:** `addons/account_edi_proxy_client/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module adds generic features to register an Odoo DB on the proxy responsible for receiving data (via requests from web-services).
- An edi_proxy_user has a unique identification on a specific proxy type (e.g. l10n_it_edi, peppol) which
allows to identify him when receiving a document addressed to him. It is linked to a specific company on a specific
Odoo database.
- Encryption features allows to decrypt all the user's data when receiving it from the proxy.
- Authentication offers an additionnal level of security to avoid impersonification, in case someone gains to the user's database.

**Scope evidence:** The module contains 61 files, including 9 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `certificate`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 1
- Browser asset files: 0
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/account_edi_proxy_client/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 18 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/account_edi_proxy_client/models/account_edi_proxy_user.py:26`, `addons/account_edi_proxy_client/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 4 record/template/menu identifiers.
- **Evidence:** `addons/account_edi_proxy_client/views/account_edi_proxy_user_views.xml:4`, `addons/account_edi_proxy_client/views/account_edi_proxy_user_views.xml:27`, `addons/account_edi_proxy_client/views/account_edi_proxy_user_views.xml:43`, `addons/account_edi_proxy_client/views/account_edi_proxy_user_views.xml:50`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/account_edi_proxy_client/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/account_edi_proxy_client/tests/test_neutralize.py`, `addons/account_edi_proxy_client/tests/test_account_edi_proxy_client.py`, `addons/account_edi_proxy_client/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `view_form_account_edi_proxy_client_user`, `view_tree_account_edi_proxy_client_user`, `action_tree_account_edi_proxy_client_user`, `menu_account_proxy_client_user`
- Menus: 1; representative evidence: `addons/account_edi_proxy_client/views/account_edi_proxy_user_views.xml:50`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/account_edi_proxy_client/views/account_edi_proxy_user_views.xml:6`, `addons/account_edi_proxy_client/views/account_edi_proxy_user_views.xml:7`, `addons/account_edi_proxy_client/views/account_edi_proxy_user_views.xml:29`, `addons/account_edi_proxy_client/views/account_edi_proxy_user_views.xml:30`, `addons/account_edi_proxy_client/views/account_edi_proxy_user_views.xml:45`, `addons/account_edi_proxy_client/views/account_edi_proxy_user_views.xml:46`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/account_edi_proxy_client/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: `account_edi_proxy_client.user` (addons/account_edi_proxy_client/models/account_edi_proxy_user.py:26); inherits `res.company` (addons/account_edi_proxy_client/models/res_company.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `certificate`
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

- `addons/account_edi_proxy_client/__init__.py`
- `addons/account_edi_proxy_client/__manifest__.py`
- `addons/account_edi_proxy_client/data/neutralize.sql`
- `addons/account_edi_proxy_client/i18n/account_edi_proxy_client.pot`
- `addons/account_edi_proxy_client/i18n/ar.po`
- `addons/account_edi_proxy_client/i18n/az.po`
- `addons/account_edi_proxy_client/i18n/bg.po`
- `addons/account_edi_proxy_client/i18n/bs.po`
- `addons/account_edi_proxy_client/i18n/ca.po`
- `addons/account_edi_proxy_client/i18n/cs.po`
- `addons/account_edi_proxy_client/i18n/da.po`
- `addons/account_edi_proxy_client/i18n/de.po`
- `addons/account_edi_proxy_client/i18n/el.po`
- `addons/account_edi_proxy_client/i18n/es.po`
- `addons/account_edi_proxy_client/i18n/es_419.po`
- `addons/account_edi_proxy_client/i18n/et.po`
- `addons/account_edi_proxy_client/i18n/fa.po`
- `addons/account_edi_proxy_client/i18n/fi.po`
- `addons/account_edi_proxy_client/i18n/fr.po`
- `addons/account_edi_proxy_client/i18n/he.po`
- `addons/account_edi_proxy_client/i18n/hi.po`
- `addons/account_edi_proxy_client/i18n/hr.po`
- `addons/account_edi_proxy_client/i18n/hu.po`
- `addons/account_edi_proxy_client/i18n/id.po`
- `addons/account_edi_proxy_client/i18n/it.po`
- `addons/account_edi_proxy_client/i18n/ja.po`
- `addons/account_edi_proxy_client/i18n/kab.po`
- `addons/account_edi_proxy_client/i18n/ko.po`
- `addons/account_edi_proxy_client/i18n/ku.po`
- `addons/account_edi_proxy_client/i18n/lo.po`
- `addons/account_edi_proxy_client/i18n/lt.po`
- `addons/account_edi_proxy_client/i18n/lv.po`
- `addons/account_edi_proxy_client/i18n/mn.po`
- `addons/account_edi_proxy_client/i18n/my.po`
- `addons/account_edi_proxy_client/i18n/nb.po`
- `addons/account_edi_proxy_client/i18n/nl.po`
- `addons/account_edi_proxy_client/i18n/pl.po`
- `addons/account_edi_proxy_client/i18n/pt.po`
- `addons/account_edi_proxy_client/i18n/pt_BR.po`
- `addons/account_edi_proxy_client/i18n/ro.po`
- `addons/account_edi_proxy_client/i18n/ru.po`
- `addons/account_edi_proxy_client/i18n/sk.po`
- `addons/account_edi_proxy_client/i18n/sl.po`
- `addons/account_edi_proxy_client/i18n/sr@latin.po`
- `addons/account_edi_proxy_client/i18n/sv.po`
- `addons/account_edi_proxy_client/i18n/th.po`
- `addons/account_edi_proxy_client/i18n/tr.po`
- `addons/account_edi_proxy_client/i18n/uk.po`
- `addons/account_edi_proxy_client/i18n/uz.po`
- `addons/account_edi_proxy_client/i18n/vi.po`
- `addons/account_edi_proxy_client/i18n/zh_CN.po`
- `addons/account_edi_proxy_client/i18n/zh_TW.po`
- `addons/account_edi_proxy_client/models/__init__.py`
- `addons/account_edi_proxy_client/models/account_edi_proxy_auth.py`
- `addons/account_edi_proxy_client/models/account_edi_proxy_user.py`
- `addons/account_edi_proxy_client/models/res_company.py`
- `addons/account_edi_proxy_client/security/ir.access.csv`
- `addons/account_edi_proxy_client/tests/__init__.py`
- `addons/account_edi_proxy_client/tests/test_account_edi_proxy_client.py`
- `addons/account_edi_proxy_client/tests/test_neutralize.py`
- `addons/account_edi_proxy_client/views/account_edi_proxy_user_views.xml`
