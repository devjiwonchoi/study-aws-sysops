Limit max 1000 concurrent executions (a.k.a. reserved concurrency) on function level
If need higher limit, request AWS

## Throttle

> Occurs when the execution limit exceeds

### Sync

Returns `ThrottleError - 429` error.

### Async

- Returns event to the dead-letter queue, then retries up to 6 hr
- The retry interval increases exponentially from 1 sec to max 5 min

