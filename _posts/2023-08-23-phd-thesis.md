---
title: 'Defended my PhD thesis'
date: 2023-08-23
permalink: /blog/phd-thesis/
tags:
  # - cool posts
  # - category1
  # - category2 
---
My PhD thesis addresses multiple aspects of distributed protocols and cryptographic schemes.
Distributed systems today power almost all online applications,
with distributed protocols and cryptographic primitives being constantly deployed.
However, resilience, efficiency, and scalability issues still remain open.

### General trust assumptions
A big part of this thesis concerns the trust assumptions of a system.
Dominant in practice is so far the *threshold* setting:
networks, for example, expect that at most *t* out of their *n* servers may fail, or that 50% of the stake may be corrupted.
However, in this setting all parties are viewed as identical, making correlations indescribable.
For instance, in a setting where some servers run the same operating system, or are hosted by the same cloud provider,
we have no way of saying that, if one gets compromised (e.g., due to a vulnerability),
then the rest might get compromised as well.
This has been called the *general* setting.
Our work addresses theoretical and practical aspects and shows how general trust assumptions
can be efficiently used in consensus and in cryptographic protocols
such as secret sharing, distributed signatures, and randomness beacons.

### Composition of distributed systems
Moreover, the thesis addresses the task of *composing* distributed systems.
Take the example of two or more systems, consisting of different and possibly disjoint servers,
running a consensus protocol.
Each system may use threshold or general trust assumptions.
How can they work together, without manually agreeing on the new trust assumptions?
Our work describes rules to achieve this.

### Distributed randomness generation
The next part of the thesis addresses randomness generation.
Randomness is a common requirement of all asynchronous consensus protocols.
A typical approach is to employ threshold cryptography, which, in turn, necessitates a threshold setup.
This is typically achieved either through a Distributed Key Generation (DKG) protocol,
which often leads to performance bottlenecks,
or through a trusted dealer, which, of course, assumes the dealer can be trusted.
Our work proposes an alternative method, employing a large number of untrusted dealers,
leading to a practical and concretely-efficient protocol, which also supports the proof-of-stake setting.

### Ordering of smart contract calls
Efficiency and scalability of blockchains are
often compromised due to the total ordering of all user transactions.
This thesis shows that this is not required for calls to ERC20 Ethereum smart contracts,
and formally establishes the subsets of parties that need to synchronize their transactions.

### Deniability in digital signatures
Lastly, the thesis addresses the issue of deniability in distributed systems.
The problem arises from the fact that a digital signature authenticates a message
for an indefinite period.  We introduce a scheme that allows the recipients
to verify signatures, while allowing plausible deniability for signers.
This is done by transforming a polynomial commitment scheme into a digital signature scheme.

Download the thesis [here](/files/papers/phd_thesis.pdf).<br>
Published by the University of Bern [here](https://boristheses.unibe.ch/4731/).