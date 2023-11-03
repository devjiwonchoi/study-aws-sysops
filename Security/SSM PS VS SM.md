
[[Parameter Store]] vs Secrets Manager

## Secrets Manager

1. Automatic rotation of secrets with [[Lambda]]
2. [[Lambda]] is provided for [[RDS (Relational Database Service)]], Redshift, DocumentDB
3. [[KMS (Key Management Service)]] encryption is mandatory
4. Can integrate with [[CloudFormation]]

## [[Parameter Store]]

1. Simple API
2. No secret rotation (can enable rotation using [[Lambda]] triggered by [[EventBridge]])
3. [[KMS (Key Management Service)]] encryption is optional
4. Can integrate with [[CloudFormation]]
5. Can pull a [[#Secrets Manager]] secret using the SSM Parameter Store API