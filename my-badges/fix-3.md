<img src="https://my-badges.github.io/my-badges/fix-3.png" alt="I did 3 sequential fixes." title="I did 3 sequential fixes." width="128">
<strong>I did 3 sequential fixes.</strong>
<br><br>

Commits:

- <a href="https://github.com/eyolas/conveyor/commit/a3be878cb7ac7c0d2c272b295da15b7d541d8aab">a3be878</a>: fix(test): replace .resolves.not.toThrow() with plain await for bun test compatibility

The bun native test runner does not support .resolves.not.toThrow() and
throws "Thrown value: undefined" even when the promise resolves normally.
- <a href="https://github.com/eyolas/conveyor/commit/69544d52e0fe0b185c9b3263f405560e8306acee">69544d5</a>: fix(test): fix formatting, lint, and remove non-portable conformance test

Apply deno fmt, fix unused variable lint error, remove clean createdAt
fallback test that is not portable across store implementations (PgStore
does not support updating createdAt).
- <a href="https://github.com/eyolas/conveyor/commit/438b70d5f431c5ba98a99a58e71f89c1dfd9d25b">438b70d</a>: fix(test): cast invalid parseDelay args to satisfy type checker


Created by <a href="https://github.com/my-badges/my-badges">My Badges</a>