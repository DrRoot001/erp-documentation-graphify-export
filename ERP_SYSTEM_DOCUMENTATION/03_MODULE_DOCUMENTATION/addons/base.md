# Module: base

- **Module ID:** MOD-648
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `odoo/addons/base`
- **Manifest:** `odoo/addons/base/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

The kernel of Odoo, needed for all installation.
===================================================

**Scope evidence:** The module contains 661 files, including 107 Python, 88 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: None declared.

## 2. Module structure

- Model/business logic files: 130
- Controller/API files: 0
- XML/data/view/template files: 88
- Browser asset files: 1
- Security files: 2
- Test files: 42
- Scheduled/automation evidence files: 28
- Reporting evidence files: 13

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `odoo/addons/base/security/base_groups.xml`, `odoo/addons/base/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 130 model declarations, 2500 methods, 49 constraint handlers, 35 onchange handlers, and 134 dependency declarations.
- **Evidence:** `odoo/addons/base/models/properties_base_definition_mixin.py:8`, `odoo/addons/base/models/res_partner.py:141`, `odoo/addons/base/models/res_partner.py:153`, `odoo/addons/base/models/res_partner.py:231`, `odoo/addons/base/models/res_partner.py:271`, `odoo/addons/base/models/res_partner.py:2453`, `odoo/addons/base/models/ir_access.py:64`, `odoo/addons/base/models/ir_profile_query.py:15`, `odoo/addons/base/models/res_lang.py:83`, `odoo/addons/base/models/ir_config_parameter.py:33`, `odoo/addons/base/models/ir_profile.py:21`, `odoo/addons/base/models/ir_profile.py:259`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 88 XML files and 1 JavaScript/TypeScript files; static XML analysis found 1141 record/template/menu identifiers.
- **Evidence:** `odoo/addons/base/security/base_groups.xml:6`, `odoo/addons/base/security/base_groups.xml:11`, `odoo/addons/base/security/base_groups.xml:16`, `odoo/addons/base/security/base_groups.xml:26`, `odoo/addons/base/security/base_groups.xml:31`, `odoo/addons/base/security/base_groups.xml:37`, `odoo/addons/base/security/base_groups.xml:42`, `odoo/addons/base/security/base_groups.xml:46`, `odoo/addons/base/security/base_groups.xml:53`, `odoo/addons/base/security/base_groups.xml:57`, `odoo/addons/base/security/base_groups.xml:61`, `odoo/addons/base/security/base_groups.xml:66`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `odoo/addons/base/security/base_groups.xml`, `odoo/addons/base/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 28 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `odoo/addons/base/__manifest__.py`, `odoo/addons/base/models/ir_profile.py`, `odoo/addons/base/models/res_device.py`, `odoo/addons/base/models/ir_model.py`, `odoo/addons/base/models/ir_actions.py`, `odoo/addons/base/models/ir_http.py`, `odoo/addons/base/models/ir_module.py`, `odoo/addons/base/models/res_users_deletion.py`, `odoo/addons/base/models/ir_autovacuum.py`, `odoo/addons/base/models/res_users.py`, `odoo/addons/base/models/__init__.py`, `odoo/addons/base/models/ir_cron.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 13 files contain report-action/template indicators.
- **Evidence:** `odoo/addons/base/models/ir_actions_report.py`, `odoo/addons/base/models/ir_module.py`, `odoo/addons/base/models/ir_qweb_fields.py`, `odoo/addons/base/models/ir_ui_menu.py`, `odoo/addons/base/models/report_paperformat.py`, `odoo/addons/base/report/ir_model_report.xml`, `odoo/addons/base/report/report_base_report_irmodulereference.py`, `odoo/addons/base/report/ir_module_reports.xml`, `odoo/addons/base/views/ir_actions_views.xml`, `odoo/addons/base/views/report_paperformat_views.xml`, `odoo/addons/base/tests/test_ir_ui_view.py`, `odoo/addons/base/tests/test_ir_module.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 42 test files are present.
- **Evidence:** `odoo/addons/base/tests/test_calendar_view.py`, `odoo/addons/base/tests/test_avatar_mixin.py`, `odoo/addons/base/tests/test_res_lang.py`, `odoo/addons/base/tests/test_ir_cron.py`, `odoo/addons/base/tests/test_ir_http.py`, `odoo/addons/base/tests/test_res_currency.py`, `odoo/addons/base/tests/test_ir_model.py`, `odoo/addons/base/tests/test_ir_mail_server_smtpd.py`, `odoo/addons/base/tests/test_res_users.py`, `odoo/addons/base/tests/mail_examples.py`, `odoo/addons/base/tests/test_ir_mail_server.py`, `odoo/addons/base/tests/test_ir_actions.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 88; representative identifiers: `module_category_master_data`, `res_groups_privilege_export`, `res_groups_privilege_contact`, `group_user`, `group_user_regular`, `group_erp_manager`, `group_sanitize_override`, `group_system`, `group_multi_company`, `group_multi_currency`, `group_no_one`, `group_allow_export`, `group_partner_manager`, `group_portal`, `group_public`, `group_everyone`, `public_user`, `template_portal_user_id`, `default_template_user_config`, `default_user_group`
- Menus: 66; representative evidence: `odoo/addons/base/views/base_menus.xml:4`, `odoo/addons/base/views/base_menus.xml:11`, `odoo/addons/base/views/base_menus.xml:12`, `odoo/addons/base/views/base_menus.xml:13`, `odoo/addons/base/views/base_menus.xml:14`, `odoo/addons/base/views/base_menus.xml:15`, `odoo/addons/base/views/base_menus.xml:18`, `odoo/addons/base/views/base_menus.xml:25`, `odoo/addons/base/views/base_menus.xml:33`, `odoo/addons/base/views/base_menus.xml:40`, `odoo/addons/base/views/base_menus.xml:41`, `odoo/addons/base/views/base_menus.xml:42`
- Templates: 5; representative evidence: `odoo/addons/base/report/ir_model_templates.xml:3`, `odoo/addons/base/report/ir_module_report_templates.xml:4`, `odoo/addons/base/views/ir_qweb_widget_templates.xml:3`, `odoo/addons/base/views/ir_qweb_widget_templates.xml:17`, `odoo/addons/base/views/ir_qweb_widget_templates.xml:68`
- View/action field declarations: 504; representative evidence: `odoo/addons/base/report/ir_model_report.xml:5`, `odoo/addons/base/report/ir_module_reports.xml:7`, `odoo/addons/base/wizard/base_export_language_views.xml:6`, `odoo/addons/base/wizard/base_export_language_views.xml:7`, `odoo/addons/base/wizard/base_export_language_views.xml:68`, `odoo/addons/base/wizard/base_export_language_views.xml:69`, `odoo/addons/base/wizard/base_partner_merge_views.xml:5`, `odoo/addons/base/wizard/base_partner_merge_views.xml:6`, `odoo/addons/base/wizard/base_partner_merge_views.xml:13`, `odoo/addons/base/wizard/base_partner_merge_views.xml:14`, `odoo/addons/base/wizard/base_partner_merge_views.xml:104`, `odoo/addons/base/wizard/base_partner_merge_views.xml:105`
- Browser assets: 1; representative files: `odoo/addons/base/static/tests/test_ir_model_fields_translation.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `odoo/addons/base/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `odoo/addons/base/__manifest__.py`, `odoo/addons/base/models/ir_profile.py`, `odoo/addons/base/models/res_device.py`, `odoo/addons/base/models/ir_model.py`, `odoo/addons/base/models/ir_actions.py`, `odoo/addons/base/models/ir_http.py`, `odoo/addons/base/models/ir_module.py`, `odoo/addons/base/models/res_users_deletion.py`, `odoo/addons/base/models/ir_autovacuum.py`, `odoo/addons/base/models/res_users.py`, `odoo/addons/base/models/__init__.py`, `odoo/addons/base/models/ir_cron.py`
- **Report entry points:** `odoo/addons/base/models/ir_actions_report.py`, `odoo/addons/base/models/ir_module.py`, `odoo/addons/base/models/ir_qweb_fields.py`, `odoo/addons/base/models/ir_ui_menu.py`, `odoo/addons/base/models/report_paperformat.py`, `odoo/addons/base/report/ir_model_report.xml`, `odoo/addons/base/report/report_base_report_irmodulereference.py`, `odoo/addons/base/report/ir_module_reports.xml`, `odoo/addons/base/views/ir_actions_views.xml`, `odoo/addons/base/views/report_paperformat_views.xml`, `odoo/addons/base/tests/test_ir_ui_view.py`, `odoo/addons/base/tests/test_ir_module.py`

