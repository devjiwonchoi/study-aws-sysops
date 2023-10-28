
### Server-side Encryption (SSE)

- With [[S3]] Managed Keys (SSE-S3) enabled by default 
	- header `x-amz-server-side-encryption: AES-256`
- KMS Keys (SSE-KMS)
	- header `x-amz-server-side-encryption: aws:kms`
- Customer-Provided Keys (SSE-C) own encryption keys
	- HTTPS required

### Client-side Encryption

- Use client libraries like Amazon S3 Client-Side Encryption Library
- Clients must encrypt data themselves before sending to [[S3]]
- Clients must decrypt data themselves before retrieving from [[S3]]
- Customer fully manages the keys and encryption cycle
