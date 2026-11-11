# Module: html_builder

- **Module ID:** MOD-105
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/html_builder`
- **Manifest:** `addons/html_builder/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `not declared`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Generic html builder

**Manifest description:**

This addon contains a generic html builder application. It is designed to be
    used by the website builder and mass mailing editor.

**Scope evidence:** The module contains 868 files, including 7 Python, 81 XML, and 214 JavaScript/TypeScript files. The manifest declares dependencies: `html_editor`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 81
- Browser asset files: 214
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 18 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/html_builder/models/ir_ui_view.py:16`, `addons/html_builder/models/ir_qweb.py:11`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 81 XML files and 214 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/html_builder/tests/__init__.py`, `addons/html_builder/tests/test_html_builder_assets_bundle.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 81; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 214; representative files: `addons/html_builder/static/src/builder.js`, `addons/html_builder/static/image_shapes/convert-to-percentages.js`, `addons/html_builder/static/tests/operation.test.js`, `addons/html_builder/static/tests/font.test.js`, `addons/html_builder/static/tests/contenteditable.test.js`, `addons/html_builder/static/tests/builder_sliding_panel.test.js`, `addons/html_builder/static/tests/anchor_plugin.test.js`, `addons/html_builder/static/tests/drop_zone.test.js`, `addons/html_builder/static/tests/image_field.test.js`, `addons/html_builder/static/tests/section_contenteditable.test.js`, `addons/html_builder/static/tests/many2one_field.test.js`, `addons/html_builder/static/tests/drag_and_drop.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/html_builder/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `ir.ui.view` (addons/html_builder/models/ir_ui_view.py:16); inherits `ir.qweb` (addons/html_builder/models/ir_qweb.py:11)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `html_editor`
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

