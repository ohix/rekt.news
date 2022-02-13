---
title: Grim Finance - REKT
date: 12/20/2021
rekt:
  amount: 30000000
  audit: Solidity Finance
  date: 12/18/2021
tags:
  - Grim Finance
  - REKT
excerpt: Fürchte den Sensenmann nicht. Grim Finance ist rekt. 30 Millionen US-Dollar weg; Position 18 auf der Rangliste.

banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/grim-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/grim-header.png)

**Fürchte den Sensenmann nicht.**

_Grim Finance ist rekt._

Der jüngste Eintrag in unserer [Rangliste](https://rekt.news/leaderboard/) (#18) war ein Fork von „_Beefy Finance_“, der automatisch kumulierte LP Tresore auf Fantom anbietet.

Nach dem Angriff wurde hat das Projekt in seiner ersten [Ankündigung](https://twitter.com/financegrim/status/1472357770846519312) ihn als „_Anspruchsvoll_“ bezeichnet, jedoch sind _reentrancy (wiedereintritt)_ Schwachstellen nichts Neues.

**Der Preis von [$GRIM](https://www.coingecko.com/en/coins/grimtoken) fiel nach dem Angriff um 80%.**

[Charge DeFi](https://twitter.com/ChargeDeFi/status/1472136494085296128) verlor 1849 [$CHARGE](https://www.coingecko.com/en/coins/chargedefi-charge) an denselben Angriffsvektor nur wenige Stunden zuvor…

_War das ein Serienangreifer?_

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/rekt-investigates-linebreak.png)

_Quelle: [RugDoc](https://twitter.com/RugDocIO/status/1472293717725913089)_

**Der Angriff nutzte eine _depositFor()_ Funktion aus, die nicht gegen _reentrancy_ geschützt war.**

Dies ermöglichte es dem Hacker, zusätzliche falsche Einzahlungen innerhalb des ersten Anrufs zu wiederholen und seinen Anteil am Tresor erheblich zu erhöhen.

Wie nachfolgend gezeigt, kann der Benutzer das Einzahlungstoken auswählen, in das der Angreifer seinen eigenen Contract eingefügt hat, der die _reentrancy_ Einzahlungsschleifen enthält.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/grim-code.png)

[Beispiel für Transaktion](https://ftmscan.com/tx/0x19315e5b150d0a83e797203bb9c957ec1fa8a6f404f4f761d970cb29a74a5dd6) und Workflow (Quelle: [@k3mmio](https://threadreaderapp.com/thread/1472315936166219777.html)):

**1)** Hole dir einen Flashloan für XXX und YYY Tokens (z.B.: WBTC-FTM)

**2)** Füge SpiritSwap Liquidität hinzu

**3)** Präge SPIRIT-LPs

**4)** Rufe depositFor() in GrimBoostVault mit token==ATTACKER, user==ATTACKER auf

**5)** Nutze token.safeTransferFrom für den wiedereintritt

**6)** goto (4)

**7)** Im letzten Schritt beim Wiedereintritt rufe depositFor() mit token==SPIRIT-LP, user==ATTACKER auf

**8)** Die Menge der geprägten GB-XXX-YYY Tokens wird in jedem Wiedereintritt erhöht

**9)** Der Angreifer hält am Ende eine riesige Menge an GB-XXX-YYY-Tokens

**10**) GB-Token abheben und mehr SPIRIT-LP-Token zurückerhalten

**11**) Entferne die Liquidität und erhalte mehr XXX und YYY Tokens

**12**) Flashloan zurückzahlen

**des Angreifers Adresse:** [0xdefc385d7038f391eb0063c2f7c238cfb55b206c](https://ftmscan.com/address/0xdefc385d7038f391eb0063c2f7c238cfb55b206c)

**Das Team von Grim Finance führt eine laufende Untersuchung durch, die die Bewegungen von Geldern auf den Konten des Angreifers verfolgt, und hat Verbindungen zu verschiedenen CEXs gefunden.**

_Weitere Details gibt es in der Telegrammgruppe [rekt.news](https://t.me/Rekt_HQ)._

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png) 

**Charge DeFi behauptet, sie hätten sich [an Projekte gewandt](https://twitter.com/ChargeDeFi/status/1472223355352895490), die denselben Code verwendeten, um vor der Schwachstelle zu warnen.**

Möglicherweise hatten diese Nachrichten jedoch nicht die gewünschte Wirkung. Ein discord Nutzer versuchte, die Verantwortung für den Angriff zu übernehmen.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/grim-discord.png)

**Wenn man diesen Botschaften Glauben schenken darf, wird zumindest ein Teil der gestohlenen 30 Millionen US-Dollar für wohltätige Zwecke verwendet.**

_Aber es wird ein düsteres Weihnachtsfest für die unwilligen Spender._

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/rekt-outline-conc.png)

