<img src="https://my-badges.github.io/my-badges/fix-2.png" alt="I did 2 sequential fixes." title="I did 2 sequential fixes." width="128">
<strong>I did 2 sequential fixes.</strong>
<br><br>

Commits:

- <a href="https://github.com/eyolas/conveyor/commit/5d6e016450601e1cf724439af727de9aa950e281">5d6e016</a>: Fix behavioral completeness issues in queue, worker, and utils

- Use recursive sortDeep() in hashPayload for deterministic nested
  object hashing during deduplication
- Mark every() as not yet implemented to prevent silent one-shot
  behavior when users expect repeating jobs
- Handle numeric removeOnComplete/removeOnFail values via shouldRemove()
  helper instead of only checking === true
- Respect maxAttempts in stalled job detection: mark as failed when
  retry budget is exhausted instead of re-enqueuing forever
- Emit waiting/delayed events and publish to store in addBulk() to
  match add() behavior
- Wrap fetchAndProcess() in try/catch inside poll loop to prevent
  unhandled rejections from store errors
- <a href="https://github.com/eyolas/conveyor/commit/4ecf3a408b2eb7d95662a2e6cd24501a39e12322">4ecf3a4</a>: Fix critical and medium bugs across core, shared, and store-memory

Critical: fix timer leak in Worker.withTimeout, hashPayload crash on
non-objects, unhandled promise rejection in fire-and-forget processJob,
and stalled jobs re-enqueuing without incrementing attemptsMade.

Medium: add deduplication support to addBulk, allow retry without
backoff configured, preserve all fields in Job.toJSON, clean up
insertionOrder in MemoryStore clean/drain, snapshot handler Set in
EventBus.emit to prevent mid-iteration mutation, and tighten Worker.on
parameter type from string to QueueEventType.


Created by <a href="https://github.com/my-badges/my-badges">My Badges</a>