<img src="https://my-badges.github.io/my-badges/fix-2.png" alt="I did 2 sequential fixes." title="I did 2 sequential fixes." width="128">
<strong>I did 2 sequential fixes.</strong>
<br><br>

Commits:

- <a href="https://github.com/eyolas/voyageDL/commit/e508e8edca2f2497c7995bbf88f8d1311dcab729">e508e8e</a>: Fix missing Deezer covers: cache invalidation and attached_pic on MP3

Per-track cache v2 (old entries without album_cover_url ignored),
-disposition:v:0 attached_pic now applied to MP3s as well, and embed
errors are logged instead of being silently swallowed.

Co-Authored-By: Claude Opus 4.7 (1M context) <noreply@anthropic.com>
- <a href="https://github.com/eyolas/voyageDL/commit/471a4d86b02b442ab71d96c54b62f62aab9ff532">471a4d8</a>: Fix download duplicates: clean up finished jobs and harden the queue

Finished jobs used to stick around in downloadJobs, causing
re-downloads after a queue clear. Refactored processJobs into a while
loop over jobsRef to pick up new jobs added during an ongoing
download.

Co-Authored-By: Claude Opus 4.6 (1M context) <noreply@anthropic.com>


Created by <a href="https://github.com/my-badges/my-badges">My Badges</a>