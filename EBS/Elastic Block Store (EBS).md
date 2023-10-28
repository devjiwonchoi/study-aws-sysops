
EBS is a network drive, not hard drive. Allows the [[EC2]] instances to persist data even after termination.

- Only mounted to ONE INSTANCE, ONE AZ AT A TIME
- Cannot decrease size. Need to create smaller volume then migrate.
- When increase, do on flight, then repartition.

### Multi Attach

Can attach to multiple instances (max 16) within the AZ

### Migration to different AZ

[[Snapshots|Snapshot]] the volume, then create a volume from the snapshot in different AZ.

### Encryption

When enabled, the data, in-flight, snapshots, volumes created from snapshots are encrypted with KMS key (AES-256).

When encrypt UNENCRYPTED volume, create [[Snapshots]], encrypt the snapshot, create new volume from the snapshot, then attach new volume to the instance.