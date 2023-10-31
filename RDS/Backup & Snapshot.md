
## Backups

- continuous & allow point in time recovery
- happen during maintenance windows
- when delete DB instance, can retain automated backups
- have retention period you set between 0~35 days
- to disable, set retention period as 0

## Snapshots

- takes IO ops and can stop the DB from seconds to minutes
- taken on [[Multi AZ]] DB don't impact the master - just the standby
- incremental after the first snapshot (which is full)
- can copy & share
	- Manual snapshots can be shared right away
	- Automated snapshots need to be copied first
	- can only share unencrypted and encrypted with customer managed key snapshots
	- if share encrypted, need to share the customer managed key also
- **Manual** snapshots don't expire
- can take the final snapshot when delete DB