# Module: hr

- **Module ID:** MOD-081
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr`
- **Manifest:** `addons/hr/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Human Resources/Employees`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Centralize employee information

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 315 files, including 70 Python, 55 XML, and 79 JavaScript/TypeScript files. The manifest declares dependencies: `auth_signup`, `base_setup`, `digest`, `phone_validation`, `resource_mail`, `web_hierarchy`.

## 2. Module structure

- Model/business logic files: 34
- Controller/API files: 3
- XML/data/view/template files: 55
- Browser asset files: 79
- Security files: 2
- Test files: 28
- Scheduled/automation evidence files: 9
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr/security/ir.access.csv`, `addons/hr/security/hr_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 34 model declarations, 612 methods, 10 constraint handlers, 10 onchange handlers, and 75 dependency declarations.
- **Evidence:** `addons/hr/models/hr_employee_departure.py:9`, `addons/hr/models/res_partner.py:8`, `addons/hr/models/mail_activity.py:6`, `addons/hr/models/hr_employee_type.py:5`, `addons/hr/models/discuss_channel.py:8`, `addons/hr/models/hr_mixin.py:8`, `addons/hr/models/res_config_settings.py:4`, `addons/hr/models/hr_employee_public.py:11`, `addons/hr/models/hr_department.py:10`, `addons/hr/models/hr_work_location.py:9`, `addons/hr/models/hr_version.py:26`, `addons/hr/models/hr_employee_location.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 3 route declarations.
- **Evidence:** `addons/hr/controllers/hr_org_chart.py:36`, `addons/hr/controllers/hr_org_chart.py:42`, `addons/hr/controllers/hr_org_chart.py:78`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 55 XML files and 79 JavaScript/TypeScript files; static XML analysis found 257 record/template/menu identifiers.
- **Evidence:** `addons/hr/security/hr_security.xml:3`, `addons/hr/security/hr_security.xml:9`, `addons/hr/security/hr_security.xml:17`, `addons/hr/security/hr_security.xml:28`, `addons/hr/security/hr_security.xml:31`, `addons/hr/report/hr_employee_badge.xml:3`, `addons/hr/report/hr_employee_badge.xml:14`, `addons/hr/wizard/mail_activity_schedule_views.xml:4`, `addons/hr/wizard/hr_bank_account_allocation_wizard_line.xml:3`, `addons/hr/wizard/hr_bank_account_allocation_wizard.xml:3`, `addons/hr/wizard/hr_bank_account_allocation_wizard.xml:21`, `addons/hr/wizard/hr_employee_create_version_wizard.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/hr/security/ir.access.csv`, `addons/hr/security/hr_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 9 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/hr/__manifest__.py`, `addons/hr/models/hr_employee_departure.py`, `addons/hr/models/hr_employee.py`, `addons/hr/data/hr_data.xml`, `addons/hr/data/ir_cron_data.xml`, `addons/hr/views/hr_employee_views.xml`, `addons/hr/tests/test_hr_employee.py`, `addons/hr/tests/test_calendar_sync.py`, `addons/hr/tests/test_hr_version.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/hr/report/hr_employee_badge.xml`, `addons/hr/tests/test_multi_company.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 28 test files are present.
- **Evidence:** `addons/hr/tests/test_get_employee_working_periods.py`, `addons/hr/tests/test_resource.py`, `addons/hr/tests/test_lite_user_core.py`, `addons/hr/tests/test_hr_employee.py`, `addons/hr/tests/test_self_user_access.py`, `addons/hr/tests/test_mail_features.py`, `addons/hr/tests/test_multi_company.py`, `addons/hr/tests/test_departure.py`, `addons/hr/tests/test_multiple_bank_accounts.py`, `addons/hr/tests/test_mail_activity_plan.py`, `addons/hr/tests/test_hr_department.py`, `addons/hr/tests/test_hr_org_chart.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 55; representative identifiers: `res_groups_privilege_employees`, `group_hr_user`, `group_hr_manager`, `base.res_partner_bank_rule_user`, `base.res_partner_bank_rule_user_1`, `hr_employee_print_badge`, `print_employee_badge`, `mail_activity_schedule_view_form`, `view_bank_account_allocation_line_list`, `view_bank_account_allocation_wizard`, `action_bank_account_allocation_wizard`, `action_open_hr_employee_create_version_wizard`, `hr_employee_create_version_wizard_view_form`, `dep_administration`, `onboarding_plan`, `onboarding_setup_it_materials`, `onboarding_plan_training`, `onboarding_training`, `offboarding_plan`, `offboarding_setup_compute_out_delais`
- Menus: 19; representative evidence: `addons/hr/views/res_config_settings_views.xml:91`, `addons/hr/views/hr_views.xml:4`, `addons/hr/views/hr_views.xml:11`, `addons/hr/views/hr_views.xml:17`, `addons/hr/views/hr_views.xml:25`, `addons/hr/views/hr_views.xml:32`, `addons/hr/views/hr_views.xml:39`, `addons/hr/views/hr_views.xml:45`, `addons/hr/views/hr_views.xml:52`, `addons/hr/views/hr_views.xml:58`, `addons/hr/views/hr_views.xml:65`, `addons/hr/views/hr_views.xml:72`
- Templates: 2; representative evidence: `addons/hr/report/hr_employee_badge.xml:14`, `addons/hr/views/hr_templates.xml:3`
- View/action field declarations: 203; representative evidence: `addons/hr/report/hr_employee_badge.xml:5`, `addons/hr/wizard/mail_activity_schedule_views.xml:6`, `addons/hr/wizard/mail_activity_schedule_views.xml:8`, `addons/hr/wizard/hr_bank_account_allocation_wizard_line.xml:5`, `addons/hr/wizard/hr_bank_account_allocation_wizard_line.xml:6`, `addons/hr/wizard/hr_bank_account_allocation_wizard.xml:5`, `addons/hr/wizard/hr_bank_account_allocation_wizard.xml:6`, `addons/hr/wizard/hr_bank_account_allocation_wizard.xml:23`, `addons/hr/wizard/hr_bank_account_allocation_wizard.xml:24`, `addons/hr/wizard/hr_employee_create_version_wizard.xml:5`, `addons/hr/wizard/hr_employee_create_version_wizard.xml:6`, `addons/hr/wizard/hr_employee_create_version_wizard.xml:13`
- Browser assets: 79; representative files: `addons/hr/static/tests/m2x_avatar_employee.test.js`, `addons/hr/static/tests/profile_form_view.test.js`, `addons/hr/static/tests/hr_org_chart.test.js`, `addons/hr/static/tests/resource_calendar_form.test.js`, `addons/hr/static/tests/hr_employee_hierarchy_view.test.js`, `addons/hr/static/tests/hr_presence_status.test.js`, `addons/hr/static/tests/thread_actions.test.js`, `addons/hr/static/tests/date_dynamic_min_widget.test.js`, `addons/hr/static/tests/versions_timeline.test.js`, `addons/hr/static/tests/hr_test_helpers.js`, `addons/hr/static/src/js/DynamicMinDateTimeField.js`, `addons/hr/static/src/js/contract_template_button.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr/__manifest__.py`
- **HTTP entry points:** `addons/hr/controllers/hr_org_chart.py:36`, `addons/hr/controllers/hr_org_chart.py:42`, `addons/hr/controllers/hr_org_chart.py:78`
- **Scheduled entry points:** `addons/hr/__manifest__.py`, `addons/hr/models/hr_employee_departure.py`, `addons/hr/models/hr_employee.py`, `addons/hr/data/hr_data.xml`, `addons/hr/data/ir_cron_data.xml`, `addons/hr/views/hr_employee_views.xml`, `addons/hr/tests/test_hr_employee.py`, `addons/hr/tests/test_calendar_sync.py`, `addons/hr/tests/test_hr_version.py`
- **Report entry points:** `addons/hr/report/hr_employee_badge.xml`, `addons/hr/tests/test_multi_company.py`

