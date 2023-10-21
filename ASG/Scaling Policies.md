
### Dynamic Scaling Policies

1. Target Tracking Scaling - Most simple, easy to set up
2. Simple / Step Scaling - When CloudWatch alarm is triggered, then do something
3. Scheduled Actions - Scale based on scheduling

### Predictive Scaling

Continuously forecast load and schedule scaling **ahead**

Note: Good metrics to scale - `CPUUtilization`, `RequestCountPerTarget`, Average Network I/O

![[Screenshot 2023-10-21 at 10.44.50 PM.png]]