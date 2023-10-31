Basically Content Delivery Network. (CDN)

1. Improve read performance and cached at the edge
2. DDoS protection, WAF (Web App Firewall), integration with Shield

## Origins

- [[Buckets|S3 Buckets]]
- Custom HTTP Origin
- [[ALB (Application Load Balancer)]] (ALB must be public, but the EC2 instance may be private)
- [[EC2]] (Allow public ip of Edge locations, and the instance must be public)

Note: Good for static content EVERYWHERE, for dynamics [[S3]] Cross Region Replication is good for low-latency in few regions