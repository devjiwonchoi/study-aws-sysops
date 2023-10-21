
[[ELB (Elastic Load Balancer)]]'s entry group of these:

- EC2 instances
- ECS tasks
- Lamda functions
- IP Adresses

> You can't specify publicly routable IP addresses. - public IPv4
### Settings

- [[Deregistration Delay (Connection Draining)]] seconds
- [[#^d29493|Slow Start Mode]]
- Algorithm Type - how the load balancer selects targets when routing requests ([[#^8d2b5e|Round Robin]], [[#^9b78aa|Least Outstanding Requests]])
- [[Sticky Sessions]]
	- type ([[Sticky Sessions]] app-based or duration based cookie)
	- [[Sticky Sessions#App-based Cookies]] - cookie name, cookie duration
	- [[Sticky Sessions#Duration-based Cookies]] - expiration period

### Slow Start Mode

^d29493

- Gives healthy targets time to warm-up before load balancer sends full share of requests
- Load balancer linearly increases the number of requests until:
	- The duration period elapses
	- The target becomes unhealthy

### Request Routing Algorithms

> Works with [[ALB (Application Load Balancer)]] and CLB
#### Least Outstanding Requests

^9b78aa

The next instance to receive the request is the instance with lowest number of pending/unfinished requests

#### Round Robin

^8d2b5e

Equally choose the targets from the target group

#### Flow Hash

> Works with [[NLB (Network Load Balancer)]]

Selects target based on the protocol, source/destination IP address || port, and TCP sequence number

Each TCP/UDP connection is routed to a single target for the life of the connection