# Splunk Searches Used

## Successful logons
index=* EventCode=4624

## Privileged logons
index=* EventCode=4672

## Combined events
index=* (EventCode=4625 OR EventCode=4672)
