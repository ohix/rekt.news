---
title: yCredit the Ape
date: 01/03/2021
tags:
  - ycredit
  - Cronje
  - interview
excerpt: Cronje doesn’t build for speculators, yet his new code seems to be used for speculation and nothing else. The Cronje audit process sees him throw unfinished products to the apes, who gladly feast on whatever token is thrown their way.
banner: https://lh6.googleusercontent.com/sv-PN0hSY1Cgjid_grLz74bTXRSJHL7aLHjDvD4Kgbk_r-_d6QH_EIohZEqQ1bcXwtfsm4mNktsgh-FMrcQaSq-oTIlZ2evVgheMT2gnu6rdOGJAYkYd1lizbnz9d8AdqBZWp3im
---

![](https://lh6.googleusercontent.com/sv-PN0hSY1Cgjid_grLz74bTXRSJHL7aLHjDvD4Kgbk_r-_d6QH_EIohZEqQ1bcXwtfsm4mNktsgh-FMrcQaSq-oTIlZ2evVgheMT2gnu6rdOGJAYkYd1lizbnz9d8AdqBZWp3im)
**Why credit the ape?**

If contracts are known to be vulnerable, why release them to the public?

**Does the deployer care about their users?**

If they do, why deploy the contracts?

If they don’t, why try to get people to withdraw?

**In his own [words](https://andrecronje.medium.com/unpacking-my-involvement-in-defi-cdb6479e337d), Cronje doesn’t build for speculators, yet new Cronje code seems to be used for speculation and nothing else.**

**The Cronje audit process sees him throw unfinished products to the apes, who gladly feast on whatever token is thrown their way.**

Perhaps he doesn’t build for speculators, but he certainly relies on them to test his work.

**Both black and white hats look down on their behaviour, but if apes didn’t ape, there would be no clout to chase, and there’s no better way to crowdsource your audits…**

On the 1st January, Cronje [announced](https://andrecronje.medium.com/tokenized-yield-credit-via-ycredit-48330f312d2) the launch of tokenised yield credit via [yCredit](https://ycredit.finance/). As he no longer uses Twitter, this announcement was made with little fuss via a Medium post.

**However, this didn’t stop the usual Andre Ape Army Activity, and ~$45k quickly flowed into the contracts.**

When Nour Haridy made a public announcement on Twitter, warning people to withdraw from the contracts, he was [accused](https://twitter.com/0xdeadf4ce/status/1345388627694661632?s=20) of clout chasing, and abandoning [responsible disclosure](https://en.m.wikipedia.org/wiki/Responsible_disclosure#:~:text=In%20computer%20security%20or%20elsewhere,the%20model%20from%20full%20disclosure%E2%80%A6.) in exchange for self-promotion.

**Everybody wants to be seen in a white hat, but how many wear them when no one is looking?**

We spoke to Nour to find out.

---

**rekt:**

_Hi Nour, sorry for the delay, are you free to talk?_

**Nour:**

I can talk today.

**rekt:**

_Did you contact the yearn team before your public announcement?_

**Nour:**

I contacted Andre, Yearn has nothing to do with yCredit according to Andre.

They also didn’t know anything about it.

**rekt:**

_Why did you feel a public announcement was necessary?_

**Nour:**

Because otherwise there was going to be no response, because the contract was not publicly announced.

**rekt:**

_Do you consider your announcement to be responsible disclosure?_

**Nour:**

I consider it the most responsible disclosure available, since the only other option was doing nothing.

**rekt:**

_Andre was not going to do anything?_

**Nour:**

You should ask him that question not me.

All I know is that the contract was only meant to be used by him.

Therefore he had no reason to tell anyone there’s a bug.

**rekt:**

_If he was going to do something, why would you make the announcement?_

**Nour:**

You’re right. I wouldn’t.

**rekt:**

_Did you tell Andre you were going to announce the vulnerability?_

**Nour:**

Yup.

He said I’m free to do so if I want to.

**rekt:**

_Could you prove that?_

**Nour:**

Nope.

Not without screenshotting our chats. Which I can’t do without his permission.

**rekt:**

_After your announcement, the attack vector you pointed out was exploited, as well as a different vector which you did not announce._

_If you could repeat the events, would you do anything differently?_

**Nour:**

It's also worth mentioning that hundreds of thousands were in fact withdrawn after. However, I would alert the Yearn guys in addition to Andre. Which btw I did suggest but I was told they had no affiliation with yCredit.

The fact is I did responsibly disclose.

Yearn team never knew anything about yCredit before or after it was released.

**rekt:**

_Do you think Andre should have done anything differently?_

**Nour:**

I think a deposit cap would be helpful to cap potential risk.

But other than that he did say it can be economically exploited.

He did not share the contract address or invite anyone to use it.

He didn’t launch a UI.

I personally would share the source code with other devs to review first. But these are different styles. Maybe he did also

**rekt:**

_[https://ycredit.finance](https://ycredit.finance)?_

**Nour:**

That’s connected to the older contract

scUSD

**rekt:**

_Your tweet got a lot of attention, and you were accused by some of "clout chasing"._

_Did you view this as an opportunity for self-promotion?_

**Nour:**

Sure

I chose self-promotion over using the exploit myself.

I think that’s a pretty good deal for those who were able to withdraw.

I'm pretty sure if I used the exploit everyone would just blame the apes who put their money in instead of me.

But yeah I wouldn’t have done that anyway.

Maybe I would’ve done it if only Andre’s funds were there so I could just send them back to his address for fun.

**rekt:**

_Do you think Andre uses this "test in prod" approach as a cheaper / decentralised audit technique?_

**Nour:**

Yep both of us do.

I did it with Inverse, only difference was deposit cap.

**rekt:**

_Thanks for your time Nour, do you have anything you'd like to say to our readers?_

**Nour:**

I just wanna say that their money isn’t any more safe on any other audited contract than it could be on yCredit.

Aave barely dodged burning a billion $ last month in a faulty (audited) upgrade.

Audits really are a meme.

The only viable proof of security is on-chain battle testing measured by potential attacker profit over time. So don’t yell audits and unit tests etc at Andre, his way really is the only way, especially when it comes to economic vulnerabilities.

The guy never invited anyone to test in prod for him anyway. He was testing using his own money. So you’re not entitled to anything if you participate, including a vulnerability response or disclosures.

Thanks for the interview.

---

**\*editor's note\*** **- Despite having already made a public announcement, Nour initially refused to share the exploit details with rekt OPSEC, stating that he wanted to wait until there were zero funds in the contract.**

**This slowed our investigation and meant we were unable to take action before the inevitable hacks.**

---

**ySwap Contracts**

**Stable AMM:** 0x5cB5e2d7Ab9Fd32021dF8F1D3E5269bD437Ec3Bf

**Exchange Router**: 0xDD05437d7c7aF576b58262AE5ac6D37515168BE3

**Swap Factory:** 0x3A4FF19554b0F997A4cEF14A8860DcF813b738a4

**Redeployed:** 0x71b6296174c5f07d37cafd6e9b72ab5bb3f14fac

[**Banteg analysis**](https://github.com/banteg/exploit-ycredit)

---

![](https://lh3.googleusercontent.com/Excpd2s-dUx0Kh2tpgzAYN8I6l3gEPSDyLfaYAl4EdwDPQGjZDY8HJtJIwDpYlYkgbn-q15GGEl7g3UZ5sDBBp_thwP1anSdO283bELkfAkju-BpOTS26V2_IHCcnFpmkguZNHjA)

> _**Who the fuck is Nour** to decide a single "nah, shouldn't be used anyway" is a reason to basically do a public invitation to rekt people and also essentially discredit Andre for the sake of pumping his own clout._
>
> _**This is not the way responsible disclosure is done.** Did you get in touch with the team? If you didn't, why not? If you did, why the PSA? You're literally calling for the attention of every black hat not sleeping this way._
>
> _I legit tried to go for some more info as to why or how this is not handled in a responsible manner and he was basically just like "lol, whadda ya want". At that point I didn't see much sense in communicating with this guy and just hoped DeFi police would show up._
>
> _It is not that you wouldn't know who to ask privately if you're paying at least a minimum of attention. Yet he decided to pull some sort of publicity stunt._
>
> _**Apart from that... warnings were given, no blame for Andre. Yet he's hiding again and I honestly feel sorry for him.** Sure it is debatable whether this test in prod stuff shouldn't be a little more fenced against apes. I think he's s very sensible person and stupid clout chasing like this might very well be the reason we lose one of the most ingenious builders at some point._
>
> _If people only interacted via Etherscan then fuck them._
>
> _Take ownership of your actions and take ownership of your losses._

---

**It seems this contract has served its purpose.**

Another lesson to the apes, who live but don’t learn.

**At least apes have their purpose; the ignorance of others is a tool for some.**

The contract has been redeployed, clout and cash has been redistributed, and we move on.

**Our inbox is always open...**
