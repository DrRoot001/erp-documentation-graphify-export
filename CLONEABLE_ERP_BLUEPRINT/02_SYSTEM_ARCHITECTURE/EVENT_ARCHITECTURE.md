# Event Architecture

## Verified source capabilities

The source contains scheduled actions, background services, bus/event facilities, notifications, mail, and integration callbacks. Exact event names, delivery guarantees, retry policy, and ordering are deployment/runtime dependent unless established by a specific module artifact.

## Clone event contract

Use explicit domain events for state changes that cross module boundaries. Each event should define producer, schema/version, consumer, idempotency key, transaction boundary, retry/dead-letter behavior, and audit impact. Where source evidence does not establish an event contract, mark it `ASSUMPTION` and validate against module workflows.
