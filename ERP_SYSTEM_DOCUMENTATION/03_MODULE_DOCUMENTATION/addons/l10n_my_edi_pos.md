# Module: l10n_my_edi_pos

- **Module ID:** MOD-280
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_my_edi_pos`
- **Manifest:** `addons/l10n_my_edi_pos/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Consolidated E-invoicing using MyInvois

**Manifest description:**

This modules allows the user to send consolidated invoices to the MyInvois system when using the POS app.

**Scope evidence:** The module contains 26 files, including 13 Python, 10 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_my_edi`, `point_of_sale`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 2
- XML/data/view/template files: 10
- Browser asset files: 1
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 80 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/l10n_my_edi_pos/models/res_partner.py:4`, `addons/l10n_my_edi_pos/models/pos_order.py:6`, `addons/l10n_my_edi_pos/models/myinvois_document_pos.py:10`, `addons/l10n_my_edi_pos/models/account_edi_xml_ubl_my.py:7`, `addons/l10n_my_edi_pos/wizard/myinvois_consolidate_invoice_wizard.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/l10n_my_edi_pos/controllers/portal.py`, `addons/l10n_my_edi_pos/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 10 XML files and 1 JavaScript/TypeScript files; static XML analysis found 14 record/template/menu identifiers.
- **Evidence:** `addons/l10n_my_edi_pos/views/ticket_validation_screen.xml:4`, `addons/l10n_my_edi_pos/views/pos_order_views.xml:3`, `addons/l10n_my_edi_pos/views/pos_order_views.xml:22`, `addons/l10n_my_edi_pos/views/pos_order_views.xml:38`, `addons/l10n_my_edi_pos/views/pos_order_views.xml:63`, `addons/l10n_my_edi_pos/views/res_partner_view.xml:3`, `addons/l10n_my_edi_pos/views/portal_address_templates.xml:3`, `addons/l10n_my_edi_pos/views/product_view.xml:3`, `addons/l10n_my_edi_pos/views/myinvois_document_pos_views.xml:4`, `addons/l10n_my_edi_pos/views/myinvois_document_pos_views.xml:17`, `addons/l10n_my_edi_pos/views/myinvois_document_pos_views.xml:31`, `addons/l10n_my_edi_pos/views/myinvois_document_pos_views.xml:50`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_my_edi_pos/tests/test_myinvois_pos.py`, `addons/l10n_my_edi_pos/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 10; representative identifiers: `ticket_validation_screen`, `view_pos_pos_form`, `view_pos_order_tree`, `view_pos_order_filter`, `view_pos_order_tree_consolidated`, `view_partner_form_pos_ui_inherit_l10n_my_edi_pos`, `portal_address_form_fields_my`, `myinvois_product_product_view_form_normalized_pos`, `myinvois_document_form_view`, `myinvois_document_pos_form_view`, `myinvois_document_pos_list_view`, `myinvois_document_pos_search_view`, `action_consolidated_invoices`, `l10n_my_edi_pos.menu_consolidated_invoices`
- Menus: 1; representative evidence: `addons/l10n_my_edi_pos/views/myinvois_document_pos_views.xml:80`
- Templates: 2; representative evidence: `addons/l10n_my_edi_pos/views/ticket_validation_screen.xml:4`, `addons/l10n_my_edi_pos/views/portal_address_templates.xml:3`
- View/action field declarations: 22; representative evidence: `addons/l10n_my_edi_pos/views/pos_order_views.xml:5`, `addons/l10n_my_edi_pos/views/pos_order_views.xml:7`, `addons/l10n_my_edi_pos/views/pos_order_views.xml:24`, `addons/l10n_my_edi_pos/views/pos_order_views.xml:26`, `addons/l10n_my_edi_pos/views/pos_order_views.xml:40`, `addons/l10n_my_edi_pos/views/pos_order_views.xml:42`, `addons/l10n_my_edi_pos/views/pos_order_views.xml:65`, `addons/l10n_my_edi_pos/views/pos_order_views.xml:69`, `addons/l10n_my_edi_pos/views/res_partner_view.xml:5`, `addons/l10n_my_edi_pos/views/res_partner_view.xml:7`, `addons/l10n_my_edi_pos/views/product_view.xml:5`, `addons/l10n_my_edi_pos/views/product_view.xml:7`
- Browser assets: 1; representative files: `addons/l10n_my_edi_pos/static/src/interactions/address.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_my_edi_pos/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `res.partner` (addons/l10n_my_edi_pos/models/res_partner.py:4); inherits `pos.order` (addons/l10n_my_edi_pos/models/pos_order.py:6); inherits `myinvois.document` (addons/l10n_my_edi_pos/models/myinvois_document_pos.py:10); inherits `account.edi.xml.ubl_myinvois_my` (addons/l10n_my_edi_pos/models/account_edi_xml_ubl_my.py:7); inherits `myinvois.consolidate.invoice.wizard` (addons/l10n_my_edi_pos/wizard/myinvois_consolidate_invoice_wizard.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_my_edi`, `point_of_sale`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_my_edi_pos/__init__.py`
- `addons/l10n_my_edi_pos/__manifest__.py`
- `addons/l10n_my_edi_pos/controllers/__init__.py`
- `addons/l10n_my_edi_pos/controllers/portal.py`
- `addons/l10n_my_edi_pos/i18n/l10n_my_edi_pos.pot`
- `addons/l10n_my_edi_pos/i18n/ms.po`
- `addons/l10n_my_edi_pos/models/__init__.py`
- `addons/l10n_my_edi_pos/models/account_edi_xml_ubl_my.py`
- `addons/l10n_my_edi_pos/models/myinvois_document_pos.py`
- `addons/l10n_my_edi_pos/models/pos_order.py`
- `addons/l10n_my_edi_pos/models/res_partner.py`
- `addons/l10n_my_edi_pos/static/src/interactions/address.js`
- `addons/l10n_my_edi_pos/tests/__init__.py`
- `addons/l10n_my_edi_pos/tests/expected_xmls/consolidated_invoice.xml`
- `addons/l10n_my_edi_pos/tests/expected_xmls/consolidated_invoice_refund.xml`
- `addons/l10n_my_edi_pos/tests/expected_xmls/consolidated_invoice_tax_included.xml`
- `addons/l10n_my_edi_pos/tests/expected_xmls/consolidated_invoice_tax_included_with_discount.xml`
- `addons/l10n_my_edi_pos/tests/test_myinvois_pos.py`
- `addons/l10n_my_edi_pos/views/myinvois_document_pos_views.xml`
- `addons/l10n_my_edi_pos/views/portal_address_templates.xml`
- `addons/l10n_my_edi_pos/views/pos_order_views.xml`
- `addons/l10n_my_edi_pos/views/product_view.xml`
- `addons/l10n_my_edi_pos/views/res_partner_view.xml`
- `addons/l10n_my_edi_pos/views/ticket_validation_screen.xml`
- `addons/l10n_my_edi_pos/wizard/__init__.py`
- `addons/l10n_my_edi_pos/wizard/myinvois_consolidate_invoice_wizard.py`
