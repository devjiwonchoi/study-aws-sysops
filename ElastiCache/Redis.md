- [[Multi AZ]] with Auto-Failover
- [[Read Replica]] to scale reads and high availability
- Data Durability using AOF (Append Only File) persistence
	- **AOF** (Append Only File): AOF persistence logs every write operation received by the server. These operations can then be replayed again at server startup, reconstructing the original dataset. Commands are logged using the same format as the Redis protocol itself.
- Backup and restore features
- Supports Sets and Sorted Sets

### Cluster Mode

- When disabled, replica max 5
- Data is partitioned across shards
- Multi-AZ
- Up to 500 nodes per cluster

#### Online Scaling
- continue serving requests during the scaling
#### Offline Scaling
- unable to serve requests during the scaling
### Auto Scaling

- Automated in/decrease the desired shards or replicas
- Target Tracking and Scheduled Scaling
- Works only for [[#Cluster Mode]]
