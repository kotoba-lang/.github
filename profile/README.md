# Kotoba

We love Lisp: programs as data, a small expressive core, and the possibility of
understanding and reshaping a system from within. Kotoba carries that spirit
into a modern Lisp machine in development, with explicit authority and bounded
resources for humans and AI agents.
The name Kotoba evokes “the Word” in John 1:1.

Amu is Kotoba's native compiler. On one Apple M4 measurement, translated
Kotoba ports ran in 0.80× the time of C across 19 Embench workloads. That
exploratory result used a particular compiler snapshot, including audited
algorithm substitutions; it is not a released-toolchain result or a universal
speed ranking. [Measurements, limitations, and reproduction](https://kotoba-lang.org/blog/embench-c-parity-20261015/).

**[kotoba-lang.org](https://kotoba-lang.org)**

- Language contract: [`kotoba-lang/kotoba-lang`](https://github.com/kotoba-lang/kotoba-lang)
- CLI / implementation: [`kotoba-lang/kotoba`](https://github.com/kotoba-lang/kotoba)
- Native compiler: [`kotoba-lang/amu`](https://github.com/kotoba-lang/amu)

Try the [Apple Silicon native first-run guide](https://github.com/kotoba-lang/amu/blob/main/examples/foundation-starter/MACOS-ARM64.md)
or the [pinned Linux starter](https://github.com/kotoba-lang/amu/blob/main/examples/foundation-starter/README.md).
Each describes its host scope and remaining qualification; the complete Lisp
machine and independent-user release are still in development.

An empty policy denies every host effect, including `:host/http`. Hosted billed deploy of those grants is not live.

This organization also holds compiler, storage, and database repos. They are implementation pieces, not extra Kotoba products.

Repositories named after another vendor or authority (`com-*`, dotted names such as `gov.sec.edgar`, and `cloud-*`) hold vendor-compatible API shapes, API clients and data snapshots. They are not Kotoba products. Their API shapes are catalogued as `api` entries in [itonami-registry](https://github.com/cloud-itonami/itonami-registry/blob/main/docs/adr/0005-api-entries.md), pinned per commit and marked shape-only, which grants nothing. The repositories themselves stay here.
