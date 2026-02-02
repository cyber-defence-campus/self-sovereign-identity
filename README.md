# Introduction
This page provides an overview on our reseach activities in the area of self-sovereign-identity (SSI). Real-world applications of the SSI paradigm include the [Swiss e-ID](https://www.eid.admin.ch) and the European [EUDI](https://eudi.dev).

# Privacy-Preserving Presentation of Credentials

The Swiss Confederation has been tasked with developing the Swiss
e-ID, an infrastructure for digital identities, following the principles of
SSI, which enforce strong privacy requirements. These requirements
are, however, hard to achieve with classical, standard methods such
as ECDSA signatures. Recently, verifiable credentials based on zeroknowledge
proofs have been proposed as an alternative to achieve
higher privacy guarantees. In this thesis, we study the feasibility of
implementing flexible, privacy-preserving verification logic for anonymous
credentials using general-purpose zero-knowledge proofs. We
provide an overview, comparison, and performance analysis of stateof-
the-art zero-knowledge frameworks, and we design flexible credential
verification logic using arithmetic circuits. We then implement a
proof-of-concept framework for anonymous credentials based on zk-
SNARKs and integrate it into the Swiss e-ID infrastructure. Our work
highlights the flexibility of this approach, for example, we can seamlessly
prove properties of values that were computed, or aggregated,
from claims of multiple linked credentials. We also uncover issues and
limitations of current zero-knowledge frameworks, especially regarding
performance. For these, we indicate possible ways in which they
could be addressed by future work. We show that this approach is
practical with current technologies for reasonably complex statements,
such as validating a credential, while future research is very likely to
allow for much more complex verification logic.

[Full report and sourceode...](https://github.com/mombelld/general-purpose-zkps-vcs)

# Privacy-Preserving Revocation of Credentials

# Distributed Key and Trust Management

# Security Testing 

# Social Vault Recovery
<img src="images/Apollo-Overview.png" width="600" />

Social key recovery mechanisms enable users to recover their vaults with the help of trusted contacts, or trustees,
avoiding the need for a single point of trust or memorizing complex strings. However, existing mechanisms overlook the
memorability demands on users for recovery, such as the need to recall a threshold number of trustees. Therefore, we first
formalize the notion of recovery metadata in the context of social key recovery, illustrating the tradeoff between easing
the burden of memorizing the metadata and maintaining metadata privacy. We present Apollo, the first framework
that addresses this tradeoff by distributing indistinguishable data within a user’s social circle, where trustees hold relevant
data and non-trustees store random data. Apollo eliminates the need to memorize recovery metadata since a user eventually
gathers sufficient data from her social circle for recovery. Due to indistinguishability, Apollo protects metadata privacy by
forming an anonymity set that hides the trustees among non-trustees. To make the anonymity set scalable, Apollo proposes
a novel multi-layered secret sharing scheme that mitigates the overhead due to the random data distributed among non-trustees. 

[Full report...](https://arxiv.org/abs/2507.19484)

