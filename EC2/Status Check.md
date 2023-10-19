Automated checks to identify hardware & software issues

### System Status Check

- Monitors problems on AWS Systems
- Personal Health Dashboard - scheduled critical maintenance by AWS
	- If failure on AWS Hardware, stop and start the instance - [[Elastic IP#^restart-instance-changes-ip|which will migrate to new host]]

### Instance Status Check

- Monitors SW/network config of instance
- If failure, reboot or change instance config

### Automating & Recovery

#### CW Metrics (1 min interval)

1. CloudWatch Alarm - Recommended
	1. Recover with same public / private IP, EIP, metadata, Placement Group ^bd76fb
	2. Send Notification by SNS
2. ASG (Auto Scaling Group)
	1. Set min/max/desired 1 to recover instance
	2. Won't keep the same [[#^bd76fb | public / private IP, etc.]]
