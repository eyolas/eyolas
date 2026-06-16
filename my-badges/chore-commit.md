<img src="https://my-badges.github.io/my-badges/chore-commit.png" alt="I did a little housekeeping! 🧹" title="I did a little housekeeping! 🧹" width="128">
<strong>I did a little housekeeping! 🧹</strong>
<br><br>

Commits:

- <a href="https://github.com/eyolas/conveyor/commit/901e5c4ad5e9a9664606593e439a99cf836c8688">901e5c4</a>: chore(ci): replace Dependabot with Renovate for Deno + npm deps (#69)

Dependabot has no Deno support (deno.json / JSR specifiers). Renovate's
deno manager handles jsr:/npm: imports in deno.json alongside the npm
package.json files and GitHub Actions, so a single tool covers everything.

- Add renovate.json (npm + deno + github-actions managers)
- Disable @conveyor/** to avoid bumping internal JSR cross-refs
- Group actions into one PR (parity with old Dependabot 'actions' group)
- Remove .github/dependabot.yml to prevent duplicate action PRs

Co-authored-by: Claude Opus 4.8 (1M context) <noreply@anthropic.com>


Created by <a href="https://github.com/my-badges/my-badges">My Badges</a>