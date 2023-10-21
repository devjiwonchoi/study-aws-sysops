
> Layer 7 (HTTP)

### Routing tables

Based on path / hostname / query / headers

Retrieve with `X-Forwarded-` header, port, proto

### Listener Rules

![[Screenshot 2023-10-21 at 8.24.31 PM.png]]

> Great diagram by [Stephane Maarek](https://www.udemy.com/course/ultimate-aws-certified-sysops-administrator-associate/)

### Target Group Weighting

Specify weight for each [[Target Group]] on a single rule

Allows you to control the distribution of the traffic to apps

Good for blue/green deployment.