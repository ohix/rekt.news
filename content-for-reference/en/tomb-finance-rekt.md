---
title: Tomb Finance - REKT
date: 09/03/2021
tags:
  - Fantom
  - Tomb Finance
excerpt: The raid of Tomb Finance makes for Fantom's first fatality. The Tomb team say it wasn't a hack, but we’ll let the rekt readers be the judge of that.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/tomb-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/tomb-header.png)
**The raid of [Tomb Finance](https://twitter.com/tombfinance/status/1433646257533243399?s=09) makes for Fantom’s first fatality.**

_Was it an exploit, or on-chain tax evasion?_

The “attacker” set up a website so that others could join in.

**Tomb Finance had created an algorithmic stablecoin on the Fantom chain.**

[Their website](https://tomb.finance/) states that; 

>TOMB is a taxed token, which means you will pay a service fee when selling TOMB. 

A “taxed token” doesn’t sound very appealing, especially to the crypto crowd.

Perhaps that’s why an anonymous actor made a website allowing users to evade this tax.

_The [Tomb team say](https://twitter.com/tombfinance/status/1433663013492600844?s=20) it wasn't a hack, but we’ll let the rekt readers be the judge of that._ 

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/tomb-investigates.png)

**The root of the problem was a method of circumventing the protocol’s [Gatekeeper](https://docs.tomb.finance/protocol/gatekeeper-fee-system) fee system, which aims to keep the price of $TOMB pegged to $FTM.**

The Gatekeeper collects a service fee on all $TOMB sales, which increases drastically (up to 20%) as the token reaches peg with $FTM.

The $TOMB collected from fees is then used by the DAO, either by selling half for $FTM and providing the other half as liquidity (above the peg) or burning the $TOMB (below peg).

Given these exorbitant fees, an enterprising user found a way to avoid the tax, and even set up a UI for avoiding the Gatekeeper at [notomb.tax](https://notomb.tax/), stating:

>There will be a fee to do so but it is much smaller than the actual gatekeeper tax.

**Example transaction:** [0x0a967da...](https://ftmscan.com/tx/0x0a967da30446b41edccc98c2dc85bcf340758d04ac62e0f192ded43c0ae11d09)

**Tax-dodger contract:** [0xC1C6caCb78466a555b11dA0Df6D0BB07a1Afb708](https://ftmscan.com/address/0xC1C6caCb78466a555b11dA0Df6D0BB07a1Afb708)

Faced with such a public tax-evasion strategy for their protocol, the Tomb team decided to deactivate the Gatekeeper, depriving themselves of the funds needed to stabilise the price.

As word got out and the peg was lost, the protocol found itself buried alive with a plummeting token price and a social media FUD frenzy.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png) 

**For a protocol that asked this question in [their FAQ:](https://docs.tomb.finance/faq-1)**

> Ok, so what the hell is the point of having a token that’s pegged to the price of $FTM when you could just use $FTM itself instead?

Charging your users 20% to use the token when it’s functioning as intended seems to go against their stated aim of creating:

> a mirrored, liquid asset that can be moved around and traded without restrictions”

_Was the Tomb team digging their own grave?_

**One of our readers was in the Tomb Discord call when they were discussing the incident.** 

They reported the following to [our Telegram group;](https://t.me/Rekt_HQ)

>It sounds like they [Tomb Finance] knew about it for weeks and then the website went up so the devs pulled the plug on the gatekeeper tax — that's how I interpreted the voice discussion they had on Discord. But since "nobody was losing money" it wasn't a rug or exploit and no big deal…

>Also something mentioned in the voice chat was that Tomb has been using the DAO funds to prop up TOMB . The number spoken was "100s of 1000s" of DAO funds have been spent prior to keep TOMB on peg.

>Which sounds like the gatekeeper / exit tax wasn't even sufficient and yet again any algostable proves fruitless...

**To end today’s article, let’s play a game of “guess the algorithmic stablecoin”:**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/tomb-price0.png)

_a clue:_

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/tomb-price.png)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/tomb-conclusion.png)