## 7. Database interactions

- Model declarations: 130
- Representative model evidence: `properties.base.definition.mixin` (odoo/addons/base/models/properties_base_definition_mixin.py:8); `format.vat.label.mixin` (odoo/addons/base/models/res_partner.py:141); `format.address.mixin` (odoo/addons/base/models/res_partner.py:153); `res.partner.category` (odoo/addons/base/models/res_partner.py:231); `res.partner` (odoo/addons/base/models/res_partner.py:271); `res.partner.industry` (odoo/addons/base/models/res_partner.py:2453); `ir.access` (odoo/addons/base/models/ir_access.py:64); `ir.profile.query` (odoo/addons/base/models/ir_profile_query.py:15); `res.lang` (odoo/addons/base/models/res_lang.py:83); `ir.config_parameter` (odoo/addons/base/models/ir_config_parameter.py:33); `ir.profile` (odoo/addons/base/models/ir_profile.py:21); `base.enable.profiling.wizard` (odoo/addons/base/models/ir_profile.py:259); `ir.ui.view.custom` (odoo/addons/base/models/ir_ui_view.py:73); `ir.ui.view` (odoo/addons/base/models/ir_ui_view.py:146); `reset.view.arch.wizard` (odoo/addons/base/models/ir_ui_view.py:2728); inherits `base` (odoo/addons/base/models/ir_ui_view.py:2810); `res.groups` (odoo/addons/base/models/res_groups.py:14); `ir.asset` (odoo/addons/base/models/ir_asset.py:51); `avatar.mixin` (odoo/addons/base/models/avatar_mixin.py:36); `res.device.log` (odoo/addons/base/models/res_device.py:26); `res.device` (odoo/addons/base/models/res_device.py:175); `res.session` (odoo/addons/base/models/res_device.py:265); `ir.sequence` (odoo/addons/base/models/ir_sequence.py:84); `ir.sequence.date_range` (odoo/addons/base/models/ir_sequence.py:311); `ir.qweb` (odoo/addons/base/models/ir_qweb.py:699); `res.currency` (odoo/addons/base/models/res_currency.py:51); `res.currency.rate` (odoo/addons/base/models/res_currency.py:396); `base` (odoo/addons/base/models/ir_model.py:211); `_unknown` (odoo/addons/base/models/ir_model.py:217); `ir.model` (odoo/addons/base/models/ir_model.py:226)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: None declared
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

