# Module: spreadsheet

- **Module ID:** MOD-544
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/spreadsheet`
- **Manifest:** `addons/spreadsheet/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Productivity/Dashboard`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Spreadsheet

**Manifest description:**

Spreadsheet

**Scope evidence:** The module contains 257 files, including 24 Python, 13 XML, and 152 JavaScript/TypeScript files. The manifest declares dependencies: `bus`, `web`, `portal`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 2
- XML/data/view/template files: 13
- Browser asset files: 152
- Security files: 0
- Test files: 8
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 51 methods, 1 constraint handlers, 1 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/spreadsheet/models/res_lang.py:11`, `addons/spreadsheet/models/res_currency_rate.py:5`, `addons/spreadsheet/models/res_currency.py:4`, `addons/spreadsheet/models/ir_model.py:6`, `addons/spreadsheet/models/spreadsheet_mixin.py:20`, `addons/spreadsheet/models/ir_http.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/spreadsheet/controllers/main.py:12`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 13 XML files and 152 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/spreadsheet/views/public_readonly_spreadsheet_templates.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 8 test files are present.
- **Evidence:** `addons/spreadsheet/tests/test_ir_model.py`, `addons/spreadsheet/tests/test_currency.py`, `addons/spreadsheet/tests/test_currency_rate.py`, `addons/spreadsheet/tests/test_locale.py`, `addons/spreadsheet/tests/test_session_info.py`, `addons/spreadsheet/tests/test_utils.py`, `addons/spreadsheet/tests/test_display_names.py`, `addons/spreadsheet/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 13; representative identifiers: `Public spreadsheet layout`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/spreadsheet/views/public_readonly_spreadsheet_templates.xml:4`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 152; representative files: `addons/spreadsheet/static/lib/chart_js_treemap.js`, `addons/spreadsheet/static/src/command_provider.js`, `addons/spreadsheet/static/src/command_palette.js`, `addons/spreadsheet/static/src/index.js`, `addons/spreadsheet/static/src/hooks.js`, `addons/spreadsheet/static/src/model.js`, `addons/spreadsheet/static/src/plugins.js`, `addons/spreadsheet/static/src/server_data_plugin.js`, `addons/spreadsheet/static/tests/command_palette.test.js`, `addons/spreadsheet/static/tests/hoot_override.js`, `addons/spreadsheet/static/tests/logging_ui_plugin.test.js`, `addons/spreadsheet/static/lib/chartjs-chart-geo/chartjs-chart-geo.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/spreadsheet/__manifest__.py`
- **HTTP entry points:** `addons/spreadsheet/controllers/main.py:12`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `res.lang` (addons/spreadsheet/models/res_lang.py:11); inherits `res.currency.rate` (addons/spreadsheet/models/res_currency_rate.py:5); inherits `res.currency` (addons/spreadsheet/models/res_currency.py:4); inherits `ir.model` (addons/spreadsheet/models/ir_model.py:6); `spreadsheet.mixin` (addons/spreadsheet/models/spreadsheet_mixin.py:20); inherits `ir.http` (addons/spreadsheet/models/ir_http.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/spreadsheet/controllers/main.py:12`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `bus`, `web`, `portal`
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

- `addons/spreadsheet/__init__.py`
- `addons/spreadsheet/__manifest__.py`
- `addons/spreadsheet/controllers/__init__.py`
- `addons/spreadsheet/controllers/main.py`
- `addons/spreadsheet/i18n/ar.po`
- `addons/spreadsheet/i18n/az.po`
- `addons/spreadsheet/i18n/bg.po`
- `addons/spreadsheet/i18n/bs.po`
- `addons/spreadsheet/i18n/ca.po`
- `addons/spreadsheet/i18n/cs.po`
- `addons/spreadsheet/i18n/da.po`
- `addons/spreadsheet/i18n/de.po`
- `addons/spreadsheet/i18n/el.po`
- `addons/spreadsheet/i18n/es.po`
- `addons/spreadsheet/i18n/es_419.po`
- `addons/spreadsheet/i18n/et.po`
- `addons/spreadsheet/i18n/fa.po`
- `addons/spreadsheet/i18n/fi.po`
- `addons/spreadsheet/i18n/fr.po`
- `addons/spreadsheet/i18n/he.po`
- `addons/spreadsheet/i18n/hi.po`
- `addons/spreadsheet/i18n/hr.po`
- `addons/spreadsheet/i18n/hu.po`
- `addons/spreadsheet/i18n/id.po`
- `addons/spreadsheet/i18n/it.po`
- `addons/spreadsheet/i18n/ja.po`
- `addons/spreadsheet/i18n/kab.po`
- `addons/spreadsheet/i18n/ko.po`
- `addons/spreadsheet/i18n/ku.po`
- `addons/spreadsheet/i18n/lo.po`
- `addons/spreadsheet/i18n/lt.po`
- `addons/spreadsheet/i18n/lv.po`
- `addons/spreadsheet/i18n/mn.po`
- `addons/spreadsheet/i18n/my.po`
- `addons/spreadsheet/i18n/nb.po`
- `addons/spreadsheet/i18n/nl.po`
- `addons/spreadsheet/i18n/pl.po`
- `addons/spreadsheet/i18n/pt.po`
- `addons/spreadsheet/i18n/pt_BR.po`
- `addons/spreadsheet/i18n/ro.po`
- `addons/spreadsheet/i18n/ru.po`
- `addons/spreadsheet/i18n/sk.po`
- `addons/spreadsheet/i18n/sl.po`
- `addons/spreadsheet/i18n/spreadsheet.pot`
- `addons/spreadsheet/i18n/sr@latin.po`
- `addons/spreadsheet/i18n/sv.po`
- `addons/spreadsheet/i18n/th.po`
- `addons/spreadsheet/i18n/tr.po`
- `addons/spreadsheet/i18n/uk.po`
- `addons/spreadsheet/i18n/uz.po`
- `addons/spreadsheet/i18n/vi.po`
- `addons/spreadsheet/i18n/zh_CN.po`
- `addons/spreadsheet/i18n/zh_TW.po`
- `addons/spreadsheet/models/__init__.py`
- `addons/spreadsheet/models/ir_http.py`
- `addons/spreadsheet/models/ir_model.py`
- `addons/spreadsheet/models/res_currency.py`
- `addons/spreadsheet/models/res_currency_rate.py`
- `addons/spreadsheet/models/res_lang.py`
- `addons/spreadsheet/models/spreadsheet_mixin.py`
- `addons/spreadsheet/static/description/icon.png`
- `addons/spreadsheet/static/description/icon.svg`
- `addons/spreadsheet/static/description/icon_hi.png`
- `addons/spreadsheet/static/img/spreadsheet.svg`
- `addons/spreadsheet/static/lib/chart_js_treemap.js`
- `addons/spreadsheet/static/lib/chartjs-chart-geo/chartjs-chart-geo.js`
- `addons/spreadsheet/static/src/@types/commands.d.ts`
- `addons/spreadsheet/static/src/@types/env.d.ts`
- `addons/spreadsheet/static/src/@types/functions.d.ts`
- `addons/spreadsheet/static/src/@types/getters.d.ts`
- `addons/spreadsheet/static/src/@types/global_filter.d.ts`
- `addons/spreadsheet/static/src/@types/misc.d.ts`
- `addons/spreadsheet/static/src/@types/models.d.ts`
- `addons/spreadsheet/static/src/@types/pivot.d.ts`
- `addons/spreadsheet/static/src/@types/plugins.d.ts`
- `addons/spreadsheet/static/src/actions/helpers.js`
- `addons/spreadsheet/static/src/actions/spreadsheet_component.js`
- `addons/spreadsheet/static/src/actions/spreadsheet_component.scss`
- `addons/spreadsheet/static/src/actions/spreadsheet_component.xml`
- `addons/spreadsheet/static/src/actions/spreadsheet_download_action.js`
- `addons/spreadsheet/static/src/assets_backend/spreadsheet_action_loader.js`
- `addons/spreadsheet/static/src/assets_backend/spreadsheet_binary_field/spreadsheet_binary_field.js`
- `addons/spreadsheet/static/src/assets_backend/spreadsheet_binary_field/spreadsheet_binary_field.xml`
- `addons/spreadsheet/static/src/chart/data_source/chart_data_source.js`
- `addons/spreadsheet/static/src/chart/index.js`
- `addons/spreadsheet/static/src/chart/odoo_chart/odoo_chart_datasource.js`
- `addons/spreadsheet/static/src/chart/odoo_chart/odoo_chart_helpers.js`
- `addons/spreadsheet/static/src/chart/odoo_chart/odoo_chart_zoomable_component.js`
- `addons/spreadsheet/static/src/chart/odoo_chart/odoo_dataset_styles.js`
- `addons/spreadsheet/static/src/chart/odoo_link/chartjs/odoo_link_chartjs_plugin.js`
- `addons/spreadsheet/static/src/chart/odoo_link/components/chart_menu.js`
- `addons/spreadsheet/static/src/chart/odoo_link/components/figure_component.js`
- `addons/spreadsheet/static/src/chart/odoo_link/components/figure_component.xml`
- `addons/spreadsheet/static/src/chart/plugins/chart_odoo_link_plugin.js`
- `addons/spreadsheet/static/src/chart/plugins/odoo_chart_core_plugin.js`
- `addons/spreadsheet/static/src/chart/plugins/odoo_chart_core_view_plugin.js`
- `addons/spreadsheet/static/src/chart/plugins/odoo_chart_feature_plugin.js`
- `addons/spreadsheet/static/src/chart/plugins/operational_transform.js`
- `addons/spreadsheet/static/src/command_palette.js`
- `addons/spreadsheet/static/src/command_provider.js`
- `addons/spreadsheet/static/src/components/share_button/share_button.js`
- `addons/spreadsheet/static/src/components/share_button/share_button.scss`
- `addons/spreadsheet/static/src/components/share_button/share_button.xml`
- `addons/spreadsheet/static/src/currency/formulas.js`
- `addons/spreadsheet/static/src/currency/helpers.js`
- `addons/spreadsheet/static/src/currency/plugins/currency.js`
- `addons/spreadsheet/static/src/data_sources/data_source.js`
- `addons/spreadsheet/static/src/data_sources/data_source_link.js`
- `addons/spreadsheet/static/src/data_sources/odoo_data_provider.js`
- `addons/spreadsheet/static/src/data_sources/odoo_views_data_source.js`
- `addons/spreadsheet/static/src/data_sources/server_data.js`
- `addons/spreadsheet/static/src/global_filters/components/date_filter_dropdown/date_filter_dropdown.js`
- `addons/spreadsheet/static/src/global_filters/components/date_filter_dropdown/date_filter_dropdown.xml`
- `addons/spreadsheet/static/src/global_filters/components/date_filter_value/date_filter_value.js`
- `addons/spreadsheet/static/src/global_filters/components/date_filter_value/date_filter_value.scss`
- `addons/spreadsheet/static/src/global_filters/components/date_filter_value/date_filter_value.xml`
- `addons/spreadsheet/static/src/global_filters/components/default_date_value/default_date_value.js`
- `addons/spreadsheet/static/src/global_filters/components/default_date_value/default_date_value.xml`
- `addons/spreadsheet/static/src/global_filters/components/filter_text_value/filter_text_value.js`
- `addons/spreadsheet/static/src/global_filters/components/filter_text_value/filter_text_value.xml`
- `addons/spreadsheet/static/src/global_filters/components/filter_value/filter_value.js`
- `addons/spreadsheet/static/src/global_filters/components/filter_value/filter_value.scss`
- `addons/spreadsheet/static/src/global_filters/components/filter_value/filter_value.xml`
- `addons/spreadsheet/static/src/global_filters/components/selection_filter_value/selection_filter_value.js`
- `addons/spreadsheet/static/src/global_filters/components/selection_filter_value/selection_filter_value.xml`
- `addons/spreadsheet/static/src/global_filters/helpers.js`
- `addons/spreadsheet/static/src/global_filters/index.js`
- `addons/spreadsheet/static/src/global_filters/plugins/global_filters_core_plugin.js`
- `addons/spreadsheet/static/src/global_filters/plugins/global_filters_core_view_plugin.js`
- `addons/spreadsheet/static/src/global_filters/plugins/global_filters_ui_plugin.js`
- `addons/spreadsheet/static/src/helpers/constants.js`
- `addons/spreadsheet/static/src/helpers/geo_json_service.js`
- `addons/spreadsheet/static/src/helpers/helpers.js`
- `addons/spreadsheet/static/src/helpers/model.js`
- `addons/spreadsheet/static/src/helpers/neutralized_link.js`
- `addons/spreadsheet/static/src/helpers/odoo_functions_helpers.js`
- `addons/spreadsheet/static/src/hooks.js`
- `addons/spreadsheet/static/src/index.js`
- `addons/spreadsheet/static/src/ir_ui_menu/index.js`
- `addons/spreadsheet/static/src/ir_ui_menu/ir_ui_menu_plugin.js`
- `addons/spreadsheet/static/src/ir_ui_menu/odoo_menu_link_cell.js`
- `addons/spreadsheet/static/src/ir_ui_menu/spreadsheet_link_service.js`
- `addons/spreadsheet/static/src/list/index.js`
- `addons/spreadsheet/static/src/list/list_actions.js`
- `addons/spreadsheet/static/src/list/list_data_source.js`
- `addons/spreadsheet/static/src/list/list_functions.js`
- `addons/spreadsheet/static/src/list/list_helpers.js`
- `addons/spreadsheet/static/src/list/plugins/list_core_global_filter_plugin.js`
- `addons/spreadsheet/static/src/list/plugins/list_core_plugin.js`
- `addons/spreadsheet/static/src/list/plugins/list_core_view_plugin.js`
- `addons/spreadsheet/static/src/list/plugins/list_ui_plugin.js`
- `addons/spreadsheet/static/src/logging/logging_ui_plugin.js`
- `addons/spreadsheet/static/src/model.js`
- `addons/spreadsheet/static/src/o_spreadsheet/cancelled_reason.js`
- `addons/spreadsheet/static/src/o_spreadsheet/errors.js`
- `addons/spreadsheet/static/src/o_spreadsheet/icons.xml`
- `addons/spreadsheet/static/src/o_spreadsheet/init_callbacks.js`
- `addons/spreadsheet/static/src/o_spreadsheet/migration.js`
- `addons/spreadsheet/static/src/o_spreadsheet/o_spreadsheet.css`
- `addons/spreadsheet/static/src/o_spreadsheet/o_spreadsheet.js`
- `addons/spreadsheet/static/src/o_spreadsheet/o_spreadsheet.xml`
- `addons/spreadsheet/static/src/o_spreadsheet/o_spreadsheet_extended.scss`
- `addons/spreadsheet/static/src/o_spreadsheet/odoo_module.js`
- `addons/spreadsheet/static/src/o_spreadsheet/translation.js`
- `addons/spreadsheet/static/src/pivot/index.js`
- `addons/spreadsheet/static/src/pivot/odoo_pivot.js`
- `addons/spreadsheet/static/src/pivot/odoo_pivot_loader.js`
- `addons/spreadsheet/static/src/pivot/pivot_actions.js`
- `addons/spreadsheet/static/src/pivot/pivot_functions.js`
- `addons/spreadsheet/static/src/pivot/pivot_helpers.js`
- `addons/spreadsheet/static/src/pivot/pivot_model.js`
- `addons/spreadsheet/static/src/pivot/pivot_time_adapters.js`
- `addons/spreadsheet/static/src/pivot/pivot_to_function_values.js`
- `addons/spreadsheet/static/src/pivot/pivot_values_normalizers.js`
- `addons/spreadsheet/static/src/pivot/plugins/pivot_core_global_filter_plugin.js`
- `addons/spreadsheet/static/src/pivot/plugins/pivot_core_view_global_filter_plugin.js`
- `addons/spreadsheet/static/src/pivot/plugins/pivot_odoo_core_plugin.js`
- `addons/spreadsheet/static/src/pivot/plugins/pivot_odoo_core_view_plugin.js`
- `addons/spreadsheet/static/src/pivot/plugins/pivot_odoo_ui_plugin.js`
- `addons/spreadsheet/static/src/plugins.js`
- `addons/spreadsheet/static/src/public_spreadsheet/chart_component.js`
- `addons/spreadsheet/static/src/public_spreadsheet/clipboard_plugin.js`
- `addons/spreadsheet/static/src/public_spreadsheet/odoo_menu_fill.js`
- `addons/spreadsheet/static/src/scss/spreadsheet_dashboard.scss`
- `addons/spreadsheet/static/src/server_data_plugin.js`
- `addons/spreadsheet/static/tests/charts/model/link_chart_plugin.test.js`
- `addons/spreadsheet/static/tests/charts/model/odoo_chart_plugin.test.js`
- `addons/spreadsheet/static/tests/charts/ui/link_chart_figure.test.js`
- `addons/spreadsheet/static/tests/charts/ui/odoo_chart_component.test.js`
- `addons/spreadsheet/static/tests/charts/ui/scorecard_figure.test.js`
- `addons/spreadsheet/static/tests/command_palette.test.js`
- `addons/spreadsheet/static/tests/currency/currency_plugin.test.js`
- `addons/spreadsheet/static/tests/currency/currency_rate_function.test.js`
- `addons/spreadsheet/static/tests/data_fetching/data_source.test.js`
- `addons/spreadsheet/static/tests/data_fetching/server_data.test.js`
- `addons/spreadsheet/static/tests/global_filters/date_filter_value.test.js`
- `addons/spreadsheet/static/tests/global_filters/default_date_value.test.js`
- `addons/spreadsheet/static/tests/global_filters/filter_value_component.test.js`
- `addons/spreadsheet/static/tests/global_filters/global_filter_helper.test.js`
- `addons/spreadsheet/static/tests/global_filters/global_filters_chart.test.js`
- `addons/spreadsheet/static/tests/global_filters/global_filters_core_view.test.js`
- `addons/spreadsheet/static/tests/global_filters/global_filters_model.test.js`
- `addons/spreadsheet/static/tests/global_filters/odoo_filter_value_v18.test.js`
- `addons/spreadsheet/static/tests/global_filters/selection_filter_value.test.js`
- `addons/spreadsheet/static/tests/helpers/chart.js`
- `addons/spreadsheet/static/tests/helpers/commands.js`
- `addons/spreadsheet/static/tests/helpers/data.js`
- `addons/spreadsheet/static/tests/helpers/date_domain.js`
- `addons/spreadsheet/static/tests/helpers/getters.js`
- `addons/spreadsheet/static/tests/helpers/global_filter.js`
- `addons/spreadsheet/static/tests/helpers/list.js`
- `addons/spreadsheet/static/tests/helpers/locale.js`
- `addons/spreadsheet/static/tests/helpers/model.js`
- `addons/spreadsheet/static/tests/helpers/pivot.js`
- `addons/spreadsheet/static/tests/helpers/pivot_list.js`
- `addons/spreadsheet/static/tests/helpers/stores.js`
- `addons/spreadsheet/static/tests/helpers/ui.js`
- `addons/spreadsheet/static/tests/helpers/zones.js`
- `addons/spreadsheet/static/tests/hoot_override.js`
- `addons/spreadsheet/static/tests/links/menu_data_utils.js`
- `addons/spreadsheet/static/tests/links/model/link_menu_cells.test.js`
- `addons/spreadsheet/static/tests/links/open_links.test.js`
- `addons/spreadsheet/static/tests/lists/list_computed_columns.test.js`
- `addons/spreadsheet/static/tests/lists/list_plugin.test.js`
- `addons/spreadsheet/static/tests/logging_ui_plugin.test.js`
- `addons/spreadsheet/static/tests/migrations/migrations.test.js`
- `addons/spreadsheet/static/tests/pivots/model/pivot_custom_groups_model.test.js`
- `addons/spreadsheet/static/tests/pivots/model/pivot_plugin.test.js`
- `addons/spreadsheet/static/tests/pivots/model/pivot_positional_formula.test.js`
- `addons/spreadsheet/static/tests/pivots/model/pivot_table_function.test.js`
- `addons/spreadsheet/static/tests/pivots/pivot_core_view_global_filter_plugin.test.js`
- `addons/spreadsheet/static/tests/pivots/pivot_helpers.test.js`
- `addons/spreadsheet/static/tests/pivots/pivot_see_records.test.js`
- `addons/spreadsheet/static/tests/public_spreadsheet/freeze.test.js`
- `addons/spreadsheet/static/tests/widgets/spreadsheet_binary_field.test.js`
- `addons/spreadsheet/static/topojson/africa.topo.json`
- `addons/spreadsheet/static/topojson/asia.topo.json`
- `addons/spreadsheet/static/topojson/europe.topo.json`
- `addons/spreadsheet/static/topojson/north_america.topo.json`
- `addons/spreadsheet/static/topojson/oceania.topo.json`
- `addons/spreadsheet/static/topojson/south_america.topo.json`
- `addons/spreadsheet/static/topojson/usa.topo.json`
- `addons/spreadsheet/static/topojson/world.topo.json`
- `addons/spreadsheet/tests/__init__.py`
- `addons/spreadsheet/tests/test_currency.py`
- `addons/spreadsheet/tests/test_currency_rate.py`
- `addons/spreadsheet/tests/test_display_names.py`
- `addons/spreadsheet/tests/test_ir_model.py`
- `addons/spreadsheet/tests/test_locale.py`
- `addons/spreadsheet/tests/test_session_info.py`
- Additional source files not expanded in this page: 7; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
