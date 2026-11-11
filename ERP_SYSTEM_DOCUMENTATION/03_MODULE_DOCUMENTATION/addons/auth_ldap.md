# Module: auth_ldap

- **Module ID:** MOD-020
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/auth_ldap`
- **Manifest:** `addons/auth_ldap/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 78 files, including 9 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `base_setup`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/auth_ldap/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 26 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/auth_ldap/models/res_config_settings.py:7`, `addons/auth_ldap/models/res_company_ldap.py:40`, `addons/auth_ldap/models/res_users.py:10`, `addons/auth_ldap/models/res_company.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 4 record/template/menu identifiers.
- **Evidence:** `addons/auth_ldap/views/ldap_installer_views.xml:5`, `addons/auth_ldap/views/ldap_installer_views.xml:41`, `addons/auth_ldap/views/ldap_installer_views.xml:54`, `addons/auth_ldap/views/res_config_settings_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/auth_ldap/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/auth_ldap/tests/test_auth_ldap.py`, `addons/auth_ldap/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `view_ldap_installer_form`, `res_company_ldap_view_tree`, `action_ldap_installer`, `res_config_settings_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 8; representative evidence: `addons/auth_ldap/views/ldap_installer_views.xml:7`, `addons/auth_ldap/views/ldap_installer_views.xml:8`, `addons/auth_ldap/views/ldap_installer_views.xml:43`, `addons/auth_ldap/views/ldap_installer_views.xml:44`, `addons/auth_ldap/views/ldap_installer_views.xml:56`, `addons/auth_ldap/views/ldap_installer_views.xml:57`, `addons/auth_ldap/views/res_config_settings_views.xml:5`, `addons/auth_ldap/views/res_config_settings_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/auth_ldap/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `res.config.settings` (addons/auth_ldap/models/res_config_settings.py:7); `res.company.ldap` (addons/auth_ldap/models/res_company_ldap.py:40); inherits `res.users` (addons/auth_ldap/models/res_users.py:10); inherits `res.company` (addons/auth_ldap/models/res_company.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `base_setup`
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

- `addons/auth_ldap/README.rst`
- `addons/auth_ldap/__init__.py`
- `addons/auth_ldap/__manifest__.py`
- `addons/auth_ldap/i18n/af.po`
- `addons/auth_ldap/i18n/am.po`
- `addons/auth_ldap/i18n/ar.po`
- `addons/auth_ldap/i18n/auth_ldap.pot`
- `addons/auth_ldap/i18n/az.po`
- `addons/auth_ldap/i18n/bg.po`
- `addons/auth_ldap/i18n/bs.po`
- `addons/auth_ldap/i18n/ca.po`
- `addons/auth_ldap/i18n/cs.po`
- `addons/auth_ldap/i18n/da.po`
- `addons/auth_ldap/i18n/de.po`
- `addons/auth_ldap/i18n/el.po`
- `addons/auth_ldap/i18n/es.po`
- `addons/auth_ldap/i18n/es_419.po`
- `addons/auth_ldap/i18n/es_CL.po`
- `addons/auth_ldap/i18n/et.po`
- `addons/auth_ldap/i18n/eu.po`
- `addons/auth_ldap/i18n/fa.po`
- `addons/auth_ldap/i18n/fi.po`
- `addons/auth_ldap/i18n/fo.po`
- `addons/auth_ldap/i18n/fr.po`
- `addons/auth_ldap/i18n/fr_BE.po`
- `addons/auth_ldap/i18n/fr_CA.po`
- `addons/auth_ldap/i18n/gl.po`
- `addons/auth_ldap/i18n/gu.po`
- `addons/auth_ldap/i18n/he.po`
- `addons/auth_ldap/i18n/hi.po`
- `addons/auth_ldap/i18n/hr.po`
- `addons/auth_ldap/i18n/hu.po`
- `addons/auth_ldap/i18n/id.po`
- `addons/auth_ldap/i18n/is.po`
- `addons/auth_ldap/i18n/it.po`
- `addons/auth_ldap/i18n/ja.po`
- `addons/auth_ldap/i18n/ka.po`
- `addons/auth_ldap/i18n/kab.po`
- `addons/auth_ldap/i18n/km.po`
- `addons/auth_ldap/i18n/ko.po`
- `addons/auth_ldap/i18n/ku.po`
- `addons/auth_ldap/i18n/lo.po`
- `addons/auth_ldap/i18n/lt.po`
- `addons/auth_ldap/i18n/lv.po`
- `addons/auth_ldap/i18n/mk.po`
- `addons/auth_ldap/i18n/ml_IN.po`
- `addons/auth_ldap/i18n/mn.po`
- `addons/auth_ldap/i18n/my.po`
- `addons/auth_ldap/i18n/nb.po`
- `addons/auth_ldap/i18n/nl.po`
- `addons/auth_ldap/i18n/pl.po`
- `addons/auth_ldap/i18n/pt.po`
- `addons/auth_ldap/i18n/pt_BR.po`
- `addons/auth_ldap/i18n/ro.po`
- `addons/auth_ldap/i18n/ru.po`
- `addons/auth_ldap/i18n/sk.po`
- `addons/auth_ldap/i18n/sl.po`
- `addons/auth_ldap/i18n/sq.po`
- `addons/auth_ldap/i18n/sr@latin.po`
- `addons/auth_ldap/i18n/sv.po`
- `addons/auth_ldap/i18n/ta.po`
- `addons/auth_ldap/i18n/th.po`
- `addons/auth_ldap/i18n/tr.po`
- `addons/auth_ldap/i18n/uk.po`
- `addons/auth_ldap/i18n/uz.po`
- `addons/auth_ldap/i18n/vi.po`
- `addons/auth_ldap/i18n/zh_CN.po`
- `addons/auth_ldap/i18n/zh_TW.po`
- `addons/auth_ldap/models/__init__.py`
- `addons/auth_ldap/models/res_company.py`
- `addons/auth_ldap/models/res_company_ldap.py`
- `addons/auth_ldap/models/res_config_settings.py`
- `addons/auth_ldap/models/res_users.py`
- `addons/auth_ldap/security/ir.access.csv`
- `addons/auth_ldap/tests/__init__.py`
- `addons/auth_ldap/tests/test_auth_ldap.py`
- `addons/auth_ldap/views/ldap_installer_views.xml`
- `addons/auth_ldap/views/res_config_settings_views.xml`
