# Unit 2:

## Deploy Azure AD connect:
- Hybrid Identity is the `process of connecting your on-premises Active Directory with your Azure Active Directory`.

## Authentication methods:
- Cloud Authentication (Azure AD password hash Sync, Azure AD Pass-through Auth)
- Federated Authentication (Auth by on-premises Active Directory Federation Services (AD FS))

- Azure AD Connect features:
  1. Password hash synchronization (sync & use hash of a user on on-prem & AD) `same sign-in, not single sign-on`
    - Use this feature to sign in to Azure AD services like Microsoft 365, Microsoft Intune, CRM Online, and Azure Active Directory Domain Services (Azure AD DS).
    - This option just shares the password hash between two federated systems.
      
  2. Pass-through authentication (Same pwd can be used on on-prem & AD)
    - alternative to Azure AD Password Hash Synchronization.
    - Supports user sign-in into all web browser-based app
    - PTA is a free feature uses 

  3. Federation integration (used to configure a hybrid environment using an on-premises AD FS infrastructure)
     - Federation is a collection of domains that have established trust.
     - You can federate your on-premises environment with Azure AD and use this federation for authentication and authorization.
    
## Password writeback:
- a feature enabled with Azure AD Connect that allows password changes in the cloud to be written back to an existing on-premises directory in real time.

## Authentication protocol:
- Azure AD supports `SAML 2.0[^1] , OpenID Connect[^2], OAuth 2.0[^3], and WS-Federation protocols` for authentication and authorization.
- OpenID is an authentication protocol that allows users to use a single set of credentials to authenticate themselves across multiple websites or applications.
- OAuth (Open Authorization) is an authorization framework.
- Single Sign-On (SSO) granting you seamless access without requiring multiple logins.
- SAML 2.0 focuses on enterprise integration, while OpenID is more consumer-centric.


[^1]: SAML 2.0, which stands for Security Assertion Markup Language 2.0, is a protocol used for exchanging authentication and authorization information between different systems. Used in SSO, Federation (To build trust between 2 orgs), Azure AD.
[^2]: OpenID, verifies the user from an identity provider (like Google or Facebook) & allows access/login to the site. OpenID Connect: OpenID Connect is an authentication layer built on top of OAuth 2.0.
[^3]: OAuth 2.0, allows applications to obtain limited access to a user's resources on another system (referred to as the resource server) without sharing the user's credentials. 

