---
title: Coinbase & The Oracle
date: 11/26/2020
tags:
  - coinbase
  - oracle
  - liquidation
excerpt: Recent attacks have seen hackers returning millions of dollars to their victims, or simply leaving money on the table when they could have taken more.  Various methods have been used to steal funds in the recent hack epidemic, but one character has played a role throughout...
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/MV5BMjQ1NDAwMzI4Nl5BMl5BanBnXkFtZTgwMDkwMTEyMjI@._V1_.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/MV5BMjQ1NDAwMzI4Nl5BMl5BanBnXkFtZTgwMDkwMTEyMjI@._V1_.jpg)
**We can never see past the choices we don't understand.**

Recent attacks have seen hackers returning millions of dollars to their victims, or simply leaving money on the table when they could have taken more.

Various methods have been used to steal funds in the recent [hack epidemic](/hack-epidemic/), but one character has played a role throughout...

According to Morpheus, The Oracle has been in the service of the resistance "since the beginning”. She is a sentient program that aids the human resistance in freeing humanity from the oppression of the Machines.

Recently, The Oracle has been under constant attack by anonymous agents who aim to manipulate her perception of reality in order to maximise their profits.
![](https://lh4.googleusercontent.com/nhT68w2sqe78xupagMe6jDYDzLskFBs0GOd2etbcsldnFj0LNkNHCvMRApiO8qLy91wYNoO96OsN4oupin4YuJSDs_uaxUdpvp7Ae4CTaro405Kjt8FcLNajbg3am9mC7UoV-Emi)

> [NEO](https://youtu.be/CsigSyTME9E?t=87): _I suppose the most obvious question is, how can I trust you?_
>
> ORACLE: _It’s a [pickle](/pickle-finance-rekt/), no doubt about it._

**Trust issues are common with price oracles, which can either be on or off-chain.**

As samczsun [wrote](https://samczsun.com/so-you-want-to-use-a-price-oracle/):

_In one approach, you can simply take the existing off-chain price data from price APIs or exchanges and bring it on-chain. In the other, you can calculate the instantaneous price by consulting on-chain decentralized exchanges._

Both options have their advantages and disadvantages.

On-chain price oracles such as Uniswap, Kyber, or Balancer don’t require any privileged access and are always up-to-date, however, this means they are easily manipulated by attackers.

Off-chain oracles **such as Coinbase** are usuallyslower to react to volatility, and they also require

>_privileged users to push the data on-chain, so you have to trust that they won’t turn evil and can’t be coerced into pushing bad updates._

Today’s mass liquidation was due to an error, or manipulation, of the Coinbase oracle.

**We saw over $110m of loan liquidations on Compound Finance due to their reliance on Coinbase as a single oracle.**

![](https://lh6.googleusercontent.com/sR9XX4BQ3SiHSNM2iZzUh8msdZQ45UDfTkhhChTlKD55pzU3rNQU8hPyHUJndLeW7jXvbW0CWRErqePHbQQNnZ-KlR8HWbGNz2ImvumqAKO2sDaQozoq5pHTVyB7kmOhc6ZWj9P5)
The popular yield farming pair DAI/USDC came off peg as the DAI price spiked to $1.3, causing mass liquidations and huge profits for the anonymous agents who were waiting to liquidate these positions.

[Sam Priestley](https://twitter.com/arbingsam/status/1331922588193484800?s=20) explains how liquidation can occur and how people can profit from it.

> _Someone got liquidated for $49m on compound today. Liquidator got $3.7m just for calling a method._
>
> _The victim was a leveraged comp farmer. They were lending DAI and USDC and borrowing DAI and USDC. When the price of DAI changed it pushed their account into liquidation. If they had kept DAI and USDC in separate wallets this wouldn't have happened._
>
> _When your account is in liquidation the liquidator can choose to take any of your collateral in exchange for repaying your debt. So the liquidator took DAI. Borrow DAI from Uniswap. Repay DAI debt. Get more DAI from liquidation. Repay Uniswap. Profit._
>
> _The whale may have thought they were safe because they never called 'enter-markets' function on USDC. But by borrowing USDC they activated USDC as collateral for their DAI debt._

![](https://lh4.googleusercontent.com/4s6zvtJuvM2gvebHTrXn_Nn5yf2wCtpMGMgQYkWmRFNgmyyT4vcfw1BpOKTNaZQkwMJ2dBo9ObVKOapaqOwykDqfT8f_Dx7dTBATRTD7egKq6y0il5mGetT2Jz6etsB97j0Cm4dC)
Thank you to [@arbingsam](https://twitter.com/arbingsam/status/1331922588193484800?s=20) for the analysis.

The below graph shows the DAI price spike - a massive fluctuation for a supposedly stable coin.

![](https://lh4.googleusercontent.com/CWugWH8TcpdzKzgTzseevvzKjHuVzZGZ7XbUD1k6w5JT4v9Sqx2e0u4WsFoND5rFrb7cPehLXQhpNhwKNrtVOnlc7V51HSHaXMm0zvN9rELvuuTDzvFESAxTCo0SJPsQwnlt_K0k)
When Coinbase [introduced ](https://blog.coinbase.com/introducing-the-coinbase-price-oracle-6d1ee22c7068)their Oracle they were aware of the issues that come with reliance on off chain oracles;

> _Using data from an off-chain source requires trusting the publisher to post correct prices and keep the signing key safe_

However, rather than attempt to reduce the need for trust, they just reassured the reader that they were worthy of this trust.

> _Coinbase is one of the most trusted companies in the crypto space and a major part of our mission is growing the cryptoeconomy. A highly reliable price feed anchored into Coinbase’s secure infrastructure can help make the DeFi ecosystem safer, reduce systemic risks and unlock the next wave of growth and adoption._

It seems that Robert Leshner believed them, as he said at the time;

> _Coinbase price oracle will increase the security and decentralization of Compound’s price feed, which is mission-critical to the protocol and the ecosystem of applications built on top of Compound. We’re not alone — the rest of DeFi will benefit with faster development, consistent data, and shared standards._
>
> _— Robert Leshner, Compound CEO_

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/image.png)

**So what went wrong?**

If _“off-chain oracles require privileged users to push the data on-chain”_, how did this happen?

The Coinbase [status page](https://status.coinbase.com/) currently shows the following:
![](https://lh6.googleusercontent.com/WQdMK6Voz-KX1DowA36GhZf8G3xrLN91xG6hFjHpevjVeA8VUL-2b3YPb-QYqyUBb9EjOoRG4c_M-gHNuoaMkmlze58fQUvpkim6SA-GtjkDt9KBh8gjFbMHwcjmk5QCZpt-LNVp)
Coinbase Oracle has had “issues” in the past, which always seem to lead to highly profitable situations for certain actors.

Whether this was a manipulation or a technical issue isn’t yet clear, but we do know that no flash loans were used. To manipulate the Coinbase order book to such a state would have cost 100k DAI, as the order book had 300k of depth, and the off peg price reached $1.3.

Was this malicious, careless, or expired tech? Either way, those liquidation bots profited from this incident.

Using any singular centralised data source as a price oracle is unwise, and Coinbase is particularly bad, especially if you can wipe the order book with 100k.

> _There are programs running all over the place. The ones doing their job, doing what they were meant to do, are invisible. You’d never even know they were here. But the other ones, well, we hear about them all the time._

![](https://lh6.googleusercontent.com/7H_rZ46PnRaGA2vlOfTOgp5Lz0wtz7M4nNyuqEnLDDEx8fd2U5j5kOsfyw7MOWSo406JcW5btz4BYFBKT6KwZeAZDsMZayIuWC_K_0HB4zfRwkP03AweiMCJkwT6TX7w3krY1Nfs)

And don’t worry about the vase.
