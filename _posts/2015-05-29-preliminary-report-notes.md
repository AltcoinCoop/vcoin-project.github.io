---
layout: post
title: Preliminary report notes
date: 2015-05-29T20:03:58+01:00
modified:
excerpt: VCoin identified as a clone of Zetacoin.
author: graham_higgins
tags: []
---

I looked more closely. VCoin as published on cryptocointalk is a minimal-change clone of Fireflycoin:
[https://github.com/vcoindev/vcoin/blob/master/src/qt/bitcoingui.cpp#L190](https://github.com/vcoindev/vcoin/blob/master/src/qt/bitcoingui.cpp#L190)

`sendCoinsAction->setStatusTip(tr("Transfer FFC to another Wallet"));`

Fireflycoin is itself is also a minimal-change clone of ZetaCoin:
[https://github.com/dannyasia/FireflyCoin-master/blob/master/src/qt/askpassphrasedialog.cpp#L101](https://github.com/dannyasia/FireflyCoin-master/blob/master/src/qt/askpassphrasedialog.cpp#L101)

`tr("Warning: If you encrypt your wallet and lose your passphrase, you will <b>LOSE ALL OF YOUR ZETACOINS</b>!")`

So, I re-seated VCoin back into the ZetaCoin commit history and merge-upgraded to the latest ZetaCoin 0.8.x version (0.8.99).

[https://github.com/gjhiggins/vcoin-dev](https://github.com/gjhiggins/vcoin-dev)

Changes are limited to the rebranding and the addition of the code implementing the diffplot chart:
[https://github.com/gjhiggins/vcoin-dev/commit/2791dd31b564f4e89d7273d31612ec9c0a501982](https://github.com/gjhiggins/vcoin-dev/commit/2791dd31b564f4e89d7273d31612ec9c0a501982)

(notice: 4261 commits in the history)

Chris and I have been batting PMs back and forth, mainly in response to queries from the community such as “what about masternodes?” and “what about an upgrade to Bitcoin 0.10.x”.

There is a potential path that may not involve extensive re-coding: ZetaCoin-0.8.99 -> ZetaCoin-0.9.2 -> Bitcoin-0.9.2 and from there to Bitcoin 0.10.

With respect to overlay network altcoins (*nodes), there's a crop of 0.8 clones and a couple at 0.9 (IIRC), so adapting an overlay network coin comes (atm) at the cost of (at least temporarily) limiting the upgrading to 0.8/9.

I think a Core 0.10 solution has to be the most forward-looking strategy, there's no substantive mainstream development of the 0.8 or 0.9 series now, we'd be limited to picking from an array of hacks introduced by random altcoin devs. Still, it might be an effective interim position until a more coherent and compelling brand story can be developed.

There are two profound problems that require addressing before the \*node hype even begins to sound plausible:

i) a workaround for the symbol grounding problem - the *only* reliable information is that which is stored in the blockchain and secured by cryptography, all information obtained from the “outside world” demands a trusted third party - for which there are already commercial solutions

ii) a solution or workaround to the problem that the network inherently cannot conceal the content of a private key, so cannot initiate transactions - so no “automatic contracts” -- in reality, a trusted third party is required and, as before, commercial solutions already exist.

AFAIK, the only actual, functioning innovation from overlay networks in cryptocurrency has been “instant transactions”, relying on an augmented protocol used by the overlay network population to speed confirmations. That's not to be sneezed at for a coin with ambitions for wide adoption but that's an ambition for the community to discover within itself.

Just thought you'd like to know.

Cheers

Graham

---

<div><a markdown="0" href="{{ site.url }}/news" class="btn">BACK: News</a></div>