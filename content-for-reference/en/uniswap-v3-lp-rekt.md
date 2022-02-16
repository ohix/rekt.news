---
title: Uniswap V3 LP - REKT
date: 11/18/2021
tags:
  - Uniswap
excerpt: It’s not all rainbows and unicorns in Uniswap V3. A recent study suggests that ~50% of UNI V3 LPs are losing money. 
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/11/Uni-Header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/11/Uni-Header.png)
**It’s not all rainbows and unicorns in Uniswap V3.**

A [recent study](https://arxiv.org/abs/2111.09192) suggests that around 50% of UNI V3 LPs are losing money compared to if they just held their assets _(and the fees they earn don’t make up for it)_.

When V3 was [launched](https://uniswap.org/blog/uniswap-v3), Uniswap promised their LPs increased capital efficiency via the use of concentrated liquidity positions.

But after 6 months of use, it appears that the increased complexity (and risk) have left half of LPs losing out under the new system.

**Even active LPs attempting to time the market don’t outperform their passive counterparts.**

_Liquidity provision wasn’t broken. Why did they “fix it”?_

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/rekt-investigates-linebreak.png)

The team _(which includes [members](https://twitter.com/NateHindmanhttps://twitter.com/NateHindman) of Uniswap competitor [Bancor](https://twitter.com/Bancor))_ analysed non-like-asset pools with > $10M TVL, representing 43% of the platform’s total liquidity across 17 pools.

Between V3’s launch on May 5th and September 20th, these pools saw over $100B of trading volume, earning LPs ~$200M in fees.

However, over the same period, LPs lost more than $260M to impermanent loss, resulting in a net loss of over $60M.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/11/Uni-cohort.png)

**Of the ~17,000 addresses studied, 49.5% lost out when compared to simply holding the assets.**

In fact, in 80% of pools analysed, impermanent loss outweighed the trading fee income received by LPs.

The % of users to lose out varies greatly by pool, with the highest percentage found in the MKR/WETH pool, where 74% of users made a loss.

The study also investigated whether actively managed positions were more fruitful than passive LPing. The duration of positions was analysed to see how the balance between fees earned and IL played out over time.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/11/Uni-il2fees.png)

**LPs lose out over all timescales > 1s, as evidenced by an IL/Fees score of > 1 in the above graph, however, more surprisingly, the longer-held “passive” positions lost less than the short term “active” positions.**

**The only time-horizon to avoid losses is flash LPing within a single block, also known as just-in-time (JIT) liquidity.**

JIT liquidity is provided by MEV searchers (currently only 2) who scan the mempool for substantial pending trades, adding and withdrawing an LP position within the same block. Using V3’s concentrated liquidity settings, the position’s range can be tightly defined to match the trade in order to poach an amplified portion of the trading fees.

As well as reaping [juicy rewards](https://dune.xyz/ChainsightAnalytics/Uniswap-v3-Just-in-Time-(JIT)-Liquidity-MEV) on targeted trades, JIT liquidity avoids exposure to impermanent loss by its very nature since it is added and removed within the same block.

_However, this is not an option for the retail DeFi user, who [may not notice](https://twitter.com/NateHindman/status/1460962230778974210?s=20) their fees being siphoned-off, while impermanent loss continues to take its toll._

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png) 

**Uniswap have damaged their product through overcomplication, and their users have lost money because of it.**

Trading fees are not helping to rebalance positions, and Uniswaps expectation that highly skilled traders would optimise the market for them has so far been unsuccessful.
 
**As JIT liquidity bots become more widespread, will we see a further decrease in profitability of traditional LP positions?**

The industry is now looking beyond yield farming, and those who implement features such as bonds and protocol-owned liquidity (yes, including [Bancor)](https://earn.bancor.network/safe-staking/) are already attracting a great deal of attention.

_Yield farming won’t be around forever. If IL is really as bad as it looks, then could it be time to reconsider your positions?_

**We will conclude with a line from [the study:](https://arxiv.org/abs/2111.09192)**

> _on a global level, IL wipes out all fees earned by Uniswap v3 liquidity providers. In other words, as a group they would have been better off HODLing than providing liquidity on Uniswap v3._

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/rekt-outline-conc.png)
