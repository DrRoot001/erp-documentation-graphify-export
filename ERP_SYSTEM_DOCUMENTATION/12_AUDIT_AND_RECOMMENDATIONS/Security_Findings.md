# Security Findings — Phase 12

This static audit does **not** claim a confirmed exploitable vulnerability. It identifies security review priorities that require contextual testing and deployment verification.

| ID | Severity | Finding | Evidence |
|---|---|---|---|
| AUD-008 | Medium | Safe-evaluation whitelist contains addon wildcard entries explicitly marked for future restriction. | `odoo/tools/safe_eval/runtime.py:768-769` |
| AUD-002 | High | Secret handling, backup encryption, production monitoring, and recovery controls are not established by repository deployment artifacts. | Phase 11 deployment inventory |
| AUD-004 | Medium | Route-level authorization and payload behavior require runtime verification for the deployed module set. | Phase 7/8 route and security inventories |

Recommended validation includes route authentication/authorization tests, company/record-rule isolation tests, file/attachment access tests, dependency scanning, secret scanning, and safe-evaluation regression tests.
