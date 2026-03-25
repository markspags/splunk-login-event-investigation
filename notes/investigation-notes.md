# Investigation Notes

## Investigation Question
Does this login activity represent expected administrative behavior or potentially risky privileged access?

## Scope of Analysis
- Reviewed Windows authentication logs in Splunk
- Focused on successful logon events (4624)
- Reviewed privileged access events (4672)

## Observations
- A successful login (EventCode 4624) was identified
- A privileged logon event (EventCode 4672) followed the authentication
- This indicates that the account session was granted elevated privileges

## What This Means
The combination of a successful login followed by privileged access suggests that:
- the account has administrative-level permissions, or
- the session triggered elevated privileges upon login

## Risk Considerations

### This activity may be expected if:
- the account is a known administrator
- the system regularly assigns privileges to that account
- the login occurred during normal usage

### This activity may be risky if:
- the account is not typically privileged
- the login occurred at an unusual time
- the source system or workstation is unfamiliar
- the behavior deviates from normal patterns

## Analyst Assessment
Privileged logon events represent higher-risk activity and should always be reviewed in context. Without additional indicators of compromise, this activity cannot be confirmed as malicious but warrants validation.
