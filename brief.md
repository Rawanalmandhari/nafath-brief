Version: NAFATH-V1
Track: Networking

## Overview
Building a national single sign-on (SSO) service requires seamless integration across six IT fields. OpenID Connect and OAuth 2.0 establish secure authentication and authorization standards across platforms. Android runtime permissions ensure mobile applications collect only essential user data, safeguarding privacy on mobile devices. To identify suspicious logins automatically, an AI risk engine applies risk management frameworks to mitigate operational and algorithmic risks. All systems are enforced with phishing-resistant multi-factor authentication to secure user sessions against credential theft. All implementations comply with Oman’s Personal Data Protection Law, ensuring civil data is lawfully processed and stored. Above all, resolving network queries securely against interception and tampering relies on DNS over HTTPS (DoH).

## Software
OAuth 2.0 provides delegated authorization by issuing access tokens for resource access without sharing credentials. Conversely, OpenID Connect (OIDC) is an authentication identity layer built on OAuth 2.0 that uses ID Tokens (JWTs) to verify user identity. In NAFATH-V1, OIDC handles single sign-on user logins, while OAuth 2.0 manages delegated permissions for connected government services.

Resource: Final: OpenID Connect Core 1.0 incorporating errata set 2 - https://openid.net/specs/openid-connect-core-1_0.html

## AI
Deploying AI to flag suspicious logins requires managing risks using frameworks like NIST AI RMF. Essential risks include algorithmic bias against valid demographics, false positive lockouts, privacy leaks from behavioral data, and vulnerability to adversarial manipulation. These risks must be audited before live deployment to ensure fair, secure, and reliable fraud detection.

Resource: Artificial Intelligence Risk Management Framework (AI RMF 1.0) - https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf

## Mobile
Android’s runtime permission model restricts application access to sensitive system resources until explicitly requested at runtime. The NAFATH-V1 mobile application must prompt citizens for permissions, such as camera or notifications, only when required for biometric verification or authentication alerts, ensuring compliance with least privilege principles.

Resource: Request runtime permissions | Android Developers - https://developer.android.com/training/permissions/requesting

## Networking
DNS over HTTPS (DoH) encrypts domain name lookups via HTTPS protocols. It protects NAFATH-V1 users from eavesdropping, man-in-the-middle attacks, and DNS spoofing on public networks. However, DoH does not conceal destination IP addresses, shield against endpoint compromise, or encrypt data payloads after initial DNS resolution is complete.

Resource: RFC 8484 - DNS Queries over HTTPS (DoH) - https://datatracker.ietf.org/doc/html/rfc8484
## Cybersecurity
Phishing-resistant authentication binds login credentials cryptographically to the specific origin domain, preventing credential interception by proxy sites. Hardware security keys (FIDO2/WebAuthn) and platform passkeys qualify as phishing-resistant. Conversely, SMS OTPs, email codes, and basic push notifications do not qualify because attackers can relay them through fraudulent login pages.

Resource: Digital Identity Guidelines: Authentication and Lifecycle Management - https://pages.nist.gov/800-63-3/sp800-63b.html

## Data
Under Oman’s Personal Data Protection Law (Royal Decree 6/2021), the authority must obtain explicit citizen consent, adhere to data minimization, maintain transparency, and implement security measures. The authority is legally obligated to protect personal identifiers and honor citizen rights regarding data access, rectification, and erasure.

Resource: Royal Decree 6/2021 Promulgating the Personal Data Protection Law - https://moci.gov.om/pdpl

## Misconception in My Track
A common misconception in networking is that DNS over HTTPS (DoH) provides full end-to-end anonymity and complete network privacy. In reality, DoH only encrypts DNS resolution requests between the client and resolver. It does not hide the server's target IP address, nor does it encrypt traffic data after DNS resolution occurs. RFC 8484 explicitly states that DoH does not protect against IP tracking or endpoint monitoring.

Resource: RFC 8484 - DNS Queries over HTTPS (DoH) - https://datatracker.ietf.org/doc/html/rfc8484

## Open Question
How will NAFATH-V1 handle offline identity verification or fallback authentication for citizens with limited internet connectivity?
