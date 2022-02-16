---
title: Infura - Issue of Consensus
date: 11/11/2020
tags:
  - geth
  - infura
  - ethereum
  - Fork
excerpt: Consensus isn’t just about agreement, it’s about changing things around.There were problems across the Ethereum network today as consensus flaws were hit on mainnet.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/12-angry-men-1.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/12-angry-men-1.jpg)
**Consensus isn’t just about agreement, it’s about changing things around.**

There were problems across the Ethereum network today as consensus flaws were hit on mainnet.

Services running older versions of geth nodes found themselves stuck on a minority chain, creating a knock-on effect for all apps that were reliant on them.

Most users learnt of the issue when the Infura API went down. Infura is the largest node provider on the Ethereum network, they provide tools and infrastructure to some of the most commonly used Web 3.0 apps and CEXs, such as Metamask, Uniswap and Binance.

The service degradation of Infura revealed that Binance either relies on Infura or is running outdated nodes, neither of which are appropriate for such a large exchange.

Although it may seem odd that Infura was not running the latest [geth](https://geth.ethereum.org/downloads/) versions, it makes sense that such a large scale operator would not be moving straight onto the latest version, as without a hard fork, there’s no urgent reason to switch from a stable working code to an unknown one.
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/add3dbfcb32773693acdf1699dc73e8f.png)
The search and analytics engine Blockchair also experienced issues, releasing the following tweet;

> _We're experiencing an issue with our [#Ethereum](https://twitter.com/hashtag/Ethereum?src=hashtag_click) explorer and working on a fix. It seems like there is a chain split, and some nodes (including ours and some miners') are stuck on a minority chain._

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/Emh9J7sW8AEB_FT.jpg)
Lead developer at Blockchair, [Nikita Zhavonronkov](https://twitter.com/nikzh/status/1326455533927329792?s=20) reported receiving the following error:

> _########## BAD BLOCK #########_
>
> _<…>_
>
> _Error: invalid merkle root (remote: 57cc91ee8b91b956592a27b14386abc2aba723b5f4f9e5d3181ace6b5d3cd433 local: 1f9ee59bfa683a25c7a15b626995a3ad7c58c571b40df96eea31e5c5eed9732d)_

**There were two serious vulnerabilities found in the geth network**, both of which were found by [John Youngseok Yang](https://github.com/johnyangk) (Software Platform Lab), earning him 20k points on the Ethereum Bounty Program [leaderboard](https://bounty.ethereum.org/).

To avoid exploitation, consensus flaws are not discussed on Github Issues, so the specific details of the vulnerabilities are not yet known. For those who are keen to know more about the technical details, [Mhswende ](https://twitter.com/mhswende/status/1326489526450221056?s=20)states that

> _“There may well be a write-up or devcon presentation about this in the future”_

In order to minimise disruption, the Ethereum developers decided to hard fork.

As [Péter Szilágyi wrote](https://twitter.com/peter_szilagyi/status/1326476649278414850?s=20) on Twitter;

> _It was an "unannounced hard fork" (from a bad chain to the good one). That said, silently fixing a bug dormant for 2+ years has a much lower chance of causing a disruption than raising awareness to it. We strive to minimize potential damage._

For anyone complaining about the outage of Infura, this incident should serve as a timely reminder to keep your node/s up to date, as once you delegate your node to another party, it’s their decision how they conduct their business.

Infura have been transparent about the whole affair, and are clearly working hard to fix the problem.

Infura is now back [online](https://forkmon.ethdevops.io/), status updates can be found [here](https://status.infura.io/).

**The outage of Infura has made many of us realise how dependent we are on this single entity.**

**This is a centralised service acting as a gatekeeper to our decentralised system.**

**Individuals and institutions alike need to consider their approach going forward.**

The perceived competence of large trusted exchanges such as Binance and Bithumb has fallen, as they were forced to disable ETH and ERC-20 withdrawals during the outage, despite having a responsibility to their users to not be affected by such incidents.

**We cannot rely on Infura to this extent.** Due to MetaMask’s default dependency on the centralised node provider, the entire Ethereum network became temporarily desolate, and gas shrank to only 12 gwei.

This is proof of an unhealthy dependence, and a clear indicator of the potential harm that could arise from such a dependency.

Do we want our digital society to reproduce the same mistakes as elsewhere, reliant on centralised single points of failure?

**We’ve built a free internet but given it to a small group of centralised authorities -** Chrome, Safari, Brave.. We’ve built an alternative internet where the original values of anonymity and decentralisation live on, yet we label it the Dark Net and access is limited to alternative, often blocked software.

We can’t let the same thing happen to cryptocurrency.

[David Mihal](https://twitter.com/dmihal/status/1326520031379853313?s=20) wrote:

> _Today's Infura outage sent users scrambling to find an alternative RPC provider._
>
> _I just threw together [**http://ethereumnodes.com**](https://ethereumnodes.com/) to be a central list of public, free RPC endpoints & their current status._

[Michael O’Rourke](https://twitter.com/o_rourke/status/1326509249825038336?s=20) pointed out

> _If your Metamask is down you can change the RPC provider to Pocket with the following URL_
>
> [_https://eth-mainnet.gateway.pokt.network/v1/5f3453978e354ab992c4da79…_](https://t.co/7a76Xoo8Qu?amp=1)

**Any failure of consensus is a serious issue**. An unannounced hard fork suggests that these vulnerabilities, left unchecked, could have been very harmful to Ethereum.

Fortunately, thanks to the keen eyes of bug bounty hunters and the diligent work of Ethereum developers, no damage was done, and as Nikita Zhavonronkohov wrote on Twitter, the fix appears to be quite simple...

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/end2.jpg)

Images from [12 Angry Men](https://www.imdb.com/title/tt0050083/)
