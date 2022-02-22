---
title: Cream Finance - REKT 2
date: 10/28/2021
rekt:
  amount: 130000000
  audit:  Unaudited
  date: 10/27/2021
tags:
  - Cream
  - Yearn
  - REKT
excerpt: Cream Finance wurde (erneut) für ~130 Millionen US-Dollar gehackt. Das dezentralisierte Monopol von Yearn Finance ist zu groß geworden. Warum so viele Protokolle anhäufen, wenn man sich nicht um deren Nutzer kümmert?
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/10/cream2-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/10/cream2-header.png)

**Ein weiteres gescheitertes Experiment aus dem Yearn Finance-Ökosystem.**

**Cream Finance wurde _([erneut](https://rekt.news/cream-rekt/))_ für ~130 Millionen US-Dollar gehackt.**

Das [dezentrale Monopol](https://rekt.news/decentralised-monopoly/) von Yearn Finance ist zu groß geworden, und seine Betreiber; zu sorglos.

_Warum so viele Protokolle anhäufen, wenn man sich nicht um deren Nutzer kümmert?_

Wir gingen davon aus, dass nach der Reihe aggressiver Übernahmen durch Yearn im Jahr 2020 die Sicherheit auf diesen Plattformen verbessert würde.

_Das war jedoch eindeutig nicht das Ziel._

Die [CoinGecko Yearn Ökosystem Seite](https://www.coingecko.com/en/categories/yearn-yfi-partnerships-mergers?__cf_chl_captcha_tk__=OPpx03zypJXPB4a8bKf354z2Zvl2TO7NF6bMRogkBh4-1635437847-0-gaNycGzNByU) zeigt die Preisauswirkungen dieses Hacks.

>Das ist Platz drei auf unserer Rangliste, der zweite Eintrag für das Cream Finance-Protokoll und **insgesamt zehn Positionen für das Yearn Ökosystem**.

Während die Yearn-Entwickler weiterhin [schnelle](https://medium.com/@geistfantom/pre-launch-announcement-geist-finance-fbfb938afd2f) [Forks](https://twitter.com/The3D_/status/1452779577739202569?s=20) von anderen Plattformen erstellen und den Nutzern Anreize zur Verwendung von Chains bieten, die zu ihren Gunsten funktionieren, [missbrauchen sie die Entwickler](https://twitter.com/bantg/status/1453678280914128900?s=20), die am ursprünglichen Code gearbeitet haben, und setzen die Gelder anderer Nutzer aufs Spiel.

**Das soll nicht heißen, dass Yearn versucht, seine Nutzer auszutricksen – alle DeFi-Degenerierten sind sich der Risiken bewusst, aber wir können diese Bilanz nicht ignorieren.**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/10/cream2-leaderboard.png)

**Geschäft ist Geschäft, ob on-Chain oder off-Chain.**

**Einige dieser Protokolle wurden nach dem Hack aufgegriffen, aber wer hatte das größte Motiv für das Scheitern dieser Yearn-Konkurrenten?**

**Es war ein klarer Vorteil für Yearn, dass sie in der Lage waren, eine solche Reihe von Protokollen zu verknüpfen und zu nutzen, aber mit großer Macht geht auch große Verantwortung einher...**

_Wer trägt die Schuld am Verlust von 130 Millionen US-Dollar?_

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/10/cream2-investigates.png)

> _Quelle: [@Mudit__Gupta](https://twitter.com/Mudit__Gupta/status/1453401698563596293) und [@cryptofishx](https://twitter.com/cryptofishx/status/1453425047108927488?t=M6S6eaD0LPtB9fxqIsXQmQ&s=19)_

**Exploiter Wallets:**

[Adresse A](https://etherscan.io/address/0x961d2b694d9097f35cfffa363ef98823928a330d), [Adresse B](https://etherscan.io/address/0x24354d31bc9d90f62fe5f2454709c32049cf866b)

**Der Hacker war in der Lage, eine Schwachstelle der Preiskalkulation auszunutzen, indem er wiederholt Flash-Loans über zwei Adressen auslieh und verlieh.**

Nachdem er mit yUSDVault besicherte crYUSD angehäuft hatte, wurde der Preis des zugrunde liegenden yUSDVault-Tokens manipuliert, um den Wert der Sicherheiten im Besitz des Angreifers effektiv zu verdoppeln.

Mit den nun überbewerteten Sicherheiten hat der Angreifer schließlich so viele Assets wie möglich aus CREAMs Vaults entwendet.

Eine vollständige Tabelle der gestohlenen Gelder, darunter mehr als 2760 ETH, insgesamt 76 BTC in renBTC, WBTC und HBTC sowie mehrere zig Millionen in Stablecoins und anderen Tokens, findest du [hier](https://twitter.com/SlowMist_Team/status/1453398034151194627?t=EjgoIA992F938Hoc1oyBVw&s=19).

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png)

**Über die Adresse A nahm der Angreifer ein Flash-Darlehen in Höhe von 500 Mio. DAI von MakerDAO auf und zahlte diese in den yPool von Curve für yDAI ein, die dann zum minten von yUSD verwendet wurden. Die yUSD wurden dann in die yUSD-Strategie von Yearn eingezahlt.**

Durch die Verwendung der yUSDVault-Tokens von Yearn als Sicherheit für CREAM konnte der Angreifer anschliessend ~500 Millionen crYUSD minten.

Mit Adresse B nahm der Hacker dann einen Flash-Loan von AAVE im Wert von 2 Milliarden US-Dollar in ETH auf, um ihn als Sicherheit auf CREAM zu verwenden. Dies ermöglichte das Ausleihen von weiteren ~500 Millionen US-Dollar, die erneut eingezahlt wurden, um crYUSD zu mint.

Die beiden Konten führten dann eine Schleife von Einzahlungen und Krediten durch, wobei B jedes Mal ~$500 Millionen in yUSDVault-Tokens an A überwies, bis Konto A im Besitz von ~1,5 Milliarden US-Dollar in crYUSD und ~500 Millionen US-Dollar in yUSDVault war.

Der Angreifer nutzte dann eine Schwachstelle in CREAMs internem PriceOracleProxy von yUSDVault-Tokens aus. Der Preis von yUSDVault hängt von seinem Preis pro Anteil ab, der durch das yUSD-Guthaben / totalSupply yUSDVault des Vaults definiert wird.

Indem er ~500 Millionen US-Dollar yUSDVault für den zugrunde liegenden yUSD einlöste, konnte der Angreifer den Gesamtvorrat des Vaults auf nur 8 Millionen US-Dollar reduzieren. In Kombination mit einer Einzahlung von ~8 Millionen US-Dollar in yUSD in den Vault konnte CREAM den Wert der yUSDVault-Anteile um etwa den Faktor zwei erhöhen.

Aufgrund der Preismanipulation **sieht CREAM bei Adresse A nun 3 Milliarden US-Dollar crYUSD an Sicherheiten**. Davon wurden 2 Milliarden US-Doller in ETH abgehoben, um den Flash-Loan von B zurückzuzahlen, während die ~500 Millionen US-Dollar an yUSD, die aus dem yUSDVault zurückgezahlt wurden, das DAI-Darlehen von A zurückzahlen.

**Die 1 Milliarde US-Dollar, die übrig blieben, waren mehr als genug, um die $130M von CREAM, die für die Kreditvergabe zur Verfügung standen, abzuschöpfen (ausleihen und ausfallen lassen).**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png)

**Nach dem Angriff wurden Gelder aus dem [Exploit-Contract](https://etherscan.io/address/0x961d2b694d9097f35cfffa363ef98823928a330d) zurück in [diese Wallet](https://etherscan.io/address/0x24354d31bc9d90f62fe5f2454709c32049cf866b) [gezogen](https://etherscan.io/tx/0xafd29e7918112de30a8c994f19bb503ee9ce717030b0da43a68e2bd9ae25f86a), die etwa 30 Minuten vor dem Angriff in zwei Transaktionen von Tornado Cash finanziert worden war: [eins](https://etherscan.io/tx/0x753cce254051aae778af6f46e999ed9927cc4d93e5cfb95b23f90ff902d7c090), [zwei](https://etherscan.io/tx/0xaa47963fc4471f81550a830d679c0c14a9ba30d886a8c70ae9653bd78a55b089).**

Seit dem Angriff [nutzt der Hacker die renBridge](https://etherscan.io/tx/0x9fdcfe7ba45d092ac3f819f746fa2000a344861f3cc100fdefc1c0957cdba7a1), um Gelder an BTC zu senden und dem [ETH-CRETH2 Pool](https://info.uniswap.org/#/tokens/0xcbc1065255cbc3ab41a6868c22d1f1c573ab89fd) von Uniswap über 40 Millionen US-Dollar an CRETH2 an einseitiger Liquidität [hinzuzufügen](https://etherscan.io/tx/0xc79559d42a4c25c92ca8511c3dd5dfcdd41f0382e1f7577abc7224c5ae8ac343), vermutlich in dem Versuch, so viel wie möglich abzuladen da CRETH2 eventuell noch [verwertbar sein könnte](https://twitter.com/adamscochran/status/1453382363753459714).

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/10/cream2-whatnow.png)

**Der Cream.Finance: Deployer ist einer der [vielen Accounts](https://pentacle.xyz/bad-things-cream), die versucht haben, mit dem Hacker zu kommunizieren.**

[Ihre Nachricht](https://etherscan.io/tx/0x606bdd12584ccda8a3ecdb9e4bd43046d066d2b223d857121eec51820f34cc89);

>_du gewinnst. wir sind rekt. Bitte gib uns das Geld zurück und wir werden eine Prämie von 10% auszahlen._

Wenn erfahrene Angreifer solche Schritte unternehmen, sind die Motive nicht nur finanzieller Natur.

Dies ist sowohl eine Manipulation der Branche als auch der Märkte, und wir müssen uns überlegen, wer davon profitiert.

Andere Protokolle wurden in einer mysteriösen Nachricht in den [Eingabedaten der Haupttransaktion des Exploits](https://etherscan.io/tx/0x0fe2542079644e107cbf13690eb9c2c65963ccb79089ff96bfaf8dced2331c92) genannt;

> _gÃTµ Baave lucky, iron bank lucky, cream not. ydev : incest bad, dont do_

In [Mudit Guptas](https://twitter.com/Mudit__Gupta/status/1453417777599901702) [_Beobachtungen und Theorien_](https://mudit.blog/cream-hack-analysis/) über den Angriff weist er auf mehrere Gründe hin, warum er glaubt, dass der Hacker (oder die Hacker) erfahrene DeFi-Entwickler sind, und dass es sich nicht um den durchschnittlichen Black-Hat-Angriff handelt.

**Dieser Hack enthüllte nicht nur Schwachstellen im Projektcode, sondern auch tiefere Rivalitäten, die für den durchschnittlichen DeFi-Nutzer möglicherweise nicht offensichtlich waren.**

_Ein einst verborgener Krieg wird nun öffentlich ausgetragen._

Ein 130-Millionen-US-Dollar-Hack sorgt für Schlagzeilen, aber für viele wird dieser Angriff nicht wegen des Verlustes in Erinnerung bleiben, sondern wegen der Art und Weise, wie er von den gegnerischen Teams als Wahlkampfmittel eingesetzt wurde, von denen keines als Sieger hervorging.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/rekt-outline-conc.png)
