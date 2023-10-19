
## Cluster

Clustered instances on single rack, single AZ 

- Low latency, great network (10Gbps)
- If the rack fails, all instances fail also.

### Spread

Each instances are placed to a different rack, different AZ

- Safe from the rack or AZ failure
- Limit to 7 per group

### Partition

Instances can be placed on partitions, which uses separate racks each.

- Up to 100 instances per partitions
- Up to 7 partitions per AZ