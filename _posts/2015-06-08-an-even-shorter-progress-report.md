---
layout: post
title: An even shorter progress report
date: 2015-06-08T15:32:58+01:00
modified:
excerpt: The upgrade to Core 0.9 is now available for testing on testnet.
author: graham_higgins
tags: []
---

# An even shorter progress report


Feel free to play with VCoin 0.9.2.2 prerelease **on testnet**:

[https://github.com/gjhiggins/vcoin09](https://github.com/gjhiggins/vcoin09)

It’s not exactly “done” in that it's not yet up to release candidate standard but at least it gives people something to play with in the interim. The migration from 0.9.x to 10.x is quite taxing and a successful upgrade to 0.9 will be a useful staging-post, I feel.

The default clone is set to the prerelease, this is **FOR TESTNET ONLY**. It's a soft fork, so it *does* sync to mainnet BUT it's not been tested, so **NOT RECOMMENDED FOR MAINNET**.

![Screenshot](/assets/images/graphics/vcoin0.9-wallet-commented.jpg)

There are remaining issues, the most important of which is:

THE EXCHANGE TRADING TAB HAS NOT BEEN TESTED

In order to have *reliable and reproducible tests*, I'll need to create mock responses to calls on Bleutrade's API. The upgrade will only get released for general use when all the API tests pass.

There are several feature branches in which the individual features were developed and later merged into the prerelease version. The graphic shows what's different (apart from the enhancements accruing from just the upgrade from 0.8.x to 0.9.x.)

The master branch is pretty much the basic upgrade to 0.9.2 with “just” the addition of the in-tab block explorer and a misconceived installation of an implementation of the IRC tab that actually opens a separate window instead, an infelicity which is addressed in the prerelease version.

There are indeed two different in-wallet block explorer implementations, feel free to choose/vote for the most useful/attractive, whatever floats the boat.

The content of the “News” tab simply indicates “available functionality”. Basically, the tab gets web content from a hard-coded URL. Obviously this is a point of centralisation at the moment but it doesn't have to be that way for ever.

**An opportunity for all to consider: what user-oriented advantages might accrue from the addition of a News tab? Please spend a little while thinking on or around this subject, perhaps from your own perspective as a coin user ... but do feel free to allow your imagination to venture further abroad if that suits.**

Please feel free to create issues for any problems ([https://github.com/gjhiggins/vcoin09/issues](https://github.com/gjhiggins/vcoin09/issues)), the discussions that happen in an active repos form a valuable technical comms channel for any altcoin and VCoin is no exception.

I will try to maintain a consistent IRC presence for a while as a temporary measure of support. My laptop has a habit of rebooting at random intervals (an issue somewhere in the 8Gb of RAM I guess) and I'll have to remember to reconnect, so some patience may be required.

As ever, comments, observations, questions, critiques, are all welcome.

Cheers

Graham

---

<div><a markdown="0" href="{{ site.url }}/news" class="btn">BACK: News</a></div>