By default, the state of ASG will be `Pending` -> `InService`.

You can invoke [[Auto Scaling Group]] `Pending` state, `Pending:Wait`, and perform extra steps needed before instance goes in service (e.g. define scripts to run on instances as they start).

Then the `Pending:Wait` state will turn to `Pending:Proceed`, then `InService`.

You can also do with `Terminating` state also.

Pending -> Pending:Wait -> do something -> Pending:Proceed -> InService -> Terminating -> Terminating:Wait -> -> do something (e.g. cleanup, log extraction, special health checks, etc.)-> Terminating:Proceed -> Terminated
