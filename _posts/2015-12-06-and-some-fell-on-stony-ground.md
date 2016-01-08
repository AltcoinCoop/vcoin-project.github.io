---
layout: post
title: And some fell on stony ground
excerpt: Differences in classification of failed non-standard scripts
author: graham_higgins
date: 2015-12-06T10:05:00+01:00
tags: []
---

Derived from [Bill White‘s bitcointalk notes](https://bitcointalk.org/index.php?topic=563972.msg13160607#msg13160607) on reconciling the interpretation and classification of unspendable scripts.


> I have finished analyzing the discrepancies between my snapshot and sfultong's. Details are available [here](https://mega.nz/#!UxZwGTBZ!5EoQyezyIu8wBTefINg9EuRNMN9JWE71bBIyukYNPK8).
>
> Here is a short summary. There were 9 kinds of discrepancies:
>
> 1. 620 of the p2pkhs and 17 of the p2shs I omitted were because they had 0 balances.
>
> 2. 438 superficially seem to be pubkey outputs, but are unspendable because the pubkey is ill-formed; I included them as p2sh while sfultong included them as p2pkh; I will now omit them.
>
> 3. 10 p2sh sfultong omitted are unspendable raw scripts due to clear errors; I will now omit them as well.
>
> 4. 4 are essentially p2pkh except with a OP_NOP at the end; I made them p2pkh while sfultong made them p2sh.
>
> 5. 3 of the p2pkhs I omitted because the pubkey while formatted in an acceptable way was nevertheless not on the curve
>
> 6. 2 of the p2pkh disagreements is because the balances were composed of one std p2pkh txout and one pubkey txout, but the pubkey one was invalid so I omitted that part of the balance. I now omit these two unspendable addresses altogether.
>
> 7. 2 of the p2pkh disagreements is due to the duplicate txid bug for coinbase rewards (I made both spendable)
>
> 8. 1 of the p2pkh disagreements is due to the genesis block reward (which I accepted as spendable)
>
> 9. 1 of the p2shs I omitted was described by sfultong above: the unspendable 5 byte script 76a90088ac
> 
> A v2 of my snapshot omitting the unspendable addresses from (B), (C) and (F) is [here](https://mega.nz/#!IkBUzT5A!P4Ea4zLiJtnzFTHyqxyiNFZ00_N3E45Ra6LmFoVqCao):

Useful list of specific failure conditions that illuminates where some basic machanical checks would be useful to coin users.
