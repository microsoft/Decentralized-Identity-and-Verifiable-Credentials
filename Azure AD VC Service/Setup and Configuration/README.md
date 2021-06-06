# Set up Verifiable Issuer
The tutorial from Microsoft documentation [Configure Azure Active Directory to issue verifiable credentials](https://docs.microsoft.com/en-us/azure/active-directory/verifiable-credentials/enable-your-tenant-verifiable-credentials) covers the set up of an Issuer in Azure AD tenant.

* Currently the service requires an Azue Account, Azure AD with a P2 license and Azure Key Vault service
* As service is enabled in Azure AD, a decentralized identifier (DID) is enabled for the issuance organization
* Any verifiable credential issued by the organization is issued by the tenant and its DID
* The DID is used when verifying verifiable credentails
* Cryptographic keys used by the tenant to digitally sign verifiable credentials are stored in Azure Key Vault

# Issue and verify verifiable credential
The tutorial from Microsoft documentation [Issue and verify verifiable credentials using Azure AD tenant](https://docs.microsoft.com/en-us/azure/active-directory/verifiable-credentials/issue-verify-verifiable-credentials-your-tenant) covers the issuance and verification process flow.

