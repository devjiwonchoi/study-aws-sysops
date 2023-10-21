
### SSL, TLS Certs

Allows traffic between client to load balancer to be encrypted in transit (in-flight encryption)

`User -> HTTPS (encrypted) -> Load Balancer -> HTTP (private VPC) -> EC2 Instance`

Manage via ACM (AWS Certificate Manager) or upload own certs

### SNI on Load Balancers

> Works on [[ALB (Application Load Balancer)]], [[NLB (Network Load Balancer)]], CloudFront

Handles multiple SSL certs, requires the client to indicated the hostname of the target server in the initial SSL handshake, and the server will find the correct cert or return default

![[Screenshot 2023-10-21 at 7.45.12 PM.png]]

> Great diagram by [Stephane Maarek](https://www.udemy.com/course/ultimate-aws-certified-sysops-administrator-associate/)

Therefore [[ALB (Application Load Balancer)]] and [[NLB (Network Load Balancer)]] can handle multiple certs and multiple [[Target Group]] using SNI.