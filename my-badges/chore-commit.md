<img src="https://my-badges.github.io/my-badges/chore-commit.png" alt="I did a little housekeeping! 🧹" title="I did a little housekeeping! 🧹" width="128">
<strong>I did a little housekeeping! 🧹</strong>
<br><br>

Commits:

- <a href="https://github.com/eyolas/conveyor/commit/c3e440abc423057719b30fe098c50cdc9a029e62">c3e440a</a>: chore(store-sqlite): allowlist ORDER BY fragments (#64)

* chore(store-sqlite): allowlist ORDER BY fragments

Defense-in-depth against future regressions. The three ORDER BY
interpolations in sqlite-store.ts are currently safe (values derived
from booleans / enum states), but nothing prevents a later change from
feeding attacker-controlled input into the same template.

Introduce SAFE_FETCH_ORDERS / SAFE_LIST_ORDERS allowlists and an
assertSafeSqlFragment helper that throws if an interpolated fragment
falls outside the list. Same wire behavior, runtime guard on drift.

Flagged in a full-project security review (no exploit today, hardening
only).

Co-Authored-By: Claude Opus 4.7 (1M context) <noreply@anthropic.com>

* test(store-sqlite): cover assertSafeSqlFragment guard

Lock in the allowlist contract so a future regression that adds an
unsafe ORDER BY fragment fails loudly at unit-test level instead of
only at the interpolation sites.

Co-Authored-By: Claude Opus 4.7 (1M context) <noreply@anthropic.com>

---------

Co-authored-by: Claude Opus 4.7 (1M context) <noreply@anthropic.com>


Created by <a href="https://github.com/my-badges/my-badges">My Badges</a>