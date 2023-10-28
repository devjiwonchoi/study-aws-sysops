
Not necessary, but recommended. - stored in S3 internally.

### Fast Snapshot Restore (FSR)

No I/O latency.
Helps create a volume from a snapshot that is fully initialized at creation.

### Snapshot Archive

Move the snapshot to "archive tier" - 75% cheaper (stays 24~72hr to restore)

### Snapshot Recycle Bin

Set retention rules for deleted snapshots - able to recover from accidental deletion
Specify retention (1day ~ 1yr)