
1. Multi-part upload ^43046c
	1. Good for files over 100MB, MUST for over 5GB
	2. Can help parallelize uploads (speed up)
2. Transfer Acceleration
	1. Use edge location
	2. Compatible with [[#^43046c|Multi-part upload]]
3. Byte-Range Fetches
	1. Speed up downloads by parallelize GET request by specific byte ranges
	2. Better resilience in case of failures
	3. Can be used to retrieve partial data