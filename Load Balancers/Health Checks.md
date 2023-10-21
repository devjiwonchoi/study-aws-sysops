
Let the load balancers know if the instance is good to forward traffic.

Health checks are done by accessing port and route. (common by /health)

If response is not 200 (OK), then the instance is unhealthy, and the load balancers will not send traffic to the certain instance.