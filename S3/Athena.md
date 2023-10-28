
**Serverless Query** service to analyze data stored in [[S3]]
Use SQL

Good for reporting, analyze and query VPC Flow Logs, [[ELB (Elastic Load Balancer)]] Logs, CloutTrail trails, etc.

1. Columnar data - cost saving by less scan
2. Compress data - smaller retrievals (gzip, etc.)
3. Partition - datasets in S3 for easy querying on virtual columns
4. Use larger files over 128 MB to minimize overheads (additional costs, time, resources, or other factors associated with a particular activity or process that are not directly tied to the primary or core function of that activity)