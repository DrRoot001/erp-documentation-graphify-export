# Module: auth_passkey

- **Module ID:** MOD-022
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/auth_passkey`
- **Manifest:** `addons/auth_passkey/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Log in with a Passkey

**Manifest description:**

The implementation of Passkeys using the webauthn protocol.
===========================================================

Passkeys are a secure alternative to a username and a password.
When a user logs in with a Passkey, MFA will not be required.

**Scope evidence:** The module contains 129 files, including 61 Python, 5 XML, and 9 JavaScript/TypeScript files. The manifest declares dependencies: `base_setup`, `web`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 2
- XML/data/view/template files: 5
- Browser asset files: 9
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/auth_passkey/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 40 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/auth_passkey/models/auth_passkey_key.py:21`, `addons/auth_passkey/models/auth_passkey_key.py:159`, `addons/auth_passkey/models/res_users.py:11`, `addons/auth_passkey/models/res_users_identitycheck.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 2 route declarations.
- **Evidence:** `addons/auth_passkey/controllers/main.py:11`, `addons/auth_passkey/controllers/main.py:16`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 9 JavaScript/TypeScript files; static XML analysis found 9 record/template/menu identifiers.
- **Evidence:** `addons/auth_passkey/views/res_users_identitycheck_views.xml:3`, `addons/auth_passkey/views/auth_passkey_login_templates.xml:3`, `addons/auth_passkey/views/auth_passkey_login_templates.xml:9`, `addons/auth_passkey/views/auth_passkey_key_views.xml:3`, `addons/auth_passkey/views/auth_passkey_key_views.xml:25`, `addons/auth_passkey/views/auth_passkey_key_views.xml:43`, `addons/auth_passkey/views/auth_passkey_key_views.xml:50`, `addons/auth_passkey/views/res_users_views.xml:3`, `addons/auth_passkey/views/res_users_views.xml:27`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/auth_passkey/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/auth_passkey/tests/test_passkey_demo.py`, `addons/auth_passkey/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `res_users_identitycheck_view_form_passkey`, `auth_passkey_login`, `Passkey Login OAuth`, `auth_passkey_key_view_kanban`, `auth_passkey_key_rename`, `action_auth_passkey_key_create`, `auth_passkey_key_create_view_form`, `auth_passkey_users_form`, `auth_passkey_users_preferences`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/auth_passkey/views/auth_passkey_login_templates.xml:3`, `addons/auth_passkey/views/auth_passkey_login_templates.xml:9`
- View/action field declarations: 14; representative evidence: `addons/auth_passkey/views/res_users_identitycheck_views.xml:4`, `addons/auth_passkey/views/res_users_identitycheck_views.xml:6`, `addons/auth_passkey/views/auth_passkey_key_views.xml:5`, `addons/auth_passkey/views/auth_passkey_key_views.xml:6`, `addons/auth_passkey/views/auth_passkey_key_views.xml:27`, `addons/auth_passkey/views/auth_passkey_key_views.xml:28`, `addons/auth_passkey/views/auth_passkey_key_views.xml:45`, `addons/auth_passkey/views/auth_passkey_key_views.xml:47`, `addons/auth_passkey/views/auth_passkey_key_views.xml:52`, `addons/auth_passkey/views/auth_passkey_key_views.xml:53`, `addons/auth_passkey/views/res_users_views.xml:5`, `addons/auth_passkey/views/res_users_views.xml:7`
- Browser assets: 9; representative files: `addons/auth_passkey/static/lib/simplewebauthn.js`, `addons/auth_passkey/static/tests/passkeys_login.js`, `addons/auth_passkey/static/tests/passkeys_registration.js`, `addons/auth_passkey/static/tests/passkeys_verify.js`, `addons/auth_passkey/static/tests/passkeys_delete.js`, `addons/auth_passkey/static/src/interactions/passkey_login.js`, `addons/auth_passkey/static/src/views/auth_passkey_key_create_form_view.js`, `addons/auth_passkey/static/src/views/auth_passkey_identity_check_form_view.js`, `addons/auth_passkey/static/src/services/check_identity/check_identity.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/auth_passkey/__manifest__.py`
- **HTTP entry points:** `addons/auth_passkey/controllers/main.py:11`, `addons/auth_passkey/controllers/main.py:16`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: `auth.passkey.key` (addons/auth_passkey/models/auth_passkey_key.py:21); `auth.passkey.key.create` (addons/auth_passkey/models/auth_passkey_key.py:159); inherits `res.users` (addons/auth_passkey/models/res_users.py:11); inherits `res.users.identitycheck` (addons/auth_passkey/models/res_users_identitycheck.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 2
- Route evidence: `addons/auth_passkey/controllers/main.py:11`, `addons/auth_passkey/controllers/main.py:16`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base_setup`, `web`
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

