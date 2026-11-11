# Authentication — Phase 8

## Provider and session evidence

The authentication inventory identifies 37 relevant addon manifests. Capabilities include local/session authentication, LDAP, OAuth, passkey/WebAuthn, TOTP/MFA, password policy, signup/registration, session timeout, portal access, privacy, certificates, and captcha where corresponding modules are present.

Route auth distribution from the authoritative endpoint inventory:

- `public`: 384 routes
- `user`: 229 routes
- `none`: 38 routes
- `outlook`: 5 routes
- `calendar`: 5 routes
- `bearer`: 6 routes
- `thing`: 2 routes


Authentication configuration, provider credentials, password policy settings, MFA enrollment state, session expiry, and external identity-provider availability require deployment verification. No secret values are included.
