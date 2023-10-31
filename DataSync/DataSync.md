
1. Move large amount of data to and from
	1. On-premises / other cloud to AWS (NFS, SMB, HDFS, [[S3]] API) - needs agent
	2. Different storage services - no agent needed
2. Can sync to
	1. [[S3]]
	2. [[Elastic File System (EFS)]]
	3. [[FSx]]
3. Replication tasks can be scheduled hourly/daily/weekly
4. **File permissions and metadata are preserved** - IMPORTANT
5. One agent task can use 10 Gbps, can setup a bandwidth limit

### Alternate

- AWS Snowcone