- `addons/html_builder/__init__.py`
- `addons/html_builder/__manifest__.py`
- `addons/html_builder/i18n/af.po`
- `addons/html_builder/i18n/ar.po`
- `addons/html_builder/i18n/az.po`
- `addons/html_builder/i18n/bg.po`
- `addons/html_builder/i18n/bs.po`
- `addons/html_builder/i18n/ca.po`
- `addons/html_builder/i18n/cs.po`
- `addons/html_builder/i18n/da.po`
- `addons/html_builder/i18n/de.po`
- `addons/html_builder/i18n/el.po`
- `addons/html_builder/i18n/es.po`
- `addons/html_builder/i18n/es_419.po`
- `addons/html_builder/i18n/es_CL.po`
- `addons/html_builder/i18n/et.po`
- `addons/html_builder/i18n/fa.po`
- `addons/html_builder/i18n/fi.po`
- `addons/html_builder/i18n/fr.po`
- `addons/html_builder/i18n/fr_CA.po`
- `addons/html_builder/i18n/gl.po`
- `addons/html_builder/i18n/gu.po`
- `addons/html_builder/i18n/he.po`
- `addons/html_builder/i18n/hi.po`
- `addons/html_builder/i18n/hr.po`
- `addons/html_builder/i18n/html_builder.pot`
- `addons/html_builder/i18n/hu.po`
- `addons/html_builder/i18n/id.po`
- `addons/html_builder/i18n/is.po`
- `addons/html_builder/i18n/it.po`
- `addons/html_builder/i18n/ja.po`
- `addons/html_builder/i18n/ka.po`
- `addons/html_builder/i18n/kab.po`
- `addons/html_builder/i18n/km.po`
- `addons/html_builder/i18n/ko.po`
- `addons/html_builder/i18n/ku.po`
- `addons/html_builder/i18n/lo.po`
- `addons/html_builder/i18n/lt.po`
- `addons/html_builder/i18n/lv.po`
- `addons/html_builder/i18n/mk.po`
- `addons/html_builder/i18n/mn.po`
- `addons/html_builder/i18n/my.po`
- `addons/html_builder/i18n/nb.po`
- `addons/html_builder/i18n/nl.po`
- `addons/html_builder/i18n/pl.po`
- `addons/html_builder/i18n/pt.po`
- `addons/html_builder/i18n/pt_BR.po`
- `addons/html_builder/i18n/ro.po`
- `addons/html_builder/i18n/ru.po`
- `addons/html_builder/i18n/sk.po`
- `addons/html_builder/i18n/sl.po`
- `addons/html_builder/i18n/sr@latin.po`
- `addons/html_builder/i18n/sv.po`
- `addons/html_builder/i18n/th.po`
- `addons/html_builder/i18n/tr.po`
- `addons/html_builder/i18n/uk.po`
- `addons/html_builder/i18n/uz.po`
- `addons/html_builder/i18n/vi.po`
- `addons/html_builder/i18n/zh_CN.po`
- `addons/html_builder/i18n/zh_TW.po`
- `addons/html_builder/models/__init__.py`
- `addons/html_builder/models/ir_qweb.py`
- `addons/html_builder/models/ir_ui_view.py`
- `addons/html_builder/static/image_shapes/brushed/brush_1.svg`
- `addons/html_builder/static/image_shapes/brushed/brush_2.svg`
- `addons/html_builder/static/image_shapes/brushed/brush_3.svg`
- `addons/html_builder/static/image_shapes/brushed/brush_4.svg`
- `addons/html_builder/static/image_shapes/composite/composite_cut_circle.svg`
- `addons/html_builder/static/image_shapes/composite/composite_double_pill.svg`
- `addons/html_builder/static/image_shapes/composite/composite_half_circle.svg`
- `addons/html_builder/static/image_shapes/composite/composite_sonar.svg`
- `addons/html_builder/static/image_shapes/composite/composite_triple_pill.svg`
- `addons/html_builder/static/image_shapes/composition/composition_line_1.svg`
- `addons/html_builder/static/image_shapes/composition/composition_line_2.svg`
- `addons/html_builder/static/image_shapes/composition/composition_line_3.svg`
- `addons/html_builder/static/image_shapes/composition/composition_mixed_1.svg`
- `addons/html_builder/static/image_shapes/composition/composition_mixed_2.svg`
- `addons/html_builder/static/image_shapes/composition/composition_organic_line.svg`
- `addons/html_builder/static/image_shapes/composition/composition_oval_line.svg`
- `addons/html_builder/static/image_shapes/composition/composition_planet_1.svg`
- `addons/html_builder/static/image_shapes/composition/composition_planet_2.svg`
- `addons/html_builder/static/image_shapes/composition/composition_square_1.svg`
- `addons/html_builder/static/image_shapes/composition/composition_square_2.svg`
- `addons/html_builder/static/image_shapes/composition/composition_square_3.svg`
- `addons/html_builder/static/image_shapes/composition/composition_square_4.svg`
- `addons/html_builder/static/image_shapes/composition/composition_square_line.svg`
- `addons/html_builder/static/image_shapes/composition/composition_triangle_line.svg`
- `addons/html_builder/static/image_shapes/convert-to-percentages.html`
- `addons/html_builder/static/image_shapes/convert-to-percentages.js`
- `addons/html_builder/static/image_shapes/devices/browser_01.svg`
- `addons/html_builder/static/image_shapes/devices/browser_02.svg`
- `addons/html_builder/static/image_shapes/devices/browser_03.svg`
- `addons/html_builder/static/image_shapes/devices/galaxy_3d_landscape_01.svg`
- `addons/html_builder/static/image_shapes/devices/galaxy_3d_landscape_02.svg`
- `addons/html_builder/static/image_shapes/devices/galaxy_3d_portrait_01.svg`
- `addons/html_builder/static/image_shapes/devices/galaxy_3d_portrait_02.svg`
- `addons/html_builder/static/image_shapes/devices/galaxy_front_landscape.svg`
- `addons/html_builder/static/image_shapes/devices/galaxy_front_portrait.svg`
- `addons/html_builder/static/image_shapes/devices/galaxy_front_portrait_half.svg`
- `addons/html_builder/static/image_shapes/devices/imac_3d_01.svg`
- `addons/html_builder/static/image_shapes/devices/imac_3d_02.svg`
- `addons/html_builder/static/image_shapes/devices/imac_front.svg`
- `addons/html_builder/static/image_shapes/devices/ipad_3d_landscape_01.svg`
- `addons/html_builder/static/image_shapes/devices/ipad_3d_landscape_02.svg`
- `addons/html_builder/static/image_shapes/devices/ipad_3d_portrait_01.svg`
- `addons/html_builder/static/image_shapes/devices/ipad_3d_portrait_02.svg`
- `addons/html_builder/static/image_shapes/devices/ipad_front_landscape.svg`
- `addons/html_builder/static/image_shapes/devices/ipad_front_portrait.svg`
- `addons/html_builder/static/image_shapes/devices/iphone_3d_landscape_01.svg`
- `addons/html_builder/static/image_shapes/devices/iphone_3d_landscape_02.svg`
- `addons/html_builder/static/image_shapes/devices/iphone_3d_portrait_01.svg`
- `addons/html_builder/static/image_shapes/devices/iphone_3d_portrait_02.svg`
- `addons/html_builder/static/image_shapes/devices/iphone_front_landscape.svg`
- `addons/html_builder/static/image_shapes/devices/iphone_front_portrait.svg`
- `addons/html_builder/static/image_shapes/devices/iphone_front_portrait_half.svg`
- `addons/html_builder/static/image_shapes/devices/macbook_3d_01.svg`
- `addons/html_builder/static/image_shapes/devices/macbook_3d_02.svg`
- `addons/html_builder/static/image_shapes/devices/macbook_front.svg`
- `addons/html_builder/static/image_shapes/devices/macbook_front_half.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_cornered_triangle.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_diamond.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_door.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_emerald.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_gem.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_heptagon.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_hexagon.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_kayak.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_pentagon.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_shuriken.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_slanted.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_sonar.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_square.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_square_1.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_square_2.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_square_3.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_square_4.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_square_5.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_square_6.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_star.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_star_16pin.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_star_8pin.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_tear.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_tetris.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_triangle.svg`
- `addons/html_builder/static/image_shapes/geometric/geo_triangle_corner.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_blob_hard.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_blob_medium.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_blob_soft.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_bread.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_circle.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_clover.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_cornered.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_diamond.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_door.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_emerald.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_gem.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_heptagon.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_hexagon.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_lemon.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_pentagon.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_pill.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_shuriken.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_sonar.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_square.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_square_1.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_square_2.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_star.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_star_16pin.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_star_7pin.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_star_8pin.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_tear.svg`
- `addons/html_builder/static/image_shapes/geometric_round/geo_round_triangle.svg`
- `addons/html_builder/static/image_shapes/panel/panel_duo.svg`
- `addons/html_builder/static/image_shapes/panel/panel_duo_r.svg`
- `addons/html_builder/static/image_shapes/panel/panel_duo_step.svg`
- `addons/html_builder/static/image_shapes/panel/panel_duo_step_pill.svg`
- `addons/html_builder/static/image_shapes/panel/panel_trio_in_r.svg`
- `addons/html_builder/static/image_shapes/panel/panel_trio_out_r.svg`
- `addons/html_builder/static/image_shapes/panel/panel_window.svg`
- `addons/html_builder/static/image_shapes/pattern/pattern_circuit.svg`
- `addons/html_builder/static/image_shapes/pattern/pattern_labyrinth.svg`
- `addons/html_builder/static/image_shapes/pattern/pattern_line_star.svg`
- `addons/html_builder/static/image_shapes/pattern/pattern_line_sun.svg`
- `addons/html_builder/static/image_shapes/pattern/pattern_organic_caps.svg`
- `addons/html_builder/static/image_shapes/pattern/pattern_organic_cross.svg`
- `addons/html_builder/static/image_shapes/pattern/pattern_organic_dot.svg`
- `addons/html_builder/static/image_shapes/pattern/pattern_oval_zebra.svg`
- `addons/html_builder/static/image_shapes/pattern/pattern_point.svg`
- `addons/html_builder/static/image_shapes/pattern/pattern_wave_1.svg`
- `addons/html_builder/static/image_shapes/pattern/pattern_wave_2.svg`
- `addons/html_builder/static/image_shapes/pattern/pattern_wave_3.svg`
- `addons/html_builder/static/image_shapes/pattern/pattern_wave_4.svg`
- `addons/html_builder/static/image_shapes/solid/solid_blob_1.svg`
- `addons/html_builder/static/image_shapes/solid/solid_blob_2.svg`
- `addons/html_builder/static/image_shapes/solid/solid_blob_3.svg`
- `addons/html_builder/static/image_shapes/solid/solid_blob_4.svg`
- `addons/html_builder/static/image_shapes/solid/solid_blob_5.svg`
- `addons/html_builder/static/image_shapes/solid/solid_blob_shadow_1.svg`
- `addons/html_builder/static/image_shapes/solid/solid_blob_shadow_2.svg`
- `addons/html_builder/static/image_shapes/solid/solid_square_1.svg`
- `addons/html_builder/static/image_shapes/solid/solid_square_2.svg`
- `addons/html_builder/static/image_shapes/solid/solid_square_3.svg`
- `addons/html_builder/static/image_shapes/special/special_filter.svg`
- `addons/html_builder/static/image_shapes/special/special_flag.svg`
- `addons/html_builder/static/image_shapes/special/special_layered.svg`
- `addons/html_builder/static/image_shapes/special/special_organic.svg`
- `addons/html_builder/static/image_shapes/special/special_rain.svg`
- `addons/html_builder/static/image_shapes/special/special_snow.svg`
- `addons/html_builder/static/image_shapes/special/special_speed.svg`
- `addons/html_builder/static/img/options/bg_shape.svg`
- `addons/html_builder/static/img/options/bring-backward.svg`
- `addons/html_builder/static/img/options/bring-forward.svg`
- `addons/html_builder/static/img/options/desktop_invisible.svg`
- `addons/html_builder/static/img/options/mobile_invisible.svg`
- `addons/html_builder/static/img/options/shadow_in.svg`
- `addons/html_builder/static/img/options/shadow_out.svg`
- `addons/html_builder/static/img/options/size_large.svg`
- `addons/html_builder/static/img/options/size_medium.svg`
- `addons/html_builder/static/img/options/size_small.svg`
- `addons/html_builder/static/img/phone.svg`
- `addons/html_builder/static/img/phone_dark.svg`
- `addons/html_builder/static/img/snippet_disabled.svg`
- `addons/html_builder/static/img/snippets_options/align_bottom.svg`
- `addons/html_builder/static/img/snippets_options/align_middle.svg`
- `addons/html_builder/static/img/snippets_options/align_solo_between.svg`
- `addons/html_builder/static/img/snippets_options/align_solo_bottom.svg`
- `addons/html_builder/static/img/snippets_options/align_solo_middle.svg`
- `addons/html_builder/static/img/snippets_options/align_solo_top.svg`
- `addons/html_builder/static/img/snippets_options/align_stretch.svg`
- `addons/html_builder/static/img/snippets_options/align_top.svg`
- `addons/html_builder/static/shapes/Airy/01.svg`
- `addons/html_builder/static/shapes/Airy/01_001.svg`
- `addons/html_builder/static/shapes/Airy/02.svg`
- `addons/html_builder/static/shapes/Airy/02_001.svg`
- `addons/html_builder/static/shapes/Airy/03.svg`
- `addons/html_builder/static/shapes/Airy/03_001.svg`
- `addons/html_builder/static/shapes/Airy/04.svg`
- `addons/html_builder/static/shapes/Airy/04_001.svg`
- `addons/html_builder/static/shapes/Airy/05.svg`
- `addons/html_builder/static/shapes/Airy/05_001.svg`
- `addons/html_builder/static/shapes/Airy/06.svg`
- `addons/html_builder/static/shapes/Airy/06_001.svg`
- `addons/html_builder/static/shapes/Airy/07.svg`
- `addons/html_builder/static/shapes/Airy/07_001.svg`
- `addons/html_builder/static/shapes/Airy/08.svg`
- `addons/html_builder/static/shapes/Airy/08_001.svg`
- `addons/html_builder/static/shapes/Airy/09.svg`
- `addons/html_builder/static/shapes/Airy/09_001.svg`
- `addons/html_builder/static/shapes/Airy/10.svg`
- `addons/html_builder/static/shapes/Airy/10_001.svg`
- Additional source files not expanded in this page: 618; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
