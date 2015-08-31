---
layout: post
title: VCoin upgrade to Bitcoin Core 0.11
date: 2015-06-18T16:33:58+01:00
modified:
excerpt: The upgrade to Core 0.11 is now available for testing on testnet.
author: graham_higgins
tags: []
---

# VCoin upgrade to Bitcoin Core 0.11


A bit of a first, the upgrade to 0.11 (master) is pretty much complete (with the exception of a transcription error or two here'n'there, soon to be resolved).

[https://github.com/gjhiggins/vcoincore](https://github.com/gjhiggins/vcoincore)

w.r.t. branches: vcoin-core is basic vanilla (as near as makes no difference) and vcoin-core.features.prerelease is the bundle of vanilla + branch features for overall kicking-of-the-tyres).

See it run, click the buttons. As suggested, it's 99.99% rebranded Bitcoin Core 0.11 which, even if I say so myself, has been done with surgical precision in order to present the lowest possible impedance to merged upstream development.  

But clicking the buttons is all you can do atm, will not sync with anything other than another 0.11 vcoin-core node 'cos none of the 0.8/9 nodes can speak the new (improved blockheader) protocol.

I have successfully compiled it on both Ubuntu 14.04 and 13.10 with the following command-line sequence:

    $ ./autogen.sh
    $ ./configure --with-incompatible-bdb --with-gui=qt5
    $ ./make

For running the node, my working practice atm is start VCoin 0.9 and wait till it syncs. Then shut it down and create a copy of the datadir to use with the 0.11 upgrade:

    $ cp -R ~/.vcoin /tmp/vcoincore
    $ ./src/qt/vcoin-qt -testnet -datadir=/tmp/vcoincore


The 0.11 node will/should pick up the testnet and the Minkiz node will be showing up in the “Console->Peers” list plus a handful of other nodes. T'others will gradually get banned, leaving just the Minkiz node.

For extra thrills, omit the “-testnet” ... an 0.11 node [i]will[/i] read a fresh mainnet blockchain (although it argues with the 0.8/9 clients over the indexing) and it’s safe enough if using a different datadir - obligatory promissory screenshot:

![Screenshot](http://i.imgur.com/8ZM0maI.jpg)

Minkiz' domain is (atm) hard-wired as a DNSSeed node ([minkiz.co](https://minkiz.co)). If you have strenuous objections to this arrogant centralisation (I know I would/do) then I direct your attention to the fact that the crowdsourced campaign for a community-owned node has to date received the grand total of [color=red]0 USD[/color]. Contributions of additional IP addresses / hostnames of stable VCoin nodes as advertised DNSSeeds are welcome, especially so if they arrive as github PRs.


Cheers

Graham
---

<div><a markdown="0" href="{{ site.url }}/news" class="btn">BACK: News</a></div>