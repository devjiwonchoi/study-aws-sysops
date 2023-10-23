
When using event source mapping like [[CloudWatch and EventBridge]] or S3, Lambda uses the execution role to read the event data.

Best practice: One execution role per [[Lambda]] function.