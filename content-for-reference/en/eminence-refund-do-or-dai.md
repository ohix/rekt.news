---
title: Eminence Refund - Do or DAI
date: 10/02/2020
tags:
  - Eminence
  - Cronje
  - defi
excerpt: With his hand forced by threats from community members, Andre Cronje and team have quickly taken action to refund the $8M that was mysteriously returned after the EMN contract was exploited for $15M on the 29th September.
---

With his hand forced by threats from community members, Andre Cronje and team have quickly taken action to refund the $8M that was mysteriously returned after the [EMN contract was exploited](https://www.rekt.news/eminence-rekt-in-prod/) for $15M on the 29th September.

Why would anyone return $8M?

This was a sophisticated hack that probably took days of work, why would they choose to return half the money only a few minutes later?

Is it possible that Yearn knows the identity of the attacker?

If you were the hacker, would you rather have $15M and be doxxed, or $8M, and enjoy your life in peace?

These are just some of the questions that the community is asking after the dramatic exploit and refund on September the 29th.

A full analysis of the three transactions involved in the exploit can be found below.

[Transaction 1 Sep-29-2020 01:20:41 AM +UTC](https://ethtx.info/0x3503253131644dd9f52802d071de74e456570374d586ddd640159cf6fb9b8ad8)

[Transaction 2 Sep-29-2020 01:22:28 AM +UTC](https://ethtx.info/0x045b60411af18114f1986957a41296ba2a97ccff75a9b38af818800ea9da0b2a)

[Transaction 3 Sep-29-2020 01:23:28 AM +UTC](https://ethtx.info/0x4f0f495dbcb58b452f268b9149a418524e43b13b55e780673c10b3b755340317)

The return transaction came 8 minutes later.

[Return Transaction Sep-29-2020 01:31:04 AM +UTC](https://ethtx.info/0x7bc97357364222207f1f011b22ad98ba78fcd3c25d3398346caa3928cdf4a4dd)

There are several theories about who was responsible for the heist, and some are debating whether this was really a hack, or just an exploit of unfinished code.

[@mierzwik](https://twitter.com/mierzwik) wrote [this article](https://medium.com/@mierzwik/hey-bot-give-me-all-your-money-e1f692594f2e) on the bot responsible ([0x762bfbd](https://etherscan.io/address/0x762bfbd8dc93fac514fd89c027e81621e8597441)), which shows how the bot stole 400 UNI one week prior to the EMN attack.

[@frankresearcher](https://twitter.com/FrankResearcher) has since done some great work investigating the same wallet used in the hack / exploit.
![](https://lh6.googleusercontent.com/qov3BuEa6rc6VT97cxBh7jgvRYxeOMDi8PbS3qgjTyIKLVIZwE5d8yA1TtDPCuXM-7WmFhMAma9hdVdskBbEEZWG3XMl3ntRdiGVKhbnk2aDnlzTBOSpf1Iz0R_hTbj4yFdLxKVz)
Read the rest of Frank’s tweets [here](https://twitter.com/FrankResearcher/status/1310885102407254021?s=20). He goes on to hypothesise the role of various addresses involved in the hack / exploit.

Frank’s hypothesis based on on-chain data:

0x223034e =[ $ENM](https://twitter.com/search?q=%24ENM&src=cashtag_click) hacker

0x762bfbd = the contract from which the hacker withdrawn[ $UNI](https://twitter.com/search?q=%24UNI&src=cashtag_click)

0x2d033fe = address of creator of 0x762bfbd

0x2f14f72 = address which funded creator (very likely one owner)

This is an on-going investigation, subscribe now and we’ll keep you up to date.

![](https://lh5.googleusercontent.com/bElo-Tzz3WEbKufKV60H8JybrfXU_jwZ4m5XmRARI3FsQCE9v57iOqnrOb89woPqABSKOBpGd6oMpwr4okPa42bKsiXrzNYkuoUNwXTN7sM6P9pxmXKpxBma5XIxHC5AzE5wMTnq)

In what he described as an “[elegant solution](https://github.com/banteg/your-eminence)” Yearn developer @bantg used the Uniswap LP distribution code and a merkle tree implementation to refund the money.
![](https://lh4.googleusercontent.com/N6RtgR2lbxx_noX8jN7NPq5o3kmScgGaOhpQnBgS6-QPU3l7GnWvEvbGBGybHNOKsMmpgR_gOCAxA4BALyDaHXkub1i89MDIyVjRDN-spFd7TgejtVFygH88VbZnjSPgsOytYUYu)![](https://lh6.googleusercontent.com/KBuK7SdgDK_F5xS3SDpMwR3mawVkKuG4YhPOS90HjyjY1JewDai5IXxp7dsA3ROWvabWdhr2AI7YX2GeJhlT92bbIFctdRKwk-SjE_O0IXogKOYFLDALNu5DAZQEzww3gNFGzbmX)
Milkyklim created a similar yYFI refund [solution ](https://gist.github.com/banteg/b2a3b78cdd59ea346afc56181e7a07cd)for those who claimed from the yYFI contract between blocks 10923319-10954777 and suffered from a 5% fee issue.
![](https://lh4.googleusercontent.com/FiHtOA8Xk-LxkXVD4Cm-eq0ftH7tPFPxNoCmbzX1EXzppq4Hz_Ge9RIgHdD8gzV02dexKQGrljMg46xXl0mJTrocaHofDR2fdgpOYcA2bDxGAxH8fM0NE9rWTajN5duN4i4NG3ro)

Once the refunds were made available on youreminence.finance, refunds were distributed at a rate of $250,000 per minute.
![](https://lh4.googleusercontent.com/Cj0OwsQJkhLnq8Lheqzy6Qa_rLUbG0x4h_xkBLpeLSZPETYI5Tt4TaGlA9_4HACZw-0mSCnW0kYejV0F88Hb6nWlvTTEUTlhx3pMeGczF2nJ9QzwR3pdO5ydhQk_pfT3OG6FheMR)

This resulted in half of the $8 million refund being claimed in just 20 minutes.
![](https://lh3.googleusercontent.com/jSpxxX0Z1wyYeVZlXFy6ToRnqV0kpyzqiaVS-t_UB8GSuYgPCfLkzfAnIwZJWweng1Ymx2l3lVTa3TGKOjGMbPCamGtfvLtSn_hT8fsE1yjeeAHD5tYfvvAnC5kSUSR3IxsFnM9l)
In a sharp contrast to the amount of focus and work put into creating this snapshot refund, it appears many users did not pay enough attention when claiming their refund, and simply copied banteg’s screenshot, resulting in donating their full claim straight back to banteg and team.

[100% tip for 340 DAI](https://etherscan.io/tx/0x6a17f1b30b8c5479e6542fb3d6189cf67f34bbc85cba7d669cbf72367bfb724f)

[100% tip for 66.9 DAI ](https://etherscan.io/tx/0xa7ad9985bc7ba00070f5ef18b766e10ca4c0d155cf4ca6ae2e11df9af41b6fc1)

[100% tip for 993.3 DAI](https://etherscan.io/tx/0x835b998d086ea0aee96d1e0a3e5b558c62da8d621959f213c10bed6250c9f9c0)

[100% tip for 263.1 DAI](https://etherscan.io/tx/0x7c759f66b058eb2dceb8a67a648dd4d0a0857bbfd38f51e8b058d18673f1c616)

The full list of tip transactions can be found [here](https://etherscan.io/token/0x6b175474e89094c44da98b954eedeac495271d0f?a=0x7a1057e6e9093da9c1d4c1d049609b6889fc4c67)

Some have questioned why this option of returning the claim as a 100% tip was made available, when it could have been capped at 10 or 20%.

Interestingly, those who benefitted the most from the refund left the smallest percentage of tips relative to their claim.
![](https://lh5.googleusercontent.com/w3CD80RlDF-F-FnDBUlO5UdU0pEm4X5tgy87FpLXyBGXXQInQ4_9A9op0xp8bTaPrNjtLaAkGDe8G1AhR61qyW-YuGJUXCW_JDyCXM6xsNKh47TGPCimBoez_F1dqVcwc7rr-0Xs)Greedy whales...
Here are some more figures on the DAI claims and donations through youreminence.finance, courtesy of Alphaleakers.
![](https://lh6.googleusercontent.com/goJyvxqXCAg8kCYnCZj5di0wvRE5I4BtroyTdY3GK88wyX67fJ4rAoWSPkTtXVa_CQ5Lo7Oba2kS0K_t8AHtvgoAkLBzKv8wHk_OIk3T4UOr1ux3SSsYBpjcAOzmoE-0ZRYq6kG4)
rektHQ is by and for the community. We’re very grateful for the community members who have reached out to us in recent days offering their knowledge and support.
We are here to present your stories and opinions, we will protect your identity and promote your story, placing honesty and accuracy above all else.

The following opinion pieces are from anonymous community members. rektHQ has a lot of respect for those who have contributed their thoughts and information to today’s article. Our inbox remains open and anonymous for anyone who wishes to contact us.

_As always, rektHQ takes no responsibility for the content or opinions presented in this newsletter._

---

**ANON 1**

I'm not a fan of the $8M refund from two perspectives.

Firstly because of the threats made to Andre in the lead up to him asking the yearn treasury to assist with refunding the $8M. I haven't seen the nature of the threats but going through with the refund sets a very dangerous precedence where it reinforces the notion that threatening project members is a viable course of action to get your desired outcome.

The second perspective is obviously the moral hazard aspect which has been discussed at length already on CT. Austrian economists love to use the term “moral hazard” when describing interventionism, which in DeFi layman's terms refers to degens degen'ing on more and more risky and unaudited projects because they 'expect' to be partially bailed out in situations such as these. This type of risk transfer certainly exists in the real world where major banks have an expectation for the federal government to bail them out if they land on hard times. But do we really want to replicate this in the DeFi space?

Whoever exploited EMN displayed great initiative and ingenuity, but more importantly he/she essentially shared a blueprint on how to carry out a simple yet lucrative attack and divert attention back to the very project that they attacked, letting them take on all the misguided anger and threats. We may even start seeing this become the new norm for exploiters to tip the systems they've just gamed, akin to an unspoken code of conduct among thieves.

Wherever this latest incident takes us in the coming weeks, it's worth considering the message it's sending out to all the bad actors in this space or even the neutral ethically-fluid ones watching these perpetrators get away with it, time after time, with absolute impunity.

**ANON 2**

On the technical side, I think the implementation was a bit unfleshed out as it was deployed on testnet first.

Admittedly it's still relatively hard to fork mainnet and run locally to have uniswap, balancer or bonding curve testing so I can understand the “test as much as possible” but real testing happens in prod...

However that narrative opens the ground for shit developers and scammers, which given the amount of “Uniswap” rug pulls recently is awful.

I mean in hindsight it was *and* wasn't Andre's fault, considering there is so much hype around him that it was even a plausible idea that it could have happened.

I mean there's only so much you can cognitively think about when developing, you're more focused on the project roadmap rather than these extra degen defi risks that admittedly are still emerging.

Team or not working behind this, it'd still be the same issue

I guess the timing was a bit messed up re: communications, people like to not keep so many communication lines especially with how many new devs have joined the[ $](https://twitter.com/search?q=%24yFi&src=cashtag_click)YFI community...

Andre retweeted the photo then people started to create a conspiracy about surprising everyone.

Personally I was under that impression too, it's just crypto culture being so twisted, people like puzzles and anonymity, quite to its own detriment but that's my bias.

Refund wise, it shows that the project will still be continued in good faith.

It also shows that there is a human touch to all of these high TVL degen actions.

People risk a lot in general, it doesn't matter what space or asset class.

You can't fault people for returning an exploiter's funds to those[ #halfrekt](https://twitter.com/hashtag/halfrekt?src=hashtag_click), just as much as you can't fault the exploiter for returning half the funds in the first place.

I'm technically not on Andre's level and had a hunch that this could have been rug pulled before going to sleep but really, it was just a whole narrative of chance.

Everyone just really needs to sleep more.
