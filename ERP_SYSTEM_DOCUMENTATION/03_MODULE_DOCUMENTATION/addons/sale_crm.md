# Module: sale_crm

- **Module ID:** MOD-510
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_crm`
- **Manifest:** `addons/sale_crm/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module adds a shortcut on one or several opportunity cases in the CRM.
===========================================================================

This shortcut allows you to generate a sales order based on the selected case.
If different cases are open (a list), it generates one sales order by case.
The case is then closed and linked to the generated sales order.

We suggest you to install this module, if you installed both the sale and the crm
modules.

**Scope evidence:** The module contains 77 files, including 13 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `sale`, `crm`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 0
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/sale_crm/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 25 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/sale_crm/models/sale_order.py:7`, `addons/sale_crm/models/crm_team.py:6`, `addons/sale_crm/models/crm_lead.py:7`, `addons/sale_crm/wizard/crm_opportunity_to_quotation.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 10 record/template/menu identifiers.
- **Evidence:** `addons/sale_crm/wizard/crm_opportunity_to_quotation_views.xml:3`, `addons/sale_crm/wizard/crm_opportunity_to_quotation_views.xml:23`, `addons/sale_crm/data/crm_lead_merge_template.xml:4`, `addons/sale_crm/views/crm_team_views.xml:3`, `addons/sale_crm/views/crm_lead_views.xml:4`, `addons/sale_crm/views/crm_lead_views.xml:34`, `addons/sale_crm/views/crm_lead_views.xml:38`, `addons/sale_crm/views/sale_order_views.xml:4`, `addons/sale_crm/views/sale_order_views.xml:12`, `addons/sale_crm/views/sale_order_views.xml:40`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/sale_crm/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/sale_crm/tests/test_crm_lead_convert_quotation.py`, `addons/sale_crm/tests/test_crm_lead_merge.py`, `addons/sale_crm/tests/__init__.py`, `addons/sale_crm/tests/test_res_partner.py`, `addons/sale_crm/tests/test_sale_crm.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `crm_quotation_partner_view_form`, `crm_quotation_partner_action`, `crm_lead_merge_summary_inherit_sale_crm`, `crm_team_salesteams_view_form_in_sale_crm`, `crm_case_form_view_oppor`, `crm.crm_lead_opportunities`, `sales_team.mail_activity_type_action_config_sales`, `sale_action_quotations_new`, `sale_view_inherit123`, `My Quotations`
- Menus: 1; representative evidence: `addons/sale_crm/views/sale_order_views.xml:40`
- Templates: 1; representative evidence: `addons/sale_crm/data/crm_lead_merge_template.xml:4`
- View/action field declarations: 12; representative evidence: `addons/sale_crm/wizard/crm_opportunity_to_quotation_views.xml:5`, `addons/sale_crm/wizard/crm_opportunity_to_quotation_views.xml:6`, `addons/sale_crm/wizard/crm_opportunity_to_quotation_views.xml:25`, `addons/sale_crm/wizard/crm_opportunity_to_quotation_views.xml:26`, `addons/sale_crm/views/crm_team_views.xml:5`, `addons/sale_crm/views/crm_team_views.xml:7`, `addons/sale_crm/views/crm_lead_views.xml:6`, `addons/sale_crm/views/crm_lead_views.xml:8`, `addons/sale_crm/views/sale_order_views.xml:6`, `addons/sale_crm/views/sale_order_views.xml:7`, `addons/sale_crm/views/sale_order_views.xml:14`, `addons/sale_crm/views/sale_order_views.xml:16`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale_crm/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `sale.order` (addons/sale_crm/models/sale_order.py:7); inherits `crm.team` (addons/sale_crm/models/crm_team.py:6); inherits `crm.lead` (addons/sale_crm/models/crm_lead.py:7); `crm.quotation.partner` (addons/sale_crm/wizard/crm_opportunity_to_quotation.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale`, `crm`
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

- `addons/sale_crm/__init__.py`
- `addons/sale_crm/__manifest__.py`
- `addons/sale_crm/data/crm_lead_merge_template.xml`
- `addons/sale_crm/i18n/af.po`
- `addons/sale_crm/i18n/ar.po`
- `addons/sale_crm/i18n/az.po`
- `addons/sale_crm/i18n/bg.po`
- `addons/sale_crm/i18n/bs.po`
- `addons/sale_crm/i18n/ca.po`
- `addons/sale_crm/i18n/cs.po`
- `addons/sale_crm/i18n/da.po`
- `addons/sale_crm/i18n/de.po`
- `addons/sale_crm/i18n/el.po`
- `addons/sale_crm/i18n/es.po`
- `addons/sale_crm/i18n/es_419.po`
- `addons/sale_crm/i18n/es_CL.po`
- `addons/sale_crm/i18n/et.po`
- `addons/sale_crm/i18n/eu.po`
- `addons/sale_crm/i18n/fa.po`
- `addons/sale_crm/i18n/fi.po`
- `addons/sale_crm/i18n/fr.po`
- `addons/sale_crm/i18n/fr_CA.po`
- `addons/sale_crm/i18n/gl.po`
- `addons/sale_crm/i18n/gu.po`
- `addons/sale_crm/i18n/he.po`
- `addons/sale_crm/i18n/hi.po`
- `addons/sale_crm/i18n/hr.po`
- `addons/sale_crm/i18n/hu.po`
- `addons/sale_crm/i18n/id.po`
- `addons/sale_crm/i18n/is.po`
- `addons/sale_crm/i18n/it.po`
- `addons/sale_crm/i18n/ja.po`
- `addons/sale_crm/i18n/kab.po`
- `addons/sale_crm/i18n/km.po`
- `addons/sale_crm/i18n/ko.po`
- `addons/sale_crm/i18n/ku.po`
- `addons/sale_crm/i18n/lo.po`
- `addons/sale_crm/i18n/lt.po`
- `addons/sale_crm/i18n/lv.po`
- `addons/sale_crm/i18n/mk.po`
- `addons/sale_crm/i18n/mn.po`
- `addons/sale_crm/i18n/my.po`
- `addons/sale_crm/i18n/nb.po`
- `addons/sale_crm/i18n/nl.po`
- `addons/sale_crm/i18n/pl.po`
- `addons/sale_crm/i18n/pt.po`
- `addons/sale_crm/i18n/pt_BR.po`
- `addons/sale_crm/i18n/ro.po`
- `addons/sale_crm/i18n/ru.po`
- `addons/sale_crm/i18n/sale_crm.pot`
- `addons/sale_crm/i18n/sk.po`
- `addons/sale_crm/i18n/sl.po`
- `addons/sale_crm/i18n/sr@latin.po`
- `addons/sale_crm/i18n/sv.po`
- `addons/sale_crm/i18n/th.po`
- `addons/sale_crm/i18n/tr.po`
- `addons/sale_crm/i18n/uk.po`
- `addons/sale_crm/i18n/uz.po`
- `addons/sale_crm/i18n/vi.po`
- `addons/sale_crm/i18n/zh_CN.po`
- `addons/sale_crm/i18n/zh_TW.po`
- `addons/sale_crm/models/__init__.py`
- `addons/sale_crm/models/crm_lead.py`
- `addons/sale_crm/models/crm_team.py`
- `addons/sale_crm/models/sale_order.py`
- `addons/sale_crm/security/ir.access.csv`
- `addons/sale_crm/tests/__init__.py`
- `addons/sale_crm/tests/test_crm_lead_convert_quotation.py`
- `addons/sale_crm/tests/test_crm_lead_merge.py`
- `addons/sale_crm/tests/test_res_partner.py`
- `addons/sale_crm/tests/test_sale_crm.py`
- `addons/sale_crm/views/crm_lead_views.xml`
- `addons/sale_crm/views/crm_team_views.xml`
- `addons/sale_crm/views/sale_order_views.xml`
- `addons/sale_crm/wizard/__init__.py`
- `addons/sale_crm/wizard/crm_opportunity_to_quotation.py`
- `addons/sale_crm/wizard/crm_opportunity_to_quotation_views.xml`
