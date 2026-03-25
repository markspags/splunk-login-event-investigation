# Splunk Login Event Investigation

## Objective
Analyze Windows authentication events in Splunk to identify and assess privileged login activity and determine whether the behavior appears expected or potentially risky.

## Scenario
This project reviews Windows Event Logs in Splunk, focusing on successful authentication events and privileged access assignments. The goal is to evaluate how elevated access is granted and whether such activity warrants further investigation.

## Tools Used
- Splunk (SIEM)
- Windows Event Logs
- Windows 11 Virtual Machine

## Relevant Event Codes
- 4624 = Successful logon  
- 4672 = Special privileges assigned to new logon  

## Investigation Steps
1. Identify successful login events (EventCode 4624)  
2. Review associated privileged login events (EventCode 4672)  
3. Correlate login activity with elevated privilege assignment  
4. Evaluate whether privileged access aligns with expected user behavior  
5. Assess potential risk based on account context and activity patterns  

## Queries Used
See `queries/splunk-searches.md`

## Evidence
Event log samples and analysis notes are included in the repository.

## Findings
- A successful login event (4624) was identified  
- A privileged logon event (4672) was observed following authentication  
- The event sequence indicates that the account was granted elevated privileges during the session  

## Analysis
Privileged logon events represent higher-risk activity because they provide elevated access to critical system functions. While this behavior may be expected for administrative accounts, it becomes a concern if:
- the account is not typically privileged  
- the login originates from an unfamiliar system  
- the timing of the login is unusual  

## Conclusion
This project demonstrates how to identify and assess privileged login activity using Splunk. Monitoring and validating privileged access events is critical to detecting potential misuse, unauthorized access, or escalation of privileges within an environment.
