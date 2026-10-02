# Microsoft 365 Identity Investigations

These cases use fictional Microsoft 365 / Entra ID scenarios. They are investigation exercises only and do not contain live tenant data.

## Case 1 - Unusual geographic activity

A user successfully signs in from New York at 9:05 AM. Twenty-seven minutes later, the same account signs in from Albania from an unfamiliar IP and unmanaged Windows device. MFA is reported as satisfied.

**Disposition:** Undetermined / requires additional investigation  
**Severity:** Medium

The timing and change in location are unusual, and the unfamiliar IP and device add risk. I would not call the account compromised from this evidence alone. I would review MFA details, Conditional Access, device information, previous sign-ins, related alerts, and recent account changes, then confirm the activity with the user.

## Case 2 - Possible password spray

Twenty Microsoft 365 accounts receive one or two failed sign-in attempts each from the same previously unseen external IP during 15 minutes. No successful sign-in from that IP is identified.

**Disposition:** Suspected password-spray activity  
**Severity:** Medium

The pattern matters because the attempts are spread across many accounts. I would preserve timestamps, targeted accounts, source IP, applications, failure reasons, authentication methods, Conditional Access results, and related alerts. I would then look for later successful sign-ins, new devices/IPs, privileged accounts, or MFA anomalies.

## Case 3 - Unexpected administrator role

At 11:40 PM, a standard user is assigned the Helpdesk Administrator role by an existing Global Administrator. There is no approved change ticket and the user does not normally perform administrative work.

**Disposition:** Unauthorized privileged-role assignment suspected  
**Severity:** High pending validation

I would preserve the role-assignment record and review the administrator's sign-in activity, source IP/device, MFA and Conditional Access results, nearby administrative changes, activity by the affected user, and available approval records. The change should also be independently confirmed.

Removing the role, revoking sessions, resetting passwords, or disabling accounts would require the appropriate authorization.

## Investigation workflow

**Preserve alert → review sign-ins → check MFA/Conditional Access → review IP/device/location → compare user context → correlate related activity → classify → assign severity → recommend containment → escalate/document**
