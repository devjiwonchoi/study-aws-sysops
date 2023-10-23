### RAM

1. From 128MB ~ 10GB in 1MB increment.
2. Increase RAM => vCPU credit increases.
	1. Cannot manually increase vCPU only.
	2. If app is CPU-bound, just increase RAM
3. Timeout: default 3 sec, min 1 sec, max 900 sec (15 min)

### Execution Context (environment)

Temporary runtime environment that inits any external deps of [[Lambda]] codes.
Can be re-used and save time init connection

##### `/tmp` Directory

1. Good to use when [[Lambda]] needs to download big file to work or needs disk space to perform
2. 10 GB of use space
3. Provides caching method to used for multiple invocation
4. If the object needs to be permanent persistence, use S3
5. To encrypt, use KMS Data Keys
