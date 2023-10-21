
### Dynamic Scaling Policies

1. Target Tracking Scaling - Most simple, easy to set up
2. Simple / Step Scaling - When CloudWatch alarm is triggered, then do something
3. Scheduled Actions - Scale based on scheduling

### Predictive Scaling

Continuously forecast load and schedule scaling **ahead**

Note: Good metrics to scale - `CPUUtilization`, `RequestCountPerTarget`, Average Network I/O

![ASG Scaling Plans PPT by Stephane Maarek](https://github.com/devjiwonchoi/study-aws-sysops/blob/23426cb768b7fe5992c2320933c7f7e3a4e5f390/Screenshot%202023-10-21%20at%2010.44.50%E2%80%AFPM.png?raw=true)