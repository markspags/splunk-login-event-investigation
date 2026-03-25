# Splunk Login Event Investigation

## Objective
Analyze Windows authentication events in Splunk to identify suspicious login activity.

## Scenario
This project investigates failed logons, successful logons, and privileged access events to determine whether behavior appears suspicious or normal.

## Tools Used
- Splunk
- Windows Event Logs
- Windows 11 VM

## Relevant Event Codes
- 4625 = Failed logon
- 4624 = Successful logon
- 4672 = Special privileges assigned

## Investigation Steps
1. Search for failed logons
2. Identify repeated attempts
3. Check for successful login after failures
4. Check for privileged access
5. Analyze pattern

## Queries Used
(see queries/splunk-searches.md)

## Evidence
Screenshots will be added in the evidence folder.

## Conclusion
This project demonstrates how to investigate login activity using SIEM (Splunk) and determine whether behavior is suspicious.
