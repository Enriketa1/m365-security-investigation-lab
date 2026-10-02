# Email Header Analysis

I reviewed two legitimate emails from my own Gmail mailbox to practice reading authentication and routing information. I did not click links or open attachments as part of the review.

## Sample 1

The first message was an H&M membership email.

### Evidence reviewed

- From domain: `email.hm.com`
- Reply-To domain: `hm.com`
- Return-Path domain: `email.hm.com`
- SPF: PASS
- DKIM: PASS
- DMARC: PASS
- DKIM signing domain: `email.hm.com`
- Message-ID domain: `email.hm.com`
- TLS was present in the delivery chain

### Assessment

I did not find an obvious sender-spoofing indicator in the header information I reviewed. The authentication checks passed and the sender-related domains were reasonably consistent.

I would treat the message as likely legitimate based on the available header evidence, but I would not use SPF, DKIM, or DMARC alone to decide that a message or link is safe.

## Sample 2

I repeated the review with a Forage email. The message also passed SPF, DKIM, and DMARC. This gave me a second legitimate sample to compare against different mail infrastructure.

## Fields I checked

From, Reply-To, Return-Path, Message-ID, Received, Authentication-Results, SPF, DKIM, and DMARC.

Personal recipient information and full raw headers are intentionally not published.
