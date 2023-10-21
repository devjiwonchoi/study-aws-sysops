
Let the load balancers know if the instance is good to forward traffic.

Health checks are done by accessing port and route. (common by /health)

If response is not 200 (OK), then the instance is unhealthy, and the load balancers will not send traffic to the certain instance.

### ELB Health Status

1. Initial - registering the target
2. Healthy - 200 OK
3. Unhealthy - Other than 200 OK
4. Unused - target not registered
5. Draining - de-registering the target (see [[Deregistration Delay (Connection Draining)]])
6. Unavailable - health checks disabled

Note: If all targets in [[Target Group]] are unhealthy, ELB routes requests across its unhealthy targets.