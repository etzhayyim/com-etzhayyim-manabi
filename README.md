# manabi (学び)

`manabi` is the standalone Etzhayyim education actor. It provides CLJC state
machines for literacy, numeracy, civics, vocational learning, lifelong inquiry,
certificate-preparation scaffolds, and social publication planning.

## Repository contract

- `manifest.edn`, `actor.edn`, and `dependencies.edn` are canonical metadata.
- `contracts/` contains canonical EDN schemas, cell declarations, and lexicons.
- `wire/` contains JSON required at DID, registry, and AT Protocol boundaries.
- `src/` and `test/` contain the independent CLJC implementation and suite.
- `data/identity/` and `docs/adr/` contain actor-owned history imported from the
  former root repository.

Go, TinyGo, Python cells, wasm build artifacts, JSON-LD manifests, and shell test
runners are prohibited by `repository-contracts.edn`.

## Verify

```sh
bb test
clojure -M:test
clojure -M:lint
```

The Babashka task is the comprehensive standalone test entry point.
