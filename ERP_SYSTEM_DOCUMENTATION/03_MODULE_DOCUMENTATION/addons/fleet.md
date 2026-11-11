# Module: fleet

- **Module ID:** MOD-072
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/fleet`
- **Manifest:** `addons/fleet/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Human Resources/Fleet`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Manage your fleet and track car costs

**Manifest description:**

Vehicle, leasing, insurances, cost
==================================
With this module, Odoo helps you managing all your vehicles, the
contracts associated to those vehicle as well as services, costs
and many other features necessary to the management of your fleet
of vehicle(s)

Main Features
-------------
* Add vehicles to your fleet
* Manage contracts for vehicles
* Reminder when a contract reach its expiration date
* Add services, odometer values for all vehicles
* Show all costs associated to a vehicle or to a type of service
* Analysis graph for costs

**Scope evidence:** The module contains 182 files, including 30 Python, 15 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `mail`.

## 2. Module structure

- Model/business logic files: 17
- Controller/API files: 0
- XML/data/view/template files: 15
- Browser asset files: 2
- Security files: 2
- Test files: 8
- Scheduled/automation evidence files: 2
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/fleet/security/ir.access.csv`, `addons/fleet/security/fleet_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 17 model declarations, 100 methods, 0 constraint handlers, 2 onchange handlers, and 28 dependency declarations.
- **Evidence:** `addons/fleet/models/res_partner.py:6`, `addons/fleet/models/fleet_vehicle_model.py:22`, `addons/fleet/models/fleet_vehicle_tag.py:7`, `addons/fleet/models/res_config_settings.py:7`, `addons/fleet/models/fleet_vehicle_state.py:7`, `addons/fleet/models/fleet_vehicle_log_services.py:8`, `addons/fleet/models/fleet_service_type.py:7`, `addons/fleet/models/fleet_vehicle_assignation_log.py:7`, `addons/fleet/models/fleet_vehicle_model_category.py:7`, `addons/fleet/models/mail_activity_type.py:4`, `addons/fleet/models/fleet_vehicle_model_brand.py:7`, `addons/fleet/models/fleet_vehicle_odometer.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 15 XML files and 2 JavaScript/TypeScript files; static XML analysis found 325 record/template/menu identifiers.
- **Evidence:** `addons/fleet/security/fleet_security.xml:2`, `addons/fleet/security/fleet_security.xml:7`, `addons/fleet/security/fleet_security.xml:13`, `addons/fleet/wizard/fleet_vehicle_send_mail_views.xml:3`, `addons/fleet/data/fleet_data.xml:4`, `addons/fleet/data/fleet_data.xml:14`, `addons/fleet/data/fleet_data.xml:19`, `addons/fleet/data/fleet_data.xml:24`, `addons/fleet/data/fleet_data.xml:29`, `addons/fleet/data/fleet_data.xml:34`, `addons/fleet/data/fleet_data.xml:39`, `addons/fleet/data/mail_activity_type_data.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/fleet/security/ir.access.csv`, `addons/fleet/security/fleet_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/fleet/data/fleet_data.xml`, `addons/fleet/views/fleet_vehicle_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 8 test files are present.
- **Evidence:** `addons/fleet/tests/test_access_rights.py`, `addons/fleet/tests/test_plan_to_change.py`, `addons/fleet/tests/test_send_mail.py`, `addons/fleet/tests/test_vehicle_model_fields.py`, `addons/fleet/tests/test_fleet_ui.py`, `addons/fleet/tests/test_overdue.py`, `addons/fleet/tests/__init__.py`, `addons/fleet/tests/test_unique_license_plate.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 15; representative identifiers: `res_groups_privilege_fleet`, `fleet_group_user`, `fleet_group_manager`, `fleet_vehicle_send_mail_view_form`, `ir_cron_contract_costs_generator`, `fleet_vehicle_state_new_request`, `fleet_vehicle_state_to_order`, `fleet_vehicle_state_registered`, `fleet_vehicle_state_downgraded`, `type_contract_omnium`, `type_contract_leasing`, `mail_act_fleet_contract_to_renew`, `base.user_demo`, `base.default_user_group`, `fleet_vehicle_state_ordered`, `fleet_vehicle_state_reserve`, `fleet_vehicle_state_waiting_list`, `type_service_service_1`, `type_service_service_2`, `type_service_service_3`
- Menus: 23; representative evidence: `addons/fleet/views/fleet_vehicle_cost_views.xml:224`, `addons/fleet/views/fleet_vehicle_cost_views.xml:410`, `addons/fleet/views/fleet_board_view.xml:107`, `addons/fleet/views/fleet_board_view.xml:108`, `addons/fleet/views/fleet_vehicle_views.xml:376`, `addons/fleet/views/fleet_vehicle_views.xml:377`, `addons/fleet/views/fleet_vehicle_views.xml:446`, `addons/fleet/views/fleet_vehicle_views.xml:505`, `addons/fleet/views/fleet_vehicle_views.xml:506`, `addons/fleet/views/fleet_vehicle_views.xml:523`, `addons/fleet/views/fleet_vehicle_views.xml:524`, `addons/fleet/views/fleet_vehicle_views.xml:569`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 137; representative evidence: `addons/fleet/wizard/fleet_vehicle_send_mail_views.xml:4`, `addons/fleet/wizard/fleet_vehicle_send_mail_views.xml:5`, `addons/fleet/data/mail_activity_type_data.xml:8`, `addons/fleet/data/mail_message_subtype_data.xml:7`, `addons/fleet/views/fleet_vehicle_cost_views.xml:5`, `addons/fleet/views/fleet_vehicle_cost_views.xml:6`, `addons/fleet/views/fleet_vehicle_cost_views.xml:83`, `addons/fleet/views/fleet_vehicle_cost_views.xml:84`, `addons/fleet/views/fleet_vehicle_cost_views.xml:113`, `addons/fleet/views/fleet_vehicle_cost_views.xml:114`, `addons/fleet/views/fleet_vehicle_cost_views.xml:134`, `addons/fleet/views/fleet_vehicle_cost_views.xml:135`
- Browser assets: 2; representative files: `addons/fleet/static/src/js/fleet_form.js`, `addons/fleet/static/tests/tours/fleet_manager_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/fleet/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/fleet/data/fleet_data.xml`, `addons/fleet/views/fleet_vehicle_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 17
- Representative model evidence: inherits `res.partner` (addons/fleet/models/res_partner.py:6); `fleet.vehicle.model` (addons/fleet/models/fleet_vehicle_model.py:22); `fleet.vehicle.tag` (addons/fleet/models/fleet_vehicle_tag.py:7); inherits `res.config.settings` (addons/fleet/models/res_config_settings.py:7); `fleet.vehicle.state` (addons/fleet/models/fleet_vehicle_state.py:7); `fleet.vehicle.log.services` (addons/fleet/models/fleet_vehicle_log_services.py:8); `fleet.service.type` (addons/fleet/models/fleet_service_type.py:7); `fleet.vehicle.assignation.log` (addons/fleet/models/fleet_vehicle_assignation_log.py:7); `fleet.vehicle.model.category` (addons/fleet/models/fleet_vehicle_model_category.py:7); inherits `mail.activity.type` (addons/fleet/models/mail_activity_type.py:4); `fleet.vehicle.model.brand` (addons/fleet/models/fleet_vehicle_model_brand.py:7); `fleet.vehicle.odometer` (addons/fleet/models/fleet_vehicle_odometer.py:7); `fleet.vehicle.log.contract` (addons/fleet/models/fleet_vehicle_log_contract.py:9); `fleet.vehicle` (addons/fleet/models/fleet_vehicle.py:23); `fleet.vehicle.odometer.report` (addons/fleet/report/odometer_report.py:7); `fleet.vehicle.cost.report` (addons/fleet/report/fleet_report.py:8); `fleet.vehicle.send.mail` (addons/fleet/wizard/fleet_vehicle_send_mail.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `mail`
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

- `addons/fleet/__init__.py`
- `addons/fleet/__manifest__.py`
- `addons/fleet/data/fleet_cars_data.xml`
- `addons/fleet/data/fleet_data.xml`
- `addons/fleet/data/fleet_demo.xml`
- `addons/fleet/data/mail_activity_type_data.xml`
- `addons/fleet/data/mail_message_subtype_data.xml`
- `addons/fleet/i18n/af.po`
- `addons/fleet/i18n/am.po`
- `addons/fleet/i18n/ar.po`
- `addons/fleet/i18n/az.po`
- `addons/fleet/i18n/bg.po`
- `addons/fleet/i18n/bs.po`
- `addons/fleet/i18n/ca.po`
- `addons/fleet/i18n/cs.po`
- `addons/fleet/i18n/da.po`
- `addons/fleet/i18n/de.po`
- `addons/fleet/i18n/el.po`
- `addons/fleet/i18n/es.po`
- `addons/fleet/i18n/es_419.po`
- `addons/fleet/i18n/es_CL.po`
- `addons/fleet/i18n/et.po`
- `addons/fleet/i18n/eu.po`
- `addons/fleet/i18n/fa.po`
- `addons/fleet/i18n/fi.po`
- `addons/fleet/i18n/fleet.pot`
- `addons/fleet/i18n/fo.po`
- `addons/fleet/i18n/fr.po`
- `addons/fleet/i18n/fr_CA.po`
- `addons/fleet/i18n/gl.po`
- `addons/fleet/i18n/gu.po`
- `addons/fleet/i18n/he.po`
- `addons/fleet/i18n/hi.po`
- `addons/fleet/i18n/hr.po`
- `addons/fleet/i18n/hu.po`
- `addons/fleet/i18n/id.po`
- `addons/fleet/i18n/is.po`
- `addons/fleet/i18n/it.po`
- `addons/fleet/i18n/ja.po`
- `addons/fleet/i18n/ka.po`
- `addons/fleet/i18n/kab.po`
- `addons/fleet/i18n/km.po`
- `addons/fleet/i18n/ko.po`
- `addons/fleet/i18n/ku.po`
- `addons/fleet/i18n/lb.po`
- `addons/fleet/i18n/lo.po`
- `addons/fleet/i18n/lt.po`
- `addons/fleet/i18n/lv.po`
- `addons/fleet/i18n/mk.po`
- `addons/fleet/i18n/mn.po`
- `addons/fleet/i18n/my.po`
- `addons/fleet/i18n/nb.po`
- `addons/fleet/i18n/nl.po`
- `addons/fleet/i18n/pl.po`
- `addons/fleet/i18n/pt.po`
- `addons/fleet/i18n/pt_BR.po`
- `addons/fleet/i18n/ro.po`
- `addons/fleet/i18n/ru.po`
- `addons/fleet/i18n/sk.po`
- `addons/fleet/i18n/sl.po`
- `addons/fleet/i18n/sq.po`
- `addons/fleet/i18n/sr@latin.po`
- `addons/fleet/i18n/sv.po`
- `addons/fleet/i18n/th.po`
- `addons/fleet/i18n/tr.po`
- `addons/fleet/i18n/uk.po`
- `addons/fleet/i18n/uz.po`
- `addons/fleet/i18n/vi.po`
- `addons/fleet/i18n/zh_CN.po`
- `addons/fleet/i18n/zh_TW.po`
- `addons/fleet/models/__init__.py`
- `addons/fleet/models/fleet_service_type.py`
- `addons/fleet/models/fleet_vehicle.py`
- `addons/fleet/models/fleet_vehicle_assignation_log.py`
- `addons/fleet/models/fleet_vehicle_log_contract.py`
- `addons/fleet/models/fleet_vehicle_log_services.py`
- `addons/fleet/models/fleet_vehicle_model.py`
- `addons/fleet/models/fleet_vehicle_model_brand.py`
- `addons/fleet/models/fleet_vehicle_model_category.py`
- `addons/fleet/models/fleet_vehicle_odometer.py`
- `addons/fleet/models/fleet_vehicle_state.py`
- `addons/fleet/models/fleet_vehicle_tag.py`
- `addons/fleet/models/mail_activity_type.py`
- `addons/fleet/models/res_config_settings.py`
- `addons/fleet/models/res_partner.py`
- `addons/fleet/report/__init__.py`
- `addons/fleet/report/fleet_report.py`
- `addons/fleet/report/odometer_report.py`
- `addons/fleet/security/fleet_security.xml`
- `addons/fleet/security/ir.access.csv`
- `addons/fleet/static/description/icon.png`
- `addons/fleet/static/description/icon.svg`
- `addons/fleet/static/description/icon_hi.png`
- `addons/fleet/static/img/brand_abarth-image.png`
- `addons/fleet/static/img/brand_acura-image.png`
- `addons/fleet/static/img/brand_alfa-image.png`
- `addons/fleet/static/img/brand_audi-image.png`
- `addons/fleet/static/img/brand_austin-image.png`
- `addons/fleet/static/img/brand_bentley-image.png`
- `addons/fleet/static/img/brand_bmw-image.png`
- `addons/fleet/static/img/brand_bugatti-image.png`
- `addons/fleet/static/img/brand_buick-image.png`
- `addons/fleet/static/img/brand_byd-image.png`
- `addons/fleet/static/img/brand_cadillac-image.png`
- `addons/fleet/static/img/brand_chevrolet-image.png`
- `addons/fleet/static/img/brand_chrysler-image.png`
- `addons/fleet/static/img/brand_citroen-image.png`
- `addons/fleet/static/img/brand_corre-la-licorne-image.png`
- `addons/fleet/static/img/brand_daewoo-image.png`
- `addons/fleet/static/img/brand_dodge-image.png`
- `addons/fleet/static/img/brand_ferrari-image.png`
- `addons/fleet/static/img/brand_fiat-image.png`
- `addons/fleet/static/img/brand_ford-image.png`
- `addons/fleet/static/img/brand_gmc-image.png`
- `addons/fleet/static/img/brand_holden-image.png`
- `addons/fleet/static/img/brand_honda-image.png`
- `addons/fleet/static/img/brand_hyundai-image.png`
- `addons/fleet/static/img/brand_infiniti-image.png`
- `addons/fleet/static/img/brand_isuzu-image.png`
- `addons/fleet/static/img/brand_jaguar-image.png`
- `addons/fleet/static/img/brand_jeep-image.png`
- `addons/fleet/static/img/brand_kia-image.png`
- `addons/fleet/static/img/brand_koenigsegg-image.png`
- `addons/fleet/static/img/brand_lagonda-image.png`
- `addons/fleet/static/img/brand_lamborghini-image.png`
- `addons/fleet/static/img/brand_lancia-image.png`
- `addons/fleet/static/img/brand_land-rover-image.png`
- `addons/fleet/static/img/brand_lexus-image.png`
- `addons/fleet/static/img/brand_lincoln-image.png`
- `addons/fleet/static/img/brand_lotus-image.png`
- `addons/fleet/static/img/brand_maserati-image.png`
- `addons/fleet/static/img/brand_maybach-image.png`
- `addons/fleet/static/img/brand_mazda-image.png`
- `addons/fleet/static/img/brand_mercedes-image.png`
- `addons/fleet/static/img/brand_mg-image.png`
- `addons/fleet/static/img/brand_mini-image.png`
- `addons/fleet/static/img/brand_mitsubishi-image.png`
- `addons/fleet/static/img/brand_morgan-image.png`
- `addons/fleet/static/img/brand_nissan-image.png`
- `addons/fleet/static/img/brand_oldsmobile-image.png`
- `addons/fleet/static/img/brand_opel-image.png`
- `addons/fleet/static/img/brand_peugeot-image.png`
- `addons/fleet/static/img/brand_pontiac-image.png`
- `addons/fleet/static/img/brand_porsche-image.png`
- `addons/fleet/static/img/brand_rambler-image.png`
- `addons/fleet/static/img/brand_renault-image.png`
- `addons/fleet/static/img/brand_rolls-royce-image.png`
- `addons/fleet/static/img/brand_saab-image.png`
- `addons/fleet/static/img/brand_scion-image.png`
- `addons/fleet/static/img/brand_skoda-image.png`
- `addons/fleet/static/img/brand_smart-image.png`
- `addons/fleet/static/img/brand_steyr-image.png`
- `addons/fleet/static/img/brand_subaru-image.png`
- `addons/fleet/static/img/brand_suzuki-image.png`
- `addons/fleet/static/img/brand_tesla-motors-image.png`
- `addons/fleet/static/img/brand_toyota-image.png`
- `addons/fleet/static/img/brand_trabant-image.png`
- `addons/fleet/static/img/brand_volkswagen-image.png`
- `addons/fleet/static/img/brand_volvo-image.png`
- `addons/fleet/static/img/brand_willys-image.png`
- `addons/fleet/static/src/js/fleet_form.js`
- `addons/fleet/static/src/scss/fleet_form.scss`
- `addons/fleet/static/tests/tours/fleet_manager_tour.js`
- `addons/fleet/tests/__init__.py`
- `addons/fleet/tests/test_access_rights.py`
- `addons/fleet/tests/test_fleet_ui.py`
- `addons/fleet/tests/test_overdue.py`
- `addons/fleet/tests/test_plan_to_change.py`
- `addons/fleet/tests/test_send_mail.py`
- `addons/fleet/tests/test_unique_license_plate.py`
- `addons/fleet/tests/test_vehicle_model_fields.py`
- `addons/fleet/views/fleet_board_view.xml`
- `addons/fleet/views/fleet_vehicle_cost_views.xml`
- `addons/fleet/views/fleet_vehicle_model_views.xml`
- `addons/fleet/views/fleet_vehicle_odometer_report.xml`
- `addons/fleet/views/fleet_vehicle_views.xml`
- `addons/fleet/views/mail_activity_views.xml`
- `addons/fleet/views/res_config_settings_views.xml`
- `addons/fleet/views/res_partner_views.xml`
- `addons/fleet/wizard/__init__.py`
- `addons/fleet/wizard/fleet_vehicle_send_mail.py`
- `addons/fleet/wizard/fleet_vehicle_send_mail_views.xml`
