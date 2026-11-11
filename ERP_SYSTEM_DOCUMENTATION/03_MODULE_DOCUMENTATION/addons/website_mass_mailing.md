# Module: website_mass_mailing

- **Module ID:** MOD-626
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_mass_mailing`
- **Manifest:** `addons/website_mass_mailing/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Attract visitors to subscribe to mailing lists

**Manifest description:**

This module brings a new building block with a mailing list widget to drop on any page of your website.
On a simple click, your visitors can subscribe to mailing lists managed in the Email Marketing app.

**Scope evidence:** The module contains 106 files, including 12 Python, 12 XML, and 18 JavaScript/TypeScript files. The manifest declares dependencies: `website`, `mass_mailing`, `google_recaptcha`.

## 2. Module structure

- Model/business logic files: 0
- Controller/API files: 3
- XML/data/view/template files: 12
- Browser asset files: 18
- Security files: 1
- Test files: 7
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_mass_mailing/security/ir.access.csv`

## 4. Functionalities

### HTTP/API surface

- **Description:** 3 controller files and 2 route declarations.
- **Evidence:** `addons/website_mass_mailing/controllers/main.py:14`, `addons/website_mass_mailing/controllers/main.py:49`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 12 XML files and 18 JavaScript/TypeScript files; static XML analysis found 15 record/template/menu identifiers.
- **Evidence:** `addons/website_mass_mailing/data/ir_model_data.xml:4`, `addons/website_mass_mailing/views/snippets_templates.xml:3`, `addons/website_mass_mailing/views/snippets_templates.xml:7`, `addons/website_mass_mailing/views/snippets_templates.xml:53`, `addons/website_mass_mailing/views/snippets_templates.xml:72`, `addons/website_mass_mailing/views/snippets_templates.xml:80`, `addons/website_mass_mailing/views/snippets_templates.xml:92`, `addons/website_mass_mailing/views/snippets_templates.xml:119`, `addons/website_mass_mailing/views/snippets_templates.xml:142`, `addons/website_mass_mailing/views/snippets_templates.xml:167`, `addons/website_mass_mailing/views/snippets_templates.xml:267`, `addons/website_mass_mailing/views/snippets_templates.xml:302`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_mass_mailing/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 7 test files are present.
- **Evidence:** `addons/website_mass_mailing/tests/test_property_field_mailing_contact.py`, `addons/website_mass_mailing/tests/test_controllers.py`, `addons/website_mass_mailing/tests/common.py`, `addons/website_mass_mailing/tests/test_mailing_controllers.py`, `addons/website_mass_mailing/tests/test_website_mass_mailing.py`, `addons/website_mass_mailing/tests/test_snippets.py`, `addons/website_mass_mailing/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 12; representative identifiers: `mass_mailing.model_mailing_contact`, `remove_external_snippets`, `snippets`, `Newsletter`, `Newsletter Block`, `s_newsletter_block_default_template`, `Newsletter Box`, `Newsletter Centered`, `Newsletter Grid`, `s_newsletter_block_form_template`, `Newsletter Popup`, `Newsletter Aside`, `Waiting List`, `theme_default_template`, `Newsletter Benefits`
- Menus: 0; representative evidence: Not found in module
- Templates: 14; representative evidence: `addons/website_mass_mailing/views/snippets_templates.xml:3`, `addons/website_mass_mailing/views/snippets_templates.xml:7`, `addons/website_mass_mailing/views/snippets_templates.xml:53`, `addons/website_mass_mailing/views/snippets_templates.xml:72`, `addons/website_mass_mailing/views/snippets_templates.xml:80`, `addons/website_mass_mailing/views/snippets_templates.xml:92`, `addons/website_mass_mailing/views/snippets_templates.xml:119`, `addons/website_mass_mailing/views/snippets_templates.xml:142`, `addons/website_mass_mailing/views/snippets_templates.xml:167`, `addons/website_mass_mailing/views/snippets_templates.xml:267`, `addons/website_mass_mailing/views/snippets_templates.xml:302`, `addons/website_mass_mailing/views/snippets_templates.xml:373`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 18; representative files: `addons/website_mass_mailing/static/src/website_builder/mailing_list_subscribe_translation_option_plugin.js`, `addons/website_mass_mailing/static/src/website_builder/recaptcha_subscribe_option_plugin.js`, `addons/website_mass_mailing/static/src/website_builder/newsletter_layout_option_plugin.js`, `addons/website_mass_mailing/static/src/website_builder/mailing_list_subscribe_option_plugin.js`, `addons/website_mass_mailing/static/src/website_builder/newsletter_subscribe_common_option_plugin.js`, `addons/website_mass_mailing/static/src/website_builder/mailing_list_subscribe_option.js`, `addons/website_mass_mailing/static/src/website_builder/recaptcha_subscribe_option.js`, `addons/website_mass_mailing/static/src/website_builder/newsletter_subscribe_common_option.js`, `addons/website_mass_mailing/static/src/js/mass_mailing_form_editor.edit.js`, `addons/website_mass_mailing/static/src/interactions/subscribe.js`, `addons/website_mass_mailing/static/src/interactions/popup.js`, `addons/website_mass_mailing/static/src/interactions/fix_newsletter_list_class.edit.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_mass_mailing/__manifest__.py`
- **HTTP entry points:** `addons/website_mass_mailing/controllers/main.py:14`, `addons/website_mass_mailing/controllers/main.py:49`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 2
- Route evidence: `addons/website_mass_mailing/controllers/main.py:14`, `addons/website_mass_mailing/controllers/main.py:49`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website`, `mass_mailing`, `google_recaptcha`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Not found
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/website_mass_mailing/__init__.py`
- `addons/website_mass_mailing/__manifest__.py`
- `addons/website_mass_mailing/controllers/__init__.py`
- `addons/website_mass_mailing/controllers/main.py`
- `addons/website_mass_mailing/controllers/website_form.py`
- `addons/website_mass_mailing/data/ir_model_data.xml`
- `addons/website_mass_mailing/i18n/ar.po`
- `addons/website_mass_mailing/i18n/az.po`
- `addons/website_mass_mailing/i18n/bg.po`
- `addons/website_mass_mailing/i18n/bs.po`
- `addons/website_mass_mailing/i18n/ca.po`
- `addons/website_mass_mailing/i18n/cs.po`
- `addons/website_mass_mailing/i18n/da.po`
- `addons/website_mass_mailing/i18n/de.po`
- `addons/website_mass_mailing/i18n/el.po`
- `addons/website_mass_mailing/i18n/es.po`
- `addons/website_mass_mailing/i18n/es_419.po`
- `addons/website_mass_mailing/i18n/et.po`
- `addons/website_mass_mailing/i18n/fa.po`
- `addons/website_mass_mailing/i18n/fi.po`
- `addons/website_mass_mailing/i18n/fr.po`
- `addons/website_mass_mailing/i18n/gu.po`
- `addons/website_mass_mailing/i18n/he.po`
- `addons/website_mass_mailing/i18n/hi.po`
- `addons/website_mass_mailing/i18n/hr.po`
- `addons/website_mass_mailing/i18n/hu.po`
- `addons/website_mass_mailing/i18n/id.po`
- `addons/website_mass_mailing/i18n/is.po`
- `addons/website_mass_mailing/i18n/it.po`
- `addons/website_mass_mailing/i18n/ja.po`
- `addons/website_mass_mailing/i18n/kab.po`
- `addons/website_mass_mailing/i18n/km.po`
- `addons/website_mass_mailing/i18n/ko.po`
- `addons/website_mass_mailing/i18n/ku.po`
- `addons/website_mass_mailing/i18n/lo.po`
- `addons/website_mass_mailing/i18n/lt.po`
- `addons/website_mass_mailing/i18n/lv.po`
- `addons/website_mass_mailing/i18n/mk.po`
- `addons/website_mass_mailing/i18n/mn.po`
- `addons/website_mass_mailing/i18n/my.po`
- `addons/website_mass_mailing/i18n/nb.po`
- `addons/website_mass_mailing/i18n/nl.po`
- `addons/website_mass_mailing/i18n/pl.po`
- `addons/website_mass_mailing/i18n/pt.po`
- `addons/website_mass_mailing/i18n/pt_BR.po`
- `addons/website_mass_mailing/i18n/ro.po`
- `addons/website_mass_mailing/i18n/ru.po`
- `addons/website_mass_mailing/i18n/sk.po`
- `addons/website_mass_mailing/i18n/sl.po`
- `addons/website_mass_mailing/i18n/sr@latin.po`
- `addons/website_mass_mailing/i18n/sv.po`
- `addons/website_mass_mailing/i18n/th.po`
- `addons/website_mass_mailing/i18n/tr.po`
- `addons/website_mass_mailing/i18n/uk.po`
- `addons/website_mass_mailing/i18n/uz.po`
- `addons/website_mass_mailing/i18n/vi.po`
- `addons/website_mass_mailing/i18n/website_mass_mailing.pot`
- `addons/website_mass_mailing/i18n/zh_CN.po`
- `addons/website_mass_mailing/i18n/zh_TW.po`
- `addons/website_mass_mailing/security/ir.access.csv`
- `addons/website_mass_mailing/static/description/icon.png`
- `addons/website_mass_mailing/static/description/icon.svg`
- `addons/website_mass_mailing/static/description/icon_hi.png`
- `addons/website_mass_mailing/static/shapes/s_newsletter_benefits_popup.svg`
- `addons/website_mass_mailing/static/snippets/snippets_templates.xml`
- `addons/website_mass_mailing/static/src/img/snippets_thumbs/s_newsletter_block.svg`
- `addons/website_mass_mailing/static/src/interactions/fix_newsletter_list_class.edit.js`
- `addons/website_mass_mailing/static/src/interactions/popup.js`
- `addons/website_mass_mailing/static/src/interactions/subscribe.js`
- `addons/website_mass_mailing/static/src/interactions/subscribe_list_missing_error.xml`
- `addons/website_mass_mailing/static/src/js/mass_mailing_form_editor.edit.js`
- `addons/website_mass_mailing/static/src/plugins/form_option_plugin.js`
- `addons/website_mass_mailing/static/src/scss/website_mass_mailing.scss`
- `addons/website_mass_mailing/static/src/scss/website_mass_mailing_edit_mode.scss`
- `addons/website_mass_mailing/static/src/scss/website_mass_mailing_popup.scss`
- `addons/website_mass_mailing/static/src/snippets/s_newsletter_benefits_popup/s_newsletter_benefits_popup.preview.scss`
- `addons/website_mass_mailing/static/src/website_builder/mailing_list_subscribe_option.edit.scss`
- `addons/website_mass_mailing/static/src/website_builder/mailing_list_subscribe_option.js`
- `addons/website_mass_mailing/static/src/website_builder/mailing_list_subscribe_option.xml`
- `addons/website_mass_mailing/static/src/website_builder/mailing_list_subscribe_option_plugin.js`
- `addons/website_mass_mailing/static/src/website_builder/mailing_list_subscribe_translation_option_plugin.js`
- `addons/website_mass_mailing/static/src/website_builder/newsletter_layout_option.xml`
- `addons/website_mass_mailing/static/src/website_builder/newsletter_layout_option_plugin.js`
- `addons/website_mass_mailing/static/src/website_builder/newsletter_options.xml`
- `addons/website_mass_mailing/static/src/website_builder/newsletter_subscribe_common_option.js`
- `addons/website_mass_mailing/static/src/website_builder/newsletter_subscribe_common_option.xml`
- `addons/website_mass_mailing/static/src/website_builder/newsletter_subscribe_common_option_plugin.js`
- `addons/website_mass_mailing/static/src/website_builder/recaptcha_subscribe_option.js`
- `addons/website_mass_mailing/static/src/website_builder/recaptcha_subscribe_option.xml`
- `addons/website_mass_mailing/static/src/website_builder/recaptcha_subscribe_option_plugin.js`
- `addons/website_mass_mailing/static/src/website_builder/toggle_thanks_message_translation_option.xml`
- `addons/website_mass_mailing/static/src/xml/website_mass_mailing.xml`
- `addons/website_mass_mailing/static/tests/builder/mailing_list_subscribe_translation_option_plugin.test.js`
- `addons/website_mass_mailing/static/tests/interactions/popup.test.js`
- `addons/website_mass_mailing/static/tests/tours/snippet_newsletter_block_with_edit.js`
- `addons/website_mass_mailing/static/tests/tours/snippet_newsletter_popup_edition.js`
- `addons/website_mass_mailing/static/tests/tours/snippet_newsletter_popup_use.js`
- `addons/website_mass_mailing/tests/__init__.py`
- `addons/website_mass_mailing/tests/common.py`
- `addons/website_mass_mailing/tests/test_controllers.py`
- `addons/website_mass_mailing/tests/test_mailing_controllers.py`
- `addons/website_mass_mailing/tests/test_property_field_mailing_contact.py`
- `addons/website_mass_mailing/tests/test_snippets.py`
- `addons/website_mass_mailing/tests/test_website_mass_mailing.py`
- `addons/website_mass_mailing/views/snippets/s_newsletter_benefits_popup.xml`
- `addons/website_mass_mailing/views/snippets_templates.xml`
