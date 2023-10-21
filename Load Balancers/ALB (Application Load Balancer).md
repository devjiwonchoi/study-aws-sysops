
> Layer 7 (HTTP)

### Routing tables

Based on path / hostname / query / headers

Retrieve with `X-Forwarded-` header, port, proto

### Listener Rules

![ALB Listener Rules diagram by Stephane Maarek](https://github.com/devjiwonchoi/study-aws-sysops/blob/36509294e801537074ebfdab510d6c4daab06dd6/Screenshot%202023-10-21%20at%208.24.31%E2%80%AFPM.png?raw=true)

> Great diagram by [Stephane Maarek](https://www.udemy.com/course/ultimate-aws-certified-sysops-administrator-associate/)

### Target Group Weighting

Specify weight for each [[Target Group]] on a single rule

Allows you to control the distribution of the traffic to apps

Good for blue/green deployment.