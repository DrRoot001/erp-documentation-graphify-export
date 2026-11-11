# API Authentication

Route evidence includes public, user, none, bearer, and provider-specific authentication values. Authentication must be implemented independently from business services and combined with model/record/tenant authorization.

The clone must document session/token lifecycle, expiration, CSRF, replay protection, password/MFA/provider flows, logout/revocation, and error responses. Only source-backed mechanisms are `VERIFIED`; deployment-specific token policy is `UNKNOWN` or an approved `ASSUMPTION`.
