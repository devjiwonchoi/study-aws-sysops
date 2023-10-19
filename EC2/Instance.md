So basically, EC2 is a service that rents the instances, which are virtual servers running on the AWS data center.

For types, see [[Purchasing Options]]

When you launch an EC2 instance and you get this error `InstanceLimitExceeded`, then you have **reached your limit of a maximum number of <u>vCPUs per AWS Region</u>**. Either launch the EC2 instance in a different AWS Region or contact AWS Support to increase your limit of the AWS Region.

`InsufficientInstanceCapacity` error occurs when AWS does not have enough on-demand capacity in <u>particular AZ</u>.