- `odoo/addons/base/__init__.py`
- `odoo/addons/base/__manifest__.py`
- `odoo/addons/base/data/base_data.sql`
- `odoo/addons/base/data/base_data_test.sql`
- `odoo/addons/base/data/clearing_label_data.xml`
- `odoo/addons/base/data/ir_action_data.xml`
- `odoo/addons/base/data/ir_config_parameter_data.xml`
- `odoo/addons/base/data/ir_cron_data.xml`
- `odoo/addons/base/data/ir_demo_data.xml`
- `odoo/addons/base/data/ir_demo_failure_data.xml`
- `odoo/addons/base/data/ir_module_category_data.xml`
- `odoo/addons/base/data/ir_module_module.xml`
- `odoo/addons/base/data/neutralize.sql`
- `odoo/addons/base/data/report_paperformat_data.xml`
- `odoo/addons/base/data/res.country.state.csv`
- `odoo/addons/base/data/res.lang.csv`
- `odoo/addons/base/data/res_company_data.xml`
- `odoo/addons/base/data/res_country_data.xml`
- `odoo/addons/base/data/res_currency_data.xml`
- `odoo/addons/base/data/res_currency_demo.xml`
- `odoo/addons/base/data/res_currency_rate_demo.xml`
- `odoo/addons/base/data/res_lang_data.xml`
- `odoo/addons/base/data/res_partner_bank_demo.xml`
- `odoo/addons/base/data/res_partner_data.xml`
- `odoo/addons/base/data/res_partner_demo.xml`
- `odoo/addons/base/data/res_partner_image_demo.xml`
- `odoo/addons/base/data/res_users_data.xml`
- `odoo/addons/base/data/res_users_demo.xml`
- `odoo/addons/base/data/rtlcss.json`
- `odoo/addons/base/data/website.xml`
- `odoo/addons/base/i18n/af.po`
- `odoo/addons/base/i18n/am.po`
- `odoo/addons/base/i18n/ar.po`
- `odoo/addons/base/i18n/az.po`
- `odoo/addons/base/i18n/base.pot`
- `odoo/addons/base/i18n/bg.po`
- `odoo/addons/base/i18n/bs.po`
- `odoo/addons/base/i18n/ca.po`
- `odoo/addons/base/i18n/cs.po`
- `odoo/addons/base/i18n/da.po`
- `odoo/addons/base/i18n/de.po`
- `odoo/addons/base/i18n/el.po`
- `odoo/addons/base/i18n/es.po`
- `odoo/addons/base/i18n/es_419.po`
- `odoo/addons/base/i18n/es_CL.po`
- `odoo/addons/base/i18n/et.po`
- `odoo/addons/base/i18n/eu.po`
- `odoo/addons/base/i18n/fa.po`
- `odoo/addons/base/i18n/fi.po`
- `odoo/addons/base/i18n/fo.po`
- `odoo/addons/base/i18n/fr.po`
- `odoo/addons/base/i18n/fr_BE.po`
- `odoo/addons/base/i18n/fr_CA.po`
- `odoo/addons/base/i18n/gl.po`
- `odoo/addons/base/i18n/gu.po`
- `odoo/addons/base/i18n/he.po`
- `odoo/addons/base/i18n/hi.po`
- `odoo/addons/base/i18n/hr.po`
- `odoo/addons/base/i18n/hu.po`
- `odoo/addons/base/i18n/id.po`
- `odoo/addons/base/i18n/is.po`
- `odoo/addons/base/i18n/it.po`
- `odoo/addons/base/i18n/ja.po`
- `odoo/addons/base/i18n/ka.po`
- `odoo/addons/base/i18n/kab.po`
- `odoo/addons/base/i18n/km.po`
- `odoo/addons/base/i18n/ko.po`
- `odoo/addons/base/i18n/ku.po`
- `odoo/addons/base/i18n/lb.po`
- `odoo/addons/base/i18n/lo.po`
- `odoo/addons/base/i18n/lt.po`
- `odoo/addons/base/i18n/lv.po`
- `odoo/addons/base/i18n/mk.po`
- `odoo/addons/base/i18n/mn.po`
- `odoo/addons/base/i18n/my.po`
- `odoo/addons/base/i18n/nb.po`
- `odoo/addons/base/i18n/nl.po`
- `odoo/addons/base/i18n/pl.po`
- `odoo/addons/base/i18n/pt.po`
- `odoo/addons/base/i18n/pt_BR.po`
- `odoo/addons/base/i18n/ro.po`
- `odoo/addons/base/i18n/ru.po`
- `odoo/addons/base/i18n/sk.po`
- `odoo/addons/base/i18n/sl.po`
- `odoo/addons/base/i18n/sq.po`
- `odoo/addons/base/i18n/sr@latin.po`
- `odoo/addons/base/i18n/sv.po`
- `odoo/addons/base/i18n/th.po`
- `odoo/addons/base/i18n/tr.po`
- `odoo/addons/base/i18n/uk.po`
- `odoo/addons/base/i18n/uz.po`
- `odoo/addons/base/i18n/vi.po`
- `odoo/addons/base/i18n/zh_CN.po`
- `odoo/addons/base/i18n/zh_TW.po`
- `odoo/addons/base/models/__init__.py`
- `odoo/addons/base/models/assetsbundle.py`
- `odoo/addons/base/models/avatar_mixin.py`
- `odoo/addons/base/models/clearing_label.py`
- `odoo/addons/base/models/decimal_precision.py`
- `odoo/addons/base/models/image_mixin.py`
- `odoo/addons/base/models/ir_access.py`
- `odoo/addons/base/models/ir_actions.py`
- `odoo/addons/base/models/ir_actions_report.py`
- `odoo/addons/base/models/ir_asset.py`
- `odoo/addons/base/models/ir_attachment.py`
- `odoo/addons/base/models/ir_autovacuum.py`
- `odoo/addons/base/models/ir_binary.py`
- `odoo/addons/base/models/ir_config_parameter.py`
- `odoo/addons/base/models/ir_cron.py`
- `odoo/addons/base/models/ir_default.py`
- `odoo/addons/base/models/ir_demo.py`
- `odoo/addons/base/models/ir_demo_failure.py`
- `odoo/addons/base/models/ir_embedded_actions.py`
- `odoo/addons/base/models/ir_exports.py`
- `odoo/addons/base/models/ir_fields.py`
- `odoo/addons/base/models/ir_filters.py`
- `odoo/addons/base/models/ir_http.py`
- `odoo/addons/base/models/ir_logging.py`
- `odoo/addons/base/models/ir_mail_server.py`
- `odoo/addons/base/models/ir_model.py`
- `odoo/addons/base/models/ir_module.py`
- `odoo/addons/base/models/ir_profile.py`
- `odoo/addons/base/models/ir_profile_query.py`
- `odoo/addons/base/models/ir_qweb.py`
- `odoo/addons/base/models/ir_qweb_fields.py`
- `odoo/addons/base/models/ir_sequence.py`
- `odoo/addons/base/models/ir_ui_menu.py`
- `odoo/addons/base/models/ir_ui_view.py`
- `odoo/addons/base/models/properties_base_definition.py`
- `odoo/addons/base/models/properties_base_definition_mixin.py`
- `odoo/addons/base/models/report_layout.py`
- `odoo/addons/base/models/report_paperformat.py`
- `odoo/addons/base/models/res_company.py`
- `odoo/addons/base/models/res_config.py`
- `odoo/addons/base/models/res_country.py`
- `odoo/addons/base/models/res_currency.py`
- `odoo/addons/base/models/res_device.py`
- `odoo/addons/base/models/res_groups.py`
- `odoo/addons/base/models/res_groups_privilege.py`
- `odoo/addons/base/models/res_lang.py`
- `odoo/addons/base/models/res_partner.py`
- `odoo/addons/base/models/res_partner_bank.py`
- `odoo/addons/base/models/res_users.py`
- `odoo/addons/base/models/res_users_deletion.py`
- `odoo/addons/base/models/res_users_settings.py`
- `odoo/addons/base/models/website.py`
- `odoo/addons/base/populate/common.xml`
- `odoo/addons/base/report/__init__.py`
- `odoo/addons/base/report/corporate_defaults.xsl`
- `odoo/addons/base/report/custom_default_printscreen.xsl`
- `odoo/addons/base/report/custom_new.xsl`
- `odoo/addons/base/report/custom_rml_printscreen.xsl`
- `odoo/addons/base/report/ir_model_report.xml`
- `odoo/addons/base/report/ir_model_templates.xml`
- `odoo/addons/base/report/ir_module_report_templates.xml`
- `odoo/addons/base/report/ir_module_reports.xml`
- `odoo/addons/base/report/mako_footer.html`
- `odoo/addons/base/report/mako_header.html`
- `odoo/addons/base/report/mako_template.css`
- `odoo/addons/base/report/report_base_report_irmodulereference.py`
- `odoo/addons/base/rng/activity_view.rng`
- `odoo/addons/base/rng/calendar_view.rng`
- `odoo/addons/base/rng/common.rng`
- `odoo/addons/base/rng/graph_view.rng`
- `odoo/addons/base/rng/list_view.rng`
- `odoo/addons/base/rng/pivot_view.rng`
- `odoo/addons/base/rng/search_view.rng`
- `odoo/addons/base/security/base_groups.xml`
- `odoo/addons/base/security/ir.access.csv`
- `odoo/addons/base/static/description/board.png`
- `odoo/addons/base/static/description/board.svg`
- `odoo/addons/base/static/description/exception.png`
- `odoo/addons/base/static/description/exception.svg`
- `odoo/addons/base/static/description/icon.png`
- `odoo/addons/base/static/description/icon.svg`
- `odoo/addons/base/static/description/modules.png`
- `odoo/addons/base/static/description/modules.svg`
- `odoo/addons/base/static/description/settings.png`
- `odoo/addons/base/static/description/settings.svg`
- `odoo/addons/base/static/img/avatar.png`
- `odoo/addons/base/static/img/avatar_grey.png`
- `odoo/addons/base/static/img/avatar_placeholder_company.png`
- `odoo/addons/base/static/img/avatar_placeholder_delivery.png`
- `odoo/addons/base/static/img/avatar_placeholder_invoice.png`
- `odoo/addons/base/static/img/avatar_placeholder_other.png`
- `odoo/addons/base/static/img/bill.png`
- `odoo/addons/base/static/img/company_image.png`
- `odoo/addons/base/static/img/country_flags/419.png`
- `odoo/addons/base/static/img/country_flags/ad.png`
- `odoo/addons/base/static/img/country_flags/ae.png`
- `odoo/addons/base/static/img/country_flags/af.png`
- `odoo/addons/base/static/img/country_flags/ag.png`
- `odoo/addons/base/static/img/country_flags/ai.png`
- `odoo/addons/base/static/img/country_flags/al.png`
- `odoo/addons/base/static/img/country_flags/am.png`
- `odoo/addons/base/static/img/country_flags/an.png`
- `odoo/addons/base/static/img/country_flags/ao.png`
- `odoo/addons/base/static/img/country_flags/ar.png`
- `odoo/addons/base/static/img/country_flags/as.png`
- `odoo/addons/base/static/img/country_flags/at.png`
- `odoo/addons/base/static/img/country_flags/au.png`
- `odoo/addons/base/static/img/country_flags/aw.png`
- `odoo/addons/base/static/img/country_flags/ax.png`
- `odoo/addons/base/static/img/country_flags/az.png`
- `odoo/addons/base/static/img/country_flags/ba.png`
- `odoo/addons/base/static/img/country_flags/bb.png`
- `odoo/addons/base/static/img/country_flags/bd.png`
- `odoo/addons/base/static/img/country_flags/be.png`
- `odoo/addons/base/static/img/country_flags/bf.png`
- `odoo/addons/base/static/img/country_flags/bg.png`
- `odoo/addons/base/static/img/country_flags/bh.png`
- `odoo/addons/base/static/img/country_flags/bi.png`
- `odoo/addons/base/static/img/country_flags/bj.png`
- `odoo/addons/base/static/img/country_flags/bl.png`
- `odoo/addons/base/static/img/country_flags/bm.png`
- `odoo/addons/base/static/img/country_flags/bn.png`
- `odoo/addons/base/static/img/country_flags/bo.png`
- `odoo/addons/base/static/img/country_flags/br.png`
- `odoo/addons/base/static/img/country_flags/bs.png`
- `odoo/addons/base/static/img/country_flags/bt.png`
- `odoo/addons/base/static/img/country_flags/bw.png`
- `odoo/addons/base/static/img/country_flags/by.png`
- `odoo/addons/base/static/img/country_flags/bz.png`
- `odoo/addons/base/static/img/country_flags/ca.png`
- `odoo/addons/base/static/img/country_flags/cc.png`
- `odoo/addons/base/static/img/country_flags/cd.png`
- `odoo/addons/base/static/img/country_flags/cf.png`
- `odoo/addons/base/static/img/country_flags/cg.png`
- `odoo/addons/base/static/img/country_flags/ch.png`
- `odoo/addons/base/static/img/country_flags/ci.png`
- `odoo/addons/base/static/img/country_flags/ck.png`
- `odoo/addons/base/static/img/country_flags/cl.png`
- `odoo/addons/base/static/img/country_flags/cm.png`
- `odoo/addons/base/static/img/country_flags/cn.png`
- `odoo/addons/base/static/img/country_flags/co.png`
- `odoo/addons/base/static/img/country_flags/cr.png`
- `odoo/addons/base/static/img/country_flags/cu.png`
- `odoo/addons/base/static/img/country_flags/cv.png`
- `odoo/addons/base/static/img/country_flags/cw.png`
- `odoo/addons/base/static/img/country_flags/cx.png`
- `odoo/addons/base/static/img/country_flags/cy.png`
- `odoo/addons/base/static/img/country_flags/cz.png`
- `odoo/addons/base/static/img/country_flags/de.png`
- `odoo/addons/base/static/img/country_flags/dj.png`
- `odoo/addons/base/static/img/country_flags/dk.png`
- `odoo/addons/base/static/img/country_flags/dm.png`
- `odoo/addons/base/static/img/country_flags/do.png`
- `odoo/addons/base/static/img/country_flags/dz.png`
- `odoo/addons/base/static/img/country_flags/ec.png`
- `odoo/addons/base/static/img/country_flags/ee.png`
- Additional source files not expanded in this page: 411; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
