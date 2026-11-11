# Module: website_mass_mailing_sms

- **Module ID:** MOD-628
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_mass_mailing_sms`
- **Manifest:** `addons/website_mass_mailing_sms/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Attract visitors to subscribe to mailing lists

**Manifest description:**

This module adds a new template to the Newsletter Block to allow
your visitors to subscribe with their phone number.

**Scope evidence:** The module contains 59 files, including 6 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `website_mass_mailing`, `mass_mailing_sms`.

## 2. Module structure

- Model/business logic files: 0
- Controller/API files: 2
- XML/data/view/template files: 3
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

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/website_mass_mailing_sms/controllers/main.py`, `addons/website_mass_mailing_sms/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 4 record/template/menu identifiers.
- **Evidence:** `addons/website_mass_mailing_sms/views/snippets/snippets_templates.xml:4`, `addons/website_mass_mailing_sms/views/snippets/snippets_templates.xml:12`, `addons/website_mass_mailing_sms/views/snippets/snippets_templates.xml:23`, `addons/website_mass_mailing_sms/views/snippets/snippets_templates.xml:34`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/website_mass_mailing_sms/tests/test_website_mass_mailing_sms.py`, `addons/website_mass_mailing_sms/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `snippets`, `s_newsletter_subscribe_form`, `s_newsletter_block_sms_template`, `SMS Notifications`
- Menus: 0; representative evidence: Not found in module
- Templates: 4; representative evidence: `addons/website_mass_mailing_sms/views/snippets/snippets_templates.xml:4`, `addons/website_mass_mailing_sms/views/snippets/snippets_templates.xml:12`, `addons/website_mass_mailing_sms/views/snippets/snippets_templates.xml:23`, `addons/website_mass_mailing_sms/views/snippets/snippets_templates.xml:34`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_mass_mailing_sms/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_mass_mailing`, `mass_mailing_sms`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Not found
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/website_mass_mailing_sms/__init__.py`
- `addons/website_mass_mailing_sms/__manifest__.py`
- `addons/website_mass_mailing_sms/controllers/__init__.py`
- `addons/website_mass_mailing_sms/controllers/main.py`
- `addons/website_mass_mailing_sms/data/ir_model_data.xml`
- `addons/website_mass_mailing_sms/i18n/ar.po`
- `addons/website_mass_mailing_sms/i18n/az.po`
- `addons/website_mass_mailing_sms/i18n/bg.po`
- `addons/website_mass_mailing_sms/i18n/bs.po`
- `addons/website_mass_mailing_sms/i18n/ca.po`
- `addons/website_mass_mailing_sms/i18n/cs.po`
- `addons/website_mass_mailing_sms/i18n/da.po`
- `addons/website_mass_mailing_sms/i18n/de.po`
- `addons/website_mass_mailing_sms/i18n/el.po`
- `addons/website_mass_mailing_sms/i18n/es.po`
- `addons/website_mass_mailing_sms/i18n/es_419.po`
- `addons/website_mass_mailing_sms/i18n/et.po`
- `addons/website_mass_mailing_sms/i18n/fa.po`
- `addons/website_mass_mailing_sms/i18n/fi.po`
- `addons/website_mass_mailing_sms/i18n/fr.po`
- `addons/website_mass_mailing_sms/i18n/he.po`
- `addons/website_mass_mailing_sms/i18n/hi.po`
- `addons/website_mass_mailing_sms/i18n/hr.po`
- `addons/website_mass_mailing_sms/i18n/hu.po`
- `addons/website_mass_mailing_sms/i18n/id.po`
- `addons/website_mass_mailing_sms/i18n/it.po`
- `addons/website_mass_mailing_sms/i18n/ja.po`
- `addons/website_mass_mailing_sms/i18n/kab.po`
- `addons/website_mass_mailing_sms/i18n/ko.po`
- `addons/website_mass_mailing_sms/i18n/ku.po`
- `addons/website_mass_mailing_sms/i18n/lo.po`
- `addons/website_mass_mailing_sms/i18n/lt.po`
- `addons/website_mass_mailing_sms/i18n/lv.po`
- `addons/website_mass_mailing_sms/i18n/mn.po`
- `addons/website_mass_mailing_sms/i18n/my.po`
- `addons/website_mass_mailing_sms/i18n/nb.po`
- `addons/website_mass_mailing_sms/i18n/nl.po`
- `addons/website_mass_mailing_sms/i18n/pl.po`
- `addons/website_mass_mailing_sms/i18n/pt.po`
- `addons/website_mass_mailing_sms/i18n/pt_BR.po`
- `addons/website_mass_mailing_sms/i18n/ro.po`
- `addons/website_mass_mailing_sms/i18n/ru.po`
- `addons/website_mass_mailing_sms/i18n/sk.po`
- `addons/website_mass_mailing_sms/i18n/sl.po`
- `addons/website_mass_mailing_sms/i18n/sr@latin.po`
- `addons/website_mass_mailing_sms/i18n/sv.po`
- `addons/website_mass_mailing_sms/i18n/th.po`
- `addons/website_mass_mailing_sms/i18n/tr.po`
- `addons/website_mass_mailing_sms/i18n/uk.po`
- `addons/website_mass_mailing_sms/i18n/uz.po`
- `addons/website_mass_mailing_sms/i18n/vi.po`
- `addons/website_mass_mailing_sms/i18n/website_mass_mailing_sms.pot`
- `addons/website_mass_mailing_sms/i18n/zh_CN.po`
- `addons/website_mass_mailing_sms/i18n/zh_TW.po`
- `addons/website_mass_mailing_sms/static/shapes/s_newsletter_sms_notifications.svg`
- `addons/website_mass_mailing_sms/static/src/website_builder/newsletter_layout_option.xml`
- `addons/website_mass_mailing_sms/tests/__init__.py`
- `addons/website_mass_mailing_sms/tests/test_website_mass_mailing_sms.py`
- `addons/website_mass_mailing_sms/views/snippets/snippets_templates.xml`
