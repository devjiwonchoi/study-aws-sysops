
All [[Lambda]] execution logs are automatically stored to [[CloudWatch Logs]].

### CloudWatch Metrics

### X-Ray

1. Enable in [[Lambda]] configuration (Active Tracing)
2. Runs X-Ray daemon
3. Use X-Ray SDK in the Lambda code.
4. [[Execution Role (IAM Role)]] : `AWSXRayDaemonWriteAccess`

- `AWS_XRAY_DAEMON_ADDRESS` : X-Ray daemon `ip address:port`
- 