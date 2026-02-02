# Introduction
This page provides an overview on our reseach activities in the area of self-sovereign-identity (SSI). Real-world applications of the SSI paradigm include the [Swiss e-ID](https://www.eid.admin.ch) and the European [EUDI](https://eudi.dev).

# Privacy-Preserving Presentation of Credentials

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

