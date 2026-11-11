# Implementation Inventory

## Static inventory

- 50,889 files were enumerated recursively outside `.git` and the generated package.
- Python AST inspection found 8,626 classes and 57,645 functions/methods.
- Decorator/call inspection found `3,750` `depends`, `583` `onchange`, `573` `constrains`, and `975` HTTP route declarations.
- 4,204 class definitions contained model metadata such as `_name`, `_inherit`, or `_inherits`.

## Entry points

- `odoo-bin:1-6` delegates to `odoo.cli.main()`.
- `odoo/__main__.py:1-3` delegates to `odoo.cli.command.main`.
- CLI server startup is implemented under `odoo/cli/server.py` and service startup under `odoo/service/server.py`.
- Addon loading and registry initialization are implemented under `odoo/modules/` and `odoo/modules/registry.py`.
- HTTP dispatch/routing/session behavior is implemented under `odoo/http/`.

## Status semantics used in this package

- **Implemented artifact**: source, manifest, data, route, security, or test evidence exists.
- **Partially implemented / requires verification**: static declarations exist but runtime execution, configuration, or end-to-end behavior is not established by source inspection alone.
- **Not found in codebase**: no matching artifact was found by the documented inventory query; this is not a guarantee about dynamically generated or external behavior.
