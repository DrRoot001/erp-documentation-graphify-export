# Module APIs — Phase 7

The machine-readable endpoint inventory contains 669 rows. API routes are grouped by source module in the `Module` column and linked to controller source locations. Route declarations establish the transport contract surface; they do not alone establish response schemas or successful runtime availability.

## API processing path

`odoo/http/` provides routing, request/session handling, dispatch, and response mechanisms. Addon controllers call ORM models and services, may apply authentication/authorization, and may return rendered views, HTTP responses, JSON/JSON-RPC responses, redirects, files, or explicit exceptions.
