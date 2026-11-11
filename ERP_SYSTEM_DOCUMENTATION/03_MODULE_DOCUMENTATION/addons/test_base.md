# Module: test_base

- **Module ID:** MOD-650
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `odoo/addons/test_base`
- **Manifest:** `odoo/addons/test_base/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tests`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

A module to test the ORM.

**Scope evidence:** The module contains 136 files, including 112 Python, 10 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `base`.

## 2. Module structure

- Model/business logic files: 255
- Controller/API files: 0
- XML/data/view/template files: 10
- Browser asset files: 0
- Security files: 1
- Test files: 107
- Scheduled/automation evidence files: 8
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `odoo/addons/test_base/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 255 model declarations, 1791 methods, 4 constraint handlers, 0 onchange handlers, and 103 dependency declarations.
- **Evidence:** `odoo/addons/test_base/models/test_access_rights.py:4`, `odoo/addons/test_base/models/test_access_rights.py:22`, `odoo/addons/test_base/models/test_access_rights.py:29`, `odoo/addons/test_base/models/test_access_rights.py:38`, `odoo/addons/test_base/models/test_access_rights.py:45`, `odoo/addons/test_base/models/test_access_rights.py:58`, `odoo/addons/test_base/models/test_access_rights.py:69`, `odoo/addons/test_base/models/test_read_group.py:4`, `odoo/addons/test_base/models/test_read_group.py:12`, `odoo/addons/test_base/models/test_read_group.py:23`, `odoo/addons/test_base/models/test_read_group.py:40`, `odoo/addons/test_base/models/test_read_group.py:60`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 10 XML files and 0 JavaScript/TypeScript files; static XML analysis found 68 record/template/menu identifiers.
- **Evidence:** `odoo/addons/test_base/data/test_orm_partner.xml:4`, `odoo/addons/test_base/data/test_orm_partner.xml:7`, `odoo/addons/test_base/data/test_orm_partner.xml:10`, `odoo/addons/test_base/data/test_orm_partner.xml:13`, `odoo/addons/test_base/data/test_action_bindings.xml:3`, `odoo/addons/test_base/data/test_action_bindings.xml:10`, `odoo/addons/test_base/data/test_action_bindings.xml:17`, `odoo/addons/test_base/data/test_action_bindings.xml:23`, `odoo/addons/test_base/data/test_action_bindings.xml:29`, `odoo/addons/test_base/data/test_action_bindings.xml:35`, `odoo/addons/test_base/data/test_inherits.xml:3`, `odoo/addons/test_base/data/test_inherits.xml:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `odoo/addons/test_base/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 8 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `odoo/addons/test_base/models/test_orm.py`, `odoo/addons/test_base/tests/test_modules/test_loading.py`, `odoo/addons/test_base/tests/test_tools/test_cloc.py`, `odoo/addons/test_base/tests/test_tools/test_config.py`, `odoo/addons/test_base/tests/test_orm/test_properties.py`, `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_auto/__manifest__.py`, `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_auto/models/res_currency.py`, `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_auto/data/ir_cron.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `odoo/addons/test_base/tests/test_orm/test_action_bindings.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 107 test files are present.
- **Evidence:** `odoo/addons/test_base/models/test_access_rights.py`, `odoo/addons/test_base/models/test_read_group.py`, `odoo/addons/test_base/models/test_domain_expression.py`, `odoo/addons/test_base/models/test_performance.py`, `odoo/addons/test_base/models/test_convert.py`, `odoo/addons/test_base/models/test_fields.py`, `odoo/addons/test_base/models/test_unity_read.py`, `odoo/addons/test_base/models/test_acl.py`, `odoo/addons/test_base/models/test_properties.py`, `odoo/addons/test_base/models/test_inherits.py`, `odoo/addons/test_base/models/test_schema.py`, `odoo/addons/test_base/models/test_ir_qweb_fields.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 10; representative identifiers: `test_orm_partner_1`, `test_orm_partner_2`, `test_orm_partner_3`, `test_orm_partner_4`, `act1`, `act2`, `act3`, `r1`, `r2`, `r3`, `unit_a`, `box_a`, `pallet_a`, `category_0`, `category_0_0`, `discussion_0`, `message_0_0`, `message_0_1`, `message_0_2`, `emailmessage_0_0`
- Menus: 10; representative evidence: `odoo/addons/test_base/views/test_orm_views.xml:3`, `odoo/addons/test_base/views/test_orm_views.xml:5`, `odoo/addons/test_base/views/test_orm_views.xml:12`, `odoo/addons/test_base/views/test_orm_views.xml:19`, `odoo/addons/test_base/views/test_orm_views.xml:26`, `odoo/addons/test_base/views/test_orm_views.xml:28`, `odoo/addons/test_base/views/test_orm_views.xml:35`, `odoo/addons/test_base/views/test_orm_views.xml:154`, `odoo/addons/test_base/views/test_orm_views.xml:189`, `odoo/addons/test_base/views/test_orm_views.xml:491`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 64; representative evidence: `odoo/addons/test_base/data/test_action_bindings.xml:5`, `odoo/addons/test_base/data/test_action_bindings.xml:12`, `odoo/addons/test_base/data/test_action_bindings.xml:19`, `odoo/addons/test_base/data/test_action_bindings.xml:25`, `odoo/addons/test_base/data/test_action_bindings.xml:31`, `odoo/addons/test_base/data/test_action_bindings.xml:37`, `odoo/addons/test_base/views/test_acl.xml:5`, `odoo/addons/test_base/views/test_acl.xml:6`, `odoo/addons/test_base/views/test_orm_views.xml:9`, `odoo/addons/test_base/views/test_orm_views.xml:10`, `odoo/addons/test_base/views/test_orm_views.xml:16`, `odoo/addons/test_base/views/test_orm_views.xml:17`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `odoo/addons/test_base/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `odoo/addons/test_base/models/test_orm.py`, `odoo/addons/test_base/tests/test_modules/test_loading.py`, `odoo/addons/test_base/tests/test_tools/test_cloc.py`, `odoo/addons/test_base/tests/test_tools/test_config.py`, `odoo/addons/test_base/tests/test_orm/test_properties.py`, `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_auto/__manifest__.py`, `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_auto/models/res_currency.py`, `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_auto/data/ir_cron.xml`
- **Report entry points:** `odoo/addons/test_base/tests/test_orm/test_action_bindings.py`

## 7. Database interactions

- Model declarations: 255
- Representative model evidence: `test_access_right.some_obj` (odoo/addons/test_base/models/test_access_rights.py:4); `test_access_right.container` (odoo/addons/test_base/models/test_access_rights.py:22); `test_access_right.inherits` (odoo/addons/test_base/models/test_access_rights.py:29); `test_access_right.child` (odoo/addons/test_base/models/test_access_rights.py:38); `test_access_right.obj_categ` (odoo/addons/test_base/models/test_access_rights.py:45); `test_access_right.ticket` (odoo/addons/test_base/models/test_access_rights.py:58); inherits `res.partner` (odoo/addons/test_base/models/test_access_rights.py:69); `test_read_group.on_date` (odoo/addons/test_base/models/test_read_group.py:4); `test_read_group.aggregate.boolean` (odoo/addons/test_base/models/test_read_group.py:12); `test_read_group.aggregate.monetary.related` (odoo/addons/test_base/models/test_read_group.py:23); `test_read_group.aggregate.monetary` (odoo/addons/test_base/models/test_read_group.py:40); `test_read_group.aggregate` (odoo/addons/test_base/models/test_read_group.py:60); `test_read_group.partner` (odoo/addons/test_base/models/test_read_group.py:72); `test_read_group.on_selection` (odoo/addons/test_base/models/test_read_group.py:84); `test_read_group.fill_temporal` (odoo/addons/test_base/models/test_read_group.py:99); `test_read_group.order` (odoo/addons/test_base/models/test_read_group.py:108); `test_read_group.order.line` (odoo/addons/test_base/models/test_read_group.py:126); `test_read_group.null.order` (odoo/addons/test_base/models/test_read_group.py:136); `test_read_group.null.order.line` (odoo/addons/test_base/models/test_read_group.py:145); `test_read_group.user` (odoo/addons/test_base/models/test_read_group.py:152); `test_read_group.task` (odoo/addons/test_base/models/test_read_group.py:166); `test_read_group.tag` (odoo/addons/test_base/models/test_read_group.py:213); `test_read_group.related_bar` (odoo/addons/test_base/models/test_read_group.py:221); `test_read_group.related_foo` (odoo/addons/test_base/models/test_read_group.py:237); `test_read_group.related_base` (odoo/addons/test_base/models/test_read_group.py:252); `test_read_group.related_inherits` (odoo/addons/test_base/models/test_read_group.py:268); `test_read_group.chain_inherits` (odoo/addons/test_base/models/test_read_group.py:278); `test_orm.domain_expression.partner` (odoo/addons/test_base/models/test_domain_expression.py:12); `test_orm.domain_expression.partner.bank` (odoo/addons/test_base/models/test_domain_expression.py:45); `test_orm.domain_expression.country` (odoo/addons/test_base/models/test_domain_expression.py:67)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`
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

