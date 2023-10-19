Automated checks to identify hardware & software issues

### System Status Check

- Monitors problems on AWS Systems
	- Loss of network connectivity
	- Loss of system power
	- Software issues on the physical host 
	- Hardware issues on the physical host that impact network reachability
- Personal Health Dashboard - scheduled critical maintenance by AWS
	- If failure on AWS Hardware, choose one:
		- Wait for AWS to fix the host
		- Stop and start the instance - [[Elastic IP#^restart-instance-changes-ip|which will migrate to new host]]

### Instance Status Check

- Monitors SW/network config of **individual** instance
    - Incorrect networking or startup configuration
    - Exhausted memory
    - Corrupted file system
    - Incompatible kernel
- If failure, reboot or change instance config

### Automating & Recovery

#### CW Metrics (1 min interval)

1. CloudWatch Alarm - Recommended ^be8f04
	1. Recover with same public / private IP, EIP, metadata, Placement Group ^bd76fb
	2. Send Notification by SNS
2. ASG (Auto Scaling Group)
	1. Set min/max/desired 1 to recover instance
	2. Won't keep the same [[#^bd76fb | public / private IP, etc.]]

#### [[#^be8f04|CW Alarm Action]]

1. Use "Recover" to recover from physical host issue from AWS
2. Use "Reboot" to recover from SW issues