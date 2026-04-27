<img src="https://my-badges.github.io/my-badges/fix-4.png" alt="I did 4 sequential fixes." title="I did 4 sequential fixes." width="128">
<strong>I did 4 sequential fixes.</strong>
<br><br>

Commits:

- <a href="https://github.com/eyolas/voyageDL/commit/923b1fa1cea9ec8d82f4220b32845b92444e9b5f">923b1fa</a>: Fix sidecar lookup: search by target triple (yt-dlp-x86_64-pc-windows-msvc.exe)

Tauri bundles the sidecars with the target triple suffix in the name.
find_sidecar now tries every variant: with triple, without triple,
with/without .exe. The target triple is injected via build.rs.
Improved error message listing the names attempted.

Co-Authored-By: Claude Opus 4.6 (1M context) <noreply@anthropic.com>
- <a href="https://github.com/eyolas/voyageDL/commit/23fd042cee8fefe2d3af6356ddc7faf28448590f">23fd042</a>: Fix Windows build: missing CommandExt import in kill_process

Co-Authored-By: Claude Opus 4.6 (1M context) <noreply@anthropic.com>
- <a href="https://github.com/eyolas/voyageDL/commit/dc3d63f19ad62a8d29749b8171a4120ca0b81f08">dc3d63f</a>: Fix Windows console popups: CREATE_NO_WINDOW on all child processes

Added the CREATE_NO_WINDOW flag (0x08000000) on every yt-dlp/ffmpeg
spawn via a centralized spawn_sidecar function. Cross-platform
kill_process helper (kill on unix, taskkill /F on Windows).

Co-Authored-By: Claude Opus 4.6 (1M context) <noreply@anthropic.com>
- <a href="https://github.com/eyolas/voyageDL/commit/e56d798060abbf8fda3a50aab8f54628ecb25a04">e56d798</a>: Fix GitHub Actions release permissions and Rust warnings

Added permissions: contents: write on the workflow so GITHUB_TOKEN
can create releases. Silenced Rust warnings on variables only used
in debug builds.

Co-Authored-By: Claude Opus 4.6 (1M context) <noreply@anthropic.com>


Created by <a href="https://github.com/my-badges/my-badges">My Badges</a>