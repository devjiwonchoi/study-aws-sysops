
Names must be globally unique name, and not include `xn--` or `-s3alias`

### Policies

1. User Based: [[IAM]] Policies - which API calls should be allowed for a specific user from IAM
2. Resource-Based
	1. Bucket Policies - bucket wide rules from the [[S3]] console
	2. Object Access Control List (ACL) - finer grain (can be disabled)
	3. Bucket Access Control List (ACL) - less common (can be disabled)

Note: IAM principal can access an S3 object IF:
1. There's no explicit DENY
2. IAM permissionsOR resource policy allows it

### Versioning

1. Enabled at bucket level
2. If not versioned, it'll be version as 'null'
3. Suspending versioning won't delete previous versions
