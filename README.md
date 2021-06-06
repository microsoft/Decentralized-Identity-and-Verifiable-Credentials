# Why do we need Decentralized Identity (DID) and Verifiable Credentials (VCs)

The initial goal of the Word Wide Web (WWW) was to build the internet, as a decentralized architecture, with open standards so everyone could freely communicate and access information. But the current internet is largely centralized and siloed. The web traffic is controlled by few powerful organization which serves the data through platforms that selectively serve up information based on user's data and thier activity. There is no identity system native to the internet and thus the digital identity is held and controlled through centralized Identity Providers (IdPs). This also resulted in spam, fraud, abuse, misinformation, etc.

The internet is its current form has made it difficult to establish trust with others online, thus leaving the everyday users out of the value chain. Information and data, and the value they create are no longer owned and/or freely accessible by the users.

To fix the above fundamental problem, we need a system that inherently provides [Web of Trust](https://en.wikipedia.org/wiki/Web_of_trust) and allowing the users to control thier identities and to move thier personal data freely from one online system to other without fear of vendor lock-in. 

# Decentralized Identity
Decentralized Identity (DID), also know as "self-sovereign identity" (or SSI) is driven by open web standards at organizations such as W3C, Decentralized Identity Foundation (DIF) and the Hyperledger Project at Linux Foundation.

DIDs are cryptographically secure identifiers that are owned and controlled by a user without a third party Identity Providers (IdPs). It enables the user to prove the ownership of the identity using thier wallet (eg. a mobile device). Using the DID, the user can obtain Verifiable Credentials (VCs) from trusted organizations and, subsequently, present elements of these credentials as proof of claims without the need to authenticate with service providers using usernames and passwords.

DIDs use [Decentralized Public Key Infrastructure (DPKI)](https://github.com/WebOfTrustInfo/rwot1-sf/blob/master/draft-documents/Decentralized-Public-Key-Infrastructure-CURRENT.md) technology by providing identities for people, organizations, and [Internet of things (IoT)](https://en.wikipedia.org/wiki/Internet_of_things). DPKI returns control of identities to the entities they belong to, bringing the power of cryptography to everyday users by delegating the responsibility of public key management to secure decentralized datastores (blockchains and public databases), so anyone and anything can realize the web of trust.  

## Standards
* [W3C Decentralized Identifiers](https://www.w3.org/TR/did-core/)
* [Decentralized Identity Foundation (DID)](https://identity.foundation/)
* [Hyperledger Project at Linux Foundation](https://www.hyperledger.org/use/aries)

# Verifiable Credentials
Identity records are used in everyones daily lives. Driver license is used as evidence to operate a vehicle, education institutions issue diplomas that prove the education qualifications, passports are used to prove the nationality, etc. Verifable Credential (VC) specification defines a model how we could issue, own, store and verify the data over the internat but in a secure manner that respects user's privacy.  

Verifiable Credentials form the foundation for verifiable data in web of trust. They can contain many different type of information as well as different type of credentials. Many software providers, institutions, governments, and businesses are implementing the technology in thier service offerings.

## Standards
* [W3C Verifable Credentials](https://www.w3.org/TR/vc-data-model/)
* [The Verifable Credential Data Model 1.0](https://www.w3.org/TR/vc-data-model/)


# Building a Trust Model
A web of trust typically involves the following roles:
* **Subject** an entity about which verifiable credentials (claims) are made
* **Holder** an entity that holds one or more verifable credentials in thier wallet and also generates verifiable presentations for the verifiers. Holder is typically the **subject** but in cases where verifiable credentials of a child (**subject**) are held by parents (**holder**)
* **Issuer** an entity that asserts the claims about **subject(s)** by creating a verifiable credential from the claims and then transmits them to a holder
* **Verifier** an entity (relying party) that receives the verifiable credentials (presentations) from a **holder** and verifies the claims asserted by the **issuer** without their knowledge or interaction
* **Verifable data registry** a system that mediates the creation and verification of identifiers, public keys, verifable credential schemas, revocation registries, etc. A blockchain or public database is typically used as registry and verifiable credentials (asserted claims) are never stored in the registry

![image](https://user-images.githubusercontent.com/26188338/120909336-4cda3c80-c631-11eb-8881-cc3422a5f623.png "Roles and information flows")

# Wallets and Agents
Web of trust model is built on self-certifying identifiers and user-centric cryptography. The role of the user (**holder**) is central to the ecosystem and offers greater sovereignty of thier own information and empowerement to manage thier digital identity through new class of software known as **digital wallets**.

Digital wallets are applications that allow an end user to manage thier digital credentials and associated crytographic keys. They allow **holders** to prove identity related information about **subject(s)** by sharing a selective disclosure of attributes of the verifiable credentials in a privacy-preserving manner.

The concept of wallet can be further identified as a simple Wallet or Agent. The role of a wallet is to store keys, credentials and secrets. An agent is a software that controls access to a wallet and other storage, which can live in different locations on a network (cloud vs local), and can facilitate or perform messaging or interaction with other agents.