- `odoo/addons/test_base/__init__.py`
- `odoo/addons/test_base/__manifest__.py`
- `odoo/addons/test_base/data/test_access_rights_data.xml`
- `odoo/addons/test_base/data/test_action_bindings.xml`
- `odoo/addons/test_base/data/test_inherits.xml`
- `odoo/addons/test_base/data/test_orm_data.xml`
- `odoo/addons/test_base/data/test_orm_partner.xml`
- `odoo/addons/test_base/data/test_translated_field/test_model_data.xml`
- `odoo/addons/test_base/data/test_translated_field/test_tools.convert.csv`
- `odoo/addons/test_base/i18n/fr.po`
- `odoo/addons/test_base/models/__init__.py`
- `odoo/addons/test_base/models/common.py`
- `odoo/addons/test_base/models/models_translation.py`
- `odoo/addons/test_base/models/test_access_rights.py`
- `odoo/addons/test_base/models/test_acl.py`
- `odoo/addons/test_base/models/test_action_bindings.py`
- `odoo/addons/test_base/models/test_config.py`
- `odoo/addons/test_base/models/test_convert.py`
- `odoo/addons/test_base/models/test_domain_expression.py`
- `odoo/addons/test_base/models/test_fields.py`
- `odoo/addons/test_base/models/test_inherits.py`
- `odoo/addons/test_base/models/test_ir_qweb_fields.py`
- `odoo/addons/test_base/models/test_orm.py`
- `odoo/addons/test_base/models/test_performance.py`
- `odoo/addons/test_base/models/test_properties.py`
- `odoo/addons/test_base/models/test_read_group.py`
- `odoo/addons/test_base/models/test_schema.py`
- `odoo/addons/test_base/models/test_search.py`
- `odoo/addons/test_base/models/test_tools.py`
- `odoo/addons/test_base/models/test_unity_read.py`
- `odoo/addons/test_base/security/ir.access.csv`
- `odoo/addons/test_base/test_file.txt`
- `odoo/addons/test_base/tests/__init__.py`
- `odoo/addons/test_base/tests/test_core/__init__.py`
- `odoo/addons/test_base/tests/test_core/shell_file.txt`
- `odoo/addons/test_base/tests/test_core/test_cli.py`
- `odoo/addons/test_base/tests/test_core/test_core_init.py`
- `odoo/addons/test_base/tests/test_core/test_monkeypatch_lxml.py`
- `odoo/addons/test_base/tests/test_core/test_monkeypatch_num2words.py`
- `odoo/addons/test_base/tests/test_core/test_monkeypatch_num2words_es.py`
- `odoo/addons/test_base/tests/test_core/test_monkeypatch_zoneinfo.py`
- `odoo/addons/test_base/tests/test_modules/__init__.py`
- `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_auto/__init__.py`
- `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_auto/__manifest__.py`
- `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_auto/data/ir_cron.xml`
- `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_auto/models/__init__.py`
- `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_auto/models/res_currency.py`
- `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_base/__init__.py`
- `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_base/__manifest__.py`
- `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_fail/__init__.py`
- `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_fail/__manifest__.py`
- `odoo/addons/test_base/tests/test_modules/test_install_addons/test_install_fail/views/res_currency_views.xml`
- `odoo/addons/test_base/tests/test_modules/test_install_addons/test_isolated_install.md`
- `odoo/addons/test_base/tests/test_modules/test_loading.py`
- `odoo/addons/test_base/tests/test_modules/test_manifest.py`
- `odoo/addons/test_base/tests/test_modules/test_module_graph.py`
- `odoo/addons/test_base/tests/test_modules/test_neutralize.py`
- `odoo/addons/test_base/tests/test_orm/__init__.py`
- `odoo/addons/test_base/tests/test_orm/common.py`
- `odoo/addons/test_base/tests/test_orm/test_access.py`
- `odoo/addons/test_base/tests/test_orm/test_access_feedback.py`
- `odoo/addons/test_base/tests/test_orm/test_access_monetary_related.py`
- `odoo/addons/test_base/tests/test_orm/test_acl.py`
- `odoo/addons/test_base/tests/test_orm/test_action_bindings.py`
- `odoo/addons/test_base/tests/test_orm/test_all_models.py`
- `odoo/addons/test_base/tests/test_orm/test_autovacuum.py`
- `odoo/addons/test_base/tests/test_orm/test_cache.py`
- `odoo/addons/test_base/tests/test_orm/test_check_access.py`
- `odoo/addons/test_base/tests/test_orm/test_company_checks.py`
- `odoo/addons/test_base/tests/test_orm/test_config_settings.py`
- `odoo/addons/test_base/tests/test_orm/test_copy.py`
- `odoo/addons/test_base/tests/test_orm/test_create.py`
- `odoo/addons/test_base/tests/test_orm/test_domain.py`
- `odoo/addons/test_base/tests/test_orm/test_domain_expression.py`
- `odoo/addons/test_base/tests/test_orm/test_fields.py`
- `odoo/addons/test_base/tests/test_orm/test_index_method.py`
- `odoo/addons/test_base/tests/test_orm/test_indexed_translation.py`
- `odoo/addons/test_base/tests/test_orm/test_inherits.py`
- `odoo/addons/test_base/tests/test_orm/test_ir_qweb_fields.py`
- `odoo/addons/test_base/tests/test_orm/test_ir_rules.py`
- `odoo/addons/test_base/tests/test_orm/test_json_field.py`
- `odoo/addons/test_base/tests/test_orm/test_many2many.py`
- `odoo/addons/test_base/tests/test_orm/test_models.py`
- `odoo/addons/test_base/tests/test_orm/test_modules_db.py`
- `odoo/addons/test_base/tests/test_orm/test_one2many.py`
- `odoo/addons/test_base/tests/test_orm/test_parent_store.py`
- `odoo/addons/test_base/tests/test_orm/test_performance.py`
- `odoo/addons/test_base/tests/test_orm/test_prefetch.py`
- `odoo/addons/test_base/tests/test_orm/test_properties.py`
- `odoo/addons/test_base/tests/test_orm/test_query.py`
- `odoo/addons/test_base/tests/test_orm/test_read_group_override.py`
- `odoo/addons/test_base/tests/test_orm/test_read_group_private.py`
- `odoo/addons/test_base/tests/test_orm/test_read_grouping_sets.py`
- `odoo/addons/test_base/tests/test_orm/test_registry.py`
- `odoo/addons/test_base/tests/test_orm/test_registry_signaling.py`
- `odoo/addons/test_base/tests/test_orm/test_schema.py`
- `odoo/addons/test_base/tests/test_orm/test_search.py`
- `odoo/addons/test_base/tests/test_orm/test_search_order.py`
- `odoo/addons/test_base/tests/test_orm/test_sort.py`
- `odoo/addons/test_base/tests/test_orm/test_timeit.py`
- `odoo/addons/test_base/tests/test_orm/test_transactions.py`
- `odoo/addons/test_base/tests/test_orm/test_uninstall.py`
- `odoo/addons/test_base/tests/test_orm/test_views.py`
- `odoo/addons/test_base/tests/test_tools/__init__.py`
- `odoo/addons/test_base/tests/test_tools/config/16.0.conf`
- `odoo/addons/test_base/tests/test_tools/config/cli`
- `odoo/addons/test_base/tests/test_tools/config/empty.conf`
- `odoo/addons/test_base/tests/test_tools/config/environ`
- `odoo/addons/test_base/tests/test_tools/config/multidb.conf`
- `odoo/addons/test_base/tests/test_tools/config/non_default.conf`
- `odoo/addons/test_base/tests/test_tools/config/save_posix.conf`
- `odoo/addons/test_base/tests/test_tools/config/sysloglogfile.conf`
- `odoo/addons/test_base/tests/test_tools/test_barcode.py`
- `odoo/addons/test_base/tests/test_tools/test_binary.py`
- `odoo/addons/test_base/tests/test_tools/test_cloc.py`
- `odoo/addons/test_base/tests/test_tools/test_config.py`
- `odoo/addons/test_base/tests/test_tools/test_convert.py`
- `odoo/addons/test_base/tests/test_tools/test_date_utils.py`
- `odoo/addons/test_base/tests/test_tools/test_float_utils.py`
- `odoo/addons/test_base/tests/test_tools/test_func.py`
- `odoo/addons/test_base/tests/test_tools/test_i18n.py`
- `odoo/addons/test_base/tests/test_tools/test_image.py`
- `odoo/addons/test_base/tests/test_tools/test_intervals.py`
- `odoo/addons/test_base/tests/test_tools/test_mail.py`
- `odoo/addons/test_base/tests/test_tools/test_mimetypes.py`
- `odoo/addons/test_base/tests/test_tools/test_misc.py`
- `odoo/addons/test_base/tests/test_tools/test_pdf.py`
- `odoo/addons/test_base/tests/test_tools/test_profiler.py`
- `odoo/addons/test_base/tests/test_tools/test_safe_eval.py`
- `odoo/addons/test_base/tests/test_tools/test_safe_eval_expr.py`
- `odoo/addons/test_base/tests/test_tools/test_set_expression.py`
- `odoo/addons/test_base/tests/test_tools/test_sql.py`
- `odoo/addons/test_base/tests/test_tools/test_translate.py`
- `odoo/addons/test_base/tests/test_tools/test_xml_utils.py`
- `odoo/addons/test_base/views/test_acl.xml`
- `odoo/addons/test_base/views/test_orm_views.xml`
