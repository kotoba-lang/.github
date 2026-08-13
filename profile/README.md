# Kotoba

Capability-safe language for **untrusted AI-written code**. A compiled program can use only the authority it was granted. Deny-by-default.

**[kotoba-lang.org](https://kotoba-lang.org)**

- Language contract: [`kotoba-lang/kotoba-lang`](https://github.com/kotoba-lang/kotoba-lang)
- CLI / implementation: [`kotoba-lang/kotoba`](https://github.com/kotoba-lang/kotoba)

```sh
brew tap kotoba-lang/kotoba && brew install kotoba
kotoba -e '(+ 1 2)'
```

An empty policy denies every host effect, including `:host/http`. Hosted billed deploy of those grants is not live.

This organization also holds compiler, storage, and database repos. They are implementation pieces, not extra Kotoba products.
