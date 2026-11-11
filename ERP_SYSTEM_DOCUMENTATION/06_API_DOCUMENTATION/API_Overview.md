# API Overview — Phase 7

## Static endpoint inventory

The controller AST extraction found **669 actual `@route` declarations** across **117 modules**. The earlier `Route_Inventory.csv` contains 975 broad text matches, including framework examples and non-controller references; it is retained as a broad discovery inventory, not as the authoritative endpoint count. The complete route contract evidence is `API_Endpoint_Inventory.csv`; each row retains source file, line, controller class/method, route path(s), HTTP methods, request type, auth, CSRF, readonly, CORS, bearer scope, session behavior, and a bounded source context.

| Request type | Count |
|---|---:|
| `http` | 446 |
| `jsonrpc` | 216 |
| `json2` | 7 |


| Auth mode | Count |
|---|---:|
| `public` | 384 |
| `user` | 229 |
| `none` | 38 |
| `bearer` | 6 |
| `outlook` | 5 |
| `calendar` | 5 |
| `thing` | 2 |


| HTTP method explicitly declared | Count |
|---|---:|
| `POST` | 123 |
| `GET` | 80 |
| `OPTIONS` | 3 |
| `PUT` | 2 |
| `post` | 1 |
| `get` | 1 |
| `DELETE` | 1 |
| `PATCH` | 1 |


Routes without an explicit method list inherit framework defaults; that default is not fabricated in the endpoint CSV. Request and response body schemas, validation details, and error payloads require route-method tracing and/or runtime OpenAPI-like introspection.
