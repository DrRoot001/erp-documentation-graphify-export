# Module: website_mass_mailing_event

- **Module ID:** MOD-627
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_mass_mailing_event`
- **Manifest:** `addons/website_mass_mailing_event/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Email Marketing/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Add pre-filled snippets in mass_mailing with an event snapshot

**Manifest description:**

Add pre-filled event snippets for the mass_mailing html builder, with links to the matching website event page.
    The snippet is linked to specified events and will load a snapshot of their data to be sent by email.

**Scope evidence:** The module contains 55 files, including 2 Python, 3 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `mass_mailing`, `website_event`.

## 2. Module structure

- Model/business logic files: 0
- Controller/API files: 0
- XML/data/view/template files: 3
- Browser asset files: 1
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### User interface and data

- **Description:** 3 XML files and 1 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 1; representative files: `addons/website_mass_mailing_event/static/src/builder/options/event_snapshot_snippet_info.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_mass_mailing_event/__manifest__.py`
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

- Declared dependencies: `mass_mailing`, `website_event`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Not found
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/website_mass_mailing_event/__init__.py`
- `addons/website_mass_mailing_event/__manifest__.py`
- `addons/website_mass_mailing_event/i18n/ar.po`
- `addons/website_mass_mailing_event/i18n/az.po`
- `addons/website_mass_mailing_event/i18n/bg.po`
- `addons/website_mass_mailing_event/i18n/bs.po`
- `addons/website_mass_mailing_event/i18n/ca.po`
- `addons/website_mass_mailing_event/i18n/cs.po`
- `addons/website_mass_mailing_event/i18n/da.po`
- `addons/website_mass_mailing_event/i18n/de.po`
- `addons/website_mass_mailing_event/i18n/el.po`
- `addons/website_mass_mailing_event/i18n/es.po`
- `addons/website_mass_mailing_event/i18n/es_419.po`
- `addons/website_mass_mailing_event/i18n/et.po`
- `addons/website_mass_mailing_event/i18n/fa.po`
- `addons/website_mass_mailing_event/i18n/fi.po`
- `addons/website_mass_mailing_event/i18n/fr.po`
- `addons/website_mass_mailing_event/i18n/he.po`
- `addons/website_mass_mailing_event/i18n/hi.po`
- `addons/website_mass_mailing_event/i18n/hr.po`
- `addons/website_mass_mailing_event/i18n/hu.po`
- `addons/website_mass_mailing_event/i18n/id.po`
- `addons/website_mass_mailing_event/i18n/it.po`
- `addons/website_mass_mailing_event/i18n/ja.po`
- `addons/website_mass_mailing_event/i18n/kab.po`
- `addons/website_mass_mailing_event/i18n/ko.po`
- `addons/website_mass_mailing_event/i18n/ku.po`
- `addons/website_mass_mailing_event/i18n/lo.po`
- `addons/website_mass_mailing_event/i18n/lt.po`
- `addons/website_mass_mailing_event/i18n/lv.po`
- `addons/website_mass_mailing_event/i18n/mn.po`
- `addons/website_mass_mailing_event/i18n/my.po`
- `addons/website_mass_mailing_event/i18n/nb.po`
- `addons/website_mass_mailing_event/i18n/nl.po`
- `addons/website_mass_mailing_event/i18n/pl.po`
- `addons/website_mass_mailing_event/i18n/pt.po`
- `addons/website_mass_mailing_event/i18n/pt_BR.po`
- `addons/website_mass_mailing_event/i18n/ro.po`
- `addons/website_mass_mailing_event/i18n/ru.po`
- `addons/website_mass_mailing_event/i18n/sk.po`
- `addons/website_mass_mailing_event/i18n/sl.po`
- `addons/website_mass_mailing_event/i18n/sr@latin.po`
- `addons/website_mass_mailing_event/i18n/sv.po`
- `addons/website_mass_mailing_event/i18n/th.po`
- `addons/website_mass_mailing_event/i18n/tr.po`
- `addons/website_mass_mailing_event/i18n/uk.po`
- `addons/website_mass_mailing_event/i18n/uz.po`
- `addons/website_mass_mailing_event/i18n/vi.po`
- `addons/website_mass_mailing_event/i18n/website_mass_mailing_event.pot`
- `addons/website_mass_mailing_event/i18n/zh_CN.po`
- `addons/website_mass_mailing_event/i18n/zh_TW.po`
- `addons/website_mass_mailing_event/static/src/builder/options/event_snapshot_fragments.xml`
- `addons/website_mass_mailing_event/static/src/builder/options/event_snapshot_snippet_info.js`
- `addons/website_mass_mailing_event/static/src/snippets/s_event_snapshot.xml`
- `addons/website_mass_mailing_event/static/src/snippets/snippet_categories.xml`
