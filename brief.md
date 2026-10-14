Version: NAFATH-V1
Track: Networking

## Overview
Building a national single sign-on (SSO) service requires seamless integration across six IT fields. OpenID Connect and OAuth 2.0 establish secure authentication and authorization standards across platforms. Android runtime permissions ensure mobile applications collect only essential user data, safeguarding privacy on mobile devices. To identify suspicious logins automatically, an AI risk engine applies risk management frameworks to mitigate operational and algorithmic risks. All systems are enforced with phishing-resistant multi-factor authentication to secure user sessions against credential theft. All implementations comply with Oman’s Personal Data Protection Law, ensuring civil data is lawfully processed and stored. At the network level, domain resolution queries are secured against interception using DNS over HTTPS (DoH).

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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
