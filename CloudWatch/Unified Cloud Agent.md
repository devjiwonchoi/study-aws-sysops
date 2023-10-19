This is for Virtual Servers (EC2 instances, on-premise servers, etc.)

Collect additional system metrics such as RAM (which [[Metrics For EC2]] couldn't do), processes, used disk space, etc.

Collect logs from inside EC2 to send to CloudWatch Logs
	No logs will be sent to CloudWatch Logs if not set an agent.

Centralize Config by SSM Parameter Store

`CWAgent` is default namespace for metrics collected by Unified Cloud Agent.

## Procstat Plugin

- Collect metrics and monitor system utilization of individual process
- Select which process to monitor by:
	- pid_file: name of PID (Process Identification Number) files they create
	- exe: process name that match string you specify (regex)
	- pattern: command lines used to start the process (regex)
- Metrics collected by procstat plugin starts with "procstat" prefix