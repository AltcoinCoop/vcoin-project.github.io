---
layout: post
title: Some background
date: 2015-05-30T01:00:30+01:00
modified:
excerpt: Some background to the further development of VCoin.
author: graham_higgins
tags: []
---
# Some background

> So Graham you have linked up with the OP dev and are helping to move this coin forward ?

Yes I am but I'd be hesitant to describe it as “linked up”, I'm mostly providing free advice (NB. of legendary worth).

Seems as though some background is in order ...

To summarise, Chris took the initiative originally and did the bitcointalk community a favour by re-posting to bitcointalk the cryptocointalk ANN for vcoin. The OP's motivation for creating the coin in the first place is not known.

Not-entirely-unrelatedly, I maintain a comprehensive catalogue of altcoin metadata which (since about March 2014) necessitates me checking out every single altcoin that is launched/announced. Over the course of my peregrinations, I’ve developed a habit of making contributions to nascent altcoins where I think it might actually be useful, usually as a quid pro quo for me being lucky enough to grab a few early blocks from an overlooked coin before the diff rises above 0.01 (the effective limit for my laptop). But mostly I appreciate the positive camaraderie that seems to result from the group’s focus on getting the coin stabilised. (Incidentally, does anyone have news of shadow_runner?)

It seemed clear to me that Chris had found himself in the driving seat, possibly to his slight surprise but was nevertheless intending to try and make a decent fist of it. He set up a crowdfunding project to cover the cost of a full-time node which I considered to be an eminently sensible community-oriented approach. He also caught some undeserved flak for the OP's inadequate graphics and I thought I'd lend a hand, re-doing the logo in SVG and refreshing the icons. I chucked in the diffplot code partly in supportive recognition of his stepping up to the plate, partly 'cos it looks cool in the wallet but mostly because it's useful data for the early adopter (okay, *I've* found it useful).

So, the motivation for my involvement is primarily collegial, a common phenomenon in experimental fields.

Chris PM'd me a few queries about technical issues, I was able to opine. But it did prompt me to scope out possible intermediate futures for the coin. There is some low-hanging fruit that could be plucked and scoffed without leaving the community to cope with a disproportionate amount of technical debt. Because VCoin is a straight clone with almost no changes other than the parameters/variables, reconnecting it to its cloneparent commit history is basically a click'n'drool job if you have the right tool ([meld 1.8.4](http://meldmerge.org/)).

In another thread, some time ago, I posted details of my approach. I'll include the post here for convenience just to provide some detail for the context of my “contribution”

## Preliminaries - taking a closer look

When I put an altcoin under the microscope the first thing I do is use a little Python script I wrote to rebrand the coin as Zencoin (ZENZ). I did this with Godcoin and Achilles, giving me ZenGodcoin and ZenAchilles. 

I then compare the two directories and their contents, side-by-side, using a visual diff and merge tool: [http://meldmerge.org/](http://meldmerge.org/). It gives a very clear and accessible visual presentation of differences in directory structure and between files. 

What the hey, lets have some piccies ...

![Image](/assets/images/graphics/meld-dircomp-front.png) ![Image](/assets/images/graphics/meld-mary.png)




Here's a screenshot of ZencoinGodcoin vs ZencoinAchilles:

![Image](/assets/images/graphics/meldimage01.png)



Meld allows me to double-click the blue-lit names to show the content side-by-side. In a moment, we'll have a look at the differences in base58.h but first I need to draw your attention to the left-and-right vertical navigation scrollers - the coloured blocks show the location of pairs of files that differ. In the directory-level presentation, one coloured block = one filepair. In the above listing, a total of eight (8!) changed files is sufficient to create a functionally distinct altcoin.

There's a similar vertical nav scroller for the file-level presentation and again, coloured bars (a single line differing in content) or coloured blocks (several contiguous lines of code differing). Not too challenging I hope but an illustration should be, er, well, illuminating ...

Here's a screenshot of the one-and-only difference between `godcoin/src/base58.h` and `achilles/src/base58.h`:

![Image](/assets/images/graphics/meldimage02.png)


That's it.

That's the difference which shows up as a blue block in the directory-level display. 


Pretty much the same goes for all but a few of the rest of the blue-lit files, e.g. here’s a screenshot of the (again, one-and-only) difference between `godcoin/src/net.cpp` and `achilles/src/net.cpp`:

![Image](/assets/images/graphics/meldimage03.png)


I re-ran diff configured to output just the minimum context (filename and line no) for clarity - [these are the only differences](http://pastebin.com/dWht3JRu)

And (for eyewatering completeness) files matching the patterns below were excluded from the comparison:

    $ cat notthese
    *.qm
    *.ts
    *.png
    *.jpg
    *.svg
    *.o
    *~
    *.ico
    *.icns

In essence, my workflow runs as follows:

    $ git clone http://github.com/foo/bazcoin.git
    $ cd bazcoin
    $ rm -rf .git*  # don't need it
    $ ln -s bazcoin-qt.pro coin-qt.pro  # allows meld comparison
    $ grep 'BTC' src/qt/bitcoinunits.cpp  # what units were actually coded?
    $ grep -r BAZZA src/  # ensure no clash with source code
    $ ../omm.exe BazCoin BAZZA # use XYZZY to suppress symbol replacement if it'd muck up the source code
    $ cd ..
    $ meld bazcoin godcoin


If you feel up to it, you can have a go yourself. We've set up [a bitbucket repository](https://bitbucket.org/minkizmates/zencoin.git) that you can use:


There's a small collection of zenified coins (incl godcoin and achilles) for use when comparing with fresh candidates along with the “[omm.exe](https://bitbucket.org/minkizmates/zencoin/src)” Python script to create Zencoins:


meld will usefully show 3 sources side-by-side, viewing recently-launched [elitecoin, fusecoin and sumcoin side-by-side](https://bitbucket.org/minkizmates/zencoin/src/d09edc2fd3737e3f439bdd16803d0dba1f15bb3b/omm.exe?at=master) is quite instructive in showing how little they differ.




## Summary of findings

To recap, I used the above Python script to rebrand VCoin as ZenCoin, I used the same script to rebrand ZetaCoin 0.8.2 as ZenCoin too.

I then used meld to compare the two codebases side by side. Rebranding to a common name suppresses naming differences and reveals just the differences in variable bindings, parameter settings and changes to the code functionality. I inspected the differences between VCoin and ZetaCoin 0.8.2 and found them unexceptional, restricted to just the economic parameters and key differentiating variables such as pchMessageStart, et al. Once I was satisfied that VCoin was devoid of nasty surprises, I junked the zenified coins, checked out a fresh copy of Zetacoin, created a vcoin branch and overwrote the source with VCoin:

`cd vcoin; rm -rf .git; tar cf - . | (cd ../zetacoin; tar xf -)`

Because VCoin is an open source project, I am comfortable using SmartGit as a my click'n'drool tool to work my way through, committing the (vcoin) parameter changes (and the handful of other changes required for the diffplot feature).

End result is: either “*a branch of the latest version of 0.8.x ZetaCoin, rebranded as VCoin*” or “*a version of VCoin upgraded to Zetacoin 0.8.7.99*”, whichever way you want to look at it.

That isn't the most recent version of ZetaCoin though, ZetaCoin has been ported to Bitcoin Core 0.9.2. That 8->9 major version change denotes significant changes in the codebase. The meld listing is nearly all blue, just about *everything* has changed. Fortunately, there is a bit of wiggle room: the differences between ZetaCoin 0.8 and VCoin 0.8 are restricted to just parameter and variable changes. The difference between ZetaCoin 0.8 and 0.9.2 is in the parameters and that also characterises the difference between a VCoin rebranding of Zetacoin 0.8 and a VCoin rebranding of Zetacoin 0.9. In principle, all I need to do is copy over the parameters/variable bindings and Bob's your uncle.

## Future developments
After that, we're on our own. And there is a ways to go yet, ZetaCoin is a major version behind Bitcoin Core which is now at 0.10 (and notes for 0.11 are already appearing in the commit descriptions). Fortunately I have, for my own porpoises, developed a template-based approach for re-branding a Bitcoin Core 0.[9|10] codebase. As you might infer, it really only works for straightforward clones ... like VCoin :) 

So, in theory, all I need to do is plug in the parameters and out will pop an upgraded VCoin, the first altcoin to be based on Bitcoin Core 0.10.2.

And, I need not write a single line of C++ ... which means people can sleep more soundly in their beds (mainly, me).

It is important to recognise that the current performance of VCoin is felicitous and entirely due to its selection of parameters and an unchanged Bitcoin core functionality. A VCoin based on Bitcoin 0.10.2 may well have those same properties, assuming that Bitcoin Core 0.10.2 behaves as smoothly as Bitcoin 0.8.2.

I'd prefer to break new ground and for VCoin not to have “a dev” in the conventional altcoin sense. I'd expect some members of the community with a technical interest to engage at a technical level, others may seek to develop technical skills. At least, that's my expectation based on experience elsewhere. It definitely shouldn't be formalised, that's my sense.

So, that's the technical landscape according to my perceptions.

## Issues to be addressed
There are some profound issues related to community ownership and control of the private key that authorises the broadcast of CAlert messages, that's something that unfortunately cannot be crowdsourced, we'll just have to be innovative about it. A technical solution is infeasible, we are obliged to seek a social solution to the problem. However, whatever we come up with will also be invaluable as a solution for other instances of the same problem of establishing community ownership of resources in a plausibly decentralised way.

As ever, this is a p2p application and depends crucially on community consensus of action in that it's entirely up to the community to adopt a change to the current implementation or to choose not to, whether it's an upgrade to a more recent version, fancier graphics, additional services or whatever. 

My experience is that by and large, people learn fairly quickly to identify those whose technical advice is worth taking seriously, i.e. advice from a stable core of technically knowledgeable people who can describe in accessible terms the options and tradeoffs.

As Mark Twain once wrote: I apologise for the length of this letter, had I more time it would have been shorter.

Cheers

Graham

---

<div><a markdown="0" href="{{ site.url }}/news" class="btn">BACK: News</a></div>