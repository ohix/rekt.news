---
title: SushiSwap Saved - 0xMaki Speaks Out
date: 11/29/2020
tags:
  - sushiswap
  - 0xmaki
excerpt: Out of the frying pan and into the fire - The anonymous developer 0xMaki took on the lead development of SushiSwap after founder Chef Nomi let greed get the better of him.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/header-6.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/header-6.jpg)
**Out of the frying pan and into the fire.**

The anonymous developer [0xMaki](https://twitter.com/0xMaki) took on the lead development of SushiSwap after founder Chef Nomi let [greed](https://twitter.com/NomiChef/status/1304442495342796800) get the better of him.

After the end of DeFi Summer and the fall of the food farm, many assumed SushiSwap to be dead and gone. However, their developers [never](https://twitter.com/zhusu/status/1329932138171404290?s=20) stopped building, and SushiSwap has recently returned with a new menu.

**いらっしゃいませ!!!**

However, it’s not all been easy in the Omakase bar.

**Late last night, an anonymous actor poked a hole in their smart contracts and stole ~$15k before the team of Sushi chefs chased them out of the kitchen.**

rekt reached out to 0xMaki to hear his side of the story.

![](https://lh5.googleusercontent.com/bLAbz--dDRJoIQjlauDxi08j9x-pObms6J3_LmI2hhMGNs5kCYYxs-Dz13TsdF6IRgQ36NlQ-CiJpWUCZ9IVZaYGMju15bhw3vwVmG6WzAigF_sPkGojiOPjj6Ve3vdCiUJEOBZN)

**0xMaki:** Since the [Nansen](https://research.nansen.ai/sushiswap-farming/) report, I had been serving the Sushibar myself in order to mitigate arb opportunities. I had seen a few small weird transactions, but assumed nothing bad was happening since the bar was still working fine.

The first micro-tx came maybe 2-3 days ago but yesterday it became automated, “industrial level” lets say.

Here’s the first [mention](https://discord.com/channels/748031363935895552/753626532500734014/782428289868365884) of an issue with the Sushibar. ([Discord](https://discord.com/channels/748031363935895552/753626532500734014/782428289868365884))

**Monstar**

@0xMaki 源 義経 what's going on with the sushibar? all sorts of weird transactions in there and it looks like the people staking the bar aren't getting any of the sushi from them

[TX 1](https://etherscan.io/tx/0x3534241a7354a8f9c8a9d0209730167a888d923b08c19c20623cd78637faadd0)

[TX 2](https://etherscan.io/tx/0x3ffcfc9985622ad7cf0fdc2eb582ad7ce8bf9e9295fd7a4de44354fdd71a688a)

[TX 3](https://etherscan.io/tx/0xc75a8ca881d4da75774f51006651c9946311d40145ce69d07aee3a85627153d6)

**0xMaki 源 義経** replied to Monstar

it is working as intended it is just very very very very small amount from my understanding

seems like a loosing tx, looking at it

**Monstar**

I don't think that's right

because the amount in the bar available to claim went down significantly from those transactions

it seems like they are claiming the LP tokens themselves (not sure how that's possible) instead of claiming sushi like it's supposed to

so it's not converting to sushi and rewarding stakers

**0xMaki 源 義経**

looking with someone atm

maybe its just boring app that is acting odd

**Monstar**

i think people figured out a way to bypass boring app(edited)

and not share the sushi with everyone in the bar

but i don't know how to replicate what they are doing so i can't test it

yeah, they definitely are

[https://etherscan.io/tx/0x7c6af5ca27ceb04aad514ddcaee8afc6dd4eb79d0816e24b007e7db205e93ce3](https://etherscan.io/tx/0x7c6af5ca27ceb04aad514ddcaee8afc6dd4eb79d0816e24b007e7db205e93ce3)

[https://etherscan.io/address/0x1925e832c22522e0d9947ee4677120b2f28e4cd4#internaltx](https://etherscan.io/address/0x1925e832c22522e0d9947ee4677120b2f28e4cd4#internaltx) you can see all the claims from that one wallet here(edited)

**0xMaki 源 義経**

@Monstar we have the steps working on a fix atm no funds are in trouble, just an exploit of the sushibar for the fees, sucks but it is a good bug bounty

we will forego 10k ish for today as people in the Sushibar

---

**rekt:** _Thanks for the link. What were your first thoughts?_

**0xMaki:** My first impressions were, there’s no way the bar would be having an issue right?! It must be on the frontend.. The tx didn’t make sense. But then the bar wasn’t raking in money when it should have had way more inside.

About 15 minutes later I realise it’s not good, so I immediately contact [Banteg](https://twitter.com/bantg)

![](https://lh5.googleusercontent.com/2nOrhx84dL0WXXOLQy-RuEuZQo05qVC2rS7DtAYxQ207NRzWglhhEUhIO6dsES1F9ls81HYZINxkn5f2idaSXxlcgKuDDUVTe160boHCzME0RqL8Ci6R-gdZlcXTYl2Aj4jJStv5)![](https://lh5.googleusercontent.com/e9ULQE7bDt7_iZJyvYGz3oph9OzHxyilopiD0JmhhOv09ZfsJxtFS9ubho8a4eof3YflICXhptgZsU4ZhApjNGyYtpkEscsW7s8SOoG1pn120KB57RyRvZLu5yumbm9jz0hVPcPg)

Banteg couldn’t help, 6am his time and he’d been busy working on the pickle / cornichon thing. All the Sushi devs were asleep - Europe / Tokyo timezone, I’m the only one in NA.

**rekt:** _Who did you get to help?_

**0xMaki:** I got the help of [Andy](https://twitter.com/andy8052) a strategist at yEarn / ex-makerdao smart contract engineer and [Daniel Que](https://twitter.com/danielque) ex Coinbase

**rekt:** _How long did it take to fix?_

**0xMaki:** It took 3 - 4 hours to reproduce and find the issue.

**rekt:** _How much was lost?_

**0xMaki:** Only 15k lost because the sushibar only accrues 20-30k per day. 0.05% goes to the pools, and it all needs to be done manually, with a risk that the tx will fail.

**rekt: _Hack or exploit?_**

**0xMaki:** _Exploit totally, a smart one - and he deserves the funds. I think I’ve found him btw…_

**rekt:** _Are you more impressed or embarrassed?_

**0xMaki:** I’m impressed totally! There is no way I’m embarrassed! It’s fascinating to see all these hacks / exploits happening, even with robust audits there’s always some sort of new scenario emerging that we wouldn’t necessarily have planned or thought about.

This makes the ecosystem stronger and more resilient.

We only lost 15k from this attacker, maybe there were other individuals doing the same, I’ll need to take a closer look - we spotted this one because he started to affect the whole bar.

Anyway, at around 23:28 my time we (0xMaki and Andy) started to fix the issue.

![](https://lh6.googleusercontent.com/AfYQkR2nEmDTLYAIcqA0n-6GtaGpsDSSDB6Y-NykyBE2znVpyhpTcqNTSt_Wx-8B2V1OSScQyW8Ekxvgr8NiK-pABsM26u4aGxzIckiwstGUMhB_0MqLAOxGJjxSfQRm0MMXUR1v)

Then we were inspecting the smaller transactions, just to check they were benign, and then - shit - turns out they are not.

Andy had just come back from a flight, he was jet lagged and couldn’t stay up, he had to go to sleep, so it was just me, until…

![](https://lh5.googleusercontent.com/AoC4V0gDiIzCSg0MedJONypm9V7KpfN4kQZc3qmeRvGN2CyaHsOGQv_0fEosKO6766h3M_VynadJdaKHAnj7aUg7_Po7BCzDCLOjzKfCXlC_1AbQKjuG-57IN4TvEhqyDppvaIDj)

[(samczsun)](https://twitter.com/samczsun)

**rekt:** _How did he find out?_

**0xMaki:** I’d contacted him since I’d been left alone without any .sol jedi.

**rekt:** _.sol-diers_

![](https://lh6.googleusercontent.com/XmqXGATsYH7SArH7jLF82J1KLSczUODpWDI6AfY4yXUSJYrPQNoAt-TE8sueyr97jK83hDBrAK4lYtm0XfZvxGRhbPM3jNbpLuCHd4eHO4e1lSuTkrYE0KpiA384Y4et4IYy8Kw4)![](https://lh4.googleusercontent.com/AVz2977b1kJ93j9w8YlTFnQ728CBJhIKkie-4Gn-MDdqIErJbSXCYr-qLbTpxiCT70IPzzmQy6aBZ7jtrO0V4ZQsXY1FSoCawBsVPv3uwkAxYzoA3Lrsd7qRFd5-ikwliik1l0rQ)![](https://lh4.googleusercontent.com/CzyFAdpwpd5iAHD-S5EHgPAnlPl_B_IhbS8rNOsE5T5g-X_HLimDvQi6hIm8sQu_GCBTog_KKRxDwj1gXafHuywBpCdHFmthdL-GylfH0h6gkX-Ep91ucovdYvan78k_cdzHzPJg)![](https://lh4.googleusercontent.com/Cv4Ty0uF7kAY9EMIETzT26Eabe2jnfyQtFGsoA6qRJSrG1Lk7GIQlIKlLtngeneyL-kz5Q7m1S5dft6pooiYQ7r9jQMzHQsnTSjXgpjx1kVT4VOy6cHJ650KAwL_ErFcKCJbJltE)

**0xMaki:** but sadly... it was late and he had plans like any sane person on a saturday night amirite?!

Back to square, one no one to help...

Tried Chef Nomi, all the core devs, leaving a step by steps of the process in the main team channel in the hope someone wakes up

Then I remembered [Daniel](https://twitter.com/danielque), someone who had been keeping us in check since the start, so I contacted him, got on a call, briefed him.

![](https://lh5.googleusercontent.com/j49oC75qzLg9IBSO0zD5190VA4aZK2jETW8GG4S1XHZPEAKRKuu1Ney6hjysi_J3rn2DLUZ9WJDUFGgaR8ug8bIFNgdIGWqJ7tzgFHKkAURTBsmFKnHHp9Aj62Uh5Cy_UHpvl0dm)

**rekt:** _Do you still speak to Nomi?_

**0xMaki:** No.

![](https://lh5.googleusercontent.com/KxNo_yX9tboZIjfc6xvqsUs_Z13C9OSb28xmCCuF_1UFKbhDNs_el1Nd7nFflSzBGefGiA5r3w7deozbKxFk-SfGPTxDg-DzXWVFyUP3EzkHdRLjFFvtcu7hqMSq8KEgMsYh-zgo)

**0xMaki:** 02:35 and we had a reproduction!!! We had figured out how the exploit worked and were able to reproduce it, so we could work on a fix.

03:19 we had the fix.

![](https://lh6.googleusercontent.com/KmbawxTOw3xF7yC0w63X6K_XzBY85q5G4c4LAuWLqWEnq64DZcNbbUxnAHVY6iKnNUZdle8IgJrm1yf2E5VqA9skhtkLDFWwkex7tVZxfDb2TYI3sE_ML3AAoF4PJV0NTHNcNmhW)

**0xMaki:** Things were looking better, the team was awakening and working on a fix. In the meantime - I turned to our exploiter, and saw that he was mainly a holder of SNX and ETH.

I look through his tx - this wasn't an account made to hack, this was someone poking around and finding an exploit.

**rekt:** _What makes you say that?_

**0xMaki:** Tips. He received numerous tips in SNX and ESD, so he is someone hanging out in both communities, most likely Discord.

I cross referenced who received and who sent certain tips across multiple dates, and bingo…

![](https://lh4.googleusercontent.com/v8i6j6fMZvLnlXWy2qTbgcKVCTOoVmuNzCrBFKGpa3UJ_VGt_wW59AO2pIepBC7DObq-eKnV_aX7xX2P5iOL-z6-U4ArJd_hWbCL0N6IeQDrY4qlzRyNdEA0nX5f4MOD0jJ91k7x)

An insider from the SNX community helped me to identify the recipients of tips.

![](https://lh5.googleusercontent.com/HEooziQ-CV7OH0y1_D-Fo9uhj8kEYEE2kqmQkge3MDEB-avcdoOOQFvaPnxhkLeG3Ld41GDuZ4t5yS8EiuaieOuIBn2m0mDfFEIzjB1XLGqrzrBRorAosQo_xDC63AXm3p_K2tWI)

So that was that, the whole team was awake, we had a [preliminary](https://etherscan.io/address/0x280ac711bb99de7c73fb70fb6de29846d5e4207f) fix, and the attack had stopped. That’s when the news reached [Twitter](https://twitter.com/Juan_Snow1/status/1332992258115657730?s=20).

**Editors Note:** We've since received the following indisputable evidence from the suspect -

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/image-1.png)

_"could never be me"_

**0xMaki:** Nobody lost any funds since the money was pure profits destined to xSushi holders. We will be sending from our treasury 15k worth of Sushi divided pro-rata.

**rekt:** _Nothing heavy then, a light meal! Any final message to the suspect?_

**0xMaki:** Contact me! We have more smart contracts for you to poke at & we pay bug bounties!

I’d also like to [thank](https://twitter.com/0xMaki/status/1332993111950319618?s=20) everyone involved in the story, _including_ the attacker.
