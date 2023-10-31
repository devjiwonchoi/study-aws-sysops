> Send logs to: [[S3]] (export), Kinesis Data Streams/Firehose, [[Lambda]], OpenSearch
> Logs are encrypted by default
> Can setup KMS-based encryption with own keys
## Log Groups

Arbitrary name, usually representing an app

## Log Streams

Instances within app / log files / containers

### Logs Subscriptions

Get real-time log events - send to Kinesis, Lambda, etc.

Cross-Account is possible