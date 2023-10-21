## Goals

1. Scale in/out (add/remove EC2 instances) to match (increased/decreased) the incoming load
2. Ensure min/max number of EC2 instances running
3. Automatically register new instances to a load balancer
4. Re-create an instance in case a prev one is terminated

Note: ASG is FREE

Possible to scale based on CloudWatch

Capacity: min / avg / max - ASG will not automatically increase max

## Scaling Cooldowns

cooldown period - default 300 sec

During cooldown, ASG will not launch or terminate additional instances, therefore recommended to use ready-to-use [[AMI (Amazon Machine Image)]]


### Health Checks

[[EC2]], [[ELB (Elastic Load Balancer)]], and Custom Health Check (by CLI, SDK, etc.)

ASG will launch a new instance after terminating unhealthy one

ASG will not reboot unhealthy hosts

If ASG fails to launch instance for over 24 hr, it'll suspend the process as administration suspension