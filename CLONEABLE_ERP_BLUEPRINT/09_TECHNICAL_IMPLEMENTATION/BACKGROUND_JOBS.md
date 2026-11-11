# Background Jobs

Scheduled-file and automation evidence is preserved in the module workflow register. The clone job runtime must define schedule, trigger, execution identity/context, locking/concurrency, idempotency, retry/backoff, failure/dead-letter handling, transaction boundaries, monitoring, and manual replay.

A static scheduler reference does not prove that a job is configured, enabled, or successfully executed.
