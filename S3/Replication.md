1. Must enable [[Buckets#Versioning|Versioning]] 
2. [[Buckets]] can be in different AWS accounts
3. Copying is async
4. Must give proper [[IAM]] permissions to [[S3]]
### Cross Region Replication (CRR)

Used for compliance, lower latency access, replication across accounts
### Same Region Replication (SRR)

Log aggregation, live replication between prod and test accounts

Note:

1. After enabled replication, only new objects will be replicated
2. Optionally, can replicate existing objects using [[S3]] Batch 
	1. Replicates existing and replication failed objects
3. Can replicate delete markers from source to target by optional
	1. Deletions with [[Buckets#Versioning|version]] ID are not replicated
4. There is no chaining of replication
	1. A -> B, B -> C, A++ !== C++
