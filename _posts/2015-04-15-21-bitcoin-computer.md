---
layout: post
title: 21 Bitcoin computer
modified:
excerpt: A Bitcoin computer, after a fashion
author: graham_higgins
date: 2015-04-15T00:57:10+01:00
tags: []
---

## 21 Bitcoin computer

### 1.
My theory is that their real motivation is to ensure that there continues to be a robust mining ecosystem when the block reward falls off to the point that nobody wants to mine anymore without high transaction fees. So they proliferate a bunch of low cost mining gadgets that people will use primarily for the convenience it offers in making micropayments and in verifying identity, while they also do mining to ensure the health of the network but not actually make any significant money for the owner.

This would be the first iteration of their first gadget, which isn't cheap yet but could be if volumes are high enough, and future iterations would be cheaper and better.

The identity feature is my speculation based on tweets by the CEO about the need for better identity solutions and the enormous market for solving identity fraud problems. Not sure how a gadget like this addresses that but I think it is part of their plan.

### 2.

The three most difficult questions with blockchain technology are "where is the blockchain data?", "where are the keys that represent my wallet?" and "how do I get my initial bitcoin?"

This product very succinctly answers both questions in a reliable way.

It looks like they've got some basic ability to write to the blockchain, and since this only costs a few thousand satoshis, the very small amounts of Bitcoin that this device mine will be useful.

It looks like they're hoping that further profits can be driven back to the address that wrote to the blockchain.

This is a really good idea but fully dependent on how hackable this is.

Like, do I get the full Bitcoin JSON-RPC interface?

This would let me use this device as a pretty reliable source of identification, using Bitcoin's public key infrastructure to sign and authenticate messages.

It would also let me write client software on behalf of the physical device that could read and write arbitrary messages to the Bitcoin blockchain, allowing for custom colored coins, but with keychain ownership contained only within the physical device, instead of on an external server or running on a laptop.

Do I have direct programmable access to the SHA-256 ASIC?

This would help with content-addressable distributions systems like IPFS.

It would be great if the device could expose an interface that was compatible with both Common Wallet and Common Blockchain.

Common Blockchain[1] is a protocol that aims to make an abstraction of queries against the blockchain, allowing devices like the 21 Bitcoin Computer, the Bitcoin Core software, and web services like Blockcypher to expose a single interface to client software and Blockchain meta-protocols like Open Assets, Blockcast [2] and Open Publish [3].

Likewise, Common Wallet is a protocol that aims to make an abstraction for wallets and key signing devices like the 21 Bitcoin Computer, Trezor, Mycellium, or Bitcoin Core, so all of these devices can sign custom transactions that were built by external libraries like Open Publish and to sign authentication messages for services like Bitstore [5].

There is a very big problem with interoperability between various Bitcoin wallets, protocols, and services, and there is really no reason for this to be the case if everyone were to expose the proper interfaces, which roughly model the Bitcoin JSON-RPC.

[1] https://github.com/blockai/abstract-common-blockchain
[2] https://github.com/blockai/blockcast
[3] https://github.com/blockai/openpublish
[4] https://github.com/blockai/abstract-common-wallet
[5] https://github.com/blockai/bitstore-client

<div><a markdown="0" href="{{ site.url }}/news" class="btn">BACK: News</a></div>
