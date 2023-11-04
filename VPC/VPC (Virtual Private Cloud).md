VPC [[CIDR (Classless Inter-Domain Routing)|CIDR]] should not overlap with other networks

CIDR not should overlap, and the max CIDR size in AWS is /16


1. CIDR - IP Range
2. VPC - define a list of IPv4 and v6 CIDR
3. Subnets - tied to an AZ, define a CIDR
4. Internet Gateway - at VPC level, provide IPv4/6 Internet access
5. Route tables - must be edited to add routes from subnets to the Internet Gateway, VPC peering Connections, VPC Endpoints
6. Bastion Host - public EC2 instance to SSH into that has SSH connectivity to EC2 instances in private subnets
7. NAT Instances - gives Internet access to EC2 instances in private subnets. Old, must be setup in a public subnet, disable Source / Destination check flag
8. NAT Gateway - managed by AWS, provides scalable internet access to private EC2 instances, IPv4 only
9. Private DNS + Route 53 - enable DNS Resolution + DNS Hostnames (VPC)
10. NACL - stateless, subnet rules for inbound and outbound, don't forget Ephemeral ports
11. Security Groups - stateful, operate at the EC2 instance level
12. Reachability Analyzer - perform network connectivity testing between AWS resources
13. VPC Peering - connect two VPCs with non overlapping CIDR, non-transitive
14. VPC Endpoints - provide private access to AWS Services (S3, DynamoDB, CloudFormation, SSM) within a VPC
15. VPC Flow Logs - can be setup at the VPC / Subnet / ENI Level, for ACCEPT and REJECT traffic, helps identifying attacks, analyze using Athena or CloudWatch Logs insights
16. Site-to-Site VPN - setup a Customer Gateway on DC, Virtual Private Gateway on VPC, and site-tosite VPN over public internet
17. AWS VPN CloudHub - hub and spoke VPN model to connect your sites
18. Direct Connect - setup a virtual private gateway on vpc, and establish a direct private connection to an aws direct connect location
19. Direct Connect Gateway - setup a direct connect to many vpcs in diff aws regions
20. AWS PrivateLin / VPC Endpoint Services
	1. Connect services privately from your service vpc to custommers vpc
	2. doesnt need vpc peering public internet nat gateway route tables
	3. must be used with network load balancer and eni
21. classic link connect ec2 classic ec2 instances privately to yoyr vpc
22. transit gateway transitive peering connections for vpc vpn dx
23. traffic mirroring copy network traffic from enis for further analysis
24. egress only internet gateway like a nat gateway but ipv6