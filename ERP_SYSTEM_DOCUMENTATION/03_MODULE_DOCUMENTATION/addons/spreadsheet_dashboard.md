# Module: spreadsheet_dashboard

- **Module ID:** MOD-546
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/spreadsheet_dashboard`
- **Manifest:** `addons/spreadsheet_dashboard/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Productivity/Dashboard`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Spreadsheet

**Manifest description:**

Spreadsheet

**Scope evidence:** The module contains 132 files, including 18 Python, 15 XML, and 37 JavaScript/TypeScript files. The manifest declares dependencies: `spreadsheet`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 3
- XML/data/view/template files: 15
- Browser asset files: 37
- Security files: 2
- Test files: 8
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/spreadsheet_dashboard/security/ir.access.csv`, `addons/spreadsheet_dashboard/security/security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 60 methods, 0 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/spreadsheet_dashboard/models/spreadsheet_dashboard_share.py:8`, `addons/spreadsheet_dashboard/models/spreadsheet_dashboard_group.py:5`, `addons/spreadsheet_dashboard/models/spreadsheet_dashboard_favorite_filters.py:4`, `addons/spreadsheet_dashboard/models/spreadsheet_dashboard.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 4 route declarations.
- **Evidence:** `addons/spreadsheet_dashboard/controllers/dashboards_controllers.py:7`, `addons/spreadsheet_dashboard/controllers/share.py:13`, `addons/spreadsheet_dashboard/controllers/share.py:33`, `addons/spreadsheet_dashboard/controllers/share.py:46`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 15 XML files and 37 JavaScript/TypeScript files; static XML analysis found 33 record/template/menu identifiers.
- **Evidence:** `addons/spreadsheet_dashboard/security/security.xml:2`, `addons/spreadsheet_dashboard/security/security.xml:9`, `addons/spreadsheet_dashboard/data/dashboard.xml:4`, `addons/spreadsheet_dashboard/data/dashboard.xml:9`, `addons/spreadsheet_dashboard/data/dashboard.xml:14`, `addons/spreadsheet_dashboard/data/dashboard.xml:19`, `addons/spreadsheet_dashboard/data/dashboard.xml:24`, `addons/spreadsheet_dashboard/data/dashboard.xml:29`, `addons/spreadsheet_dashboard/data/dashboard.xml:34`, `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml:4`, `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml:20`, `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml:34`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/spreadsheet_dashboard/security/ir.access.csv`, `addons/spreadsheet_dashboard/security/security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 8 test files are present.
- **Evidence:** `addons/spreadsheet_dashboard/tests/test_share_dashboard_tour.py`, `addons/spreadsheet_dashboard/tests/test_share_controllers.py`, `addons/spreadsheet_dashboard/tests/test_dashboard_controllers.py`, `addons/spreadsheet_dashboard/tests/test_dashboard_share.py`, `addons/spreadsheet_dashboard/tests/common.py`, `addons/spreadsheet_dashboard/tests/test_dashboard_favorite_filters.py`, `addons/spreadsheet_dashboard/tests/test_spreadsheet_dashboard.py`, `addons/spreadsheet_dashboard/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 15; representative identifiers: `res_groups_privilege_dashboard`, `spreadsheet_dashboard.group_dashboard_manager`, `spreadsheet_dashboard_group_finance`, `spreadsheet_dashboard_group_sales`, `spreadsheet_dashboard_group_hr`, `spreadsheet_dashboard_group_website`, `spreadsheet_dashboard_group_project`, `spreadsheet_dashboard_group_logistics`, `spreadsheet_dashboard_group_marketing`, `spreadsheet_dashboard_view_list`, `spreadsheet_dashboard_view_search`, `spreadsheet_dashboard_container_view_list`, `spreadsheet_dashboard_view_form`, `spreadsheet_dashboard_view_kanban`, `spreadsheet_dashboard_share_view_list`, `spreadsheet_dashboard_share_view_search`, `spreadsheet_dashboard_favorite_filters_view_form`, `spreadsheet_dashboard_favorite_filters_view_edit_form`, `spreadsheet_dashboard_favorite_filters_view_list`, `spreadsheet_dashboard_favorite_filters_view_search`
- Menus: 8; representative evidence: `addons/spreadsheet_dashboard/views/menu_views.xml:9`, `addons/spreadsheet_dashboard/views/menu_views.xml:17`, `addons/spreadsheet_dashboard/views/menu_views.xml:24`, `addons/spreadsheet_dashboard/views/menu_views.xml:54`, `addons/spreadsheet_dashboard/views/menu_views.xml:61`, `addons/spreadsheet_dashboard/views/menu_views.xml:68`, `addons/spreadsheet_dashboard/views/menu_views.xml:75`, `addons/spreadsheet_dashboard/views/menu_views.xml:80`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 29; representative evidence: `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml:6`, `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml:7`, `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml:22`, `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml:23`, `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml:36`, `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml:37`, `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml:47`, `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml:48`, `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml:72`, `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml:73`, `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml:86`, `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml:87`
- Browser assets: 37; representative files: `addons/spreadsheet_dashboard/static/src/public/public_dashboard.js`, `addons/spreadsheet_dashboard/static/src/assets/global_filter_widget_loader.js`, `addons/spreadsheet_dashboard/static/src/assets/dashboard_action_loader.js`, `addons/spreadsheet_dashboard/static/src/bundle/pivot/clickable_cell.js`, `addons/spreadsheet_dashboard/static/src/bundle/chart/chart_menu.js`, `addons/spreadsheet_dashboard/static/src/bundle/chart/chart_js_component_dashboard.js`, `addons/spreadsheet_dashboard/static/src/bundle/global_filter_widget/global_filter_widget.js`, `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_search_model.js`, `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_action.js`, `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_menu_translate_service.js`, `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_loader_service.js`, `addons/spreadsheet_dashboard/static/src/bundle/list/clickable_cell.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/spreadsheet_dashboard/__manifest__.py`
- **HTTP entry points:** `addons/spreadsheet_dashboard/controllers/dashboards_controllers.py:7`, `addons/spreadsheet_dashboard/controllers/share.py:13`, `addons/spreadsheet_dashboard/controllers/share.py:33`, `addons/spreadsheet_dashboard/controllers/share.py:46`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: `spreadsheet.dashboard.share` (addons/spreadsheet_dashboard/models/spreadsheet_dashboard_share.py:8); `spreadsheet.dashboard.group` (addons/spreadsheet_dashboard/models/spreadsheet_dashboard_group.py:5); `spreadsheet.dashboard.favorite.filters` (addons/spreadsheet_dashboard/models/spreadsheet_dashboard_favorite_filters.py:4); `spreadsheet.dashboard` (addons/spreadsheet_dashboard/models/spreadsheet_dashboard.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 4
- Route evidence: `addons/spreadsheet_dashboard/controllers/dashboards_controllers.py:7`, `addons/spreadsheet_dashboard/controllers/share.py:13`, `addons/spreadsheet_dashboard/controllers/share.py:33`, `addons/spreadsheet_dashboard/controllers/share.py:46`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `spreadsheet`
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

- `addons/spreadsheet_dashboard/__init__.py`
- `addons/spreadsheet_dashboard/__manifest__.py`
- `addons/spreadsheet_dashboard/controllers/__init__.py`
- `addons/spreadsheet_dashboard/controllers/dashboards_controllers.py`
- `addons/spreadsheet_dashboard/controllers/share.py`
- `addons/spreadsheet_dashboard/data/dashboard.xml`
- `addons/spreadsheet_dashboard/i18n/ar.po`
- `addons/spreadsheet_dashboard/i18n/az.po`
- `addons/spreadsheet_dashboard/i18n/bg.po`
- `addons/spreadsheet_dashboard/i18n/bs.po`
- `addons/spreadsheet_dashboard/i18n/ca.po`
- `addons/spreadsheet_dashboard/i18n/cs.po`
- `addons/spreadsheet_dashboard/i18n/da.po`
- `addons/spreadsheet_dashboard/i18n/de.po`
- `addons/spreadsheet_dashboard/i18n/el.po`
- `addons/spreadsheet_dashboard/i18n/es.po`
- `addons/spreadsheet_dashboard/i18n/es_419.po`
- `addons/spreadsheet_dashboard/i18n/et.po`
- `addons/spreadsheet_dashboard/i18n/fa.po`
- `addons/spreadsheet_dashboard/i18n/fi.po`
- `addons/spreadsheet_dashboard/i18n/fr.po`
- `addons/spreadsheet_dashboard/i18n/he.po`
- `addons/spreadsheet_dashboard/i18n/hi.po`
- `addons/spreadsheet_dashboard/i18n/hr.po`
- `addons/spreadsheet_dashboard/i18n/hu.po`
- `addons/spreadsheet_dashboard/i18n/id.po`
- `addons/spreadsheet_dashboard/i18n/it.po`
- `addons/spreadsheet_dashboard/i18n/ja.po`
- `addons/spreadsheet_dashboard/i18n/kab.po`
- `addons/spreadsheet_dashboard/i18n/ko.po`
- `addons/spreadsheet_dashboard/i18n/ku.po`
- `addons/spreadsheet_dashboard/i18n/lo.po`
- `addons/spreadsheet_dashboard/i18n/lt.po`
- `addons/spreadsheet_dashboard/i18n/lv.po`
- `addons/spreadsheet_dashboard/i18n/mn.po`
- `addons/spreadsheet_dashboard/i18n/my.po`
- `addons/spreadsheet_dashboard/i18n/nb.po`
- `addons/spreadsheet_dashboard/i18n/nl.po`
- `addons/spreadsheet_dashboard/i18n/pl.po`
- `addons/spreadsheet_dashboard/i18n/pt.po`
- `addons/spreadsheet_dashboard/i18n/pt_BR.po`
- `addons/spreadsheet_dashboard/i18n/ro.po`
- `addons/spreadsheet_dashboard/i18n/ru.po`
- `addons/spreadsheet_dashboard/i18n/sk.po`
- `addons/spreadsheet_dashboard/i18n/sl.po`
- `addons/spreadsheet_dashboard/i18n/spreadsheet_dashboard.pot`
- `addons/spreadsheet_dashboard/i18n/sr@latin.po`
- `addons/spreadsheet_dashboard/i18n/sv.po`
- `addons/spreadsheet_dashboard/i18n/th.po`
- `addons/spreadsheet_dashboard/i18n/tr.po`
- `addons/spreadsheet_dashboard/i18n/uk.po`
- `addons/spreadsheet_dashboard/i18n/uz.po`
- `addons/spreadsheet_dashboard/i18n/vi.po`
- `addons/spreadsheet_dashboard/i18n/zh_CN.po`
- `addons/spreadsheet_dashboard/i18n/zh_TW.po`
- `addons/spreadsheet_dashboard/models/__init__.py`
- `addons/spreadsheet_dashboard/models/spreadsheet_dashboard.py`
- `addons/spreadsheet_dashboard/models/spreadsheet_dashboard_favorite_filters.py`
- `addons/spreadsheet_dashboard/models/spreadsheet_dashboard_group.py`
- `addons/spreadsheet_dashboard/models/spreadsheet_dashboard_share.py`
- `addons/spreadsheet_dashboard/security/ir.access.csv`
- `addons/spreadsheet_dashboard/security/security.xml`
- `addons/spreadsheet_dashboard/static/description/icon.png`
- `addons/spreadsheet_dashboard/static/description/icon.svg`
- `addons/spreadsheet_dashboard/static/description/icon_hi.png`
- `addons/spreadsheet_dashboard/static/src/assets/dashboard_action_loader.js`
- `addons/spreadsheet_dashboard/static/src/assets/global_filter_widget_loader.js`
- `addons/spreadsheet_dashboard/static/src/bundle/chart/chart_js_component_dashboard.js`
- `addons/spreadsheet_dashboard/static/src/bundle/chart/chart_menu.js`
- `addons/spreadsheet_dashboard/static/src/bundle/chart/chart_menu.scss`
- `addons/spreadsheet_dashboard/static/src/bundle/chart/chart_menu.xml`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_action.js`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_action.scss`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_action.xml`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_date_filter/dashboard_date_filter.js`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_date_filter/dashboard_date_filter.scss`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_date_filter/dashboard_date_filter.xml`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_facet/dashboard_facet.js`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_facet/dashboard_facet.xml`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_filter_list/dashboard_filter_list.js`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_filter_list/dashboard_filter_list.scss`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_filter_list/dashboard_filter_list.xml`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_loader_service.js`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_menu_translate_service.js`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_search_bar/dashboard_search_bar.js`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_search_bar/dashboard_search_bar.scss`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_search_bar/dashboard_search_bar.xml`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_search_bar_menu/dashboard_custom_favorite_item.js`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_search_bar_menu/dashboard_search_bar_menu.js`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_search_bar_menu/dashboard_search_bar_menu.scss`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_search_bar_menu/dashboard_search_bar_menu.xml`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/dashboard_search_model.js`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/mobile_figure_container/mobile_figure_container.js`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/mobile_figure_container/mobile_figure_container.scss`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/mobile_figure_container/mobile_figure_container.xml`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/mobile_search_panel/mobile_search_panel.js`
- `addons/spreadsheet_dashboard/static/src/bundle/dashboard_action/mobile_search_panel/mobile_search_panel.xml`
- `addons/spreadsheet_dashboard/static/src/bundle/global_filter_widget/global_filter_widget.js`
- `addons/spreadsheet_dashboard/static/src/bundle/global_filter_widget/global_filter_widget.xml`
- `addons/spreadsheet_dashboard/static/src/bundle/list/clickable_cell.js`
- `addons/spreadsheet_dashboard/static/src/bundle/list/sort_icon.js`
- `addons/spreadsheet_dashboard/static/src/bundle/pivot/clickable_cell.js`
- `addons/spreadsheet_dashboard/static/src/public/public_dashboard.js`
- `addons/spreadsheet_dashboard/static/src/public/public_dashboard.scss`
- `addons/spreadsheet_dashboard/static/src/public/public_dashboard.xml`
- `addons/spreadsheet_dashboard/static/tests/chart/chart_dashboard_menu.test.js`
- `addons/spreadsheet_dashboard/static/tests/chart/dashboard_chart_animations.test.js`
- `addons/spreadsheet_dashboard/static/tests/chart/dashboard_chart_menu.test.js`
- `addons/spreadsheet_dashboard/static/tests/clickable_cells/clickable_cells.test.js`
- `addons/spreadsheet_dashboard/static/tests/dashboard/dashboard_action.test.js`
- `addons/spreadsheet_dashboard/static/tests/dashboard/dashboard_action_mobile.test.js`
- `addons/spreadsheet_dashboard/static/tests/dashboard/dashboard_date_filter.test.js`
- `addons/spreadsheet_dashboard/static/tests/dashboard/dashboard_filter_list.test.js`
- `addons/spreadsheet_dashboard/static/tests/dashboard/dashboard_loader.test.js`
- `addons/spreadsheet_dashboard/static/tests/dashboard/dashboard_search_model.test.js`
- `addons/spreadsheet_dashboard/static/tests/global_filter_widget/global_filter_widget.test.js`
- `addons/spreadsheet_dashboard/static/tests/helpers/dashboard_action.js`
- `addons/spreadsheet_dashboard/static/tests/helpers/data.js`
- `addons/spreadsheet_dashboard/static/tests/mobile/mobile_dashboard_action.test.js`
- `addons/spreadsheet_dashboard/static/tests/public/public_dashboard.test.js`
- `addons/spreadsheet_dashboard/static/tests/tours/share_dashboard_public_tour.js`
- `addons/spreadsheet_dashboard/tests/__init__.py`
- `addons/spreadsheet_dashboard/tests/common.py`
- `addons/spreadsheet_dashboard/tests/data/sample_dashboard.json`
- `addons/spreadsheet_dashboard/tests/test_dashboard_controllers.py`
- `addons/spreadsheet_dashboard/tests/test_dashboard_favorite_filters.py`
- `addons/spreadsheet_dashboard/tests/test_dashboard_share.py`
- `addons/spreadsheet_dashboard/tests/test_share_controllers.py`
- `addons/spreadsheet_dashboard/tests/test_share_dashboard_tour.py`
- `addons/spreadsheet_dashboard/tests/test_spreadsheet_dashboard.py`
- `addons/spreadsheet_dashboard/views/menu_views.xml`
- `addons/spreadsheet_dashboard/views/spreadsheet_dashboard_views.xml`