- `addons/auth_passkey/__init__.py`
- `addons/auth_passkey/__manifest__.py`
- `addons/auth_passkey/_vendor/webauthn/INFO`
- `addons/auth_passkey/_vendor/webauthn/LICENSE`
- `addons/auth_passkey/_vendor/webauthn/__init__.py`
- `addons/auth_passkey/_vendor/webauthn/authentication/__init__.py`
- `addons/auth_passkey/_vendor/webauthn/authentication/generate_authentication_options.py`
- `addons/auth_passkey/_vendor/webauthn/authentication/verify_authentication_response.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/__init__.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/aaguid_to_string.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/algorithms.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/asn1/__init__.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/asn1/android_key.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/base64url_to_bytes.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/bytes_to_base64url.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/byteslike_to_bytes.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/cose.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/decode_credential_public_key.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/decoded_public_key_to_cryptography.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/encode_cbor.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/exceptions.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/generate_challenge.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/generate_user_handle.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/hash_by_alg.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/known_root_certs.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/options_to_json.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/parse_attestation_object.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/parse_attestation_statement.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/parse_authentication_credential_json.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/parse_authenticator_data.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/parse_backup_flags.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/parse_cbor.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/parse_client_data_json.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/parse_registration_credential_json.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/pem_cert_bytes_to_open_ssl_x509.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/snake_case_to_camel_case.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/structs.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/tpm/__init__.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/tpm/parse_cert_info.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/tpm/parse_pub_area.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/tpm/structs.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/validate_certificate_chain.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/verify_safetynet_timestamp.py`
- `addons/auth_passkey/_vendor/webauthn/helpers/verify_signature.py`
- `addons/auth_passkey/_vendor/webauthn/py.typed`
- `addons/auth_passkey/_vendor/webauthn/registration/__init__.py`
- `addons/auth_passkey/_vendor/webauthn/registration/formats/__init__.py`
- `addons/auth_passkey/_vendor/webauthn/registration/formats/android_key.py`
- `addons/auth_passkey/_vendor/webauthn/registration/formats/android_safetynet.py`
- `addons/auth_passkey/_vendor/webauthn/registration/formats/apple.py`
- `addons/auth_passkey/_vendor/webauthn/registration/formats/fido_u2f.py`
- `addons/auth_passkey/_vendor/webauthn/registration/formats/packed.py`
- `addons/auth_passkey/_vendor/webauthn/registration/formats/tpm.py`
- `addons/auth_passkey/_vendor/webauthn/registration/generate_registration_options.py`
- `addons/auth_passkey/_vendor/webauthn/registration/verify_registration_response.py`
- `addons/auth_passkey/controllers/__init__.py`
- `addons/auth_passkey/controllers/main.py`
- `addons/auth_passkey/i18n/ar.po`
- `addons/auth_passkey/i18n/auth_passkey.pot`
- `addons/auth_passkey/i18n/az.po`
- `addons/auth_passkey/i18n/bg.po`
- `addons/auth_passkey/i18n/bs.po`
- `addons/auth_passkey/i18n/ca.po`
- `addons/auth_passkey/i18n/cs.po`
- `addons/auth_passkey/i18n/da.po`
- `addons/auth_passkey/i18n/de.po`
- `addons/auth_passkey/i18n/el.po`
- `addons/auth_passkey/i18n/es.po`
- `addons/auth_passkey/i18n/es_419.po`
- `addons/auth_passkey/i18n/et.po`
- `addons/auth_passkey/i18n/fa.po`
- `addons/auth_passkey/i18n/fi.po`
- `addons/auth_passkey/i18n/fr.po`
- `addons/auth_passkey/i18n/he.po`
- `addons/auth_passkey/i18n/hi.po`
- `addons/auth_passkey/i18n/hr.po`
- `addons/auth_passkey/i18n/hu.po`
- `addons/auth_passkey/i18n/id.po`
- `addons/auth_passkey/i18n/it.po`
- `addons/auth_passkey/i18n/ja.po`
- `addons/auth_passkey/i18n/kab.po`
- `addons/auth_passkey/i18n/ko.po`
- `addons/auth_passkey/i18n/ku.po`
- `addons/auth_passkey/i18n/lo.po`
- `addons/auth_passkey/i18n/lt.po`
- `addons/auth_passkey/i18n/lv.po`
- `addons/auth_passkey/i18n/mn.po`
- `addons/auth_passkey/i18n/my.po`
- `addons/auth_passkey/i18n/nb.po`
- `addons/auth_passkey/i18n/nl.po`
- `addons/auth_passkey/i18n/pl.po`
- `addons/auth_passkey/i18n/pt.po`
- `addons/auth_passkey/i18n/pt_BR.po`
- `addons/auth_passkey/i18n/ro.po`
- `addons/auth_passkey/i18n/ru.po`
- `addons/auth_passkey/i18n/sk.po`
- `addons/auth_passkey/i18n/sl.po`
- `addons/auth_passkey/i18n/sr@latin.po`
- `addons/auth_passkey/i18n/sv.po`
- `addons/auth_passkey/i18n/th.po`
- `addons/auth_passkey/i18n/tr.po`
- `addons/auth_passkey/i18n/uk.po`
- `addons/auth_passkey/i18n/uz.po`
- `addons/auth_passkey/i18n/vi.po`
- `addons/auth_passkey/i18n/zh_CN.po`
- `addons/auth_passkey/i18n/zh_TW.po`
- `addons/auth_passkey/mobile_utils.py`
- `addons/auth_passkey/models/__init__.py`
- `addons/auth_passkey/models/auth_passkey_key.py`
- `addons/auth_passkey/models/res_users.py`
- `addons/auth_passkey/models/res_users_identitycheck.py`
- `addons/auth_passkey/security/ir.access.csv`
- `addons/auth_passkey/static/lib/simplewebauthn.js`
- `addons/auth_passkey/static/src/interactions/passkey_login.js`
- `addons/auth_passkey/static/src/scss/res_users.scss`
- `addons/auth_passkey/static/src/services/check_identity/check_identity.js`
- `addons/auth_passkey/static/src/services/check_identity/check_identity.xml`
- `addons/auth_passkey/static/src/views/auth_passkey_identity_check_form_view.js`
- `addons/auth_passkey/static/src/views/auth_passkey_key_create_form_view.js`
- `addons/auth_passkey/static/tests/passkeys_delete.js`
- `addons/auth_passkey/static/tests/passkeys_login.js`
- `addons/auth_passkey/static/tests/passkeys_registration.js`
- `addons/auth_passkey/static/tests/passkeys_verify.js`
- `addons/auth_passkey/tests/__init__.py`
- `addons/auth_passkey/tests/test_passkey_demo.py`
- `addons/auth_passkey/views/auth_passkey_key_views.xml`
- `addons/auth_passkey/views/auth_passkey_login_templates.xml`
- `addons/auth_passkey/views/res_users_identitycheck_views.xml`
- `addons/auth_passkey/views/res_users_views.xml`
