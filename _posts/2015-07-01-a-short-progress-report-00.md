---
layout: post
title: A short progress report
date: 2015-07-01T11:42:43+01:00
modified:
excerpt: A discussion of the possible VCoin adoption of experimental features in Elements Alpha.
author: graham_higgins
tags: []
---

# A short progress report.

I'm working my way through the commit history of elements, integrating some of the features into VCoin 0.11 ...

> **What is Elements?**

> Elements is a collection of experiments to bring more technical innovation to Bitcoin.

> **What is [Elements Alpha?](https://github.com/ElementsProject/elements/tree/alpha)**

> Elements Alpha is the Elements project's first experimental test chain.

> Compared to Bitcoin itself, it adds the following features:

> * Confidential Transactions
> * Segregated Witness
> * Relative Lock Time
> * Schnorr Signatures
> * Additional opcodes
> * Deterministic Peg (pegged to Bitcoin's testnet currency).
> * Signed Blocks

That’s quite a shopping list. The items are too experimental to feature in Bitcoin right now, they might upset the applecart and could seriously diminish Bitcoin’s value if things went badly wrong.

VCoin has no such handicap to speak of and is an eminently suitable vehicle for offering innovative services enabled by these features.

Some of the power-ups are easy to obtain because they are contained in a single commit, I can just cherry-pick the commit and merge it. Some are much more challenging, requiring extensive re-factoring from 0.10.2 to 0.11.

Elements runs on its own Bitcoin-protocol testnet, the services haven’t been exhaustively tested, nor does any trace of them appear in the wallet GUI. 

It's a shopping list of ingredients, not ready-meals. Cuisine has yet to happen.

Cheers

Graham
---

<div><a markdown="0" href="{{ site.url }}/news" class="btn">BACK: News</a></div>