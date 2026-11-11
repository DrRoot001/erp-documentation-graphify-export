# Frontend Architecture

## Verified source architecture

The source client combines browser JavaScript/TypeScript, XML/QWeb templates and views, SCSS/CSS assets, registries, services, client routes, actions, and server-rendered/API-backed screens. It is delivered through Odoo asset bundles and depends on installed addon declarations and XML inheritance.

## Cloneable architecture

Implement a presentation layer with route/view resolution, reusable components, application services, client state, asset packaging, authorization-aware navigation, accessibility, and API error handling. Keep business rules in backend/domain services; frontend validation improves UX but is not the security boundary.

Runtime component lifecycles, bundle ordering, inherited templates, and responsive behavior remain `UNKNOWN` until browser execution and asset-build validation.
