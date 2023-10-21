## Goals

1. Scale in/out (add/remove EC2 instances) to match (increased/decreased) the incoming load
2. Ensure min/max number of EC2 instances running
3. Automatically register new instances to a load balancer
4. Re-create an instance in case a prev one is terminated

Note: ASG is FREE

Possible to scale based on CloudWatch