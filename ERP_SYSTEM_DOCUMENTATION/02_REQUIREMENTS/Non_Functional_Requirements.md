# Non-Functional Requirements

## Verified characteristics

- **Maintainability:** modular addon manifests, dependency graph, namespaced Python packages, tests, and migration support.
- **Portability:** packaging assets exist for Python installation, Debian, Windows/IOT support; actual deployment portability remains environment dependent.
- **Security:** authentication providers, sessions, access-control artifacts, password/TOTP/passkey-related addons, and security tests are present. Presence does not prove a secure deployment configuration.
- **Observability:** logging, server logging, profiling/debug configuration, and test diagnostics are present in source.
- **Internationalization:** translation `.po/.pot` files and localization addons are present.
- **Data integrity:** ORM constraints, transactions, PostgreSQL, access rules, and migration mechanisms are present.

## Not established statically

No production SLA, throughput target, latency budget, backup RPO/RTO, availability target, accessibility conformance level, or capacity limit is asserted by this repository snapshot.
