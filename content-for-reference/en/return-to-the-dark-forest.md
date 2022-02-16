---
title: Return to the dark forest
date: 02/03/2021
tags:
  - dark forest
  - mempool
excerpt: A new anonymous author speaks out. Join us, as we venture deep into the Dark Forest to uncover a mafia business model being operated by bloXrouteLabs. This protection racket turns Ethereum into a pay-to-play game, which only the frontrunners can win.
banner: https://lh4.googleusercontent.com/iktwCVrKSfn6UOX1ugIip014XKpTSpwNXbNv1GjBaFBxtvSqZdGNC8qGdqHpjCdmT_JZYMQ5E7OceWXGoHujsNVj7CCQdH4RCokX0SvEbsqSSadeMVzVLZHp-9rXGYbtTSGlQFmZ
---

![](https://lh4.googleusercontent.com/iktwCVrKSfn6UOX1ugIip014XKpTSpwNXbNv1GjBaFBxtvSqZdGNC8qGdqHpjCdmT_JZYMQ5E7OceWXGoHujsNVj7CCQdH4RCokX0SvEbsqSSadeMVzVLZHp-9rXGYbtTSGlQFmZ)

**Before transactions are etched into the history of the blockchain, they must first pass through the Ethereum mempool; a digital limbo where detection means death.**

Flowing across nodes in multiple, shifting forms, the waters of the mempool are as vague as they are dangerous. Unconfirmed transactions are a feast for trading bots, and they are fed upon with a malignant efficiency.

Apex predators haunt the mempool, systematically accruing profits by using the pool to engineer price movements.

Ethereum is littered with the corpses of transactions that have been frontrun before they could fulfil a trade, typically followed by repeat transactions that only continue to generate revenue for the frontrunner, miners and infrastructure operators.

![](https://lh4.googleusercontent.com/Ze_6wdupdomp2nAWyruTbdV_EpwUX1hCrSqQn6hYRQ4ykClx-C3fKOJfDdbXK2PoDAdJN8FKlJzW1LE6q9Lt2rxU0tVrQ0czRPcq5FfK2975SQfLMGdsVWx6SK6tkfsYr0UnV3Nm)

The dark forest theory was first expounded in Liu Cixin’s science fiction novel of the same name. It is a theory for how interstellar civilizations interact and a potential explanation as to why the universe is [silent](https://philosophy.stackexchange.com/questions/18127/dark-forest-postulate-used-to-explain-the-fermi-paradox).

**Inside the dark forest, civilizations are separated by huge stretches of space and time. Resources are scarce, yet life is always expanding, creating the ultimate competition.**

When one civilization confronts another, a chain of suspicion is created. As the distance is vast and the stakes are high, suspicion intensifies into mutual annihilation. Anticipating this, the most advanced civilizations keep tabs on all life in the universe, and instantly destroy it as soon as it reveals its location.

As with Cixin’s civilisations, Ethereum frontrunners must maintain an instantaneous picture of all transactions on the network. Speed is critical, and the most competitive frontrunners target a transaction within milliseconds. The better the picture, the more profits they accrue.

**Frontrunning is zero-sum: the success of a frontrunner is directly proportional to the suffering of others. Recent events indicate that frontrunning is evolving away from Ethereum’s open architecture into pay-to-play infrastructure and mining.**

Frontrunners have found a powerful edge.

![](https://lh3.googleusercontent.com/5qnXgd3wmTEyiiW29895tetcYAKMUN0XoWpRddEPi64-PuJlzn3ymXvYzjUgH5UpFTqPelLoxmGyRyZezaQd_5jnOC4YTRhcErQOMZakWNhr3yeLiZ8UU5zLr_qnu-0c3ieKgOmx)

**The fastest frontrunner always wins.**

Due to Ethereum’s open market for fees, mining pools give transaction finality to the highest bidder. Frontrunners observe a transaction in the mempool, and send the same transaction with a higher fee, driving up the price of a trade.

However, even high gas fees aren’t a reliable way to have your transaction processed quickly. Transactions share a common bottleneck: the speed at which they are propagated.

**At its basis, frontrunning is a race: a quick draw, played out on the quicksand of Ethereum’s peer-to-peer network. Frontrunners will pay a premium to play first.**

The first startup to cater to this demand is called bloXroute. It operates a high-speed network inside of Ethereum, that offers customers privileged access to mining pools, and the ability to bypass the heavily armed bots that patrol the mempool.

bloXroute prioritizes traffic based on how much you pay, with priority given to the highest paying customer. Think of it as a pay-to-play super-sonic highway inside of Ethereum that has been custom-built for a highly militarized mempool.

**bloXroute is building weapons to facilitate wars that play out on a microsecond timescale.**

rekt observed 22,391 transactions from the bloXroute network in a 30 hour period. One [address](https://etherscan.io/address/0xa57bd00134b2850b2a1c55860c9e9ea100fdd6cf) accounted for 10081 transactions: more than 3x the number of transactions of the next highest player, and accounting for nearly half the entire transactions on the network.

**Hone in on the trade, and it shows the unmistakable, bloodstained footprint of a frontrunner.** To take one of countless transactions, rekt observed a victim attempting to trade CRV for ETH on Uniswap with a modest $4.17 in transaction fees.

Within milliseconds, our frontrunner pounced, placing the same trade with a transaction fee of $16.29. The victim’s transaction fails while the frontrunner’s transaction is accepted. It is all over within 30 seconds.

The [culprit](https://etherscan.io/tx/0xafbba07b8638c2b9adba6320b12878518ceffd12b42fbed04506adf687a064a2):

![](https://lh4.googleusercontent.com/fG1SAIGuE4IRGiGtm-LKpCvAqt1X8aEsANDHBV9w4AHNLicD206CJkK0D66_DCThEh5j8KNHeclSk6LHbrVwH2Nj6Ls9EF4Uwjm4SGaE5N78TcuWyiJRmzpjVFOezOmVeAa_U9Nx)

The [victim](https://etherscan.io/tx/0xafbba07b8638c2b9adba6320b12878518ceffd12b42fbed04506adf687a064a2):

![](https://lh3.googleusercontent.com/edRRJu6b45A-Y-OOkLscdA6Z0b6VdgY9YufUsp8nh4EjytLceyezgeLEFwfWJwBalKrtNr2_d-RGT7Pagg6LT0gU5J1xbPoHqfUOd3Hl_2O8_ggrpIXXsrynpF7IIPZsWazGRCWx)

Too often, such transactions are followed by a [repeat attempt](https://etherscan.io/tx/0x83f14e55e4560a37deb60fc3f7103c5ea2a3ece0fce8c62c4f41c004057c3944):

![](https://lh3.googleusercontent.com/TfKlr15GdeXVna-GMqkcxt-rEQ7qE_1MmbUA_IkgSGbAQim2whKVsMAnOlTLjm5NmE6jKOio3HFcBvWTrkbGZX-IYSttdNW83A7-IgiovvHdckNi8lSTZNi_9_Ha4FpLbkYqM6tS)

And [another](https://etherscan.io/tx/0xc2dd31b7219f6601c6ad1c8cd0fc0b4d2dbbcdbd89e833a9e4c066907d564c82):

![](https://lh5.googleusercontent.com/QR5w3eRawnOI6dPp1f5nMRxwBJaeKl465hCxKN3F5-F6m02gKOs5u1uKTyORv5GlxpVldPaVJRJsycs2SkJgA55jV2Mh2gut73J7PWxeU6tJ18bRYGqBS52hLZQVlstd2UYWuKTg)

**The fastest, most efficient transactions on Ethereum are now malicious in nature.**

**Frontrunning is vampiric.** It feeds off weaker participants, while conflicts with other bots push gas prices to unusable levels. Most of the time, frontrunners win, locking in profit in the 10s to 100s of ETH. Normal users lose: pointlessly issuing repeat transactions, and suffering punishing gas costs as a downstream effect of the bots.

**This is a game of value-extraction driven purely by self-interest.** In such a glacial climate, it is perhaps inevitable that having cornered the frontrunning market, bloXroute would find another revenue stream: frontrunning protection.

For $1,250 per month, bloXroute customers can avail of “private transactions” that bypass the mempool. **There is a dark circularity to this business model: akin to a violent gang demanding protection tax.**

For the highest price, bots can frontrun the market in stealth tech, sending transactions directly into the miner’s pocket. Stripped of all its PR packaging, bloXroute is a fully-fledged frontrunning dark pool.

![](https://lh3.googleusercontent.com/0Jg2ErrAP6KEX0jbVstwqbdkno7gh2JeqVcR1E2rcnjetvYApdtYuXu4CrofHLRxDxxBfzG0X2wpRe1nnTU1U5UXPQb6FgKsvV3IqirCbIjauLUVLUnhghqSUSlB1QY4DYVvOLgk)

In 2019, the seminal paper on Ethereum frontrunning; [Flash Boys 2.0](https://arxiv.org/pdf/1904.05234.pdf), found no indication that miners and frontrunners were acting in collusion.

But with the development of the bloXroute highway, we may be witness to its genesis.

Currently, 40-50% of all miners are running bloXroute nodes. These are highly efficient, privately paying nodes that bypass Ethereum’s open architecture.

The elegance of Nakamoto consensus is that miner’s greed actively protects the network. But self-interest can always tilt the other way: _if the money is right._

**Inside the dark forest, the only rational strategy is aggression.** Opponents may be innocent, but the potential cost of assuming their innocence outweighs the benefit of destroying them.

The dark forest is a self-fulfilling prophecy. Once the norm of mutual annihilation is established, no one can afford to act otherwise. Attacks can only escalate, become faster and more automated.

As long as frontrunning remains profitable, it will continue to seek out optimal strategies, inevitably proliferating in pay-to-play pools.

EIP 1559 may improve the situation. This long anticipated EIP seeks to stabilize gas costs on Ethereum, introducing an upper bound to prices that may eliminate the run-away auction scenarios that empower frontrunning.

**However, nothing is stopping dark pools from continuing to allow gas auctions on their private networks.**

Such openly illegitimate behavior might seem unlikely. But miners are unlikely to take the EIP 1559 pay-cut gladly. Already, they have been stepping up to reject the change, and could collude to add their own fee requirements to Ethereum without changing the protocol.

**Mutual suspicion between Ethereum and its infrastructure has never been more intense.**

---

_**Editor's Note**_

**BloXroute is running a mafia business model. They make the mempool more dangerous, then profit from selling [protection](https://docs.bloxroute.com/apis/frontrunning-protection).**

By increasing the perceived and the actual dangers of the mempool, bloXroute steals power and independence from Ethereum users on a promise of security.

_The more elusive or imaginary the foe, the better for manufacturing consent.[[1](https://en.wikipedia.org/wiki/A_Short_History_of_Progress)]_

**BloXroutes’ protection racket is leading us down the path to pay-to-play Ethereum.**

A parasitic business model that values profit over progress, but it’s legitimate - they play by the same rules as we do.

For better or for worse, code is law.

**This article was written by an anonymous contributor.**

We welcome and reward any author, investigator or whistleblower who provides a valuable contribution to rekt. The anonymity of all contributors is guaranteed.

**We are all rekt.**
