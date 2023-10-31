Is SYNCHRONOUS

Used to disaster recovery (increase availability)

Note: [[Read Replica]] can also be set as multi AZ for disaster recovery

### Good to know

> From Single AZ to Multi AZ
1. No need to stop the DB (zero downtime)
2. Just click on `modify` on the database and enable Multi AZ

Process:

- Snapshot taken
- New DB is created at new AZ from the snapshot
- Synchronization is established between the two DBs.

### Failover Conditions

- The primary DB instance
	- Failed
	- OS is undergoing software patching
	- Loss of network connect
	- Modified (e.g. DB instance type changed)
	- Busy & unresponsive
	- Underlying storage failure
- AZ outage
- Manual failover of the DB instance was initiated using **Reboot with failover**
