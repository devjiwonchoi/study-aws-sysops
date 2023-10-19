- If exceed configured max price, 2 min grace period whether to [[Shutdown Behavior#Stop (default) |Stop]] or [[Shutdown Behavior#Terminate|Terminate]] the instance.

### Spot Block

Claim an instance for a specified time (1~6 hr)

### Types of Spot Instance Request

1. One-Time - As soon as the instances launch, the request will go away.
2. [[#Persistent Type|Persistent]] - Specified number of instances will be active until the specified time range.

### Persistent Type

The request will be valid until you cancel the request.
Therefore, if you want to terminate the instances requested by persistent request type, you have to first cancel the request then terminate the associated instances.
Otherwise, the request will restart to launch the instances for you.



