
By default, when restart an instance, it changes its public IP.

To have a fixed IP, use Elastic IP.

Elastic IP is a IPv4 that you can reserve and attach to an instance at a time.

Don't pay for it unless it's detached from a server.

By default you can have 5 Elastic IPs per account (request AWS to increase it)

## Usage

Replace failed instance to another

### Alternates (Recommended)

1. Use DNS name
2. Use Load Balancer with static hostname