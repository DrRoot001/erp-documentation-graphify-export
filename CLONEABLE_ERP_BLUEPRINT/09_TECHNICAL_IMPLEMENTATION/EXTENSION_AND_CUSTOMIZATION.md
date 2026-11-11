# Extension and Customization

The original system uses addon manifests, model inheritance, XML view/template inheritance, registries, assets, security data, and module dependency/load order. A clone should provide explicit extension contracts for domain models, UI views/components, routes, events, jobs, reports, and security policies.

Extensions must declare dependencies, avoid modifying core behavior invisibly, include migrations and tests, and preserve authorization and transaction invariants.
