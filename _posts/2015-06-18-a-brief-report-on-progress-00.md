---
layout: post
title: A brief report on progess
date: 2015-06-18T16:33:58+01:00
modified:
excerpt: The upgrade to Core 0.11 is now available for testing on testnet.
author: graham_higgins
tags: []
---

# A brief report on progress.

The upgrade's pretty much done, testnet is now accessible to 0.11 nodes. Linux source code is downloadable and ready to roll.

After people have had a chance to kick the tyres, the next step will be to reach out to Bleutrade, see if there's anything they need from us.

VCoin 0.11 is the default branch in the vcoincore repos: [https://github.com/gjhiggins/vcoincore.git](https://github.com/gjhiggins/vcoincore.git)

    $ git branch -a
    - vcoin-0.11
      remotes/origin/HEAD -> origin/vcoin-0.11
      remotes/origin/master
      remotes/origin/vcoin-0.11
      remotes/origin/vcoin-0.11.feature.chat.window
      remotes/origin/vcoin-0.11.feature.explore.window
      remotes/origin/vcoin-0.11.feature.overviewplus.tab
      remotes/origin/vcoin-0.11.feature.trade.window
      remotes/origin/vcoin-0.11.prerelease
      remotes/origin/vcoin.0.11.feature.charts.window
      remotes/origin/vcoin.feature.charts.window
      remotes/origin/vcoin.feature.chat.window
      remotes/origin/vcoin.feature.explore.window
      remotes/origin/vcoin.feature.overviewplus.tab
      remotes/origin/vcoin.feature.prerelease
      remotes/origin/vcoin.feature.trade.window

VCoin replicates the upstream distinction between stable release and in-development master approach.

Features are maintained in separate branches for reasons of sanity. This also effectively preserves a differentiation between the “vanilla” codebase, sans branches and a “prosumer” version that integrates all the features.

So ...

* 0.11 release vanilla = `git checkout vcoin-0.11 *(the default)*
* 0.11 release prosumer = `git checkout vcoin-0.11.prerelease`
* development vanilla = `git checkout master`
* development prosumer = `git checkout vcoin.feature.prerelease`

Newly-launched 0.11+ nodes on mainnet will not recognise blocks submitted by 0.8 nodes but will recognise blocks submitted by other 0.11 nodes and so a blockchain fork will inevitably occur - the 0.8 clients mining one fork and the 0.11 clients mining another. And this is okay, it is expected, if not indefinitely sustainable because when the switchover occurs, the 0.8 blockchain at that point will become the new 0.11 blockchain, obliterating the previous “unofficial” one.

Just be clear: MINING THE TEMPORARY 0.11 MAINNET BLOCKCHAIN IS FEASIBLE BUT FUTILE.

Pragmatism rather dictates that the chain being used by Bleutrade (as the one and only exchange listing VCN) is probably going to have some influence on which chain is collectively perceived as the “right” one. 

I don’t expect folks to jump without looking, so feel free to thrash the testnet.

Recommended working practice:

    cd /tmp/
    git clone https://github.com/gjhiggins/vcoincore.git
    cd vcoincore
    ./autogen.sh
    ./configure --with-incompatible-bdb --with-gui=qt5
    make
    cp -R ${HOME}/.vcoin ${HOME}/.vcoincore
    ./src/qt/vcoin-qt -datadir="${HOME}/.vcoincore" -testnet


Currently, the daemon, tx and cli binaries are compiled as “bitcoind”, “bitcoin-tx” and “bitcoin-cli”. For purity, they can just be renamed as vcoind, vcoin-tx and vcoin-cli.

I do recommend you try the prosumer version, adds information-related features at only a slight network cost (of occasional calls on Bleutrade's API).

Obligatory screengrab:

![Screenshot](http://i.imgur.com/BWU2eUb.png)


Cheers

Graham

---

<div><a markdown="0" href="{{ site.url }}/news" class="btn">BACK: News</a></div>