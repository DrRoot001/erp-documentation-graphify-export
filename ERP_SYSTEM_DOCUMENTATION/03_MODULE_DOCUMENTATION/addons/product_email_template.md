# Module: product_email_template

- **Module ID:** MOD-471
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/product_email_template`
- **Manifest:** `addons/product_email_template/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Add email templates to products to be sent on invoice confirmation
==================================================================

With this module, link your products to a template to send complete information and tools to your customer.
For instance when invoicing a training, the training agenda and materials will automatically be sent to your customers.'

**Scope evidence:** The module contains 68 files, including 7 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 2
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

- **Description:** 2 model declarations, 5 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/product_email_template/models/product.py:6`, `addons/product_email_template/models/account_move.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/product_email_template/views/mail_template_views.xml:3`, `addons/product_email_template/views/product_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/product_email_template/tests/__init__.py`, `addons/product_email_template/tests/test_account_move.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `email_template_form_simplified`, `product_template_form_view`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 5; representative evidence: `addons/product_email_template/views/mail_template_views.xml:5`, `addons/product_email_template/views/mail_template_views.xml:7`, `addons/product_email_template/views/mail_template_views.xml:12`, `addons/product_email_template/views/product_views.xml:5`, `addons/product_email_template/views/product_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/product_email_template/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `product.template` (addons/product_email_template/models/product.py:6); inherits `account.move` (addons/product_email_template/models/account_move.py:6)
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

- `addons/product_email_template/__init__.py`
- `addons/product_email_template/__manifest__.py`
- `addons/product_email_template/i18n/af.po`
- `addons/product_email_template/i18n/ar.po`
- `addons/product_email_template/i18n/az.po`
- `addons/product_email_template/i18n/bg.po`
- `addons/product_email_template/i18n/bs.po`
- `addons/product_email_template/i18n/ca.po`
- `addons/product_email_template/i18n/cs.po`
- `addons/product_email_template/i18n/da.po`
- `addons/product_email_template/i18n/de.po`
- `addons/product_email_template/i18n/el.po`
- `addons/product_email_template/i18n/es.po`
- `addons/product_email_template/i18n/es_419.po`
- `addons/product_email_template/i18n/es_CL.po`
- `addons/product_email_template/i18n/et.po`
- `addons/product_email_template/i18n/eu.po`
- `addons/product_email_template/i18n/fa.po`
- `addons/product_email_template/i18n/fi.po`
- `addons/product_email_template/i18n/fr.po`
- `addons/product_email_template/i18n/gl.po`
- `addons/product_email_template/i18n/gu.po`
- `addons/product_email_template/i18n/he.po`
- `addons/product_email_template/i18n/hi.po`
- `addons/product_email_template/i18n/hr.po`
- `addons/product_email_template/i18n/hu.po`
- `addons/product_email_template/i18n/id.po`
- `addons/product_email_template/i18n/is.po`
- `addons/product_email_template/i18n/it.po`
- `addons/product_email_template/i18n/ja.po`
- `addons/product_email_template/i18n/ka.po`
- `addons/product_email_template/i18n/kab.po`
- `addons/product_email_template/i18n/kk.po`
- `addons/product_email_template/i18n/ko.po`
- `addons/product_email_template/i18n/ku.po`
- `addons/product_email_template/i18n/lo.po`
- `addons/product_email_template/i18n/lt.po`
- `addons/product_email_template/i18n/lv.po`
- `addons/product_email_template/i18n/mk.po`
- `addons/product_email_template/i18n/mn.po`
- `addons/product_email_template/i18n/my.po`
- `addons/product_email_template/i18n/nb.po`
- `addons/product_email_template/i18n/nl.po`
- `addons/product_email_template/i18n/pl.po`
- `addons/product_email_template/i18n/product_email_template.pot`
- `addons/product_email_template/i18n/pt.po`
- `addons/product_email_template/i18n/pt_BR.po`
- `addons/product_email_template/i18n/ro.po`
- `addons/product_email_template/i18n/ru.po`
- `addons/product_email_template/i18n/sk.po`
- `addons/product_email_template/i18n/sl.po`
- `addons/product_email_template/i18n/sr@latin.po`
- `addons/product_email_template/i18n/sv.po`
- `addons/product_email_template/i18n/th.po`
- `addons/product_email_template/i18n/tr.po`
- `addons/product_email_template/i18n/uk.po`
- `addons/product_email_template/i18n/uz.po`
- `addons/product_email_template/i18n/vi.po`
- `addons/product_email_template/i18n/zh_CN.po`
- `addons/product_email_template/i18n/zh_TW.po`
- `addons/product_email_template/models/__init__.py`
- `addons/product_email_template/models/account_move.py`
- `addons/product_email_template/models/product.py`
- `addons/product_email_template/static/img/online_training.png`
- `addons/product_email_template/tests/__init__.py`
- `addons/product_email_template/tests/test_account_move.py`
- `addons/product_email_template/views/mail_template_views.xml`
- `addons/product_email_template/views/product_views.xml`
