# Module Dependencies

A module may depend on other modules through manifest declarations, model inheritance, XML inheritance, asset bundles, routes, services, data files, and tests. The clone must preserve dependency ordering and make each dependency explicit before implementation.

## Required dependency rules

1. Load a module only after its declared prerequisites are available.
2. Reject or clearly report missing/cyclic dependencies.
3. Keep source dependency evidence separate from clone deployment packaging.
4. Test module installation, update, uninstall, and migration ordering.
5. Treat cross-domain dependencies as workflow and data-contract dependencies, not merely package imports.

The complete 666-module coverage map is [`../13_TRACEABILITY_AND_GOVERNANCE/Module_Blueprint_Coverage.csv`](../13_TRACEABILITY_AND_GOVERNANCE/Module_Blueprint_Coverage.csv). Detailed dependency extraction and module build order are later-phase work.
