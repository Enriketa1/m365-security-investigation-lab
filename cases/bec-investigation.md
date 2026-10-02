# Simulated BEC Investigation

## Alert

A finance employee receives an email that appears to come from the CEO.

- Display name: Michael Turner - CEO
- Sender: `michael.turner@northstarr-demo.com`
- Reply-To: `payments@secure-mailbox.net`
- Subject: Urgent Wire Transfer - Today
- Requested payment: $18,750
- SPF: PASS
- DKIM: PASS
- DMARC: PASS
- User interaction: no reply, click, or attachment opened

## What stood out

The sender domain contains an extra **r** compared with the expected `northstar-demo.com` domain. The Reply-To address also points to a different domain.

The message asks for an urgent financial transaction and tells the employee not to call the supposed executive. Those details make the request more suspicious.

The authentication results passed, but that does not make the sender the real CEO. A sender can authenticate mail correctly for a domain they control, including a lookalike domain.

## Disposition

**Likely BEC / phishing attempt**

**Severity:** Medium

There is no evidence in the scenario that the employee interacted with the message, so I would not claim credential theft, malware execution, or financial loss.

## Recommended follow-up

- Preserve the message and header evidence.
- Report/quarantine the message through the normal security process.
- Search for other recipients of the same campaign.
- Review the lookalike sender domain and related indicators.
- Confirm with the employee that no interaction occurred.
- Verify financial requests using an established out-of-band process.

Containment or blocking actions would follow the organization's approval process.
