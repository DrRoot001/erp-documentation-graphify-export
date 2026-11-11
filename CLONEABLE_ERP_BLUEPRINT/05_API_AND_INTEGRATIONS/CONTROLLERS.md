# Controllers

Controllers are transport adapters. For each source controller method, the clone must preserve route reachability, authentication and CSRF metadata, input validation, authorization checks, service invocation, serialization/rendering, transaction behavior, and error mapping.

The source context is retained in `Endpoint_Register.csv`; complete payload schemas and runtime response variants require route-by-route review.
