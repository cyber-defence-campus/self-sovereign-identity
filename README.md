# Introduction
This repository presents research at the [Cyber-Defence Campus](https://www.cydcampus.admin.ch/en) on **self-sovereign identity (SSI)**, with a focus on building secure, privacy-preserving, and scalable digital identity systems. SSI shifts control over digital identities to users and underpins emerging real-world deployments such as the [Swiss e-ID](https://www.eid.admin.ch) and the European [EUDI](https://eudi.dev).

Our work covers important challenges across the SSI stack: key recovery for identity vaults, security testing of national e-ID infrastructures, privacy-preserving credential revocation and presentation, and distributed key and trust management. Several projects are evaluated at scale and directly applied to the Swiss e-ID ecosystem. Together, our efforts identify practical limitations of current approaches and inform the design of future national and cross-border digital identity systems.


## Contact
For questions, collaborations, or access to additional materials, please contact us through cydcampus@ar.admin.ch


# Security Testing 
Security testing involves threat modeling, creation of attack trees, and vulnerability analysis of the Swiss e-ID trust infrastructure.
We scrutinized the security of protocols, implementations and mobile platforms. 


| Title | Description | Links | 
| -------- | -------- | -------- |
| SWIYU Infrastructure | A rigorous security analysis of the Swiss trust infrastructure. | [Full report](https://github.com/user-attachments/files/21157739/Security_Analysis_of_the_Swiss_e_ID___Trust_Infrastructure.pdf), [Presentation in e-ID participation meeting (July 2025)](https://youtu.be/ASgnpElZsk0?si=IzKH53iatFxuzroD&t=2663) |
| SWIYU Wallet | Evaluation of the security of the Swiss e-ID mobile wallet (beta version), swiyu, with a specific focus on the Android platform.  | [Full report](https://github.com/cyber-defence-campus/self-sovereign-identity/blob/main/reports/Security_Analysis_of_Mobile_e_ID_Wallet_Applications-2025.pdf) |


# Privacy Preservation
Unlinkability of credential presentations is an important goal in the design of verifiable credential systems. That is, verifiers must not be
able to determine whether two anonymous credential presentations, e.g., proving legal age, belong to the same user or not. 
An even stronger notion of unlinkability retains anonymity of users even if issuers and verifiers collude to deanonymize presentations.
Achieving unlinkability is challenging, because static public keys, hashes, signatures or network metadata typically allow tracking of users across different credential presentations.

| Title | Description | Links | 
| -------- | -------- | -------- |
| Accountable Anonymity for National Digital Identity | We introduce the cryptographic forensic trail (CFT), a mechanism enabling controlled and transparent revocation of anonymity through a multi-party protocol with democratic checks and balances. | [Full report](https://eprint.iacr.org/2026/389), [Slides (PDF)](https://github.com/cyber-defence-campus/self-sovereign-identity/blob/main/reports/Frontdoors-not-Backdoors-Slides-2026-06.pdf) |
| Revocation of Credentials | We address the challenge of revoking verifiable credentials by proposing a privacy-preserving revocation scheme based on cryptographic accumulators, designed to be scalable for national e-ID systems. | [Full report and sourcecode](https://github.com/alecolo129/eid-revocation-rs) |
| Presentation of Credentials  | We study the feasibility of implementing flexible, privacy-preserving verification logic for anonymous credentials using general-purpose zero-knowledge proofs. | [Full report and sourcecode](https://github.com/mombelld/general-purpose-zkps-vcs) |

# Distributed Key and Trust Management
Key management is the foundation of secure distributed systems. Social key recovery mechanisms are studied and the *Apollo* framework for usable and privacy-preserving vault recovery is presented.
Moreover, [KERI](https://keri.one/) (Key Event Receipt Infrastructure), a fully decentralized identity system, is analyzed in terms of use cases and security. In KERI, keys are controlled by users and 
a system of witnesses and watchers enables users to manage trust in a distributed way.

| Title | Description | Links | 
| -------- | -------- | -------- |
| Social Vault Recovery with Apollo | Social key recovery mechanisms enable users to recover their vaults with the help of trusted contacts, or trustees, avoiding the need for a single point of trust or memorizing complex strings. | [Full report](https://arxiv.org/abs/2507.19484) |
| KERI: A Use-Case Study for the Swiss e-ID | With the goal of providing the basis for a digital identity system for Switzerland, a KERI Network model is proposed and analyzed. | [Full report and sourcecode](https://github.com/luffa99/KERI-Under-Scrutiny-Master-Thesis/) |
| KERI: A Security Analysis | This work describes KERI and analyzes the security properties it provides to its users both in the role of controllers and of validators. | [Full report](https://doi.org/10.3929/ethz-b-000735690) |

# Use Cases
National digital identity systems aim at providing an ecosystem of digital credentials, covering sector-specific use cases in health, finance, education, etc. We explore how the technology could be used to implement a security-critical credential: an electronic personnel security clearance  (e-PSP). 

| Title | Description | Links | 
| -------- | -------- | -------- |
| Electronic Personnel Security Clearance (e-PSP) | A proof-of-concept for electronic personal security clearances based on the SWIYU trust infrastructure. | [Full report](https://www.utupub.fi/items/0f9e0f7a-7d16-4b64-88c2-c468e073c18c), [e-PSP Demo](https://epsp.ch/)|
