
ELB is managed by AWS.

Health Checks available.

End point for users, and distribute the load(connection) to instances.

Types of ELB:

1. Classic Load Balancer (legacy)
2. [[ALB (Application Load Balancer)]] - HTTP, HTTPS, WebSocket
3. [[NLB (Network Load Balancer)]] - TCP, TLS
4. [[GWLB (Gateway Load Balancer)]] - Operates at Network layer - IP Protocol

Link security group of instance to load balancers.

### Monitoring and Logs

Logs can be sent to S3