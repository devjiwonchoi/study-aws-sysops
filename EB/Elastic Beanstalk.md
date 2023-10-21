
(pretty used to this, no worries on this topic)

Just upload the code, and AWS will handle the other (ALB, ASG, EC2, etc.)

### Application

- version
- environment(s)
	- tiers
		- Web Server
		- Worker - something for SQS to send messages

### Deployment Modes

- Single Instance
- High Availability with ALB, RDS, etc.