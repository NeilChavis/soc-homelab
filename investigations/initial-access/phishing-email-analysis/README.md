# Phishing Email Analysis

## Scenario Overview
This investigation documents the analysis of a suspicious payment failure email designed to impersonate a cloud service provider.

The objective was to review the sender identity, embedded URL, and authentication results to determine whether the message was legitimate or part of a phishing attempt.

## Email Description and Artifacts Collected
The email was staged as a payment failure notice that attempted to direct the user to an HTML page.

The message was suspicious because it used:
- a random sender domain
- urgent language to push for action
- abnormal header values
- a hosted external link

These indicators suggested the email was likely a phishing attempt to steal sensitive information.

Artifacts collected during the investigation included:
- Sender address
- Return-Path
- Sending IP address
- Embedded URL
- Email header authentication results
- Message body content

## Artifact Analysis
### Sender Analysis
The sender was suspicious because the From and Return-Path fields both used randomized domains that did not align with any legitimate cloud provider.

This mattered because the sender identity did not match the service the email claimed to represent.

This suggested the email likely originated from attacker controlled or otherwise suspicious infrastructure.
### URL Analysis
The embedded URL pointed to a file hosted on `storage[.]googleapis[.]com`.

This was notable because the root domain is legitimate Google infrastructure, but the hosted HTML file itself did not appear to lead to a real billing page.

VirusTotal relationship data also showed the domain is commonly communicated with and referenced by files, which suggests the platform can be abused to host or deliver malicious content.
### Authentication Analysis
Authentication analysis showed that SPF and DKIM passed for the sending domain.

However, these results only validated the suspicious sender domain itself and did not establish trust in the claimed cloud provider.

As a result, the authentication results did not reduce the phishing assessment.

## Suggested Defensive Measures
The sender domain, sending IP address, and embedded malicious URLs should be reviewed for blocking.

The message should also be reported as phishing and removed from any other user inboxes if found.

Because the embedded link used legitimate Google cloud infrastructure, defenders should avoid broadly blocking the entire root domain unless a more targeted control is not possible.

## Investigation Conclusion
Based on the suspicious sender identity, deceptive payment themed lure, misuse of trusted cloud hosting, and authentication results that only validated the suspicious sender domain, this email was assessed as a malicious phishing attempt.

The evidence suggested the attacker used believable branding and legitimate hosting infrastructure to increase credibility and improve the likelihood of user interaction.