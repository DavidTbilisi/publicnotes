---
tags:
  - it/ProgrammingLanguages
---
![[Logging_best_practice.png]]
## Error details
- Where: file, function, line
- When: timestamp timezone
- Log Level:
	- DEBUG - Detailed information for diagnosing problems.
	- INFO - General operational events (e.g., startup, shutdown, configuration).
	- WARNING - Potentially harmful situations (e.g., deprecated APIs, low disk space)
	- ERROR - Errors that allow the application to continue running.
	- CRITICAL - Severe errors that require immediate attention (e.g., service crashes).
- Source (file, function, or module name)
- Identifiers/Context (user ID, transaction ID)
- Message
- Error details (stack traces if available)
## Structured logs
- JSON

## Logs sampling
for memory saving
???

## Retention policy
Rotate and Archive Logs

using tags? 

Use asynchronous logging to reduce performance impact.

Telemetry aggregator of logs



https://youtu.be/9L77QExPmI0?si=e_tAxik73oHTjg5k

[Знакомство с модулем logging в Python](https://youtu.be/dmJVJ9eFVn4?si=auNTnGiYwXq_5Lld)