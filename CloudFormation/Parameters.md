
Provide inputs to [[CloudFormation]] template

Reusable

![Parameters Settings by Stephane Maarek](https://github.com/devjiwonchoi/study-aws-sysops/blob/main/Screenshot%202023-10-23%20at%207.29.08%E2%80%AFPM.png?raw=true)

Reference parameter using `!Ref`

### Pseudo Params

## `AWS::AccountId`

Returns the AWS account ID of the account in which the stack is being created, such as `123456789012`.

## `AWS::NotificationARNs`

Returns the list of notification Amazon Resource Names (ARNs) for the current stack.

To get a single ARN from the list, use [Fn::Select](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-select.html).

## `AWS::NoValue`

Removes the corresponding resource property when specified as a return value in the `Fn::If` intrinsic function.

For example, you can use the `AWS::NoValue` parameter when you want to use a snapshot for an Amazon RDS DB instance only if a snapshot ID is provided. If the `UseDBSnapshot` condition evaluates to true, CloudFormation uses the `DBSnapshotName` parameter value for the `DBSnapshotIdentifier` property. If the condition evaluates to false, CloudFormation removes the `DBSnapshotIdentifier` property.

Returns the partition that the resource is in. For standard AWS Regions, the partition is `aws`. For resources in other partitions, the partition is `aws-``partitionname`. For example, the partition for resources in the China (Beijing and Ningxia) Region is `aws-cn` and the partition for resources in the AWS GovCloud (US-West) region is `aws-us-gov`.

## `AWS::Region`

Returns a string representing the Region in which the encompassing resource is being created, such as `us-west-2`.

## `AWS::StackId`

Returns the ID of the stack as specified with the `aws cloudformation create-stack` command, such as `arn:aws:cloudformation:us-west-2:123456789012:stack/teststack/51af3dc0-da77-11e4-872e-1234567db123`.

## `AWS::StackName`

Returns the name of the stack as specified with the `aws cloudformation create-stack` command, such as `teststack`.

## `AWS::URLSuffix`

Returns the suffix for a domain. The suffix is typically `amazonaws.com`, but might differ by Region. For example, the suffix for the China (Beijing) Region is `amazonaws.com.cn`.

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/pseudo-parameter-reference.html