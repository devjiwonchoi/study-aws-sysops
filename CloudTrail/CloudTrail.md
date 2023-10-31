1. Provides governance, compliance and audit for the account, and is enabled by default.
2. Get an history of events / API calls made within the account by:
	- Console
	- SDK
	- CLI
	- AWS Services
3. Can put logs from CloudTrail into [[CloudWatch Logs]] or [[S3]]
4. A trail can be applied to All Regions (default) or single.
5. If a resource is deleted, investigate CloudTrail first.


### Log File Integrity Validation

1. Digest Files
	1. Ref the log files for the last hour and contains a hash of each
	2. Stored in the same [[Buckets]] as log files
2. Helps determine whether the log file was modified/deleted after CloudTrail delivered it
3. Hashing using SHA-256, Digital Signing using SHA-256 with RSA
4. Protect the S3 bucket with bucket policy, versioning, MFA Delete protection, encryption, object lock

### Integration with [[EventBridge]]

1. Used to react to ANY API call being made in your account
2. CloudTrail is NOT realtime, within 15min and log files to bucket every 5 min

### Org Trails

A trail that will log all events for all accounts in org, members can view only


# NOTE

[[CloudWatch Logs|CloudWatch]] vs CloudTrail vs [[Config]]

## CloudWatch

1. Performance monitoring (metrics, CPU, network, etc.) & dashboards
2. Events & Alerting
3. Log Aggregation & Analysis

## CloudTrail

1. Record API calls made within your Account by everyone
2. Can define trails for specific resources
3. Global Service

## Config

1. Record configurational changes
2. Evaluate resources against compliance rules
3. Get timeline of changes and compliance