# Microsoft 365 Security Investigation Lab

This project documents email and identity-security investigation practice. I used real email headers from messages in my own mailbox for the authentication review and fictional scenarios for the Microsoft 365 identity cases.

No employer, client, or production data is included.

## What I worked on

- Email header review
- SPF, DKIM, and DMARC validation
- Business email compromise indicators
- Unusual sign-in investigation
- Password-spray analysis
- Privileged-role activity
- Severity and escalation decisions

## Cases

### [Email Header Analysis](cases/email-header-analysis.md)
Reviewed legitimate email headers and compared sender information, Return-Path, Reply-To, Message-ID, authentication results, and delivery information.

### [Simulated BEC Investigation](cases/bec-investigation.md)
Investigated an executive-impersonation scenario involving a lookalike domain, unusual Reply-To address, and urgent wire-transfer request.

### [Microsoft 365 Identity Investigations](cases/identity-investigations.md)
Worked through three fictional identity alerts: unusual geographic activity, possible password spraying, and an unexpected administrator-role assignment.

## Main takeaway

The biggest lesson from this lab was not to rely on one indicator by itself. An email can pass SPF, DKIM, and DMARC and still be suspicious, and an unusual sign-in does not automatically prove account compromise. I need to correlate authentication results, user context, device/IP information, related activity, and the actions that followed.

> Real email samples were reviewed in my own mailbox. Public notes are sanitized. Microsoft 365 identity and BEC scenarios are simulated.
