AMI is basically an image of EC2 instance.

AMI is useful when want to migrate instances from AZ to AZ.

When sharing AMI to different account (cross-account) the EBS volume can be encrypted or not.

If encrypted, need to share the CMK (Customer Managed Key) also.

The account that has been shared will use that CMK to decrypt the volume, that encrypted with their own CMK.

Pre-configured AMI for creating other AMIs is called Golden AMI