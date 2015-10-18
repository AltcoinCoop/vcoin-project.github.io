---
layout: socpage
title: Non-curricular content
excerpt: Summary information about available resources.
image:
  feature:
---

## Contents

- [Blockchain-based services](/social/school/blockchain-based-services.html), a tour d’horizon of what’s available
- [Confidential Transactions in Elements Aplha](/social/school/confidential-transactions.html), Greg Maxwell’s write-up of confidential transactions as implemented for Elements Alpha
- [The Commitcoin protocol](/social/school/commitcoin-protocol.html), an implementation of enforced transactions
- [Enterprise thinking and the blockchain](/social/school/enterprise-thinking-and-the-blockchain.html) An enterprise architect’s view 
- [How DECOR can eradicate selfish mining incentive by design](/social/school/how-decor-can-eradicate-selfish-mining-incentive-by-design.html), an algorithmic approach to disincentivising selfish mining
- [Identity-formation strategies](/social/school/identity-formation-strategies.html), a typology of identity formation strategies which a person may use to adapt to the social world
- [Paying tax on bitcoin in the US](/social/school/paying-tax-on-bitcoin-in-the-us.html), gory details of Uncle Sam’s revenue tactics
- [Phishing for phools](/social/school/phishing-for-phools.html), a review of a book on the economics of manipulation and deception
- [“Bitcoin and Cryptocurrency Technologies”](/social/school/princeton-bitcoin-and-cryptocurrency-technologies-online-course-videos.html), videos from Princeton U’s online course on cryptocurrency
- [Smart contracts](/social/school/smart-contracts.html), according to Nick Szabo
- [The social network illusion](/social/school/social-network-illusion.html), why some messages spread like wildfire through social media and others don’t.
- [Decentralised thinking](/social/school/thinking.html), aka “distributed intelligence”
- [Unique blockchain storage](/social/school/unique-blockchain-storage.html), an algorithmic solution to proving that a node is running a complete blockchain

## Use-case-ideas
- [5 industry scenarios](/social/school/use-case-ideas/5-industry-scenarios.html) that are ripe for disruption
- [Peer-to-peer insurance](/social/school/use-case-ideas/peer-to-peer-insurance.html), how it works, who’s doing it.
- [Bithire](/social/school/use-case-ideas/peer-to-peer-employment.html), a fatally limited model of how peer-to-peer employment might (not) work.
- [Publishing transparent lender criteria](/social/school/use-case-ideas/publishing-transparent-lender-criteria.html), they should - but they don’t. And what lenders look for in loan applications. 

# To be processed ...

## Key and address specs

    case 1:
      + secret (hex): 1111111111111111111111111111111111111111111111111111111111111111
      + uncompressed:
        + secret (base58): 91iS7EZqPeRGqPXcPiKLtbfjfLVUYYj17oQ54H3iFFw3n1UmZSS
        + pubkey (hex): 044f355bdcb7cc0af728ef3cceb9615d90684bb5b2ca5f859ab0f0b704075871aa385b6b1b8ead809ca67454d9683fcf2ba03456d6fe2c4abe2b07f0fbdbb2f1c1
        + address (base58): VXXWS2sMVZnwJE6HqdMPRJvW8ShMT9xKWi
      + compressed:
        + secret (base58): cN9spWsvaxA8taS7DFMxnk1yJD2gaF2PX1npuTpy3vuZFJdwavaw
        + pubkey (hex): 034f355bdcb7cc0af728ef3cceb9615d90684bb5b2ca5f859ab0f0b704075871aa
        + address (base58): VZg39gnYxrfh5mNZ8ivC86B85r8Ron95sz

    case 2:
      + secret (hex): dddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddd
      + uncompressed:
        + secret (base58): 93GdT28G5Bm49FCB7n1k449ZCEBefWbhkK4A3zoEEywMmcwU2gm
        + pubkey (hex): 04ed83704c95d829046f1ac27806211132102c34e9ac7ffa1b71110658e5b9d1bdedc416f5cefc1db0625cd0c75de8192d2b592d7e3b00bcfb4a0e860d880fd1fc
        + address (base58): VUdaFXFTTUdjsUVUaCmixdEwDw3XVTj2AY
      + compressed:
        + secret (base58): cV1ysqy3XUVSsPeKeugH2Utm6ZC1EyeArAgvxE73SiJvfa6AJng7
        + pubkey (hex): 02ed83704c95d829046f1ac27806211132102c34e9ac7ffa1b71110658e5b9d1bd
        + address (base58): VXyed2ytF6hnpWRe8TJS8ghEMxusL3G4VB

    case 3:
      + secret (hex): 47f7616ea6f9b923076625b4488115de1ef1187f760e65f89eb6f4f7ff04b012
      + uncompressed:
        + secret (base58): 928cSrNCuL6kPYy9EHejxR8v7nHPuXX1X1wH49bPhpeVZjq4b7B
        + pubkey (hex): 042596957532fc37e40486b910802ff45eeaa924548c0e1c080ef804e523ec3ed3ed0a9004acf927666eee18b7f5e8ad72ff100a3bb710a577256fd7ec81eb1cb3
        + address (base58): VZ1G1SrCcZdZExENc69XPggEdtNtH8FFTZ
      + compressed:
        + secret (base58): cPzbT6tbXyJNWY6oKeVabbXwSvsN6qhTHV8ZrtvoDBJV5BRY1G5Q
        + pubkey (hex): 032596957532fc37e40486b910802ff45eeaa924548c0e1c080ef804e523ec3ed3
        + address (base58): VKGy56BMnxAcCkuQ23NXK8Ug7PsHiWy5CJ

