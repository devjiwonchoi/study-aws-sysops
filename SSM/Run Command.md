
Execute [[Documents]], rate control and error control.

Can run on multiple instances with [[Resource Groups]].

No need SSH.

Output to S3 or CloudWatch Logs

Send notification to SNS

EventBridge trigger

Q:

You have a fleet of EC2 instances and you want to apply a patch to all of them without SSH into each EC2 instance. What's the easiest way to patch this fleet of EC2 instances?

- AWS Lambda
    
- Amazon CloudWatch Events
    
- SSM Resource Groups
    
- SSM Run Command