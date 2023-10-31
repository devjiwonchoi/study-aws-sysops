
PSQL & MySQL are both supported as Aurora DB
Costs more, but is more efficient - managed by AWS

Is clustered, high availability

### Backup

- Retention period 1 ~ 35 days (can't be disabled)
- Restore to new DB cluster

### Backtracking

- Rewind the cluster back and forth in time (up to 72 hr)
- Don't create new DB cluster
- MySQL only

### Cloning

- Create new DB cluster as same DB cluster volume of original
- copy on write protocol

### Security

- At-rest encryption
- In-flight encryption
- [[IAM]] Auth
- Security Groups
- No SSH

### Good to know

1. Associate priority tier (0~15) on each [[Read Replica]]
	1. Controls failover priority
	2. [[RDS (Relational Database Service)]] will promote the [[Read Replica]] with highest priority
	3. If replicas have same priority, RDS promotes the largest in size
	4. If same priority & size, RDS promotes arbitrary replica
2. Can migrate RDS MySQL snapshot to Aurora MySQL Cluster