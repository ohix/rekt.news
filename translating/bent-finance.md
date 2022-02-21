---
title: Bent Finance - REKT
date: 12/21/2021
rekt:
  amount: 1750000
  audit: Unaudited 
  date: 12/21/2021
tags:
  - Bent Finance
  - REKT
excerpt: Wer hat bei Bent Finance die Regeln verbogen? ~1,75 Millionen US-Dollar gestohlen. Kommissar rekt bringt Ordnung.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/bent-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/bent-header.png)
**Ein weiteres Projekt krumm gebogen.**

Diesmal, so scheint es, aufgrund eines strukturellen Versagens von innen heraus.

[Bent Finance](https://app.bentfinance.com/) ist eine „staking- und farming-Plattform zur Verbesserung Ihrer curve-Renditen“.

**In den letzten Wochen hat eine Adresse die Regeln des Protokolls verbogen und ~1,75 Millionen US-Dollar extrahiert, bevor alles wieder gerade gebogen wurden.**

Als die Nachricht bekannt wurde und der Preis von [$BENT](https://www.coingecko.com/en/coins/bent-finance) einknickte, gab das Team eine lauwarme [Warnung](https://twitter.com/BENT_Finance/status/1473109745942687745) heraus, in der es die Nutzer darüber informierte, dass die Belohnungen ausgesetzt wurden, _aber keine Gelder verloren gegangen war_.

**Als PeckShield jedoch [behauptete](https://twitter.com/peckshield/status/1473175071560994816), den Exploit als von innen kommend identifiziert zu haben...**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/bent-peckshield.png)

**...sah sich das Team gezwungen, ein [Update](https://twitter.com/BENT_Finance/status/1473188374492053505) zu veröffentlichen, das als Anschuldigung für einen Insider-Job verstanden werden könnte:**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/bent-tweet.png)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/rekt-investigates-linebreak.png)

_Quelle: [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1473188863136780288?s=20)_

Dieser Fall ist weitaus einfacher als eine technische Smart-Contract-Manipulation.

Der Bent Finance [cvxCRV-Contract](https://etherscan.io/address/0x270b6aff561284ef380cdd6d8b036f4981049a86) wurde am 30. November [aktualisiert](https://etherscan.io/tx/0xf711641ea9814d78780c8a51ad734ad44d58baf3f97256a3f5ec3200a29eadc7), wobei der Betrag der [Adresse](https://etherscan.io/address/0xd23cfffa066f81c7640e3f0dc8bb2958f7686d1f) des Exploiters manuell angepasst wurde.

**Dadurch wurden dem Exploiter enorme Summen an Belohnungen zugewiesen, die die TVL von Bent Finance selbst weit übersteigen.**

**Obwohl der Exploit fast drei Wochen lang aktiv war, wurde das Problem erst mit der kürzlichen Auflistung von Bent Finance auf [DeBank](https://twitter.com/DeBankDeFi/status/1473077001267253248) deutlich, als das [Wallet-Profil](https://debank.com/profile/0xd23cfffa066f81c7640e3f0dc8bb2958f7686d1f) des Exploiters die Milliarden von Dollar an ausstehenden Rewards auf der Plattform zeigte.**

Ein Blick auf die [Token-Transaktionen][Transaktionen](https://etherscan.io/tokentxns?a=0xd23cfffa066f81c7640e3f0dc8bb2958f7686d1f) der Haupt-Wallet zeigt eine Handvoll kleiner Einzahlungen, gefolgt von einigen sehr großen Abhebungen, eine am [12. Dezember](https://etherscan.io/tx/0x11961c4df0b27bd7188d451dd18005dc8aff7ad4a80c7f7441b56495cae219c5) (von 263.000 cvxcrv-f) und eine weitere [heute](https://etherscan.io/tx/0x52d4d5a9a83ff8ca6a7fd102954c4c5d2658043d9049abfc47cd8c37692b95be) um 02:45 UTC (von 250.000 cvxcrv-f).

Die Tokens wurden dann an die [sekundäre Adresse](https://etherscan.io/address/0x9e966a54082427d7ac56aeaee4baae7d11a6e468) des Exploiters geschickt, wo sie gegen CRV ausgezahlt, in ETH geswapt und an Tornado Cash geschickt wurden.

**Insgesamt wurden zwischen dem 12.12. und heute 440 ETH (~1,75 Millionen US-Dollar) über Tornado Cash gewaschen.**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/bent-linebreak.png)

**Die Rolle, die DeBank's Auflistung von Bent Finance im heutigen Fall gespielt hat, und Nansen's jüngste [75 Millionen US-Dollar Erhöhung](https://www.theblockcrypto.com/post/127747/data-startup-nansen-secures-fresh-funding-at-750-million-valuation) zeigen den Wert, den diese Dienste für eine zunehmend komplexere Industrie bringen.**

Obwohl on-Chain-Daten denjenigen, die über das Wissen (und die Motivation) verfügen, Nachforschungen anzustellen, alle notwendigen Informationen liefern, erhöhen diese Tools die Wahrscheinlichkeit, Unregelmäßigkeiten bei weniger bekannten Projekten zu erkennen, erheblich.

Im Fall von Bent Finance scheint es sich jedoch angesichts der Quelle des Exploits sowie der Reaktion des Teams wahrscheinlich um einen insider Job zu handeln:

_Rug pull oder abtrünniges Teammitglied?_

[Viel](https://rekt.news/ascendex-rekt/) [größere](https://rekt.news/vulcan-forged-rekt/) [Hacks](https://rekt.news/grim-finance-rekt/) haben in letzter Zeit die Schlagzeilen dominiert, und Vorfälle wie dieser werden bald in Vergessenheit geraten.

_Vielleicht hofft das Bent Finance-Team genau darauf..._

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/rekt-outline-conc.png)
