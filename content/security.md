---
uid: security
---

# Security

PI Cloud Connect deploys several levels of security to keep your information secure and still allow users access to the data they need. Security levels include: infrastructure level, account level, sign-in level, and user level.

- At the infrastructure level: PI Cloud Connect uses the HTTP protocol in conjunction with Transport Layer Security (TLS) 1.2 to form an HTTPS connection for the secure encryption of all in-transit data. PI Cloud Connect authenticates calls between the customer portal using Microsoft Accounts in conjunction with OSIsoft’s access control services. PI Cloud Connect also makes secure calls to the PI Data Archive and PI AF utilizing "claims-aware" tokens. This allows the Windows service that runs on-premises to map the claims-aware security token that it receives from PI Cloud Connect to a Windows security token on-premises.

- At the account level: an account represents a company, partner, or affiliate that has signed up for the PI Cloud Connect. Each account is fully isolated from other accounts.

- At the sign-in level: to access PI Cloud Connect features, all users must sign in to their secure customer portal and authenticate using a Microsoft account.

- At the user level: When publishing data, the publisher decides which users have access to subscribe to publications. This is done on a per user basis, not a per account basis.

For additional information regarding the security configuration for the on-premises PI Connect service account, see [Download and install PI Cloud Connect](xref:download-and-install).
