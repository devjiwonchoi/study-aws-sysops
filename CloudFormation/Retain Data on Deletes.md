
### `DeletionPolicy=Retain`

- Specify on [[Resources]] to preserve / backup in case of [[CloudFormation]] deletes

### `DeletionPolicy=Snapshot`

- EBS Volumes, ElastiCache Cluster, ElastiCache ReplicationGroup
- RDS DBInstance, RDS DBCluster, Redshift Cluster
### `DeletionPolicy=Delete`

- `AWS::RDS::DBCluster` default: [[#`DeletionPolicy=Snapshot`]]
- To delete an S3 bucket, empty the bucket first