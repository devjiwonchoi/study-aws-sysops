
## `cfn-init`

Helps complex [[EC2]] config readable, EC2 instance will query the [[CloudFormation]] service to get init data, then the logs go to `/var/log/cfn-init.log`

### `cfn-signal`

Run right after [[User Data#`cfn-init`|cfn-init]] then returns if service is going on or failing
Need to define `WaitCondition`

When fail, investigate, fix or [[Rollback]].