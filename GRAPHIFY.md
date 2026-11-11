# Graphify for ERP SYSTEM

This repository includes a committed `graphify-out/` knowledge graph optimized for AI-assisted cloning. It is a deterministic baseline built from the existing reverse-engineering inventories and cloneable blueprint.

## Use the committed graph first

Read `graphify-out/ai-index.md`, then query `graphify-out/graph.json` and follow each node's `source_file`. This avoids loading the entire source tree for ordinary architecture, module, API, database, workflow, security, or UI questions.

## Enrich or refresh with upstream Graphify

The upstream tool is Graphify by Graphify Labs. The package is currently installed as `graphifyy`; the CLI is `graphify`.

```bash
pip install graphifyy
graphify install
/graphify CLONEABLE_ERP_BLUEPRINT --update
```

Run the semantic Graphify pipeline only when provider credentials and review time are available. Keep generated caches and sensitive provider output out of Git. The committed baseline labels only directly evidenced relationships as `EXTRACTED`; future `INFERRED` and `AMBIGUOUS` relationships require review.

## Scope

The graph covers the source evidence package and the cloneable blueprint, including 666 modules, 2,963 requirements, 4,209 ORM entities, 669 API routes, 666 workflow evidence rows, security declarations, frontend surfaces, and test/deployment evidence.
