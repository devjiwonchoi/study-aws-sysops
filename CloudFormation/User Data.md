
## `cfn-init`

Helps complex [[EC2]] config readable, EC2 instance will query the [[CloudFormation]] service to get init data, then the logs go to `/var/log/cfn-init.log`

### `cfn-signal`

Run right after [[User Data#`cfn-init`|cfn-init]] then returns if service is going on or failing
Need to define `WaitCondition`

When fail, investigate, fix or [[Rollback]].

Q:
You would like to troubleshoot why an EC2 instance keeps on failing to correctly bootstrap itself using the `cfn-init` signal. Each time, it fails, and then sends the `cfn-signal` to CloudFormation. Therefore, CloudFormation fails and deletes the newly created resources. What should you do?

You can configure the CloudFormation stack to do nothing when there's a failure so you can troubleshoot the error. To do so, configure the "onFailure" option while creating the stack.