---
layout: post
title: Bitfury research papers on blockchain voting and smart contracts
modified:
excerpt: Pertinent research papers from “a leading bitcoin blockchain infrastructure provider”.
author: graham_higgins
date: 2015-10-23T12:52:10+01:00
tags: []
---

## [Bitfury research](http://bitfury.com/white-papers-research)

> DRW Venture Capital, iTech Capital and the Georgian Co-Investment Fund participated in the round. The company has raised $60 million to date over three rounds. CEO Valery Vavilov co-founded the San Francisco-based company in 2011 to become a leading bitcoin blockchain infrastructure provider and transaction processing company. The startup just rolled out its “high-performance” 28-nm chip and recently acquired immersion cooling tech startup Allied Control. BitFury also announced plans to further expand operations in the Republic of Georgia with a new data center it’s calling the “Techno Park.”


### Public versus Private Blockchains - Oct 20, 2015

Blockchain-based solutions are one of the major areas of research for institutions, particularly in the financial and the government sectors. There is little disagreement that backbone technologies currently used in these sectors are outdated and need an overhaul to conform to the needs of the times. Distributed or decentralized ledgers in the form of blockchains are one of the most discussed potential solutions to the stated problem.

We provide a description of permissioned blockchain systems that could be used in creating secure ledgers or timestamped registries. We contend that the blockchain protocol and data should be accessible to end users to provide a higher level of decentralization and transparency and argue that proof of work could be effectively used in permissioned blockchains as a decentralized and auditable means of providing and diversifying security. We describe merged mining and blockchain anchoring concepts, which would be instrumental in implementing proof of work security for permissioned blockchains.

There is currently an ongoing debate whether the existing blockchain-based systems (such as Bitcoin and other cryptocurrencies) can be utilized as is in proprietary contexts, and whether their openness and censorship resistance are fitting properties in this case. We provide arguments for the use of permissionless blockchains and open, standardized blockchain protocols in creating ledgers and registries, devoting particular attention to the Bitcoin blockchain as the most commercially successful and secure permissionless blockchain. We argue that many permissioned applications could be effectively implemented using existing technologies on top of existing permissionless blockchains:

- Colored coins protocols could provide a means to encode transfer of arbitrary assets into ordinary transactions, thus extending the utility of public blockchains for financial institutions.
- Similar protocols could enable timestamping documents, assisting in development of decentralized timestamped registries.
- Payment channel networks could streamline payments by creating a scalable peer-to-peer layer on top of permissionless blockchains.
- Sidechain technology could be used to integrate permissionless and permissioned blockchains into a single interconnected environment. Sidechains could be used in cases when the protocol of the underlying permissionless blockchain is too restricting (e.g., in terms of transaction throughput or the required maximum settlement period).
- Transaction processing by known validators could be used to achieve regulatory compliance.

Download full document: [Public versus Private Blockchains Part 1, Permissioned Blockchains] and [Public versus Private Blockchains Part 2, Permissionless Blockchains]


### Mathematical formalism for the voting process in Bitcoin ecosystem - Sep 13, 2015

