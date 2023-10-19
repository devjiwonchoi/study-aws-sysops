> Based on the request within the OS, not the console.
### Stop (default)

The instance may stop, and will remain as stopped.

**The data on disk (EBS) is kept intact on the next start**
### Terminate

If the instance is shutdown, it will terminate the instance it is GONE.

**Any EBS volumes (root) also set-up to be destroyed is LOST.**

#### Terminate Protection

If enabled, it is unable to terminate by console.

Note: If shutdown by OS, it will still terminate the instance.

See [[Hibernate - Instance Never Stops!]]