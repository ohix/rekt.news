---
title: Badgers digg sushi
date: 01/26/2021
tags:
  - sushi
excerpt: Badgers are known to take the same routes when they are out foraging for food during the night. This creates well-worn paths through fields and woods.When a badger’s usual path is disturbed or obstructed in some way, this confuses the animal, and results in them rebasing to the incorrect pairing.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/header-3.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/header-3.jpg)

**Badgers are known to take the same routes when they are out foraging for food during the night. This creates well-worn paths through fields and woods.**

**When a badger’s usual path is disturbed or obstructed in some way, this confuses the animal, and results in them rebasing to the incorrect pairing.**

We were alerted to a trade that appeared to show an [experienced DeFi user](https://etherscan.io/address/0x51841d9afe10fe55571bdb8f4af1060415003528) turning 0.001 into 81.68 ETH via the [Badger DAO](https://app.badger.finance/) token [DIGG](https://www.coingecko.com/en/coins/digg).

After researching further, we found that although there had been an exploit, the damage had already been contained, and what had been perceived as a threat to the entire SushiSwap protocol was simply a smart scavenger picking up food that had been left behind.

**An already known wallet was taking advantage of an old loophole that had reopened due to a moment of forgetfulness by the SushiSwap team.**

**Although the transaction that caught our eye seemed alarming at first, once we spoke to the Sushi team, it became clear there was no huge cause for concern.**

The [transaction](https://etherscan.io/tx/0x0af5a6d2d8b49f68dcfd4599a0e767450e76e08a5aeba9b3d534a604d308e60b) showed SushiMaker attempting to convert 0.05% of the DIGG/WBTC swap fees (for ~24hrs) through a DIGG/ETH pool with little liquidity and suffering high slippage, resulting in outsized fees for the liquidity providers of the DIGG/ETH pool.

These are fees that would have been paid to XSUSHI holders, but went to the attacker instead.

**How did this happen?**

Although a solution had been created some weeks earlier, it had to be applied manually along with each new pool. As this had not been applied, the scavenger was able to sneak in and take fees which should have gone to xSushi holders.

**When new pairs were added in Sushiswaps’ [Onsen](https://sushiswap.fi/onsen), some non-ETH pairs were added, but no "bridge" was set up in the SushiMaker for DIGG/WBTC.**

SushiMaker is the contract that takes 0.05% of trading fees and passes them on to users who have staked SUSHI as xSUSHI to earn additional SUSHI rewards without impermanent loss.

By default SushiMaker sells the accumulated fees (and their pairs) to ETH and then to SUSHI.

The bridge means that when SushiMaker sells the fees of an asset without an ETH pair, it can do so to an asset other than ETH that has appropriate liquidity.

Without a bridge, liquidity could be added to create an ETH pair through which SushiMaker would attempt to convert the fees for that asset and subsequently suffer a high price impact due to the small amount of liquidity.

**This results in the fees accumulated up to that SushiMaker "serving" rewarding the liquidity providers for that ETH pair as opposed to the xSUSHI participants.**

**Fortunately, no underlying LP or xSUSHI positions were affected, only the earnings for the affected asset (0.05% fees for DIGG/WBTC swaps - 81 ETH) from the previous day were lost.**

A bridge has been set up for DIGG through the maker contract to resolve this issue for xSUSHI participants. This bridge is also included in SushiMaker.

**A conversation in the Sushiswap Discord gave us more insight into the mechanics of the exploit:**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/1.png)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/2.png)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/3.png)

**We analysed the address of the scavenger and found him to be a known user of bots and flash loans.**

![](https://lh4.googleusercontent.com/mbHCt8MYOKLIbVMR8ZEUaz0LHxerb8pKXbTDahY_U_KS_IocDL9ymBER2j0VVVHSIAQQLKb7mc3XorPJV382OJK0KUFe1rvEQcr4-3zJqOg_t435UtQzUtwjB_UGGgODeEsgWbCg)
![](https://lh4.googleusercontent.com/KLD2d5wTEfMmuh5P7IBIy4k17OMfA4UGgnNSZQ38roXBLH4-8DDMlLEc_9KNs4YIHTSkzh3sVdHsSHR_c-RZYTwBfqbwzKUF6yUJ-UjP5y1c0mQpmgyRTl_0McCU1lrNgKrJH-zC)

Data from [Nansen](https://nansen.ai/)

We found several transactions showing that [this actor](https://etherscan.io/address/0x51841d9afe10fe55571bdb8f4af1060415003528) had been attempting to take advantage of this loophole and steal the LP fees.

[0x90fb0c9976361f537330a5617a404045ffb3fef5972cf67b531386014eeae7a9](https://etherscan.io/tx/0x90fb0c9976361f537330a5617a404045ffb3fef5972cf67b531386014eeae7a9)

[0x0af5a6d2d8b49f68dcfd4599a0e767450e76e08a5aeba9b3d534a604d308e60b](https://etherscan.io/tx/0x0af5a6d2d8b49f68dcfd4599a0e767450e76e08a5aeba9b3d534a604d308e60b)

[0xcec93808a657d00cbb0245711e9419d0ea278b3a60a9a6d0a8c3353523c0e982](https://etherscan.io/tx/0xcec93808a657d00cbb0245711e9419d0ea278b3a60a9a6d0a8c3353523c0e982)

[0xe0527f7befaea54257113a09c8b3f4cd416e11a0e196cd2ba2e5e07c47767ddf](https://etherscan.io/tx/0xe0527f7befaea54257113a09c8b3f4cd416e11a0e196cd2ba2e5e07c47767ddf)

---

**What could have been a disaster turned out to be a slight humiliation for the Sushi team.**

Although the attacker was successful in their exploit, we can consider this a close call for SushiSwap, who currently have [$1.9B TVL](https://defillama.com/protocol/sushiswap) to protect.

The conversation in Discord stating that they won’t be automating this fix and will continue to rely on remembering to apply it each time is somewhat concerning.

**Why allow scope for human error if it’s not needed?**

Although the code may be decentralised, developers take on huge responsibility when they work on protocols with such huge TVL. The effects of stress are often underestimated and we see many developers fall victim to “burn out”. There are many things that can go wrong when coding, so perhaps Sushiswap would benefit from some automation here.

**This story serves as a reminder that protocols are under constant watch by hackers and arbitrageurs, who follow their every move and try to pick their pockets or knock them out completely.**

However, this inspection goes both ways - even amateurs such as Twitter user “simp2win” can watch the hackers from afar. Their effort is commendable, but perhaps they should leave the analysis to the experts.

We love a hacker who has something to say, so we were pleased to see them send the following message via [Ethereum call data](https://twitter.com/EtherText/status/1354078163022868481?s=20).

[**_Who is this guy on twitter simp2win saying I made 10 mil? lol I wish_**](https://etherscan.io/tx/0x48963b96df0949a893401635b0900064aecae780ec0950cbbd4122005eb4e14a)