We propose a mathematical formalism for the voting process in Bitcoin ecosystem. This formalism can be used to algorithmically determine the best value of a certain parameter (e.g., a block size limit) which will be considered appropriate by all voters. The proposed approach is aimed to clarify vagueness of some proposed voting processes that potentially allows a party with marginal voting power to dictate their conditions to the rest of the network. To solve the problem, we introduce a non-negative dissatisfaction function and minimize its value summed over all votes. The value of the block size limit (and, potentially, other parameters of the protocol) found this way will satisfy voters provided the dissatisfaction function is chosen appropriately. [Download as PDF](http://bitfury.com/content/4-white-papers-research/2-mathematical-formalism-for-the-voting-process-in-bitcoin-ecosystem/voting-1.pdf)


### Proof of Stake vs Proof of Work - Sep 11, 2015

Proof of stake is a consensus mechanism for digital currencies that is an alternative to proof of work used in Bitcoin. The main declared advantages of proof of stake approaches are the absence of expensive computations and hence a lower entry barrier for block generation rewards. In this white paper, we examine the pros and cons of both consensus systems and show that existing implementations of proof of stake are vulnerable to attacks which are highly unlikely in Bitcoin and proof of work approaches in general.

We consider several problems and possible attack vectors arising in proof of stake cryptocurrencies:

- "nothing at stake" problem
- initial distribution problem
- short range attacks (e.g., bribe attacks)
- long range attacks
- coin age accumulation attacks.

We estimate the cost of various types of attacks on proof of stake currencies and compare it with the cost of similar attacks on a proof of work currency. The cost of attacks on proof of stake is shown to be significantly lower.

We also consider delegated, or deposit-based, proof of stake consensus as an ongoing evolution of basic proof of stake. This version of proof of stake is more resistant to attacks and could potentially be a formidable opponent to proof of work, when it is sufficiently tested in practice and gains a foothold. On the other hand, just like basic proof of stake, delegated systems require a combination of algorithmic and social-driven security; the social component of proof of stake currencies could weaken their decentralization and mathematical soundness. [Download as PDF](http://bitfury.com/content/4-white-papers-research/3-proof-of-stake-vs-proof-of-work/pos-vs-pow-1.0.2.pdf)

### BitFury Report On Block Size Increase - Aug 31, 2015

We believe that in order for Bitcoin ecosystem to prosper, the maximum block size must be increased. It is a common understanding among Bitcoin developers that the current limit of one megabyte hinders scalability of Bitcoin Blockchain and prevents its wide adoption as the technology of the future.

We have thoroughly studied all block size increase proposals and find that Jeff Garzik's BIP 100 proposal is the most reasonable and considerate one. We think that the block size debate must be resolved by a consensus and the voting mechanism introduced in BIP 100 is a good way to achieve such a consensus. The forecasts of growth of the Bitcoin network made in other proposals don't provide enough predictive power, so in such case the cost of mistake is extremely high. The power to make such future defining decisions must belong to the community. Ultimately, it is up to all network participants to decide what number of full nodes is sufficient to preserve decentralization, not just hardware growth trends. We believe that BIP 100 is the best solution in this regard.

Please see the extended report below. [Download as PDF](http://bitfury.com/content/4-white-papers-research/4-bitfury-report-on-block-size-increase/block-size-1.1.1.pdf)

### Smart Contracts on Bitcoin Blockchain - Aug 13, 2015

Smart contracts are one of the more promising directions for cryptocurrencies and Bitcoin in particular. A smart contract is understood as a computer protocol used to facilitate and automate financial contracts. The term smart contract was introduced by Nick Szabo in 1990s and became more relevant than ever before in 2010s after digital currencies gained popularity.

One of the advantages in using Bitcoin as a medium for smart contracts is the inherent low trust approach. Built-in Bitcoin mechanisms let users minimize counterparty risks by utilizing mathematical and algorithmic tools, not by relying on a mediator’s authority, as is often the case in the traditional approach.

Bitcoin is criticized because of the insufficient expressive means for smart contracts. The Ethereum project launched on July 30th, 2015 was developed as a replacement of the Bitcoin protocol specifically targeted for smart contract users. Because of the critique, the following questions arise: 

- what possibilities and perspectives does the Bitcoin protocol have as a medium for smart contracts?
- what are the main drawbacks of Bitcoin compared to the alternatives (e.g., Ethereum)?
- Can these drawbacks be eliminated or alleviated while staying within the protocol?

This report studies possible smart contract applications for Bitcoin and outlines directions for further research. [Download as PDF](http://bitfury.com/content/4-white-papers-research/5-smart-contracts-on-bitcoin-blockchain/contracts-1.1.1.pdf)



---

<div><a markdown="0" href="{{ site.url }}/news" class="btn">BACK: News</a></div>
