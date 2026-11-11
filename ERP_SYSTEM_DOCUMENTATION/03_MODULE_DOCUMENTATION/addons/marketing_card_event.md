# Module: marketing_card_event

- **Module ID:** MOD-361
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/marketing_card_event`
- **Manifest:** `addons/marketing_card_event/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Marketing Card`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Generate dynamic shareable cards for entities linked to events.

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 59 files, including 8 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `marketing_card`, `event`.

## 2. Module structure

- Model/business logic files: 3
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

- **Description:** 3 model declarations, 10 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/marketing_card_event/models/card_campaign.py:4`, `addons/marketing_card_event/models/event_event.py:4`, `addons/marketing_card_event/models/mailing_mailing.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/marketing_card_event/views/mailing_mailing_views.xml:2`, `addons/marketing_card_event/views/event_event_views.xml:2`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/marketing_card_event/tests/test_mailing.py`, `addons/marketing_card_event/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `mailing_mailing_view_form_event_send_card`, `event_event_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/marketing_card_event/views/mailing_mailing_views.xml:6`, `addons/marketing_card_event/views/mailing_mailing_views.xml:8`, `addons/marketing_card_event/views/event_event_views.xml:4`, `addons/marketing_card_event/views/event_event_views.xml:6`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/marketing_card_event/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `card.campaign` (addons/marketing_card_event/models/card_campaign.py:4); inherits `event.event` (addons/marketing_card_event/models/event_event.py:4); inherits `mailing.mailing` (addons/marketing_card_event/models/mailing_mailing.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `marketing_card`, `event`
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

- `addons/marketing_card_event/__init__.py`
- `addons/marketing_card_event/__manifest__.py`
- `addons/marketing_card_event/i18n/ar.po`
- `addons/marketing_card_event/i18n/az.po`
- `addons/marketing_card_event/i18n/bg.po`
- `addons/marketing_card_event/i18n/bs.po`
- `addons/marketing_card_event/i18n/ca.po`
- `addons/marketing_card_event/i18n/cs.po`
- `addons/marketing_card_event/i18n/da.po`
- `addons/marketing_card_event/i18n/de.po`
- `addons/marketing_card_event/i18n/el.po`
- `addons/marketing_card_event/i18n/es.po`
- `addons/marketing_card_event/i18n/es_419.po`
- `addons/marketing_card_event/i18n/et.po`
- `addons/marketing_card_event/i18n/fa.po`
- `addons/marketing_card_event/i18n/fi.po`
- `addons/marketing_card_event/i18n/fr.po`
- `addons/marketing_card_event/i18n/he.po`
- `addons/marketing_card_event/i18n/hi.po`
- `addons/marketing_card_event/i18n/hr.po`
- `addons/marketing_card_event/i18n/hu.po`
- `addons/marketing_card_event/i18n/id.po`
- `addons/marketing_card_event/i18n/it.po`
- `addons/marketing_card_event/i18n/ja.po`
- `addons/marketing_card_event/i18n/kab.po`
- `addons/marketing_card_event/i18n/ko.po`
- `addons/marketing_card_event/i18n/ku.po`
- `addons/marketing_card_event/i18n/lo.po`
- `addons/marketing_card_event/i18n/lt.po`
- `addons/marketing_card_event/i18n/lv.po`
- `addons/marketing_card_event/i18n/marketing_card_event.pot`
- `addons/marketing_card_event/i18n/mn.po`
- `addons/marketing_card_event/i18n/my.po`
- `addons/marketing_card_event/i18n/nb.po`
- `addons/marketing_card_event/i18n/nl.po`
- `addons/marketing_card_event/i18n/pl.po`
- `addons/marketing_card_event/i18n/pt.po`
- `addons/marketing_card_event/i18n/pt_BR.po`
- `addons/marketing_card_event/i18n/ro.po`
- `addons/marketing_card_event/i18n/ru.po`
- `addons/marketing_card_event/i18n/sk.po`
- `addons/marketing_card_event/i18n/sl.po`
- `addons/marketing_card_event/i18n/sr@latin.po`
- `addons/marketing_card_event/i18n/sv.po`
- `addons/marketing_card_event/i18n/th.po`
- `addons/marketing_card_event/i18n/tr.po`
- `addons/marketing_card_event/i18n/uk.po`
- `addons/marketing_card_event/i18n/uz.po`
- `addons/marketing_card_event/i18n/vi.po`
- `addons/marketing_card_event/i18n/zh_CN.po`
- `addons/marketing_card_event/i18n/zh_TW.po`
- `addons/marketing_card_event/models/__init__.py`
- `addons/marketing_card_event/models/card_campaign.py`
- `addons/marketing_card_event/models/event_event.py`
- `addons/marketing_card_event/models/mailing_mailing.py`
- `addons/marketing_card_event/tests/__init__.py`
- `addons/marketing_card_event/tests/test_mailing.py`
- `addons/marketing_card_event/views/event_event_views.xml`
- `addons/marketing_card_event/views/mailing_mailing_views.xml`
