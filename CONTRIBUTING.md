# Contributing to kotoba-lang

These defaults apply to every repository in the [kotoba-lang](https://github.com/kotoba-lang)
organization unless that repository overrides them with its own `CONTRIBUTING.md`.

## Licensing

All kotoba-lang code is licensed under the
[Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

By submitting a contribution you agree that it is licensed under Apache-2.0, and
you confirm you have the right to submit it (see Apache-2.0 §5 — contributions
are inbound-equals-outbound by default; there is no separate CLA).

A small number of repositories are deliberately licensed differently — currently
`comfyui` (GPL-3.0, derivative of an upstream GPL work) and six AGPL-3.0
repositories. Those keep their own `LICENSE`; check the file in the repository
you are contributing to.

## Ground rules for the codebase

kotoba-lang is a multi-repository workspace whose composition is managed by a
[west](https://docs.zephyrproject.org/latest/develop/west/) manifest in the
`com-junkawasaki/root` superproject. Two conventions matter most to outside
contributors:

- **Portable `.cljc` first.** Runtime priority is `kotoba wasm` → `clojurewasm` →
  ClojureScript → nbb. JVM-only and Babashka-only paths are compatibility layers,
  not the design premise. New tooling scripts are written in nbb (`.cljs`).
- **Content addressing is the base, not an add-on.** In the datom-plane repos
  (`kotobase*`, `io-ipld`, `prolly-tree`, `chain`, `arrangement`, `datalog`),
  facts are CIDv1 blocks and the index is a content-addressed Prolly Tree. Changes
  that break CID determinism break every downstream consumer.

## Pull requests

1. Branch from the repository's default branch. Do not rebase shared branches and
   do not force-push.
2. Keep the diff scoped to one concern.
3. Include a test that fails before your change and passes after it. For the
   datom plane that usually means an assertion on datoms/CIDs, not a screenshot.
4. State in the PR what you actually ran, including failures. A PR that says
   "tests pass" without saying which ones is not reviewable.

## Reporting bugs

Open an issue in the specific repository. Include the repository, the commit SHA,
what you ran, what you expected, and what happened. For anything that looks like a
security issue, use the process in [`SECURITY.md`](SECURITY.md) instead — do not
open a public issue.

## Code of conduct

Participation is governed by [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md)
(Contributor Covenant 2.1).
