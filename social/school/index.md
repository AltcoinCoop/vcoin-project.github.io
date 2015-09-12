---
layout: socpage
title: School
excerpt: Some more formally-presented information
image:
  feature:
---

# [Title]()

## Header

How does Bitcoin work? What makes Bitcoin different? How secure are your Bitcoins? How anonymous are Bitcoin users? What determines the price of Bitcoins? Can cryptocurrencies be regulated? What might the future hold?

https://piazza.com/princeton/spring2015/btctech/home

- [Lecture 1 — Intro to Crypto and Cryptocurrencies](https://www.youtube.com/watch?v=fOMVZXLjKYo)
- [Lecture 2 — How Bitcoin Achieves Decentralization](https://www.youtube.com/watch?v=q5GWwTgRIT4)
- [Lecture 3 — Mechanics of Bitcoin](https://www.youtube.com/watch?v=t3hJsFpPmXs)
- [Lecture 4 — How to Store and Use Bitcoins](https://www.youtube.com/watch?v=NKqHXoYZvMg)
- [Lecture 5 — Bitcoin Mining](https://www.youtube.com/watch?v=jXerV3f5jN8)
- [Lecture 6 — Bitcoin and anonymity](https://www.youtube.com/watch?v=glyQy_e5LmM)
- [Lecture 7 — Community, Politics, and Regulation](https://www.youtube.com/watch?v=IRbgZUGHn9g)
- [Lecture 8 — Alternative Mining Puzzles](https://www.youtube.com/watch?v=TipGy2bOVL4)
- [Lecture 9 — Bitcoin as a Platform](https://www.youtube.com/watch?v=aM3OP4gazWw)
- [Lecture 10 — Altcoins and the Cryptocurrency Ecosystem](https://www.youtube.com/watch?v=l-3kOuF0dts)
- [Lecture 11 — The Future of Bitcoin?](https://www.youtube.com/watch?v=YG7l0XPtzD4)
- [Lecture 12 — The History of Cryptocurrencies [Bonus lecture]](https://www.youtube.com/watch?v=1VYs_zZsorU")

## Key and address specs

case 1:
  * secret (hex): 1111111111111111111111111111111111111111111111111111111111111111
  * uncompressed:
    * secret (base58): 91iS7EZqPeRGqPXcPiKLtbfjfLVUYYj17oQ54H3iFFw3n1UmZSS
    * pubkey (hex): 044f355bdcb7cc0af728ef3cceb9615d90684bb5b2ca5f859ab0f0b704075871aa385b6b1b8ead809ca67454d9683fcf2ba03456d6fe2c4abe2b07f0fbdbb2f1c1
    * address (base58): VXXWS2sMVZnwJE6HqdMPRJvW8ShMT9xKWi
  * compressed:
    * secret (base58): cN9spWsvaxA8taS7DFMxnk1yJD2gaF2PX1npuTpy3vuZFJdwavaw
    * pubkey (hex): 034f355bdcb7cc0af728ef3cceb9615d90684bb5b2ca5f859ab0f0b704075871aa
    * address (base58): VZg39gnYxrfh5mNZ8ivC86B85r8Ron95sz

case 2:
  * secret (hex): dddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddd
  * uncompressed:
    * secret (base58): 93GdT28G5Bm49FCB7n1k449ZCEBefWbhkK4A3zoEEywMmcwU2gm
    * pubkey (hex): 04ed83704c95d829046f1ac27806211132102c34e9ac7ffa1b71110658e5b9d1bdedc416f5cefc1db0625cd0c75de8192d2b592d7e3b00bcfb4a0e860d880fd1fc
    * address (base58): VUdaFXFTTUdjsUVUaCmixdEwDw3XVTj2AY
  * compressed:
    * secret (base58): cV1ysqy3XUVSsPeKeugH2Utm6ZC1EyeArAgvxE73SiJvfa6AJng7
    * pubkey (hex): 02ed83704c95d829046f1ac27806211132102c34e9ac7ffa1b71110658e5b9d1bd
    * address (base58): VXyed2ytF6hnpWRe8TJS8ghEMxusL3G4VB

case 3:
  * secret (hex): 47f7616ea6f9b923076625b4488115de1ef1187f760e65f89eb6f4f7ff04b012
  * uncompressed:
    * secret (base58): 928cSrNCuL6kPYy9EHejxR8v7nHPuXX1X1wH49bPhpeVZjq4b7B
    * pubkey (hex): 042596957532fc37e40486b910802ff45eeaa924548c0e1c080ef804e523ec3ed3ed0a9004acf927666eee18b7f5e8ad72ff100a3bb710a577256fd7ec81eb1cb3
    * address (base58): VZ1G1SrCcZdZExENc69XPggEdtNtH8FFTZ
  * compressed:
    * secret (base58): cPzbT6tbXyJNWY6oKeVabbXwSvsN6qhTHV8ZrtvoDBJV5BRY1G5Q
    * pubkey (hex): 032596957532fc37e40486b910802ff45eeaa924548c0e1c080ef804e523ec3ed3
    * address (base58): VKGy56BMnxAcCkuQ23NXK8Ug7PsHiWy5CJ

-- 
# “Cross my heart and hope to die”
Consider the scenario where Alice makes an important discovery.

It is important to her that she receives recognition for her breakthrough, however she would also like to keep it a secret until she can establish a suitable infrastructure for monetizing it. By forgoing publication of her discovery, she risks Bob independently making the same discovery and publicizing it as his own.

Folklore suggests that Alice might mail herself a copy of her discovery and leave the letter sealed, with the postal service’s timestamp intact, for a later resolution time. If Bob later claims the same discovery, the envelope can be produced and opened.

In reality, this approach does not work as (among other shortcomings) most postal services are pleased to timestamp and deliver unsealed empty envelopes that can be retroactively stuffed with “discoveries.”

## CommitCoin protocol
If Alice can put her commitment value into a Bitcoin transaction, it will be included in the chain of puzzles and the network will provide carbon dating without Alice having to perform the computation herself.

Bob only has to trust that Alice cannot produce a fraudulent block chain, longer than the canonical one and in less time (which would, incidentally, allow Alice to claim all the rewards for the fraudulent portion).

This idea has been considered on the Bitcointalk message board [10] in the context of the distributed network vouching for the timestamp. Our observation is that even if you do not trust the timestamp or any node in the network, the proof of work itself can be used to carbon date the transaction (and thus commitment value).

Alice has control over three parameters in a Bitcoin transaction: her private key(s), her public key(s), and the randomness used in the signature algorithm which, importantly, is ECDSA.

If she sets the receiver’s public key *(technically, the fingerprint of the public key)* to be her commitment value `c` and sends 1 BTC to it, the 1 BTC will be unrecoverable.

We consider this undesirable for two reasons: (a) it is financially wasteful for Alice and (b) it is not being a good citizen of the Bitcoin community.

By setting `c` equal to a private key or the signature randomness and following the protocol, `c` itself will never directly appear in the transcript.

To get around this, Alice sets `c` to the private key of a new account and then purposely leaks the value of the private key by signing two different transactions with the same randomness.

*(The CommitCoin protocol is given in Protocol 2.)*

Since `c` is randomized, it has sufficient entropy to function (temporarily) as a secret key. A few bits of the secret key could be used as a pointer (e.g., URL) to a place to post the opening of the commitment.

- 9
http://deepbit.net; http://blockexplorer.com/q/interval
- 10 http://goo.gl/fBNnA

## CommitCoin proof of concept
We committed to the title and abstract of this paper and, as proof of concept, inserted it into the Bitcoin block chain on September 15, 2011 (the submission deadline for FC 2012). We used a simplified version of CommitCoin, with `c` set to be the public key fingerprint. As noted, this effectively burns the money. A proper implementation using `c` as the private key is forthcoming.

First we ran,

`openssl rand -out random.dat 20`

creating a file containing a 20 byte random factor. [12] Then we concatenated the randomness to the end of the abstract PDF [13] and hashed it using RIPEMD-160,

`cat abstract.pdf random.dat > preimage.dat`
`openssl dgst -ripemd160 preimage.dat`

giving us the result:

`135e3712334428d4061efe4e5ffd5ff817aeb817`

This serves as a basic commitment scheme. We called an online tool [14] to convert this hash into a valid Bitcoin address giving us:

`12mQhpvGYdBrvDJq6sFGwEe3GETaqEM4Jk`

Finally, we used the Bitcoin Faucet[15] to send BTC0.005 to this address. This transaction ostensibly appeared in the Bitcoin blockchain on 2011-09-16 00:24:32 which can be seen in blockexplorer. [16]

However it may be the case that we actually committed to our abstract long after 2011-09-16 00:24:32 and colluded with blockexplorer or the Bitcoin network to display the wrong timestamp. How can you really be sure?

By the time you are reading this, many more blocks will have been added to the blockchain. Each block that is added is a solution to a moderately hard problem.

Suppose we actually committed to the abstract yesterday. That means we would have had to forge the entire chain from Block 145535 [17] to the current block. [18]

Given each block takes on average 10 minutes for the entire Bitcoin network to solve, we could not have solved that many blocks in a single day even if we controlled the whole network.

- 13 [http://people.scs.carleton.ca/~clark/commitcoin/abstract.pdf](http://people.scs.carleton.ca/~clark/commitcoin/abstract.pdf)
- 14 [http://blockexplorer.com/q/hashtoaddress/135e3712334428d4061efe4e5ffd5ff817aeb817](http://blockexplorer.com/q/hashtoaddress/135e3712334428d4061efe4e5ffd5ff817aeb817)
- 15 [https://freebitcoins.appspot.com/](https://freebitcoins.appspot.com/)
- 16 [http://blockexplorer.com/tx/2993c284f0b6838386ddd286af415384560d93cc4e27d25087fd6534f8e0d276](http://blockexplorer.com/tx/2993c284f0b6838386ddd286af415384560d93cc4e27d25087fd6534f8e0d276)
- 17 [http://blockexplorer.com/b/145535](http://blockexplorer.com/b/145535)
- 18 [http://blockexplorer.com/q/getblockcount](http://blockexplorer.com/q/getblockcount)

### References
1. [CommitCoin: Carbon Dating Commitments with Bitcoin](http://eprint.iacr.org/2011/677.pdf)

---

https://github.com/OpenAssets/open-assets-protocol

https://github.com/OpenAssets/open-assets-protocol/issues/6
https://github.com/OpenAssets/open-assets-protocol/issues/15


The standard client will not relay non-standard transactions. However, if you get them directly to a miner that accepts them, clients will process them correctly and the transaction will work.

You can send your transactions to 173.242.112.53. This is a server run by Eligius that will relay all valid transactions and they will include even non-standard transactions in the blocks they mine. Others who are willing to relay or include free and non-standard transactions also tend to link to this node, so it can get your transaction included in blocks mined by other pools as well.

This is for sending transactions directly to Eligius: http://eligius.st/~wizkid057/newstats/pushtxn.php

A completely separate 1995-established PGP+email binary data timestamping service: http://stamper.itconsult.co.uk/stamper-files/index.htm

https://bitcointalk.org/index.php?topic=28811.msg363505#msg363505

>  I think you focus on the downside and miss the upside. Every single one of these things is more robust and secure together than they would be alone. The more processing power going to extend a hash chain, the harder it is to attack that hash chain by accumulating 51% of the power. If all of these things are in the same chain, someone would need the computing power to attack all of them just to attack one of them. If that power is divided over a dozen projects, it becomes much easier.

That kind of gives me an idea for a project -- a generic hash chain system using proof of work just like bitcoin, but that include any data just by keeping its hash. So it can include all of those things. By analogy, you can mine bitcoins without ever seeing a transaction, they just keep a hash -- today's miners typically do just that. If the hash chain included many projects you could keep just a hash of each one. For projects you are interested in, you could keep the transactions data.

This can be incorporated without damage into the existing bitcoin system. Nodes in the timestamp chain, for example, can be included as nothing but transactions in the bitcoin chain (including only their hash). The real underlying transactions themselves need never be seen by the bitcoin system.


> I wonder if it would be feasible to include the hash to timestamp in the input and not in the output.

What like “coin_base”? Where they shove the “it’s a coloured coin” tag? And like - “doacc:D3db0e182-a26f-4083-93ff-de3b5d874d06”, maybe?