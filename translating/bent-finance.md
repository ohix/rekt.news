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
excerpt: Wer hat bei Bent Finance die Regeln verbogen? ~1,75 Millionen USD gestohlen. Kommissar rekt bringt Ordnung.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/bent-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/bent-header.png)
**Ein weiteres Projekt krumm gebogen.**

Diesmal, so scheint es, aufgrund eines strukturellen Versagens von innen.

[Bent Finance](https://app.bentfinance.com/) ist eine „staking- und farming-Plattform zur Verbesserung Ihrer curve-Renditen“.

**In den letzten Wochen hat eine Adresse die Regeln des Protokolls verbogen und ~1,75 Millionen Dollar extrahiert, bevor alles wieder gerade gebogen wurden.**

Als die Nachricht bekannt wurde und der Preis von [$BENT](https://www.coingecko.com/en/coins/bent-finance) einknickte, gab das Team eine lauwarme [Warnung](https://twitter.com/BENT_Finance/status/1473109745942687745) heraus, in der es die Benutzer darüber informierte, dass die Belohnungen ausgesetzt wurden, _aber kein Geld verloren gegangen war_.

**Als PeckShield jedoch [behauptete](https://twitter.com/peckshield/status/1473175071560994816), den Exploit als von innen kommend identifiziert zu haben...**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/bent-peckshield.png)

**...das Team war gezwungen, ein [Update](https://twitter.com/BENT_Finance/status/1473188374492053505) zu veröffentlichen, das als Vorwurf eines Insider-Jobs interpretiert werden könnte:**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/bent-tweet.png)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/rekt-investigates-linebreak.png)

_Quelle: [BlockSecTeam](https://twitter.com/BlockSecTeam/status/1473188863136780288?s=20)_

Dieser Fall ist weitaus einfacher als eine technische Smart-Contract-Manipulation.

Der Bent Finance [cvxCRV-Contract](https://etherscan.io/address/0x270b6aff561284ef380cdd6d8b036f4981049a86) wurde am 30. November [aktualisiert](https://etherscan.io/tx/0xf711641ea9814d78780c8a51ad734ad44d58baf3f97256a3f5ec3200a29eadc7), wobei der Saldo der [Adresse](https://etherscan.io/address/0xd23cfffa066f81c7640e3f0dc8bb2958f7686d1f) des Exploiters manuell angepasst wurde.

**Dies wies dem Ausbeuter enorme Belohnungen zu, die selbst die TVL von Bent Finance weit überstiegen.**

**Obwohl der Exploit fast drei Wochen lang aktiv war, wurde das Problem erst mit der jüngsten Notierung von Bent Finance auf der [DeBank](https://twitter.com/DeBankDeFi/status/1473077001267253248) deutlich, als das [Wallet-Profil](https://debank.com/profile/0xd23cfffa066f81c7640e3f0dc8bb2958f7686d1f) des Ausbeuter die ausstehenden Belohnungen im Wert von Milliarden von Dollar auf der Plattform zeigte.**

Wenn wir uns die Token [Transaktionen](https://etherscan.io/tokentxns?a=0xd23cfffa066f81c7640e3f0dc8bb2958f7686d1f) der Hauptgeldbörse ansehen, sehen wir eine Handvoll kleiner Einzahlungen, gefolgt von einigen sehr großen Abhebungen, eine am [12. Dezember](https://etherscan.io/tx/0x11961c4df0b27bd7188d451dd18005dc8aff7ad4a80c7f7441b56495cae219c5) (263.000 cvxcrv-f) und eine weitere [heute](https://etherscan.io/tx/0x52d4d5a9a83ff8ca6a7fd102954c4c5d2658043d9049abfc47cd8c37692b95be) um 02:45 UTC (250.000 cvxcrv-f).

Die Tokens wurden dann an die [sekundäre Adresse](https://etherscan.io/address/0x9e966a54082427d7ac56aeaee4baae7d11a6e468) des Exploiters gesendet, wo sie gegen CRV ausgezahlt, gegen ETH getauscht und an Tornado Cash gesendet wurden.

**Insgesamt wurden zwischen dem 12.12. und heute 440 ETH (~1,75 Millionen USD) über Tornado Cash gewaschen.**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/bent-linebreak.png)

**Die Rolle, die die Notierung von Bent Finance durch die DeBank im heutigen Fall spielte, und Nansens jüngste [Einsammlung von 75 Millionen Dollar](https://www.theblockcrypto.com/post/127747/data-startup-nansen-secures-fresh-funding-at-750-million-valuation) zeigen den Wert, den diese Dienstleistungen für eine immer komplexer werdende Branche bringen.**

Obwohl on-Chain Daten alle notwendigen Informationen für diejenigen liefern, die über das Wissen (und die Motivation) zur Untersuchung verfügen, erhöhen diese Werkzeuge die Wahrscheinlichkeit, Unregelmäßigkeiten in weniger bekannten Projekten zu entdecken, erheblich.

Im Fall von Bent Finance scheint es sich jedoch angesichts der Quelle des Exploits sowie der Reaktion des Teams wahrscheinlich um einen insider Job zu handeln:

_Rug pull oder abtrünniges Teammitglied?_

[Viel](https://rekt.news/ascendex-rekt/) [größere](https://rekt.news/vulcan-forged-rekt/) [Hacks](https://rekt.news/grim-finance-rekt/) haben in letzter Zeit die Schlagzeilen dominiert, und Vorfälle wie dieser werden bald in Vergessenheit geraten.

_Vielleicht rechnet das Bent Finance Team damit..._

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/rekt-outline-conc.png)
