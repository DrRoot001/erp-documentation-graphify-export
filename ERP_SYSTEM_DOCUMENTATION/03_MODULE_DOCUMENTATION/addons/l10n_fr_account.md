# Module: l10n_fr_account

- **Module ID:** MOD-190
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_fr_account`
- **Manifest:** `addons/l10n_fr_account/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the module to manage the accounting chart for France in Odoo.
========================================================================

This module applies to companies based in France mainland. It doesn't apply to
companies based in the DOM-TOMs (Guadeloupe, Martinique, Guyane, Réunion, Mayotte).

This localisation module creates the VAT taxes of type 'tax included' for purchases
(it is notably required when you use the module 'hr_expense'). Beware that these
'tax included' VAT taxes are not managed by the fiscal positions provided by this
module (because it is complex to manage both 'tax excluded' and 'tax included'
scenarios in fiscal positions).

This localisation module doesn't properly handle the scenario when a France-mainland
company sells services to a company based in the DOMs. We could manage it in the
fiscal positions, but it would require to differentiate between 'product' VAT taxes
and 'service' VAT taxes. We consider that it is too 'heavy' to have this by default
in l10n_fr_account; companies that sell services to DOM-based companies should update the
configuration of their taxes and fiscal positions manually.

**Credits:** Sistheo, Zeekom, CrysaLEAD, Akretion and Camptocamp.

**Scope evidence:** The module contains 39 files, including 23 Python, 6 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`, `l10n_fr`.

## 2. Module structure

- Model/business logic files: 14
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 0
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_fr_account/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 14 model declarations, 50 methods, 0 constraint handlers, 1 onchange handlers, and 5 dependency declarations.
- **Evidence:** `addons/l10n_fr_account/models/res_partner.py:4`, `addons/l10n_fr_account/models/template_mq.py:5`, `addons/l10n_fr_account/models/base_document_layout.py:5`, `addons/l10n_fr_account/models/template_fr_comp.py:5`, `addons/l10n_fr_account/models/template_re.py:5`, `addons/l10n_fr_account/models/template_fr_asso.py:5`, `addons/l10n_fr_account/models/template_yt.py:5`, `addons/l10n_fr_account/models/template_gf.py:5`, `addons/l10n_fr_account/models/template_mc.py:6`, `addons/l10n_fr_account/models/account_move.py:4`, `addons/l10n_fr_account/models/template_fr.py:6`, `addons/l10n_fr_account/models/template_gp.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 0 JavaScript/TypeScript files; static XML analysis found 489 record/template/menu identifiers.
- **Evidence:** `addons/l10n_fr_account/wizard/account_fr_fec_export_wizard_view.xml:3`, `addons/l10n_fr_account/data/account_data.xml:4`, `addons/l10n_fr_account/data/account_data.xml:9`, `addons/l10n_fr_account/data/account_chart_template_data.xml:3`, `addons/l10n_fr_account/data/account_chart_template_data.xml:9`, `addons/l10n_fr_account/data/account_chart_template_data.xml:15`, `addons/l10n_fr_account/data/tax_report_data.xml:3`, `addons/l10n_fr_account/data/tax_report_data.xml:12`, `addons/l10n_fr_account/data/tax_report_data.xml:17`, `addons/l10n_fr_account/data/tax_report_data.xml:24`, `addons/l10n_fr_account/data/tax_report_data.xml:29`, `addons/l10n_fr_account/data/tax_report_data.xml:33`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_fr_account/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/l10n_fr_account/tests/test_fec_export.py`, `addons/l10n_fr_account/tests/__init__.py`, `addons/l10n_fr_account/tests/test_res_partner.py`, `addons/l10n_fr_account/tests/test_fr_tax_report.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `fec_export_wizard_view`, `display_name_in_footer_param`, `europe_vat_without_mc`, `account_fr_tag_salaires`, `account_fr_tag_charges_sociales`, `France`, `tax_report`, `tax_report_balance`, `tax_report_adjustment`, `tax_report_montant_op_realisees`, `tax_report_op_imposables_ht`, `tax_report_A1`, `tax_report_A1_tag`, `tax_report_A1_tag_rounded`, `tax_report_A1_balance_from_tags`, `tax_report_A1_adjustment`, `tax_report_A2`, `tax_report_A2_tag`, `tax_report_A2_tag_rounded`, `tax_report_A2_balance_from_tags`
- Menus: 1; representative evidence: `addons/l10n_fr_account/data/account_chart_template_data.xml:15`
- Templates: 1; representative evidence: `addons/l10n_fr_account/views/report_invoice.xml:3`
- View/action field declarations: 2; representative evidence: `addons/l10n_fr_account/wizard/account_fr_fec_export_wizard_view.xml:5`, `addons/l10n_fr_account/wizard/account_fr_fec_export_wizard_view.xml:6`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_fr_account/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 14
- Representative model evidence: inherits `res.partner` (addons/l10n_fr_account/models/res_partner.py:4); inherits `account.chart.template` (addons/l10n_fr_account/models/template_mq.py:5); inherits `base.document.layout` (addons/l10n_fr_account/models/base_document_layout.py:5); inherits `account.chart.template` (addons/l10n_fr_account/models/template_fr_comp.py:5); inherits `account.chart.template` (addons/l10n_fr_account/models/template_re.py:5); inherits `account.chart.template` (addons/l10n_fr_account/models/template_fr_asso.py:5); inherits `account.chart.template` (addons/l10n_fr_account/models/template_yt.py:5); inherits `account.chart.template` (addons/l10n_fr_account/models/template_gf.py:5); inherits `account.chart.template` (addons/l10n_fr_account/models/template_mc.py:6); inherits `account.move` (addons/l10n_fr_account/models/account_move.py:4); inherits `account.chart.template` (addons/l10n_fr_account/models/template_fr.py:6); inherits `account.chart.template` (addons/l10n_fr_account/models/template_gp.py:5); inherits `res.company` (addons/l10n_fr_account/models/res_company.py:7); `l10n_fr.fec.export.wizard` (addons/l10n_fr_account/wizard/account_fr_fec_export_wizard.py:14)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `account_edi_ubl_cii`, `l10n_fr`
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