## Open Assets protocol

> The Open Assets Protocol is a simple and powerful protocol built on top of the Bitcoin Blockchain. It allows issuance and transfer of user-created assets. The Open Assets Protocol is an evolution of the concept of colored coins.

- [Open Assets Protocol](https://github.com/OpenAssets/open-assets-protocol) : https://github.com/OpenAssets/open-assets-protocol
- [Missing the point](https://github.com/OpenAssets/open-assets-protocol/issues/6) : https://github.com/OpenAssets/open-assets-protocol/issues/6
- [canonicalizing the JSON](https://github.com/OpenAssets/open-assets-protocol/issues/15) : https://github.com/OpenAssets/open-assets-protocol/issues/15


## Sending non-standard transactions

> The standard client will not relay non-standard transactions. However, if you get them directly to a miner that accepts them, clients will process them correctly and the transaction will work.

You can send your transactions to 173.242.112.53. This is a server run by Eligius that will relay all valid transactions and they will include even non-standard transactions in the blocks they mine. Others who are willing to relay or include free and non-standard transactions also tend to link to this node, so it can get your transaction included in blocks mined by other pools as well.

This is for sending transactions directly to Eligius: http://eligius.st/~wizkid057/newstats/pushtxn.php

## Existing PGP+email binary data timestamping service
A completely separate 1995-established PGP+email binary data timestamping service: http://stamper.itconsult.co.uk/stamper-files/index.htm


##  Use Block Chain as a distributed digital time stamp service (July 14, 2011)

https://bitcointalk.org/index.php?topic=28811.msg363505#msg363505

> That kind of gives me an idea for a project -- a generic hash chain system using proof of work just like bitcoin, but that include any data just by keeping its hash. So it can include all of those things. By analogy, you can mine bitcoins without ever seeing a transaction, they just keep a hash -- today's miners typically do just that. If the hash chain included many projects you could keep just a hash of each one. For projects you are interested in, you could keep the transactions data.
> 
> This can be incorporated without damage into the existing bitcoin system. Nodes in the timestamp chain, for example, can be included as nothing but transactions in the bitcoin chain (including only their hash). The real underlying transactions themselves need never be seen by the bitcoin system.
>
> I wonder if it would be feasible to include the hash to timestamp in the input and not in the output.

(What like `coin_base`? Where they stuff the “it’s a coloured coin” tag? Like - `doacc:D3db0e182-a26f-4083-93ff-de3b5d874d0`, maybe?)

---

## Marks out of 10

### Methods

Factors to consider when choosing amongst transfer methods.

> consider time factors, price factors associated with particular currencies, price factors associated with particular cryptocurrencies, fees charged by third parties, volatility of particular currencies, volatility of particular cryptocurrencies, economic risk factors, currency exchange rates, or any other information that may facilitate determining one method of transfer is should be used over another method.


### Cryptocurrency

Factors to consider when choosing amongst cryptocurrencies.

> Determine which cryptocurrency to use is based on cryptocurrency price, volatility of the cryptocurrency, popularity of the cryptocurrency, availability of the cryptocurrency at a local cryptocurrency exchange, availability of the cryptocurrency at a foreign cryptocurrency exchange, or any potential risk factor that may be associated with a particular cryptocurrency.


### Cryptocurrency exchanges

Factors to consider when choosing amongst cryptocurrency exchanges.

> determining whether using cryptocurrency is optimal is based at least in part upon an exchange rate associated with the cryptocurrency

> May choose a particular cryptocurrency exchange because the cryptocurrency is priced favorably (e.g., cheap if purchasing, expensive if selling) or because the cryptocurrency exchange has a relationship with the enterprise.

“Examples of cryptocurrency exchanges are OKCoin, BitStamp, BTCChina, Cryptsy, CoinMarket, Justcoin.”

“The local cryptocurrency exchange that is associated with local exchange server may be associated with the same jurisdiction (e.g., country, economic union, political union, etc.) with which a particular customer account may be associated or conducts transactions in a currency associated with the jurisdiction associated with a particular customer account”

---
