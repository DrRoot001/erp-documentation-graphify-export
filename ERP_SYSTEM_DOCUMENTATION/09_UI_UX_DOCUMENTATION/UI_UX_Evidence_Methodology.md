# UI/UX Evidence Methodology — Phase 9

## Extraction rules

- XML records are parsed from `<record>` elements; view/action subsets are identified by model name.
- Menus are parsed from `<menuitem>` elements with parent/action/group metadata.
- Templates are parsed from `<template>` elements with inheritance/template identifiers.
- Frontend class evidence is extracted from JavaScript/TypeScript class declarations using repository-specific regex patterns for `Component`, `AbstractAction`, `Widget`, `Controller`, and `Store` bases, plus static template declarations. JavaScript is not parsed with Python's AST parser.
- Services, registries, client routes, and frontend tests are identified from source registration patterns and test naming/path conventions.
- Style assets are inventoried by SCSS/CSS file path and line count.

## Limitations

Static extraction cannot resolve XML inheritance, asset bundle ordering, dynamic registry additions, runtime group visibility, browser state, responsive behavior, accessibility behavior, or translated labels. These require a configured Odoo database and browser execution.
