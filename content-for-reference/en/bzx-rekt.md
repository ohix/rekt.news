---
title: bZx - REKT
date: 11/06/2021
rekt:
  amount: 55000000
  audit:  Unaudited
  date: 11/05/2021
tags:
  - bZx
  - REKT
excerpt: Attacks can come from all angles. Straight to number 6 on our leaderboard for bZx, who lost $55M to a phishing attack.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/11/bzx-header.png
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/11/bzx-header.png)

**Attacks can come from all angles.**

_It may be their first time on our leaderboard, but this protocol has priors._

**The debut entry for [bzx.network](https://bzx.network/) goes straight into [the top 10.](https://rekt.news/leaderboard/)**

>_A bZx developer was sent a phishing email to his personal computer with a malicious macro in a Word document that was disguised as a legitimate email attachment, which then ran a script on his Personal Computer. This led to his personal mnemonic wallet phrase being compromised._

Before yesterday's events, the [last incident](https://bzx.network/blog/incident) to hit the project was in September 2020, when $8M was taken (and later returned).

Previously, in February 2020, bZx fell victim to two attacks, in which [$298,000](https://bzx.network/blog/postmortem-ethdenver) and [$645,000](https://twitter.com/bneiluj/status/1228757175595438080) were lost to the first flash loan based exploits.

**Looks like 4th time’s the charm for bZx.**

Given their chequered past, when the [announcement](https://twitter.com/bZxHQ/status/1456603269355094021?s=20) came yesterday that the “_private key controlling the Polygon and BSC deployments was compromised_”, the replies were more of exasperation than of shock...

> _["What is this like 4th time?"](https://twitter.com/BitCoinN00b/status/1456603995116654596?s=20)_

> _["It’s probably time for you guys to just give up on this whole crypto thing. Y’all ngmi."](https://twitter.com/AltsMang/status/1456617000692822023?s=20)_

**~10 hours after the initial announcement, bZx published an [update](https://twitter.com/bZxHQ/status/1456749615521406978) stating that one of their devs had fallen victim to a phishing attack, stressing that the code itself hadn’t been compromised...**

_Which was of little comfort for the users who lost their money._

[Slowmist](https://twitter.com/SlowMist_Team/status/1456647033826123780) have been keeping a running total of funds lost, which at the time of writing is up to ~$55M.

It’s hard to blame the team when the attack is so sneaky. Can bZx recover, or is this their fourth and final fatality?

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/rekt-investigates-linebreak.png)

**bZx have issued a [preliminary post mortem](https://bzx.network/blog/prelminary-post-mortem), detailing the events and containing a list of addresses used by the hacker across [Polygon](https://polygonscan.com/address/0xafad9352eb6bcd085dd68268d353d0ed2571af89), BSC ([1](https://bscscan.com/address/0x0ACC0e5faA09Cb1976237c3a9aF3D3d4b2f35FA5), [2](https://bscscan.com/address/0x74487eed1e67f4787e8c0570e8d5d168a05254d4), [3](https://bscscan.com/address/0x967bb571f0fc9ee79c892abf9f99233aa1737e31)) and multiple Ethereum addresses ([primary wallet](https://etherscan.io/address/0x74487eEd1E67F4787E8C0570E8D5d168a05254D4)).**

In place of the more technically advanced exploits that the protocol has faced in the past, this time the root of the issue was a simple phishing attack.

Sometime before the exploit, a bZx dev was sent a phishing email with an attached Word document containing a malicious macro. Opening this document resulted in the dev having the keys to their personal wallet compromised.

**But this was not a personal attack. This EOA had control over bZx’s Polygon and BSC deployments.**

The hacker was therefore able to gain control of the contracts and drain them of [BZRX](https://www.coingecko.com/en/coins/bzx-protocol). The code was then updated to enable the extraction of tokens from any wallet which had granted token approvals to the affected contracts.

**Check your token approvals here: [Polygon](https://polygonscan.com/tokenapprovalchecker), [BSC](https://bscscan.com/tokenapprovalchecker)**

**[List of bZx contracts](https://bzx.network/contracts)**

Despite bZx’s [attempts](https://twitter.com/bZxHQ/status/1456749615521406978) to convince the community that the damage was contained to just Polygon and BSC, the hacker then [sent stolen BZRX](https://etherscan.io/tx/0xee445ec9a098e9b8db744a5677422515602dc8dfb35ea60865b65c73b1704dfc) to Ethereum to use as collateral and [borrow](https://etherscan.io/tx/0xffb56ebef55a9bd4e963557bcc97594ceff97207b2aa680f7d2b9c9615cedcba) a variety of other assets.

Though the attacker nets less profit this way, they also find a way around the liquidity problem of attempting to dump such a large quantity of BZRX.

bZx [state](https://bzx.network/blog/prelminary-post-mortem) that they have reached out to centralised services, requesting that Circle freeze the stolen USDC, while the funds on Binance as well as USDT were quickly frozen.

They have also [reached](https://etherscan.io/tx/0x099aac0b0d308b7c17ea62bafbec06760cb044fb049e80ea72a810d170eafed0)  [out](https://polygonscan.com/tx/0x8eebe7f20a89c6a63b45ed870d3f98ad5c4dc19dc7bf37ee6e050069aa48693c) to the hacker offering to “_chat and reach an agreement_”

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png)

**The fact that such a large loss of funds can be attributed to such a simple attack vector is hard to believe, especially for a protocol that has experienced more than their fair share of security issues in the past.**

Anyone in crypto should be expected to be wary, and devs working on high TVL projects especially so. _But human error in this case should never have been able to lead to such an enormous loss_.

**But does all the blame lie with the protocol?**

Losing control of contracts due to their being vulnerable to a single EOA security breach is unimaginable for any responsible project, and there is no room for “_[incompetence or negligence](https://mobile.twitter.com/ChrisBlec/status/1456649881234415622)_” when $55M is at stake.

That being said, it takes an especially callous and greedy hacker to go on to drain individual users’ wallets after having extracted millions.

_**So long rekt readers.**_

_Until next time, bZx..._

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/rekt-outline-conc.png)
