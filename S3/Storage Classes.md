### General Purpose

- Frequently accessed data
- Low latency, high throughput
- Sustain 2 concurrent facility failures

### Infrequent Access

- For data less frequently accessed, but requires rapid access when needed
- Cheaper than [[S3]] standard
- S3 Standard-IA - for backups and recovery
- S3 One Zone-IA - single AZ, data lost when AZ destroyed

### Glacier Storage

Low cost, good for archiving and backup

- S3 Glacier Instant Retrieval - very short
- S3 Glacier Flexible Retrieval - average (free)
- S3 Glacier Deep Archive - long term

### Intelligent-Tiering

- Small monthly monitoring & auto-tiering fee
- Moves objects automatically between Access Tiers based on usage
- No retrieval charges

Frequent: default
Infrequent: not accessed for 30 days
Archive Instant: not accessed for 90 days
Archive: " 90~700+ days
Deep Archive: " 180~700+ days

> Note: Can move between classes manually or using [[S3]] Lifecycle config