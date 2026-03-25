# Splunk Searches Used

## Successful Logon Events
Search used to identify successful authentication activity:

index=* EventCode=4624


## Privileged Logon Events
Search used to identify when elevated privileges were assigned:

index=* EventCode=4672


## Correlating Authentication Events
Search used to review both successful and privileged logon events together:

index=* (EventCode=4624 OR EventCode=4672)


## Basic Event Count by User (if available)
Used to observe frequency of activity by account:

index=* EventCode=4624 | stats count by Account_Name
