# REST and HTTP Endpoints

`Endpoint_Register.csv` contains 669 source-derived records with route, controller, method, route type, authentication, CSRF, readonly, CORS, session, classification, source line, and bounded context.

The clone should expose stable versioned contracts where appropriate, but versioning policy is an `ASSUMPTION` unless approved. Routes without explicit source HTTP methods must not receive invented methods; resolve framework defaults during semantic/runtime review.

| Authentication evidence | Count |
|---|---:|
| `public` | 384 |
| `user` | 229 |
| `none` | 38 |
| `outlook` | 5 |
| `calendar` | 5 |
| `bearer` | 6 |
| `thing` | 2 |