## 7. Database interactions

- Model declarations: 34
- Representative model evidence: `hr.employee.departure` (addons/hr/models/hr_employee_departure.py:9); inherits `res.partner` (addons/hr/models/res_partner.py:8); inherits `mail.activity` (addons/hr/models/mail_activity.py:6); `hr.employee.type` (addons/hr/models/hr_employee_type.py:5); inherits `discuss.channel` (addons/hr/models/discuss_channel.py:8); `hr.mixin` (addons/hr/models/hr_mixin.py:8); inherits `res.config.settings` (addons/hr/models/res_config_settings.py:4); `hr.employee.public` (addons/hr/models/hr_employee_public.py:11); `hr.department` (addons/hr/models/hr_department.py:10); `hr.work.location` (addons/hr/models/hr_work_location.py:9); `hr.version` (addons/hr/models/hr_version.py:26); `hr.employee.location` (addons/hr/models/hr_employee_location.py:9); inherits `resource.calendar` (addons/hr/models/resource_calendar.py:7); inherits `mail.activity.plan` (addons/hr/models/mail_activity_plan.py:8); `hr.departure.reason` (addons/hr/models/hr_departure_reason.py:7); inherits `mail.activity.plan.template` (addons/hr/models/mail_activity_plan_template.py:8); inherits `resource.resource` (addons/hr/models/resource.py:13); `hr.job` (addons/hr/models/hr_job.py:7); inherits `mail.alias` (addons/hr/models/mail_alias.py:7); inherits `publisher_warranty.contract` (addons/hr/models/update.py:4); `hr.payroll.structure.type` (addons/hr/models/hr_payroll_structure_type.py:4); inherits `res.users` (addons/hr/models/res_users.py:89); inherits `base` (addons/hr/models/models.py:8); inherits `resource.calendar.leaves` (addons/hr/models/resource_calendar_leaves.py:9); `hr.employee.category` (addons/hr/models/hr_employee_category.py:9); inherits `res.partner.bank` (addons/hr/models/res_partner_bank.py:8); `hr.employee` (addons/hr/models/hr_employee.py:36); inherits `ir.ui.menu` (addons/hr/models/ir_ui_menu.py:6); inherits `res.company` (addons/hr/models/res_company.py:6); `hr.manager.department.report` (addons/hr/report/hr_manager_department_report.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 3
- Route evidence: `addons/hr/controllers/hr_org_chart.py:36`, `addons/hr/controllers/hr_org_chart.py:42`, `addons/hr/controllers/hr_org_chart.py:78`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `auth_signup`, `base_setup`, `digest`, `phone_validation`, `resource_mail`, `web_hierarchy`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/hr/README.md`
- `addons/hr/__init__.py`
- `addons/hr/__manifest__.py`
- `addons/hr/controllers/__init__.py`
- `addons/hr/controllers/hr_org_chart.py`
- `addons/hr/controllers/webclient.py`
- `addons/hr/data/digest_data.xml`
- `addons/hr/data/hr_data.xml`
- `addons/hr/data/hr_demo.xml`
- `addons/hr/data/hr_employee_type_data.xml`
- `addons/hr/data/ir_cron_data.xml`
- `addons/hr/data/report_paperformat.xml`
- `addons/hr/data/scenarios/hr_scenario.xml`
- `addons/hr/i18n/af.po`
- `addons/hr/i18n/am.po`
- `addons/hr/i18n/ar.po`
- `addons/hr/i18n/az.po`
- `addons/hr/i18n/bg.po`
- `addons/hr/i18n/bs.po`
- `addons/hr/i18n/ca.po`
- `addons/hr/i18n/cs.po`
- `addons/hr/i18n/da.po`
- `addons/hr/i18n/de.po`
- `addons/hr/i18n/el.po`
- `addons/hr/i18n/en_AU.po`
- `addons/hr/i18n/es.po`
- `addons/hr/i18n/es_419.po`
- `addons/hr/i18n/es_CL.po`
- `addons/hr/i18n/et.po`
- `addons/hr/i18n/eu.po`
- `addons/hr/i18n/fa.po`
- `addons/hr/i18n/fi.po`
- `addons/hr/i18n/fo.po`
- `addons/hr/i18n/fr.po`
- `addons/hr/i18n/fr_CA.po`
- `addons/hr/i18n/gl.po`
- `addons/hr/i18n/gu.po`
- `addons/hr/i18n/he.po`
- `addons/hr/i18n/hi.po`
- `addons/hr/i18n/hr.po`
- `addons/hr/i18n/hr.pot`
- `addons/hr/i18n/hu.po`
- `addons/hr/i18n/id.po`
- `addons/hr/i18n/is.po`
- `addons/hr/i18n/it.po`
- `addons/hr/i18n/ja.po`
- `addons/hr/i18n/ka.po`
- `addons/hr/i18n/kab.po`
- `addons/hr/i18n/km.po`
- `addons/hr/i18n/ko.po`
- `addons/hr/i18n/ku.po`
- `addons/hr/i18n/lb.po`
- `addons/hr/i18n/lo.po`
- `addons/hr/i18n/lt.po`
- `addons/hr/i18n/lv.po`
- `addons/hr/i18n/mk.po`
- `addons/hr/i18n/mn.po`
- `addons/hr/i18n/my.po`
- `addons/hr/i18n/nb.po`
- `addons/hr/i18n/nl.po`
- `addons/hr/i18n/pl.po`
- `addons/hr/i18n/pt.po`
- `addons/hr/i18n/pt_BR.po`
- `addons/hr/i18n/ro.po`
- `addons/hr/i18n/ru.po`
- `addons/hr/i18n/sk.po`
- `addons/hr/i18n/sl.po`
- `addons/hr/i18n/sq.po`
- `addons/hr/i18n/sr@latin.po`
- `addons/hr/i18n/sv.po`
- `addons/hr/i18n/th.po`
- `addons/hr/i18n/tr.po`
- `addons/hr/i18n/uk.po`
- `addons/hr/i18n/uz.po`
- `addons/hr/i18n/vi.po`
- `addons/hr/i18n/zh_CN.po`
- `addons/hr/i18n/zh_TW.po`
- `addons/hr/models/__init__.py`
- `addons/hr/models/discuss_channel.py`
- `addons/hr/models/hr_department.py`
- `addons/hr/models/hr_departure_reason.py`
- `addons/hr/models/hr_employee.py`
- `addons/hr/models/hr_employee_category.py`
- `addons/hr/models/hr_employee_departure.py`
- `addons/hr/models/hr_employee_location.py`
- `addons/hr/models/hr_employee_public.py`
- `addons/hr/models/hr_employee_type.py`
- `addons/hr/models/hr_job.py`
- `addons/hr/models/hr_mixin.py`
- `addons/hr/models/hr_payroll_structure_type.py`
- `addons/hr/models/hr_version.py`
- `addons/hr/models/hr_work_location.py`
- `addons/hr/models/ir_ui_menu.py`
- `addons/hr/models/mail_activity.py`
- `addons/hr/models/mail_activity_plan.py`
- `addons/hr/models/mail_activity_plan_template.py`
- `addons/hr/models/mail_alias.py`
- `addons/hr/models/models.py`
- `addons/hr/models/res_company.py`
- `addons/hr/models/res_config_settings.py`
- `addons/hr/models/res_partner.py`
- `addons/hr/models/res_partner_bank.py`
- `addons/hr/models/res_users.py`
- `addons/hr/models/resource.py`
- `addons/hr/models/resource_calendar.py`
- `addons/hr/models/resource_calendar_leaves.py`
- `addons/hr/models/update.py`
- `addons/hr/report/__init__.py`
- `addons/hr/report/hr_employee_badge.xml`
- `addons/hr/report/hr_manager_department_report.py`
- `addons/hr/security/hr_security.xml`
- `addons/hr/security/ir.access.csv`
- `addons/hr/static/description/icon.png`
- `addons/hr/static/description/icon.svg`
- `addons/hr/static/description/icon_hi.png`
- `addons/hr/static/img/employee-image.webp`
- `addons/hr/static/img/employee_admin-image.webp`
- `addons/hr/static/img/employee_al-image.webp`
- `addons/hr/static/img/employee_awa-image.webp`
- `addons/hr/static/img/employee_chs-image.webp`
- `addons/hr/static/img/employee_fme-image.webp`
- `addons/hr/static/img/employee_fpi-image.webp`
- `addons/hr/static/img/employee_han-image.webp`
- `addons/hr/static/img/employee_hne-image.webp`
- `addons/hr/static/img/employee_jep-image.webp`
- `addons/hr/static/img/employee_jgo-image.webp`
- `addons/hr/static/img/employee_jod-image.webp`
- `addons/hr/static/img/employee_jog-image.webp`
- `addons/hr/static/img/employee_jth-image.webp`
- `addons/hr/static/img/employee_jve-image.webp`
- `addons/hr/static/img/employee_lur-image.webp`
- `addons/hr/static/img/employee_md-image.webp`
- `addons/hr/static/img/employee_mit-image.webp`
- `addons/hr/static/img/employee_ngh-image.webp`
- `addons/hr/static/img/employee_niv-image.webp`
- `addons/hr/static/img/employee_qdp-image.webp`
- `addons/hr/static/img/employee_stw-image.webp`
- `addons/hr/static/img/employee_vad-image.webp`
- `addons/hr/static/src/components/background_image/background_image.js`
- `addons/hr/static/src/components/background_image/background_image.scss`
- `addons/hr/static/src/components/background_image/background_image.xml`
- `addons/hr/static/src/components/button_new_contract/button_new_contract.js`
- `addons/hr/static/src/components/button_new_contract/button_new_contract.xml`
- `addons/hr/static/src/components/contract_end_dialog/contract_end_dialog.js`
- `addons/hr/static/src/components/contract_end_dialog/contract_end_dialog.xml`
- `addons/hr/static/src/components/department_chart/department_chart.js`
- `addons/hr/static/src/components/department_chart/department_chart.scss`
- `addons/hr/static/src/components/department_chart/department_chart.xml`
- `addons/hr/static/src/components/employee_user_status/employee_user_status.js`
- `addons/hr/static/src/components/employee_user_status/employee_user_status.scss`
- `addons/hr/static/src/components/employee_user_status/employee_user_status.xml`
- `addons/hr/static/src/components/employee_user_status/user_deactivation_dialog.js`
- `addons/hr/static/src/components/employee_user_status/user_deactivation_dialog.xml`
- `addons/hr/static/src/components/float_time_selection/float_time_selection.js`
- `addons/hr/static/src/components/float_time_selection/float_time_selection.xml`
- `addons/hr/static/src/components/float_time_selection/float_time_selection_popover.js`
- `addons/hr/static/src/components/float_time_selection/float_time_selection_popover.xml`
- `addons/hr/static/src/components/float_without_trailing_zeros/float_without_trailing_zeros.js`
- `addons/hr/static/src/components/hr_presence_status/hr_presence_status.js`
- `addons/hr/static/src/components/hr_presence_status/hr_presence_status.xml`
- `addons/hr/static/src/components/hr_presence_status_private/hr_presence_status_private.js`
- `addons/hr/static/src/components/many2many_tags_salary_bank/many2many_tags_salary_bank.js`
- `addons/hr/static/src/components/resource_calendar_form/form_controller.js`
- `addons/hr/static/src/components/resource_calendar_form/resource_calendar_plugin_patch.js`
- `addons/hr/static/src/components/versions_timeline/versions_timeline.js`
- `addons/hr/static/src/components/versions_timeline/versions_timeline.scss`
- `addons/hr/static/src/components/versions_timeline/versions_timeline.xml`
- `addons/hr/static/src/core/common/@types/models.d.ts`
- `addons/hr/static/src/core/common/hr_department_model.js`
- `addons/hr/static/src/core/common/hr_employee_model.js`
- `addons/hr/static/src/core/common/hr_employee_public_model.js`
- `addons/hr/static/src/core/common/hr_employee_type_model.js`
- `addons/hr/static/src/core/common/hr_work_location_model.js`
- `addons/hr/static/src/core/common/im_status_patch.js`
- `addons/hr/static/src/core/common/res_partner_model_patch.js`
- `addons/hr/static/src/core/common/res_users_model_patch.js`
- `addons/hr/static/src/core/common/resource_resource_model_patch.js`
- `addons/hr/static/src/core/common/store_service_patch.js`
- `addons/hr/static/src/core/web/avatar_card/avatar_card_patch.js`
- `addons/hr/static/src/core/web/avatar_card/avatar_card_patch.xml`
- `addons/hr/static/src/core/web/thread_actions.js`
- `addons/hr/static/src/default_image.png`
- `addons/hr/static/src/fields/boolean_radio.js`
- `addons/hr/static/src/fields/hooks.js`
- `addons/hr/static/src/fields/hr_org_chart.js`
- `addons/hr/static/src/fields/hr_org_chart.scss`
- `addons/hr/static/src/fields/hr_org_chart.xml`
- `addons/hr/static/src/fields/optional_float_field.js`
- `addons/hr/static/src/fields/optional_float_field.xml`
- `addons/hr/static/src/fields/radio_followed_by_element.js`
- `addons/hr/static/src/img/default_image.png`
- `addons/hr/static/src/img/icons/hatched.svg`
- `addons/hr/static/src/img/icons/hatched_dark.svg`
- `addons/hr/static/src/img/icons/line.svg`
- `addons/hr/static/src/img/icons/line_dark.svg`
- `addons/hr/static/src/img/icons/plain.svg`
- `addons/hr/static/src/img/icons/plain_dark.svg`
- `addons/hr/static/src/js/DynamicMinDateTimeField.js`
- `addons/hr/static/src/js/contract_template_button.js`
- `addons/hr/static/src/js/departure_conflict_dialog.js`
- `addons/hr/static/src/scss/char_hours_popover.scss`
- `addons/hr/static/src/scss/hr.scss`
- `addons/hr/static/src/scss/res_config_settings.scss`
- `addons/hr/static/src/scss/res_users.scss`
- `addons/hr/static/src/scss/variables.scss`
- `addons/hr/static/src/search/hr_action_menus/hr_action_menus.js`
- `addons/hr/static/src/search/hr_action_menus/hr_action_menus.xml`
- `addons/hr/static/src/views/fields/employee_field_relation_mixin.js`
- `addons/hr/static/src/views/fields/many2many_avatar_employee_field/many2many_avatar_employee_field.js`
- `addons/hr/static/src/views/fields/many2one_avatar_employee_field/kanban_many2one_avatar_employee_field.js`
- `addons/hr/static/src/views/fields/many2one_avatar_employee_field/kanban_many2one_avatar_employee_field.xml`
- `addons/hr/static/src/views/fields/many2one_avatar_employee_field/many2one_avatar_employee_field.js`
- `addons/hr/static/src/views/fields/many2one_avatar_employee_field/many2one_avatar_employee_field.xml`
- `addons/hr/static/src/views/form/multi_version_update_confirmation_dialog.js`
- `addons/hr/static/src/views/form/multi_version_update_confirmation_dialog.xml`
- `addons/hr/static/src/views/form_view.js`
- `addons/hr/static/src/views/hr_employee_action_helper/hr_employee_action_helper.js`
- `addons/hr/static/src/views/hr_employee_action_helper/hr_employee_action_helper.xml`
- `addons/hr/static/src/views/hr_employee_action_helper/onboarding_helper_blocks.xml`
- `addons/hr/static/src/views/hr_employee_hierarchy/hr_employee_hierarchy_model.js`
- `addons/hr/static/src/views/hr_employee_hierarchy/hr_employee_hierarchy_renderer.js`
- `addons/hr/static/src/views/hr_employee_hierarchy/hr_employee_hierarchy_renderer.xml`
- `addons/hr/static/src/views/hr_employee_hierarchy/hr_employee_hierarchy_view.js`
- `addons/hr/static/src/views/hr_kanban_view.js`
- `addons/hr/static/src/views/hr_list_view.js`
- `addons/hr/static/src/views/preferences_form_view.js`
- `addons/hr/static/src/xml/contract_template_button.xml`
- `addons/hr/static/tests/date_dynamic_min_widget.test.js`
- `addons/hr/static/tests/hr_employee_hierarchy_view.test.js`
- `addons/hr/static/tests/hr_org_chart.test.js`
- `addons/hr/static/tests/hr_presence_status.test.js`
- `addons/hr/static/tests/hr_test_helpers.js`
- `addons/hr/static/tests/legacy/disable_patch.js`
- `addons/hr/static/tests/m2x_avatar_employee.test.js`
- `addons/hr/static/tests/mock_server/mock_models/fake_user.js`
- `addons/hr/static/tests/mock_server/mock_models/hr_department.js`
- `addons/hr/static/tests/mock_server/mock_models/hr_employee.js`
- `addons/hr/static/tests/mock_server/mock_models/hr_employee_hierarchy.js`
- `addons/hr/static/tests/mock_server/mock_models/hr_employee_public.js`
- `addons/hr/static/tests/mock_server/mock_models/hr_job.js`
- `addons/hr/static/tests/mock_server/mock_models/hr_version.js`
- `addons/hr/static/tests/mock_server/mock_models/hr_work_location.js`
- `addons/hr/static/tests/mock_server/mock_models/m2x_avatar_employee.js`
- `addons/hr/static/tests/mock_server/mock_models/res_partner.js`
- `addons/hr/static/tests/mock_server/mock_models/res_users.js`
- `addons/hr/static/tests/mock_server/mock_models/resource_resource.js`
- `addons/hr/static/tests/profile_form_view.test.js`
- `addons/hr/static/tests/resource_calendar_form.test.js`
- `addons/hr/static/tests/thread_actions.test.js`
- `addons/hr/static/tests/tours/check_public_employee_link_redirect.js`
- Additional source files not expanded in this page: 65; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
