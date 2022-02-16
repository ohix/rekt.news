---
title: Overcompensated
date: 09/30/2021
tags:
  - Compound
excerpt: A Compound governance proposal contained a bug which allowed for the distribution of ~$80M in excess COMP rewards. Mistakes were made, but who lost out?
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/compcont-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/compcont-header.png)
**Mistakes were made, but who lost out?**

A community led _(but professionally checked)_ [proposal](https://compound.finance/governance/proposals/62) contained a bug which allowed for the distribution of ~$80M in excess [COMP rewards.](https://twitter.com/compoundfinance/status/1443359184897069060?s=20)

Starting from ~22:20 UTC on Sep 29th, certain users could claim rewards that they had not earned.

**Like an “infinite mint” but not quite as deadly, the damage done was indirect.** 

The only victims were COMP token holders, who temporarily suffered faster dilution than they expected. 

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/compcont-price.png)

**Even with the excess dilution, it’s hard to call this a crash.**

Big players like Compound have earned the confidence of the community, making this $80 million mishap seem like a drop in the ocean. 

The Compound team did their part to [downplay](https://twitter.com/compoundfinance/status/1443359184897069060) the situation, while Robert Leshner was quick to [distance himself](https://twitter.com/rleshner/status/1443380524567912448) from the incident.

However, Compound Labs cannot escape their involvement, as they were [clearly credited](https://compound.finance/governance/proposals/62) with reviewing the faulty code before it was deployed.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/rekt-investigates-linebreak.png)

[Compound: Comptroller contract](https://etherscan.io/address/0x3d9819210a31b4961b30ef54be2aed79b9c9cd3b)

The bug was contained in the [_comptrollerImplementation_](https://etherscan.io/address/0x374abb8ce19a73f2c4efad642bda76c797f19233#code#F4#L1217)’s calculations for long-term users who were supplying or borrowing before the _compInitialIndex_ was established.

[Kurt Barry](https://twitter.com/Kurt_M_Barry/status/1443414565878910976?s=20) identified the root of the exploit on Twitter;

> _Smart contracts are unforgiving of the tiniest errors...COMP bug is a tragic case of ">" instead of ">=" (in two code locations)._ 

**For a full breakdown, see Mudit Gupta’s [thread](https://twitter.com/Mudit__Gupta/status/1443454935639609345).**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/compcont-code1.png)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/comcont-code2.png)

**Those early to interact were able to withdraw enormously [inflated](https://etherscan.io/tx/0xbc246c878326f2c128462d08a0b74048b1dbee733adde8863f569c949c06422a) rewards, but as the Comptroller’s funds dwindled, latecomers could only pick up the [scraps](https://etherscan.io/tx/0xed77e2c4c5573392cfe680fed6201c8b052b5a9d19203fcd28539911ab798679).**

A further community [proposal](https://compound.finance/governance/proposals/63) to disable COMP rewards and halt losses has been launched, however with only around $250k remaining in the Comptroller contract, it seems to be too late.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png) 

If you compare the negative impact on token holders to the happiness of the users who “won” their rewards, then this doesn’t seem to be a disaster. However, a repeat of this would not be sustainable.

The full consequences are yet to be revealed, as 0xngmi pointed out on Twitter, perhaps those users who could incorrectly claim rewards were not used to covering their tracks. 

>One of the people that exploited @compoundfinance took their 10M in COMP and dumped them on OKEX and Huobi for stables, then started farming curve with them.

>[their account] Must be KYC'd because they withdrew millions from these CEXes

>Ser, I got bad news for you

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png) 

**This is a story of system failure, in which no singular party is to blame.**

Many individuals were involved in a complex, collaborative project, but in the end it comes down to:

>Two characters, tens of millions of value lost[.](https://twitter.com/Kurt_M_Barry/status/1443414565878910976?s=20)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/rekt-outline-conc.png)
