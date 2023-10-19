Default behavior when starting instance without Hibernate:

1. OS booting starts, EC2 User Data Script runs
2. OS boots up
3. App starts, cache gets warmed up - takes time

Hibernate lets the OS not stopped or restarted... It just hibernates!

1. RAM state is preserved - written in file in root EBS volume ^4e02ea
2. Instance boot much faster
3. EBS volume must be encrypted

Instance running -> Instance Stopping ([[#^4e02ea|copy RAM state to a file, write to root EBS volume]]) -> Instance Stopped (RAM goes away) -> Running (RAM state loaded from EBS root volume to Instance's memory)

### Use-case

1. Long running process
2. Save RAM state
3. Service takes long time to initiate