- `addons/l10n_fr_account/__init__.py`
- `addons/l10n_fr_account/__manifest__.py`
- `addons/l10n_fr_account/data/account_chart_template_data.xml`
- `addons/l10n_fr_account/data/account_data.xml`
- `addons/l10n_fr_account/data/l10n_fr_account_demo.xml`
- `addons/l10n_fr_account/data/tax_report_data.xml`
- `addons/l10n_fr_account/data/template/account.account-fr.csv`
- `addons/l10n_fr_account/data/template/account.account-fr_asso.csv`
- `addons/l10n_fr_account/data/template/account.account-fr_comp.csv`
- `addons/l10n_fr_account/data/template/account.depreciation.model-fr_comp.csv`
- `addons/l10n_fr_account/data/template/account.fiscal.position-fr.csv`
- `addons/l10n_fr_account/data/template/account.tax-fr.csv`
- `addons/l10n_fr_account/data/template/account.tax.group-fr.csv`
- `addons/l10n_fr_account/i18n/fr.po`
- `addons/l10n_fr_account/i18n/l10n_fr_account.pot`
- `addons/l10n_fr_account/migrations/2.2/pre-migrate-add-bank-xmlid.py`
- `addons/l10n_fr_account/models/__init__.py`
- `addons/l10n_fr_account/models/account_move.py`
- `addons/l10n_fr_account/models/base_document_layout.py`
- `addons/l10n_fr_account/models/res_company.py`
- `addons/l10n_fr_account/models/res_partner.py`
- `addons/l10n_fr_account/models/template_fr.py`
- `addons/l10n_fr_account/models/template_fr_asso.py`
- `addons/l10n_fr_account/models/template_fr_comp.py`
- `addons/l10n_fr_account/models/template_gf.py`
- `addons/l10n_fr_account/models/template_gp.py`
- `addons/l10n_fr_account/models/template_mc.py`
- `addons/l10n_fr_account/models/template_mq.py`
- `addons/l10n_fr_account/models/template_re.py`
- `addons/l10n_fr_account/models/template_yt.py`
- `addons/l10n_fr_account/security/ir.access.csv`
- `addons/l10n_fr_account/tests/__init__.py`
- `addons/l10n_fr_account/tests/test_fec_export.py`
- `addons/l10n_fr_account/tests/test_fr_tax_report.py`
- `addons/l10n_fr_account/tests/test_res_partner.py`
- `addons/l10n_fr_account/views/report_invoice.xml`
- `addons/l10n_fr_account/wizard/__init__.py`
- `addons/l10n_fr_account/wizard/account_fr_fec_export_wizard.py`
- `addons/l10n_fr_account/wizard/account_fr_fec_export_wizard_view.xml`
