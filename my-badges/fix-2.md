<img src="https://my-badges.github.io/my-badges/fix-2.png" alt="I did 2 sequential fixes." title="I did 2 sequential fixes." width="128">
<strong>I did 2 sequential fixes.</strong>
<br><br>

Commits:

- <a href="https://github.com/eyolas/conveyor/commit/69544d52e0fe0b185c9b3263f405560e8306acee">69544d5</a>: fix(test): fix formatting, lint, and remove non-portable conformance test

Apply deno fmt, fix unused variable lint error, remove clean createdAt
fallback test that is not portable across store implementations (PgStore
does not support updating createdAt).
- <a href="https://github.com/eyolas/conveyor/commit/438b70d5f431c5ba98a99a58e71f89c1dfd9d25b">438b70d</a>: fix(test): cast invalid parseDelay args to satisfy type checker


Created by <a href="https://github.com/my-badges/my-badges">My Badges</a>