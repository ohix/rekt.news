---
title: Fei - REKT
date: 04/07/2021
tags:
   - Fei Protocol
   - Stablecoins
excerpt:  FEI has failed to maintain its $1 peg, and protocol governance token TRIBE has dropped by around 30% since launch. Fei’s tokenomics imprison and punish their users for the failures of the founders, and the project is widely seen as a disaster. What does the future hold for Fei, and for algorithmic stablecoins in general?

banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/04/fei-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/04/fei-header.png)
**Overfunded, unpegged, and everybody rekt.**

The launch of FEI gained huge momentum with money from Andreessen Horowitz, Framework, Coinbase and more, but being backed by big names means little in DeFi, and it’s hard to see this project as a success.

The above names are used to buying in at low valuations, but do they still add the value that we assign to their names?

FEI has failed to maintain its $1 peg, and protocol governance token TRIBE has dropped by around 30% since launch. 

Fei’s tokenomics imprison and punish their users for the failures of the founders, and the project is widely seen as a disaster.

_What does the future hold for Fei, and for algorithmic stablecoins in general?_

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/04/rekt-linebreak.png)

**In 2014, two [academic](https://insights.deribit.com/market-research/stability-elasticity-and-reflexivity-a-deep-dive-into-algorithmic-stablecoins/) papers were published detailing the two main concepts that most algorithmic stablecoins build upon today.** 

[Hayek Money](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2425270) by Ferdinando M Ametrano proposed the rebasing model, in which the total money supply changes according to demand.

[Seigniorage Shares](https://github.com/rmsams/stablecoins/blob/master/paper.pdf) by Robert Sams proposed a two-token system, the stablecoin itself and the volatile “seigniorage shares”, the owners of which benefit and bear burden according to the supply and demand for the stable asset. 

These two seminal papers laid the foundations for many of the later attempts to build decentralised non-volatile crypto assets such as ESD, Basis, RSR, Frax, and now FEI.

Most stablecoins considered “successful” are based on collateral reserve models. These models work well, but the decentralised versions are capital inefficient, and put the underlying assets at risk. The adoption of these coins is also somewhat limited due to the required overcollateralisation.

Projects such as [Ampleforth](https://www.coingecko.com/en/coins/ampleforth) and [Empty Set Dollar](https://www.coingecko.com/en/coins/empty-set-dollar) attempted to create sovereign stable currencies without relying on any collateral, however, the coins they created were far from stable.

Arguably the most successful decentralised stablecoin protocol is Maker [(DAI)](https://www.coingecko.com/en/coins/dai) which relies on user-owned collateral to create a non volatile decentralised asset. However, it’s not perfect; it is [impossible](https://medium.com/@hasufly/maker-dai-stable-but-not-scalable-3107ba730484) to execute closed cycle arbitrage for DAI, so the price is not entirely  stable, and the protocol faces scaling issues.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/04/fei-collateral.png)
[source](https://complementcap.substack.com/p/esd-a-sensible-haircut)

**The total supply for all [forms of stablecoin](https://www.coingecko.com/en/stablecoins) has recently grown by over 577%**, from $5.9 billion at the beginning of 2020 to over $40 billion by the beginning of 2021.
Along with ESD 1.5 and multichain concepts such as Frax, Fei represents part of the [second](https://twitter.com/Rewkang/status/1377330694389559299?s=20) major wave of algo stablecoins. Although the launch of Fei was far from perfect, and cast doubt over the future success of the project, it’s easy to see why people are still pushing to conceive what could be considered the “immaculate stablecoin”. 

FEI used a bonding curve and “direct incentives” token model in an attempt to; 

>maintain a liquid market in which ETH/FEI trades at approximately the ETH/USD price.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/04/fei-burnmint.png)

**During the much hyped Token Genesis Event, users were able to mint FEI from the ETH bonding curve for up to a 50% discount.** This also made them eligible for an airdrop of the protocol governance token TRIBE, which seemed to represent an appealing opportunity for many, as over 17,000 unique addresses participated in the event.

This advertised discount would turn out to be just the first of many pieces of bad news for the Fei Protocol. The terms and conditions of the discount meant that participants would only get this discount if under $250m in ETH was contributed. As $1.3B in ETH was collected at launch, this discount was taken away, and the ETH was irreversibly given to the project for their “Protocol Controlled Value” model, which; 

>gives the protocol more flexibility to engage in activities that are not profit-oriented.

The entirety of this PCV was initially used to build liquidity on Uniswap.

At one point, the Uniswap FEI/ETH pool had over $2.6B in liquidity, created from the ETH raised during the initial sale.

However, these numbers mean nothing in regards to the success of the project, as FEI then rapidly lost its peg and its reputation along with it.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/04/fei-cg.png)

**What went wrong?**

The initial peg was lost mainly due to the “pre-swap” option allowing participants to automatically swap their FEI tokens for TRIBE upon launch, which created millions of dollars of selling pressure. 

The Fei protocol punishes those who sell FEI and reward those who buy it whenever it is below the peg. Because approximately 98% of the liquidity for TRIBE comes from the TRIBE-FEI pair, users who wish to sell their TRIBE for ETH will either be forced to take a punishment for selling FEI as they are routed through the TRIBE-FEI pair, or lose equal sums to slippage from the low liquidity of the TRIBE-ETH pair.

Matters were made worse when, despite audits from [Consensys Diligence](https://consensys.net/diligence/audits/2021/01/fei-protocol/) and [Open Zeppelin](https://blog.openzeppelin.com/fei-protocol-audit/), a “vulnerability was found in the incentive calculation” of Fei. This caused them to shut down all minting rewards, and state that;

>reweights will still occur without mint rewards.

**The following chart from [@bantg](https://twitter.com/bantg) shows the impact of these FEI reweights.** 

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/04/fei-price.png)

**As Emin Gün Sirer said on [Twitter](https://twitter.com/el33th4xor/status/1379759409111392265?s=20);** 

>Let's examine FEI. The thinking goes like this: Why do stablecoins go lower than their peg? Because people sell. So let's punish people who sell FEI when it's trading below the peg!

>The lower the price, the greater the punishment, aka penalty. If you sell FEI when it's trading below its peg, the recipient receives fewer FEI than you transferred, taking some of the transferred coins out of circulation. The thinking is that this should boost the price.
But now, instead of just doing the obvious, single step of logical inference ("let's penalize transfers when below the peg"), let's look ahead a bit. 

>Every sale has a buyer and a seller. If you punish the sellers, you're also punishing the buyers.

>The penalty mechanism in FEI not only makes the supply disappear, it also makes demand disappear. 

>**It punishes both sides, and thereby narrows the feasibility envelope for the coin.** 

>**Making the effective price lower when the price is low is exactly the opposite of what you want in an algorithmic stablecoin!**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/04/fei-brianna.png)

**When one of the Fei founders was seen to suggest allocating some of the PCV to Yearn, the idea was criticised on [Twitter](https://twitter.com/DefiDuck_Karoo/status/1379631539978436612), as Karoo joked;**

>Our project isn't quite going as planned, so why don't we at least get some yield on all this eth you gave us.

And Banteg said in a public group;

>Personally I’d vehemently want them to dismantle and refund their users, even if it means not deploying +50% tvl to Yearn.

>We don't decide who uses the protocol. After all, neutrality is something we all have been fighting for.

However, Julien Bouteloup may disagree with this statement, as he publicly posted a [“blacklist”](https://twitter.com/bneiluj/status/1379777167563833344?s=21) of Fei holders which he suggested should not be included in future airdrops.

The Fei project has been an overfunded disaster which has brought out extreme opinions from both its supporters and detractors, as many consider it a failed experiment, and that “all ETH should be refunded”, and others simply reaffirm their confidence in the project and offer to buy unlimited FEI in a crude gesture of support.

>I'm still $0.70 USDC bid. I'll buy all the $FEI you can sell me there.
[R. Leshner.](https://twitter.com/rleshner/status/1379765204477689856?s=20)

**Perhaps the wisest position would be slightly less extreme.** 

It’s true that currently, this experiment does not look set to succeed, but it does remain [“an experiment”](https://twitter.com/StaniKulechov/status/1379511859540324353?s=20) and they do fail. [Users](https://rekt.eth.link/ape-tax/) had all the information available to them before they deposited their money, and if every failed experiment had to refund those who decided to partake then we would see much less creativity in the space.

On the other hand, there was absolutely no need to raise this much money, and if the founders are known to have failed at running smaller projects, it’s not clear why such big name investors would give them so much more money to try again. Well known names on Twitter who are publicly tying their reputation to the price of the token and indirectly encouraging others to purchase at this price or above don’t help the situation either.

As [Fiskantes](https://twitter.com/Fiskantes/status/1379814065544044554?s=20) said on Twitter;

>The most crowded investment opportunities are NEVER the best ones. 

_Will we continue to see this level of funding for future financial experiments, or are we reaching a turning point?_

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/04/rekt-text-linebreak.png)
